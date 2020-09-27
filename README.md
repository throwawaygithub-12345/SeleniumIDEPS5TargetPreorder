# SeleniumIDEPS5TargetPreorder
A quick and (very) dirty script file (.side) for Selenium IDE browser plugins to attempt to pre-order the PS5 console from Target


## Instructions
1. __Create an account and/or log into the account on Target's website.__
1. __Be sure your correct default payment details are entered and properly selected in the account section of the website.__

2. Download and install the Selenium IDE plugin for your favorite browser.

    __Chrome:__ https://chrome.google.com/webstore/detail/selenium-ide/mooikfkahbdckldjjndioackbalphokd?hl=en

    __Firefox:__ https://addons.mozilla.org/en-US/firefox/addon/selenium-ide/

1. Download the 'TargetPreorder.side' file from this repository and save it someplace on your computer.

1. Open the Selenium IDE plugin and import the saved 'TargetPreorder.side' project file.

1. You should see two unit tests in the left column named __'Pre-order PS5 console'__ and __'TEST: Pre-order PS5 controller'__
    
    1. You will possibly need to make modifications to the script to get it to work properly on your system based on hardware and connection speed differences.
    1. Running the __'TEST: Pre-order PS5 controller'__ will run the script against the PS5 controller pre-order page. You will want to test this prior to running the 'Pre-order PS5 console' test.
    1. __By default, the 'TEST: Pre-order PS5 controller' unit test WILL NOT complete the final action to submit the order.__ Line 26 is commented out by default. This is the line that tells Selenium IDE to click the final "Place Order" button which completes the transaction.
    1. There are several 'pause' commands throughout the script that are used for timing between actions and page loads. The pauses on lines 20, 24, and 26 will most likely need to be tweaked based on your connection speed.
    1. Run the 'TEST: Pre-order PS5 controller' unit test until you are able to have the browser properly navigate to the final "Place Order" screen.
    1. Once you have the correct pause values, copy those values to the exact same lines in the 'Pre-order PS5 console' unit test.

1. Run the 'Pre-order PS5 console' unit test and watch it attempt to go through the pre-order process.


## FAQ
### What is Selenium IDE?
Selenium IDE is an open source tool used to automate unit tests for web based pages and applications.

### Can't resellers just use this script too? Why are you making it public?
Yes. It's possible for resellers to use this script to automate a pre-order for a console that they would then resell for profit. However, I have to believe that they are in the minority and more people will want to pre-order a console to keep it for themselves. Releasing this script publicly levels the playing field between bot-driven resellers snapping up stock as it becomes available and the actual gamer who wants to pre-order for themselves.

# DISCLAIMER
__DO NOT USE THIS SCRIPT UNSUPERVISED!__ Using automated tools against third-party websites can produce denial of service situations. This script is provided __AS-IS__ and __no warranty__ is provided. This script is in no way affiliated with Target Corporation or the Selenium / Selenium IDE project. The author of this script takes no responsibility for missuse of this script or any unintended purchases/results that may occur during use of this script.
