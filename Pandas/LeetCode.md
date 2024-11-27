Q1. 
a. Input: student_data: [[1, 15], [2, 11], [3, 11], [4, 20]]
b. Output:
| student_id | age |
---:|---
| 1          | 15  |
| 2          | 11  |
| 3          | 11  |
| 4          | 20  |

c. Solution: 
```python
import pandas as pd
df = pd.DataFrame(student_data,columns=['student_id','age'])
```
---

Q2. 
a. Input:

| player_id | name     | age | position    | team               |
|---|---|---|---|---|
| 846       | Mason    | 21  | Forward     | RealMadrid         |
| 749       | Riley    | 30  | Winger      | Barcelona          |
| 155       | Bob      | 28  | Striker     | ManchesterUnited   |
| 583       | Isabella | 32  | Goalkeeper  | Liverpool          |
| 388       | Zachary  | 24  | Midfielder  | BayernMunich       |
| 883       | Ava      | 23  | Defender    | Chelsea            |
| 355       | Violet   | 18  | Striker     | Juventus           |
| 247       | Thomas   | 27  | Striker     | ParisSaint-Germain |
| 761       | Jack     | 33  | Midfielder  | ManchesterCity     |
| 642       | Charlie  | 36  | Center-back | Arsenal            |

b. Output:
[10, 5]
c. Solution;
```list(df.shape)```

---

Display the First Three Rows ```df.head(3)```
Filter Rows and Columns: Write a solution to select the name and age of the student with player_id = 155 ```df[df['id' == 155]][['name','age']```
Create a New Column: Write a solution to create a new column name bonus that contains the doubled values of the salary column. ```df['bonus'] = df['salary'] * 2```
Drop Duplicate Rows based on a column ```df.drop_duplicates(subset=['col1'],inplace=True)```
Drop Na Rows based on a columns ```df.dropna(subset=['col1'],inplace=True)```
Modify the column by * 4 ```df['salary'] = df['salary'] * 2```
Rename Columns ```students.rename({'id':'student_id','first':'first_name','last':'last_name','age':'age_in_years'},axis = 1, inplace=True)```
Change Data Type ```students['grade'] = students['grade'].astype(int)```
Fill Missing Data ```products['quantity'].fillna(0, inplace=True)```
Concatenate these two DataFrames vertically into one DataFrame. ```df = pd.concat([df1,df2])```
Pivot ```table = pd.pivot_table(weather,values='temperature',index='month',columns=['city'])```
Melt ```table = report.melt(id_vars='product',var_name='quarter',value_name='sales')```
