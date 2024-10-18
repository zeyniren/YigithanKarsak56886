# YigithanKarsak56886
#include "Std2DArrays.h"
#include <iostream>

void fillArray(std::array<std::array<int, MAXNUMBEROFCOLUMNS>, MAXNUMBEROFROWS>& arr, int rows, int columns) {
    if (rows > MAXNUMBEROFROWS || columns > MAXNUMBEROFCOLUMNS) {
        throw std::invalid_argument("Incorrect number of rows or columns");
    }

    int startValue = 1;

    for (int i = rows - 1; i >= 0; i--) {  // Start from the bottom row
        for (int j = 0; j < columns; j++) {  // Fill each row from left to right
            arr[i][j] = startValue;
            startValue++;
        }
    }
}
