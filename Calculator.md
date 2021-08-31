# Calcuator API

### Request
URL: ```/api/calculator```

Method: ```GET```

Query parameters:

| Name              | Value                            |
| ----------------- | -------------------------------- |
| Amount            | Unit: Toman, Exp: 2000000        |
| Prepayment        | Unit: Toman, Exp: 500000         |
| FactorDate        | Type: Gregorian, Exp: 30-08-2021 |
| InstallmentsCount | Exp: 6                           |
| MonthsCount       | Exp: 12                          |

### Response
Status codes: 200, 400 

- **Ok (200) response body:** list of installments 
``` json
[
  {
    "amount": 175000,
    "date": "2021-09-30T00:00:00"
  },
  {
    "amount": 175000,
    "date": "2021-09-30T00:00:00"
  }
]
```

- **Bad request (400) response body:** Error code

| Error code | Description                                                        |
| ---------- | ------------------------------------------------------------------ |
| 1710       | Prepayment larger than factor amount                               |
| 1711       | Factor amount is too small (must be larger than 500,000T)          |
| 1712       | Prepayment is too small (must be larger than 25% of factor amount) |
| 1714       | Store financial data is incomplete                                 |
