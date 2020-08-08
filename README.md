# NodeExpressSetup


# How to setup a Node project?

1. Create a new directory which is preferarbly outside of the front-end directory (i.e. my-blog-backend)! And go to the backend folder

2. Initialize it as a npm package. 

    a. npm init -y
    
3. Install express into the project using:

    a. npm install --save express
    
4. Create a new folder in my-blog-backend folder called "src" and within it, create a file called server.js.

5. Consider that Node.js doesn't have native support for JS modern ES6 syntax hence we will install a few packages from babel (transpiler that allows us to write out code in ES6 syntax and still have it work on systems where ES6 isn't supported natively. 

    a. npm install --save-dev @babel/core @babel/node @babel/present-env

5. Create a file called .babelrc in my-blog-backend directory. This will tell how we want to transform the ES6 code that we write in common JS code that Node.js can execute

6. In .babel.rc insert the following:

    {
      "presets": ["@babel/preset-env]
    
    }

7. In server.js code write the below. 

    import express from "express"; 

    const app = express(); //app object.

    app.get("/hello", (req, res) => res.send("hello")); //within localhost:8000/hello, once the request is receive respond with hello (as a callback). 

    app.listen(8000, () => console.log("App is listening on port 8000")); //Two parameters 1. what port to listen in and 2. (callback) what to do once it's listening. 
    
    
