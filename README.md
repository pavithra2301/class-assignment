# class-assignment
class Tree(object):
    def __init__(self):
        self.left = None
        self.right = None
        self.data = None

# A function to do inorder tree traversal 
def printInorder(root): 
    if root: 
        printInorder(root.left) 
        print(root.data), 
        printInorder(root.right) 
  
# A function to do postorder tree traversal 
def printPostorder(root): 
    if root:
        printPostorder(root.left) 
        printPostorder(root.right) 
        print(root.data), 
  
  
# A function to do preorder tree traversal 
def printPreorder(root): 
    if root: 
        print(root.data),
        printPreorder(root.left) 
        printPreorder(root.right) 

root = Tree()
root.data = "A"     
root.left = Tree()
root.left.data = "B"
root.right = Tree()
root.right.data = "C"
root.left.left = Tree()
root.left.left.data = "D"
root.right.left = Tree()
root.right.left.data = "E"
root.right.right = Tree()
root.right.right.data = "G"
root.left.right = Tree()
root.left.right.data = "F"
root.left.right.left = Tree()
root.left.right.left.data = "M"
root.right.left.right = Tree()
root.right.left.right.data = "N"


print(root.right.left.right.data)
print(root.left.right.left.data)
print(root.right.left.data)
print(root.left.left.data)
print(root.right.left.right.data)
print(root.left.right.data)
print(root.right.right.data)
print(root.left.data)
print(root.right.data)
print(root.data)

print("to print preorder data")
printPreorder(root) 
print("to print inorder data")
printInorder(root) 
print("to print post order data")
printPostorder(root)


#generic tree traversal
class Node(object):
    def __init__(self, data):
        self.data = data
        self.childern = []
        
    def add_childern(self, obj):
        self.childern.append(obj)
 
n = Node(5)    
p = Node(6)
q = Node(7)
r = Node(9)
m = Node(11)
s = Node(12)
l = Node(14)
t = Node(15)
n.add_childern(p)
n.add_childern(q)
n.add_childern(r)
p.add_childern(m)
p.add_childern(s)
q.add_childern(l)
r.add_childern(t)

for c in n.childern:
    print(c.data)

for c in p.childern:
    print(c.data)
    
for c in q.childern:
    print(c.data)
    
for c in r.childern:
    print(c.data)



  
    
