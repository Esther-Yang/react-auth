# React Auth
Use Firebase Auth REST API to implement authentication in React App.

# Feature
* Starting page is with a form to input email and password to sign in or create account.
* After signing in, **profile** and **logout** button is visible. 
* In **profile**, the user can change password.
* Auto logout after 1 hour, the time is a default value in [Firebase Auth REST API -  `expiresIn`](https://firebase.google.com/docs/reference/rest/auth#section-sign-in-email-password).
* User authentication persistence - the user stay sign in even after reloading page.

# Notes
## Authentication tokens
* Typically created in [JSON Web Token (JWT)](https://jwt.io/) Format.
* Tokens are long strings constructed by algorithm, with a private key wchih only known by the server.

## Firebase Auth REST API
* Read the [documentation](https://firebase.google.com/docs/reference/rest/auth) to know about the **method**, **content-type**, **endpoint**, **request body payload**, and **response payload**.
* Operation used in this repo:
    * Sign up with email/ password
    * Sign in with email/ password
    * Change password

## Firebase Console Authentication Setup
* In [Firebase Console](https://console.firebase.google.com/) > Choose Firebase Project > Authentication > Sign-in method > **Enable Email/Password**.

## Firebase Web API key
* In [Firebase Console](https://console.firebase.google.com/) > Choose Firebase Project > Project Overview > Project Settings > General > **Web API key**.

## Implementation
* Managing authentication with `context`.
* Redirect user after signing in with `useHistory`.
* Persisting user authentication status with  `localStorage`.
* Auto logout with `setTimeout()`.
* Clear timer when user log out manually with `clearTimeout()`.
* Stay sign in even after reloading by checking `localStorage`.

