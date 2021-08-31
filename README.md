# ByCheck API gateway
Base URL: [gateway.bycheck.ir](https://gateway.bycheck.ir)

### Authentication
Send ```E-Access-Key={access_key}``` in request headers for verify its identity in API gateway.

### Status Codes
| Code | Description                                                              |
| ---- | ------------------------------------------------------------------------ |
| 200  | OK                                                                       |
| 400  | Bad request (client error)                                               |
| 401  | Unauthorized (invalid acccess key)                                       |
| 402  | Forbidden                                                                |
| 429  | Too many request (Rate limited)                                          |
| 490  | Access key expired                                                       |
| 491  | Origin server not valid (client IP address not exists in trusted list)   |
| 492  | Account suspended                                                        |

### Sections
- [Calculator](/Calculator.md)
