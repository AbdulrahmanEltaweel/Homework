# Homework
#Python homework

#EX1:
def fibonacci1(n):
   if n==1 or n==2:
       return 1
   return fibonacci1(n-1)+ fibonacci1(n-2)
for i in range(1,101):
   print (fibonacci1(i))


#EX5:




#EX12:
# returns True if parameter n is a prime number, False if composite and "Neither prime, nor composite" if neither
def isPrime(n):
    if n < 2: return "Neither prime, nor composite"
    for i in range(2, int(n**0.5) + 1):
        if n % i == 0:
            return False
    return True

# returns the nth prime number
def nthPrime(n):
    numberOfPrimes = 0
    prime = 1

    while numberOfPrimes < n:
        prime += 1
        if isPrime(prime):
            numberOfPrimes += 1
    return prime

print(nthPrime(10001))
