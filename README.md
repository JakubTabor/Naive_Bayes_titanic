# Naive_Bayes_titanic
# First i "load" my "csv" and drop "useles" "columns" """df.drop(['PassengerId','Name','SibSp','Parch','Ticket','Cabin','Embarked'],  axis = 'columns', inplace = True)"""
# The "target" column will be "df.Survived" and "inputs" will be my "df" without columns "Survived" "df.drop('Survived', axis = 'columns')"
# Now I need to create (2) different columns with numerical values on my columns "Sex", so I use method "get_dummies" "pd.get_dummies(inputs.Sex)"
