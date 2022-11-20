## Bases de datos de modelos multidimensionales SSAS

Implementando tareas de SSAS

Descargue la base de datos AdventureWorksDW2017 o la versión que vaya acorde al manejador de MS SQL Server que tenga instalado en su máquina.

Importe la BD AdventureWorksDW2014 a MS SQL Server.

Liste todas las dimensiones creadas.

Liste todas las tablas de hechos creadas.

Cree un nuevo proyecto BI (Practice6Cubes) usando Analysis Services de SQL Server Data Tools.

Cree un Data Source para definir la conexión a la BD AdventureWorksDW2014.

Cree un Data Source View seleccionando como tabla de hechos inicial FactInternetSales.

Seleccione las tablas que están asociadas a la tabla elegida en el punto 7.

En el diagrama de Estrella creado por el paso anterior, seleccione la dimensión Customer y cree una nueva columna calculada, que consista de la concatenación del nombre y el apellido separados por un espacio. Llame a esta nueva columna como FullName.

Muestre la data generada en la dimensión Customer y revise la nueva columna creada.

Cree un Cubo, seleccionando como tabla principal FactInternetSales, luego seleccione las dimensiones que se relacionen y mantenga los demás valores por defecto.

Seleccione algunos atributos adicionales de las dimensiones:

De Customer seleccione: FirstName, LastName, FullName y Gender.

De Promotion seleccione: EnglishPromotionName, StartDate, EndDate, MinQty y MaxQty.

De Date seleccione: EnglishDayNameOfWeek, EnglishMonthName, CalendarQuarter, CalendarSemester y CalendarYear. Crear también una jerarquía con los siguientes atributos: DateKey, EnglishMonthName, CalendarQuarter, CalendarSemester y CalendarYear. Ordene los meses y los días de la semana numéricamente.

De SalesTerritory: SalesTerritoryRegion, SalesTerritoryCountry y SalesTerritoryGroup.

De Product: EnglishProductName.

De InternetSales: OrderQuantity y SalesAmount.

Procese el cubo para que el mismo pueda ser implementado y corrido.

![image](https://user-images.githubusercontent.com/86633500/202924732-56b8dc1f-d754-443b-b3d8-86f4152ca780.png)

Aquí podemos ver la ejecución de nuestro Proyecto de Bases de datos de modelos multidimensionales, sin ningún tipo de problema.

![image](https://user-images.githubusercontent.com/86633500/202924869-22c028e6-0ce4-4627-b709-55fffb5fd57d.png)

¿Cuál es la cantidad y total de ventas por sexo? Incluya el sexo en la salida.

![image](https://user-images.githubusercontent.com/86633500/202924907-b9436fd6-bc15-4c77-bd66-5ca14a0aa90c.png)
