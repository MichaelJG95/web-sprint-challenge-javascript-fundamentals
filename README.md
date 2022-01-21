# Sprint Challenge - JavaScript Fundamentals

**Read these instructions carefully. Understand exactly what is expected _before_ starting this Sprint Challenge.**

This challenge allows you to practice the concepts and techniques learned over the past week and apply them in project. This Sprint explored JavaScript Fundamentals. During this Sprint, you studied array methods, this keyword, prototypes, and class syntax. In your challenge this week, you will demonstrate proficiency by completing a range of JavaScript problems.

This is an individual assessment. All work must be your own. Your challenge score is a measure of your ability to work independently using the material covered through this sprint. You need to demonstrate proficiency in the concepts and objectives introduced and practiced in preceding days.

You are not allowed to collaborate during the sprint challenge. 

## Introduction

The index.js file contains all of your challenges. Please review it in full before answering the questions. If you complete the stretch goals please leave them in your file but commented out so that they do not affect the MVP tasks 

In meeting the minimum viable product (MVP) specifications listed below, you should have all tests passing. You can console.log to check your work and ensure you are submitting the correct results 

### Commits

Set up codegrade early and commit your code regularly and meaningfully. 

## Interview Questions
### (please edit this file and write your answer below each question.)
Demonstrate your understanding of this week's concepts by answering the following free-form questions.

Edit this document to include your answers after each question. Make sure to leave a blank line above and below your answer so it is clear and easy to read.

1. Explain the differences between `.map`, `.reduce` and `.filter` and describe a use case for each. 
    
    - The .map method iterates through each index of an array and applies its conditions to the item at each index. It returns a new array. .map could be used to apply a change to the value at each index, such as changing each word in an array of words according to how it would appear in pig latin. Example.
            const words = ['Pig', 'laTin', 'is', 'Hard', 'to', 'speak']; // an array of words ready to be changed to pig latin

            // I'll use the .map method to apply the rules of pig latin to each word in the array 'words'. I'll save the returned array to the variable 'pigLatin'
            const pigLatin = words.map(word => {
                const vowels = 'aeiou'; // I'll need to know what vowels are so I can to check how each word starts
                word = word.toLowerCase(); // in case the words in the array are not all lowercase
                
                // A series of conditionals to check how the word starts and apply changes according to the rules of pig latin
                if(vowels.includes(word[0]) === false && vowels.includes(word[1])){
                    let start = word.slice(0, 1);
                    return word.slice(1) + start + 'ay';
                } else if(vowels.includes(word[0]) === false && vowels.includes(word[1]) === false){
                    let start = word.slice(0, 2);
                    return word.slice(2) + start + 'ay';
                } else {
                    return word + 'way';
                }
            });
 
            console.log(words); 
            console.log(pigLatin); // let's make sure it all worked
    

    - The .reduce method takes an array of values and reduces it returning a single value. A possible use for this would be in finding the sum of an array of numbers to use in calculating an average.

            const scores = [87, 76, 94, 100, 97, 79, 63, 52]; // an array of test scores, I need to find the average score.
            // I'll use the .reduce method to tally up all the scores.
            const sumScores = scores.reduce((acc, score) => acc + score, 0);
            // Now I just need to divide the sumScores by the number of scores in the scores array.
            const averageScores = sumScores / scores.length;

            console.log(averageScores);// I'll need to test with console.log to make sure it's working.

    - The .filter method iterates through an array passing the value at each index through its conditions. It returns a new array containing all passing values. It could be used to find all words in an array that start with a certain letter.

            const fruits = ['apple', 'banana', 'kiwi', 'apricot', 'cherry', 'avocado'];// an array of differnt fruits. I like fruits that start with the letter 'a'.

            const aFruits = fruits.filter(fruit => fruit[0] === 'a');// I use .filter to find all fruits in the fruits array that start with the letter 'a'.

            console.log(aFruits);// I'll console.log to make sure I didn't put a semi-colon in the wrong place.

2. Explain the difference between a callback and a higher order function.

    - A callback function is a function passed into another function as an argument, helpfully thought of as helper functions. A higher order function is a function that has other functions passed into it.

3. Explain what a closure is.
    
    - Closure is when a nested function reaches into the outer function to access a value declared in the outer function.

4. Describe the four principles of the 'this' keyword.

    -Window binding, by default 'this' will return the window or global object. In strict mode it will return undefined.

    -Implicit binding, when used in the context of an object's methods, 'this' refers to the object, that is when the method is invoked the thing to the left of the dot is what 'this' refers to.

    -Explicit binging, we can use 'call', 'apply', or 'bind' to explicitly say what 'this' refers to.

    -New binding, when the 'new' keyword is used with a constructor function, 'this' in the context of the constructor refers to the new object that is created.

5. Why do we need super() in an extended class?
    
    - super() tells what values to pass to the keys of the parent class.

You are expected to be able to answer questions in these areas. Your responses contribute to your Sprint Challenge grade. 

## Instructions

### Task 1: Set up Project

Using VSCode and Command Line:


1. Fork the repo
2. Go into canvas and connect your reop to codegrade
3. Clone your forked version of the repo
4. DO NOT CREATE A BRANCH. You will be pushing your changes to the main/master today
5. cd into your repo
6. open the terminal in your vs code and type `npm install`
7. next type `npm run test` in your terminal
8. Complete your work making regular commits to main/ master your codegrade score will update each time you make a push.


### Testing & Debugging

Open a second terminal inside of your project by clicking on the split terminal icon
![alt text](assets/split_terminal.png "Split Terminal")

Inside of your second terminal type `npm start` 
![alt text](assets/npm_start.png "type npm start")

You will be running your tests in one terminal and debugging in the other. As you work on your code you should make use of `console.log` to check your progress and debug.
![alt text](assets/tests_debug_terminal_final.png "your terminal should look like this")

### Task 2: Project Requirements (MVP)

You must complete all tasks inside of `index.js` and answer the questions above.

In your solutions, it is essential that you follow best practices and produce clean and professional results. Schedule time to review, refine, and assess your work and perform basic professional polishing including spell-checking and grammar-checking on your work. It is better to submit a challenge that meets MVP than one that attempts too much and does not.

## Resources
 
 [Sprint Challenge Study Guide](https://www.notion.so/bloomtech/Unit-1-Sprint-3-Study-Guide-033a9a00659a4ef98c12eb97e49a6110)

## Submission format

Please submit your project via codegrade by following [these instructions](https://notion.so.bloomtech.BloomTech-Git-Flow-Step-by-step-269f68ae3bf64eb689a8328715a179f9) See part 2, submitting an assignment with codegrade
