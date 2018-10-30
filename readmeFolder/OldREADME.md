> This is a technical readme not a proper one. A proper one would be directed at project managers and the user. So 'code related' information is incorrectly used below 


### <a name="techspec"></a>Tech Specification :

|Technical Case Name|API Template|
|---|---|
|Summary Description| API CRUD functionality for User/Post/Comment |
|Preconditions| HTTP requests must be submitted with correct headers and key:value notation |
|Post conditions| The HTTP responses need to be parsed to benefit from them |
|Actors| • API <br> • Developer <br> • UI |
|Triggers|• Post request to register a user <br>• Get request to get all usernames <br>• Put request to update user data <br>• Delete request to delete user data <br>• Post request to make a post <br>• Get request to get all posts <br>• Update request to update a post <br>• Delete request to delete a post <br>• Post request to make a comment <br>• Get request to get all comments <br>• Update request to update comment <br>• Delete request to delete a comment|
|Post request to register a user|1- {username: username, email:email, password:password, confirmPassword:confirmPassword} <br> 2- Username has a regex restriction <br> 3- email has a regex restriction and email validation <br> 4- password has regex restrictions <br> 5- confirmPassword must match password|
|Get request to get all usernames|6- .find method to get all usernames|
|Put request to update user data|7- {username:username, password:password} <br> 8- To {email:email, password:password} <br> 9- Password can be updated by sending an email to the user *this is not a functionality I will be working on at the moment*|
|Delete request to delete user data|10- {email:email, password:password, confirmPassword:confirmPassword}|
|Post request to make a post|11- {description:description, image:image, location:location (optional)} timestamp is auto generated with this request|
|Get request to get all posts|12- .find method to get all posts |
|Update request to update a post|13- All three fields can be updated without the password being a part of the sent request|
|Delete request to delete a post|14- {description:description, image:image, location:location (optional), password:password, confirmPassword:confirmPassword}|
|Post request to make a comment|15- {text:text} timestamp is auto generated with this request|
|Get request to get all comments|16- .find method to get all comments related to each individual post|
|Update request to update comment|17- Text field can be updated. Not sure if I want the timestamp to be auto updated if a comment is edited |
|Delete request to delete a comment|18- Text and timestamp will be deleted |


### <a name="howto"></a>How to use :

From the command line  
`git clone <link>`  
`cd user_authentication`  
`npm install`  
if you do not have nodemon installed on your computer  `npm install nodemon --save`
`brew install mongodb`  
If you don't have brew you can install it from [here](https://brew.sh/)  
`sudo mkdir -p /data/db` then enter your password  
``sudo chown -R `id -un` /data/db`` to confirm everything is working
`nodemon` to start and automatically restart your server after you change and save a file  
`mongod` to run the database  
You should be able to see this line on your command line `waiting for connections on port 27017`
