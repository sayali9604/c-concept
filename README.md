This repository contains practical examples and projects showcasing key C++ concepts with a focus on Object-Oriented Programming (OOP). It covers:

Classes and Objects: Demonstrates how to create and use classes with constructors and destructors.
Encapsulation: Using access specifiers to control data visibility (public, private, protected).
Inheritance: Shows examples of single and multiple inheritance.
Polymorphism: Illustrates method overloading and virtual functions for dynamic behavior.
Abstraction: Implements abstract classes and interfaces.
File Handling: Examples of reading and writing files using C++ file streams.
Exception Handling: Handling errors with try-catch blocks.
STL: Using containers like vectors and lists for data management.


#include <stdio.h>
struct Complex {
    int  real;
    int imaginary;

Complex()
{
    this->real=0;
    this->imaginary=0;
    printf("\n \ndefault constructor called:Real=%d,Imaginary=%d",this->real,this->imaginary);
}
Complex(int real,int imaginary)
{
    this->real=real;
    this->imaginary=imaginary;
    printf("\n\n parameterise constructor called:Real=%d,Imaginary=%d",this->real,this->imaginary);
}
void setReal(int real)
    {
    this->real=real;
    // printf("\n setreal=Real=%d",this->real);
}
int getReal()
{
    return this->real;
}

void setImaginary(int imaginary)
{
    this->imaginary=imaginary;
    // printf("\n setImaginary=imaginary=%d",this->imaginary);
}
int getImaginary()
{
    return this->imaginary;
}
void display()
{
    printf("\n \nReal=%d,Imaginary=%d",this->real,this->imaginary);
}

Complex add(Complex c2)
{
Complex c3;
c3.real= this->real+c2.real;
c3.imaginary=this->imaginary+c2.imaginary;
return c3;
}
Complex add(int a)
{
    Complex c3;
    c3.real=this->real+a;
    c3.imaginary=this->imaginary+a;
    return c3;
}
Complex sub(Complex c2)
{
Complex c6;
c6.real= this->real-c2.real;
c6.imaginary=this->imaginary-c2.imaginary;
return c6;
}
Complex sub(int a)
{
    Complex c6;
    c6.real=this->real-a;
    c6.imaginary=this->imaginary-a;
    return c6;
}
Complex multi(Complex c2)
{
Complex c9;
c9.real= this->real*c2.real;
c9.imaginary=this->imaginary*c2.imaginary;
return c9;
}
Complex multi(int a)
{
    Complex c9;
    c9.real=this->real*a;
    c9.imaginary=this->imaginary*a;
    return c9;
}

Complex div(Complex c2)
{
Complex c12;
c12.real= this->real/c2.real;
c12.imaginary=this->imaginary/c2.imaginary;
return c12;
}
Complex div(int a)
{
    Complex c12;
    c12.real=this->real/a;
    c12.imaginary=this->imaginary/a;
    return c12;
}

};


Complex add(int a,Complex c1)
{
    printf("\n addition");
    Complex c3;
    c3.real=c1.real+a;
    c3.imaginary=c1.imaginary+a;
    return c3;
 
}
Complex sub(int a,Complex c1)
{
    printf("\n substraction");
    Complex c6;
    c6.real=c1.real-a;
    c6.imaginary=c1.imaginary-a;
    return c6;    
}
Complex multi(int a,Complex c1)
{
    printf("\n multiplication");
    Complex c9;
    c9.real=c1.real*a;
    c9.imaginary=c1.imaginary*a;
    return c9;  
}
Complex div(int a,Complex c1)
{
    printf("\n Division");
    Complex c12;
    c12.real=c1.real/a;
    c12.imaginary=c1.imaginary/a;
    return c12;  
}


int main()
{
    struct Complex c1(10,20);
   struct  Complex c2(5,5);
// addition
    Complex c3=c1.add(c2);
   
    int a=10;
    Complex c4=c1.add(a);
    c4.display();

    Complex c5=add(a,c1);
    c5.display();

// substraction
    Complex c6=c1.sub(c2);

    Complex c7=c1.sub(a);
    c7.display();

    Complex c8=sub(a,c1);
    c8.display();

// Mlutipliication
 Complex c9=c1.multi(c2);

Complex c10=c1.multi(a);
    c10.display();

Complex c11=multi(a,c1);
    c11.display();

// division
Complex c12=c1.div(c2);

Complex c13=c1.div(a);
    c13.display();

Complex c14=div(a,c1);
    c14.display();


    return 0;
}
