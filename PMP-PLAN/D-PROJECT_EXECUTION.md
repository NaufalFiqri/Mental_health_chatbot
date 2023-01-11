# PROJECT OVERVIEW

## D. EXECUTING THE PROJECT

### Project Design and Coding

Flowchart of Chatbot’s functionality
<img src="
 
Flowchart of Implementing the Chatbot
<src="images/Flowchart_Implementation.png" width="60%">         
 
Description of the project coding and implementation
First, we install required libraries and packages in order to use their functions. The libraries and packages are as follows:
numpy = =1.18.1
torch torchvision torchaudio
nltk = = 3.7

Intents,json is a training data which have different intents. Each intents have different tags, patterns, and responses. Thus, whenever new sentences come in, the bot will classify it in one of these tags and takes the corresponding response.






 



 
Nltk_utils.py is a Python file that consists of a few methods of basic Natural Language Processing (NLP) such as tokenization, stemming, and bagging of words. In the tokenize method, the sentence is split into an array of words or tokens, and the punctuation characters or numbers are included. The stemming method will generate the root form of the word. For example, "organize," "organizes," and "organises" will become "organ." While the bag of words method takes each stemmed word and places it in an array called "bag of words," which converts it to 1 (known words that exist in the sentence) and 0 (unknown words that do not exist in the sentence).

 
Implementation of the chatbot is using a model called Feed Forward Neural Network, which consists of a few layers such as an input layer (bag of words), hidden layers, an output layer (number of classes) and the activation function RELU. The torch library is imported into the coding.












 
Train.py is for the NLP processing pipeline, which combines all the processes. Firstly, the data will tokenize each word in the patterns. Then, the process will do the stemming, which generates the root form of the words and lowers their case. Punctuation characters have been ignored too. After that, the words will be converted into a numerical concept called "bag of words." The data will be trained using a Feed-Forward Neural Network, and the hyper-parameters are set as follows:
Number of epochs = 1000
Batch size = 8
Learning rate = 0.001
Input size = number of bag words
Hidden size = 8
Output size = number of different classes or tags
The optimizer was also used in the model, where it changed the neural network's attributes such as weights and learning rate to reduce losses. The train will stop until the number of epochs reaches 1000, and the final loss will be displayed in 4 decimal places. Lastly, the trained data will be saved into data.pth.





























Implementation of the chatbot starts by loading the trained data (data,pth). The get_response method is implemented where it will do tokenization and all words will put in the bag of words. The output will then use SoftMax to get the probability of accuracy of the sentence. The condition is set up at 0.75 of accuracy. If the probability of sentence is more than 0.75, it will classify which tag it belongs to. Hence, the bot will response according to that tag. If less than 0.75, “Sorry, I do not understand…” will be displayed by the chatbot

 
The GUI of Mental Health Chatbot is implemented by using Tkinter library and get_response method is imported from the chat.py file so that the method will run in GUI to response the user. The GUI is set as follows:

Interfaces	Descriptions
Window size	12800 x 720 x 0 x 0 with functionalities of delete and maximize or minimize the size of the frame.
Window title	Group J Project NLP
Background colour	Green symbolises as breast cancer awareness
Text colour	Black
Font	Brixton
Font size	13
Head label	“MENTAL HEALTH CHATBOT” is written at the middle of the frame and the colour is pink
Scroll bar	Scrolling up and down the chat.

Message entry box	0.74 x 0.06 x 0.011 x 0.008 place at the bottom of the frame and the colour is green
Send button	0.22 x 0.06 x 0.77 x 0.008 place beside message entry box and has press functionality to send the chat as “You” and the colour of button is green








 
Project Result
Result using Tkinter:
 



