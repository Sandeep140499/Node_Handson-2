# Node_Handson-2

// Loading Express in the app through require method

const express = require('express');

// creating app object using express 
const app = express();                      // Another Way : ->    const app = require('express')();

const port = 3040;

app.get('/',(req,res)=>{

    res.send(
        `<h1>Welcome to Server</h1>`
    )
})

app.get('/api/main',(req,res)=>{
    res.send(`
        <h1>What is Express ?</h1>
        <p>
            Express is a minimal and flexible node js web application Framework that provides a robust set of features to develop mobile and web application. It facilitates the rapid development of Node based Web applications . Following are some of the core features of Express js framework - 
            <ul>
                <li>It allows to set up middlewares to respond to HTTP request </li>
                <li>Defines a routing table which is used to perform different actions based on HTTP method and URL</li>
                <li>Allows to dynamically render HTML pages based on passing arguments to templates .</li>
            </ul>
        </p>
    `)
})

app.listen(port);
