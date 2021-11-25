# python-programming-challeging-Q-A


```
"""
problem : 1

Finding the sum of list excepting every iterating index item

Given list :  [1, 2, 3, 6, 7, 8]
--------------------------------------------------
[2, 3, 6, 7, 8]
[1, 3, 6, 7, 8]
[1, 2, 6, 7, 8]
[1, 2, 3, 7, 8]
[1, 2, 3, 6, 8]
[1, 2, 3, 6, 7]

Expected output : ['26', '25', '24', '21', '20', '19']


"""

final_output = []

print("Given list : ",x)
print("-"*50)

for i , item in enumerate(x):

  indexed_list = x[:i] + x[i+1:]

  result = f"{sum(indexed_list)}"

  print(indexed_list)

  final_output.append(result)
  
print(final_output)

```
