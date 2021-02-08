# Basic_Python_programs
Basics program to learn python
#1. Write a program which will find factors of given number and find whether the
factor is even or odd.

Code:

n=int(input('enter the number'))
print("The factors of",n,"are:")
for i in range(1, n+1):
    if(n % i == 0):
        print(i)
        
if(n%2==0):
    print('number is even')
else:
    print('number is odd')

Output:

enter the number50
The factors of 50 are:
1
2
5
10
25
50
number is even






#2. Write a code which accepts a sequence of words as input and prints the words in a
sequence after sorting them alphabetically. 

Code:

n=int(input('enter the number of words: '))
str1 =[]
str2 =[]
for i in range(0,n):
    #str1[i]=input('enter the words')
    str1.append(input('enter the words to be sorted:  '))
    
str2 = sorted(str1)
print('final sorted list is:',str2)

Output:

enter the number of words: 4
enter the words to be sorted:  rose
enter the words to be sorted:  lotus
enter the words to be sorted:  jasmine
enter the words to be sorted:  lily
final sorted list is: ['jasmine', 'lily', 'lotus', 'rose']






#3. Write a program, which will find all the numbers between 1000 and 3000 (both
included) such that each digit of a number is an even number. The numbers
obtained should be printed in a comma separated sequence on a single line.

Code:

nums = []
for i in range(1000, 3001):
    s = str(i)
    if (int(s[0])%2==0) & (int(s[1])%2==0) & (int(s[2])%2==0) & (int(s[3])%2==0):
        nums.append(s)
print( 'The numbers are:',",".join(nums))

Output:

The numbers are: 2000,2002,2004,2006,2008,2020,2022,2024,2026,2028,2040,2042,2044,2046,2048,2060,2062,2064,2066,2068,2080,2082,2084,2086,2088,2200,2202,2204,2206,2208,2220,2222,2224,2226,2228,2240,2242,2244,2246,2248,2260,2262,2264,2266,2268,2280,2282,2284,2286,2288,2400,2402,2404,2406,2408,2420,2422,2424,2426,2428,2440,2442,2444,2446,2448,2460,2462,2464,2466,2468,2480,2482,2484,2486,2488,2600,2602,2604,2606,2608,2620,2622,2624,2626,2628,2640,2642,2644,2646,2648,2660,2662,2664,2666,2668,2680,2682,2684,2686,2688,2800,2802,2804,2806,2808,2820,2822,2824,2826,2828,2840,2842,2844,2846,2848,2860,2862,2864,2866,2868,2880,2882,2884,2886,2888


#4. Write a program that accepts a sentence and calculate the number of letters and
digits.

Code:

str1 = input('enter string -  ')
#str1 =('Python12345')
n=len(str1)
str2 = []
str3 = []
count1=0
count2=0
for i in range(n):
   # print(str1[i])
    #s=str(str1[i])
    if str1[i].isdigit():
        str2.append(str1[i])
        count1+=1
    elif str1[i].isalpha():
        str3.append(str1[i])
        count2+=1
print('no of digits are',str2)
print('no of letters are',str3)
print('counts of digits are',count1)
print('counts of letters are',count2)

Output:

enter string -  Python12345
no of digits are ['1', '2', '3', '4', '5']
no of letters are ['P', 'y', 't', 'h', 'o', 'n']
counts of digits are 5
counts of letters are 6


#5.Design a code which will find the given number is Palindrome number or not.

Code:

str1 = int(input('enter the number to check:  '))
temp = str1
rev_num =0
while(temp > 0):
        remainder=temp % 10
        rev_num = rev_num * 10 + remainder
        temp = temp//10

print('the rev_numrse no is:%d ',rev_num)

if(str1==rev_num):
    print('no is palindrome')
else:
    print('no is not palindrome')

Output:

enter the number to check:  1244554421
the rev_numrse no is:%d  1244554421
no is palindrome
