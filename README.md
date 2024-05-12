### Golang microservice project

#### Testing endpoint
- Registration
```
curl --request POST \
  --url http://localhost:3000/auth/register \
  --header 'Content-Type: application/json' \
  --data '{
 "email": "elon@musk.com",
 "password": "1234567"
}'
```
- Login
```
curl --request POST \
  --url http://localhost:3000/auth/login \
  --header 'Content-Type: application/json' \
  --data '{
 "email": "elon@musk.com",
 "password": "1234567"
}'
```
- Create Product
```
curl --request POST \
  --url http://localhost:3000/product \
  --header 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJleHAiOjE3NDcwNzI5NzMsImlzcyI6ImdvLWdycGMtYXV0aC1zdmMiLCJJZCI6MSwiRW1haWwiOiJlbG9uQG11c2suY29tIn0.GnvcDqCygS5XCEYEVaEE0nUP7WKFOmN8sELqxh8maks' \
  --header 'Content-Type: application/json' \
  --data '{
 "name": "Product A",
 "stock": 5,
 "price": 15
}'
```
- Find one product
```
curl --request GET \
  --url http://localhost:3000/product/1 \
  --header 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJleHAiOjE3NDcwNzI5NzMsImlzcyI6ImdvLWdycGMtYXV0aC1zdmMiLCJJZCI6MSwiRW1haWwiOiJlbG9uQG11c2suY29tIn0.GnvcDqCygS5XCEYEVaEE0nUP7WKFOmN8sELqxh8maks'
```