# cat JSON

This is a little helper script to make JSON files better "grepable".

```json
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25,
  "address": {
    "streetAddress": "21 2nd Street",
    "city": "New York",
    "state": "NY",
    "postalCode": "10021"
  },
  "phoneNumber": [
    {
      "type": "home",
      "number": "212 555-1234"
    },
    {
      "type": "fax",
      "number": "646 555-4567"
    }
  ],
  "gender": {
    "type": "male"
  }
}
```

Output of catjson.sh
```
./catjson.sh /tmp/foobar.json

.address.city = "New York"
.address.postalCode = "10021"
.address.state = "NY"
.address.streetAddress = "21 2nd Street"
.age = 25
.firstName = "John"
.gender.type = "male"
.lastName = "Smith"
.phoneNumber[0].number = "212 555-1234"
.phoneNumber[0].type = "home"
.phoneNumber[1].number = "646 555-4567"
.phoneNumber[1].type = "fax"
```
