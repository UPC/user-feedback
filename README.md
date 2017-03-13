# user-feedback #

## API-Rest (v1) ##

### Afegir una valoració ###

Aquesta operació afegeix una nova valoració a un servei.

* **URL** `/api/v1/service/:service/rate`
* **Method** `POST`
* **URL parameters**
  * `service=[string]` _required_
* **Data parameters**
  * `rate=[string]` _required_
  * `app_key=[string]` _required_
* **Success Response:**
  * **Code** 201
  * **Content** `{ id : 12, service: "#1234", rate: "1", timestamp: "1488984558" }`
* **Error Response:**
  * **Code** 401 _(Unauthorized)_
  * **Content** `{ error : "App key unauthorized" }`

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
