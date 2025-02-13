# Hands-on-Activity-2.1-The-Tower-of-Hanoi-Problem

def tower_hanoi(n, source, auxiliary, destination):
# Base case, if there's only 1 disk print append it in destination
    if n == 1:
        destination.append(source.pop())
#pop the last value in source
        print(destination[-1], source, auxiliary, destination,"\n")
        return
# 
    tower_hanoi(n-1, source, destination, auxiliary)

    destination.append(source.pop())
    print(destination[-1], source, auxiliary, destination,"\n")
    
    tower_hanoi(n-1, auxiliary, source, destination)


source = [4,3,2,1]
auxiliary = []         
destination = []  
n=len(source)     

tower_hanoi(n, source, auxiliary, destination)

