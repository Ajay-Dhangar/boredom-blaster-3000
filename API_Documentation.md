The Bored API helps you find things to do when you're bored! There are fields like the number of participants, activity type, and more that help you narrow down your results.

## API Documentation

### Base URL

https://www.boredapi.com/api/

### Endpoints

#### GET /activity

Returns a random activity based on the parameters passed in the query string.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| **type** | *string* | The activity type, e.g. education, recreational, social, diy, charity, cooking, relaxation, music, busywork. |
| **participants** | *integer* | The number of participants, e.g. 1, 2, 3, 4. |
| **price** | *float* | The price range between 0.0 and 1.0, e.g. 0.1, 0.2, 0.3. |
| **accessibility** | *float* | The accessibility range between 0.0 and 1.0, e.g. 0.1, 0.2, 0.3. |

##### Example

```bash
curl -X GET "https://www.boredapi.com/api/activity?type=recreational&participants=1&price=0.1&accessibility=0.1"
```

##### Response

```json
{
  "activity": "Learn how to play a new sport",
  "type": "recreational",
  "participants": 1,
  "price": 0.1,
  "link": "",
  "key": "3943500",
  "accessibility": 0.1
}
```

