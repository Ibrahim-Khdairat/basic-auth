# Lab 06 : Basic-Auth
##### Author : Ibrahim Khdairat 

* [GitHub Repo Link](https://github.com/Ibrahim-Khdairat/basic-auth)

* [Pull Request](https://github.com/Ibrahim-Khdairat/basic-auth/pull/1)

* [Heroku Link](https://ibrahim-basic-auth.herokuapp.com/) : https://ibrahim-basic-auth.herokuapp.com/



##### Setup
`.env` requirements
  * `PORT` - Port Number
  * `POSTGRES_URI` : POSTGRES_URI

**Running the app**
* `npm start`
* Endpoints:
* ##### 1 -  `/status`
https://ibrahim-basic-auth.herokuapp.com/status
Returns Object

>{
  "domain": "ibrahim-basic-auth.herokuapp.com",
  "status": "running",
  "port": 3000
}

* ##### 2 -  `/signin`
`using get method`
https://ibrahim-basic-auth.herokuapp.com/signin

***If the user is existed***
Returns Object
> {
    "id": 1,
    "userName": "hema",
    "userPassword": "$2b$10$aWoXfbGQ73kW78P/HHrZ9.rIlc/VqpZ9.3KP6WdG013EACmWFI6ta",
    "createdAt": "2021-08-22T18:19:02.413Z",
    "updatedAt": "2021-08-22T18:19:02.413Z"
}

***If the user not existed or the password is wrong existed***

Returns
> "Invalid User"



* ##### 3 -  `/signup`
`using post method`
https://ibrahim-basic-auth.herokuapp.com/signup

***If the user not existed***
Returns Object
> {
    "id": 4,
    "userName": "Isra'a Othman",
    "userPassword": "$2b$10$3q24YyaNF3DA/JA4Jp2Hb.OOHV7AbcTkQkZ0TiX0caqXZhn.Wt65y",
    "updatedAt": "2021-08-22T19:27:24.870Z",
    "createdAt": "2021-08-22T19:27:24.870Z"
}

***If the user is existed***

Returns
> "Error In Creating User"