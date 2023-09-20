# CodSoft_tasks_internship
program that generates a random number and asks the user to guess it. Provide feedback on whether the guess is too high or too low until the user guesses the correct number
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
