# python-programming-challeging QA


```
"""
problem : 1 (list)

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


```
"""
problem : 2 (pandas)

Finding the highest tempeture month for given city dataframe. 

"""

import pandas as pd

df = pd.DataFrame({'city': ['Mumbai', 'Delhi', 'Hyderabad', 'Chennai','Mumbai', 'Delhi', 'Hyderabad', 'Chennai'],
                  'month': ['January', 'January', 'January', 'January','February','February','February','February'],
                  'temp': [30,40,50,60,40,50,60,70]})


df = df.groupby(['city','month']).first()
df.sort_values(by=['temp'], ascending=False)
```
![image](https://user-images.githubusercontent.com/42869040/143419686-935de0c6-4013-4177-b410-f36b90cffd69.png)




```
"""
problem : 3 (pandas)

Change the tempeture value to 100 , if city is Mumbai and month is January 

"""

import pandas as pd

df = pd.DataFrame({'city': ['Mumbai', 'Delhi', 'Hyderabad', 'Chennai','Mumbai', 'Delhi', 'Hyderabad', 'Chennai'],
                  'month': ['January', 'January', 'January', 'January','February','February','February','February'],
                  'temp': [30,40,50,60,40,50,60,70]})



df.loc[(df['city'] == "Mumbai" ) & (df["month"] == "January"),['temp']]=100
```
![image](https://user-images.githubusercontent.com/42869040/143420127-edff7c40-e9b0-4f91-baad-7066b642a59b.png)
