# Functions-in-Python

# why function are required in python
    #Increase Code Readability
    #Increase Code Reusability
    #Functions allow the same piece of code to run multiple times
    #Functions break long programs up into smaller components
    #Functions can be shared and used by other programmers




'''def greeting():
    print('Good morning')
greeting()'''



'''def greeting(name):
    print('Hello',name,'Good morning')
greeting('Ram')'''




'''def square(x):
    print('The square of {} is : {}'.format(x,x*x))
square(11)'''




'''def add(a,b):
    return a+b
answer = add(10,10)
print(answer)'''




'''def sub(a,b):
    return a-b
answer = sub(10,10)
print(answer)'''




'''def mul(a,b):
    return a*b
answer = mul(10,10)
print(answer)'''




'''def div(a,b):
    return a/b
answer = div(10,10)
print(answer)'''




'''def mod(a,b):
    return a%b
answer = mod(10,10)
print(answer)'''




'''def f():
    print('hello')
f()'''




# Even OR Odd:


'''def evenodd(n):
    if n%2 == 0:
        print("Even")
    else:
        print("Odd")
evenodd(99)'''



'''def evenodd(n):
    if n%2 == 0:
        print("{} is Even no".format(n))
    else:
        print("{} is Odd no".format(n))
evenodd(88)'''



# factorial of given number:



'''def fact(n):
    result = 1
    while n>=1:
        result = result*n
        n = n-1
    return result
print(fact(13))'''



'''def sum_sub(a,b):
    sum = a+b
    sub = a-b
    return sum,sub
print(sum_sub(100,50))'''




# Types of Arguments
  #Positional Arguments
  #Keyword Arguments
  #Default Arguments
  #Variable length Arguments



'''def sum(a,b):      #Here (a,b) is Arguments.|| Formal Parameters
    pass
sum(10,20)        #Here (10,20) is actual Arguments.'''



# Positional Arguments - Exact correct positional order and number of arguments is important


'''def sum(a,b):
    print(a+b)
sum(100,401)'''



# Keyword Arguments



'''def greeting(name,msg):
    print('Hello',name,msg)
greeting(name='Rahul',msg='Welcome')'''



# Default Arguments


'''def greeting(name='student'):
    print('Hello',name,'Good morning')
greeting('Sagar')
greeting()'''



# Variable length Arguments


'''def mul(a,b):
    print(a*b)
mul(10,20)'''



'''def mul(a,b,c,d):
    print(a*b*c*d)
mul(10,20,30,40)'''




# Types of Variable:-
       
# Global Variable - 
           . Global variable declared outside a function is known as Global variable.
           . Global variable can be changed
  
# Local Variable -
            . local variable declared inside a function is known as local variable.
            • local variable can't be changed.


# a = 10
# def F1():
#     print('F1:',a)
# F1()
# def F2():
#     print('F2:',a)
# F2()



'''def F1():
    a = 10
    print('F1:',a)
F1()
def F2():
    print('F2',a)  #Error
F2()'''



# p = 90
# def F1():
#     p = 10  #Local Variable gets the priority
#     print('F1:',p)
# F1()
# def F2():
#     print('F2:',p)
# F2()



'''q = 10
def F1():
    global q
    q = 100
    print('F1:',q)
F1()
def F2():
    print('F2:',q)
F2()'''



# r = 20
# def F1():
#     r = 30
#     global r
#     print('F1',r)
# F1()
# def F2():
#     print('F2',r)
# F2()             #SyntaxError: name 'r' is assigned to before global declaration



'''def F1():
    global s
    s = 111
    print('F1:',s)
def F2():
    global s
    s = 999
    print('F2:',s)
def F3():
    print('F3:',s)
F1()
F2()
F3()'''



# a=10
# def F1():
#     a = 20
#     print(a)
# F1()



'''a=10
def f1():
    a=20
    print(a)
    print(globals()['a'])
f1()'''




# Recursive Function - 
            when we call a function inside a same function

# Advantage:
          .It improves the code readability
          .Help solve to very complex problem




#fact(5)=?
# def factorial(n):
#     if n == 0 or n == 1:
#         return 1
#     else:
#         return n * factorial(n - 1)
# result = factorial(5)
# print(f"The factorial of 5 is: {result}")




'''def factorial(n):
    if n == 0:
        result = 1
    else:
        result = n*factorial(n-1)
    return result
factorial(5)'''




# Anonymous function - Lambda function
# Without name - Name less function



# def Square(n):
#     print(n*n)
# Square(9)
#
# print(lambda n : n*n)



''''s = lambda a,b:a+b
print('sum of {} and {} is : {}'.format(2,4,s(2,4)))
print('sum of {} and {} is : {}'.format(22,44,s(22,44)))

s = lambda a,b : a if a>b else b
print('the biggest of {} and {} is : {}'.format(100,20,s(100,20)))
print('the biggest of {} and {} is : {}'.format(10,200,s(10,200)))'''




# def iseven(x):
#     if x%2 == 0:
#         print('True')
#     else:
#         print('False')
# iseven(9)
# iseven(8)





# filter:
  # true value in the list,tuple & list
  # false nothing




'''def iseven(x):
    if x%2 == 0:
        return True
    else:
        return False
l = [0,2,5,7,8,8,9,44,122,33]
print(type(filter(iseven,l)))
print(list(filter(iseven,l)))
print(tuple(filter(iseven,l)))
print(set(filter(iseven,l)))

print(list(filter(lambda x:x%2 != 0,l)))'''





# map

# MUl

'''list1 = [1,2,3,4]
list2 = [9,8,7,6]
print(list(map(lambda x,y : x*y,list1,list2)))'''



# ADD

'''list3 = [1,2,3,4]
list4 = [9,8,7,6]
print(list(map(lambda x,y : x+y,list3,list4)))'''






# Reduce:

# from functools import *
# list1 = [10,30,50,70,90]
# result = reduce(lambda x,y:x+y,list1)
# print(result)



# same output


'''from functools import *
list1 = [10,30,50,70,90]
print(reduce(lambda x,y:x+y,list1))'''




# function Aliasing
'''def greeting(name):
    print('Good morning',name)
print(id(greeting))'''



# Nested Function
'''def outer():
    print('outer function started')
    def inner():
        print('Inner function started')
    inner()
outer()'''



# def f1():
#     def inner(a,b):
#         print('the sum:',a+b)
#         print('the avg:',(a+b)/2)
#         print('the mul',a*b)
#     inner(10,20)
#     inner(20,30)
#     inner(30,40)
#     inner(40,50)
# f1()



'''def outer():
    print('outer function started')
    def inner():
        print('Inner function started')
    print('outer function returning inner function')
    return inner()
f1 = outer()'''



# def f1():
#     def inner(a,b):
#         print('The sum:',a+b)
#         # n = a+b
#         # return n
#     return inner
# r = f1()
# r(10,20)




'''def a(x,y):
    r = x+y
    return r
result = a(10,50)
print(result)'''



# Decorator




'''def greeting(name):
    print('Hello',name,'good morning')
greeting('Vikas')
greeting('Rahul')
greeting('Aradhya')
greeting('Angel')'''




# def decor(func):
#     def inner(name):
#         if name == 'Vikas':
#             print('Hello',name,'bad morning')
#         else:
#             func(name)
#     return inner
# @decor
# def greeting(name):
#     print('Hello',name,'good morning')
# greeting('Vikas')
# greeting('Rahul')
# greeting('Aradhya')
# greeting('Angel')



# START PART 4


