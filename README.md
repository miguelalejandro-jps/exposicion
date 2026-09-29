#include <iostream>

using namespace std;

int main() {
    char operacion;
    double num1, num2;

    cout << "=====================================" << endl;
    cout << "        CALCULADORA BÁSICA           " << endl;
    cout << "=====================================" << endl;

    // Solicitar el primer número
    cout << "Ingresa el primer número: ";
    cin >> num1;

    // Solicitar el operador
    cout << "Ingresa la operación (+, -, *, /): ";
    cin >> operacion;

    // Solicitar el segundo número
    cout << "Ingresa el segundo número: ";
    cin >> num2;

    cout << "-------------------------------------" << endl;

    // Estructura de control para realizar el cálculo
    switch (operacion) {
        case '+':
            cout << "Resultado: " << num1 << " + " << num2 << " = " << (num1 + num2) << endl;
            break;
        case '-':
            cout << "Resultado: " << num1 << " - " << num2 << " = " << (num1 - num2) << endl;
            break;
        case '*':
            cout << "Resultado: " << num1 << " * " << num2 << " = " << (num1 * num2) << endl;
            break;
        case '/':
            // Verificación para evitar la división entre cero
            if (num2 != 0) {
                cout << "Resultado: " << num1 << " / " << num2 << " = " << (num1 / num2) << endl;
            } else {
                cout << "Error: No se puede dividir entre cero." << endl;
            }
            break;
        default:
            cout << "Error: Operador no válido." << endl;
            break;
    }

    return 0;
}
