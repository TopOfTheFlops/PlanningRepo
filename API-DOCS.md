Usage

To get everything:

[GET] /api/v1/flop
/flop will return JSON with a key of cats which is an array of objects with keys of id and name. Success returns a status code of 200.

{"cats":[
  {"id":0,"name":"fluffy"},
  {"id":1,"name":"tick"},
  {"id":2,"name":"frank"}
]}
[GET] /api/v1/cats/:id
/:id will return an object containing the specific kitty with keys of id and name. If successful this request will return a status code of 200. If the /:id is invalid you may get a status code of 404, meaning this cat does not exist (yet?).

{"id":0,"name":"fluffy"}
[POST] /api/v1/cats
This will add a cat to the database and will an object containing your new cat. Success will return a status code of 201. Failure will return a status code of 400.

{"cats":[
  {"id":0,"name":"fluffy"},
  {"id":1,"name":"tick"},
  {"id":2,"name":"frank"}
  {"id":3,"name":"puss"}
]}
[PUT] /api/v1/cats/:id
This will modify an existing cat in the database (based on give id) and return an object of the updated cat.

{"id":3,"name":"keith"}
[DELETE] /api/v1/cats/:id
This will remove the id related cat from the database and return JSON of the updated database.

{"cats":[
  {"id":0,"name":"fluffy"},
  {"id":2,"name":"frank"}
  {"id":3,"name":"keith"}
]}
Install

With npm installed, run

$ npm install meowtown-api
Acknowledgments

meowtown-api was inspired by Meowtown ... duh.

