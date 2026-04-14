class Node():                                       
   def __init__(self,content):
       self.content=content
       self.next=None

class linked_list:
    def __init__(self):
        self.front=None
        self.rear=None
    def add_front(self,new):
        if self.front==None:
            self.front=Node(new)
            self.rear=Node(new)
        else:
            Node(new).next=self.front
            self.front=Node(new)
    def add_rear(self,new):
        if self.rear==None:
            self.front=Node(new)
            self.rear=Node(new)
        else:
            self.rear.next=Node(new)
            self.rear=Node(new)
    def print_list(self):
        tmp=self.front
        while tmp is not None:
            print(tmp.content)
            tmp = tmp.next

my_str="No description,website,or,topics provided."
words=my_str.split(' ')
ll=linked_list()

for word in words:
    print(len(word))
    nn=Node(len(word))
    print(type(nn))
    ll.add_rear(nn)
