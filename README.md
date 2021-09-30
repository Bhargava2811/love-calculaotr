# love-calculaotr


from collections import Counter
c1=Counter(input("ENTER YOUR NAME:"))
c2=Counter(input("ENTER YOUR PARTNER NAME:"))
for i,j in c1.items():
    if i in c2:
        if j>c2[i]:
            c1[i]=j-c2[i]
            c2[i]=0
        elif c2[i]>j:
            c2[i]-=j
            c1[i]=0
        else:
            c2[i]=0
            c1[i]=0
s1=sum(c1.values())
s2=sum(c2.values())

sum1 = s1+s2
c=sum1


s=0
while c>0:
    r=c%10        
    s=s+r
    c=c//10


if s == 0:
    print('YOUR SOUL')
elif s == 1:
    print('FRIEND')
elif s == 2:
    print('BEST FRIEND')
elif s == 3:
    print('LOVER')
elif s == 4:
    print('CHEATER')
elif s == 5:
    print('LIFE PARTNER')
elif s == 6:
    print('JUST A PERSON IN LIFE(stranger)')
elif s == 7:
    print('DEVIL')
elif s == 8:
    print('FRIENDS LOVER')
elif s == 9:
    print('ENEMY')
else:
    print('NO RELATION')
