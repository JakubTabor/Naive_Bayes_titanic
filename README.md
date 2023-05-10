# Naive_Bayes_titanic
# First i "load" my "csv" and drop "useles" "columns" """df.drop(['PassengerId','Name','SibSp','Parch','Ticket','Cabin','Embarked'],  axis = 'columns', inplace = True)"""
# The "target" column will be "df.Survived" and "inputs" will be my "df" without columns "Survived" "df.drop('Survived', axis = 'columns')"
# Now I need to create (2) different columns with numerical values on my columns "Sex", so I use method "get_dummies" "pd.get_dummies(inputs.Sex)"
# I need to "concatenate" my "dummies" columns with rest of "df", so I use "pd.concat" and save it into "inputs" 
# """inputs = pd.concat([inputs, dummies], axis = 'columns')""" and now I dont need "Sex" columns, so I drop it 
# """inputs.drop('Sex', axis = 'columns', inplace = True)""" I also check if there is any (no value) """inputs.columns[inputs.isna().any()]"""
# I "fill" my "Age" and "Fare" columns with "mean" value "inputs.Age.fillna(inputs.Age.mean())" "inputs.Fare.fillna(inputs.Fare.mean())"
# Now I can import "train_test_split" and get "train" and "test" set, I check length of "X_train" and ""X_test" "len(X_train)" "len(X_test)"
# Then from "sklearn.naive_bayes" I import "GaussianNB" model and train it "model.fit(X_train,y_train)"
