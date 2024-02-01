---

title: My Second Blog Post
author: 'Vaccari, Franco'
description: "After learning some Astro, I couldn't stop!"
image:
url: "https://docs.astro.build/assets/arc.webp"
alt: "Thumbnail of Astro arcs."
pubDate: 2024-02-01
tags: ["astro", "blogging", "learning in public", "successes"]

---

# Fundamentos de las Bases de Datos

Uno de los usos más importantes de los dispositivos informáticos es la capacidad de almacenamiento de grandes cantidades de información, la cual luego puede ser recuperada.  
Cuando trabajamos en una computadora lo más común es querer guardar el trabajo que estamos desarrollando para luego poder retomar en un putno más tarde. Esto es posible en muchos de los programas que utilizamos a diario, gracias a que podemos producir archivos los cuales nos darán la posibilidad de almacenar información.  
Estos archivos en su mayoría son creados para almacenar el trabajo en una aplicación determinada y muy posiblemente solo puedan leerse con la misma aplicación o con alguna aplicación que tenga afinidad con el archivo.  
¿Qué pasa si solo quiero almacenar información?  
Para responder esta pregunta, deberíamos comenzar realizando otra pregunta, ¿Qué es la información?, Podemos definir información como un conjunto de Datos que relacionados entre sí nos dicen algo. Por ejemplo: _Juan, 38 años, vive en Ciudad de Buenos Aires, Es médico_.  
Miremos una cosa, aquí podemos observar que para generar información necesitamos de datos relacionados entre sí.  
Estos datos no son mas que una **abstracción** de la realidad, **codificada** para que la podamos entender. Pero estos datos solos no tendrían un sentido, por lo tanto deben estar ligados a otros datos para cobrar un sentido es así que si yo solo digo _38 años_ y no hago referencia que se trata de Juan, ese dato no tiene sentido ya que puede hacer referencia a cualquier cosa.  
Para ello es que se crearon las bases de datos, para poder almacenar estos datos, de forma ordenada y estructurada, para que sea fácil su posterior lectura y comprención.

# Bases de Datos y sus estructuras

Ahora que sabemos que una base de datos es una estructura para guardar datos relacionados entre sí y que podremos recuperar luego. Debemos tener en cuenta la forma en la que trabajaremos con las bases de datos. Generalmente pensamos en una base de datos como una estructura robusta en la cual los datos almacenados tienen cierta relación.  
Para trabajar con bases de datos debemos primero tener muy en cuenta que es lo que necesitamos representar. Recordemos que los datos son un reflejo de la realidad. Teniendo en cuenta esto, vamos a representar **entidades** por ejemplo una entidad podría ser un **auto**, sabemos que todos los autos cuentan con características comunes entre sí, los cuales vamos a llamar **atributos**.  
Podríamos tranquilamente decir que cada auto cuenta con:

- Marca
- Modelo
- Color
- Año de fabricación
- Patente o matrícula
- Tipo de motor

Estos son los Atributos que nos interesan de la entidad Autos. Pero cuidado, no siempre las entidades tienen los mismos atributos, estos van a diferir dependiendo del propósito de los datos, en pocas palabras, puede que si me dedico a vender autos necesite otros atributos más específicos como por ejemplo el número de registro o el tipo de seguro, los cuales puede que para un lavadero de autos no sean tan importantes.

Podemos clasificar los atributos en diferentes tipos:

- Según su Composición
  - Simples
  - Compuestos
- Según sus valores
  - Valor simple
  - Multivalor
- Según su origen
  - Almacenados
  - Derivados
- Identificador

### Según su composición

Podremos ver que según su composición, podremos clasificar los atributos en simples o compuestos, los atributos **simples** son aquellos que almacenan un dato concreto, por ejemplo nombre simpre va a almacenar un nombre o tambien en el caso de los autos podría ser el modelo o la marca. Ahora también nos encontraremos con los atributos **compuestos**, estos hacen referencia a un conjunto de datos simples, por ejemplo en una estructura compleja podríamos decir que una persona tiene una dirección, la cual se compone de una calle y un número. Sí lo llevamos a un gráfico lo deberíamos representar con circulos cerrados. En el caso de los datos simples el circulo estará unido directamente a la entidad, y en el caso de los compuestos Calle y Número se encontrarán unidos a Dirección la cual será el nexo a la entidad.

### Según sus valores

Podemos distinguír aquí dos tipos de valores los de **valor simple** o **monovaluados** y los de **valor múltiple** o **multivalor**, los primeros hacen referencia o son similares a los valores simples vistos anteriormente, son formados solo por un valor, estos son representados al igual que los anteriores por un circulo. En el caso de los segundos, estos pueden tener muchos valores diferentes, y son representados por un doble circulo.

### Según su origen

En este apartado reconocemos dos tipos los **Almacenados** los cuales son almacenados directamente en la base de datos, al igual que los simpres se representan con un circulo. En segundo lugar encontramos a los **Derivados**, los cuales derivan directamente de otro datos, por ejemplo, si almacenamos la fecha de fabricación de un auto, podremos determinar la antigüedad de la unidad. por lo tanto la fecha de fabricación sería un dato de tipo **Almacenado** y la Antiüedad sería un dato **Derivado**.

### Identificadores

Son datos únicos por cada registro dentro de la base de datos, nos van a servir exclusivamente para reconocer, en el caso de los autos, cada uno de los autos.

# Introducción a SQL

Existen dos tipos de bases de Datos, las Relacionales y las No relacionales, las de tipo relacionales son las conocidas como **SQL** y las no relacionales **NOsql**, ambas tienen el mismo propósito que es el almacenamiento de la información, pero su principal diferencia es que las SQL guardan información mediante tablas y manejan el modelo **Entidad-Relación** y las NoSql en cambio, manejan el modelo de **colecciones de documentos**.

## SQL

_Structured Query Language_ es un lenguaje para manejar bases de datos a través de consultas, las cuales nos permitirán **Leer, Crear, Actualizar y Eliminar** datos. Es un lenguaje muy similar al ingles en su sintaxis y permite a través de sentencias simples obtener datos de tablas.

## Motor de bases de datos

SQL es un lenguaje estandarizado, pero a pesar de ser un estandar, existen diferentes motores de bases de datos con sutiles diferencias, estos motores pueden ser PosgresSQL, MySQL, SQLite, etc. que si bien utilizan SQL para gestionar las bases de datos, tienen sutiles diferencias unas con otras.

## Bases de datos

Una base de datos SQL es un conjunto de tablas que hacen referencias a **entidades**, la cual contendrá **atributos**, Estos formarán las columnas de las tablas, Sí en algún momento trabajaste con Excel o algún gestor de hojas de cálculo, son estructuras similares.  
Estas bases de datos son de tipo **relacionales** ya que vamos a poder hacer relación entre un atributo de una tabla y un registro de otra tabla, para evitar que se repitan los datos que estamos almacenando.

### Para practicar

Para practicar SQL vamos a utilizar [SQLBOLT](https://sqlbolt.com/ "ejercicios prácticos"), donde podremos realizar ejercicios prácticos de forma online.

## Sintaxis SQL

SQL es un lenguaje que es fácil de entender a la hora de realizar consultas.
Debemos tener en cuenta que este no es key sensitive es decir que no requiere de mayusculas y minusculas en algunas palabrar específicas sino que eso no importa, a pesar de que por buenas prácticas se recomienda que las palabras clave si se escriban en mayúsculas, además todas las sentencias SQL deben ternar con el **;**.

### La primer sentencia

la primer sentencia que seguramente nos vamos a cruzar y con la cual podremos recuperar toda la información de una tabla es la siguiente: `SELECT * FROM tabla;`, en la cual seleccionamos toda la información de una tabla.

Debemos recordar que una tabla está formada por **Columnas, Filas y Celdas**. las tablas hacen referencia a una Entidad y sus columnas hacen referencia a un atributo de la entidad. Ejemplo:

| id_autos | marca     | modelo | año  |
| -------- | --------- | ------ | ---- |
| 1        | Vokswagen | GOL    | 2011 |
| 2        | Renault   | CLIO   | 2015 |
| 3        | Peugeot   | 408    | 2011 |
| 4        | Vokswagen | Voyage | 2008 |
| 5        | Renualt   | Suran  | 2007 |

Con la sentencia SQL `SELECT * FROM autos;`, estaríamos recuperando toda la información contenida en la tabla.

Para recuperar por ejemplo solo las marcas de los autos deberíamos hacer lo siguiente: `SELECT marca FROM autos;`

## Clase 2

[SQLBolt - Clase 2](https://sqlbolt.com/lesson/select_queries_with_constraints)

### Filtrar registros

Para filtrar registros de una tabla, debemos aplicar la clausura **WHERE** la cual nos traerá los registros que coincidan con el filtro. Ejemplo si solo queremos los autos de marca Volkwagen lo que debemos hacer es `SELECT * FROM autos WHERE marca = 'Volkswagen';`, deberíamos utilizar aquí operadores de comparación por ejemplo si queremos traer autos fabricados antes del 2010 `SELECT * FROM autos WHERE año < 2010;`

### Operadores de ADICIÓN:

Son operadores que permiten concatenar varias clausulas en una sola sentencia:
Ejemplo:
Sí queremos recuperar todos los autos de marca renault que fueron fabricados antes del 2010 `SELECT * FROM autos WHERE marca = 'Renault' AND año < 2010;`

### Operadores de COMPARACIÓN NUMÉRICOS:

| Operador | Acción        |
| -------- | ------------- |
| >        | Mayor         |
| <        | Menor         |
| =        | Igual         |
| !=       | Distinto      |
| >=       | Mayor o igual |
| <=       | Menor o igual |
| IN()     | en una lista  |
| NOT IN() | no inclido    |

## Clase 3

[SQLBolt - Clase 3](https://sqlbolt.com/lesson/select_queries_with_constraints_pt_2)

### Operadores de COMPARACIÓN ALFABÉTICOS:

| Operador | Acción                                            |
| -------- | ------------------------------------------------- |
| =        | exactamente Igual                                 |
| != o <>  | exactamente Distinto                              |
| LIKE     | Igual                                             |
| NOT LIKE | Distinto                                          |
| %        | se usa para buscar una cadena dentro de otra      |
| \_       | se usa para buscar una letra dentro de una cadena |
| IN()     | si la cadena existe en una lista                  |
| NOT IN() | si una cadena no esta en una lista                |

## Clase 4

[SQLBolt - Clase 4](https://sqlbolt.com/lesson/filtering_sorting_query_results)

### DISTINCT

Hace una distinción, esto queire decir que, si filtramos y tenemos varios resultados con el mismo dato supongamos el mismo nombre, lo que hace es mostrar solo uno.

```sql
SELECT DISTINCT nombre, año, …
FROM tabla
WHERE año > 2010;
```

> Sí hay más de un dato que coincida se mostrará solo uno.

### ORDER BY

nos permite una vez hecho el filtro, tomar una columna como referencia y ordenar de manera ASC (ascendente) o DESC (descendente) la información

```sql
SELECT nombres, años
FROM personas
WHERE año < 2000
ORDER BY año ASC
```

> la información se mostrará de menor a mayor, esto también funciona para las letras.

### LIMIT y OFFSET

- Limit se usa para limitar el resultado es decir por ejemplo limitar los 5 primeros.

```sql
SELECT nombres, años
FROM personas
WHERE año < 2000
ORDER BY año ASC
LIMIT 5 OFFSET 0
```

- Ahora si necesitamos que me muestre los 5 siguientes usamos offset para que los 5 anteriores no aparezcan

```sql
SELECT nombres, años
FROM personas
WHERE año < 2000
ORDER BY año ASC
LIMIT 5 OFFSET 5
```

> Clase 5 fue repaso [SQLBolt - Clse 5](https://sqlbolt.com/lesson/select_queries_with_joins)

## Clase 6

[SQLBolt - Clase 6](https://sqlbolt.com/lesson/select_queries_with_joins)

# JOINS

Se trata de relaciones entre tablas, en las cuales podremos extraer datos de varias tablas y mostrarlos todos juntos. Existen muchos tipos de joins.

![joins](https://miro.medium.com/v2/resize:fit:1400/0*rFMChX4SAmQ9RzF9.png)

- **Inner Join:** Es, si se quiere, el más importante de los joins, permite traer datos de dos tablas diferentes donde ambos coinciden.
- **Full Outer Join:** En este se traen todos los datos sin importar si algunos no tienen coincidencias.
- **Full Outer Join excludding inner:** Trae todos los tados que no tienen coincidencias.
- **Left y Right Join:** Trae la información solo de la tabla izquierda o de la derecha, sin importar que tenga coincidencias en la otra tabla, pero si las tiene las trae.
- **Left and Right Join Excludding inner:** Trae solo los datos de las tablas izquierdas o derechas que no tengan coincidencias.

#### Ejemplo:

Tabla Autos:
| id | marca | modelo | año |
| -------- | --------- | ------ | ---- |
| 1 | Vokswagen | GOL | 2011 |
| 2 | Renault | CLIO | 2015 |
| 3 | Peugeot | 408 | 2011 |
| 4 | Vokswagen | Voyage | 2008 |
| 5 | Renualt | Suran | 2007 |

Tabla Propietario:
| id |Nombre| id_auto |
|-------|-------------------|-----------|
| 1 | Gonzalo García | 2 |
| 2 | Mariana Rodríguez | 4 |
| 3| Roberto Almada | 1|

```sql
SELECT nombre, marca, modelo
FROM propietario
INNER JOIN autos on id_auto = id
```

## Clase 7

[SQLBolt - Clase 7](https://sqlbolt.com/lesson/select_queries_with_outer_joins)

# OUTER JOINS

Los OUTER JOINS nos permitirán traer datos incompletos de las tablas, estos pueden ser:

- LEFT JOIN: muestra todos los datos de la tabla de la izquierda, sin importar que en la otra tabla no haya datos, en el ejemplo anterior podría tener clientes que no tengan autos y me mostraría todos los clientes y sus autos y en el caso de no tener auto me los mostraría igual con el campo vacío.
- RIGHT JOIN: es lo inverso del anterior, mostraría todos los autos con y sin propietario.
- FULL JOIN: muestra todo propietarios con autos, propietarios sin auto y autos sin propietarios.

## Clase 8

[SQLBolt - Clase 8](https://sqlbolt.com/lesson/select_queries_with_nulls)

# NULLS

En lo posible es apropiado evitar los valores nulos en las bases de datos ya que son dificiles de trabajar.
Lo apropiado como alternativa a este tipo de datos nulos es tener un dato que lo represente según el tipo de datos que haya en el campo. Ejemplo: si el campo tiene un tipo de dato String, guardamos una string vacía, o si el dato es de tipo número, guardamos un 0.
Existen casos donde no pueden ser evitados los nulls, por lo tanto podríamos chequearlos dentro de las clausulas `WHERE`, con el comparador `IS NULL` o `IS NOT NULL`.

## Clase 9

[SQLBolt - Clase 9](https://sqlbolt.com/lesson/select_queries_with_expressions)

# Consultas con Expresiones

Con el fin de obtener resultados más concretos en las tablas, podriamos realizar consultas incluyendo opéraciones matemáticas, lo que nos ayudaría a conseguir resultados inmediatos.  
Estas columnas podrían utilizar métodos tanto para números como así tambien para String o Date.

> Cada motor de bases de datos tiene su propio formato para esto así que sería apropiado consultarlo en la documentación.

Cabe destacar que estas consultas con datos fabricados a través de expresiones matemáticas, son complejos de leer cuando se presentan en una tabla, por lo tanto es apropiado renombrar la nueva columna con la clausula `AS`.  
A su vez las expresiones matemáticas no solo permiten fabricar nuevas columnas sino también permiten ralizar filtros dentro del `WHERE`.

Ejemplos

TABLA: alumnos  
|apellido_nombre| trimestre_1 | trimestre_2 | trimestre_3|
|-----------------|-------------|-------------|------------|
| Ramírez, José | 5.5 | 6.8 | 4.5 |

```sql
SELECT apellido_nombre, (trimestre_1 + trimestre_2 + trimestre_3) / 3 AS Promedio FROM alumnos;
```

Esta consulta arrojará el siguiente resultado

| apellido_nombre | promedio |
| --------------- | -------- |
| Ramírez, José   | 5.6      |

## Clase 10

[SQLBolt - Clase 10](https://sqlbolt.com/lesson/select_queries_with_aggregates)

# Consultas con Agregados

Estas consultas permiten obtener diferentes resultados como podrían ser totales, promedios, mínimos o máximos de una columna determinada.
Para ello contamos con diferentes funciones que podemos utilizar en la consulta.
La estructura de estas consultas son de la siguiente manera:

```sql
SELECT sum(cantidad) AS total_stock
FROM productos
WHERE cantidad > 0;
```

### Funciones de Agregación

| Nombre de la Función       | Descripción                                                                                                                                                                                                                  |
| -------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| COUNT(\*) y COUNT(columna) | Una función común que se utiliza para contar el número de filas del grupo si no se especifica ningún nombre de columna. De lo contrario, cuente el número de filas del grupo con valores no NULL en la columna especificada. |
| MIN(columna)               | Encuentra el valor mínimo en la columna especificada                                                                                                                                                                         |
| MAX(columna)               | Encuentra el valor máximo en la columna especificada                                                                                                                                                                         |
| AVG(columna)               | Encuentra el valor promedio en la columna especificada                                                                                                                                                                       |
| SUM(columna)               | Encuentra el valor total de la columna especificada                                                                                                                                                                          |

## Clase 11

[SQLBolt - Clase 11](https://sqlbolt.com/lesson/select_queries_with_aggregates_pt_2)

# Consultas con Agregados pt 2

Cuando ejecutamos una consulta y utilizamos el `GROUP BY` con la intención de agrupar los resultados, nos encontramos que no podremos filtrar más, ya que el `GROUP BY` se ejecuta si o si luego del `WHERE`, por suerte SQL nos permite utilizar la clausula `HAVING` luego del `GROUP BY` para realizar este filtro.
Las clasulas `HAVING` son escritas de la misma forma que las `WHERE`.

## Clase 12

[SQLBolt - Clase 12](https://sqlbolt.com/lesson/select_queries_order_of_execution)

# Órden de Ejecución de una Consulta

El órden de ejecución de las consultas son muy importantes ya que es lo que le da coherencia a la consulta y que permite que SQL pueda funcionar correctamente.  
En este contexto, podremos decir que el orden es el siguiente:

1. `SELECT`: es el que nos permitirá seleccionar la columa que necesitamos operar.
2. `DISTINCT`: Permite hacer distinciones entre los datos y limitar los resultados repetidos.
3. `FROM`: Indica de que tabla viene dicha columna.
4. `JOIN`: indica si vamos a unir la tabla con otra este puede ser `INNER JOIN`,`OUTER JOIN`, `RHIGT/LEFT JOIN`, `FULL JOIN`, etc.
5. `ON`: Este simpre viene enganchado al `JOIN`, y determina una condición de la forma en que las tablas van a vincularse.
6. `WHERE`: Plantea una condición para poder filtrar la tabla.
7. `GROUP BY`: utilizada para determinar cómo se agruparán los datos en la tabla generada.
8. `HAVING`: Funciona como un `WHERE`, pero una vez utilizado el `GROUP BY`.
9. `ORDER BY`: Permite ordenar los datos, es decir permite mostrarlos de forma ascendente o descendente, etc.
10. `LIMIT` y `OFFSET`: permiten limitar los datos de desplegados en las tablas, y a su vez, permite determinar desde que dato comenzar a mostrar.

## Clase 13

[SQLBolt - Clase 13](https://sqlbolt.com/lesson/inserting_rows)

# Insertar Registros en las Tablas

A la hora de insertar nueva información en una tabla debemos tener en cuenta que una tabla es una entidad y esta tiene atributos que deben ser respetados.  
Para ello debemos respetar un _esquema_, el cual describe la estructura de una tabla, esto quiere decir que determina, el orden y los tipos de datos admitidos en cada campo de la tabla.  
Esta estructura es lo que le permite a las bases de datos gozar de eficiencia.
Una vez claro esto pasemos al siguiente ejemplo:

**Tabla: autos**
|id|marca|modelo|año_fabricacion|
|--|-----|------|---------------|
|1 |VW | GOL | 2011|

Si queremos insertar nueva información en esta tabla debemos reconocer el esquema, donde id es un numero autoincremental, marca es _String_, modelo es _String_ y año de fabricación es un _Integer_.

## Insert

esta clausula, nos permite insertar información en una tabla, de la cual previamente conocemos el esquema. Para ello debemos utilizar la siguiente sintaxis:

```sql
INSERT INTO nombre_de_la_tabla
VALUES (valorA1, valorA2, valorA3),
       (valorB1, valorB2, valorB3);
```

> En este ejemplo, se muestra que no solo podemos ingresar un solo registro, sino que podríamos cargar varios registros siempre y cuando estos estén entre parentesis y separados por comas.
> Siguiendo el ejemplo anterior:

```sql
INSERT INTO autos
VALUES ('Toyota', 'Hillux', 2020),
       ('Peugeot', '308', 2018);
```

¿Qué hacemos si tenemos información incompleta y necesitamos igual guardarla en la tabla?

Para ello debemos declarar cuales serán las columnas a rellenar.

```sql
INSERT INTO nombre_de_la_tabla
(columna2, columna3)
VALUES (valorA,valorB),
       (valorA2, valorB2);
```

Siguiendo el ejemplo anterior:

```sql
INSERT INTO autos
(marca, modelo)
VALUES ('Toyota', 'Hillux'),
       ('Peugeot', '308');
```

> Es preciso siempre declarar cuales son las columnas aunque sean todas ya que nos permitirán un mejor manejo de la tabla.

Cabe aclarar además que no solo valores pueden ser insertados, sino tambien operaciones matemáticas.

## Clase 14

[SQLBolt - Clase 14](https://sqlbolt.com/lesson/updating_rows)

# Actualizar registros

Así como insertar nueva información en una tabla, actualizarla o modificarla también es una acción que podemos realizar dentro de una tabla. Esta acción la debemos realizar a través de consultas.  
Para ello debemos usar la instancia `UPDATE` y especificar los datos a actualizar nombrando la columna que vamos a actualizar y el valor que esta va a tener dentro de la instancia `SET`. Además es sumamente importante que pongamos una condición y para ello usaremos un `WHERE`.

```sql
UPDATE tabla
SET columna1 = dato1,
    columna2 = dato2,
    columna3 = dato3
WHERE condición
```

Por ejemplo si queremos modificar un auto en la tabla autos debemos hacer lo siguiente:

```sql
UPDATE autos
SET marca = 'Chevrolet',
    modelo = 'Corsa',
    año_fabricacion = 2016
WHERE id = 1
```

> De esta manera modificaremos la información del primer registro ya que el id conincide con el primer auto.

> Debemos destacar que si no nombramos una columna esta no se verá modificada.

## Clase 15

[SQLBolt - Clase 15](https://sqlbolt.com/lesson/deleting_rows)

# Eliminar Registros

En el caso de la eliminación de registros, es mucho mas sensillo que la actualización o la inserción de nueva información.  
Solo con `DELETE` y una condición en `WHERE`, lograremos este propósito.

```sql
DELETE tabla
WHERE condición;
```

> **EXTREMADAMENTE IMPORTANTE**  
> En el caso de no colocar un `WHERE` y ejecutar la consulta, toda la información de nuestra tabla será eliminada completamente.

## Clase 16

[SQL Bolt - Clase 16](https://sqlbolt.com/lesson/creating_tables)

# Crear Tablas

Cuando tenemos nuevas entidades y relaciones para almacenar información, tendremos la posibilidad de crear nuevas estructuras de tablas usando una instancia llamada `CREATE TABLE`.

Definiremos la nueva tabla según el esquema de cada columna

```sql
CREATE TABLE IF NOT EXISTS tabla (
 nombre_columna TipoDeDato restricción DEFAULT valor_por_defecto,
 nombre_columna2 TipoDeDato2 restricción2 DEFAULT valor_por_defecto2,
);
```

### Tipos de datos que acepta una columna

| Tipo de Dato       | Descripción                                                                                                              |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------ |
| INTEGER            | Almacenan número enteros                                                                                                 |
| BOOLEAN            | Almacenan valores 0 o 1                                                                                                  |
| FLOAT, DOBLE, REAL | Diferentes tipos de números, siempre con punto decimal                                                                   |
| CHARACTER, VARCHAR | se refiere a cadenas de string con un largo determinado                                                                  |
| TEXT               | Almacena cadenas de texto                                                                                                |
| DATE DATETIME      | Almacena fechas y fechas con horas, cuidado con esto ya que puede traer problemas al manipular diferentes zonas horarias |
| BLOB               | se utiliza para almacenar datos binarios                                                                                 |

### Restricciónes en las tablas

Se refiere con esto a restricciónes comunes que podremos tener a la hora de construir algunas de los campos de la tabla.

| Restricción       | Descripción                                                                                                                                       |
| ----------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| PRIMARY KEY       | determina que los valores de esta columna deben ser únicos y se utilizan para identificar un registro.                                            |
| AUTOINCREMENT     | se utiliza en valores INTEGER, para hacer que se incrementen automaticamente con cada nuevo registro.                                             |
| UNIQUE            | indica que el valor insertado debe ser único en la columna, la diferencia con la PRIMARY KEY es que no necesariamente debe ser una clave primaria |
| NOT NULL          | hace referencia a que el valor no puede ser nulo                                                                                                  |
| CHECK(expression) | se asegura de chequear el valor insertado a través de una expresión, por ejemplo si necesitamos que solo se inserten valores mayores a 500        |
| FOREING KEY       | es una clave que permite enlazar una tabla con otra, se usa para cruzar datos entre tablas.                                                       |

### Ejemplo

```sql
CREATE TABLE seguros (
   id_seguros PRIMARY KEY,
   nombre TEXT,
   categoria INTEGER,
);
```

## Clase 17

[SQL Bolt - Clase 17](https://sqlbolt.com/lesson/altering_tables)

# Alterar Tablas

Como muchas veces la información es dinámica, y los esquemas que desarrollamos para nuestras tablas pueden verse alterados, es probable que muchas veces necesitemos cambiarlos, añadiendo o quitando columnas a nuestro esquema.

## Añadir columnas

Se trata de un procedimiento similar al de la creación de columnas cuando creamos tablas, pero con la diferencia que en algunos motores de bases de datos podemos especificar su posición.

```sql
ALTER TABLE tabla
ADD nombreDeColumna tipoDeDato Restricción
DEFAULT valorPorDefecto;
```

De esta manera quedaría agregada una columna a la tabla.

## Quitar Columnas

Es posible también quitar o remover una columna, sin embargo no todos los motores de bases de datos soportan esto por lo que obligan a creat una nueva tabla con el nuevo esquema, migrar toda la información y luego eliminar la tabla vieja.
Sí este no es el caso un ejemplo sería:

```SQL
ALTER TABLE tabla
DROP columna
```

## Renombrar una tabla

También es posible renombrar toda la tabla, para ello utilizaremos la clausula `RENAME TO`.

```sql
ALTER TABLE tabla
RENAME TO nuevoNombre
```

## Clase 18

[SQL Bolt - Clase 18](https://sqlbolt.com/lesson/dropping_tables)

# Desechar una Tabla

En algun raro caso podrias necesitar elimiar una tabla con toda su información. Esto es posible, aunque no recomendable, gracias a la clausula `DROP TABLE`. Esto parecería sensillo pero pensemos que si nuesta base de datos es muy grande y tenemos varias tablas que dependen unas de otras, eliminar una tabla requerirá de un trabajo más arduo ya que necesitaremos actualizar las demás tablas para que dejen de depender de la tabla que deseamos desechar.

```sql
DROP TABLE IF EXISTS tabla;
```

## Clase 19

[SQL Bolt - Clase 19](https://sqlbolt.com/topic/subqueries)

# Subconsultas

Las subconsultas, nos permitirán realizar consultas dentro de otras consultas. Se trata de consultas más pequeñas que se ejecutan antes de la consulta principal y solo sirve para recuperar datos.  
Podemos clasificar las subconsultas de acuerdo a su ubicación:

- Subconsultas en el SELECT
- Subconsultas en el WHERE
- Subconsultas en el FROM
- Subconsultas en el HAVING

También las podremos clasificar según su nivel

- 1er nivel: se encuentran dentro de las consultas
- 2do nivel: se encuentran dentro de una subconsulta

Por último podremos clasificarlas según su correlación con la tabla principal:

- Correlacionales
- No Correlacionales

> Vamos a emplear la clasificación según su ubicación.

### Subconsultas dentro del SELECT

Como su nombre lo dice son subconsultas que se realizan para traer datos dentro del select. Funcionan parecido a un JOIN y si es apropiado es mejor siempre usar un JOIN.

Ejemplo:

```sql
SELECT columna1, columna2,
(SELECT columna1B FROM tabla2 WHERE tabla2.ID = columna1) AS columna3
FROM tabla1;
```

> Esta consulta por ejemplo podria verse reflejada así

```sql
SELECT id_auto, marca, modelo,
(SELECT nombre FROM propietarios WHERE autos.id_propietario = id_propietario) AS nombre
FROM autos;
```

Esto daría el mísmo resultado que haciendo un INNER JOIN entre las dos tablas

```sql
SELECT id_autos, marca, modelo, nombre
FROM autos
INNER JOIN propietarios ON id_autos = id_propietarios;
```

### Subconsultas en el WHERE

Estas sirven para filtrar, no devuelven datos, estas son las más utilizadas.

```sql
SELECT columna1, columna2
FROM tabla1
WHERE (SELECT columna1B FROM tabla2) condición;
```

```sql
SELECT id_autos, marca, modelo
FROM autos
WHERE (SELECT nombre FROM propietario) != 'Carlos';
```

> Estas subconsultas funcionan también en el HAVING

### Subconsultas dentro del FROM

Estas subconsultas permitirán extraer información de tablas creadas en el momento, es útil si solo queremos extraer información mínima de una tabla y no necesitamos todo el esquema.

```sql
SELECT columna1, columna2
FROM (
    SELECT columna1, coumna2
    FROM tabla1
    WHERE condición
    )
```

## Clase 20

[SQL Bolt - Clase 20](https://sqlbolt.com/topic/set_operations)

# UNION, INTERSECTION & EXCEPTIONS

Esta clausula, permite la union de dos columnas provenientes de diferentes consulta, la particularidad de `UNION` es que no muestra resultados repetidos, para lograr mostrar resultados repetidos usaremos `UNION ALL`

```SQL
SELECT columna1, columna2
FROM tabla
UNION / UNION ALL / INTERSECT / EXCEPT
SELECT columna1B, columna2B
FROM tabla2
ORDER BY columna1 DESC
LIMIT 5
```

> Debemos recordar que la unión de las tablas se lleva a cabo luego del `ORDER BY` y del `LIMIT`.

No es muy habitual usar las uniones, pero si tenemos datos en dos tablas diferentes que no pueden ser procesadas juntas, este método nos brinda la alternativa para hacer multiples consultas a una base de datos.

## Clase 21

# Cardinalidad

Cuando Trabajamos con bases de datos, debemos tener en cuenta que la información debe fluir. La cardinalidad nos determina como es la relación entre entidades. Esta relación es siempre tenida en cuenta para gestionar la información.

## Tipos de cardinalidad

Encontramos en la cardinalidad que tenemos varios tipos, lo que nos ayuda a entender como debe fluir la información entre tablas, esta relación se hace a través de las calaves tanto **Primarias** como **Foraneas**

- **Uno a uno (1:1)**: en este tipo de cardinalidad un registro en una tabla se relaciona directamente solo con uno de otra tabla.
- **Uno a muchos (1:n)**: Este es el más típico donde un registro de una tabla se relaciona con varios de otra tabla.
- **Muchos a Muchos (n:m)**: Es en este tipo donde muchos registros de una tabla, tienen relación con muchos registros de otra tabla.

## Diagrama Entidad - Relación

![Diagrama entidad Relación](https://upload.wikimedia.org/wikipedia/commons/f/f6/Ejemplo_Diagrama_E-R_extendido.PNG)

Sí miramos el diagrama, veremos que las relaciones se determinan por acciones, donde se ven las relaciones (1:n) y (n:m), un cliente realiza muchos pedidos, con lo cual todos los pedidos deben tener solo un cliente y no mas, esta es la relación (1:n). En el caso de los pedidos pueden estar conformados por varios artículos, y estos artículos pueden repetirse sin importar la cantidad de pedidos esta es una relación (n:m).

## Notació de Martin

![Notación de Martin](https://d2slcw3kip6qmk.cloudfront.net/marketing/pages/chart/erd-symbols/ERD-Notation.PNG)

En la imagen anterior se ve el direccionamiento de las relaciones:

- **Uno**: desde este punto sale uno o llega uno
- **Many**: Muchos, salen o llegan muchos.
- **Uno y solo Uno**: llega o sale uno o solo uno.
- **Cero o uno**: no llega ninguno o uno.
- **Uno o Muchos**: llega o sale uno o muchos.

## Clase 22

# Normalización de una Base de datos

la normalización es un proceso que se realiza a la hora de diseñar una base de datos con el fin de eliminar algunas anomalías que pudieran existir, promover buenas practicas de diseño y hacer que las consultas sean más eficientes.

### cosas a tener en cuenta para normalizar una base de datos

- Identificar las entidades de forma apropiada y sus atributos más relevantes
- Diseñar las tablas y sus relaciones de forma certera.
- identificar claves primarias y foraneas
- identificar dependencias
- normalización progresiva.

## Formas de normalización.

- **1st Normal Form**: Esta forma consiste en evitar campos complejos y busca garantizar que no haya valores repetidos en una fila para una misma clave primaria. Ejemplo: que dentro de una sola fila no haya dos veces nombre, y que dentro de nombre no esté el nombre y el apellido sino que estos esten en dos atributos separados.

- **2nd Normal Form**: Esta forma normalizadora busca evitar la redundancia en los datos, evitando que cada atributo que no sea una clave dependa de una clave primaria.

- **3rd Normal Form**: Esta forma normalizadora busca promover que un atributo no dependa de otro que no sea una clave primaria.

- **4th Normal Forma**: En esta Forma se intenta evitar la redundancia y las anomalias de actualización, promoviendo la utilización de claves primarias compuestas.

- **5th Normal Form**: Se asegura de que no haya dependencia de unión entre atributos, evita que un atributo depende de la unión de atributos de otra tabla.

## Clase 23

# Índices

Son utilizados para mejorar el rendimiento en las consultas. Podemos ver varios tipos de índices, **Índices Primarios o de clave primaria**, **Índices Comunes**, **Índices Unicos**, **Índices Compuestos**.
Estos son de utilidad cuando realizamos repetidas búsquedas o filtrados sobre un mismo campo.
Los índices tienen la desventaha de que consumen muchos recursos y disminuyen el rendimiento en la operaciones de escritura y el mantenimiento de las bases de datos.

- **Índices primarios**: Son las Primary Key las cuales permiten indexar las tablas.
- **Índices Comunes**: Es un índice creado sobre un campo o atributo.
  `CREATE INDEX nombre ON tabla (campo)`
- **Índice Unico**: Este índice no permite campos repetidos.
  `CREATE UNIQE INDEX nombre ON tabla (campo)`
- **Índice Compuesto**: Crea un índice compuesto por dos campos, no permite duplicados.
  `CREATE UNIQUE INDEX nombre ON tabla (campo, campo)`

Estos índices pueden ser facilmente eliminados `DROP INDEX nombre`

## Clase 24

# Vistas

las vistas tienen la funcion de "Guardar" una consulta que realizamos frecuentemente, por ejemplo si frecuentemente realizamos una consula que nos muestra cierca cantidad de datos, podremos guardar esta consulta como vista. Una vista actua sobre una consulta.

### Cración de una vista

```SQL
CREATE VIEW [nombre_de_vista] AS
SELECT columna1, columna2
FROM tabla
WHERE condición
```

De esta manera cada vez que hagamos una consulta sobre la vista nos traerá los datos que le encomendamos

```sql
SELECT * FROM [nombre_de_vista]
```

Podemos eliminar la vista sensillamente de la siguiente manera  
`DROP VIEW [nombre_de_vista]`

## Clse 25

# Transacciones

Se refiere a cambios que se realizarán en las bases de datos, utilizar transacciones, nos permitirá por ejemplo volver atras con las operaciones, deshacer cambios si es necesario.  
Comenzar una tranacción es sensillo solo se debe declarar `BEGIN TRANSACTION` y seguidamente realizar la consulta.
De esta manera estaríamos abriendo una transacción.  
En el caso de necesitar deshacer los cambios por cualquier motivo, podremos hacerlo a través de la clausula, `ROLLBACK`.

En el caso de querer dejar acentado los cambios es necesario hacerlo a través de una clausula `COMMIT`, donde se cerraría la transacción.

```sql
BEGIN TRANSACTION
UPDATE tabla
SET columna1 = dato1,
    columna2 = dato2,
    columna3 = dato3
WHERE condición
COMMIT / ROLLBACK
```
