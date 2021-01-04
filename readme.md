- Deploy on Kie Server
- Run the following request (the following auth is for user kieserver, pass kieserver1!)

curl --location --request POST 'http://localhost:8080/kie-server/services/rest/server/containers/DMNDateTest/dmn' \
--header 'Authorization: Basic a2llc2VydmVyOmtpZXNlcnZlcjEh' \
--header 'Content-Type: application/json' \
--data-raw '{
  "model-namespace": "https://kiegroup.org/dmn/_3C63BA6B-725A-4FB3-ABCD-8C20C10E6019",
  "model-name": "MyDecision",
  "decision-name" : [ ],
  "dmn-context" :
    {
        "birthDate": "2018-09-10"
    }
}'
