# prime-number
# Program to check if a number is prime or not
# To take input from the user
num = int(input("Enter a number: "))
composite = []

# prime numbers are greater than 1
if num > 1:
   # check for factors
   for i in range(2,num):
       if (num % i) == 0:
           for i in range(2,num+1):
               if num%i==0:
                   composite.append(i)
           print ("{} is composite number and factors are -> {}".format(num,composite))
           #print(i,"times",num//i,"is",num)
           break
   else:
       print(num,"is a prime number and factors are -> {}".format(num))
       
# if input number is less than
# or equal to 1, it is not prime
else:
   print(num,"is not a prime number")
print ("With 1st method number of iteration is -> ",int(num-1))
print ("With 2st method number of iteration is -> ",int(i/num+2))
