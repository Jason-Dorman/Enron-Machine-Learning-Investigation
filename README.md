# Enron-Machine-Learning-Investigation
Using machine learning to find persons of interest in the Enron Scandal

Enron was formed in 1985 through a merger. It was a energy trader and supplier based in Houston. At the time the Energy industry was highly deregulated.

Enron fooled investors with fake holdings and off the book accounting practices to hide mountains of debt and toxic assets.
As an example, they would build assets and immediately add projected revenue to the books. If projected revenue didn't meet expectations they moved assets off the books to hide the loss.

At one point Enron was considered the seventh largest company in the U.S. By 2001 the company was in free fall. Their stock fell to 26 cents. At its peak it was trading at as almost 91 dollars. They lost shareholders 74 billion dollars.

After the investigation an unprecedented amount of emails and confidential financial information for employees was released in the public domain. The dataset for this project includes that financial information, a boolean column that identifies employees as a person of interest or not and the number of emails to and from persons of interest. The data was loaded int a AWS S3 bucket and analysis was done in a zeppelin notebook.

We created a heatmap which I used to create a feature list for a naive bayes model. I selected all of the features that had a 25% or higher correlation with the persons of interest column. 

The training dataset has a 87% accuracy score but the model has some interesting conclusions. The model correctly predicted the CEO and COO were persons of itnerest who both served time for securities fraud and other crimes. More interestingly two people in the model were found not to be a person of interest but the original dataset did list them as a person of interest. Both of those people went to trial but one was acquiited after a long legal battle that went to the Supreme Court and the other had his charges dropped. So the model correctly predicted their invovlement despite it differing from the original dataet.
