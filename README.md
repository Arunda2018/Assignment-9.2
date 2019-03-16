# Assignment-9.2
1. Use the below given data set
DataSet
2. Perform the below given activities:
a. Create classification model using different decision trees.
b. Verify model goodness of fit.
c. Apply all the model validation techniques.
d. Make conclusions

set.seed(678)
path <- 'https://raw.githubusercontent.com/thomaspernet/data_csv_r/master/data/titanic_csv.csv'
titanic <-read.csv(path)
head(titanic)

X pclass survived                                            name    sex
## 1 1      1        1                   Allen, Miss. Elisabeth Walton female
## 2 2      1        1                  Allison, Master. Hudson Trevor   male
## 3 3      1        0                    Allison, Miss. Helen Loraine female
## 4 4      1        0            Allison, Mr. Hudson Joshua Creighton   male
## 5 5      1        0 Allison, Mrs. Hudson J C (Bessie Waldo Daniels) female
## 6 6      1        1                             Anderson, Mr. Harry   male
##       age sibsp parch ticket     fare   cabin embarked
## 1 29.0000     0     0  24160 211.3375      B5        S
## 2  0.9167     1     2 113781 151.5500 C22 C26        S
## 3  2.0000     1     2 113781 151.5500 C22 C26        S
## 4 30.0000     1     2 113781 151.5500 C22 C26        S
## 5 25.0000     1     2 113781 151.5500 C22 C26        S
## 6 48.0000     0     0  19952  26.5500     E12        S
##                         home.dest
## 1                    St Louis, MO
## 2 Montreal, PQ / Chesterville, ON
## 3 Montreal, PQ / Chesterville, ON
## 4 Montreal, PQ / Chesterville, ON
## 5 Montreal, PQ / Chesterville, ON
## 6                    New York, NY
tail(titanic)

Output
X pclass survived                      name    sex  age sibsp
## 1304 1304      3        0     Yousseff, Mr. Gerious   male   NA     0
## 1305 1305      3        0      Zabour, Miss. Hileni female 14.5     1
## 1306 1306      3        0     Zabour, Miss. Thamine female   NA     1
## 1307 1307      3        0 Zakarian, Mr. Mapriededer   male 26.5     0
## 1308 1308      3        0       Zakarian, Mr. Ortin   male 27.0     0
## 1309 1309      3        0        Zimmerman, Mr. Leo   male 29.0     0
##      parch ticket    fare cabin embarked home.dest
## 1304     0   2627 14.4583              C          
## 1305     0   2665 14.4542              C          
## 1306     0   2665 14.4542              C          
## 1307     0   2656  7.2250              C          
## 1308     0   2670  7.2250              C          
## 1309     0 315082  7.8750              S
