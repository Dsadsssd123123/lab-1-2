#include <iostream>
#include <climits> 

int main() {
    int N; 
    int T; 

    std::cout << "Введіть розмір масиву: ";
    std::cin >> N;

    std::cout << "Введіть значення T: ";
    std::cin >> T;

    int maxNegative = INT_MIN; 
    int maxNegativeIndex = -1; 

    for (int i = 0; i < N; i++) {
        int num;
        std::cout << "Введіть елемент #" << i + 1 << ": ";
        std::cin >> num;

        if (num < 0 && num > maxNegative) {
            maxNegative = num;
            maxNegativeIndex = i;
        }

        if (num == T) {
            break; 
        }
    }

    if (maxNegativeIndex != -1) {
        std::cout << "Перший максимальний від'ємний елемент перед T знаходиться на позиції: " << maxNegativeIndex << std::endl;
    } else {
        std::cout << "Від'ємних елементів перед T не знайдено." << std::endl;
    }

    return 0;
}
