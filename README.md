# cis400-PUBG-final-project
CIS400 Social Media Data Mining Final Project (Ansell, Samuel | Haws, Samuel | Stewart, Daniel)


Our initial plans were to have all three parts of our system hosted live on Heroku,
however we have ran into problems deploying python/flask servers. Therefore, to test our
system in its current state, you must run these individual elements locally.

Overall steps for running our web sentiment analysis system:

1. Start flask server for twitter sentiment
2. Start the client

- *Please note that flask server must be started first before trying out the client!*

Guide for starting Samuel Ansell's twitter sentiment aspect of the project:

* You will need to download a few python packages to run this part of the project.
  * This should be done in the route folder of the overall project directory.
* Namely:
  * twitter
  * request
  * pymongo
  * flask
* To verify each install, simply enter in the terminal/cmd (without ''):
  * `$ 'name of package' -v`
  * `> 'name of package' --version`
* Once all dependencies have been properly installed, `cd` into the '/sansell-pubg-sentiment/' folder, then:
  * `> python MainFile.py`     - into the command prompt
* After a minute or two you should start seeing information about Flask.
* You can now move onto the client/web portal part of the project!
* If there are any problems running this part of the software locally, please send me an email at sansell@syr.edu


Guide for starting Daniel Stewart's client/web portal:

* The client is successfully deployed at https://pubg-client.herokuapp.com/
* However, because we were not able to deploy the other pieces on Heroku, you must also run the client locally.
* To do so, you must install https://nodejs.org/en/
  * If you are on a Mac, I recommend installing with Homebrew:
    * https://www.dyclassroom.com/howto-mac/how-to-install-nodejs-and-npm-on-mac-using-homebrew
  * To verify the install, the following commands should both produce version numbers:
    * `$ node -v`
    * `$ npm -v`
* Once node has been installed, `cd` into the dastew02-client/ directory

- `ls`, and verify there is indeed a file titled 'package.json'

* run `npm install` - which may take several minutes (installing all dependencies in package.json)
* run `npm start` - this will launch the local development server at localhost:3000 (and should automatically open in the browser)

- Click 'Player Stats' and enter a players in-game name to make a GET request over to one of the Flask servers, and present their player data to the user
- Click 'Twitter Sentiment' which will make a GET request over to one of the Flask servers, and present the Twitter sentiment data provided as a line graph to the user
- If there are any problems running this part of the software locally, please shoot me an email at dastew02@syr.edu


Guide for running the PUBG API Mining program:

* The part of the program that utilizes the PUBG developer API was developed by Samuel Haws. There was an error in returning the results of the program run through a flask server to the web client, however, the program is fully functional as a standalone python application. This application is written in Python 3.6, and can be run from the command line as per the usual method of navigating to the directory and typing "CIS400_PUBG.py". 
* The program uses a few dependencies/packages, all of which are easily pip installed (listed in source).
* The program has two separate functionalities: a weapon stats functionality, and a map player position trace functionality.
* The weapon stats are represented in three different count dictionaries: # of times the specified player attacked with each weapon over most recent (specified number) of matches, # of kills with each weapon, and the ratio of kills to attacks for each weapon. 
* The player position trace function is commented out by default (along with its call in the main getPlayerStats) so that the user can first easily view weapon stats. To use map functionality, uncomment these two items, and follow instructions in source to fetch base map image file. 
* If there are any questions with this program, please reach out to me at sahaws@syr.edu.
