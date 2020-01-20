Tecnologías Usadas para el desarrollo del proyecto:

La aplicación se encuentra bajo la versión 2.2 de .net core.
El servicio Web se desarrolló utilizando REST como arquitectura.
Entity Framework Core para la parsistencia de datos en Base de datos.
Se usó ASP.NET CORE como para el Web (UI).
SQL Server como provedor de base de datos para los momentos en que el servicio externo no este disponible, 
como también cuando se esten consumiendo los api's interno. 

Los excepciones que ocurran se muestran en consola y también se guardan en el Event Viewer donde se encuentre publicado, el servicio Web y  el cliente Web UI.

Requerimientos a tomar en cuenta para ejecutar la aplicación solución:

Se necesita un equipo que contenga visual studio 2019 version 16.2.0
En el appsettings.development(En caso de utilizar desde Visual Studio) o appsettings.json (Servidor Web, ej: IIS) del WebApp debe colocarse la URL con el puerto correspondiente del servicio Web (GNB.Sales.WebService).
Se necesita tener instalado un equipo que tenga SQL Server instalado y Correr los scripts(Create Rates y Creates Transactions).
Para ejecutar la aplicación se recomienda publicar el proyecto de Servicio Web(GNB.Sales.WebService) junto a la aplicación web(GNB.Sales.WebApp). 
En caso contrario la aplicación web usará el plan b y utilizará la información que este cargada en la base de datos.
