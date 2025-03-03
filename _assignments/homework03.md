---
type: assignment
date: 2024-05-15T4:00:00+4:30
title: 'Homework #3 - Connecting Figma to Web Prototyping'
hide_from_announcements: true
pdf:
attachment:
solutions:
# due_event: 
#     type: due
#     date: 2024-05-14T23:59:00+9:00
#     description: 'Assignment #2 due'
---

## Intro
In the last assignment, we built a Figma prototype of the [ChatGPT](https://chatgpt.com/?oai-dm=1) conversation page. For HW3, you will convert the Figma prototype you created in HW2 into HTML/CSS files, and implement interactive features of the chat using JavaScript based on the layout you built.  

**Note**: If you used AI-powered programming tools (e.g. ChatGPT, CoPilot) for the homework, please indicate so and describe for which part of the assignment you used those tools and how they improved your work. When submitting the homework, please include a text file named `studentid_note.txt` (e.g., 20210000_note.txt) for a detailed explanation and **.zip it with codes together**. The details of submission format are written below (section “How to submit?”) Note that we strongly encourage you to avoid relying solely on these tools, as they can hinder your understanding and practice of basic web programming concepts.

## Notes on web programming
Although we do not offer in-class web programming tutorials, we encourage you to take on the challenge of creating a basic, interactive web prototype by completing HW3 on top of HW2.

This homework is designed only in the scope of basic web programming with given templates, meaning that you will be writing code with detailed instructions. The goal of this assignment is not to implement a web prototype from scratch, but to understand how different components of web programming (HTML/CSS/JavaScript) function together in a single web prototype.

To help you get started, we have compiled a list of recommended tutorials and materials:

* From previous years' courses
  * [Tutorial #1 - HTML and CS](https://youtu.be/fimSP0ZU4O8) ([PDF](https://www.kixlab.org/courses/cs374-spring-2021/assets/tutorials/tutorial1.pdf) | [Code](https://www.kixlab.org/courses/cs374-spring-2021/assets/tutorials/tutorial1.pdf))
  * [Tutorial #2 - JavaScript](https://www.youtube.com/watch?v=SCpvAnAVF28&feature=youtu.be) ([PDF](https://www.kixlab.org/courses/cs374-spring-2021/assets/tutorials/tutorial2.pdf) | [JS Code](http://codepen.io/hgshin/pen/xqrgLg) | [jQuery Code](http://codepen.io/hgshin/pen/vxZgeR))
* (1 hour) [HTML Tutorial for Beginners: HTML Crash Course](https://www.youtube.com/watch?v=qz0aGYrrlhU)
* (1 hour) [CSS Full Course for free 🎨 (2023)](https://www.youtube.com/watch?v=wRNinF7YQqQ)
* (10 mins) [Learn jQuery in 10 Minutes | jQuery Tutorial](https://youtu.be/YprBzDEg7bc)

For those who do not have any prior experience in web programming, we have designed this assignment to serve as an entry point into the world of web programming. Do not be afraid to challenge yourself and explore this new field.

## Where to start from?
To begin with Step 1, we provide you with a [Sample Figma File](https://www.figma.com/design/WoIarRzpnReYB0YIFlgRz1/HW3-(template)?node-id=0%3A1&t=Tm8pXb3NUPw1QmZ7-1) that showcases the design of the prototype - this is the same design that was submitted as the answer for HW2. Feel free to make use of your own HW2 submission.

We provide you with the [starter kit](https://hci.kixlab.org/assets/hw3/starter_kit.zip). It includes
* `main.css`: a skeleton file for your user interface CSS code.
* `main.js`: a skeleton file for your user interface JS code.
* `main.html`: a skeleton file for your user interface HTML code.
* `images/`: a folder including all images needed for the assignment.

## How to submit?
* Compress your code into **(student_number)_hw3.zip**. Please do not create any subfolders except for the images folder.
* As written in the Intro section, if you used AI-powered programming tools, please include explanations as `studentid_note.txt` file and include it in the root directory.
* Then upload the zip file to [this link](https://www.dropbox.com/request/2ln50RwrIiXJKkXUeD48) until the due date stated above.

## How to test my code before submitting it?
* TAs will evaluate your code on the latest stable version of Chrome for OSX. We expect no browser compatibility issues in this assignment (we're not making a cutting-edge web application), but please test your code in your platform's Chrome before submission.
* If there is a browser issue between Chrome versions in different OS, TAs will follow the behavior in the student’s OS. However, please make sure that you are not using any custom stylesheet in your Chrome.

## Where to ask questions?
* If you have questions about this assignment, please post questions on Campuswire with the “Q&A - Assignment” category. TA will answer within a day. Your classmates could answer as well.
* If you believe your question should be kept private, please send an email to cs374kaist@googlegroups.com. After answering those questions, TA may share the question with other students.
* We are planning to hold **online office hours** for May 27th (Mon), 8-9pm.
  * During the office hour, we will answer questions around (1) the basics of HTML/CSS/JavaScript(JQuery) and (2) the homework.
  * Note that we cannot give you answers to the homework. Instead, we can provide some guidance around how to approach the homework.

## OK, what should I do?
Your task is to build an interactive web prototype for the conversation page in ChatGPT. You will import CSS from your Figma file, and modify parts of the HTML/CSS/JavaScript code to implement the send-and-receive chat feature of a “dumb” ChatGPT.
This assignment consists of four steps, which in total sum up to **170 points**. Please carefully read the instructions and follow them step-by-step.

## STEP 1: Complete the CSS of the Chat Page (70 pts)

When you first open up the `main.html` file on the browser, you will see the page that looks like the below image. Currently, there is a missing design on the right side, which is the chatting interface for communication between the user and ChatGPT.

![step1_1](/_images/hw3_imgs/step1_1.png)

In this step, using the Figma file that you made in HW2, you have to create and write a new CSS file named `chat.css`, which contains codes for the design of the chat interface (including the user’s chat, ChatGPT’s chat, and “regenerate response” button). Once you have successfully created this file, you will be able to make a complete interface as shown below.

![step1_2](/_images/hw3_imgs/step1_2.png)

### **Step 1-1: Create chat.css file and import into main.html (5pt)**
* Create a file with the title `chat.css`. This file must be in the same location as the `main.html` file.
* Import `chat.css` by adding the below tag inside the `<head>` tag in `main.html`
<link rel="stylesheet" href="chat.css" />

### **Step 1-2: Complete user-side conversation component (20pt)**
Let’s start writing  chat.css file now. Open up the Figma design file that you made in HW2 to refer to the CSS attributes of each component.

![step1-2](/_images/hw3_imgs/step1-2.png)

* (5pt) In the upper image, the part marked in red is the part that is generated each time the user enters their message. Find the **class name** that corresponds to this whole part in main.html, and at the same time, corresponds to the *user_conversation* component that you made in the Figma file. Make a new selector for this class in the chat.css file.

```
.(classname that you found) {}
```

* (5pt) Click on the *user_conversation* component in the Figma file, and open Inspect panel to check the generated CSS code. Read through the CSS attributes, and copy the attributes that you think should be included in chat.css. Paste them into your CSS file.

```
.(classname that you found) {
  (Paste the code here)
}
```

Now, let’s do the same for the text part of the user chat element.
* (5pt) In the upper image, the part marked in blue is the text part of the user chat. Find the **class name** that corresponds to this part in `main.html`. Make a new selector for this class in the `chat.css` file.
* (5pt) Click on the text element in *user_conversation* component in the Figma file, and open Inspect panel to check the generated CSS code. Read through the CSS attributes, and copy the attributes that you think should be included in `chat.css`. Paste them into your CSS file.

### **Step 1-3: Complete ChatGPT-side conversation component (30pt)**
Let’s complete the design for ChatGPT’s chats as well.

Just like what you have done in step 1-2, write CSS codes for the (1) entire chat component (red), (2) text (blue), and (3) icon group (green).

![step1-3](/_images/hw3_imgs/step1-3.png)

* (5pt) In the upper image, the part marked in red is the part that is generated each time the ChatGPT produces answers. Find the **class name** that corresponds to this whole part in `main.html`, and at the same time, corresponds to the *gpt_conversation* component that you made in the Figma file. Make a new selector for this class in the `chat.css` file.
* (5pt) Click on the *gpt_conversation* component in the Figma file, and open Inspect panel to check the generated CSS code. Read through the CSS attributes, and copy the attributes that you think should be included in `chat.css`. Paste them into your CSS file.
* (5pt) In the upper image, the part marked in blue is the text part of the ChatGPT’s answer. Find the **class name** that corresponds to this part in `main.html`. Make a new selector for this class in the `chat.css` file.
* (5pt) Click on the text element in *gpt_conversation* component in the Figma file, and open Inspect panel to check the generated CSS code. Read through the CSS attributes, and copy the attributes that you think should be included in `chat.css`. Paste them into your CSS file.
* (5pt) In the upper image, the part marked in green is the group of icons for pasting and rating the answers. Find the **class name** that corresponds to this **group (not a single icon)** in `main.html`. Make a new selector for this class in the `chat.css` file.
* (5pt) Click on the icon group in *gpt_conversation* component in the Figma file, and open Inspect panel to check the generated CSS code. Read through the CSS attributes, and copy the attributes that you think should be included in `chat.css`. Paste them into your CSS file.

### **Step 1-4: Complete “Regenerate response” button (15pt)**
Lastly, let's put the design in the “Regenerate response” button at the bottom of the screen. You can find out the code like this in main.html, which corresponds to this button.

```
<div class="regenerate-button">
  <img class="regenerate-button-icon" src="images/regenerate.svg" alt="regenerate" />
  <div class="regenerate-button-text">Regenerate response</div>
</div>
```

* (5pt) Go to the Figma design file, and look for the design element that corresponds to the `div` with “regenerate-button” class. Open Inspect panel to check the generated CSS code. Read through the CSS attributes, and copy the attributes that you think should be included in `chat.css`. Paste them into your CSS file.
* (5pt) Go to the Figma design file, and look for the design element that corresponds to the `div` with “regenerate-button-icon” class. Open Inspect panel to check the generated CSS code. Read through the CSS attributes, and copy the attributes that you think should be included in `chat.css`. Paste them into your CSS file.
* (5pt) Go to the Figma design file, and look for the design element that corresponds to the `div` with “regenerate-button-text” class. Open Inspect panel to check the generated CSS code. Read through the CSS attributes, and copy the attributes that you think should be included in `chat.css`. Paste them into your CSS file.

## STEP 2: Implement the Send Chat Feature (70 pts)

![step2](/_images/hw3_imgs/step2.gif)

Now you will have a styled ChatGPT chat page with HTML and CSS file. In this step, we will add the send chat feature step by step, by modifying the HTML, CSS, and JavaScript file.

### **Step 2-1: Import main.js file into main.html (5pt)**
Import `main.js` by adding the ~~`<link>` tag~~`<script>` tag inside the `<head>` tag in `main.html`

### **Step 2-2: Update HTML and CSS (35pt)**
Here, you will modify the HTML+CSS file to change non-interactive components into the appropriate HTML tag.
* (15pt) Input box for entering user chat
  * (5pt) Change the HTML tag of the chat input box into an `input`
  * (5pt) Increase the width of chat input box to 100% to make the input box fill the entire space
  * (5pt) Remove the border of the chat input box
* (5pt) Button for sending the chat
  * Change the HTML tag of the “send” icon button into a `button`

Before implementing JS codes, you need to add the id to some elements in HTML code so that you can select the exact element for each function.
* (5pt) Input box: should have an id of "hw2__input". (**Note that there are two underscores.**)
* (5pt) “Send” icon button: should have an id of "hw2__send".
* (5pt) Chat history list (div that contains all conversation components) : should have an id of "hw2__chat-history".

### **Step 2-3: Implement the behavior of the “send” icon button (30pt)**
Now let's implement the interaction so that when the user types in their input and presses the send button, user's input is added above.

You can use [JQuery](https://jquery.com/) to implement these functions. (JQuery is already imported.) Refer to the tutorial videos in the previous section if you need a quick tutorial to JQuery.

* (10pt) Implement a click event handler so that when the “send” icon button is clicked, the input text box should be cleared and get focus again.
* (10pt) Add more functions in a click event handler so that when the “send” icon is clicked, the user’s own input text is added to the chat history list in the same format as the chat history that already exists.
* You need to write a code to add an entire `div` with the class `class="user-conversation"`.
* (10pt) Implement a keypress handler so that when the user press Enter (keyboard) in the input box, it behaves same as when the user clicks the “send” icon button.

## STEP 3: Provide Response to User’s Input (30 pts)

![step3](/_images/hw3_imgs/step3.gif)

In the previous step, you have successfully implemented the send chat feature. Now, let’s add ChatGPT’s dummy response, and make it look natural.

### **Step 3-1: Provide a dummy response to the user’s input (10pt)**
Unfortunately, the ChatGPT we are implementing is not-yet-advanced, meaning that it does not have the ability to interpret user’s input and provide an appropriate response. The prototype will only output responses taken from a predefined list of responses.

* (5pt) Select a random response from the `responses` list on the top of the `main.js` file.
* (5pt) Every time when the user input is added to the chat history, the randomly selected response should be added to the chat history as well.

### **Step 3-2: Make the response look natural by adding delay and autoscroll (20pt)**
* (10pt) Add a 3-second delay to the ChatGPT’s response
* (10pt) Automatically scroll down to the bottom whenever a new response is added.