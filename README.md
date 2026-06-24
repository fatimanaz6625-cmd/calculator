# calculator
//c++ code for a calculator
#include <iostream>

using namespace std;

int main() {
    char op;
    double num1, num2;

    cout << "C++ Calculator " << endl;
    
    // Take user input
    cout << "Enter first number: ";
    cin >> num1;
    
    cout << "Enter operator (+, -, *, /): ";
    cin >> op;
    
    cout << "Enter second number: ";
    cin >> num2;

    // Perform calculation based on the operator
    switch(op) {
        case '+':
            cout << "\nResult: " << num1 << " + " << num2 << " = " << (num1 + num2) << endl;
            break;
            
        case '-':
            cout << "\nResult: " << num1 << " - " << num2 << " = " << (num1 - num2) << endl;
            break;
            
        case '*':
            cout << "\nResult: " << num1 << " * " << num2 << " = " << (num1 * num2) << endl;
            break;
            
        case '/':
            // Check for division by zero
            if (num2 == 0) {
                cout << "\nError: Division by zero is not allowed!" << endl;
            } else {
                cout << "\nResult: " << num1 << " / " << num2 << " = " << (num1 / num2) << endl;
            }
            break;
            
        default:
            // If the operator doesn't match any case
            cout << "\nError: Invalid operator!" << endl;
            break;
    }

    cout << "==========================" << endl;
    return 0;
}
