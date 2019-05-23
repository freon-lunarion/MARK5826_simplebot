These are json result of step-by-step adding NLP component into Watson Assistant.


Definitions:
- Intent:
    An intent represents the purpose of a user's input. You define an intent for each type of user request you want your application to support. Symbolized by "#"

- Entity:
    An entity represents a term or object that is relevant to your intents and that provides a specific context for an intent. You list the possible values for each entity and synonyms that users might enter. Symbolized by "@"

- Dialog:
    A dialog is a branching conversation flow that defines responses to the defined intents and entities. You use the dialog builder in the tool to create conversations with users to provide responses.


#Step0 - Create a new "Skill"
1. Click "SKill" Tab, and click "Create skill" button
2. On "Create skill" tab, give Name and Description(optional) on input fields
3. Click "Create dialog skill" button

#Step1 - Create a Intent
ref: https://www.youtube.com/watch?v=OPdOCUPGMIQ
1. Click "Create Intent" Button
2. Type the intent name on "#" fields (i.e.: "greeting")
3. Click "Create Intent" button
4. Put some examples, and click "Add example" (i.e: "hello", "hi")
    tips:
    - relevant between sentences and intent
    - have variate forms
    - more sentences is better
5. repeat for 1 or 2 more intent (i.e: "business_hour","booking")


#Step2 - Create a simple dialog
ref:
- default dialog explanation : https://youtu.be/XkhAMe9gSFU?t=44
- create dialog : https://youtu.be/XkhAMe9gSFU?t=146
1. Click Dialog Tab
2. Click "create dialog" button, click "Add Node" button
3. On "If Bot recognizes" section, choose a intent (i.e: "#booking_hour")
4. On "Then Then respond with:" section, write one or more bot response(s)
5. Try the response by using "Try it" button

#Step3 - Entities
1. Click on "Entities" Tab , "System entities" sub tab
2. Click on "Create entity" button
3. Type name of entity and click "Create entity" button
4. Click on the back arrow (top right corner) to the list
5. Click on a entities related to our bot (i.e "@sys-date" and "@sys-time")

#Step4 - connecting Entities to intent's examples
1. on Intents tab, choose a intent (i.e: #booking)
2. highlight part of sentences, type name of the entity (i.e: @num_people)
3. do the same thing to other sentences

#Step5 - Create a more complex dialog (Slots)
ref: https://youtu.be/ES4GHcDsSCI
obj: create dialog to ask back to the user if some information (entities) not given in first user sentences
1. on "dialog" tab, create new dialog
2. click gear icon (top right corner), activate "Slots" feature
3. on "If assistant recognizes:" section, put a intent (i.e: #booking)
4. on "Then check for:" section, Type a entity (i.e @sys-date) on first input field, and the question to user if the information not present, on third field (i.e: what's date?).
5. repeat for other required entities
6. finally, add some respond (on "Then respond with:" section) to giving a feed back to user when all information are complete

#Testing
1. click "Try it" button
2. try to booking with complete information (date, time and number of people).
3. try to booking without any information