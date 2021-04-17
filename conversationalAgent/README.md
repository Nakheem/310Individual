# COSC310-T11
**Note: All medical information in this project is not professional medical advice and should not be percieved as such. The sole purpose of the project is to learn how to create AI chatbots.**

**The Agent and User class files must be run to start the program. We need to start the Agent (server side) first and then start the execution of the User (client side) so that an Agent is available to provide service to a User.**

- The project is focused on creating an AI conversational agent which takes the role of a psychologist.
- Two Java programs need to be run for the converstaion, these are Agent.java and User.java. The agent acts as the server seeking connections from users continuously whereas the user establishes connection with the server when in need of a conversation, acting as a client. Only the User.java file runs at the users end. The User.java file also uses the GUI_Frame.java and GUI_Panel.java files to make a UI which the user can use to talk with the agent.
- Apart from the basic conversation and functionality such as ending and establishing connections, etc., the agent makes use of the questionBank.txt, questionBank2.txt and namedResponsesBank.txt files to provide answers to the user's questions. The file needs to be placed correctly in reference to the Agent.java file in the server-end storage.
- The code functions as required.


## **Updates**

### Features added:

**Java classes were created to handle all the GUI related aspects of the app:**
* The input is now received from the user using an ActionListener instead of a Scanner
* A method was created (getUserInput) which stalls the program to wait for user input.
* The user now has a custom text entry field to enter their responses instead of the single window in the console.

**Name recognition using Stanford CoreNLP library:**
* The agent will now recognize when the user sends a message with a name in it
* The agent will then give a response that includes the name the user mentioned making the conversation feeling more realistic
* Example: 
* <img src="conversation_examples/name_recognition_example.png?raw=true" width="500"> 

**Spelling mistake detection:**
* If the user sends a message with a word or even several words with spelling mistakes in them, the agent will still respond with the correct response.
* The threshold is that the user’s message must match 80% to the agent’s associated response data
* <img src="conversation_examples/spelling_mistake_recognition_example.png?raw=true" width="500">

**Agent understands different word orders:**
* User responses which are similar but have different word orders are still recognized by the agent
* <img src="conversation_examples/word_order_recognition_example.png?raw=true" width="500">

**The agent recognizes questions:**
* If the user sends a message with a question that the agent doesn’t understand, the agent will respond saying the don’t understand their question.
* <img src="conversation_examples/question_recognition_example.png?raw=true" width="500">

**The agent now reads from multiple response data files:**
* the agent now will check for responses related to ADHD from a file specific for that topic.

**New features added for indvidual project**

**Currently working**

**Wikipedia integration to add wikipedia snippets and links to Conversations**
*If the user as what something is and the program doesn't recognize it search wikipedia*
*Reads out wiki article snippets and proveds links*


**Currently not working  but wanted to implement**

**Google Transalate api**

*Was supposed to detect language entered into chat bot and switch the default language*
*Couldnt get it work kept getting sever errors*
