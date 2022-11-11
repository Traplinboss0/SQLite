# SQLite

# Actividad de desarrollo de base de datos en Sqlite


## Update
Esta consulta se emplea para actualizar o modificar los registros ya existentes en una tabla ya elaborada, cabe destacar que si utilizamos otro tipo de sentencias como **Where** junto con esta podremos actualizar solo filas seleccionadas. 

Para actualizar una tabla deberemos utilizar el Update seguido de la tabla para posteriormente indicar la modificacion o el cambio que se va a realizar. 

**Ejemplo**

![Alt text](https://github.com/MateoRodriguez1426/Actividad-Sqlite/blob/main/Imagenes/Aspose.Words.f9333c64-612e-45e6-a455-d9051c5a5f64.004.png)

![Alt text](https://github.com/MateoRodriguez1426/Actividad-Sqlite/blob/main/Imagenes/Aspose.Words.f9333c64-612e-45e6-a455-d9051c5a5f64.007.png)

Como podemos ver en el siguiente ejemplo actualizamos la tabla Users de tal manera que cambiamos algunos datos. 

## Estructura de la base de datos .schema
Los esquemas en bases de datos se encargan de representar la configuracion logica de toda la base de datos relacional, solo existen dos maneras de representarlos las cuales son: mediante la representacion visual y como conjunto de formulas tambuien conocidad como conjunto de restricciones de integridad . 

![Alt text](https://d2slcw3kip6qmk.cloudfront.net/marketing/pages/chart/seo/database/discovery/logical-physical-schema.svg)



 este tipo de esquemas se crean con la intencion de ayudar a los programadores que cuyo software tiene algun tipo de interaccion con la base de datos. 

 Como ya habiamos indicado antes existen dos tipos de esquemas de bases de datos:

 **Esquema Logico:** Este esquema expresa las restricciones logicas que se aplican a los datos almacenados

 **Esquema Fisico:** Los esquemas fisicos de bases de datos son aquellos que disponen como se almacenal los datos en un sistema de almacenamiento

 ## date and time function
 Estos datos y funciones se emplean en el uso de tiempo y fechas como su nombre lo indica. Las funciones con las que cuenta SQLite toman un valor de tiempo como argumento para posterior mente almaenarlo o llamarlo. 

 Los valores que pueden tomar este tipo de funciones son: 

1. texto en un subconjunto de la ISO-8601 formato.

2. números que representan el día juliano.

3. números que representan el número de segundos desde ( o antes ) 1970-01-01 00:00:00 UTC (la marca de tiempo unix).

A continuacion veremos cada una de las funciones que posee SQLite

1. **date(time-value, modifier, modifier, ...):** 
Esta funcion devuelve la fecha como texto eb el formato AAAA-MM-DD

2. **time(time-value, modifier, modifier, ...):** 
En este caso la funcion nos retorna la fecha en el formato HH: MM: SS

3. **datetime(time-value, modifier, modifier, ...):**
En el caso de la funcion datetime esta nos dara el formato de fecha AAAA-MM-DD HH: MM: SS. Es una mezcla entr la funcion date y time

4. **julianday(time-value, modifier, modifier, ...)**
Esta funcion devolvera el dia Juliano o en otras palabras el numero fraccionados de dias desde el mediodia en Greenwich el 24 de noviembre de 4714 a. C.

5. **unixepoch(time-value, modifier, modifier, ...):**
En este caso la funcion nos retornara una marca de tiempo unix, es decir la cantidad de segundos desde 1970-01-01 00:00:00 UTC.

6. **strftime(format, time-value, modifier, modifier):**
Devuelve la fecha de acuerdo con la cadena de formato que se especifica como primer argumento. 


**Ejemplo**

![Alt text](https://github.com/MateoRodriguez1426/Actividad-Sqlite/blob/main/Imagenes/Aspose.Words.f9333c64-612e-45e6-a455-d9051c5a5f64.005.png)

En el siguiente ejemplo podemos apreciar como se ve la fecha especificada en cada uno de los seis formatos

## primary key constraint
la Primary key (o llave primaria en español) es una retriccion que identifica de forma exclusiva cada registro en una tabla. Las claves primarias siempre tendran valores unicos y no puede terner valores vacion o null


**Ejemplo**


![Alt text](https://github.com/MateoRodriguez1426/Actividad-Sqlite/blob/main/Imagenes/Aspose.Words.f9333c64-612e-45e6-a455-d9051c5a5f64.008.png)

## not null constraint
Generalmente los registros pueden contener valores nulos. Para evitar que existan espacios vacios en los registros utilizamos los **Not Null**, los cuales restricciones que se utilizan para que las columnas no puedadn quedar vacias. 

**Ejemplos**

![Alt text](https://github.com/MateoRodriguez1426/Actividad-Sqlite/blob/main/Imagenes/Aspose.Words.f9333c64-612e-45e6-a455-d9051c5a5f64.008.png)


## unique constraint
los **unique constrain** son restricciones del sistema para solo tener un valor unico por columna, de tal manera que cumple la misma funcion que una **primary key**, la diferencia entre el uno y el otro es que **Unique constrain** permite tener varios en un solo  registro y **primary key** solo puede haber uno por registro

**Ejemplo**

![Alt text](https://github.com/MateoRodriguez1426/Actividad-Sqlite/blob/main/Imagenes/Aspose.Words.f9333c64-612e-45e6-a455-d9051c5a5f64.014.png)


## Default Constraint
Esta funcion se utiliza para dejar el valor de una columna predefinido, este valor predispuesto se agrega a todos los registros nuevos siempre y cuando no se especifique otro 

**Ejemplo**
![Alt text](https://github.com/MateoRodriguez1426/Actividad-Sqlite/blob/main/Imagenes/Aspose.Words.f9333c64-612e-45e6-a455-d9051c5a5f64.024.png)


## check constraint
Si se desea limitar el rango de valores que se quieren ingresar en una tabla utilizaremos Check constraint, ya que o podemos colocar en una columna y nos permitira limitar el numero de valores que puede tener 

**Ejemplo**
![Alt text](https://github.com/tcarolina/SQLite/blob/main/SQLite/Imagenes/check.PNG)



## Alter table
Esta instruccion se emplea para modificar la informacion de tablas ya cradas, estos pueden ser los nombre de columnas, datos de las filas o columnas y alterar otro tipo de datos. 

**Ejemplo**
![Alt text](https://github.com/MateoRodriguez1426/Actividad-Sqlite/blob/main/Imagenes/Aspose.Words.f9333c64-612e-45e6-a455-d9051c5a5f64.018.png)


## drop, delete
En caso de querer borrar tablas o culumnas podemos utilizar las instrucciones con **drop** o **delete**. puesto que estas se emplean para eliminar datos de las tablas o las mismas tablas.

**Ejemplo**
![Alt text](https://github.com/MateoRodriguez1426/Actividad-Sqlite/blob/main/Imagenes/Aspose.Words.f9333c64-612e-45e6-a455-d9051c5a5f64.020.png)













