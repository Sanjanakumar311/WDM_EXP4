### EX4 Implementation of Cluster and Visitor Segmentation for Navigation patterns
### DATE: 07.02.2026
### AIM: To implement Cluster and Visitor Segmentation for Navigation patterns in Python.
### Description:
<div align= "justify">Cluster visitor segmentation refers to the process of grouping or categorizing visitors to a website, 
  application, or physical location into distinct clusters or segments based on various characteristics or behaviors they exhibit. 
  This segmentation allows businesses or organizations to better understand their audience and tailor their strategies, marketing efforts, 
  or services to meet the specific needs and preferences of each cluster.</div>
  
### Procedure:
1) Read the CSV file: Use pd.read_csv to load the CSV file into a pandas DataFrame.
2) Define Age Groups by creating a dictionary containing age group conditions using Boolean conditions.
3) Segment Visitors by iterating through the dictionary and filter the visitors into respective age groups.
4) Visualize the result using matplotlib.

### Program:### EX4 Implementation of Cluster and Visitor Segmentation for Navigation patterns
### DATE: 07/02/2026
### AIM: To implement Cluster and Visitor Segmentation for Navigation patterns in Python.
### Description:
<div align= "justify">Cluster visitor segmentation refers to the process of grouping or categorizing visitors to a website, 
  application, or physical location into distinct clusters or segments based on various characteristics or behaviors they exhibit. 
  This segmentation allows businesses or organizations to better understand their audience and tailor their strategies, marketing efforts, 
  or services to meet the specific needs and preferences of each cluster.</div>
  
### Procedure:
1) Read the CSV file: Use pd.read_csv to load the CSV file into a pandas DataFrame.
2) Define Age Groups by creating a dictionary containing age group conditions using Boolean conditions.
3) Segment Visitors by iterating through the dictionary and filter the visitors into respective age groups.
4) Visualize the result using matplotlib.

### Program 1:
```python
import pandas as pd
df=pd.read_csv('/content/clustervisitor.csv')
df
cluster = {"Young": (df['Age'] <= 30),"Middle": ((df['Age'] > 30) & (df['Age'] <= 50)),"Old": (df['Age'] > 50)}
count=[]
for group,condition in cluster.items():
  visitors=df[condition]
  count.append(len(visitors))
  print(f"The visitors on {group} are :")
  print(visitors)
  print("count=",len(visitors))
import matplotlib.pyplot as plt
plt.figure(figsize=(8,6))
plt.bar(['Young','Middle','Old'],count,color="skyblue")
plt.xlabel('Age Groups')
plt.ylabel('Number of Visitors')
plt.title("Visitor Distribution Across Age Groups")
plt.show()
```
### Output:
<img width="479" height="681" alt="image" src="https://github.com/user-attachments/assets/17bffbe9-e273-4a13-86b2-566156b3333f" />
<img width="830" height="546" alt="image" src="https://github.com/user-attachments/assets/50cdad00-def3-4e40-9025-a2485a7383da" />

### Program 2: 
```python
from sklearn.preprocessing import StandardScaler
from sklearn.cluster import KMeans
df1=df['Age']
df2=df['Income']
df3=pd.concat([df1,df2],axis=1)
s=StandardScaler()
newdf=s.fit_transform(df3)
k=KMeans(n_clusters=3,random_state=55)
df3['cluster']=k.fit_predict(newdf)
df3
import matplotlib.pyplot as plt
plt.figure(figsize=(8, 6))
plt.scatter(x=df3['Age'],y=df3['Income'], c=df3['cluster'])
plt.xlabel('Age')
plt.ylabel('Income')
plt.title('Visitor Distribution in Different Clusters')
plt.show()
```
### Output:
<img width="382" height="611" alt="image" src="https://github.com/user-attachments/assets/424bad1d-3e58-40d8-aa34-efe045dfbd78" />

<img width="907" height="547" alt="image" src="https://github.com/user-attachments/assets/76d484d8-e7e5-4e99-8fd4-d98bd2ed94f6" />

### Result:
The implement Cluster and Visitor Segmentation for Navigation patterns in python is execute successfully.

```python
# Visitor segmentation based on characteristics
# read the data
/*WRITE YOUR CODE HERE

# Perform segmentation based on characteristics (e.g., age groups)
/*WRITE YOUR CODE HERE

```
### Output:

<img width="540" height="700" alt="image" src="https://github.com/user-attachments/assets/8e4813b6-bb78-452b-888f-33bdc7ac3bad" />

<img width="823" height="535" alt="image" src="https://github.com/user-attachments/assets/55863d22-e384-4423-ae69-59c804286e2c" />


### Visualization:
```python
# Create a list to store counts of visitors in each age group
/*WRITE YOUR CODE HERE

# Count visitors in each age group
/*WRITE YOUR CODE HERE
    
# Define age group labels and plot a bar chart
/*WRITE YOUR CODE HERE

plt.figure(figsize=(8, 6))
plt.bar(age_group_labels, visitor_counts, color='skyblue')
plt.xlabel('Age Groups')
plt.ylabel('Number of Visitors')
plt.title('Visitor Distribution Across Age Groups')
plt.show()
```
### Output:

<img width="429" height="789" alt="image" src="https://github.com/user-attachments/assets/d6bf59dd-31dd-4d7b-8bd3-e790f2f2fb86" />

<img width="886" height="578" alt="image" src="https://github.com/user-attachments/assets/77b270f3-e7b9-4fcb-9758-4610f138d433" />


### Result:

The implement Cluster and Visitor Segmentation for Navigation patterns in python is execute successfully.
