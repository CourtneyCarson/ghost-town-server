# Ghost Town Capstone 
This is an application to help curious travelers find abandoned ghost towns to visit in the old west. They can leave reviews on sites they have visited, and save sites to their account. 


## 1. Working Prototype 
You can access a working prototype of the React app here: https:// and Node app here: https://


## 2. User Stories 
This app is for two types of users: a visitor and a logged-in user


#### Landing Page
* as a visitor
* I want to understand what I can do with this app so I can decide if I want to use it


####  Log In Page
* as a returning registered user
* I want to enter my username and password
* so I can have access to my account, and use this app

####  Sign Up Page
* as a visitor
* I want to register to use this app  
* so I can create an account

####  Home Page
* as a visitor
* I want to be able to preview the content of the app
* to research abandoned places to visit

####  List Of Sites Page
* as a visitor
* I want to learn about all the available sites to visit per state
* so I can decide if I want to visit

#### Specific Sites Page
* as a visitor
* I want to learn about an abandoned site 
* so I can decide if I want to visit

#### Review Page
* as a logged in user
* I want to leave reviews on places I've visited
* so I can help others decide on places to visit

#### Account Page
* as a logged in user
* I want to see places I've saved to my account
* so I can easily find the places I'm interested in






## 3. Functionality 
The app's functionality includes:
* Every User has the ability to create an account
* A registered user has the ability to log in to their account
* A registered user has the ability to save ghost towns to their account
* A registered user has the ability to add reviews to ghost towns

## 4. Technology 
* Front-End: HTML5, CSS3, JavaScript ES6, React
* Back-End: Node.js, Express.js, Mocha, Chai, RESTful API Endpoints, Postgres
* Development Environment: Heroku, DBeaver

### 5. Wireframes (todo later)
Landing Page
:-------------------------:
![Landing Page](/github-images/wireframes/landing.png)

Sign Up Page
![Sign Up Page](/github-images/wireframes/sign-up.png)

Log In Page
![Log InPage](/github-images/wireframes/log-in.png)

Home Page
![Home Page](/github-images/wireframes/home.png)

About Page
![About Page](/github-images/wireframes/about.png)

How To Page
![How To Page](/github-images/wireframes/how-to.png)

Trigger Point Page
![Sign Up Page](/github-images/wireframes/trigger-point.png)

Past Treatments Page
![Past Treatments Page](/github-images/wireframes/past-treatments.png)

## 6. Front-end Structure - React Components Map (todo later)
* __Index.js__ (stateless)
    * __App.js__ (stateful)
        * __LandingPage.js__ (stateless) 
        * __Login.js__ (stateful) - user table (user name, full name, password)
        * __SignUp.js__ (stateful) - user table (user name, full name, password)
        * __Home.js__ (stateful) - trigger-point table (user_id, image,   title, content, date-created)
        * __About.js__ (stateless) 
        * __HowTo.js__ (stateless) 
        * __TriggerPoint.js__ (stateful) - trigger-points-user table (user_id, image, title, content, date-created)
        * __PastTreatments.js__ (stateful) - notes table (trigger_point_id, title, content, date-created)
        * __Navbar.js__ (stateful) - user table
        * __Noteform.js__ (stateful) - notes table (trigger_point_id, title, content, date-created)



## 7. Back-end Structure - Business Objects (todo later)
*  Users (database table)
    * id (auto-generated)
    * username (email validation)
    * full name (first & last name)
    * password (at least 8 chars, at least one alpha and a special character validation)

*  (Trigger Points) Results (database table)
    * id (auto-generated)
    * image (image)
    * title (note title)
    * content (note text)
    * date-created (auto generated)

*  trigger_points_user (database table)
    * id (auto-generated)
    * user_id (foreign key to match users (id))
    * trigger_points_id (foreign key to match trigger_points (id))

*  Notes (database table)
    * id (auto-generated)
    * trigger_point_id(foreign key to match trigger point table (id))
    * title (note title)
    * content (note text)
    * date-created (auto generated)

## 8. API Documentation (todo later)
/api
├── /auth    
│   └── POST
│       ├── /login
├── /users
│   └── GET /
│   └── GET /:id
├── /notes
│   └── GET
│       ├── /
│       ├── /:tp_id
│   └── POST
│       ├── /:tp_id
├── /tp
│   └── GET
│       ├── /user/trigger-points
│       ├── /:tp_id 
├── /tpusers
│   └── GET
│       ├── /
│       ├── /:tp_id
│   └── POST
│       ├── /

## Screenshots (todo later)
(Example) Landing Page
:-------------------------:
![Landing Page](/github-images/screenshots/landing.png)
Sign Up Page
![Register Page](/github-images/screenshots/sign-up.png)
Log In Page
![Log In Page](/github-images/screenshots/log-in.png)
Home Page
![Home Page](/github-images/screenshots/home.png)
About Page
![Register Page](/github-images/screenshots/about.png)
How To Page
![Register Page](/github-images/screenshots/how-to.png)
Trigger Point Page
![Register Page](/github-images/screenshots/trigger-point.png)
Past Treatments Page
![Register Page](/github-images/screenshots/past-treatments.png)




## Development Roadmap  (todo later)
This is v1.0 of the app, but future enhancements are expected to include:
* Ability to delete saved notes
* Ability to edit saved notes 

## How to run it 
Use command line to navigate into the project folder and run the following in terminal

### Local React scripts
* To install the react project ===> npm install
* To run react (on port 3000) ===> npm start
* To run tests ===> npm run test

### Local Node scripts
* To install the node project ===> npm install
* To migrate the database ===> npm run migrate -- 1
* To run Node server (on port 8000) ===> npm run dev
* To run tests ===> npm run test