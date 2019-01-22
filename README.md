# REST API Terminology

Fork and clone this repository. Then, push to github with all bad answers deleted and only the correct answers showing.

**1. What does it mean REST?**

Stands for Representational State Transfer is an architectural style for developing web services


**2. Who coined the REST term?**

Roy Fielding

**3. In which protocol REST is based?**

Web protocols (HTTP)


**4. What are the main building blocks of a REST Architecture?**

Identifying Resources 
Designing URLs 
API Response
Storing application data on server side 

Resources
Representations
Messages
Resource Hypermedia


**5. Identifying a resource is easy; you know how to access it and you even know how to request for a specific format. Since REST is using HTTP protocol as a standing point, there are some actions related to resources: CRUD operations.**

Complete the below table:+


|HTTP Verb|Proposed Action|
|---------|---------------|
|GET      |    Read       |
|POST     |    Create     |
|PUT      | Update/Replace|
|DELETE   |    Delete     |

**6. Status Code**

Another interesting standard that REST can benefit from when based on HTTP is the usage of HTTP status codes.

+ What’s is a status code?
Is a response that indicate wether a specific HTTP request has
been successfully completed


+ Explain with your own words, the meaning of next codes:

|Status Code|Description|
|-----------|-----------|
|404        |           |
|200        |           |
|500        |           |

404:Client error response ==> The resource doesnt exist or the server cant find requested source

200: Successful response ====> The request has succeeded

500: Internal Server Error =====> The server fail


**7. Status Code are grouped in five sets.**

Write what are their meaning.

|Group|Description              |
|-----|-------------------------|
|1XX  | Information responses   |
|2XX  | Successful  responses   |
|3XX  | Redirection messages    |
|4XX  |  Client error responses |
|5XX  | Server error responses  |

**8. HTTP Status Codes and Their Related Interpretation**

There are the most common status codes in HTTP responses. Please, fill with the required description.

|Status Code|Meaning                     |
|----------|-----------------------------|
|200       |      OK                     |
|201       |       Created               |
|204       | 			No Content             |
|301       |       Moved Permanently     |
|400       |       Bad Request           |
|401       |       Unauthorized          |
|403       |       Forbidden             |
|404       |       Not Found             |
|405       |       Method Not Allowed    |
|500       |       Internal Server error |

###### [To see the full list of HTTP status codes and their   meaning, please refer to the RFC of HTTP 1.1](http://tools.ietf.org/html/rfc7231#section-6)

**9. How are called the points of contact between all client apps and the API?**

Endpoints

**10. The following is a good example or bad example of a named access point? And why?**


_meant to list the books in a bookstore_

+ `GET /books/action1`

Bad example, need to be descriptive


**11. Uniform Interface**



To solve this problem, you can apply the REST style to the endpoints, and thanks to HTTP, you also have verbs to indicate actions.

|Old Style                 |REST Style                 |
|------------------------------------------------------|
|`/getAllBooks`            |   GET/ books              |   
|`/submitNewBook`          |   POST/ books             |
|`/updateAuthor`           |   PUT/ authors/:id        |
|`/getBooksAuthors`        |   GET/ books/:id/authors  |
|`/getNumberOfBooksOnStock`|   GET/ books              |
|`/addNewImageToBook`      |   POST/ books/:id/image   |
|`/getBooksImages`         |   GET/ books/:id/images   |
|`/addCoverImage`          |   POST/ books/:id/cover   |
|`/listBookCovers`         |   GET/ books/:id/         |

**12. What JSON does it mean?**

JavaScript Object Notation


**13. Anatomy of a `REQUEST`**

Make a `curl` "client-url" request to _GitHub API_

```sh
$ curl GET https://api.github.com/ Accedes a la información de un endpoint
```

According to the responded request, answer what does it mean the next parts from the handler:

+ _`Content-Type`_.
    El tipo de contenido que estamos manejando
+ _`Status`_.
    La respuesta dependiendo de si la peticion fue exitosa
+ _`Date`_.
    La fecha en que se hizo la peticion
+ _`Content-Length`_.
    Longitud del contenido


###### If response is not showing those parts, ask to google how to print them in console.

```sh
curl https://api.github.com/ --head
#
```
