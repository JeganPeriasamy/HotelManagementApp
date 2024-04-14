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
