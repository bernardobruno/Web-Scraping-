# Web-Scraping

First usage of Web Scraping - a study case.

In this repository we will learn about the basics of Web Scraping. 

Beautiful Soup is a widely used Python package which help to parse HTML and XML documents (including having malformed markup, i.e. non-closed tags, so named after tag soup).

It creates a parse tree for parsed pages that can be used to extract data from HTML, which is useful for web scraping.

Below are some basic questions on Web Scraping and general subjects. 

# 1. Brieﬂy describe the differences between the webbrowser, requests, BeautifulSoup, and selenium modules.

Answer: 
Browser: if we have a browser we don't need BeautifulSoup. 
The webbrowser has an open() method that will launch a web browser to a speciﬁc URL. 
The requests module can download ﬁles and pages from the Web. The BeautifulSoup module parses HTML. 
The selenium module can launch and control a browser. 

# 1.A - How web scraping is related / not-related to Data Mining and API?

Web scraping refers to the process of extracting data from web sources and structuring it into a more convenient format. It does not involve any data processing or analysis.
Data mining refers to the process of analyzing large datasets to uncover trends and valuable insights. It does not involve any data gathering or extraction.
Data mining does not involve data extraction. In fact, web scraping could be used in order to create the datasets to be used in Data Mining.
API is another data scraping method, however, it works quite differently. An API – application programming interface – is an intermediary that allows one software to talk to another software. In more simple terms, an API allows the user to open up data and functionality to other developers and businesses.


# 2. What type of object is returned by requests.get()? How can you access the downloaded content as a string value?

Answer:  The requests.get() returns a Response object, which has a text attribute that contains the downloaded content as a string. 

# 3. What Requests method checks that the download worked?

Answer:  The raise_for_status() raises an exception if the download had problems and does nothing if the download succeeded. 

# 4. How can you get the HTTP status code of a Requests response?

Answer:  The status_code attribute of the Response object contains the HTTP  status code. 

# 5. How do you save a Requests response to a ﬁle?

Answer:  After opening the new ﬁle on your computer in 'wb' “write binary” mode, use a for loop that iterates over the Response object’s iter_content() method to write out chunks to the ﬁle. Here’s an example:
saveFile = open('filename.html', 'wb') for chunk in res.iter_content(100000):    saveFile.write(chunk)

# 6. What is the keyboard shortcut for opening a browser’s developer tools?

Answer:  F12 brings up the developer tools in Chrome. Pressing CTRL-SHIFT-C (on Windows and Linux) or z-OPTION-C (on OS X) brings up the developer tools in Firefox. 

# 7. How can you view (in the developer tools) the HTML of a speciﬁc element on a web page?

Answer:  Right-click the element in the page, and select Inspect Element from the menu. 

# 8. What is the CSS selector string that would ﬁnd the element with an id attribute of main?

Answer: '#main' 

# 9. What is the CSS selector string that would ﬁnd the elements with a CSS class of highlight?

Answer:  '.highlight' 

# 10. What is the CSS selector string that would ﬁnd all the <div> elements inside another <div> element?

Answer:  'div div' 

# 11. What is the CSS selector string that would ﬁnd the <button> element with a value attribute set to favorite?

Answer:  'button[value="favorite"]' 

# 12. Say you have a Beautiful Soup Tag object stored in the variable spam for the element <div>Hello world!</div>. How could you get a string 'Hello world!' from the Tag object?

Answer:  spam.getText() 

# 13. How would you store all the attributes of a Beautiful Soup Tag object in a variable named linkElem?

Answer:  linkElem.attrs 

# 14. Running import selenium doesn’t work. How do you properly import the selenium module?

Answer: The selenium module is imported with from selenium 
import webdriver. 

# 15. What’s the difference between the find_element_* and find_elements_* methods?

Answer: The find_element_* methods return the ﬁrst matching element as a WebElement object. The find_elements_* methods return a list of all  matching elements as WebElement objects. 

# 16. What methods do Selenium’s WebElement objects have for simulating mouse clicks and keyboard keys?

Answer: The click() and send_keys() methods simulate mouse clicks and keyboard keys, respectively. 

# 17. You could call send_keys(Keys.ENTER) on the Submit button’s WebElement object, but what is an easier way to submit a form with Selenium?

Answer: Calling the submit() method on any element within a form submits the form. 

# 18. How can you simulate clicking a browser’s Forward, Back, and Refresh buttons with Selenium?

Answer: The forward(), back(), and refresh() WebDriver object methods simulate these browser buttons.
