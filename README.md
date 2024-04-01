<h1>Introduction to C Programming</h1>

<h2>History of C</h2>

<p>C was developed in the early 1970s by <b>Dennis Ritchie</b> at Bell Labs. It was initially designed for implementing the UNIX operating system. C was influenced by the BCPL and B programming languages. The first published edition of the C programming language was introduced in 1978.</p>

<h2>C Programming Fundamentals</h2>

<p>C is a procedural and structured programming language. It is a middle-level language, combining features of both high-level and low-level languages. C is a general-purpose language that can be used for various applications, from system programming to application development. C is a powerful and efficient language, providing low-level memory access and control over system resources.</p>

<h2>Structure of a C Program</h2>

<p>A C program typically consists of one or more functions, with one function being the <b>main()</b> function. The main() function is the entry point of the program, where execution begins. C programs are organized into sections, such as preprocessing directives, variable declarations, and function definitions.</p>

<pre><code>#include &lt;stdio.h&gt;  /* Preprocessing directive */

int main() {        /* Function definition */
    printf("Hello, World!");  /* Statement */
    return 0;
}
</code></pre>

<h2>Compiling and Running C Programs</h2>

<p>C programs are typically written in a text editor or an Integrated Development Environment (IDE). The source code is then compiled by a C compiler, which translates the human-readable code into machine-readable instructions. The compiled program can be executed on the target system or platform. Common C compilers include GCC (GNU Compiler Collection), Clang, and MSVC (Microsoft Visual C++).</p>

<h2>Data Types and Variables</h2>

<h3>Basic Data Types</h3>

<ul>
  <li><code>int</code>: Stores integer values (whole numbers).</li>
  <li><code>float</code>: Stores single-precision floating-point values.</li>
  <li><code>double</code>: Stores double-precision floating-point values.</li>
  <li><code>char</code>: Stores single character values.</li>
</ul>

<pre><code>int x = 10;       /* Integer */
float y = 3.14f;  /* Single-precision float */
double z = 2.718; /* Double-precision float */
char c = 'A';     /* Character */
</code></pre>

<h3>Type Modifiers</h3>

<ul>
  <li><code>short</code>: Modifies an integer type to use less memory.</li>
  <li><code>long</code>: Modifies an integer type to use more memory.</li>
  <li><code>unsigned</code>: Modifies an integer type to represent only non-negative values.</li>
  <li><code>signed</code>: Modifies an integer type to represent both positive and negative values (default for <code>int</code>).</li>
</ul>

<pre><code>short s = 32767;        /* Short integer */
unsigned int ui = 4294967295U; /* Unsigned integer */
long long ll = 9223372036854775807LL; /* Long long integer */
</code></pre>

<h3>Declaring and Initializing Variables</h3>

<p>Variables must be declared before they can be used in a C program. Variables can be initialized during declaration or later in the program.</p>

<pre><code>int a;      /* Declaration */
a = 5;      /* Initialization */

int b = 10; /* Declaration and initialization */
</code></pre>

<h3>Constants and Literals</h3>

<p>Constants are fixed values that cannot be modified during program execution. <b>Literals</b> are constant values represented directly in the source code.</p>

<pre><code>const double PI = 3.14159; /* Constant */

int x = 42;    /* Integer literal */
char y = 'Z';  /* Character literal */
float z = 3.5f; /* Floating-point literal */
</code></pre>

<h2>Operators and Expressions</h2>

<h3>Arithmetic Operators</h3>

<ul>
  <li><code>+</code> (Addition)</li>
  <li><code>-</code> (Subtraction)</li>
  <li><code>*</code> (Multiplication)</li>
  <li><code>/</code> (Division)</li>
  <li><code>%</code> (Modulus)</li>
</ul>

<pre><code>int a = 10, b = 3;
int sum = a + b;     /* sum = 13 */
int diff = a - b;    /* diff = 7 */
int prod = a * b;    /* prod = 30 */
int quot = a / b;    /* quot = 3 */
int rem = a % b;     /* rem = 1 */
</code></pre>

<h3>Relational Operators</h3>

<ul>
  <li><code>==</code> (Equal to)</li>
  <li><code>!=</code> (Not equal to)</li>
  <li><code>&gt;</code> (Greater than)</li>
  <li><code>&lt;</code> (Less than)</li>
  <li><code>&gt;=</code> (Greater than or equal to)</li>
  <li><code>&lt;=</code> (Less than or equal to)</li>
</ul>

<pre><code>int x = 5, y = 10;
if (x == y) {
    /* Code to execute if x is equal to y */
} else if (x &gt; y) {
    /* Code to execute if x is greater than y */
} else {
    /* Code to execute if x is less than y */
}
</code></pre>

<h3>Logical Operators</h3>

<ul>
  <li><code>&amp;&amp;</code> (Logical AND)</li>
  <li><code>||</code> (Logical OR)</li>
  <li><code>!</code> (Logical NOT)</li>
</ul>

<pre><code>int a = 10, b = 5, c = 20;
if (a &gt; b &amp;&amp; a &lt; c) {
    /* Code to execute if both conditions are true */
}

if (a == 10 || b == 0) {
    /* Code to execute if either condition is true */
}

if (!a) {
    /* Code to execute if a is false (0) */
}
</code></pre>

<h3>Bitwise Operators</h3>

<ul>
  <li><code>&amp;</code> (Bitwise AND)</li>
  <li><code>|</code> (Bitwise OR)</li>
  <li><code>^</code> (Bitwise XOR)</li>
  <li><code>~</code> (Bitwise Complement)</li>
  <li><code>&lt;&lt;</code> (Left Shift)</li>
  <li><code>&gt;&gt;</code> (Right Shift)</li>
</ul>

<pre><code>int a = 5;     /* 0000 0000 0000 0000 0000 0000 0000 0101 */
int b = 9;     /* 0000 0000 0000 0000 0000 0000 0000 1001 */
int c = a &amp; b; /* c = 1 (0000 0000 0000 0000 0000 0000 0000 0001) */
int d = a | b; /* d = 13 (0000 0000 0000 0000 0000 0000 0000 1101) */
int e = a ^ b; /* e = 12 (0000 0000 0000 0000 0000 0000 0000 1100) */
int f = ~a;    /* f = -6 (1111 1111 1111 1111 1111 1111 1111 1010) */
int g = a &lt;&lt; 2; /* g = 20 (0000 0000 0000 0000 0000 0000 0001 0100) */
int h = b &gt;&gt; 1; /* h = 4 (0000 0000 0000 0000 0000 0000 0000 0100) */
</code></pre>

<h3>Assignment Operators</h3>

<ul>
  <li><code>=</code> (Simple assignment)</li>
  <li><code>+=</code> (Add and assign)</li>
  <li><code>-=</code> (Subtract and assign)</li>
  <li><code>*=</code> (Multiply and assign)</li>
  <li><code>/=</code> (Divide and assign)</li>
  <li><code>%=</code> (Modulus and assign)</li>
</ul>

<pre><code>int a = 10;
a += 5;  /* a = 15 */
a -= 3;  /* a = 12 */
a *= 2;  /* a = 24 */
a /= 4;  /* a = 6 */
a %= 3;  /* a = 0 */
</code></pre>

<h1>Operator Precedence and Associativity</h1>

<p>Operator precedence determines the order in which operations are performed in an expression. Associativity determines the order in which operations of the same precedence are evaluated.</p>

<p>In C, operators have the following precedence (from highest to lowest):</p>

<ol>
  <li>Postfix operators (() [] . -> ++ --)</li>
  <li>Unary operators (+ - ! ~ ++ -- (type) * & sizeof)</li>
  <li>Multiplicative operators (* / %)</li>
  <li>Additive operators (+ -)</li>
  <li>Bitwise shift operators (<< >>)</li>
  <li>Relational operators (< > <= >=)</li>
  <li>Equality operators (== !=)</li>
  <li>Bitwise AND (&)</li>
  <li>Bitwise XOR (^)</li>
  <li>Bitwise OR (|)</li>
  <li>Logical AND (&&)</li>
  <li>Logical OR (||)</li>
  <li>Conditional operator (?:)</li>
  <li>Assignment operators (= += -= *= /= %= >>= <<= &= ^= |=)</li>
  <li>Comma operator (,)</li>
</ol>

<p>Associativity rules:</p>

<ul>
  <li>Most operators are left-to-right associative (= + - * / % << >> & ^ |)</li>
  <li>Unary operators, conditional operator, and assignment operators are right-to-left associative (++ -- (type) ?: = += -= *= /= %= >>= <<= &= ^= |=)</li>
</ul>

<p>Example:</p>

<pre><code>int a = 5, b = 3, c;

c = a + b * 3;    // c = 5 + (3 * 3) = 14 (multiplication has higher precedence than addition)
c = (a + b) * 3;  // c = (5 + 3) * 3 = 24 (parentheses override operator precedence)
c = a = b;        // c = 3, a = 3 (assignment operators are right-to-left associative)
c = a++ + ++b;    // c = 3 + 4 = 7, a = 4, b = 4 (postfix and prefix increment have higher precedence)
</code></pre>

<h1>Control Flow</h1>

<h2>Conditional Statements (if, else, else if, switch)</h2>

<p>The <code>if</code> statement is used to execute a block of code if a certain condition is true. The <code>else</code> and <code>else if</code> clauses provide alternative paths of execution based on different conditions.</p>

<pre><code>int x = 10;
if (x &gt; 0) {
    printf("x is positive\n");
} else if (x &lt; 0) {
    printf("x is negative\n");
} else {
    printf("x is zero\n");
}
</code></pre>

<p>The <code>switch</code> statement is used to execute different blocks of code based on different values of an expression.</p>

<pre><code>int day = 3;
switch (day) {
    case 1:
        printf("Monday\n");
        break;
    case 2:
        printf("Tuesday\n");
        break;
    case 3:
        printf("Wednesday\n");
        break;
    default:
        printf("Invalid day\n");
}
</code></pre>

<h2>Loops (for, while, do-while)</h2>

<p><b>Loops</b> are used to repeat a block of code multiple times. The <code>for</code> loop is used when the number of iterations is known in advance.</p>

<pre><code>for (int i = 0; i &lt; 5; i++) {
    printf("%d\n", i);  // Prints 0 1 2 3 4
}
</code></pre>

<p>The <code>while</code> loop is used when the number of iterations is unknown, and the loop continues as long as a given condition is true.</p>

<pre><code>int i = 0;
while (i &lt; 5) {
    printf("%d\n", i);
    i++;
}
</code></pre>

<p>The <code>do-while</code> loop is similar to the <code>while</code> loop, but it executes the loop body at least once, even if the condition is false.</p>

<pre><code>int i = 0;
do {
    printf("%d\n", i);
    i++;
} while (i &lt; 5);
</code></pre>

<h2>Break and Continue Statements</h2>

<p>The <code>break</code> statement is used to exit a loop prematurely.</p>

<pre><code>for (int i = 0; i &lt; 10; i++) {
    if (i == 5) {
        break;  // Exit the loop when i is 5
    }
    printf("%d\n", i);
}
</code></pre>

<p>The <code>continue</code> statement is used to skip the current iteration of a loop and move to the next iteration.</p>

<pre><code>for (int i = 0; i &lt; 10; i++) {
    if (i == 5) {
        continue;  // Skip the iteration when i is 5
    }
    printf("%d\n", i);
}
</code></pre>

<h2>Goto Statement</h2>

<p>The <code>goto</code> statement is used to transfer control to a labeled statement within the same function. However, its use is generally discouraged as it can make code harder to read and maintain.</p>

<pre><code>int i = 0;
loop:
    printf("%d\n", i);
    i++;
    if (i &lt; 5) {
        goto loop;
    }
</code></pre>

<h1>Functions</h1>

<h2>Function Definition and Declaration</h2>

<p>A function is a block of code that performs a specific task. In C, functions must be declared before they can be used, and they must be defined to provide their implementation.</p>

<pre><code>// Function declaration
int add(int a, int b);

int main() {
    int result = add(3, 4);
    printf("Result: %d\n", result);
    return 0;
}

// Function definition
int add(int a, int b) {
    int sum = a + b;
    return sum;
}
</code></pre>

<h2>Function Arguments and Return Values</h2>

<p>Functions can accept input values (arguments) and return a value (return value) after performing their tasks.</p>

<pre><code>int multiply(int a, int b) {
    int product = a * b;
    return product;
}

int main() {
    int result = multiply(5, 6);
    printf("Result: %d\n", result);  // Output: Result: 30
    return 0;
}
</code></pre>

<h1>Scope and Lifetime of Variables</h1>

<p>In C, variables have a scope and lifetime. The scope determines where a variable is accessible, and the lifetime determines how long the variable exists in memory.</p>

<h2>Local variables</h2>

<p>Declared within a function or block, and are only accessible within that scope. They are created when the function or block is entered and destroyed when it is exited.</p>

<h2>Global variables</h2>

<p>Declared outside of any function, and are accessible throughout the entire program. They are created when the program starts and destroyed when it ends.</p>

<p><strong>Example:</strong></p>

<pre><code>#include &lt;stdio.h&gt;

// Global variable
int global_var = 10;

void function() {
    // Local variable
    int local_var = 20;
    
    printf("Local variable: %d\n", local_var);
    printf("Global variable: %d\n", global_var);
}

int main() {
    function();
    
    // Accessing global variable from main
    printf("Global variable from main: %d\n", global_var);
    
    // Trying to access local variable from main (will result in error)
    // printf("Local variable from main: %d\n", local_var);
    
    return 0;
}
</code></pre>

<p>In the above example:</p>
<ul>
  <li><code>global_var</code> is a global variable accessible from both <code>function()</code> and <code>main()</code>.</li>
  <li><code>local_var</code> is a local variable defined inside <code>function()</code> and is only accessible within that function.</li>
</ul>
<p>Attempting to access <code>local_var</code> from <code>main()</code> will result in a compilation error due to its limited scope.</p>

<h1>Arrays</h1>

<h2>One-dimensional Arrays</h2>

<p>In C, an array is a collection of elements of the same data type, stored in contiguous memory locations. A one-dimensional array is a linear array that stores elements in a single row.</p>

<pre><code>int numbers[5]; // Declares an array of 5 integers
numbers[0] = 10; // Assigning values to array elements
numbers[1] = 20;
numbers[2] = 30;
numbers[3] = 40;
numbers[4] = 50;

for (int i = 0; i < 5; i++) {
    printf("%d ", numbers[i]); // Output: 10 20 30 40 50
}
</code></pre>

<h2>Multi-dimensional Arrays</h2>

<p>C also supports multi-dimensional arrays, which can be thought of as arrays of arrays. A two-dimensional array is an array of one-dimensional arrays.</p>

<pre><code>int matrix[3][4]; // Declares a 3x4 two-dimensional array

// Initializing values
matrix[0][0] = 1;
matrix[0][1] = 2;
matrix[0][2] = 3;
matrix[0][3] = 4;
matrix[1][0] = 5;
matrix[1][1] = 6;
matrix[1][2] = 7;
matrix[1][3] = 8;
matrix[2][0] = 9;
matrix[2][1] = 10;
matrix[2][2] = 11;
matrix[2][3] = 12;

// Accessing elements
printf("%d\n", matrix[1][2]); // Output: 7
</code></pre>

<h2>Array Initialization</h2>

<p>Arrays can be initialized during declaration or later in the program.</p>

<pre><code>int numbers[5] = {10, 20, 30, 40, 50}; // Initialization during declaration
char vowels[] = {'a', 'e', 'i', 'o', 'u'}; // Initialization with character literals

int scores[3];
scores[0] = 80; // Initialization later in the program
scores[1] = 75;
scores[2] = 92;
</code></pre>

<h2>Array Operations</h2>

<p>Common array operations include accessing elements, computing the length or size of an array, and passing arrays to functions.</p>

<pre><code>int numbers[] = {10, 20, 30, 40, 50};
int length = sizeof(numbers) / sizeof(numbers[0]); // Compute length of the array
printf("Length: %d\n", length); // Output: Length: 5

void printArray(int arr[], int size) {
    for (int i = 0; i < size; i++) {
        printf("%d ", arr[i]);
    }
    printf("\n");
}

printArray(numbers, length); // Output: 10 20 30 40 50
</code></pre>

<h1>Pointers</h1>

<h2>Understanding Memory Addresses</h2>

<p>In C, every variable has a memory address where its value is stored. Pointers are variables that store memory addresses of other variables.</p>

<pre><code>int x = 10;
printf("Value of x: %d\n", x); // Output: Value of x: 10
printf("Address of x: %p\n", &x); // Output: Address of x: 0x7ffee9b9c3d4 (example)
</code></pre>

<h2>Pointer Declaration and Operations</h2>

<p>Pointers are declared by specifying the data type they will point to, followed by an asterisk (*). Pointers can be dereferenced using the * operator to access the value stored at the memory address they point to.</p>

<pre><code>int x = 10;
int *ptr = &x; // Declare a pointer and initialize it with the address of x

printf("Value of x: %d\n", x); // Output: Value of x: 10
printf("Value of x via pointer: %d\n", *ptr); // Output: Value of x via pointer: 10

*ptr = 20; // Modify the value of x via the pointer
printf("New value of x: %d\n", x); // Output: New value of x: 20
</code></pre>

<h2>Pointer Arithmetic</h2>

<p>Pointers in C can be incremented or decremented to move their addresses. The amount they move depends on the size of the data type they point to.</p>

<pre><code>int numbers[] = {10, 20, 30, 40, 50};
int *ptr = numbers; // ptr points to the first element of the array

for (int i = 0; i < 5; i++) {
    printf("%d ", *ptr); // Output: 10 20 30 40 50
    ptr++; // Move the pointer to the next element
}
</code></pre>

<h2>Pointers and Arrays</h2>

<p>In C, arrays and pointers are closely related. The name of an array is a constant pointer that points to the first element of the array. Array elements can be accessed using pointer arithmetic.</p>

<pre><code>int numbers[] = {10, 20, 30, 40, 50};
int *ptr = numbers; // ptr points to the first element of the array

printf("%d\n", *ptr); // Output: 10
printf("%d\n", *(ptr + 2)); // Output: 30 (equivalent to numbers[2])
</code></pre>

<h2>Pointers and Functions</h2>

<p>Pointers are commonly used to pass large data structures, such as arrays, to functions by reference, allowing the function to modify the original data.</p>

<pre><code>void swapNumbers(int *a, int *b) {
    int temp = *a;
    *a = *b;
    *b = temp;
}

int main() {
    int x = 10, y = 20;
    printf("Before swap: x = %d, y = %d\n", x, y); // Output: Before swap: x = 10, y = 20

    swapNumbers(&x, &y); // Pass the addresses of x and y to the function

    printf("After swap: x = %d, y = %d\n", x, y); // Output: After swap: x = 20, y = 10
    return 0;
}
</code></pre>

<h1>Strings</h1>

<h2>String Literals</h2>

<p>In C, strings are represented as arrays of characters terminated by a null character ('\0'). String literals are enclosed in double quotes.</p>

<pre><code>char greeting[] = "Hello, World!";
printf("%s\n", greeting); // Output: Hello, World!
</code></pre>

<h2>String Manipulation Functions</h2>

<p>The C standard library provides several functions for manipulating strings, defined in the <code>&lt;string.h&gt;</code> header file.</p>
  
String Manipulation Functions The C standard library provides several functions for manipulating strings, defined in the <string.h> header file.
<pre><code>
strlen(str): Returns the length of the string str, excluding the null terminator.
strcpy(dest, src): Copies the string src into the array dest, including the null terminator.
strcat(dest, src): Appends the string src to the end of the string dest.
strcmp(str1, str2): Compares the strings str1 and str2, and returns 0 if they are equal.
</code></pre>

<pre><code>#include &lt;string.h&gt;

int main() {
    char str1[] = "Hello";
    char str2[20];

    printf("Length of str1: %lu\n", strlen(str1)); // Output: Length of str1: 5

    strcpy(str2, str1); // Copy str1 to str2
    printf("str2: %s\n", str2); // Output: str2: Hello

    char str3[] = ", World!";
    strcat(str2, str3); // Append str3 to str2
    printf("str2: %s\n", str2); // Output: str2: Hello, World!

    char str4[] = "Hello";
    char str5[] = "Hello";
    if (strcmp(str4, str5) == 0) {
        printf("str4 and str5 are equal\n"); // Output: str4 and str5 are equal
    } else {
        printf("str4 and str5 are not equal\n");
    }

    return 0;
}
</code></pre>

<h1>Structures and Unions</h1>

<h2>Defining and Using Structures</h2>

<p>A structure in C is a user-defined data type that allows you to combine different data types into a single entity. It is a collection of one or more variables of different data types, grouped together under a single name.</p>

<pre><code>struct Student {
    int id;
    char name[50];
    float gpa;
};

int main() {
    struct Student s1;
    s1.id = 1;
    strcpy(s1.name, "John Doe");
    s1.gpa = 3.8;

    printf("ID: %d\n", s1.id);
    printf("Name: %s\n", s1.name);
    printf("GPA: %.2f\n", s1.gpa);

    return 0;
}
</code></pre>

<h2>Nested Structures</h2>

<p>Structures in C can contain other structures as members, which are called nested structures.</p>

<pre><code>struct Address {
    char street[100];
    char city[50];
    char state[20];
};

struct Employee {
    int id;
    char name[50];
    float salary;
    struct Address address;
};

int main() {
    struct Employee emp;
    strcpy(emp.name, "Jane Smith");
    emp.salary = 5000.0;
    strcpy(emp.address.street, "123 Main St.");
    strcpy(emp.address.city, "Cityville");
    strcpy(emp.address.state, "CA");

    // Accessing nested structure members
    printf("Employee: %s\n", emp.name);
    printf("Address: %s, %s, %s\n", emp.address.street, emp.address.city, emp.address.state);

    return 0;
}
</code></pre>

<h2>Arrays of Structures</h2>

<p>C allows you to create arrays of structures, which can be useful for storing and manipulating collections of related data.</p>

<pre><code>struct Student {
    int id;
    char name[50];
    float gpa;
};

int main() {
    struct Student students[3];

    // Initialize student records
    students[0].id = 1;
    strcpy(students[0].name, "John Doe");
    students[0].gpa = 3.8;

    students[1].id = 2;
    strcpy(students[1].name, "Jane Smith");
    students[1].gpa = 3.6;

    students[2].id = 3;
    strcpy(students[2].name, "Bob Johnson");
    students[2].gpa = 3.9;

    // Print student records
    for (int i = 0; i < 3; i++) {
        printf("ID: %d, Name: %s, GPA: %.2f\n", students[i].id, students[i].name, students[i].gpa);
    }

    return 0;
}
</code></pre>

<h2>Unions</h2>

<p>A union in C is a user-defined data type that allows you to store different data types in the same memory location. At any given time, only one of the members of a union can hold a value.</p>

<pre><code>union Value {
    int x;
    float y;
    char z;
};

int main() {
    union Value val;

    val.x = 10;
    printf("val.x = %d\n", val.x); // Output: val.x = 10

    val.y = 3.14;
    printf("val.y = %f\n", val.y); // Output: val.y = 3.140000

    val.z = 'A';
    printf("val.z = %c\n", val.z); // Output: val.z = A

    return 0;
}
</code></pre>

<h1>File Handling</h1>

<h2>Opening and Closing Files</h2>

<p>In C, you need to open a file before you can read from or write to it. The <b>fopen</b> function is used to open a file, and the <b>fclose</b> function is used to close it.</p>

<pre><code>#include &lt;stdio.h&gt;

int main() {
    FILE *file;
    file = fopen("example.txt", "w"); // Open a file for writing

    if (file == NULL) {
        printf("Error opening file!\n");
        return 1;
    }

    // Write to the file
    fprintf(file, "This is some text.\n");

    fclose(file); // Close the file

    return 0;
}
</code></pre>

<h2>Reading and Writing to Files</h2>

<p>The <b>fprintf</b> function is used to write data to a file, and the <b>fscanf</b> function is used to read data from a file.</p>

<pre><code>#include &lt;stdio.h&gt;

int main() {
    FILE *file;
    char buffer[100];

    file = fopen("example.txt", "r"); // Open a file for reading

    if (file == NULL) {
        printf("Error opening file!\n");
        return 1;
    }

    // Read from the file
    while (fscanf(file, "%s", buffer) != EOF) {
        printf("%s ", buffer);
    }

    printf("\n");

    fclose(file); // Close the file

    return 0;
}
</code></pre>

<h2>File Operations</h2>

<p>C provides several functions for performing various file operations, such as fseek for moving the file position indicator, <b>ftell</b> for getting the current value of the file position indicator, and <b>rewind</b> for setting the file position indicator to the beginning of the file.</p>

<pre><code>#include &lt;stdio.h&gt;

int main() {
    FILE *file;
    char buffer[100];

    file = fopen("example.txt", "r+"); // Open a file for reading and writing

    if (file == NULL) {
        printf("Error opening file!\n");
        return 1;
    }

    // Read from the file
    fgets(buffer, sizeof(buffer), file);
    printf("First line: %s", buffer);

    // Move file position indicator to the beginning
    rewind(file);

    // Write to the file
    fprintf(file, "New first line\n");

    fclose(file); // Close the file

    return 0;
}
</code></pre>

<h2>Error Handling</h2>

<p>It's important to handle errors that may occur during file operations, such as file not found, permission denied, or read/write errors. C provides functions like ferror and perror to check for and report errors.</p>

<pre><code>#include &lt;stdio.h&gt;
#include &lt;errno.h&gt;
#include &lt;string.h&gt;

int main() {
    FILE *file;
    char buffer[100];

    file = fopen("nonexistent.txt", "r");

    if (file == NULL) {
        perror("Error opening file");
        return 1;
    }

    // Read from the file
    if (fgets(buffer, sizeof(buffer), file) == NULL) {
        if (ferror(file)) {
            perror("Error reading file");
        } else {
            printf("End of file reached.\n");
        }
    } else {
        printf("Read: %s", buffer);
    }

    fclose(file); // Close the file

    return 0;
}
</code></pre>

<h1>Memory Management</h1>

<p>In C programming, memory can be allocated statically or dynamically. Static memory allocation occurs at compile-time and is used for variables within a function or global variables. Dynamic memory allocation, on the other hand, happens at runtime and allows you to request memory from the system's heap.</p>

<h2>Static and Dynamic Memory Allocation</h2>

<p>Static memory allocation is demonstrated in the following example:</p>

<pre><code>#include &lt;stdio.h&gt;
#include &lt;stdlib.h&gt;

int global_var; // Static memory allocation for global variable

int main() {
    int static_var; // Static memory allocation for local variable

    int *dynamic_var = malloc(sizeof(int)); // Dynamic memory allocation
    if (dynamic_var == NULL) {
        printf("Memory allocation failed.\n");
        return 1;
    }

    *dynamic_var = 42;
    printf("Value of dynamically allocated variable: %d\n", *dynamic_var);

    free(dynamic_var); // Free dynamically allocated memory
    return 0;
}
</code></pre>

<p>The C standard library provides functions for dynamically allocating and deallocating memory:</p>

<ul>
  <li><code>malloc(size)</code>: Allocates a block of <code>size</code> bytes of uninitialized memory from the heap.</li>
  <li><code>calloc(count, size)</code>: Allocates an array of <code>count</code> elements, each of <code>size</code> bytes, and initializes the memory to zero.</li>
  <li><code>realloc(ptr, size)</code>: Attempts to resize the memory block pointed to by <code>ptr</code> to <code>size</code> bytes.</li>
  <li><code>free(ptr)</code>: Deallocates the memory block pointed to by <code>ptr</code>, previously allocated by <code>malloc</code>, <code>calloc</code>, or <code>realloc</code>.</li>
</ul>

<p>Dynamic memory allocation example:</p>

<pre><code>#include &lt;stdio.h&gt;
#include &lt;stdlib.h&gt;

int main() {
    int *ptr1 = malloc(sizeof(int) * 5); // Allocate memory for 5 integers
    if (ptr1 == NULL) {
        printf("Memory allocation failed.\n");
        return 1;
    }

    int *ptr2 = calloc(3, sizeof(int)); // Allocate memory for 3 integers, initialized to 0
    if (ptr2 == NULL) {
        printf("Memory allocation failed.\n");
        free(ptr1); // Free previously allocated memory
        return 1;
    }

    ptr2 = realloc(ptr2, sizeof(int) * 5); // Resize the memory block to hold 5 integers

    // Use the allocated memory
    ptr1[0] = 10;
    ptr2[2] = 20;

    // Free the allocated memory
    free(ptr1);
    free(ptr2);

    return 0;
}
</code></pre>

<h2>Memory Leaks and Their Prevention</h2>

<p>A memory leak occurs when dynamically allocated memory is not properly deallocated, leading to a gradual depletion of available memory. To prevent memory leaks, it's important to free all dynamically allocated memory when it is no longer needed. One common practice is to use a matching pair of <code>malloc</code> and <code>free</code> calls.</p>

<p>Example:</p>

<pre><code>#include &lt;stdio.h&gt;
#include &lt;stdlib.h&gt;

void leak_memory() {
    int *ptr = malloc(sizeof(int)); // Allocate memory
    // No corresponding free(ptr) call, causing a memory leak
}

int main() {
    leak_memory(); // Call the function that leaks memory
    return 0;
}
</code></pre>

<p>To prevent memory leaks:</p>

<pre><code>#include &lt;stdio.h&gt;
#include &lt;stdlib.h&gt;

int *allocate_memory() {
    int *ptr = malloc(sizeof(int));
    if (ptr == NULL) {
        printf("Memory allocation failed.\n");
        return NULL;
    }
    return ptr;
}

void free_memory(int *ptr) {
    if (ptr != NULL) {
        free(ptr);
    }
}

int main() {
    int *ptr = allocate_memory();
    if (ptr != NULL) {
        // Use the allocated memory
        *ptr = 42;
        printf("Value: %d\n", *ptr);
    }
    free_memory(ptr); // Free the allocated memory
    return 0;
}
</code></pre>

<p>In this example, the <code>allocate_memory</code> function is responsible for allocating memory and handling allocation failures, while the <code>free_memory</code> function ensures that the allocated memory is properly deallocated. Additionally, it's a good practice to check for <code>NULL</code> pointers before dereferencing or freeing them to avoid potential crashes or undefined behavior.</p>

<h1>Preprocessor Directives</h1>

<p>Preprocessor directives in C are used to manipulate the source code before it is compiled. They allow you to define macros, include files, and conditionally compile code segments.</p>

<h2>Macro Definitions</h2>

<p>Macros in C are code fragments that are substituted by the preprocessor at compile time. They are defined using the <code>#define</code> directive.</p>

<pre><code>#define PI 3.14159
#define AREA(r) (PI * r * r)

int main() {
    double radius = 5.0;
    double area = AREA(radius);
    printf("Area of circle with radius %f is %f\n", radius, area);
    return 0;
}
</code></pre>

<p>In this example, <code>PI</code> is a simple macro that substitutes its value wherever it's used, and <code>AREA(r)</code> is a macro function that calculates the area of a circle given its radius.</p>

<h2>File Inclusion (#include)</h2>

<p>The <code>#include</code> directive is used to include header files or other source files in a C program.</p>

<pre><code>#include &lt;stdio.h&gt;  // Include standard I/O header file
#include "myheader.h"  // Include a custom header file
</code></pre>

<h2>Conditional Compilation</h2>

<p>Conditional compilation directives allow you to selectively include or exclude parts of the code based on certain conditions.</p>

<pre><code>#define DEBUG

int main() {
    int x = 10, y = 20;
    int sum = x + y;

#ifdef DEBUG
    printf("x = %d, y = %d, sum = %d\n", x, y, sum);  // This line will be included
#endif

#if !defined(RELEASE)
    printf("Debug mode\n");  // This line will be included
#else
    printf("Release mode\n");  // This line will be excluded
#endif

    return 0;
}
</code></pre>

<h1>Advanced Topics</h1>

<p>In addition to the basic concepts of C programming, there are several advanced topics that provide more flexibility and power to developers.</p>

<h2>Bit Manipulation</h2>

<p>C provides bitwise operators for manipulating individual bits within a data type. This can be useful for low-level programming or optimizing certain operations.</p>

<pre><code>unsigned int a = 0x0F0F0F0F; // Binary: 0000 1111 0000 1111 0000 1111 0000 1111
unsigned int b = 0xF0F0F0F0; // Binary: 1111 0000 1111 0000 1111 0000 1111 0000

unsigned int c = a & b; // Bitwise AND: 0000 0000 0000 0000 0000 0000 0000 0000
unsigned int d = a | b; // Bitwise OR: 1111 1111 1111 1111 1111 1111 1111 1111
unsigned int e = a ^ b; // Bitwise XOR: 1111 1111 1111 1111 1111 1111 1111 1111
unsigned int f = ~a;    // Bitwise NOT: 1111 0000 1111 0000 1111 0000 1111 0000
</code></pre>

<h2>Command-line Arguments</h2>

<p>C programs can accept command-line arguments when executed from the terminal or command prompt.</p>

<pre><code>#include &lt;stdio.h&gt;

int main(int argc, char *argv[]) {
    printf("Program name: %s\n", argv[0]);

    printf("Number of arguments: %d\n", argc);

    for (int i = 1; i &lt; argc; i++) {
        printf("Argument %d: %s\n", i, argv[i]);
    }

    return 0;
}
</code></pre>

<p>When executed with command-line arguments like <code>./program arg1 arg2 arg3</code>, the program will output:</p>

<pre><code>Program name: ./program
Number of arguments: 4
Argument 1: arg1
Argument 2: arg2
Argument 3: arg3
</code></pre>

<h2>Linked Lists</h2>

<p>A linked list is a dynamic data structure where each node contains data and a reference (link) to the next node in the list.</p>

<pre><code>#include &lt;stdio.h&gt;
#include &lt;stdlib.h&gt;

typedef struct Node {
    int data;
    struct Node* next;
} Node;

void printList(Node* head) {
    Node* current = head;
    while (current != NULL) {
        printf("%d ", current->data);
        current = current->next;
    }
    printf("\n");
}

int main() {
    Node* head = NULL;
    Node* second = NULL;
    Node* third = NULL;

    // Allocate nodes in the heap
    head = (Node*)malloc(sizeof(Node));
    second = (Node*)malloc(sizeof(Node));
    third = (Node*)malloc(sizeof(Node));

    // Assign data and link nodes
    head->data = 1;
    head->next = second;
    second->data = 2;
    second->next = third;
    third->data = 3;
    third->next = NULL;

    printf("Linked List: ");
    printList(head);

    // Free dynamically allocated memory
    free(head);
    free(second);
    free(third);

    return 0;
}
</code></pre>

<h2>Sorting and Searching Algorithms</h2>

<p>C is often used for implementing and studying various sorting and searching algorithms due to its low-level control and performance.</p>

<pre><code>#include &lt;stdio.h&gt;

void bubbleSort(int arr[], int n) {
    int i, j, temp;
    for (i = 0; i &lt; n - 1; i++) {
        for (j = 0; j &lt; n - i - 1; j++) {
            if (arr[j] > arr[j + 1]) {
                temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
            }
        }
    }
}

int linearSearch(int arr[], int n, int key) {
    int i;
    for (i = 0; i &lt; n; i++) {
        if (arr[i] == key) {
            return i;
        }
    }
    return -1;
}

int main() {
    int arr[] = {64, 34, 25, 12, 22, 11, 90};
    int n = sizeof(arr) / sizeof(arr[0]);
    int key = 25;

    bubbleSort(arr, n);

    printf("Sorted array: ");
    for (int i = 0; i &lt; n; i++) {
        printf("%d ", arr[i]);
    }
    printf("\n");

    int index = linearSearch(arr, n, key);
    if (index != -1) {
        printf("%d found at index %d\n", key, index);
    } else {
        printf("%d not found in the array\n", key);
    }

    return 0;
}
</code></pre>

<p>In this example, we implement the Bubble Sort algorithm to sort an array and the Linear Search algorithm to find the index of a specific element in the sorted array.</p>
</html>

<h1>Function Pointers</h1>

<p>In C, functions can be treated as first-class citizens, meaning they can be assigned to variables, passed as arguments to other functions, and returned from functions. This is achieved through function pointers.</p>

<pre><code>#include &lt;stdio.h&gt;

int add(int a, int b) {
    return a + b;
}

int subtract(int a, int b) {
    return a - b;
}

int operate(int a, int b, int (*op)(int, int)) {
    return op(a, b);
}

int main() {
    int result_add = operate(5, 3, add);
    int result_subtract = operate(10, 4, subtract);

    printf("Result of addition: %d\n", result_add);
    printf("Result of subtraction: %d\n", result_subtract);

    return 0;
}
</code></pre>

<p>This code snippet defines two functions, <code>add</code> and <code>subtract</code>, which perform addition and subtraction operations, respectively. The <code>operate</code> function takes two integers <code>a</code> and <code>b</code>, along with a function pointer <code>op</code> that points to a function taking two integers and returning an integer. It then applies the operation specified by the function pointer to the given arguments.</p>

<p>In the <code>main</code> function, the <code>operate</code> function is called twice, once with the <code>add</code> function pointer and once with the <code>subtract</code> function pointer, to demonstrate how function pointers can be used to switch between different operations.</p>

</html>
