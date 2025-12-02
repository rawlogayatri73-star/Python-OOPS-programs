# Python-OOPS-programs
import sys,time
class employee:
    def __init__(self,eno,ename):
        self.eno=eno
        time.sleep(2)
        self.ename=ename
        print("eno={},ename={}".format(self.eno,self.ename))
    def __del__(self):
        global totmemspace
        print('\t GC del() deallocatting the memory space {}'.format(id(self)))
        totmemspace=totmemspace-sys.getsizeof(self)
eo1=employee(110,'kvr')
eo2=employee(102,'gvr')
totmemspace=sys.getsizeof(eo1)+sys.getsizeof(eo2)
time.sleep(1)
