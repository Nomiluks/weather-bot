# Weatherbot Tutorial (using the latest release of Rasa NLU and Rasa Core)

## How to use this repo

The code of this repo differs quite significantly from the original video. This is how to use it:

### Training the NLU model

Training of the NLU model didn't change much from the way it was shown in the video. To train and test the model run:  

``` python nlu_model.py ```

### Training the Rasa Core model

The biggest change in how Rasa Core model works is that custom action 'action_weather' now needs to run on a separate server. That server has to be configured in a 'endpoints.yml' file.  This is how to train and run the dialogue management model:  
1. Start the custom action server by running:  

``` python -m rasa_core_sdk.endpoint --actions actions ```  

2. Open a new terminal and train the Rasa Core model by running:  

``` python dialogue_management_model.py```  
 
3. Talk to the chatbot once it's loaded.  

### Starting the interactive training session:

The process of running the interactive session is very similar to training the Rasa Core model:
1. Make sure the custom actions server is running:  

``` python -m rasa_core_sdk.endpoint --actions actions ```  

2. Start the interactive training session by running:  

``` python train_interactive.py ```  


Latest code update: 09/06/2019
Latest compatible Rasa NLU version: 0.15.1
Latest compatible Rasa Core version: 0.14.5





