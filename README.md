# paymentBilletForWill
simple payment ecosystem


this system on creat of springboot framework 


for execute need docker 

files in local folder docker_local this project

docker-compose up -d   


exec call for payment bolet and call after anys secontes for check status update for paic out

localhost:8765 is my optional gateway 


curl --location --request POST 'http://localhost:8765/resell-person/billet/payment' \
--header 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJleHAiOjE2NTkwMjUzMDYsInVzZXJfbmFtZSI6Im5pbmFAZ21haWwuY29tIiwiYXV0aG9yaXRpZXMiOlsiUk9MRV9PUEVSQVRPUiJdLCJqdGkiOiIzNzhmOTRhNy1kMjdmLTQwY2YtOTkwNy0wYmU5ZDAxNTdiNzEiLCJjbGllbnRfaWQiOiJBUElfTkFNRV9BQ0NFU1MiLCJzY29wZSI6WyJyZWFkIiwid3JpdGUiXX0.NBpa-wWlKRUEdgW1x3epm8xKMNCYeIEg5ELNtIalCmg' \
--header 'Content-Type: application/json' \
--data-raw '{
    "amount": 12000,
    "barCode": "826500000011323116990009002022153320470000001062"
}'
