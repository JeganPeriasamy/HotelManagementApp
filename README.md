# Hotel Management App

### Backend

Tech Stack

- Express Js
- MongoDB with mongoose
- PassportJs middleware for authentication (JWT Bearer token)
- Websocket (SocketIO) for realtime communication of orders

### FrontEnd

- ReactJs
- SocketIO

## Requirement

Create a hotel management app with a login page and signup.

### Signup and login

1. By default there should be a admin user (userName: admin, password: \*)
2. The signup should get the users
   - userName (unique)
   - role (waiter,manager,chef)
   - password
3. The User should be able to login with
   - username (unique)
   - password

### Waiter

1. The left pane should have

   - Dishes
   - New Order
   - Previous Order

- The dishes page should list all the dishes the hotel currently has
- Once the waiter clicks **new order**, the waiter should
  1. Select the **table Number** / **Parcel**
  2. Select the dishes from the list with quantity and price
  3. Once the place order is clicked, the order is placed and the order is moved to the chef.
  4. Each order should have a unique number.
  5. He can also add to the existing order
  6. Once the waiter clicks **proceed to billing** and the billing is forwarded to the manager.

### Manager

1. The manager should be able to add new dishes to the list
2. The manager should be able to close the billing by marking the order as **paid**

### Chef

1. Once the order is received to the chef, he should update the status of the order
   - preparing
   - ready


PASSPORT.JS 

Passport.js is a middleware used in Node.js applications for handling authentication. It provides a way to authenticate users using different strategies, such as username/password, social logins (like Facebook or Google), or in this case, JWT (JSON Web Token) bearer tokens.

JWT bearer tokens are a type of token that you can use to authenticate requests. When a user logs in, the server creates a JWT token and sends it back to the client. The client then includes this token in the headers of future requests. The server can verify the token to make sure the request is coming from a logged-in user and respond accordingly.

So, in simple terms, Passport.js with JWT bearer tokens helps secure your application by verifying that the requests are coming from authenticated users.




WEBSOCKET 

WebSocket is a technology that allows for real-time, two-way communication between a client (like a web browser) and a server. 
It's like having a phone call where both parties can talk and listen at the same time, compared to traditional HTTP requests where the client asks for information and the server responds.

Socket.IO is a library for Node.js that makes working with WebSocket easier. It provides a way for the server and client to establish a WebSocket connection and exchange messages in real-time.

In the context of a hotel management app, using WebSocket (Socket.IO) allows the server to instantly send updates about orders to the clients (like kitchen staff or waiters) as they are placed. This means that everyone involved can stay updated in real-time without needing to refresh the page or make repeated requests to the server.
