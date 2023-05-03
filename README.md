Download Link: https://assignmentchef.com/product/solved-cs2124-homework-8-class-polynomial-for-storing-and-manipulating-polynomial-expressions
<br>
You will implement a class Polynomial for storing and manipulating polynomial expressions. A polynomial is an expression of the form

akxk + … + a2x2 + a1x + a0

The number k is called the <strong>degree of the polynomial</strong> and the numbers a0, …, ak are called the <strong>coefficients</strong>.

Store each polynomial as a degree and <strong>a singly linked list</strong> of its coefficients, but “backwards”, i.e. with the lowest degree coefficient first.  (Backwards makes your program easier!) <u>Do NOT use a doubly linked list in this assignment!</u>

For example, the polynomial 4×3 + x + 7 would be stored as:

head_ptr –&gt; 7 –&gt; 1 –&gt; 0 –&gt; 4

degree:  3

Here the constant term, 7, is first, then the linear (x) term, 1, then the quadratic (x2) term, 0, and finally the highest degree term with a coefficient of 4. In addition, the degree of the polynomial, 3, is stored in the member variable degree.

Storing the polynomials in this order, rather than in the order in which we normally write them, will make it easier to perform arithmetic operations.

The class <em>invariant</em> (i.e., the thing that must be true about the class whenever a member function is <em>finished</em> making changes) is:

<ol>

 <li>The coefficients are stored in a linked list with the constant term at the front of the list and the highest order term at the end of the list.</li>

 <li>The zero polynomial is represented by a list with a single item, zero. The degree of the zero polynomial is 0.</li>

 <li>The list for a non-zero polynomial does not end with a zero coefficient. (In other words, the highest degree coefficient is only zero if this is the zero polynomial.)</li>

 <li>The value of the degreemember variable is one less than the length of the list.</li>

</ol>

What you have to handle:

<ul>

 <li>constructor that takes a vector of its coefficients in order from highest degree term to lowest</li>

 <li>+=</li>

 <li>+</li>

 <li>copy control, i.e. destructor, copy constructor and assignment operator</li>

 <li>==</li>

 <li>!=</li>

 <li>&lt;&lt; Use the caret ^ for exponentiation. So: 5x^3 represents five times the term with an exponent of three.</li>

 <li>Takes a single argument and evaluates the polynomial for that value of “X”.</li>

</ul>

<strong>Notes</strong>

<ul>

 <li>Coefficients can be either ints or doubles, as you prefer.</li>

 <li>Feel free to make your life easier by using the linked list code that we developed. Include the Node struct definition and function prototypes in your polynomial.h and the function implementations in polynomial.cpp.</li>

</ul>

<strong>Test program:</strong> attached is a test program.  Feel free to expand on it.  You may not be familiar with all of the syntax used in this program.

<ul>

 <li> This <em>manipulator</em>tells the output stream that when it is printing a bool value, true or false, to print it that way, i.e. as the strings “true” and “false”.  Without this manipulator, C++ will print true as 1 and false as 0.</li>

 <li>{2, 4, 8}.  The use of braces around a comma-delimited sequence of values can be used to initialize a vector to hold that sequence of values.  Please note that this use of braces requires C++11.</li>

</ul>