from timeit import default_timer as timer
def fibonacci(n):
    global fibonacci_list
    if n<=0:
        return 0
    elif n<=len(fibonacci_list):
        return fibonacci_list[n-1]
    else:
        fibonacci_list.append(fibonacci(n-1)+fibonacci(n-2))
        return fibonacci_list[n-1]

fibonacci_list=[1,1]
while 1:
    try:
        n=int(input("Enter a position to get a corresponding number in a fibonacci sequence "))
    except ValueError: #to avoid inputs like characters,decimal number
        print("Please enter a positive integer")
        continue
    start=timer()
    output=fibonacci(n)
    if output!=0: #to accept only positive integer
        print("Fibonacci number at position ",n," is : ",output)
        end=timer()
        print("Time taken to get the result to the user : ","{0:.6f}".format(end-start)," seconds")
    else: #to avoid negative integer
        print("Please enter a positive integer")
        continue
    a=input("Press 'y' to Try again and any other key to exit ")
    if a=='y':
        continue
    else:
        print("Program terminated")
        break
