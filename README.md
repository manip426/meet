# meet
Objective:
To build a serverless, progressive web application (PWA) with React using a test-driven development (TDD) technique. The application uses the Google Calendar API to fetch upcoming events.

Key Features:
Filter events by city.
Show/hide event details.
Specify number of events.
Use the app when offline.
Add an app shortcut to the home screen.
View a chart showing the number of upcoming events by city.

User Stories:
As a user, I would like to be able to filter events by city so that I can see the list of events that take place in that city.
As a user, I would like to be able to show/hide event details so that I can see more/less information about an event.
As a user, I would like to be able to specify the number of events I want to view in the app so that I can see more or fewer events in the events list at once.
As a user, I would like to be able to use the app when offline so that I can see the events I viewed the last time I was online.
As a user, I would like to be able to add the app shortcut to my home screen so that I can open the app faster.
As a user, I would like to be able to see a chart showing the upcoming events in each city so that I know what events are organized in which city.

1: FILTER EVENTS BY CITY
• As a user, I would like to be able to filter events by city so that I can see the list of
events that take place in that city.
Scenario 1: WHEN USER HASN’T SEARCHED FOR A CITY, SHOW UPCOMING
EVENTS FROM ALL CITIES.
Given user hasn’t searched for any city
When the user opens the app
Then the user should see a list of all upcoming events

Scenario 2: USER SHOULD SEE A LIST OF SUGGESTIONS WHEN THEY SEARCH
FOR A CITY.
Given the main page is open
When user starts typing in the city textbox
Then the user should see a list of cities (suggestions) that match what they’ve typed
Scenario 3: USER CAN SELECT A CITY FROM THE SUGGESTED LIST.
Given the user was typing “Berlin” in the city textbox and the list of suggested cities is showing
When the user selects a city (e.g., “Berlin, Germany”) from the list
Then their city should be changed to that city (i.e., “Berlin, Germany”) and the user should 
receive a list of upcoming events in that city

2: SHOW/HIDE AN EVENT'S DETAILS
• As a user, I would like to be able to show/hide event details so that I can see more/
less information about an event.
Scenario 1: An event element is collapsed by default
Given The user is on main page
When a user selects and event
Then an element collapsed by default
Scenario 2: User can expand an event to see its details
Given user is seeing the events
When a user chooses and event and click on it
Then an element expands with details
Scenario 3: User can collapse an event to hide its details
Given user is seeing the events
When a user clicks on the event details
Then the element details hide

3: SPECIFY NUMBER OF EVENTS
• As a user, I would like to be able to specify the number of events I want to view in
the app so that I can see more or fewer events in the events list at once.
Scenario 1: When user hasn’t specified a number, 32 is the default number
Given user open the app
When user look for an event
Then 32 events max will be shown
Scenario 2: User can change the number of events they want to see
Given user open the app
When a user clicks on the event details
Then the element details hide

4: USE THE APP WHEN OFFLINE
• As a user, I would like to be able to use the app when offline so that I can see the
events I viewed the last time I was online
Scenario 1: user app when offline.
Given the user has no internet connection.
When user wants to use the app
Then the user should see cached data
Scenario 2: Show error when user changes the settings (city, time range).
Give the user has no internet connection.
When user goes to settings and try to change city and/or time range
Then show error an error message.

5: DATA VISUALIZATION
• As a user, I would like to be able to see a chart showing the upcoming events in
each city so that I know what events are organized in which city.
Scenario 1: Show a chart with the number of upcoming events in each city
Give user looking for events in general
When user clicks on a map
Then show a chart with the number of upcoming events in each city
