# Half Diamond Star Pattern in Java

## Overview
This Java program generates a **Half Diamond Star Pattern**, which consists of an increasing half-pyramid followed by a decreasing half-pyramid. The pattern is symmetric and takes user input for customization.

Example output for `n = 5`:
```
*
**
***
****
*****
******
*****
****
***
**
*
```

## Program Explanation

### 1. Package Declaration
```java
package star_patterns;
```
This declares the package name `star_patterns`, which helps in organizing Java files.

### 2. Importing Scanner Class
```java
import java.util.Scanner;
```
The `Scanner` class is imported from the `java.util` package to take input from the user.

### 3. Class Declaration
```java
public class Half_Diamond_Pattern
```
Defines a class named `Half_Diamond_Pattern` which contains the `main` method.

### 4. Scanner Input
```java
Scanner s = new Scanner(System.in);
System.out.println("Enter the size");
int n = s.nextInt();
```
- Creates a `Scanner` object `s` to take input from the user.
- Asks the user to enter the size of the pattern.
- Stores the input value in the integer variable `n`.

### 5. First Loop - Increasing Half Pyramid
```java
for(int i = 0; i <= n; i++)
```
- Outer loop runs from `0` to `n`.
- Controls the number of rows in the first half.

```java
for(int j = 1; j <= i; j++)
```
- Inner loop runs from `1` to `i`.
- Prints `*` in each row, increasing as `i` increases.

```java
System.out.print("*");
```
- Prints `*` without moving to a new line.

```java
System.out.println();
```
- Moves to the next line after printing stars for the current row.

### 6. Second Loop - Decreasing Half Pyramid
```java
for(int i = 0; i <= n; i++)
```
- Outer loop runs from `0` to `n`.
- Controls the number of rows in the second half.

```java
for(int j = i; j <= n; j++)
```
- Inner loop prints decreasing `*` as `i` increases.

```java
System.out.print("*");
```
- Prints `*` without moving to a new line.

```java
System.out.println();
```
- Moves to the next line after printing stars for the current row.

### 7. Closing Scanner
```java
s.close();
```
- Closes the `Scanner` to prevent resource leaks.

## Full Java Code
```java
package star_patterns;

import java.util.Scanner;

public class Half_Diamond_Pattern
{
    public static void main(String[] args)
    {
        Scanner s = new Scanner(System.in);
        System.out.println("Enter the size");
        int n = s.nextInt();
        
        for(int i = 0; i <= n; i++)
        {
            for(int j = 1; j <= i; j++)
            {
                System.out.print("*");
            }
            System.out.println();
        }
        
        for(int i = 0; i <= n; i++)
        {
            for(int j = i; j <= n; j++)
            {
                System.out.print("*");
            }
            System.out.println();
        }
        
        s.close();
    }
}
```

## Key Learnings
- Understanding nested loops for pattern printing.
- Using `Scanner` for user input.
- Practicing Java syntax and control structures.

## Clone
```
git clone https://github.com/Ananthadatta02/Java-Half_Diamond_pattern.git
```
