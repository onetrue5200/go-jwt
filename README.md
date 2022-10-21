# JWT Authentication in Go(Gin/Gorm)

<https://www.youtube.com/watch?v=ma7rUS_vW9M&list=WL&index=3&t=1s>

## Install Packages
[gorm](https://gorm.io/docs/connecting_to_the_database.html)
[gin](https://gin-gonic.com/docs/quickstart/)
[bcrypt](https://pkg.go.dev/golang.org/x/crypto/bcrypt)
[jwt](https://github.com/golang-jwt/jwt)
[godotenv](https://github.com/joho/godotenv)
[CompileDeamon](https://github.com/githubnemo/CompileDaemon)
```shell
go install github.com/githubnemo/CompileDaemon
compiledaemon --command="./go-jwt"
```

## Dotenv setup
Add your application configuration to your .env file in the root of your project:
```
PORT=3000
```
Then in your Go app you can do something like
```
err := godotenv.Load()
if err != nil {
log.Fatal("Error loading .env file")
}

port := os.Getenv("PORT")
```

## Gin setup
```
r := gin.Default()
	r.GET("/ping", func(c *gin.Context) {
		c.JSON(200, gin.H{
			"message": "pong",
		})
	})
	r.Run()  // try load port from os.Getenv("PORT")
```

## Connecting to a database

## The user model

## Login

when import jwt package, remember to use v4 package.

## Auth Middleware