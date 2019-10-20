# Passport React JWT App

# Users who are logged into app can store images that are only viewable to them

**_This app is simple, but utilizes Github as an Oauth2 provider to register user to application_**
**_JWT Tokens are used to authorize users to image resources_**

# Do this 1st before anything else

1. npm install at the root of project
2. npm start
3. This will bring up app. Just confirm everything works using default environment variables for now.

# Personal App Setup

1. Register an OAuth Account with Github, (currently I am sharing my private environment variables but I will be removing soon)
   a) Login into your account and click your profile --> settings. Select 'Developer Settings'
   b) Select OAuth Apps
   c) Create new Oauth App
   You will be prompted for:

   - Application Name (not too important put anything)
   - Homepage URL (not too important put anything)
   - Application Description (not too important put anything)
   - Authorization Callback URL, For dev purposes set it to the following:
     - http://localhost:3001/auth
     - (note this is a route we defined in our app)

2. Go to .env, Github will give you a client ID and secret. Replace GITHUB_CLIENT_ID and GITHUB_CLIENT_SECRET.
   - note for dev purposes leave every thing else as-is
3. Run npm install at root of file to download react and nodejs dependencies
4. Run npm start to startup app.

# Production Special Configuration

1. Be sure to setup MongoDB lab with your heroku application
2. When deploying to heroku you'll need the following environment variables:

   https://passport-react-jwt-app.herokuapp.com is the name of my app url, feel free to replace that with your heroku url app.
   Be sure to not replace the endpoints like, /auth and /login

   a) CALLBACK_URL : https://passport-react-jwt-app.herokuapp.com/auth
   b) GITHUB_CLIENT_ID : 4186fef936e04d18b1bf
   c) GITHUB_CLIENT_SECRET : 6ffafe00788dc5b9b5b8b19e25a9d4099af286e9
   d) JWT_SECRET : your_jwt_secret
   e) REACT_APP_PROD_URL : https://passport-react-jwt-app.herokuapp.com
   f) REACT_APP_PROD_URL_LOGIN : https://passport-react-jwt-app.herokuapp.com/login
   g) MONGODB_URI : HEROKU_WILL_SET_FOR_YOU_JUST_CONFIRM_YOU_HAVE
