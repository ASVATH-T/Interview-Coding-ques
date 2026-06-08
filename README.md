1. Reverse a String
s = "python"
print(s[::-1])


3. Check Palindrome
s = "madam"

if s == s[::-1]:
    print("Palindrome")
else:
    print("Not Palindrome")

    
3. Factorial
n = 5
fact = 1

for i in range(1, n + 1):
    fact *= i

print(fact)


4. Fibonacci Series
n = 10
a, b = 0, 1

for i in range(n):
    print(a, end=" ")
    a, b = b, a + b

    
5. Prime Number
n = 17

for i in range(2, n):
    if n % i == 0:
        print("Not Prime")
        break
else:
    print("Prime")

    
6. Find Largest Number
nums = [10, 20, 30, 40]

largest = nums[0]

for num in nums:
    if num > largest:
        largest = num

print(largest)


7. Find Second Largest Number
nums = [10, 20, 30, 40]

nums.sort()
print(nums[-2])


8. Count Vowels
s = "hello world"

count = 0

for ch in s.lower():
    if ch in "aeiou":
        count += 1

print(count)


9. Remove Duplicates from List
nums = [1,2,2,3,3,4]

print(list(set(nums)))


10. Count Character Frequency
s = "banana"

freq = {}

for ch in s:
    freq[ch] = freq.get(ch,0)+1

print(freq)


11. Linear Search
arr = [10,20,30,40]
target = 30

for i in range(len(arr)):
    if arr[i] == target:
        print("Found at", i)

        
12. Binary Search
arr = [10,20,30,40,50]
target = 40

low = 0
high = len(arr)-1

while low <= high:
    mid = (low+high)//2

    if arr[mid] == target:
        print("Found")
        break

    elif arr[mid] < target:
        low = mid + 1

    else:
        high = mid - 1

        
13. Bubble Sort
arr = [5,4,3,2,1]

for i in range(len(arr)):
    for j in range(len(arr)-i-1):
        if arr[j] > arr[j+1]:
            arr[j], arr[j+1] = arr[j+1], arr[j]

print(arr)


14. Check Anagram
s1 = "listen"
s2 = "silent"

if sorted(s1) == sorted(s2):
    print("Anagram")

    
15. Two Sum
nums = [2,7,11,15]
target = 9

seen = {}

for i,num in enumerate(nums):
    diff = target - num

    if diff in seen:
        print(seen[diff], i)

    seen[num] = i

    
16. Stack Implementation
stack = []

stack.append(10)
stack.append(20)

print(stack.pop())


17. Queue Implementation
from collections import deque

q = deque()

q.append(10)
q.append(20)

print(q.popleft())


18. Class and Object
class Student:
    def __init__(self,name):
        self.name = name

s = Student("Asvath")

print(s.name)


19. Inheritance
class Animal:
    def sound(self):
        print("Animal Sound")

class Dog(Animal):
    pass

d = Dog()
d.sound()


20. Flask Hello World
from flask import Flask

app = Flask(__name__)

@app.route('/')
def home():
    return "Hello World"

app.run(debug=True)


21. SQL - Second Highest Salary
SELECT MAX(salary)
FROM employee
WHERE salary <
(
SELECT MAX(salary)
FROM employee
);


22. SQL Join
SELECT e.name, d.department
FROM employees e
INNER JOIN departments d
ON e.dept_id = d.id;


24. SQL Count Records
SELECT COUNT(*)
FROM employees;


26. Flask REST API
from flask import Flask,jsonify

app = Flask(__name__)

@app.route('/api')
def api():
    return jsonify({"message":"Success"})
