# Beecology Web Services


### Introduction
Beecology Web Services is a method of communication between client end and server end over the web. Client end(Android, iOS, browser end/applications) can operate the Web servcies API to process the database distributed on server indirectly.
  - Keep the central database from remote access or attacks.
  - Likes a basic network standard/protocol based on HTTP methods and JSON, client-side could use the languages and tools they want.
  - Allows flexible business processes that can change process flow based on the specific case.
  - Allows customized version that different clients could use different APIs independently without mutual interference.


### Technology

Beecology Web Services uses following technologies or open-source frameworks to work properly:

* [PHP](http://php.net/) - a server scripting language for writing web pages.
    * *current version: 7.0.22*
* [Slim3](https://www.slimframework.com/) - a PHP micro framework for building web applications and API.
* [Swagger-UI](https://swagger.io/swagger-ui/) - a framework for writing APIs documentation.
* [RESTful mode](http://phppot.com/php/php-restful-web-service/) - an architectural style that specifies constraints on APIs.

The source of Beecology Web Service distributed on [GitLab](http://).
[API Documentation](http://beecology.wpi.edu/rest/vendor/api_v1) is an instruction of how to operate Beecology Web Service for developers.

```diff
- Web Service is also a bridge connect only DEVELOPERS and SERVER. 
- INTERNAL SHARING or CLIENT-OREIENTED SHARING SEPARATELY is recommended.
```

### Usage

To get the bumble bee information which ID is 1, client end need to send a GET http method to request the resource from server.
The following request URL includes 
- Main URL: http://beecology.wpi.edu/rest/v1
- Method Name: BeeDex
- bumble bee id: 1
```sh
GET http://beecology.wpi.edu/rest/v1/BeeDex/1
```
Web Services will return the result in JSON format
```JSON
[{"0":"1","bee_id":"1","1":"Bombus greseocollis","bee_name":"Bombus greseocollis","2":"Brown-belted bumble bee","common_name":"Brown-belted bumble bee","3":"This bumble bee has a black dot on the thorax, is dark around the wings and has a thin orange band before the abdomen becomes mostly black.","description":"This bumble bee has a black dot on the thorax, is dark around the wings and has a thin orange band before the abdomen becomes mostly black.","4":"May - October","active_months":"May - October","5":"bimaculatus, affinis, impatiens","confused":"bimaculatus, affinis, impatiens","6":"greseocollis.png","bee_pic_path":"greseocollis.png","7":null,"abdomen_list":null,"8":null,"thorax_list":null,"9":null,"head_list":null}]
```
At present, we have 3 core modules.

| Module | Description |
| ------ | ------ |
| BeeDex | methods about Bumblebee Dictionary|
| Bee Records | methods about Bumblebee Records users submit |
| USER | methods about user information |

For more details, please check [API Documentation](http://beecology.wpi.edu/rest/vendor/api_v1) 

### Links
[Module of Beecology Central Database](https://biymon.github.io/Beecology-Module/database_module)

### Todos

 - Develop new version for meeting the new requirement.(Add bumblebee behaviors, flower module etc.)
 - Android app and Web app are using the same version of APIs, I would like to separate it into 2 versions since the buiness logic processes of two apps will not completely consistent.
