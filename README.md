# assignment2-python-
#ques1
L = [11, 12, 13, 14]

# Add 50 and 60
L.extend([50, 60])
print("After adding:", L)

# Remove 11 and 13
for item in [11, 13]:
    if item in L:
        L.remove(item)
print("After removing:", L)

# Sort ascending
print("Ascending:", sorted(L))

#  Sort descending
print("Descending:", sorted(L, reverse=True))

#  Search for 13
print("13 found?" , 13 in L)

# Count elements
print("Count:", len(L))

#  Sum all elements
print("Sum:", sum(L))

#  Sum odd numbers
print("Sum of odd:", sum(x for x in L if x % 2 != 0))

# Sum even numbers
print("Sum of even:", sum(x for x in L if x % 2 == 0))

# Sum prime numbers
def is_prime(n):
    if n < 2: return False
    for i in range(2, int(n**0.5)+1):
        if n % i == 0:
            return False
    return True
print("Sum of prime:", sum(x for x in L if is_prime(x)))

#  Clear all elements
L.clear()
print("After clearing:", L)

# Delete L
del L


#ques2
lst = [1, 2, 3, 4, 5]
total = 0
for i in lst:
    total += i
print("Sum:", total)


#ques 3
lst = [1, 2, 3, 4, 5]
product = 1
for i in lst:
    product *= i
print("Product:", product)

#ques4
array = [[["*" for _ in range(6)] for _ in range(4)] for _ in range(3)]
print(array


#ques 5
D = {1:5.6, 2:7.8, 3:6.6, 4:8.7, 5:7.7}

#  Add key=8, value=8.8
D[8] = 8.8

#  Remove key=2
D.pop(2, None)

#  Check key=6
print("6 in D?", 6 in D)

#  Count elements
print("Count:", len(D))

# Add all values
print("Sum of values:", sum(D.values()))

#  Update value of 3
D[3] = 7.1

#  Clear dictionary
D.clear()
print("After clearing:", D)


#ques6
S1 = {10, 20, 30, 40, 50, 60}
S2 = {40, 50, 60, 70, 80, 90}

#  Add 55, 66
S1.update([55, 66])

# Remove 10, 30
S1.discard(10)
S1.discard(30)

#  Check if 40 present
print("40 in S1?", 40 in S1)

#  Union
print("Union:", S1 | S2)

#  Intersection
print("Intersection:", S1 & S2)

# Difference
print("S1 - S2:", S1 - S2)


#ques7
import random, string

# 100 random strings (length 6–8, letters only)
for _ in range(100):
    length = random.randint(6, 8)
    rand_str = ''.join(random.choice(string.ascii_letters) for _ in range(length))
    print(rand_str)

# Prime numbers between 600 and 800
def is_prime(n):
    if n < 2: return False
    for i in range(2, int(n**0.5)+1):
        if n % i == 0: return False
    return True

primes = [n for n in range(600, 801) if is_prime(n)]
print("Primes:", primes)

#  Numbers between 100 and 1000 divisible by 7 & 9
nums = [n for n in range(100, 1001) if n % 63 == 0]
print("Divisible by 7 and 9:", nums)


#ques8
exam_st_date = (11, 12, 2025)
print("The examination will start from: %i / %i / %i" % exam_st_date


#ques9
lst = [10, 23, 45, 67, 90, 100]
for num in lst:
    if num % 5 == 0:
        print(num)

#ques10
n = int(input("Enter a number: "))
is_even = (n % 2 == 0)
print("Even?" , is_even)


#ques11
text = "Emma is good. Emma likes Python. Emma is smart."
print("Emma appears:", text.count("Emma"), "times")


#ques12
list1 = [10, 21, 4, 45, 66, 93]
list2 = [12, 14, 17, 19, 20]

new_list = [x for x in list1 if x % 2 != 0] + [y for y in list2 if y % 2 == 0]
print("New List:", new_list)


#ques13
positions = [(2,3), (4,5), (6,7), (7,8)]
even_positions = [pos for pos in positions if pos[0] % 2 == 0]
print("Even x-positions:", even_positions)


#ques14
sensor_data = {1: 2.3, 2: 4.5, 3: 1.8, 4: 3.6}
above_3 = [k for k, v in sensor_data.items() if v > 3.0]
print("Sensor IDs above 3.0:", above_3)


#ques15
commands_received = {"MOVE", "TURN_LEFT", "TURN_RIGHT", "STOP"}
commands_executed = {"MOVE", "TURN_LEFT", "STOP"}
not_executed = commands_received - commands_executed
print("Commands not executed:", not_executed
