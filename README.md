# Calculo-de-la-muestra-finita-e-infinita-
#include <iostream>
#include <cmath>
#include <string>

using namespace std;

int main() {
    double population, sampleSize;
    string answer = "si";

    while (answer == "si" || answer == "Si" || answer == "sI" || answer == "SI") {
        cout << "Ingrese el tamaño de la poblacion: ";
        cin >> population;
        cout << "Ingrese el tamaño de la muestra: ";
        cin >> sampleSize;

        // Calcular la muestra finita
        double finiteSample = (sampleSize / population) * 100;
        cout << "La muestra finita es: " << finiteSample << "%" << endl;

        // Calcular la muestra infinita
        double infiniteSample = (1.96 * 1.96 * 0.25) / ((0.05 * 0.05) * (population - 1) + 1.96 * 1.96 * 0.25);
        cout << "La muestra infinita es: " << infiniteSample << "%" << endl;

        cout << "Desea realizar otro calculo? (si / no): ";
        cin >> answer;
    }
    return 0;
}
