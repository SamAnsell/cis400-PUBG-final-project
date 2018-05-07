# cis400-PUBG-final-project
CIS400 Social Media Data Mining Final Project (Ansell, Samuel | Haws, Samuel | Stewart, Daniel)


Our initial plans were to have all three parts of our system hosted live on Heroku,
however we have ran into problems deploying python/flask servers. Therefore, to test our
system in its current state, you must run these individual elements locally.

Overall steps for running our system:

- *Please note that both flask servers must be started first before trying out the client!*

1. Start both flask servers (one for PUBG stats, one for twitter sentiment) 
2. Start the client

Guide for starting Daniel Stewart's client/web portal:

* The client is successfully deployed at https://pubg-client.herokuapp.com/
* However, because we were not able to deploy the other pieces on Heroku, you must also run the client locally.
* To do so, you must install https://nodejs.org/en/
  * If you are on a Mac, I recommend installing with Homebrew:
    * https://www.dyclassroom.com/howto-mac/how-to-install-nodejs-and-npm-on-mac-using-homebrew
  * To verify the install, the following commands should both produce version numbers:
    * $ node -v
    * $ npm -v
* Once node has been installed, cd into the dastew02-client/ directory

- ls, and verify there is indeed a file titled 'package.json'

* run 'npm install' - which may take several minutes (installing all dependencies in package.json)
* run 'npm start' - this will launch the local development server at localhost:3000 (and should automatically open in the browser)

- Click 'Player Stats' and enter a players in-game name to make a GET request over to one of the Flask servers, and present their player data to the user
- Click 'Twitter Sentiment' which will make a GET request over to one of the Flask servers, and present the Twitter sentiment data provided as a line graph to the user
- If there are any problems running this part of the software locally, please shoot me an email at dastew02@syr.edu
