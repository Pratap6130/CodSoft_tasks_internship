# CodSoft_tasks_internship
*program that generates a random number and asks the user to guess it. 


include <iostream>
using namespace std;

int main(){
    srand(time(0));
    int n = rand() % 100 + 1;
    int x;
    int attempts = 0;

    cout<<"Welcome to number guessing game"<<endl;
    cout<<"Guess a number between 1 and 100."<<endl;

    do{
        cout << "Enter your guess: ";
        cin >> x;
        attempts++;

        if (x < n) {
            cout<<"Number is Too low! Try again."<<endl;
        } else if (x > n) {
            cout<<"Number is Too high! Try again."<<endl;
        } else {
            cout<<"You've guessed the number in "<< attempts<< "attempts."<< endl;
        }
    } while(x!= n);

    return 0;
}

*calculator program that performs basic arithmetic
operations.

#include <iostream>
using namespace std;

int main(){
    char operation;
    double num1, num2;

    cout << "Enter First numbers: ";
    cin >>num1;
    
    cout << "Choose an operation: +, -, *, /: ";
    cin >>operation;
    
    cout << "Enter Second numbers: ";
    cin>> num2;

    switch (operation) {
        case '+':
            cout << num1 << " + " << num2 << " = " << num1 + num2 << endl;
            break;
        case '-':
            cout << num1 << " - " << num2 << " = " << num1 - num2 << endl;
            break;
        case '*':
            cout << num1 << " * " << num2 << " = " << num1 * num2 << endl;
            break;
        case '/':
            if (num2 != 0) {
                cout << num1 << " / " << num2 << " = " << num1 / num2 << endl;
            } else {
                cout << "Division by zero is not possible" << endl;
            }
            break;
        default:
            cout << "Try again!" << endl;
    }

    return 0;
}


*A program that manages student grades. Allow the user
to input student names and their corresponding grades.

#include <iostream>

using namespace std;



int main(){

    int marks;



    cout<<"Enter the student marks: ";

    cin >> marks;



    if (marks >= 90) {

        cout << "Grade is A+";

    } else if (marks >= 80) {

        cout << "Grade is A";

    } else if (marks >= 70) {

        cout << "Grade is B+";

    } else if (marks >= 60) {

        cout << "Grade is B";

    } else if (marks >= 50) {

        cout << "Grade is C";

    } else if (marks >= 40) {

        cout << "Grade is D";

    } else if (marks >= 30) {

        cout << "Grade is E";

    } else {

        cout << "Grade is F";

    }



    return 0;

}









