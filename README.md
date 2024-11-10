Print Hollow Pyramid Star Pattern
Lets have a look at the program to hollow pyramid star pattern in python

Python Program for Printing Hollow Pyramid Star Pattern
We are going to discuss two methods below –

Method 1
Run
row = 8

for i in range(row):
    for j in range(row - i):
        # prints left space in the same row
        print(' ', end='')

    for j in range(2 * i + 1):
        # printing the left boundary of triangle
        if j == 0:
            print('*', end='')

            # printing the right boundary of triangle
        elif j == 2 * i:
            print('*', end='')

            # printing the bottom boundary of triangle
        elif i == row - 1:
            print('*', end='')

        # printing spaces in the middle of the triangle
        else:
            print(' ', end='')

    print()  # printing new line
Output
        *
       * *
      *   *
     *     *
    *       *
   *         *
  *           *
 ***************
Method 1.1
The above method can also be condensed down from multiple else if conditions to single as shown below –

Run
row = 8

for i in range(row):
    for j in range(row - i):
        # prints left space in the same row
        print(' ', end='')

    for j in range(2 * i + 1):

        # printing the left boundary of triangle
        if j == 0 or j == 2 * i or i == row - 1:
            print('*', end='')

        # printing spaces in the middle of the triangle
        else:
            print(' ', end='')

    print()  # printing new line
Output
        *
       * *
      *   *
     *     *
    *       *
   *         *
  *           *
 ***************
Method 2
Run
num = 8
k = 0
for i in range(1, num + 1):
    # printing left spaces in rows
    for j in range(i, num):
        print(" ", end="")

    while k != (2 * i - 1):
        # printing left/right boundaries
        if k == 0 or k == 2 * i - 2:
            print("*", end="")
        # printing spaces in the middle of the triangle
        else:
            print(" ", end="")
        k = k + 1

    k = 0
    print()

# printing bottom boundary of the triangle
for i in range(0, 2 * num - 1):
    print("*", end="")
Output
        *
       * *
      *   *
     *     *
    *       *
   *         *
  *           *
 ***************
