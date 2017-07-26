# prime_no-program-in-python
#program for converting prime no into string and obtaining the length of odd string.
import inflect
lower=int(input("enter lower range:"))
upper=int(input("enter upper range:"))
print("Prime numbers between lower",lower," and" ,upper ,"are")
for num in range(lower,upper+1):
    if(num > 1):
        for i in range(2,num):
            if((num%i)==0):
               break
        else:
            print("prime nos are:",num)
            p=inflect.engine()
            c=p.number_to_words(num)
            if((len(c)%2)!=0):
                print("length of ",c,":",len(c))
