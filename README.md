# paymentBilletForWill
simple payment ecosystem


this system on creat of springboot framework 


for execute need docker 

files in local folder docker_local this project

docker-compose up -d   

for execute need insert scritps in BD postgres
files in local folder SQL




exec call for payment bolet and call after anys secontes for check status update for paic out

localhost:8765 is my optional gateway 




need Authorization token for it call curland get token response add in next curl how new token 
curl --location --request POST 'http://localhost:8765/resell-oauth/oauth/token' \
--header 'Authorization: Basic QVBJX05BTUVfQUNDRVNTOkFQSV9TRUNSRVRfQUNDRVNT' \
--header 'Content-Type: application/x-www-form-urlencoded' \
--data-urlencode 'username=nina@gmail.com' \
--data-urlencode 'password=123456' \
--data-urlencode 'grant_type=password'


curl --location --request POST 'http://localhost:8765/resell-person/billet/payment' \
--header 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJleHAiOjE2NTkwMjUzMDYsInVzZXJfbmFtZSI6Im5pbmFAZ21haWwuY29tIiwiYXV0aG9yaXRpZXMiOlsiUk9MRV9PUEVSQVRPUiJdLCJqdGkiOiIzNzhmOTRhNy1kMjdmLTQwY2YtOTkwNy0wYmU5ZDAxNTdiNzEiLCJjbGllbnRfaWQiOiJBUElfTkFNRV9BQ0NFU1MiLCJzY29wZSI6WyJyZWFkIiwid3JpdGUiXX0.NBpa-wWlKRUEdgW1x3epm8xKMNCYeIEg5ELNtIalCmg' \
--header 'Content-Type: application/json' \
--data-raw '{
    "amount": 12000,
    "barCode": "826500000011323116990009002022153320470000001062"
}'


when calling the payment of the boleto for the first time it will be saved and prepared to be processed in the bank

then the micro service will process the payment if the customer has a balance and change the status to paid out

so check the status of the ticket by the barcode


