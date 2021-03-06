# goodlife-booking-alerter

Goodlife Booking Alerter is an automated bot that will check Goodlife Fitness for booking time slots and whether they are available or not. 
In order to use GBA, your account must first be logged in within the program. At the moment, GBA will only alert you for one time slot, not multiple.

NOTICE:
GBA is no longer working due to the fact that I've long abandoned progress on the project, as Goodlife Fitness is now closed due to COVID.
If you'd like to take the source and make your own version of GBA, feel free to fork the project and do so yourself.

Notes:
- In order for GBA to function, you need a specific version of Chrome that is specified on the Releases page. The Chrome version is related to the version of GBA.
- GBA creates a folder to store data in the running directory that you execute the JAR file in. Since GBA does not have administrative privileges, the program will not work if you run it in a folder that requires superuser/administrative privileges, such as Program Files.
- Past the login screen, the day number input field must be BEFORE the month you are currently in ends. (Goodlife updates their time slot API at the beginning of the month.)

GBA uses the following libraries and are packaged into the JAR:

- Selenium3
- gson for json parsing
- apache commons io (previously)
- javafx 

GBA also uses chrome which is packaged into the JAR as chromedriver.exe. Upon JAR execute, GBA will create a folder named "Driver" within the current running directory and unpack the chromedriver into that folder so that Java can run the executable. Chrome is used to search for web elements and interact with them, emulating a real user.

TO-DO:

- Add a config file to handle GBA looking for chrome.exe automatically on startup as well as logging and other features.
- Implement logging and print stacktraces to an output file that can either be turned off or on in the config.
- ~~Instead of freezing the Controller while the webdriver loads the page, implement a separate thread for the driver so that the Controller does not hang while it loads.~~
- ~~Restructure package access so that everything fits under com.robert~~
 
