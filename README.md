# nutrify.me
A WebApp to track your daily calorie limit.

## Setup/Installations
*  Install [nodejs 12.18.2 LTS](https://nodejs.org/en/)
*  Install [MongoDB](https://www.mongodb.com/try/download/community)

## Runing the setup
* Install dependencies 
  * for server : ``npm install``
  * for client : ``cd client && npm install``
 * Run server (in main directory of project) ``npm start``
 
 ## API Endpoints
 ### Authentication API's
 * login
    URL : ``/users/login``  
    Method : POST  
    Sample Input:   
    ```javascript 
    const data = {
      email: this.state.email,
      password: this.state.password,
    };
    // axiosfunction to make API call
    axios
      .post(`users/login`, data)
      .then((res) => {
        console.log(res)
      })
      .catch((err) => {
        console.log(err);
      });
      ```  
    Sample Output :   
    * CODE: 200
      Content: 
      ```
      {
      "id": String,
      "token": String,
      "calorie": Number,
      "username": String
      }
      ```
