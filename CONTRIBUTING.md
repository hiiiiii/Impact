n = input()
n = int(n)
 
ways = 0
if n==1:
    print(2)
    print("1/2")
elif n==2:
    print(4)
    print("2/4")
    
elif n==3:
    print(8)
    print("4/8")
    
elif n==4:
    print(15)
    print("7/15")
else:
    a=8
    b=15
    for i in range(5,n+1):
        c = a+b
        a=b
        b=c
    print(b)
    print(str(b-a)+"/"+str(b))
'''
def fact(n):
  if n==0:
    return 1
   return n*fact(n)
  
if n==1:
  print(2)
  print("1/2")
elif n==2:
  print(4)
  print("2/4")

elif n==3:
  print(8)
  print("4/8")

elif n==4:
  print(15)
  print("7/15")
else:
  ways = 0
  count = 0
  if (n-i)<3:
     ways = fact(n)/(fact(i)*fact(n-i))
     absent_ways = fact(n-1)/(fact(i)*fact(n-i-1)
     print(ways)
     print(str(absent_ways)+"/"+str(ways))

'''
