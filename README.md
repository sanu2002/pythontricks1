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










