# myFirstProjrct
To find if a pair whose sum is equal to a given sum; exists or not, in a given set of numbers. And to display the pair.(In lowest number of steps)
def search(data,sum):
    i=0
    values=[]
    result=bool(False)

    while (result==False and i<(len(data)-1)):
        new = sum - data[i]
        values.append(new)

        i = i + 1
        if (data[i] in values):
            result=bool(True)
            v1=data[i]
            v2=(sum-data[i])
            print("Result Found Set ( ",v2,",",v1,")")
            break

    if (result==False):
        print("Result Not Found")
        
set=[2,8,9,6,1,6,5,7,9,3,4,2,6,9,5,2,4,8] 
sum=int(input("Enter the sum of the pair"))

search(set,sum)
