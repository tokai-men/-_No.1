# -_No.1
import random
import numpy as np
def printnumber(x):
  if x==0:
    return np.array([["■","■","■"],["■","□","■"],["■","□","■"],["■","□","■"],["■","■","■"]])
  elif x==1:
    return np.array([["□","□","■"],["□","□","■"],["□","□","■"],["□","□","■"],["□","□","■"]])
  elif x==2:
    return np.array([["■","■","■"],["□","□","■"],["■","■","■"],["■","□","□"],["■","■","■"]])
  elif x==3:
    return np.array([["■","■","■"],["□","□","■"],["■","■","■"],["□","□","■"],["■","■","■"]])
  elif x==4:
    return np.array([["■","□","■"],["■","□","■"],["■","■","■"],["□","□","■"],["□","□","■"]])
  elif x==5:
    return np.array([["■","■","■"],["■","□","□"],["■","■","■"],["□","□","■"],["■","■","■"]])
  elif x==6:
    return np.array([["■","■","■"],["■","□","□"],["■","■","■"],["■","□","■"],["■","■","■"]])
  elif x==7:
    return np.array([["■","■","■"],["■","□","■"],["■","□","■"],["□","□","■"],["□","□","■"]])
  elif x==8:
    return np.array([["■","■","■"],["■","□","■"],["■","■","■"],["■","□","■"],["■","■","■"]])
  elif x==9:
    return np.array([["■","■","■"],["■","□","■"],["■","■","■"],["□","□","■"],["□","□","■"]])
result=[]
while True:
  roll=random.randint(1,75)
  if roll not in result:
    if roll>=10:
      print(printnumber(roll//10),"\n")
      print(printnumber(roll-(roll//10)*10))
    else:
      print(printnumber(roll))
    result.append(roll)
    print("現在出た番号:",result,"\n\n")
  if(input("中断する場合「停止」を入力")=="停止"):
    print("今回出た番号:",result)
    break
  if len(result)==75:
    break