# GROUP 5 - COMP3040

## API DESCRIPTION: 

This is an API for people to generate the list of all the malls or search malls in Manitoba by city. Besides allowing users to retrieve the list of all malls, it also allow users to search for the malls by its location, as well as opening time.

## ENDPOINTS 

**GET** malls - Retrieve the list of all malls in Manitoba.

>**Parameters:** None. 

<br>

**GET** malls/listByCity/- Retrieve the list of malls by city.

>**Parameters:**
>- cityName (String) : Name of the City that needs retrieving malls.

<br>

**GET** malls/listByHours/ - Retrieve the list of all malls by opening hours.

>**Parameters:**
>- openingHour (String): Hour that the mall will open.
>- closingHour (String): Hour that the mall will close.

## RESOURCES:

**Mall:** Used to hold and to retrieve the information of the malls.
```
{
    "mall": {
        "mallName:", 
        "location:",
        "openingHour:"
        "closingHour:"
    }
}
```

## SAMPLE REQUEST & SAMPLE RESPONSE:

**Sample Request:**

```
GET http://api.winnipegmallnetwork.net/data/list.json?location=*
```

**Sample Response:**
```
{
    "result": [
        {
            "mallName": "CF Polo Park",
            "location": "Winnipeg",
            "openingHour": "9:00:00",
            "closingHour": "19:00:00",

        },
        {
            "mallName": "Outlet Collection",
            "location": "Winnipeg",
            "openingHour": "10:00:00",
            "closingHour": "21:00:00",
        },
        {
            "mallName": "St Vital Mall",
            "location": "Winnipeg",
            "openingHour": "9:00:00",
            "closingHour": "20:00:00",
        },
        {
             "mallName": "Portage Place",
            "location": "Winnipeg",
            "openingHour": "10:00:00",
            "closingHour": "19:00:00",
        }
        ...
    ]
}
```
## REFERENCES:

[List of Manitoba Malls](https://www.shopping-canada.com/shopping-malls-centers/manitoba)


