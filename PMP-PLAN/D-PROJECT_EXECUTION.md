# PROJECT OVERVIEW

## EXECUTING THE PROJECT

### Project Design and Coding

<br>Flowchart of Chatbot’s functionality

![alt text](https://github.com/NaufalFiqri/Mental_health_chatbot/blob/main/src/images/Flowchart_Functionality.png "Flowchart_Functionality")

<br>Flowchart of Implementing the Chatbot

![alt text](https://github.com/NaufalFiqri/Mental_health_chatbot/blob/main/src/images/Flowchart_Implementation.png)       
 

<br> Description of the project coding and implementation
 
First, we install required libraries and packages in order to use their functions. The libraries and packages are as follows:
<br>numpy = =1.18.1
<br>torch torchvision torchaudio
<br>nltk = = 3.7

Intents,json is a training data which have different intents. Each intents have different tags, patterns, and responses. Thus, whenever new sentences come in, the bot will classify it in one of these tags and takes the corresponding response.

![alt text](https://github.com/NaufalFiqri/Mental_health_chatbot/blob/main/src/images/Intents1.png)
![alt text](https://github.com/NaufalFiqri/Mental_health_chatbot/blob/main/src/images/Intents2.png)
![alt text](https://github.com/NaufalFiqri/Mental_health_chatbot/blob/main/src/images/Intents3.png)
![alt text](https://github.com/NaufalFiqri/Mental_health_chatbot/blob/main/src/images/Intents4.png) 
![alt text](https://github.com/NaufalFiqri/Mental_health_chatbot/blob/main/src/images/Intents5.png)
 
<br>Nltk_utils.py is a Python file that consists of a few methods of basic Natural Language Processing (NLP) such as tokenization, stemming, and bagging of words. In the tokenize method, the sentence is split into an array of words or tokens, and the punctuation characters or numbers are included. The stemming method will generate the root form of the word. For example, "organize," "organizes," and "organises" will become "organ." While the bag of words method takes each stemmed word and places it in an array called "bag of words," which converts it to 1 (known words that exist in the sentence) and 0 (unknown words that do not exist in the sentence).

![alt text](https://github.com/NaufalFiqri/Mental_health_chatbot/blob/main/src/images/nltk_utils.png) 
<br>
<br>Implementation of the chatbot is using a model called Feed Forward Neural Network, which consists of a few layers such as an input layer (bag of words), hidden layers, an output layer (number of classes) and the activation function RELU. The torch library is imported into the coding.

![alt text](https://github.com/NaufalFiqri/Mental_health_chatbot/blob/main/src/images/model.png)
 
<br>Train.py is for the NLP processing pipeline, which combines all the processes. Firstly, the data will tokenize each word in the patterns. Then, the process will do the stemming, which generates the root form of the words and lowers their case. Punctuation characters have been ignored too. After that, the words will be converted into a numerical concept called "bag of words." The data will be trained using a Feed-Forward Neural Network, and the hyper-parameters are set as follows:
<br>Number of epochs = 1000
<br>Batch size = 8
<br>Learning rate = 0.001
<br>Input size = number of bag words
<br>Hidden size = 8
 
<br>Output size = number of different classes or tags
The optimizer was also used in the model, where it changed the neural network's attributes such as weights and learning rate to reduce losses. The train will stop until the number of epochs reaches 1000, and the final loss will be displayed in 4 decimal places. Lastly, the trained data will be saved into data.pth.

![alt text](https://github.com/NaufalFiqri/Mental_health_chatbot/blob/main/src/images/train.png) 
![alt text](https://github.com/NaufalFiqri/Mental_health_chatbot/blob/main/src/images/train2.png)
![alt text](https://github.com/NaufalFiqri/Mental_health_chatbot/blob/main/src/images/train3.png)
 
<br>Implementation of the chatbot starts by loading the trained data (data,pth). The get_response method is implemented where it will do tokenization and all words will put in the bag of words. The output will then use SoftMax to get the probability of accuracy of the sentence. The condition is set up at 0.75 of accuracy. If the probability of sentence is more than 0.75, it will classify which tag it belongs to. Hence, the bot will response according to that tag. If less than 0.75, “Sorry, I do not understand…” will be displayed by the chatbot

![alt text](https://github.com/NaufalFiqri/Mental_health_chatbot/blob/main/src/images/chat.png)
 

<br>The GUI of Mental Health Chatbot is implemented by using Tkinter library and get_response method is imported from the chat.py file so that the method will run in GUI to response the user. The GUI is set as follows:

Interfaces	Descriptions
<br>Window size	is 12800 x 720 x 0 x 0 with functionalities of delete and maximize or minimize the size of the frame.
<br>Window title is "Group J Project NLP"
<br>Background colour is	green symbolises as breast cancer awareness
<br>Text colour	is black
<br>Font	Brixton
<br>Font size	13
<br>Head label	“MENTAL HEALTH CHATBOT” is written at the middle of the frame and the colour is pink
<br>Scroll bar	Scrolling up and down the chat.
<br>Message entry box	size is 0.74 x 0.06 x 0.011 x 0.008 and place at the bottom of the frame and the colour is green
<br>Send button size is	0.22 x 0.06 x 0.77 x 0.008, place beside message entry box and has press functionality to send the chat as “You” and the colour of button is green

![alt text](https://github.com/NaufalFiqri/Mental_health_chatbot/blob/main/src/images/app1.png)
![alt text](https://github.com/NaufalFiqri/Mental_health_chatbot/blob/main/src/images/app2.png)
 
<br>Project Result
<br>Result using Tkinter:

![alt text](https://github.com/NaufalFiqri/Mental_health_chatbot/blob/main/src/images/app3.png)



