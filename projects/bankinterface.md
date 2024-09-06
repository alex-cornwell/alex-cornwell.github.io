---
layout: project
type: project
image: img/micromouse/micromouse-square.jpg
title: "Bank Account Interface"
date: 2023
published: true
labels:
  - C
summary: "A Bank User-Interface program to manage accounts created by the user that was made during my ICS-212 class."
---

<div class="text-center p-4">
  <img width="200px" src="../img/micromouse/micromouse-robot.png" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-robot-2.jpg" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-circuit.png" class="img-thumbnail" >
</div>

This was a project that allowed the user to interact with a Bank Management Interface. The user is able to create any number of accounts that stores the customers name, account number, and address into the database to be accessed at a later time. The user is also able to delete a certain record, find a certain record, or view all records currently stored in the database. The program also has a debugging mode to monitor functions being called.

Here is part of the code that allows the user to print all records stored in the database:

```
void printAllRecords(struct record *start)
{
    struct record *current;
    current = start;

    if(debugmode == 1)
    {
        printf("\nFunction printAllRecords was called.\n");
        printf("start = %p\n", (void *)start);
    }
 
    if(current == NULL)
        printf("\nNo stored records\n\n");
    else
    {
        while(current != NULL)
        {
            printf("\nAccount #: %d\n", current->accountno);
            printf("Name: %s\n", current->name);
            printf("Address:\n%s\n", current->address);
            current = current->next;
        }
    }
}
```
