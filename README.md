# JWT Go Example

I put this repo together so there would be something up for the [video][2] showing a JWT example using Go from [WilliamKennedy's][1] Youtube page.

The presenter is using the following resources to authenticate with JWTs:

- [dgrijalva/jwt-go][5]
- [codegangsta/negroni][3]
- [gorilla/mux][4]

## Set Up
```
$ git clone git@github.com:nicholasrucci/jwt-go-example.git
$ cd jwt-go-example
```

## Create Private & Public Keys
```
$ openssla rsa -in demo.rsa -pubout > demo.rsa.pub
$ openssl rsa -in demo.rsa -pubout > demo.rsa.pub
```

## Test
```js
$ curl localhost:3000/login
// returns JWT

$ curl -H <JWT> localhost:3000/api
// if valid: returns Success
// else: error
```

[1]: https://www.youtube.com/channel/UCD15RoW4ySsIE1YrQmspeeg
[2]: https://www.youtube.com/watch?v=eVlxuST7dCA
[3]: https://github.com/codegangsta/negroni
[4]: https://github.com/gorilla/mux
[5]: https://github.com/dgrijalva/jwt-go
