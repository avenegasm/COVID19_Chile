## Panel Interactivo
Para ver el Panel Interactivo visite https://datastudio.google.com/reporting/b1689869-0c59-442c-951d-2991c0fc611d/

## Base de datos
Para descargar o conectarse a la base de datos directamente, usar la dirección pública https://raw.githubusercontent.com/ivanMSC/COVID19_Chile/master/covid19_chile.csv

Aparentemente, el Ministerio cree que es una buena idea subir un PDF distinto todos los días con los casos reportados en un tabla horrenda. Por eso, en este repositorio dejo una tablita ordenada que intentaré mantener actualizada día a día.
El archivo covid19_chile.csv es una base de datos de los casos reportados [aquí](https://www.minsal.cl/nuevo-coronavirus-2019-ncov/casos-confirmados-en-chile-covid-19/) por el Ministerio de Salud de Chile.

* Update: A contar de hoy `18-mar-2020` MinSal no reporta datos granulares con `Sexo`, `Edad` ni `Centro_de_Salud`. Solo reporta el total de  casos por `Region`. Por lo que a partir de esta fecha, la base de datos tendrá muchos espacios vacíos, a menos que alguien quiera soltar la información.

Los campos de la base de datos son:
* `ID`: Número correlativo desde el primer caso. Comienza en `1`
* `Fecha`: En formato `DD-MM-YYYY`
* `Region_Numero`: Número de región de Chile, ordenado de Norte a Sur. Es decir, `Arica y Parinacota = 1`, `Magallanes = 16`
* `Region`: Nombre de región de Chile, nomenclatura según Minsal
* `Sexo`: Según lo informado por Minsal
* `Edad`: Según lo informado por Minsal
* `Centro_de_Salud`: Según lo informado por Minsal
* `Comuna`: La obtengo intentando ubicar el `Centro_de_Salud` en google Maps. A veces hay mas de un `Centro_de_Salud` con el mismo nombre, por lo que intento adivinar.
* `lat`: Ídem. Latitud del `Centro de Salud`
* `lon`: Ídem. Longitud del `Centro de Salud`
* `Tipo_de_caso`: `Confirmado`, `Muerte`, `Recuperado`
* `lat_comuna`: Latitud de la `Comuna`
* `lon_comuna`: Longitud de la `Comuna`
