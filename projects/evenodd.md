---
layout: project
type: project
image: img/evenodd.png
title: "Even or Odd"
date: 2023
published: true
labels:
  - C++
summary: "A simple interface program that lists all numbers up to a maximum as either even or odd. this was made during my ICS-212 class."
---

This is a simple interface program that asks the user to input the maximum numbers to check and prints every integer as either even or odd. There is also checks to make sure the user inputs a positive integer greater than 0.

Here is part of the code that asks for user input:

```
int user_interface()

{
    int input, valueToPass;

    std::cout << "\nThis program takes a user inputted integer and displays each value as even or odd\n" << std::endl;
    std::cout << "Enter maximum number to show: ";
    while(((std::cin >> input).fail() || input < 0 || std::cin.peek() != '\n')) 
    {
        std::cin.clear();
        while(std::cin.get() != '\n');
        std::cout << "invalid input, please enter a positive integer: ";
    }  
    std::cout << "\n";
    valueToPass = input;           
 
    return valueToPass;
}
```
