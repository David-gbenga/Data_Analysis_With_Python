This article gives a thorough explanation of sepcific Python Packages : Numpy and Pandas
	


INTRODUCTION
 Numpy and Pandas frameworks are libraries in Python programming language adapted particularly to achieve specific applications. This write-up gives a precise explanation of Numpy and Pandas Libraries and its application as summarized from the Lectures.
The IDE used for this project is Jupiter Notebook
Kindly note that the order of flow for explanation of codes will take this path





NUMPY
Numpy stands for numerical python. This library is used for specific mathematical applications.
Examples of these mathematical applications are given below.
(a)	Arrays:  Arrays can be created using the numpy library. To create single and multi-dimensional arrays, try the following codes.
First import the numpy then create the array as seen below.

Linear or one-dimensional array
import numpy as np
my_list1= [1,2,3,4]
my_array1=np.array(my_list1)
print(my_array1)
             [1 2 3 4] (This output shows the arrays created)

Two-dimensional Array
import numpy as np
my_list1= [1,2,3,4]
my_list2= [2,4,6,8]
my_array1=np.array([my_list1,my_list2])
print(my_array1) #The output below shows the arrays created)

      [[1 2 3 4]
      [2 4 6 8]]

(b)	Array dimensions using the “array.shape” function.
 my_list1= [1,2,3,4]
my_list2= [2,4,6,8]
my_array1=np.array([my_list1,my_list2])
print(my_array1.shape)  #(the output below describes the array as 2 rows and 3 columns)

     (2, 4) 


      (c)        Array type is achieved using the “array.dtype” funtion.
	my_list1= [1,2,3,4]
	my_list2= [2,4,6,8]
	my_array1=np.array([my_list1,my_list2])
	print(my_array1.dtype)

	int32  (This output describes an integer oriented array)

     (d)  Linear array with zeros
	New_array = np.zeros(5)
	print(New_array)
	[0. 0. 0. 0. 0.]

     (e)  Unitary Arrays is carried out using the “array.ones([row, column])
	New_array1 = np.ones([3,5])
	print(New_array1)
   	[[1. 1. 1. 1. 1.]
                 [1. 1. 1. 1. 1.]
                 [1. 1. 1. 1. 1.]]

      (f) Identity Array is created using “np.eye”
	New_array1 = np.eye(5)
	print(New_array1) #The output below gives an identity array

	[[1. 0. 0. 0. 0.]
 	 [0. 1. 0. 0. 0.]
	 [0. 0. 1. 0. 0.]
	 [0. 0. 0. 1. 0.]
                  [0. 0. 0. 0. 1.]] 





 (g) Arrays for Arithmetic Progression is achieved using “array.arange”
            New_array1 = np.arange(5,50,3)
            print(New_array1)

            [5 8 11 14 17 20 23 26 29 32 35 38 41 44 47]

(h)Scalar Operations: An example of this operation is the (i) scalar multiplication
	
                 import numpy as np
	my_array1=np.array([[1,2,3,4],[2,4,6,8]])
	my_array2=my_array1*my_array1
	print(my_array2)
	[[ 1  4  9 16]
	 [ 4 16 36 64]]

(ii)Exponential functions
   	import numpy as np
	my_array1=np.array([[1,2,3,4],[2,4,6,8]])
	my_array3=my_array1**3
	my_array4=my_array3 - my_array1
	print(my_array4)
	[[  0   6  24  60]
 	[  6  60 210 504]]

 (iii)Reciprocals: 
                 import numpy as np #array division
	my_array1=np.array([[1,2,3,4],[2,4,6,8]])
	print (1/my_array1)
	[[1.         0.5        0.33333333 0.25      ]
 	[0.5        0.25       0.16666667 0.125     ]]







 (iv)Array  ranging and slicing
	#array ranging and slicing 
	import numpy as np
	number_15 = np.arange(0,15)
	print(number_15)
	print(number_15[0:6])
       [ 0  1  2  3  4  5  6  7  8  9 10 11 12 13 14]
	[0 1 2 3 4 5]

(v) Exponentials of Arrays
    import numpy as np
    my_array1=np.array([[1,2,3,4],[2,4,6,8]])
    my_array3=my_array1**3
    print(my_array3)
    [[  1   8  27  64]
    [  8  64 216 512]]

(vi) Array subraction
    import numpy as np
   my_array1=np.array([[1,2,3,4],[2,4,6,8]])
   my_array3=my_array1**3
   my_array4=my_array3 - my_array1
   print(my_array4)

Special Applications in Arrays
(1)	Array indexing
            #array indexing 
             import numpy as np
             number_15 = np.arange(0,15)
            print(number_15[0])
            print(number_15[1])
            print(number_15[2])
            print(number_15[5]

           0
           1
           2
           5

(2) Array element replacement
         Import numpy as np
         #array replacement
         number_15 = np.arange(0,15)
          number_15[0:4]= 10
          print(number_15)

          [10 10 10 10  4  5  6  7  8  9 10 11 12 13 14]

(3) Special slicing techniques
      number_15 = np.arange(0,15)
      number_replaced = number_15 [0:4]
      number_15[:]=12
      print(number_replaced)

      [12 12 12 12]

(I)	Exploring Elements of an array via “array indexing” 
import numpy as np
my_array1=np.array([[1,12,3,4,5],[2,4,6,8,10],[3,5,7,9,11]])
print(my_array1[0]) #This will give elements of row 1
print(my_array1[0][1])#This will give the element of the 1st column in row 1
print(my_array1[0:1,0:2])#This gives values of column 1 and 2 in row one.  Note that column numbering starts with zero as well.
print(my_array1[0:2,0:1])
print(my_array1[0:2,0:2])
print(my_array1[0:3,0:4])
print(my_array1[:2,1:])

Some other numpy functions are listed below with examples
import numpy as np
A = np.arange(1,15,2)
print("A is")
print(A)

B = np.sqrt(A)
print("B is")
print(B)

C = np.exp (A)
print ("C is")
print(C)

D = np.add(A,B)
print("D is")
print(D)

E= np.maximum(A,B)
print("E is")
print(E)

A is
[ 1  3  5  7  9 11 13]
B is
[1.         1.73205081 2.23606798 2.64575131 3.         3.31662479
 3.60555128]
C is
[2.71828183e+00 2.00855369e+01 1.48413159e+02 1.09663316e+03
 8.10308393e+03 5.98741417e+04 4.42413392e+05]
D is
[ 2.          4.73205081  7.23606798  9.64575131 12.         14.31662479
 16.60555128]
E is
[ 1.  3.  5.  7.  9. 11. 13.]


Saving and Loading Arrays 

Saving and loading single arrays: Use the “np.save” function to save followed by “file name” and    array name all in bracket. Simply load a saved file with the “np.load” function followed by the file name and a .npy extension added to it. An example is sited below

import numpy as np
array_test = np.arange(30) 
np.save("saved_array",array_test)

new_array=np.load('saved_array.npy')
print(new_array) #The single array previously saved is loaded and printed below

output

[ 0  1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16 17 18 19 20 21 22 23
 24 25 26 27 28 29]

Saving multiple arrays
#for multiple arrays, use distinct variables to represent each array and use the np.savez function. Multiple arrays are saved as a zip folder. When loading multiple arrays use the distinct variables to call out each array. An example is sited below. 

import numpy as np
arrayA=np.arange(10)
arrayB=np.arange(15)
np.savez('saved_archive.npz', x=arrayA, y=arrayB)

loadedArray=np.load('saved_archive.npz')
print ("x is ")
print(loadedArray['x'])
print ("y is ")
print(loadedArray['y'])

Output
x is 
[0 1 2 3 4 5 6 7 8 9]
y is 
[ 0  1  2  3  4  5  6  7  8  9 10 11 12 13 14]


Alternatively, arrays can be saved as text files and loaded on text readable platforms
Saving an array as a text file. Note that arrays loaded as text files are automatically converted to  float values. 

import numpy as np
arrayA=np.arange(10)
np.savetxt("textfile1",arrayA,delimiter=",")

Load_textfiles = np.loadtxt("textfile1",delimiter=",")
print(Load_textfiles)

output
[0. 1. 2. 3. 4. 5. 6. 7. 8. 9.]

MATPLOTLIB
A quick introduction to another library called matplotlib. This library can be used along with numpy functions to plot graphs. 
Plotting graphs with a combination of numpy and matplotlib functions

import numpy as np
import matplotlib.pyplot as plt

axes_values = np.arange(-100,100,10) 
dx, dy= np.meshgrid(axes_values,axes_values)
print(dx)
print (dy)
function = 2*dx+3*dy
print(function)
plt.imshow(function) # this function helps to plot the graph
plt.title("Function of plot 2*dx+3*dy") # this function helps to give a title to the plot
plt.colorbar() #this function helps to give a color legend showing the range of numbers
plt.savefig("plottedgraph.png") # this is used to save the plotted graph


Output:

dx is
[[-100  -90  -80  -70  -60  -50  -40  -30  -20  -10    0   10   20   30
    40   50   60   70   80   90]
 [-100  -90  -80  -70  -60  -50  -40  -30  -20  -10    0   10   20   30
    40   50   60   70   80   90]
 [-100  -90  -80  -70  -60  -50  -40  -30  -20  -10    0   10   20   30
    40   50   60   70   80   90]
 [-100  -90  -80  -70  -60  -50  -40  -30  -20  -10    0   10   20   30
    40   50   60   70   80   90]
 [-100  -90  -80  -70  -60  -50  -40  -30  -20  -10    0   10   20   30
    40   50   60   70   80   90]
 [-100  -90  -80  -70  -60  -50  -40  -30  -20  -10    0   10   20   30
    40   50   60   70   80   90]
 [-100  -90  -80  -70  -60  -50  -40  -30  -20  -10    0   10   20   30
    40   50   60   70   80   90]
 [-100  -90  -80  -70  -60  -50  -40  -30  -20  -10    0   10   20   30
    40   50   60   70   80   90]
 [-100  -90  -80  -70  -60  -50  -40  -30  -20  -10    0   10   20   30
    40   50   60   70   80   90]
 [-100  -90  -80  -70  -60  -50  -40  -30  -20  -10    0   10   20   30
    40   50   60   70   80   90]
 [-100  -90  -80  -70  -60  -50  -40  -30  -20  -10    0   10   20   30
    40   50   60   70   80   90]
 [-100  -90  -80  -70  -60  -50  -40  -30  -20  -10    0   10   20   30
    40   50   60   70   80   90]
 [-100  -90  -80  -70  -60  -50  -40  -30  -20  -10    0   10   20   30
    40   50   60   70   80   90]
 [-100  -90  -80  -70  -60  -50  -40  -30  -20  -10    0   10   20   30
    40   50   60   70   80   90]
 [-100  -90  -80  -70  -60  -50  -40  -30  -20  -10    0   10   20   30
    40   50   60   70   80   90]
 [-100  -90  -80  -70  -60  -50  -40  -30  -20  -10    0   10   20   30
    40   50   60   70   80   90]
 [-100  -90  -80  -70  -60  -50  -40  -30  -20  -10    0   10   20   30
    40   50   60   70   80   90]
 [-100  -90  -80  -70  -60  -50  -40  -30  -20  -10    0   10   20   30
    40   50   60   70   80   90]
 [-100  -90  -80  -70  -60  -50  -40  -30  -20  -10    0   10   20   30
    40   50   60   70   80   90]
 [-100  -90  -80  -70  -60  -50  -40  -30  -20  -10    0   10   20   30
    40   50   60   70   80   90]]
dy is
[[-100 -100 -100 -100 -100 -100 -100 -100 -100 -100 -100 -100 -100 -100
  -100 -100 -100 -100 -100 -100]
 [ -90  -90  -90  -90  -90  -90  -90  -90  -90  -90  -90  -90  -90  -90
   -90  -90  -90  -90  -90  -90]
 [ -80  -80  -80  -80  -80  -80  -80  -80  -80  -80  -80  -80  -80  -80
   -80  -80  -80  -80  -80  -80]
 [ -70  -70  -70  -70  -70  -70  -70  -70  -70  -70  -70  -70  -70  -70
   -70  -70  -70  -70  -70  -70]
 [ -60  -60  -60  -60  -60  -60  -60  -60  -60  -60  -60  -60  -60  -60
   -60  -60  -60  -60  -60  -60]
 [ -50  -50  -50  -50  -50  -50  -50  -50  -50  -50  -50  -50  -50  -50
   -50  -50  -50  -50  -50  -50]
 [ -40  -40  -40  -40  -40  -40  -40  -40  -40  -40  -40  -40  -40  -40
   -40  -40  -40  -40  -40  -40]
 [ -30  -30  -30  -30  -30  -30  -30  -30  -30  -30  -30  -30  -30  -30
   -30  -30  -30  -30  -30  -30]
 [ -20  -20  -20  -20  -20  -20  -20  -20  -20  -20  -20  -20  -20  -20
   -20  -20  -20  -20  -20  -20]
 [ -10  -10  -10  -10  -10  -10  -10  -10  -10  -10  -10  -10  -10  -10
   -10  -10  -10  -10  -10  -10]
 [   0    0    0    0    0    0    0    0    0    0    0    0    0    0
     0    0    0    0    0    0]
 [  10   10   10   10   10   10   10   10   10   10   10   10   10   10
    10   10   10   10   10   10]
 [  20   20   20   20   20   20   20   20   20   20   20   20   20   20
    20   20   20   20   20   20]
 [  30   30   30   30   30   30   30   30   30   30   30   30   30   30
    30   30   30   30   30   30]
 [  40   40   40   40   40   40   40   40   40   40   40   40   40   40
    40   40   40   40   40   40]
 [  50   50   50   50   50   50   50   50   50   50   50   50   50   50
    50   50   50   50   50   50]
 [  60   60   60   60   60   60   60   60   60   60   60   60   60   60
    60   60   60   60   60   60]
 [  70   70   70   70   70   70   70   70   70   70   70   70   70   70
    70   70   70   70   70   70]
 [  80   80   80   80   80   80   80   80   80   80   80   80   80   80
    80   80   80   80   80   80]
 [  90   90   90   90   90   90   90   90   90   90   90   90   90   90
    90   90   90   90   90   90]]
function is
[[-500 -480 -460 -440 -420 -400 -380 -360 -340 -320 -300 -280 -260 -240
  -220 -200 -180 -160 -140 -120]
 [-470 -450 -430 -410 -390 -370 -350 -330 -310 -290 -270 -250 -230 -210
  -190 -170 -150 -130 -110  -90]
 [-440 -420 -400 -380 -360 -340 -320 -300 -280 -260 -240 -220 -200 -180
  -160 -140 -120 -100  -80  -60]
 [-410 -390 -370 -350 -330 -310 -290 -270 -250 -230 -210 -190 -170 -150
  -130 -110  -90  -70  -50  -30]
 [-380 -360 -340 -320 -300 -280 -260 -240 -220 -200 -180 -160 -140 -120
  -100  -80  -60  -40  -20    0]
 [-350 -330 -310 -290 -270 -250 -230 -210 -190 -170 -150 -130 -110  -90
   -70  -50  -30  -10   10   30]
 [-320 -300 -280 -260 -240 -220 -200 -180 -160 -140 -120 -100  -80  -60
   -40  -20    0   20   40   60]
 [-290 -270 -250 -230 -210 -190 -170 -150 -130 -110  -90  -70  -50  -30
   -10   10   30   50   70   90]
 [-260 -240 -220 -200 -180 -160 -140 -120 -100  -80  -60  -40  -20    0
    20   40   60   80  100  120]
 [-230 -210 -190 -170 -150 -130 -110  -90  -70  -50  -30  -10   10   30
    50   70   90  110  130  150]
 [-200 -180 -160 -140 -120 -100  -80  -60  -40  -20    0   20   40   60
    80  100  120  140  160  180]
 [-170 -150 -130 -110  -90  -70  -50  -30  -10   10   30   50   70   90
   110  130  150  170  190  210]
 [-140 -120 -100  -80  -60  -40  -20    0   20   40   60   80  100  120
   140  160  180  200  220  240]
 [-110  -90  -70  -50  -30  -10   10   30   50   70   90  110  130  150
   170  190  210  230  250  270]
 [ -80  -60  -40  -20    0   20   40   60   80  100  120  140  160  180
   200  220  240  260  280  300]
 [ -50  -30  -10   10   30   50   70   90  110  130  150  170  190  210
   230  250  270  290  310  330]
 [ -20    0   20   40   60   80  100  120  140  160  180  200  220  240
   260  280  300  320  340  360]
 [  10   30   50   70   90  110  130  150  170  190  210  230  250  270
   290  310  330  350  370  390]
 [  40   60   80  100  120  140  160  180  200  220  240  260  280  300
   320  340  360  380  400  420]
 [  70   90  110  130  150  170  190  210  230  250  270  290  310  330
   350  370  390  410  430  450]]

 




Conditional Statements
Datasets from arrays can be assessed using conditional statements

x=np.array([100,400,500,600])
y=np.array([10,15,20,25])
condition=np.array([True,True,False,False])
z= [a if cond else b for a,cond,b in zip(x,condition,y)] #this conditional statement gives…
print(z)

Output

[100., 400, 20, 25]


Alternatively, the function np.where() can also be used to make a meaning from the given variables
x=np.array([100,400,500,600])
y=np.array([10,15,20,25])
condition=np.array([True,True,False,False])
#np.where (#condition,#value for yes, #value for no)
z1=np.where(condition,x,y)

print(z1)

Output

[100., 400, 20, 25]

import numpy as np
x=np.array([100,25,30,600])
z2=np.where(x>40,1,0) # If the value of x is greater than 40 display 1 #otherwise display 0
print(z2)

Output
[1 0 0 1]




PANDAS
Pandas is a library in Python specifically used for analyzing data and used to perform mathematical operations. Below are some methods by which Pandas is used in a Jupiter Notebook. Just like Numpy, Pandas is also imported. 

import pandas as pd
from pandas import Series
import numpy as np
object = Series([5,10,15,20,25]) #Series function helps to create objects with index and respective values.
print(object)

print(object.values) #this function is used to print just the values.

print(object.index) #this function is used to print the index

#using Numpy to create series
array1 =([1,2,3,4,5,6,7,8,9,10])
num_series = Series(array1)
print(num_series)

The Outputs for the above print() functions are found below.

print(object)

0     5
1    10
2    15
3    20
4    25
dtype: int64

print(object.values)
[ 5 10 15 20 25]

print(object.index)
RangeIndex(start=0, stop=5, step=1)

print(num_series)
0     1
1     2
2     3
3     4
4     5
5     6
6     7
7     8
8     9
9    10
dtype: int64


import pandas as pd
from pandas import Series
import numpy as np
object = Series([5,10,15,20,25])
#change indexes
change_index =Series(object,index=[1,2,3,4,5,6])
#Note that the index ‘0” and its value is removed as soon as you change the index to start from one and not zero. Also giving an entirely different index to this value will automatically require new values. 
print(change_index)


1    10.0
2    15.0
3    20.0
4    25.0
5     NaN
6     NaN
dtype: float64


Representing Index with Strings

import pandas as pd
from pandas import Series
import numpy as np
#representing index with strings
revenue = Series([5,10,15,20], index=['ola','uber','grab','gojek'])
print(revenue)

Output
ola       5
uber     10
grab     15
gojek    20
dtype: int64


Creating a Dictionary
revenue = Series([5,10,15,20], index=['ola','uber','grab','gojek'])
revenue_dict= revenue.to_dict()
print(revenue_dict)

{'ola': 5, 'uber': 10, 'grab': 15, 'gojek': 20}



Conditional statement
Conditional statements can be used to select specific values from a dataset
revenue = Series([5,10,15,20], index=['ola','uber','grab','gojek'])
print(" Companies with Revenue greater or equals to 15 is")
print(revenue[revenue>=15])

Companies with Revenue greater or equals to 15 is
grab     15
gojek    20
dtype: int64


Using boolean conditions 
revenue = Series([5,10,15,20], index=['ola','uber','grab','gojek'])
print('ola' in revenue) #this index and value are present so the output will be True
print('taxify'in revenue)# this is not present so output will be False

True
False


 Boolean functions used for value confirmation

import pandas as pd
from pandas import Series
import numpy as np
revenue = Series([5,10,15,20], index=['ola','uber','grab','gojek'])
print(pd.isnull(revenue)) #this function gives  false as output if value is present
ola      False
uber     False
grab     False
gojek    False
dtype: bool

print(pd.notnull(revenue))#this function gives a true output if value is present

ola      True
uber     True
grab     True
gojek    True
dtype: bool


Series Addition
 Note that for addition to go smoothly, equal number of indexes and values are required. In the case of 
import pandas as pd
from pandas import Series
import numpy as np
revenue = Series([5,10,15,20], index=['ola','uber','grab','gojek'])
revenue2 = Series([10,20,30,40], index=['ola','uber','grab','gojek'])
print(revenue+revenue2)


ola      15
uber     30
grab     45
gojek    60
dtype: int64


Copying From the Clipboard 

import pandas as pd
from pandas import Series,DataFrame
import numpy as np
Copied_data = pd.read_clipboard() #This function “.read_clipboard() is used to copy from the clipboard after selecting & copying from a document
print(Copied_data)

       Name   Region Rate of goods sold Quantity     Revenue  Cost    Profit
0       John      Central            500        22               11,000     50      10,950
1      Peter        East               501        24              12,123    100     12,023
2    Matthew     West            501        28              14,169    200     13,969
3      Segun        South           502        41               20,590    307    20,283
4    Desmond    North           502        41               20,611    400    20,211
5      Ahmed     Central          503        43               21,565    435    21,129
6    Johnson     East               503        44                21,903    609    21,294
7    Bernard     West              504        44                21,925    703   21,222
8       Jaye        South              504        44               22,122    796    21,326
9    Desmond    North            505        44                22,144    890  21,254
10    Bleach     Central            505        44                22,243    985  21,259
11   Collins     East                  506        44                22,266  1,079  21,187
12     Jamiu     West               506        46                 23,286  1,173  22,113
13      Lola    South                 507        46                 23,309  1,268  22,041
14  Jennifer    North              507        46                 23,376  1,363  22,013
15   Goliath  Central              508        47                 24,053  1,457  22,596
16    Bastos     East                 508        48                 24,604  1,551  23,054
17      Zino     West                 509        51                 25,850  1,643  24,207
18     Yusuf    South                509        52                 26,345  1,737  24,607


Exploring a Dataset with rows and columns
import pandas as pd
from pandas import Series,DataFrame
import numpy as np
Copied_data = pd.read_clipboard()
print(Copied_data.columns)

Output
Index(['Name', 'Region', 'Rate  of goods sold', 'Quantity', 'Revenue', 'Cost ',
       'Profit'],
      dtype='object')



To access the values of a column e.g
print(Copied_data['Quantity'])
0     22
1     24
2     28
3     41
4     41
5     43
6     44
7     44
8     44
9     44
10    44
11    44
12    46
13    46
14    46
15    47
16    48
17    51
18    52
Name: Quantity, dtype: int64


To select different columns use the DataFrame function
DataFrame(Copied_data, columns=['Name','Quantity','Cost','Revenue','Profit'])


To select the first three rows at the top of the column 
topThreeRows = Copied_data.head(3)
print(topThreeRows)

      Name   Region  Rate  of goods sold  Quantity Revenue Cost   Profit
0     John  Central                  500        22  11,000    50  10,950
1    Peter     East                  501        24  12,123   100  12,023
2  Matthew     West                  501        28  14,169   200  13,969



To select the last two rows at the bottom of the column 
LastThreeRows = Copied_data.tail(3)
print(LastThreeRows)

      Name Region  Rate  of goods sold  Quantity Revenue  Cost   Profit
16  Bastos   East                  508        48  24,604  1,551  23,054
17    Zino   West                  509        51  25,850  1,643  24,207
18   Yusuf  South                  509        52  26,345  1,737  24,607




RE-assigning values to a Dataset
import pandas as pd
from pandas import Series,DataFrame
import numpy as np
Copied_data = pd.read_clipboard()
#USING ARRAYS FROM NUMPY
#Cost_include=np.array([200,400,600,800,1000,1200])
#Copied_data["Expense"] = Cost_include
#print(Copied_data)

Name   Region  Rate  of goods sold  Quantity Revenue  Cost   Profit  \
0       John  Central                  500        22  11,000     50  10,950   
1      Peter     East                  501        24  12,123    100  12,023   
2    Matthew     West                  501        28  14,169    200  13,969   
3      Segun    South                  502        41  20,590    307  20,283   
4    Desmond    North                  502        41  20,611    400  20,211   
5      Ahmed  Central                  503        43  21,565    435  21,129   
6    Johnson     East                  503        44  21,903    609  21,294   
7    Bernard     West                  504        44  21,925    703  21,222   
8       Jaye    South                  504        44  22,122    796  21,326   
9    Desmond    North                  505        44  22,144    890  21,254   
10    Bleach  Central                  505        44  22,243    985  21,259   
11   Collins     East                  506        44  22,266  1,079  21,187   
12     Jamiu     West                  506        46  23,286  1,173  22,113   
13      Lola    South                  507        46  23,309  1,268  22,041   
14  Jennifer    North                  507        46  23,376  1,363  22,013   
15   Goliath  Central                  508        47  24,053  1,457  22,596   
16    Bastos     East                  508        48  24,604  1,551  23,054   
17      Zino     West                  509        51  25,850  1,643  24,207   
18     Yusuf    South                  509        52  26,345  1,737  24,607   

    Expense  
0     200.0  
1     400.0  
2     600.0  
3     800.0  
4    1000.0  
5    1200.0  
6       NaN  
7       NaN  
8       NaN  
9       NaN  
10      NaN  
11      NaN  
12      NaN  
13      NaN  
14      NaN  
15      NaN  
16      NaN  
17      NaN  
18      NaN  







import pandas as pd
from pandas import Series,DataFrame
import numpy as np
Copied_data = pd.read_clipboard()

DELETE FUNCTION: This is used to delete a column in a dataset
del Copied_data['Profit']
print(Copied_data)


Name   Region  Rate  of goods sold  Quantity Revenue  Cost 
0       John  Central                  500        22  11,000     50
1      Peter     East                  501        24  12,123    100
2    Matthew     West                  501        28  14,169    200
3      Segun    South                  502        41  20,590    307
4    Desmond    North                  502        41  20,611    400
5      Ahmed  Central                  503        43  21,565    435
6    Johnson     East                  503        44  21,903    609
7    Bernard     West                  504        44  21,925    703
8       Jaye    South                  504        44  22,122    796
9    Desmond    North                  505        44  22,144    890
10    Bleach  Central                  505        44  22,243    985
11   Collins     East                  506        44  22,266  1,079
12     Jamiu     West                  506        46  23,286  1,173
13      Lola    South                  507        46  23,309  1,268
14  Jennifer    North                  507        46  23,376  1,363
15   Goliath  Central                  508        47  24,053  1,457
16    Bastos     East                  508        48  24,604  1,551
17      Zino     West                  509        51  25,850  1,643
18     Yusuf    South                  509        52  26,345  1,737


Indexes of columns, series and dataframes
import pandas as pd
from pandas import Series,DataFrame
Series1= Series([1,2,3,4,5],index =['a','b','c','d','e'])
print(Series1)

a    1
b    2
c    3
d    4
e    5
dtype: int64


Reindexing function is used to add new index to a series
Series2 = Series1.reindex(['a','b','c','d','e','f'])
print(Series2)

a    1.0
b    2.0
c    3.0
d    4.0
e    5.0
f    NaN
dtype: float64


import pandas as pd
from pandas import Series,DataFrame
Series1= Series([1,2,3,4,5],index =['a','b','c','d','e'])
print(Series1)

a    1
b    2
c    3
d    4
e    5
dtype: int64



#fill_value is used to add value for a new index.
Series3 = Series1.reindex(['a','b','c','d','e','f'], fill_value=10)
a     1
b     2
c     3
d     4
e     5
f    10
dtype: int64



import pandas as pd
from pandas import Series,DataFrame
Cars = Series(['audi','toyota', 'honda', 'mazda', 'Nissan'], index=['1','2','3','4','5'])
print(Cars)
1      audi
2    toyota
3     honda
4     mazda
5    Nissan
dtype: object



ffill and range function used along with reindex to add values constantly per interval

Cars1=Series(['audi','toyota', 'honda', 'mazda', 'Nissan'], index=[0,3,5,7,9])
Ranger=range(9)
cars_autofill = Cars1.reindex(Ranger,method='ffill')
print(cars_autofill)

0      audi
1      audi
2      audi
3    toyota
4    toyota
5     honda
6     honda
7     mazda
8     mazda
dtype: object



#Exploring with DataFrames to add rows and columns 
import numpy as np
from numpy.random import randn
import pandas as pd
from pandas import DataFrame, Series


Data_set1 = DataFrame(randn(25).reshape(5,5), index=['a','b','c','d','e'], columns=['c1','c2','c3','c4','c5'])
print(Data_set1)

              c1        c2                c3                  c4           c5
a -0.222418  2.093416 -0.537713 -0.698969 -1.234190
b  0.393166  0.447960 -1.021820  0.325406  0.899411
c -0.790347 -1.830439 -1.191472  0.847349 -0.655643
d  0.475402 -0.562171 -0.504296 -0.479039 -1.056312
e  0.448952 -0.685388 -0.902042  0.549840  0.747700







Adding a new row
Data_rowadd= Data_set1.reindex(['a','b','c','d','e','f','g'])
print(Data_rowadd)

         c1                 c2               c3                 c4        c5
a -0.222418  2.093416 -0.537713 -0.698969 -1.234190
b  0.393166  0.447960 -1.021820  0.325406  0.899411
c -0.790347 -1.830439 -1.191472  0.847349 -0.655643
d  0.475402 -0.562171 -0.504296 -0.479039 -1.056312
e  0.448952 -0.685388 -0.902042  0.549840  0.747700
f       NaN       NaN       NaN       NaN       NaN
g       NaN       NaN       NaN       NaN       NaN



Adding new columns
Data_columnadd= Data_set1.reindex(columns=['c1','c2','c3','c4','c5','c6','c7'])
print(Data_columnadd)


              c1            c2              c3                 c4           c5           c6     c7
a -0.222418  2.093416 -0.537713 -0.698969 -1.234190 NaN NaN
b  0.393166  0.447960 -1.021820  0.325406  0.899411 NaN NaN
c -0.790347 -1.830439 -1.191472  0.847349 -0.655643 NaN NaN
d  0.475402 -0.562171 -0.504296 -0.479039 -1.056312 NaN NaN
e  0.448952 -0.685388 -0.902042  0.549840  0.747700 NaN NaN




#Exploring with DataFrames to add rows and columns using ix function
import numpy as np
from numpy.random import randn
import pandas as pd
from pandas import DataFrame, Series
data_set1 = DataFrame(randn(25).reshape(5,5), index=['a','b','c','d','e'], columns=['c1','c2','c3','c4','c5'])
print(data_set1)

  c1        c2        c3        c4        c5
a  1.485586 -0.537576 -0.251050 -0.484615 -0.770363
b  0.654626  1.984487 -0.163649 -0.581720 -1.260774
c -1.488676 -1.725857 -0.113776 -0.155851 -0.440381
d -0.473619 -0.134187 -0.242518 -0.186747  0.104514
e  0.428608  0.417520  0.479541  0.277526 -3.307126












#The drop function is used delete an index and its value
import pandas as pd
from numpy.random import randn
from pandas import Series,DataFrame
Cars = Series(['audi','toyota', 'honda', 'mazda', 'Nissan'], index=['1','2','3','4','5'])
Cars_reviewed=Cars.drop('3')
print(Cars_reviewed)

1      audi
2    toyota
4     mazda
5    Nissan
dtype: object


#Drop also works with DataFrames as well. Note that you must drop with respect to the axis of the index
Data_Car_prices=DataFrame(np.arange(25).reshape(5,5), columns=['Roll-Royce', 'BMW', 'Audi', 'Toyota','Nissan'], index=['Price2001','Price2002','Price2003','Price2004','Price2005'])
print(Data_Car_prices)
              Roll-Royce  BMW Audi  Toyota  Nissan
Price2001           0    1           2       3       4
Price2002           5    6           7       8       9
Price2003          10   11       12      13      14
Price2004          15   16       17      18      19
Price2005          20   21       22      23      24



Cars_cardrop = Data_Car_prices.drop('BMW', axis=1)
print(Cars_cardrop)

           Roll-Royce  Audi  Toyota  Nissan
Price2001           0     2       3       4
Price2002           5     7       8       9
Price2003          10    12      13      14
Price2004          15    17      18      19
Price2005          20    22      23      24



Drop function continued 
import pandas as pd
import numpy as np
from numpy.random import randn
from pandas import Series,DataFrame

Cars2 = Series(['0','1','2','3','4',np.NaN,'5','6'])
print(Cars2.dropna())

0    0
1    1
2    2
3    3
4    4
6    5
7    6
dtype: object


my_array= np.array([[1,2,3,np.NaN,5],[np.NaN,4,6,8,10],[1,3,5,7,np.NaN]])
Data_Car_prices=DataFrame(my_array,index=['a','b','c'], columns=['c1','c2','c3','c4','c5']) 
print(Data_Car_prices)

Output
      c1   c2   c3   c4    c5
a  1.0  2.0  3.0  NaN   5.0
b  NaN  4.0  6.0  8.0  10.0
c  1.0  3.0  5.0  7.0   NaN

Function “dropna()” alongside “axis”when used with dataframes remove all columns having empty values
Data_dropna =Data_Car_prices.dropna(axis=1)
print(Data_dropna)


Output
    c2   c3
a  2.0  3.0
b  4.0  6.0
c  3.0  5.0


Using dropna() for dataframe causes all column or row with a NaN value to be totally deleted,                     therefore use axis method which deletes only empty columns

my_array1= np.array([[1,2,3,np.NaN,5],[np.NaN,4,6,8,10],[np.NaN,np.NaN,np.NaN,np.NaN,np.NaN]])
Data_Car_prices1=DataFrame(my_array1,index=['a','b','c'], columns=['c1','c2','c3','c4','c5'])

#Note
Data_dropna11 =Data_Car_prices1.dropna
print('Data_dropna11 is')
print(Data_dropna11)

Output

Data_dropna11 is
Empty DataFrame
Columns: [c1, c2, c3, c4, c5]
Index: []


Thresh is used to denote the dataset value delete limit. if thresh =3 
then any row with less than 3 dataset will be deleted
my_array1= np.array([[1,2,3,np.NaN,5],[np.NaN,4,6,8,10],[np.NaN,np.NaN,np.NaN,np.NaN,np.NaN]])
Data_Car_prices1=DataFrame(my_array1,index=['a','b','c'], columns=['c1','c2','c3','c4','c5'])
Data_dropna2 =Data_Car_prices1.dropna(thresh=3)
print(Data_dropna2)

Output

c1   c2   c3   c4    c5
a  1.0  2.0  3.0  NaN   5.0
b  NaN  4.0  6.0  8.0  10.0

fiilna function used to fill empty indexes
df1=Series(['audi','toyota', 'honda', 'mazda', 'Nissan',np.NaN], index=['1','2','3','4','5','6'])
print(df1)

      audi
2    toyota
3     honda
4     mazda
5    Nissan
6       NaN
dtype: object

fillup=df1.fillna(0)
print(fillup)
1      audi
2    toyota
3     honda
4     mazda
5    Nissan
6         0
dtype: object



Selecting and Modifying Entries
import pandas as pd
from numpy.random import randn
from pandas import Series,DataFrame
Modify_data=Series([100,200,300,400,500,600], index=['C','A','N','T','G','S'])
print(Modify_data)
C    100
A    200
N    300
T    400
G    500
S    600
dtype: int64



print(Modify_data['C'])# i have a challenge printing more than one indexes
Output
100



#using number indexes 
print(Modify_data[3])

output
400


print(Modify_data[0:3])
C    100
A    200
N    300
dtype: int64


#conditional indexing techniques
print(Modify_data[Modify_data>300])

T    400
G    500
S    600
dtype: int64


#Selecting and Modifying Entries in DataFrames
import pandas as pd
from numpy.random import randn
from pandas import Series,DataFrame
data_set = DataFrame(randn(25).reshape(5,5), index=['a','b','c','d','e'], columns=['c1','c2','c3','c4','c5'])
print(data_set)

          c1                c2              c3                  c4           c5
a  1.468509 -0.921706  0.371934  1.167857 -0.827985
b  0.750771  0.186614  0.415566  0.109720 -0.405131
c -0.445419 -1.697987  0.586300  0.516302 -1.659102
d -1.061300 -0.434417 -0.205844  0.065825  0.453883
e  0.824453 -0.673503  0.380882  1.026395  2.702574



print(data_set['c1']) # i also had a challenge printing values of more than one column whiles selecting indexes would give error
a    1.468509
b    0.750771
c   -0.445419
d   -1.061300
e    0.824453
Name: c1, dtype: float64




print(data_set>0.3) this gives a bolean response

      c1     c2     c3     c4     c5
a   True  False   True   True  False
b   True  False   True  False  False
c  False  False   True   True  False
d  False  False  False  False   True
e   True  False   True   True   True



Data Alignment during addition with series oriented datasets
import pandas as pd
import numpy as np
from numpy.random import randn
from pandas import Series,DataFrame
import pandas as pd

Series1=Series([100,200,300,400,500,600], index=['C','A','N','T','G','S'])
Series2=Series([100,200,300,400,np.NaN,np.NaN], index=['C','A','N','T','G','S'])
print(Series1 +Series2) Note that the indexes without values are not added even when the other indexes of the other series has values

C    200.0
A    400.0
N    600.0
T    800.0
G      NaN
S      NaN
dtype: float64


