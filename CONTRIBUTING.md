n=input()
n = int(n)
lst = ["0","1"]
for i in range(1,n):
    new_lst = []
    for l in lst:
        new_lst.append("0"+l)
        new_lst.append("1"+l)
    lst = new_lst[:]

ways = 0
absent=0
for l in lst:
    consec = 0
    count = 0
    max_ = 0
    for i in range(0,len(l)):
        if l[i]=='1':
            if(consec==1):
                count += 1
            else:
                consec = 1
                count = 1
            max_ = max(count,max_)
        else:
            consec = 0
            count = 0
    #print(l,max_)
    if max_<4:
        ways+=1
        if int(l)&1==1:
            absent+=1
print(ways)
print(absent,"/",ways)
