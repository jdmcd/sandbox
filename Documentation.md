# Devshop-API

# API (v1) Documentation
This is a sandbox api that allows students to interact with a live server and see how networking works. The endpoint is located [here](http://mcdappdev.pythonanywhere.com)

## Dependencies
To make things a little easier, you are allowed to use the following two dependencies:
- [Alamofire](https://github.com/Alamofire/Alamofire)
- [SwiftyJSON](https://github.com/SwiftyJSON/SwiftyJSON)

## Students

#### Get all students

**GET:**
```
/api/student
```

**Response:**
```json
{
	"Jimmy": 80,
    "Jason": 62,
    "Jeremy": 54,
    "Emma": 22,
    "Allie": 14,
    "Molly": 98,"
}
```

**Status Codes:**
* `200` if successful


#### Create new student

**POST:**
```
/api/student
```

**Body:**
```json
{
	"name": "Jack",
	"level": 30
}
```

**Response:**
```json
{
	"Jack": 30
}
```

**Status Codes:**
* `400` validation error. Additional information will be provided in the response
* `201` student created


#### Get information on a current student

**GET:**
```
/api/student/:student_name
```

**Response:**
```json
{
	"student_name": "level"
}
```

**Status Codes:**
* `404` student doesn't exist
* `201` returned student


#### Update a current student

**PUT:**
```
/api/student/:student_name
```

**Body:**
```json
{
	"level": 50
}
```

**Response:**
```json
{
	"student_name": "level"
}
```

**Status Codes:**
* `404` student doesn't exist
* `400` validation error. Additional information will be provided in the response
* `200` success


#### Delete a current student

**DELETE:**
```
/api/student/:student_name
```

**Status Codes:**
* `404` student doesn't exist
* `204` deleted


