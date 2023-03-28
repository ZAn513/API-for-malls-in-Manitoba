# GROUP 5 - COMP3040

## API DESCRIPTION: 

This API  provides users with the ability to get list of all the malls or search for the malls by its location, as well as opening time and closing time.

## ENDPOINTS 

Our API is a very simple REST API, you only have to do a **GET** request 

**Endpoint 1: /malls** 

Description: Retrieve the list of all malls in Manitoba.

>**Parameters:** None. 

<br>

**Endpoint 2: malls/listByCity** 
Description: Retrieve the list of malls by city.

>**Parameters:**
>- cityName (String, Optional) : Name of the City that needs retrieving malls.

<br>

**Endpoint 3: malls/listByHours** 
Description: Retrieve the list of all malls by opening hours.

>**Parameters:**
>- openingHour (String, Optional): Hour that the mall will open.
>- closingHour (String, Optional): Hour that the mall will close.

## RESOURCES:

**Mall:** Used to hold and to retrieve the information of the malls.
```
{
    "mall": {
        "mallName":, 
        "city":,
        "address":,
        "numberOfStores":,
        "openingHour":,
        "closingHour":,
    }
}
```

## SAMPLE REQUEST & SAMPLE RESPONSE:

**Sample Request:**

```
GET /malls
```

**Sample Response:**
```
{
    "result": [
        {
            "mallName": "CF Polo Park",
            "city": "Winnipeg",
            "address" : "1485 Portage Ave #233",
            "numberOfStores": 200,
            "openingHour": "10:00:00",
            "closingHour": "21:00:00",

        },
        {
            "mallName": "Outlet Collection",
            "city": "Winnipeg",
            "address": "555 Sterling Lyon Pkwy",
            "numberOfStores": 100,
            "openingHour": "10:00:00",
            "closingHour": "21:00:00",
        },
        {
            "mallName": "Shoppers Mall",
            "city": "Brandon",
            "address": "1570 18th St",
            "numberOfStores": 90,
            "openingHour": "9:00:00",
            "closingHour": "20:00:00",
        },
        {
            "mallName": "Victoria Plaza Mall",
            "city": "Steinbach",
            "address": "13 Main St",
            "numberOfStores": 22,
            "openingHour": "10:00:00",
            "closingHour": "19:00:00",
        }
        ...
    ]
}
```

**Sample Request:**

```
GET /malls/listByCity?city=Winnipeg
```

**Sample Response:**

**Sample Response:**
```
{
    "result": [
        {
            "mallName": "CF Polo Park",
            "city": "Winnipeg",
            "address" : "1485 Portage Ave #233",
            "numberOfStores": 200,
            "openingHour": "10:00:00",
            "closingHour": "21:00:00",

        },
        {
            "mallName": "Outlet Collection",
            "city": "Winnipeg",
            "address": "555 Sterling Lyon Pkwy",
            "numberOfStores": 100,
            "openingHour": "10:00:00",
            "closingHour": "21:00:00",
        }
        ...
    ]
}
```


## REFERENCES:

[List of Manitoba Malls](https://www.shopping-canada.com/shopping-malls-centers/manitoba)

# CONTRIBUTORS:

- https://github.com/ChristianTrites - Christian Trites #7823653
- https://github.com/ZAn513 - Zhiyin An
- https://github.com/komeegbedi - Oghenekome Egbedi
- https://github.com/lehuykhanh41 - Khanh Le


