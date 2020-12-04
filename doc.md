# Changelog
* [2020-12-04]
  * Added id, car_types response 
  * Added get car by :id 
  * Added filter: type displacement(cc), price, vehicle_type, fuel_type 
  
# Quick Link
###### [End Point](#end-point)
###### [Get Car List](#get-car-list)
###### [Get Car by ID](#get-car-by-id)
  
# End Point

## Get Car list
### Request
POST:  http://{url}/api/v1/car/getCarByBrand 
<br>*empty {} param will return top 100 cars*
```json
{ 
  "car_makers": ["Audi","BMW"], 
  "car_name": "", 
  "displacement": [1600,1999], 
  "price": [100000,199999], 
  "vehicle_type": "Sports", 
  "fuel_type": "Petrol-Electric" 
} 
```

| Params         | Desc             | Type            |Required  |Sample             
| -------------- |:----------------:| ---------------| --------| ------------------
|car_makers      |Car brand         | string array    | No       | ["Porsche","BMW"] 
|car_name        |Car name          | string          | No       | "BMW" 
|current         |Page number       | int; default 1  | No       | 1 
|displacement    |Car capacity(cc)  | int array       | No       | 1L-1.6L = [1000, 1599] 
|price           |Car price         | int array       | No       | 10k-50k = [10000,49999]
|vehicle_type    |Car type          | string          | No       | 1 of the below: <br>Sports<br>Stationwagon<br>Hatchback<br>Luxury Sedan<br>Commercial<br>SUV<br>MPV<br>Sedan
|fuel_type       |Fuel type         | string          | No       | 1 of the below: <br>Petrol-Electric<br>Petrol<br>Electric<br>Diesel<br>


### Response
https://github.com/gary-det/jsonjunk/blob/main/getcarlist.json 

## Get Car by ID
### Request
GET:  http://{url}/api/v1/car/{id} 

### Response
https://github.com/gary-det/jsonjunk/blob/main/getcarbyid.json 
