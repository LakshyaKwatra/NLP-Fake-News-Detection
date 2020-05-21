# NLP-Fake-News-Detection
HIGHEST ACCURACY ACHIEVED: > Binary-> 0.62	Model: SVM
                  			   > Six-way-> 0.25     Model: SVM
          
# APPROACH: 
I started with the data exploration and analysis using seaborn to check for the correlations between the data and then i tried to extract some other features like length of the statement, numerical count in the statement,etc. 
I decided to focus on the statement and not on the justification. Then I dealt with the missing data. 

For implementing binary classification, I created another column in the dataframe with 'True' and 'False' values based on the 'label' values. 
I marked 'false','barely true','pants-fire' as 'False' and rest as true for Binary Classification.

Then I created a function text_process() to process the given text to remove punctuations and clean the text and then created Pipelines to test out various models. I used CountVectorizer for tokenization and TfidfTransformer for normalization of the text.
Then I checked the classification report and confusion matrix of each model to find the best possible accuracy. 
The SVM model was giving the best accuracy (Binary: 62%, Six-way: 25%) when its 'C' and 'gamma' parameters were adjusted
with GridSearchCV (This takes some time to run depending on the computer speed).
 
# MODELS I TRIED OUT: 
Logistic Regression
SVM*
Random Forest 
Multinomial Naive Bayes

# INSTRUCTIONS:
VERSION: Python 3.7.3 
FORMAT: The code is shared as a Jupyter Notebook in .ipynb format. So you need to have jupyter notebook installed.
>Windows: pip install jupyter

# FILES:
VIEW_CODE.ipynb -> Contains fully commented code in a 'single cell' for better readability. Needs to be opened with Jupyter Notebook
RUN_CODE.ipynb** -> Contains the code segmented in different cells with the output of every cell. This demonstrates the working of my code.
Need to be opened with Jupyter Notebook.   

# LIBRARIES: 
The Following Python Libraries need to be installed:
numpy, 
pandas, 
matplotlib.pyplot, 
seaborn, 
nltk,     
sklearn
 
# OTHER DETAILS: 
nltk 'stopwords' is required which has been downloaded in the code itself with the nltk.download('stopwords') command present in the notebook after the imports.
Any cell in the notebook can be run by pressing 'Shift+Enter'.
The SVM model's pipeline takes quite some time to fit because of the Grid Search for the best parameters 'C' and 'gamma'. 

**Use 'RUN_CODE.ipynb' to run each cell for getting a better understanding.

