# CPP-Program-to-find-roots-of-a-quadratic-equation

Program to find roots of a quadratic equation in C++
Here we will discuss how to find the roots of a quadratic equation using the C++ programming language. An equation is said to be a quadratic equation if it’s in the form, ax^2+bx+c = 0 (where a!= 0).

 

Roots of a quadratic equation in C++
Algorithm
Let’s see how the code works:

The discriminant is found, d = b*b – 4*a*c
If d is greater than 0, real and different roots are found, root1 = (-b + sqrt(d)) / (2*a) and root2 = (-b – sqrt(d)) / (2*a);
If d is less than 0, complex(imaginary) roots are found, real = -b/(2*a) and imaginary =sqrt(-d)/(2*a);
If d is equal to 0 then real and equal roots are found, root1 = (-b + sqrt(d)) / (2*a);
Related Pages
Finding Number of times x digit occurs in a given input
 
Finding number of integers which has exactly x divisors
 
Power of a Number 

Prime Number

Largest element in an array

Code to find the roots of a quadratic equation in C++
Run
/* Write a program to find roots of a quadratic equation in C++*/
#include <bits/stdc++.h>
using namespace std;
 
void findRoots(int a, int b, int c)
{
    if (a == 0) {
        cout << "Invalid"; return; } int d = b * b - 4 * a * c; double sqrt_val = sqrt(abs(d)); if (d > 0) {
        cout << "Roots are real and different \n";
        cout << (double)(-b + sqrt_val) / (2 * a) << "\n"<< (double)(-b - sqrt_val) / (2 * a);
    }
    else if (d == 0) {
        cout << "Roots are real and same \n";
        cout << -(double)b / (2 * a);
    }
    else // d < 0
    {
        cout << "Roots are complex \n";
        cout << -(double)b / (2 * a) << " + i" << sqrt_val<< "\n" << -(double)b / (2 * a) << " - i" << sqrt_val;
    }
}
 
// Driver code
int main()
{
    int a = 1, b = 4, c = 4;
   
    findRoots(a, b, c);
    return 0;
}
Output :
Roots are real and same 
-2.000000
