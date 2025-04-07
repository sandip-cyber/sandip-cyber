## ReactJS Notes
Q.What is Multi-page-application?
-It is an application where it will be having multiple pages, or multiple HTML files.
- If we try to navigate from one page to another page everytime it is going to refresh or each time Dom structure will be created.
-so this makes application slower.
-we can create multi-page-application using only HTML,CSS and JAVASCRIPT.

Q.what is Single-page Application?
-It is an application where it will be having single page,or single HTML file.
-If we try to navigate from one page to aonther page it will not gonna referesh,becouse we will be staying in a the same HTML file, but we are moving from applications faster.
-To create a single-page application(SPA) we need some advance concept like angular,jQuery or React.JS etc..

## ReactJS:
-IT is a javascript library (collection of pre-defined codes.)
-It is used to build user interfaces.

## Features of ReactJS:-
1.Single-page-application(SPA)
-e.g:- Whatsapp,facebook,Gmail,etc...

2.virtual DOM
-It is a blueprint of real-DOM.
- wherever we run react application for the 1st time DOM sstucture is going to get created ,parallely a copy of real-DOM id also going to get genereted. This is called as virtual-DOM.

3.Component based Architecture(CBA):-
-React follows CBA ,beacouse we can reuse the components, better code mantainabillity.
-web pages will be divided into small parts and that small parts are called components.

## Folder Structure of reactjs:-
After successfully installation of react.js, we will be getting some default folders and files

1. node_modules:-
-It is a folder where all the pre -definded codes and dependencies of react.js will be present.

-
2.Public:-
-this folder conations the main  structure of the webpage.
-the only important file we have to maintain is "index.html".

3.src:-
-It is a source folder where we are going to write our codes.
-The 2 important files we have to maintain is "index.js" and "App.js".
    -index.js: It is considered as a root file of react.js
    -App.js: It is considered as parent component of react.js

4. package.json & packge-lock.json:
-These are the two files where it is considered as directories of the  react folder.
- It will give all the information about libraries present in the project.

## Rules while creating a component:-
1.First letter should be capital.
2.It should be written in Pascalcase.
3.File extension of component is ".js" or ".jsx".
e.g : App.jsx, App.js, content.jsx

#What is JSx?
-it is a combitation of javscript and XML (Extensible Markup Language).

##Difference between HTML and XML?
1. - In HTML  we will be using an attribute as "class"
    - In XML we will be using an attribute as " className".
2. All the events in HTML we use  are in lowercase.
    e.g: onclick, onmouseover
3. In HTML we can write two or more diffrent tags/elements

e.g: <h1>This is heading 1<h1>
    <h1>This is heading 2<h1>

-In XMl we have to Wrap all the elements into one parent container.
e.g : <div>
        <h1>This is heading 1<h1>
        <h1>This is heading 2<h1>
     </div>   

# React project Setup
##Using CRA(create-react-app)
-npx create-react-app <project-name>
-cd <project-name>
-npm start or npm run start

##Using Vite 
- npm createvite@latest <project-name>
-cd <project-name>
-npm install
-npm run dev

-After installation of react-project, we will be getting some default folders and files.

now we have to maintain two important files in "srs" folder- idex.js(main.jsx) and App.jsx

1. index.js(main.jsx):
-It is considered as a root file of react.js project.
-we are using this file to create root between index.html and App.jsx.

2. App.jsx:
-It is  considered as a parent component  of react.js  project.
-It is a component where we are going to write our codes.

e.g: 
index.js(main.jsx):
import{createRoot} from "react-dom/client";
import App from "./App";
import {StrictMode} from "react";

const root = createRoot(document.getElementById("root"));
root.render(
    <StrictMode>
    <App />
    </StrictMode>
);

App.jsx:

import React from "react";
const App =() =>{
    return(
        <div>
        <h1>App component</h1>
        </div>
    );
};


export defult App;

-After installation setup we have to create a new folder name "Components" inside "src" folder.
-After createing "Components" folder, "App" componet will be called as parent component.
- whatever component we create inside " Components" folder will be called as child component.

e.g :
 Navbar.jsx,Footer.jsx.Content.jsx

 Navbar.jsx:

 import React from "react";

const Navbar = () => {
  return (
    <nav>
      <h1>Navbar</h1>
      <ul>
        <li>Home</li>
        <li>About</li>
        <li>Contact</li>
      </ul>
    </nav>
  );
}

export default Navbar;

**Footer.jsx:

import React from "react";

const Footer = () => {
  return (
    <div>
      <p>footer</p>
    </div>
  );
}

export default Footer;

#Contents.jsx:

import React from "react";

const Contents = () => {
  return (
    <div>
      <h1>Contents</h1>
      
    </div>
  );
};

export default Contents;

**App.jsx:-

import React from "react";
import Navbar from "./Components/Navbar";
import Footer from "./Components/footer";
import Contents from "./Components/contents";
import ClassComponent from "./Components/ClassComponent";

const App = () => {
  return (
    <div>
      <Navbar />
      <h1>Hello World</h1>
      
      <p>This is my first React project!</p>
      <Footer />
      <ClassComponent />
    </div>
  );
};

export default App;

#React  Project  Setup

##Type of Compoments:
-There are 2 types of components in react:
1.class based Component
2.Fuctional Component or Function  based Component.

#Diffrence between class component and functional component
--class component :-
- use class keyword and class name 
-Statefull
-It has no Hooks
-It has lifecycle methods
-It use render() method

-Syntax:-

import react from 'react";
import {Component } from "react";
class classComponet extends Componet{
  render(){
    retun(
      <h1>class Component</h1>
      </div>
    );
  }}

  export defsult class Component;

  ##Functional Component:-
  -use function keyword and function name
  -Stateless
  -It has Hooks
  -It dosen't have lifecycle methods
  -It doesn't use render() method 

  -syntax:


##props
- props are inbuilt o bject in react.
-Props are used to pass data fromparent to child componet.
-props are immutable, it menas once the value is passed from 
-props are uni-directional.

e.g :-

-Write a program to send a string data as props.
App.jsx:
import react from 'react';

import Counter from './Components/Counter';
import './App.css';

const App = () => {
  return (
    <div>
      <h1>Counter App</h1>
      <Counter />
    </div>
  );
}
export default App;

Counter.jsx:
import React from "react";

const Counter = () => {
    const [count, setCount] = React.useState(0);
  
    const increment = () => {
        setCount(count + 1);
    };
    const decrement = () => {
        setCount(count - 1);
    };
    const reset= () => {
        setCount(0); 
    };

         
        return(
    <div>
      <h1>Counter: {count}</h1>
      <button onClick={increment}>Increment</button>
      <button onClick={decrement}>Decrement</button>
      <button onClick={()=> setCount(count + 1)}>Increment By</button>
        <button onClick={reset}>Reset</button>
    </div>
  );
};

export default Counter;

##Hooks:
-hooks are 
## Introduction
ReactJS is a JavaScript library for building user interfaces. It is maintained by Facebook and a community of developers.

<!--**Key Features** -->
- **Component-Based**: Build encapsulated components that manage their own state.
- **Declarative**: Design simple views for each state in your application.
- **Virtual DOM**: Efficiently updates and renders components.

## Installation
bash
npx create-react-app <projectName>
cd my-app
npm start
