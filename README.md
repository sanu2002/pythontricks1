# pythontricks1
here i will update my python concept



HOW TO IMPORT MODULE DYNAMICALLY??????

m.py
________
def greet(name):
    return f"Hey! my name is {name}"


main.py
________

def dynamic(*args, **kwargs):
    try:
        module=__import__(args[0])
        print(module)
        greet=module.greet(args[1])
        return greet
    
    except Exception as e:
        print(e)
        
        
m_name=input("enter a name ")
name=input("enter a name ")

print(dynamic(m_name,name))






2//  HOW TO REDUCE  MEMORY SPACE BY USING GENERATOR




def gen(n):
    for i in range(n):
        yield i**2
n=int(input("enter a number"))
for i in gen(n):
    print(i)
    
    
    
class Gen:
    def __init__(self,n):
        self.n=n
        self.last=0
        
    def __next__(self):
        return self.next()
    
    def next(self):
        try:
            if self.last < self.n:
                data=self.last**2
                self.last+=1
                return data
        except Exception as e:
            print(e)
     
        
        
data=Gen(10000)
for i in data:
    print(i)











