# Spam Detector
###### *This was a university project, copying code not allowed*


## Developers:
* #### [Siddhant Das](https://github.com/Sid-26)
* #### [Sheida Ebrahimi Siaghi](https://github.com/Sheida-Ebrahimi) 
* #### [David Houle-Tymeczko](https://github.com/DavidHTwastaken)

## Project Overview
Our project uses naive Bayes spam filtering to find the probability that an email, given in a text file, is spam.
The training files are used to create a map that associates each word to the probability of a file being spam given that it contains the word.

![dashboard_screenshot.png](Screenshots/dashboard_screenshot.png)

## API
After training the model, we use to test on additional spam and ham files. Then we store the data in an object of the class TestFile. We calculate the precision and accuracy. Then send those data in a JSON file to the server by creating an HTTP GET request for the API.

The Rest API module is created using Jakarta RESTful Web Service. Then the server is ran through glassfish.

## The Interface
When the initial UI look was done, we tried to make it look more aesthetically pleasing by changing the colour palate and the default font to something easier on the eyes. Additionally, the “blue” and “purple” looking links were changed into a set colour, and an underline would appear whenever the user hovered them. Finally, we made the table scrollable with a fixed index so that the user would be able to see it after scrolling down, and the column sizes were adjusted based on their values’ size.

## Algorithm Improvements
To avoid errors from adding or subtracting infinity due to a word having a frequency of 0, we start counting at 1.
We have also added the second ham folder into the training phase to increase the sample size of words and files.

## How to Run
In order to clone and run our application, follow these steps:
1. Clone the project from GitHub into a local directory (e.g. a folder named “SpamDetection”)
2. Open the directory from Step 1 in Intellij IDEA and run the Maven build script
3. Set up Glassfish configuration by following the instructions of Intellij IDEA
    -  when prompted to select deployment artifacts, choose the option ending in “:war exploded”
4. Run the Glassfish server and wait for deployment
5. Open “index.html”

## Resources
main.css - https://github.com/h5bp/main.css
normalize.css - https://github.com/necolas/normalize.css
loader.css - https://cssloaders.github.io
HTML Boilerplate - https://html5boilerplate.com
Improvement Ideas - https://www.baeldung.com/cs/naive-bayes-classification-performance
