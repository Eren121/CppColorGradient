# CppColorGradient
Single header gradient library designed for linear colors gradients but generic.
# Color
`gradient::Color` is a `std::valarray` typedef. Though the module can work with any valarray size, typically 3-component for RGB and 4 for RGBA, when using gradients with that, take care of that every element has the same size.
# Exemple
```c++
#include <stdlib.h>
#include <iostream>
#include "Gradient.h"

int main(int argc, char* argv[]) {
    using std::cout;
    using std::endl;
    using namespace gradient::operators;

    gradient::LinearColorGradient gradient;
    gradient[0.0] = {1,2,3};
    gradient[1.0] = {2,3,4};

    cout << gradient(1.01) << endl;

    return EXIT_SUCCESS;
}
```
