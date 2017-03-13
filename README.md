# user-feedback #

## API-Rest (v1) ##

### Afegir una nova unitat ###

* **URL** `/api/v1/unit`
* **Method** `POST`
* **Success response:**
  * **Code** 201
  * **Content** `{ id : "9548d3575165" }`

### Afegir una nova valoració a un servei ###

* **URL** `/api/v1/unit/:unit/service/:service/rate`
* **Method** `POST`
* **URL parameters**
  * `unit=[string]`
  * `service=[string]`
* **Data parameters**
  * `rate=[string]` _required_
* **Success response:**
  * **Code** 201
  * **Content** `{ id : "75e817cecc8e", service: "dhcp", rate: "1", timestamp: 1488984558 }`
* **Not found response:**
  * **Code** 404
  * **Content** `{ error : "Service not found" }`

### Obtenir les valoracions d'un servei ###

  * **URL** `/api/v1/unit/:unit/service/:service/rate`
  * **Method** `GET`
  * **URL parameters**
    * `unit=[string]`
    * `service=[string]`
  * **Success response:**
    * **Code** 200
    * **Content** `[{ rate : "1", count: 15 }, { rate: "2", count: 7 }, { rate: "3", count: 1 }]`
  * **Not found response:**
    * **Code** 404
    * **Content** `{ error : "Service not found" }`

### Obtenir tots els serveis d'una unitat ###

  * **URL** `/api/v1/unit/:unit/service`
  * **Method** `GET`
  * **URL parameters**
    * `unit=[string]`
  * **Success response:**
    * **Code** 200
    * **Content** `[{ service: "dhcp" }, { service: "web" }]`
  * **Not found response:**
    * **Code** 404
    * **Content** `{ error : "Unit not found" }`

## Llicència ##

Copyright (C) 2015-2016 Universitat Politècnica de Catalunya - UPC BarcelonaTech - www.upc.edu

```
This program is free software: you can redistribute it and/or modify
it under the terms of the GNU Affero General Public License as
published by the Free Software Foundation, either version 3 of the
License, or (at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU Affero General Public License for more details.

You should have received a copy of the GNU Affero General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.
```
