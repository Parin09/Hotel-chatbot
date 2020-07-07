# Hotel Chatbot
How to run:
1. rasa train
2. rasa shell

Steps performed:
1. Conversation design:
    * Who: Users who want to book room in the hotel or know more about it.
    * What: Basic faq coupled with room booking and room cleaning request.
    * Typical converstaion:
      * Example 1:
        User: I want to book a room.<br/>
        Bot: How many rooms would you like to book?<br/>
        User: 2 rooms<br/>
        Bot: What type of room would you want to book?<br/>
        Button1 - Simple<br/>
        Button 2 - Deluxe<br/>
        User: (Clicks on Button 1)<br/>
        Bot: You have chosen to book 2 simple rooms<br/>
        (Clicking on button 2 should be handled similarly)<br/>
      * Example 2:
        User: I want to have my room cleaned<br/>
        Bot: When should I arrange for a cleaning?<br/>
        User: Could you send someone right now?<br/>
        Bot: Sure, I will send someone to your room right away.<br/>
      * Example 3:
        User: I want to have my room cleaned<br/>
        Bot: When should I arrange for a cleaning?<br/>
        User: Could you send someone after 2 hours?<br/>
        Bot: Sure, I have scheduled a cleaning for 5 pm today.<br/>
      * Example 4:
        User: What are your check-in timings?<br/>
        Bot: Check-in time starts at 4 PM. Minimum check-in age is 21. Please contact the reception for early check-in requests.
        
 2. Intents and Entities
    * Intents:
      - Greetings
      - Goodbye
      - Room booking
         * with number of rooms specified
         * with number of rooms not specified
      - Room Cleaning
         * Right away
         * after some time
      - Check in time
      - Check out time
      - Cancel reservation
      - Cancellation Policy
      - Restaurant
      - Breakfast Availability
      - Breakfast Timings
      - Restaurant timings
      
    * Entities:
      - Number of rooms
      - Room type
         * Simple
         * Deluxe
         
    Edit nlu to include intents with entities
3. Dialouge Management
   * Stories:
      - Room booking without number of rooms specified
      - Room booking with number of rooms specified
      - Room cleaning right away
      - Room cleaning after some time
      - FAQ check in time
      - FAQ check out time
      - FAQ cancel reservation
      - FAQ cancellation policy
      - FAQ restaurant
      - FAQ breakfast avaliability
      - FAQ breakfast timing
      - FAQ restaurant timing
      - Bonus story
      
     Edit stories.md to include them
  
4. Edit domain.yml to include intents, slots and responses.

5. Edit credentials.yml to include fb credentials
(Facebook messenger works by exposing localhost port using ngrok)

Output:
All output screenshots under the folder screenshots
1. Testing on cmd line:
![](/screenshots/cmd_ss1.PNG)
2. Facebook messenger integration
![](/screenshots/bonus_fb_ss.jpg)
