STRUCTURE STUDENT


#include <iostream>
using namespace std;

struct Student
{
    string name;
    int roll;
    float marks;
};

int main()
{
    Student s;

    cout << "Enter name: ";
    cin >> s.name;

    cout << "Enter roll number: ";
    cin >> s.roll;

    cout << "Enter marks: ";
    cin >> s.marks;

    cout << "\nStudent Details";
    cout << "\nName: " << s.name;
    cout << "\nRoll Number: " << s.roll;
    cout << "\nMarks: " << s.marks;

    return 0;
}


CLASS EMPLOYEE 


#include <iostream>
using namespace std;

class Employee
{
    int id;
    string name;
    float salary;

public:
    void getData()
    {
        cout << "Enter ID, name and salary: ";
        cin >> id >> name >> salary;
    }

    void display()
    {
        if(salary > 10000)
        {
            cout << "\nID: " << id;
            cout << "\nName: " << name;
            cout << "\nSalary: " << salary;
        }
    }
};

int main()
{
    Employee e[3];

    for(int i = 0; i < 3; i++)
    {
        e[i].getData();
    }

    cout << "\nEmployees with salary above 10000:";

    for(int i = 0; i < 3; i++)
    {
        e[i].display();
    }

    return 0;
}


SINGLE INHERITANCE: VEHICLE & CAR


#include <iostream>
using namespace std;

class Vehicle
{
public:
    void showVehicle()
    {
        cout << "This is a Vehicle" << endl;
    }
};

class Car : public Vehicle
{
public:
    void showCar()
    {
        cout << "This is a Car";
    }
};

int main()
{
    Car c;

    c.showVehicle();
    c.showCar();

    return 0;
}


EXCEPTION HANDLING: MARKS GREATER THAN 100


#include <iostream>
using namespace std;

int main()
{
    int marks;

    cout << "Enter marks: ";
    cin >> marks;

    try
    {
        if(marks > 100)
        {
            throw marks;
        }

        cout << "Valid Marks";
    }
    catch(int x)
    {
        cout << "Exception: Marks cannot be greater than 100";
    }

    return 0;
}


FILE HANDLING: CREATE college.txt

 
#include <iostream>
#include <fstream>
using namespace std;

int main()
{
    ofstream file("college.txt");

    file << "St John College of Engineering and Management";

    file.close();

    cout << "Data written successfully";

    return 0;
}


SUM OF THREE NO.S USING POINTER


#include <iostream>
using namespace std;

int main()
{
    int a, b, c, sum;
    int *p, *q, *r;

    cout << "Enter three numbers: ";
    cin >> a >> b >> c;

    p = &a;
    q = &b;
    r = &c;

    sum = *p + *q + *r;

    cout << "Sum = " << sum;

    return 0;
}


CLASS RECTANGLE - AREA & PERIMETER 


#include <iostream>
using namespace std;

class Rectangle
{
    float length, breadth;

public:
    void getData()
    {
        cout << "Enter length and breadth: ";
        cin >> length >> breadth;
    }

    void calculate()
    {
        cout << "Area = " << length * breadth << endl;
        cout << "Perimeter = " << 2 * (length + breadth);
    }
};

int main()
{
    Rectangle r;

    r.getData();
    r.calculate();

    return 0;
}


FUNCTION OVERLOAD:AREA OF CIRCLE AND TRIANGLE 


#include <iostream>
using namespace std;

void area(float r)
{
    cout << "Area of circle = " << 3.14 * r * r << endl;
}

void area(float b, float h)
{
    cout << "Area of triangle = " << 0.5 * b * h;
}

int main()
{
    float r, b, h;

    cout << "Enter radius: ";
    cin >> r;

    cout << "Enter base and height: ";
    cin >> b >> h;

    area(r);
    area(b, h);

    return 0;
}


EXCEPTION HANDLING:VOTING ELIGIBILITY 


#include <iostream>
using namespace std;

int main()
{
    int age;

    cout << "Enter age: ";
    cin >> age;

    try
    {
        if(age < 18)
        {
            throw age;
        }

        cout << "Eligible to vote";
    }
    catch(int x)
    {
        cout << "Not eligible to vote";
    }

    return 0;
}


USER DEFINED NAMESPACE 


#include <iostream>
using namespace std;

namespace First
{
    int a = 10;
}

int main()
{
    cout << "Value = " << First::a;

    return 0;
}


STRUCTURE BOOK


#include <iostream>
using namespace std;

struct Book
{
    int book_id;
    string title;
    float price;
};

int main()
{
    Book b;

    cout << "Enter book ID: ";
    cin >> b.book_id;

    cout << "Enter title: ";
    cin >> b.title;

    cout << "Enter price: ";
    cin >> b.price;

    cout << "\nBook Details";
    cout << "\nBook ID: " << b.book_id;
    cout << "\nTitle: " << b.title;
    cout << "\nPrice: " << b.price;

    return 0;
}


AREA OF CIRCLE AND SQUARE USING POINTER 


#include <iostream>
using namespace std;

int main()
{
    float r, s;
    float *p, *q;

    cout << "Enter radius: ";
    cin >> r;

    cout << "Enter side: ";
    cin >> s;

    p = &r;
    q = &s;

    cout << "Area of circle = " << 3.14 * (*p) * (*p) << endl;
    cout << "Area of square = " << (*q) * (*q);

    return 0;
}


CLASS MOBILE-Display 3 objects


#include <iostream>
using namespace std;

class Mobile
{
    int id;
    string name;
    float price;

public:
    void getData()
    {
        cout << "Enter ID, name and price: ";
        cin >> id >> name >> price;
    }

    void display()
    {
        cout << "\nID: " << id;
        cout << "\nName: " << name;
        cout << "\nPrice: " << price << endl;
    }
};

int main()
{
    Mobile m[3];

    for(int i = 0; i < 3; i++)
    {
        m[i].getData();
    }

    cout << "\nMobile Details";

    for(int i = 0; i < 3; i++)
    {
        m[i].display();
    }

    return 0;
}


SINGLE INHERITANCE - PERSON & STUDENT 


#include <iostream>
using namespace std;

class Person
{
public:
    void showPerson()
    {
        cout << "This is a Person" << endl;
    }
};

class Student : public Person
{
public:
    void showStudent()
    {
        cout << "This is a Student";
    }
};

int main()
{
    Student s;

    s.showPerson();
    s.showStudent();

    return 0;
}


2 NAMESPACES WITH SAME VARIABLE NAME


#include <iostream>
using namespace std;

namespace First
{
    int a = 10;
}

namespace Second
{
    int a = 20;
}

int main()
{
    cout << "First value = " << First::a << endl;
    cout << "Second value = " << Second::a;

    return 0;
}


EXCEPTION HANDLING- AGE VALIDATION 


#include <iostream>
using namespace std;

int main()
{
    int age;

    cout << "Enter age: ";
    cin >> age;

    try
    {
        if(age < 18 || age > 100)
        {
            throw age;
        }

        cout << "Valid Age";
    }
    catch(int x)
    {
        cout << "Invalid Age";
    }

    return 0;
}
