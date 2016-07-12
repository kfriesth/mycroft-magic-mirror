# Note i am splitting this project into 3
1. Mycroft-Electro
2. Mycroft-Electro-Kiosk (Name tbc)
3. Mycroft-Electro-Plugins

##Mycroft Electro
This will be a desktop UI/Client for mycroft (based on what is currently the "Desktop Mode" of this project). This will (eventually) have things such as new windows popping up for things such as weather info and wikipedia pages and other more desktop focused features

##Mycroft-Electro-Koisk (Name tbc)
Based on Mycroft-Electro (so i will probably make it a fork or something (not too sure yet as my git-fu is not that strong)) and will have mostly the same code with a focus on touch friendlyness and will have a "mirror" mode to make it all black and white for magic mirror setups. the Idea is that this will be used for magic mirror setups and tablet setups (e.g. if you had a wall mounted ouch screen in your house with mycroft installed. or in a car??)

##Mycroft-Electro-Plugins
As the above two project will use the same type of react based plugins i will move all the currently written plugins to a new repo which can then be a submodule for each.

------------------------------------------------------------------------
Also im definetly open to suggestions on the new layout/structure :)
------------------------------------------------------------------------

# A Mycroft UI for Desktop and Magic Mirrors
A UI for Mycroft designed for a magic mirror also with a desktop mode

modular using reactjs and can handle plugins

*note* before starting edit config.json with your path to this clone and your mycroft-core folder

to run npm install && npm start

1. Have a working install of mycroft (https://github.com/MycroftAI/mycroft-core)
2. Have a working install of nodejs/npm (https://nodejs.org)
3. Clone this repo
```$ git clone https://github.com/joshymcd/mycroft-magic-mirror.git```

4. edit config.json in mycroft-magic-mirror folder with two paths to mycroft-core and this mycroft-magic-mirror (i will streamline this part);
  *NOTE* See below under 'config' section
5. in terminal
    ```$ cd mycroft-magic-mirror```
    ```$ npm install```

## Start-up scripts
There are a couple of ways to start up the UI

### Mode
1. Desktop Mode - shows a desktop friendly UI in a borderless window which can be resized and dragged around
2. Mirror Mode - A fullscreen black and white UI designed for use in magic mirror like projects

### Startup type
1. Manual - you manually have to select to start each Mycroft service and then connect (*hint* click on the 'Mycroft Inside' text to show the admin menu)
2. Auto - Automagically starts up Mycroft and connects
*Note:* Not yet implemented!

### Start Commands
####Basic
1. ``` npm start ```
This runs the UI in Desktop & Manual Mode
2. ``` npm run start-desktop ```
This runs the UI in Desktop & Manual Mode
3. ``` npm run start-mirror ```
This runs the UI in Mirror & Auto Mode

####Other Startup Modes
1. ```npm run start-desktop-auto```
2. ```npm run start-desktop-manual```
3. ```npm run start-mirror-auto```
4. ```npm run start-mirror-manual```

## Configurations
Configurations are held in a .json file under source/baseconfig.json. this contains the default settings.

Any properties placed in source/config.json will override baseconfig.json. this file is ignored by git so should persist between pulls.
