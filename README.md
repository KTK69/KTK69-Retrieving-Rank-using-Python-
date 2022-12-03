# KTK69-Retrieving-Rank-using-Python-
print("PYTHON PROJECT")
print("")
print("Greetings")
print("")
print("Name: Tanveer Krishna Kristam")
print("Section: K22FG")
print("Roll No: 70")
print("Assigned project number: 22")
print("")
print("Presenting to: Dr. Harwant Singh Arri")
print("")
print("Aim:  To find the name of the student with maximum marks after updation in marks and the jump in the student’s rank i.e., previous rank – current rank.")
print("You are given three lists’ names, mark’s and update’s where:")
print(" Names contain the names of students.")
print(" Marks contain the marks of the same students.")
print(" Updates contains the integers by which the marks of these students are to be updated.")
print("(Number of levels a student is ranking up or down must be displayed)")

print("")
print("")
print("")


names= ['ram', 'sam', 'green']
marks= [80, 79, 75]
updates = [0, 5, -9]
n = len(marks)
print("Lists taken into consideration are:")
print("NAMES:",names)
print("MARKS:",marks)
print("UPDATES:",updates)
print("")


for (i,j) in zip(names,marks):
    print("Intial MARKS of {0} are: {1}".format(i,j))
print("")


print("Descending order of names according to initial marks ")
d=dict()
for (i,j) in zip(names,marks):
    d[i]=j
print(d)
print("")

print("")






print("updates in each of their marks are:")
e=dict()
for (i,j) in zip (names,updates):
    e[i]=j
print(e)
print("")
c=[]
for (i,j) in zip(marks,updates):
    c.append(i+j)
#print(c)
a=dict()
for (i,j) in zip(names,c):
    a[i]=j
print("Updated Marks of Individual Students are:")
print(a)
print("")
print("Ascending order of names according to their marks scored:")
b=sorted(a)
print(b)
print("")
#for i in sorted(a.keys()):
    #print(i, end=" ")
#print()
#print("")





#for (i,j) in zip(names,c):
   # print("Updated marks of {0} are {1}".format(i,j))

#print("")

print("Ranks of students after updation in their marks are:")

print(b[-1],"1st RANK")
print(b[1],"2nd RANK")
print(b[0],"3rd RANK")



def nameRank(names, marks, updates, n):
     
    x = [[0 for j in range(3)] for i in range(n)]
    for i in range(n):
        
        x[i][0] = names[i]
         
        x[i][1]= marks[i] + updates[i]
         
        x[i][2] = i + 1
         
    highest = x[0]
    for j in range(1, n):
        if (x[j][1] >= highest[1]):
            highest = x[j]
             
    print("Highest Student's Name: ", highest[0], ", Jump in Rank: ",
            abs(highest[2] - 1), sep="")


print("")

print("")

nameRank(names, marks, updates, n)


















   
