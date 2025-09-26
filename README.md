

---

# Recursion in C++

## 📚 **Aim**

To understand **recursion** in C++ and implement:

* Program 1: Addition till N number
* Program 2: Factorial
* Program 3: Reversal of string

## 🛠 **Tools**

* GNU g++ compiler for local compilation
* Any online C++ compiler

---

## 📝 **Theory**

**Recursion** is a process where a function calls itself either **directly** or **indirectly** to solve a problem.
Each recursive call works on a **smaller instance** of the problem until a **base case** is reached, which stops further recursion.

Benefits:

* Reduces code complexity for repetitive tasks.
* Elegant way to solve problems like factorial, Fibonacci, string reversal, etc.

Key points of recursion:

* **Base Case** – The stopping condition.
* **Recursive Case** – The function calls itself with modified arguments.

---

## 💻 **Programs**

### **Program 1: Addition till N Number**

**Logic:**
This program calculates the sum of natural numbers from 1 to N using recursion.

**Algorithm:**

1. Start.
2. Define a recursive function `sum(n)`:

   * If `n == 0`, return 0.
   * Else return `n + sum(n - 1)`.
3. Input N.
4. Call `sum(N)` and display result.
5. End.

**Sample Code:**

```cpp
#include <iostream>
using namespace std;

int sum(int n) {
    if (n == 0)
        return 0;
    else
        return n + sum(n - 1);
}

int main() {
    int n;
    cout << "Enter a number: ";
    cin >> n;
    cout << "Sum till " << n << " = " << sum(n) << endl;
    return 0;
}
```

---

### **Program 2: Factorial Using Recursion**

**Logic:**
This program computes the factorial of a number using recursion.

**Algorithm:**

1. Start.
2. Define a recursive function `factorial(n)`:

   * If `n == 0` or `n == 1`, return 1.
   * Else return `n * factorial(n - 1)`.
3. Input number.
4. Call `factorial(n)` and display result.
5. End.

**Sample Code:**

```cpp
#include <iostream>
using namespace std;

int factorial(int n) {
    if (n == 0 || n == 1)
        return 1;
    else
        return n * factorial(n - 1);
}

int main() {
    int n;
    cout << "Enter a number: ";
    cin >> n;
    cout << "Factorial of " << n << " = " << factorial(n) << endl;
    return 0;
}
```

---

### **Program 3: Reversal of String Using Recursion**

**Logic:**
This program reverses a string using recursion.

**Algorithm:**

1. Start.
2. Define a recursive function `reverseString(str, i)`:

   * If index reaches string length, stop.
   * Else print last character and call the function again.
3. Input string.
4. Call the recursive function and display reversed string.
5. End.

**Sample Code:**

```cpp
#include <iostream>
using namespace std;

void reverseString(string str, int index) {
    if (index < 0)
        return;
    cout << str[index];
    reverseString(str, index - 1);
}

int main() {
    string str;
    cout << "Enter a string: ";
    cin >> str;

    cout << "Reversed string: ";
    reverseString(str, str.length() - 1);
    cout << endl;

    return 0;
}
```

---

## ✅ **Conclusion**

Recursion is a powerful technique in C++ that allows solving problems by **breaking them into smaller subproblems**.

* **Addition till N number** uses recursion to sum numbers.
* **Factorial** uses recursion to compute factorial efficiently.
* **Reversal of string** demonstrates recursion on strings.

By identifying a **base case** and a **recursive case**, recursion makes programs more **clean**, **structured**, and **logical**.

---

