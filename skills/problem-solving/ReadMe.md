# Problem Solving

## Why is this an important developer skill?

In many respects, this is what a developer is. It's also what distinguishes a software engineer from a robot that can write code - a robot can only operate given instructions, whereas a software engineer can actively engage with and solve problems.

More pertinently, this is a key graduate skill because, as you leave the learning environment of Makers and start to progress through your career, you'll get less and less help solving your own problems and more and more you'll become the person expected to solve problems for other people. If you're still job-hunting, you may still have some access to coach time, but it's likely to be infrequent and less focussed. Being blocked for hours because your debugging skills aren't up to scratch is going to massively impact on your learning time.

## Recording your problem solving process

### 1) What am I trying to do?

What is the definition of success? If you can't describe this in one or two sentences, it may be that you're trying to do something too big. If you can't describe this at all, it may be that you haven't fully understood what you are tryint to do (or why) - this is not uncommon if you've been following a tutorial.

Be as specific as possible, e.g:

`I want to check that the user's password is correct`

Is ok, but better would be:

`I want to check that the password that the user enters posts to the server through the login form matches the one that is stored for that user in the database`

The second one gives a clearer picture of the different components of the system and their respective roles.

### 2) What do I need to know? What do I know and what do I not know?

With any development task there is some prerequisite knowledge or skill that is required to perform the task. You might need to know basic javascript syntax, you might need to understand how APIs deal with HTTP requests, you might need to know what a bearer token is.

Again, try and be as specific as possible, but if you are unable to be specific record things anyway. If you don't know what you need to know, then this sounds like something to address!

### 3) What is the problem?

You should already have describe what you want to achieve; what is blocking you from achieving it?

e.g. I have read the documentation but I still can't find any information on how to set headers in the response.

### 4) What have I done to solve the problem?

Be as detailed as possible. In each case, record:
- The type of thing you did.
- The specific thing you did
- The result of the thing you did
- Did this get you closer to solving the problem?

Ideally, before you try and solve the problem, you should already have record parts 1-3, and you can write down each step you take to solve it as you go. An example might be:

- GET VISIBILITY: Used 'p' to check the value of the password coming in from the form. The password was what I expected it to be. This validated my assumption that I was passing the password in correctly from the login form. This has helped me solve the problem by tightening the loop.

- GET VISIBILITY: Used 'p' to check the return value of BCrypt.new. It was expecting true and it was false. This suggests that BCrypt.new is not behaving as I thought it was. This has helped me solve the problem by tightening the loop.

- ISOLATE: I created a test with Bcrypt with known test values to check whether it behaves in the way that I expected. The test did not behave in the way that I expected - it did not match the password. This helped me solve the problem by confirming my theory.

- GAIN UNDERSTANDING: Searched Google for 'Bcrypt Documentation', then 'Bcrypt Ruby Documentation'. Found https://github.com/codahale/bcrypt-ruby and read through examples. I noticed that in the examples the parameters being passed into the method were different - they were passing in the encrypted password value from the database. I altered my code based on this and the test passed. Problem solved.  
