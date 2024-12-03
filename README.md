# Ovsiyenko_lab7

#include <iostream>

int main() {
    
    int size = 5;
    int* arr = new int[size] {1, 2, 3, 4, 5};

    std::cout << "Масив до видалення: ";
    for (int i = 0; i < size; ++i) {
        std::cout << arr[i] << " ";
    }
    std::cout << std::endl;

    int indexToDelete = 2;

    for (int i = indexToDelete; i < size - 1; ++i) {
        arr[i] = arr[i + 1];
    }

    --size;

    std::cout << "Масив після видалення: ";
    for (int i = 0; i < size; ++i) {
        std::cout << arr[i] << " ";
    }
    std::cout << std::endl;

    delete[] arr;

    return 0;
}
