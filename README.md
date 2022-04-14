# security-showcase
The project is a basic showcase about Node.js security and authentication. Multiple concepts like social sign on, with Googles open authentication and security best practices are implemented in this sample. The application includes topics like encrypted connections and digital certificates (https), authentication (Oauth 2.0), securing headers (helmet), client secrets (dotenv), secure middleware, secure endpoints, ... The project is not about implementing an own authentication using Cookies and Tokens with libraries like Bcrypt and Passport. That is an "ok", but not a real world approach. It is not adiviseable to implement security from scratch, as there are well proven approaches out, like the Oauth 2.0 approach. For secure application it is always considerable, to use an available sign on service in order to keep the application safe. 

## Project execution
- Download the project
- NPM install all required dependencies
    - npm install 
- Registering with the Google Authorization Server
    - https://console.cloud.google.com/apis/credentials
    - generate OAuth 2.0 Client IDs
    - add a .env file in the root folder of the project that  includes the generated values instead of xxxxxxx:
    `
        CLIENT_ID=xxxxxxx
        CLIENT_SECRET=xxxxxxx
        COOKIE_KEY_1=abc
        COOKIE_KEY_2=abc
    `
- Start application from terminal
    - npm start
- Open Chrome browser on https://localhost:3000/
    - https://support.google.com/chrome/answer/99020?hl=en
    - Another trick if the open unsafe link is not displayed: click anywhere on the Browser screen and enter "thisisunsafe"
- Login with your Google id and verify the secret 
    (click the links provided in the displayed webpage with the following order)
    - Show me! -> {"error":"You must log in!"}
    - Google login -> you are logged in via Google, Goggle data gathered are displayed inside the terminal
    - Show me! -> Your personal secret value is 42!
    - Sign out

*This showcase application is running on https://localhost:3000/*