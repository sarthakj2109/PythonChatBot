# Contextual Voice enabled Chatbot
This is a [**Contextual**](https://medium.com/makerobos/what-are-contextual-chatbots-how-they-can-make-a-world-of-difference-in-user-experience-e7446c96664e) [**Voice enabled chatbot**](https://medium.com/@botanalytics/voice-enabled-chatbots-vs-messenger-bots-everything-you-need-to-know-29f2c7a982c1) deployed on a laptop buying guide website, named **Me..Guide**. The chatbot answers user queries asked in natural language _(currently the bot only supports English language)_ . 

### Highlights of the Chatbot
- Its ability to predict the laptop price based on specifications given by user related to brand, RAM, Storage, GPU, Screen Size, etc.
- Supporting voice based queries so that user can interact with the bot by simply speaking and listening.
- The chatbot not only uses keyword recognition technique but also answers accordingto the context of the question being asked

The chatbot uses a Machine Learning Model trained on a [dataset](https://github.com/sarthakj2109/Laptop_Price_Estimation/blob/master/Final%20Updated%20Laptop%20Dataset.csv) of about 300 different laptops to make the prediction. The [pre-processed dataset](new_df.sav) and [trained model](predict_lp_model.sav) can be found in this repository. **This is an integration of a Data Analysis using Python project** named, [**Laptop Price Estimation**](https://github.com/sarthakj2109/Laptop_Price_Estimation) developed earlier. 

To understand the nuances of human communication (natural language) while interacting with the bot, it is trained on [**intents.json**](intents.json) file using a deep learning model. A commendable training accuracy of 83% is achieved considering the multi-class classification problem involoving 85 unique classes. The complete code for training can be found under [train_chatbot.py](train_chatbot.py).    

## Steps to run the chatbot
1. Clone this repository on your local machine and install all the dependencies required in a virtual environment (_recommended_)
2. Simply run [app.py](app.py) by using the command `python flask -m run `. Then open the local host link (_that looks something like this_ http://127.0.0.1:5000/) in **Google Chrome** web browser (currently the chatbot works best in Chrome. It will be extended to other browsers soon)
3. Grant the microphone permissions and voila! the website and bot are ready to be used!

## Steps to train the chatbot 
1. If you wish to train the chatbot to support more queries or replace the existing ones with your own custom queries you need to make changes in the [**intents.json**](intents.json) file. 
2. After making the required changes in intents, run the [train_chatbot.py](train_chatbot) file from your terminal using the command `python tarin_chatbot.py`. 
3. This will create new [`words.pkl`](words.pkl) and [`classes.pkl`](classes.pkl) file which will automatically replace the exiting ones in the folder. 
4. Perform steps 2 and 3 of Steps to run the chatbot

### NOTE
The website **Me..Guide** and the **chatbot** is designed using **HTML**, **CSS** and **Javascript**. The code for the same can be located in the [`static`](static) and [`templates`](templates) folder.   
