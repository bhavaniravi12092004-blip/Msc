1. STUDY OF BASIC SYNTAX IN R

Aim: 
	To study of basic syntax in R.
Algorithm:





















Program:
# 1. Assigning values to variables

name <- "John"
age <- 25
score <- 87.5
passed <- TRUE

# 2. Printing values

print(paste("Name:", name))
print(paste("Age:", age))
print(paste("Score:", score))
print(paste("Passed:", passed))

# 3. Arithmetic operations

a <- 10
b <- 3
print(paste("Sum:", a + b))
print(paste("Product:", a * b))

# 4. Using a vector

marks <- c(80, 85, 90)
print("Marks:")
print(marks)

# 5. Conditional statement

if (score > 50) {
  print("You passed the test.")
} else {
  print("You failed the test.")
}

# 6. Loop (for loop)

print("Counting from 1 to 5:")
for (i in 1:5) {
  print(i)
}

# 7. Defining and using a function

greet <- function(person) {
  return(paste("Hello,", person))
}

message <- greet(name)
print(message)




















Result:

Output:

[1] "Name: John"
[1] "Age: 25"
[1] "Score: 87.5"
[1] "Passed: TRUE"
[1] "Sum: 13"
[1] "Product: 30"
[1] "Marks:"
[1] 80 85 90
[1] "You passed the test."
[1] "Counting from 1 to 5:
[1] 1
[1] 2
[1] 3
[1] 4
[1] 5
[1] "Hello, John"








2: IMPLEMENTATION OF VECTOR DATA OBJECTS OPERATIONS R

Aim: 
	To implementation of vector data objects operations R.
Algorithm:






















Program:

v1 <- c(10, 20, 30); v2 <- c(1, 2, 3)
cat("Add:", v1 + v2, "\n")
cat("Sub:", v1 - v2, "\n")
cat("Mul:", v1 * v2, "\n")
cat("Div:", v1 / v2, "\n")
cat("v1[1]:", v1[1], "v2[2]:", v2[2], "\n")
v1[2] <- 50
cat("Modified v1:", v1, "\nLength:", length(v1), "\n")

















Result:

Output:

Add: 11 22 33
Sub: 9 18 27
Mul: 10 40 90
Div: 10 10 10
v1[1]: 10 v2[2]: 2
Modified v1: 10 50 30
Length: 3





















3: IMPLEMENTATION OF MATRIX, ARRAY AND FACTORS AND PERFORM VARIOUS OPERATIONS IN R

Aim: 
	To implementation of matrix, array and factors and perform various operations in R.
Algorithm:




















Program:
mat <- matrix(1:9, 3, 3); mat2 <- matrix(9:1, 3, 3)
cat("mat:\n"); print(mat)
cat("mat+mat2:\n"); print(mat + mat2)
cat("mat %*% mat2:\n"); print(mat %*% mat2)
cat("mat[2,3]:", mat[2,3], "\n\n")

arr <- array(1:12, c(2,3,2))	
cat("arr:\n"); print(arr)
cat("arr[1,2,2]:", arr[1,2,2], "Sum:", sum(arr), "\n\n")

colors <- factor(c("red","blue","green","red","green","blue"))
cat("Levels:", levels(colors), "\nFreq:\n"); print(table(colors))













Result:

Output:
mat:
     [,1] [,2] [,3]
[1,]    1    4    7
[2,]    2    5    8
[3,]    3    6    9
mat+mat2:
     [,1] [,2] [,3]
[1,]   10   10   10
[2,]   10   10   10
[3,]   10   10   10
mat %*% mat2:
     [,1] [,2] [,3]
[1,]   90   54   18
[2,]  114   69   24
[3,]  138   84   30
mat[2,3]: 8
arr:
, , 1
     [,1] [,2] [,3]
[1,]    1    3    5
[2,]    2    4    6
, , 2
     [,1] [,2] [,3]
[1,]    7    9   11
[2,]    8   10   12
arr[1,2,2]: 9 Sum: 78
Levels: blue green red 
Freq:
colors
 blue green   red 
    2     2     2























4: IMPLEMENTATION AND USE OF DATA FRAMES IN R

Aim: 
	To implementation and use of data frames in R.
Algorithm:





















Program:

names <- c("Alice", "Bob", "Charlie", "David")
ages <- c(25, 30, 22, 35)
scores <- c(85.5, 90, 78.5, 88)

students_df <- data.frame(Name=names, Age=ages, Score=scores)
print("Students:")
print(students_df)

print("Names:")
print(students_df$Name)

students_df$Passed <- students_df$Score >= 80
print("With Passed column:")
print(students_df)

print("Passed students:")
print(subset(students_df, Passed))

print("Summary:")
print(summary(students_df))



Result:

Output:

[1] "Students:"
Name Age Score
1   Alice  25  85.5
2     Bob  30  90.0
3 Charlie  22  78.5
4   David  35  88.0

[1] "Names:"
[1] "Alice"   "Bob"     "Charlie" "David"

[1] "With Passed column:"
Name Age Score Passed
1   Alice  25  85.5   TRUE
2     Bob  30  90.0   TRUE
3 Charlie  22  78.5  FALSE
4   David  35  88.0   TRUE

[1] "Passed students:"
   Name Age Score Passed
1 Alice  25  85.5   TRUE
2   Bob  30  90.0   TRUE
4 David  35  88.0   TRUE

[1] "Summary:"
Name                Age            Score         Passed       
 Length:4           Min.   :22.00   Min.   :78.50   Mode :logical  
 Class :character   1st Qu.:24.25   1st Qu.:83.75   FALSE:1        
 Mode  :character   Median :27.50   Median :86.75   TRUE :3        
                    Mean   :28.00   Mean   :85.50                  
                    3rd Qu.:31.25   3rd Qu.:88.50                  
                    Max.   :35.00   Max.   :90.00 



  



















5: CREATE SAMPLE (DUMMY) DATA IN R AND PERFORM DATA MANIPULATION WITH R

Aim: 
	To create sample (dummy) data in r and perform data manipulation with R.
Algorithm:




















Program:

employees <- data.frame(
  ID = 1:5,
  Name = c("Alice", "Bob", "Charlie", "Diana", "Ethan"),
  Department = c("HR", "IT", "Finance", "IT", "HR"),
  Salary = c(50000, 60000, 55000, 62000, 48000),
  Experience = c(2,4,3,5,1),
  stringsAsFactors=FALSE
)

cat("Original Data:\n"); print(employees)
cat("\nSalary > 55000:\n"); print(subset(employees, Salary > 55000))
employees$Bonus <- employees$Salary * 0.05
cat("\nWith Bonus:\n"); print(employees)
cat("\nAvg Salary by Dept:\n"); print(aggregate(Salary ~ Department, employees, mean))
cat("\nSorted by Experience:\n"); print(employees[order(-employees$Experience), ])







Result:

Output:
Original Employee Data:
  ID    Name Department Salary Experience
1  1   Alice         HR  50000          2
2  2     Bob         IT  60000          4
3  3 Charlie    Finance  55000          3
4  4   Diana         IT  62000          5
5  5   Ethan         HR  48000          1
Employees with Salary > 55000:
ID  Name Department Salary Experience
2  2   Bob         IT  60000          4
4  4 Diana         IT  62000          5
Data with Bonus Column:
  ID    Name Department Salary Experience Bonus
1  1   Alice         HR  50000          2  2500
2  2     Bob         IT  60000          4  3000
3  3 Charlie    Finance  55000          3  2750
4  4   Diana         IT  62000          5  3100
5  5   Ethan         HR  48000          1  2400









6: STUDY AND IMPLEMENT OF VARIOUS CONTROL STRUCTURES IN R

Aim: 
	To study and implement of various control structures in R.
Algorithm:




















Program:

# 1. if and if...else

x <- 10
if (x > 0) {
  cat("x is positive\n")
} else {
  cat("x is zero or negative\n")
}

# 2. ifelse (vectorized)

marks <- c(85, 45, 70, 30, 90)
result <- ifelse(marks >= 50, "Pass", "Fail")
cat("\nResults using ifelse():\n")
print(data.frame(Marks = marks, Result = result))

# 3. for loop

cat("\nPrinting numbers using for loop:\n")
for (i in 1:5) {
  cat(i, " ")
}

# 4. while loop

cat("\n\nWhile loop (counting up to 3):\n")
count <- 1
while (count <= 3) {
  cat("Count:", count, "\n")
  count <- count + 1
}

# 5. repeat loop with break

cat("\nRepeat loop example:\n")
y <- 1
repeat {
  cat("y =", y, "\n")
  y <- y + 1
  if (y > 3) {
    break
  }
}

# 6. switch statement

cat("\nSwitch statement example:\n")
day <- 3
day_name <- switch(day,
                   "Sunday",
                   "Monday",
                   "Tuesday",
                   "Wednesday",
                   "Thursday",
                   "Friday",
                   "Saturday")
cat("Day 3 is:", day_name, "\n")














Result:

Output:

x is positive
Results using ifelse():
Marks Result
1    85   Pass
2    45   Fail
3    70   Pass
4    30   Fail
5    90   Pass
Printing numbers using for loop:
1	2  3  4  5
While loop (counting up to 3):
Count: 1 
Count: 2 
Count: 3
Repeat loop example:
y = 1 
y = 2 
y = 3
Switch statement example:
Day 3 is: Tuesday





7: STUDY AND IMPLEMENTATION OF DATA VISUALIZATION WITH GGPLOT2

Aim: 
	To study and implementation of data visualization with ggplot2
library(ggplot2).
Algorithm:




















Program:

library(ggplot2)
# Sample data
data <- data.frame(Category = c("A", "B", "C", "D"), Values = c(10, 23, 17, 9))
scatter_data <- data.frame(x = rnorm(50), y = rnorm(50), Group = sample(c("G1", "G2"), 50, TRUE))
line_data <- data.frame(Time = 1:10, Measurement = cumsum(rnorm(10)))

# Plots
print(ggplot(data, aes(Category, Values)) + geom_bar(stat="identity", fill="steelblue") + ggtitle("Bar Chart Example"))
print(ggplot(scatter_data, aes(x, y, color = Group)) + geom_point(size=3) + ggtitle("Scatter Plot Example") + theme_minimal())
print(ggplot(line_data, aes(Time, Measurement)) + geom_line(color="darkred", size=1) + ggtitle("Line Plot Example"))













Result:

Output/Plots:

   


 





 












	


8: IMPLEMENT APRIORI ALGORITHM TO EXTRACT ASSOCIATION RULE OF DATA MINING

Aim: 
	To study implement Apriori algorithm to extract association rule of data mining
Algorithm:

















Program:

# Transactions

transactions <- list(
  c("milk", "bread", "butter"),
  c("bread", "butter"),
  c("milk", "bread"),
  c("milk", "butter"),
  c("bread", "butter", "jam"),
  c("milk", "bread", "butter", "jam")
)

# Minimum thresholds

min_support <- 0.3
min_conf <- 0.7

# Support function

support <- function(items, trans) {
  sum(sapply(trans, function(t) all(items %in% t))) / length(trans)
}

# Unique items

items <- unique(unlist(transactions))

# Frequent 1-itemsets

cat("Frequent 1-itemsets:\n")
for (i in items) {
  s <- support(i, transactions)
  if (s >= min_support) cat(sprintf("{%s} support: %.2f\n", i, s))
}

# Association rules from 2-itemsets

cat("\nAssociation Rules:\n")
for (i in 1:(length(items)-1)) {
  for (j in (i+1):length(items)) {
    A <- items[i]; B <- items[j]
    sAB <- support(c(A, B), transactions)
    cA_B <- sAB / support(A, transactions)
    cB_A <- sAB / support(B, transactions)
    
    if (sAB >= min_support && cA_B >= min_conf)
      cat(sprintf("{%s} => {%s} (support: %.2f, conf: %.2f)\n", A, B, sAB, cA_B))
    if (sAB >= min_support && cB_A >= min_conf)
      cat(sprintf("{%s} => {%s} (support: %.2f, conf: %.2f)\n", B, A, sAB, cB_A))
  }
}


































Result:

Output:


Frequent 1-itemsets:

{milk} support: 0.67
{bread} support: 0.83
{butter} support: 0.83
{jam} support: 0.33

Association Rules:

{milk} => {bread} (support: 0.50, conf: 0.75)
{milk} => {butter} (support: 0.50, conf: 0.75)
{bread} => {butter} (support: 0.67, conf: 0.80)
{butter} => {bread} (support: 0.67, conf: 0.80)
{jam} => {bread} (support: 0.33, conf: 1.00)
{jam} => {butter} (support: 0.33, conf: 1.00)





























9: IMPLEMENT K-MEANS CLUSTERING TECHNIQUE

Aim: 
	To implement K-means clustering technique
Algorithm:































Program:

# Load required packages

library(ClusterR)
library(cluster)

# Load the dataset

data(iris)

# Check the structure of the dataset 

str(iris)

# Remove the species label

df <- iris[,-5]
head(df)

# Set seed for reproducibility

set.seed(123)

# Fit k-means clustering model

km <- kmeans(df, centers = 3)
km

# Check cluster assignments

km$cluster

# Confusion matrix

cm <- table(iris$Species, km$cluster)
cm

# Basic cluster visualization

plot(df[c("Sepal.Length", "Sepal.Width")],  # fixed typo
     col = km$cluster,
     main = "K-means Clustering",
     xlab = "Sepal Length",
     ylab = "Sepal Width")

# Enhanced visualization using clusplot

clust <- km$cluster
clusplot(df[, c("Sepal.Length", "Sepal.Width")],  # use 'df' instead of 'iris_1'
         clust,
         color = TRUE,
         shade = TRUE,
         labels = 2,
         lines = 0,
         main = "Clusters of iris dataset using k-means",
         xlab = "Sepal Length",
         ylab = "Sepal Width")



























Result:

Output:

'data.frame':	150 obs. of  5 variables:
 $ Sepal.Length: num  5.1 4.9 4.7 4.6 5 5.4 4.6 5 4.4 4.9 ...
 $ Sepal.Width : num  3.5 3 3.2 3.1 3.6 3.9 3.4 3.4 2.9 3.1 ...
 $ Petal.Length: num  1.4 1.4 1.3 1.5 1.4 1.7 1.4 1.5 1.4 1.5 ...
 $ Petal.Width : num  0.2 0.2 0.2 0.2 0.2 0.4 0.3 0.2 0.2 0.1 ...
 $ Species     : Factor w/ 3 levels "setosa","versicolor",..: 1 1 1 1 1 1 1 1 1 1 ...




Plots:



 



 
	















10: IMPLEMENT ANY ONE HIERARCHAL CLUSTERING


Aim: 
	To  implement any one hierarchal clustering. 
Algorithm: 




















Program:

install.packages("dplyr")
library(dplyr)

#summary of dataset in package 

head(mtcars)

#finding distance matrix

distance_mat<-dist(mtcars,method='euclidean')
distance_mat

#Fitting Hierarchical clustering Model 
#to trainind dataset

set.seed(240)

#Settind seed
Hierar_cl<-hclust(distance_mat,method="average")
Hierar_cl

#plotting dendrogram 

plot(Hierar_cl)

#choosind no of clusters
#cutting tree byu height

abline(h=110,col="green")

#cutting tree by no.of clusters

 fit<- cutree(Hierar_cl,k=3)
 fit
 table(fit)
 rect.hclust(Hierar_cl,k=3,border="green")


















Result:

Output/Plots:

 












11: IMPLEMENT CLASSIFICATION ALGORITHM

Aim:
	To implement classification algorithm.
Algorithm:









































Program:

library(rpart)
data(iris)
model <- rpart(Species ~ ., iris, method = "class")
print(model)
plot(model); text(model, use.n = TRUE)
pred <- predict(model, iris, type = "class")
conf_matrix <- table(pred, iris$Species)
print(conf_matrix)
cat("Accuracy:", round(sum(diag(conf_matrix)) / sum(conf_matrix) * 100, 2), "%\n")















Result:

Output:

n= 150 

node), split, n, loss, yval, (yprob)
      * denotes terminal node

1) root 150 100 setosa (0.33333333 0.33333333 0.33333333)  
  2) Petal.Length< 2.45 50   0 setosa (1.00000000 0.00000000 0.00000000) *
  3) Petal.Length>=2.45 100  50 versicolor (0.00000000 0.50000000 0.50000000)  
    6) Petal.Width< 1.75 54   5 versicolor (0.00000000 0.90740741 0.09259259) *
    7) Petal.Width>=1.75 46   1 virginica (0.00000000 0.02173913 0.97826087) *
pred         setosa versicolor virginica
  setosa         50          0         0
  versicolor      0         49         5
  virginica       0          1        45
Accuracy: 96 %









Plots:
12: IMPLEMENT DECISION TREE

Aim:
	To implement decision tree.
Algorithm:
























Program:

# Load necessary library
library(rpart)

# Load the iris dataset
data(iris)

# Build the decision tree model
model <- rpart(Species ~ ., data = iris, method = "class")

# Print the model
print(model)

# Plot the decision tree (basic)
plot(model)
text(model, use.n = TRUE)

library(rpart.plot)
rpart.plot(model)













Result:

Output:
n= 150 

node), split, n, loss, yval, (yprob)
      * denotes terminal node

1) root 150 100 setosa (0.33333333 0.33333333 0.33333333)  
  2) Petal.Length< 2.45 50   0 setosa (1.00000000 0.00000000 0.00000000) *
  3) Petal.Length>=2.45 100  50 versicolor (0.00000000 0.50000000 0.50000000)  
    6) Petal.Width< 1.75 54   5 versicolor (0.00000000 0.90740741 0.09259259) *
    7) Petal.Width>=1.75 46   1 virginica (0.00000000 0.02173913 0.97826087) *

Plots:

 

13: IMPLEMENT LINEAR REGRESSION

Aim:
	To implement linear regression.
Algorithm:
















Program:

data(mtcars)
model <- lm(mpg ~ hp, mtcars)
summary(model)
plot(mtcars$hp, mtcars$mpg, pch=19, col="blue", main="MPG vs Horsepower", xlab="Horsepower", ylab="MPG")
abline(model, col="red", lwd=2)
print(predict(model, data.frame(hp=c(100,150,200))))


















Result:

Output:

1        2        3 
23.27603 19.86462 16.45320



Plots:



 
