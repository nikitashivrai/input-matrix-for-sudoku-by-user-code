# input-matrix-for-sudoku-by-user-code-in-python
User entered matrix for sudoku code>>

input_string=input("enter a list numbers:")
userList=input_string.split()
for i in range(0,len(userList)):
    userList[i]=int(userList[i])

matrix=[]
while userList!=[]:
    matrix.append(userList[:9])
    userList=userList[9:]
    
def print_sudoku(matrix):
    for i in range(len(matrix)):
        if i%3==0 and i!=0:
            print("----------------------")

        for j in range(len(matrix[0])):
            if j%3==0 and j!=0:
                print("|",end="")

            if j==8:
                print(matrix[i][j])
            else:
                print(str(matrix[i][j])+" ",end="")
