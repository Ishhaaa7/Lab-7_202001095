# Lab-7_202001095

Name : Isha Popat
ID : 202001095
Date : 12-04-2023


Section A:
Consider a program for determining the previous date. Its input is
triple of day, month and year with the following ranges 1 <=
month <= 12, 1 <= day <= 31, 1900 <= year <= 2015.The possible
output dates would be previous date or invalid date. Design the
equivalence class test cases?
Answer:
Equivalence Classes:-
1. Months are less than 1.
2. Months are between 1 and 12.
3. Months are greater than 12.
4. Day is less than 1.
5. Day is between 1 and 31.
6. Day is greater than 31.
7. Year is less than 1900.
8. Year is between 1900 and 2015.
9. Year is greater than 2015.


![Screenshot 2023-04-12 231852](https://user-images.githubusercontent.com/123543637/231542007-75eb1930-facd-4a8b-b906-a9e9a2f1b88d.png)
![2021-03-06](https://user-images.githubusercontent.com/123543637/231542038-28bcae4c-0387-473f-82ee-46540dbe5439.png)


Programs:
P1: The function linearSearch searches for a value v in an array of
integers a. If v appears in the array
a, then the function returns the first index i, such that a[i] == v;
otherwise, -1 is returned.
int linearSearch(int v, int a[])
{
int i = 0; (1)
while (i < a.length) (2)
{
if (a[i] == v) (3)
return(i); (4)
i++; (5)
}
return (-1); (6)
}


![11](https://user-images.githubusercontent.com/123543637/231542636-882ef40f-e597-49d7-8654-b7b8dc179bec.png)
![12](https://user-images.githubusercontent.com/123543637/231542660-70fea363-8225-44f7-97c0-498933df8fa9.png)
![13](https://user-images.githubusercontent.com/123543637/231542677-08733a85-93d0-43f4-a378-b3234fed0a1b.png)




P2:The function countItem returns the number of times a value v
appears in an array of integers a.
int countItem(int v, int a[])
{
int count = 0;
for (int i = 0; i < a.length; i++)
{
if (a[i] == v) count++;
}
return (count);
}![21](https://user-images.githubusercontent.com/123543637/231546416-df53319b-4299-4fc1-9dfd-00ed54978fb0.png)


![22](https://user-images.githubusercontent.com/123543637/231546437-5d399087-2881-47fe-a62a-9a5f5a7a537c.png)

![23](https://user-images.githubusercontent.com/123543637/231543204-9d662543-1a63-4f89-b647-6786abb9c3ae.png)

P3: The function binarySearch searches for a value v in an
ordered array of integers a. If v appears in
the array a, then the function returns an index i, such that a[i] ==
v; otherwise, -1 is returned.
Assumption: the elements in the array a are sorted in
non-decreasing order.
int binarySearch(int v, int a[])
{
int lo,mid,hi;
lo = 0;
hi = a.length-1;
while (lo <= hi)
{
mid = (lo+hi)/2;
if (v == a[mid])
return (mid);
else if (v < a[mid])
hi = mid-1;
else
lo = mid+1;
}
return(-1);


![31](https://user-images.githubusercontent.com/123543637/231544814-c3f88999-feca-42e7-a576-bd906a273c1a.png)



![32](https://user-images.githubusercontent.com/123543637/231544885-6f270a77-ebbd-46b0-a48a-37910c545cb8.png)
![33](https://user-images.githubusercontent.com/123543637/231544928-dad8b395-b3b0-4e03-b4c3-1b79c68f44de.png)


P4: The following problem has been adapted from The Art of
Software Testing, by G. Myers (1979). The
function triangle takes three integer parameters that are
interpreted as the lengths of the sides of a
triangle. It returns whether the triangle is equilateral (three
lengths equal), isosceles (two lengths equal),
scalene (no lengths equal), or invalid (impossible lengths).
final int EQUILATERAL = 0;
final int ISOSCELES = 1;
final int SCALENE = 2;
final int INVALID = 3;
int triangle(int a, int b, int c)
{
if (a >= b+c || b >= a+c || c >= a+b)
return(INVALID);
if (a == b && b == c)
return(EQUILATERAL);
if (a == b || a == c || b == c)
return(ISOSCELES);
return(SCALENE);
}



![41](https://user-images.githubusercontent.com/123543637/231545090-8ab85c8e-f3a5-460e-987f-bf2fae14dbdd.png)
![42](https://user-images.githubusercontent.com/123543637/231545100-83f5ae58-10cc-4da4-9bee-38860fef7970.png)



P5: The function prefix (String s1, String s2) returns whether
or not the string s1 is a prefix
of string s2 (you may assume that neither s1 nor s2 is null).
public static boolean prefix(String s1, String s2)
{
if (s1.length() > s2.length())
{
return false;
}
for (int i = 0; i < s1.length(); i++)
{
if (s1.charAt(i) != s2.charAt(i))
{
return false;
}
}
return true;
}


![51](https://user-images.githubusercontent.com/123543637/231545230-4cc5d1aa-ce03-4c64-902f-958be23ba49a.png)

![52](https://user-images.githubusercontent.com/123543637/231545253-60897e0f-7334-49d9-b597-5f5b718c1185.png)


P6: Consider again the triangle classification program (P4)
with a slightly different specification: The program
reads floating values from the standard input. The three
values A, B, and C are interpreted as
representing the lengths of the sides of a triangle. The
program then prints a message to the standard output
that states whether the triangle, if it can be formed, is
scalene, isosceles, equilateral, or right angled.
Determine the following for the above program:
a) Identify the equivalence classes for the system
b) Identify test cases to cover the identified equivalence
classes. Also, explicitly mention which test case
would cover which equivalence class.
(Hint: you must need to be ensure that the identified set of
test cases cover all identified equivalence
classes)
c) For the boundary condition A + B > C case (scalene
triangle), identify test cases to verify the
boundary.
d) For the boundary condition A = C case (isosceles triangle),
identify test cases to verify the boundary.
e) For the boundary condition A = B = C case (equilateral
triangle), identify test cases to verify the boundary.
f) For the boundary condition A2 + B2 = C2 case (right-angle
triangle), identify test cases to verify the boundary.
g) For the non-triangle case, identify test cases to explore the
boundary.
h) For non-positive input, identify test points.
Ans:
a) Equivalence Classes:
1) Invalid inputs: When any of the input values are non-numeric or
negative.
2) Non-triangle: When the sum of the lengths of any two sides is less
than or equal to the length of the third side.
3) Equilateral triangle: When all sides are equal in length.
4) Isosceles triangle: When two sides are equal in length and the third
side is different.
5) Scalene triangle: When all sides are different in length.
6) Right-angled triangle: When the sum of the squares of the lengths of
the two shorter sides is equal to the square of the length of the
longest side.
b) Test cases:
1. Invalid inputs: "a", -5, "c"
2. Non-triangle: 1, 2, 5
3. Equilateral triangle: 3, 3, 3
4. Isosceles triangle: 5, 7, 5
5. Scalene triangle: 3, 4, 5
6. Right-angled triangle: 3, 4, 5
c) Test cases for boundary condition A + B > C:
1. 1, 2, 3
2. 3, 4, 7
3. 5, 6, 11
d) Test cases for boundary condition A = C:
1. 1, 2, 2
2. 4, 5, 4
3. 6, 7, 6
e) Test cases for boundary condition A = B = C:
1. 0.5, 0.5, 0.5
2. 1, 1, 1
3. 10, 10, 10
f) Test cases for boundary condition A^2 + B^2 = C^2:
1. 3, 4, 5
2. 5, 12, 13
3. 7, 24, 25
g) Test cases for non-triangle:
1. 1, 2, 3
2. 2, 3, 5
3. 4, 5, 9
h) Test cases for non-positive 
1. 0, 1, 2
2. -1, -2, -3

![61](https://user-images.githubusercontent.com/123543637/231545891-a92e81b9-a9a9-46ae-9b0c-23fce2ba1478.png)



Section B:
Below is the java code of pseudo code given in the question:

![secb1](https://user-images.githubusercontent.com/123543637/231545973-4c8a14fd-fd03-483d-a898-df73e51349fb.png)





![secb2](https://user-images.githubusercontent.com/123543637/231546002-0e4622b5-d67d-43f8-933e-bed0be61b1b7.png)



a. Test set for Statement Coverage:
The test set should cover every statement in the code at least once.
Test Set:
● p = new Point[]{new Point(0,0), new Point(1,1)}
● doGraham(p)
Explanation:
This test set contains two points, one with coordinates (0,0) and the other
with coordinates (1,1). The doGraham() method is called with these two
points as input. This test set will cover every statement in the code at least
once.
b. Test set for Branch Coverage:
The test set should cover every possible branch in the code.
Test Set:
● p = new Point[]{new Point(0,0), new Point(1,1), new Point(-1,-1)}
● doGraham(p)
Explanation:
This test set contains three points, one with coordinates (0,0), one with
coordinates (1,1) and one with coordinates (-1,-1). The doGraham() method
is called with these three points as input. This test set will cover every
possible branch in the code.
c. Test set for Basic Condition Coverage:
The test set should cover every possible condition in the code, including
both true and false evaluations.
Test Set:
● p = new Point[]{new Point(0,0), new Point(1,1), new Point(-1,-1)}
● doGraham(p)
Explanation:
This test set contains three points, one with coordinates (0,0), one with
coordinates (1,1) and one with coordinates (-1,-1). The doGraham() method
is called with these three points as input. This test set will cover every
possible condition in the code, including both true and false evaluations
