# PC_ 
1.	¿Qué es un servidor HTTP?
programa informático que procesa una aplicación del lado del servidor, realizando conexiones bidireccionales o unidireccionales y síncronas o asíncronas con el cliente y generando o cediendo una respuesta en cualquier lenguaje o aplicación del lado del cliente.


2.	¿Que son los verbos HTTP? Mencionar los más conocidos
GET: Obtiene el recurso indicado. Es el método que se utiliza cuando se pide el contenido de una página web, por ejemplo.
HEAD: Similar a GET, pero no se obtiene el cuerpo de respuesta, únicamente los metadatos de la cabecera.
POST: añade datos al servidor. Siempre es un método de creación.
PUT: es una solicitud para almacenar la entidad suministrada en el URI indicado. Si la entidad no existe, se crea. Si la entidad existe, se actualiza.
DELETE: elimina el recurso indicado.
TRACE: devolverá la misma información que se ha enviado en la solicitud. Es una especie de eco. Sirve para comprobar si la solicitud se ha visto modificada por servidores intermedios.
OPTIONS: Devuelve los métodos HTTP soportados por el servidor para la URL especificada.
CONNECT: Convierte la solicitud en un tunel TCP/IP. Normalmente se usa para crear comunicaciones HTTPS a través de proxys HTTP sin encriptación.
PATCH; Aplica modificaciones parciales al recurso especificado.

3.	¿Qué es un request y un response en una comunicación HTTP? ¿Que son los headers?
•	Request: Una solicitud que genera el navegador con la pagina para poder interactuar entre si
Estructura
Una línea de request para obtener el recurso, por ejemplo un request con el método GET /content/page1.html está requiriendo el recurso llamado /content/page1.html del servidor
Encabezados. Indican cosas como el lenguaje, codificación, tipo de datos (XML,JSON, etc). (Por ejemplo– Accept-Language: EN).
Una línea vacía.
Un cuerpo del mensaje que es opcional. Entre aplicaciones esta es la parte mas importante. Por ejemplo, yo puedo enviar un XML o un JSON  a otra máquina, y el servidor web interpretara la información que yo le mando.

•	Response: Respuesta que devuelve la pagina al navegador
Estructura
HTTP Status Code (Por ejemplo HTTP/1.1 301 Movido Permanentemente, significa que el recurso requerido fue movido permanentemente y redirigido a otro recurso).
Encabezados. Igual que en el request, describen el contenido del response (Example – Content-Type: html)
Una línea vacía.
Un cuerpo de mensaje, que es opcional. Cuando trabajamos con aplicaciones, aquí puede venir la respuesta en XML u otro formato. Cuando es una página del navegador, contiene el código HTML que forma nuestra página.

•	Header:  Transmiten información acerca del navegador del cliente, de la página solicitada, del servidor, etc. La primera línea es la línea del request, que contiene su información básica


4.	¿Qué es un queryString? (En el contexto de una url)
permiten acceder a páginas web dinámicas con distintas variables consiguiendo así que las páginas web no estén compuestas de decenas de directorios y permitiendo que su estructura esté basada en URLs amigables para el posicionamiento web SEO.


5.	¿Qué es el responseCode? ¿Qué significado tiene los posibles valores devueltos? 
un código de respuesta (similar a los códigos de estado HTTP) que indica si la solicitud de codificación geográfica se ha realizado correctamente o no
•	1xx : Los que empiezan por 100 , son los códigos de mensaje referentes a mensajes informativos a nivel de protocolo HTTP no es típico encontrarselos.
•	2xx: Los que empiezan por 200 son los más habituales ya que indican el cliente ha tenido éxito a la hora de procesar su petición
•	3xx: Son los relativos a redirecciones e indican que el cliente debe realizar alguna acción adicional a la hora de completar de forma correcta la petición.
•	4xx: Esta categoría es la mas odiada y hace referencia a un error que se ha producido desde el cliente al realizar la petición
•	5xx : Estos errores son algo menos habituales y hacen referencia a fallos que se han producido en el lado servidor.

6.	¿Como se envia data en un Get y como en un POST?
GET:  lleva los datos de forma "visible" al cliente (navegador web). El medio de envío es la URL. Los datos los puede ver cualquiera.

POST: consiste en datos "ocultos" (porque el cliente no los ve) enviados por un formulario cuyo método de envío es post. Es adecuado para formularios. Los datos no son visibles.

7.	¿Qué verbo http utiliza el navegador cuando accedamos a una página?
el navegador envía una petición de documento HTML al servidor. Entonces procesa este documento, y envía más peticiones para solicitar scripts, hojas de estilo (CSS), y otros datos que necesite (normalmente vídeos y/o imágenes). El navegador, une todos estos documentos y datos, y compone el resultado final: la página Web. Los scripts, los ejecuta también el navegador, y también pueden generar más peticiones de datos en el tiempo, y el navegador, gestionará y actualizará la página Web en consecuencia. 

8.	Explicar brevemente que son las estructuras de datos JSON y XML dando ejemplo de estructuras posibles
JSON: es un formato ligero de intercambio de datos. Leerlo y escribirlo es simple para humanos, mientras que para las máquinas es simple interpretarlo y generarlo. Está basado en un subconjunto del Lenguaje de Programación JavaScript, Standard ECMA-262 3rd Edition - Diciembre 1999. JSON es un formato de texto que es completamente independiente del lenguaje pero utiliza convenciones que son ampliamente conocidos por los programadores de la familia de lenguajes C, incluyendo C, C++, C#, Java, JavaScript, Perl, Python, y muchos otros. Estas propiedades hacen que JSON sea un lenguaje ideal para el intercambio de datos.
 

XML: El lenguaje de marcado es un conjunto de códigos que se pueden aplicar en el análisis de datos o la lectura de textos creados por computadoras o personas. El lenguaje XML proporciona una plataforma para definir elementos para crear un formato y generar un lenguaje personalizado.
Un archivo XML se divide en dos partes: prolog y body. La parte prolog consiste en metadatos administrativos, como declaración XML, instrucción de procesamiento opcional, declaración de tipo de documento y comentarios. La parte del body se compone de dos partes: estructural y de contenido (presente en los textos simples).
 

9.	Explica brevemente el estándar SOAP
es un formato de mensaje XML utilizado en interacciones de servicios web. Los mensajes SOAP habitualmente se envían sobre HTTP o JMS, pero se pueden utilizar otros protocolos. El uso de SOAP en un servicio web específico se describe mediante la definición WSDL. 

10.	Explica brevemente el estándar REST Full
Es considerada una técnica de arquitectura de software, es decir, un conjunto de principios y patrones de comunicación que ayudan a crear una forma de pensar y construir las APIs. Este tipo de arquitectura se define por un conjunto de restricciones entre los elementos, componentes, conectores y datos usados.

11.	¿Que son los headers en un request? ¿Para qué se utiliza el key Content-type en un header?
Esto sirve por ejemplo para comprobar si un link está operativo (responde) sin necesidad de recuperar todo el contenido, lo cual hace que se puedan hacer chequeos mucho más rápidos que usando get. Content-Type es la propiedad de cabecera (header) usada para indicar el media type (en-US) del recurso. Content-Type dice al cliente que tipo de contenido será retornado


Ejercicio 3

Se puede notar la diferencia del requers en la opcion “Pretty” en la que vemos distibuido a lo largo de cada linea de texto la informacion. Por otro lado en la opcion “Raw” optenemos los datos directamente del enlace que se requiere.

EJERCICIO 5
Explicar que son conceptualmente, qué datos almacenan en forma estándar y cómo se relacionan el resto (algunos no se relacionan entre sí) cada uno de los siguientes objetos de Salesforce:


1.	Lead un potencial cliente que demostró interés en un producto o servicio ofrecido por la marca a través de la interacción con contenidos y otros materiales.(Datos de usuario)
2.	Account cuenta de un cliente (Datos de usuario)
3.	Contact. Cliente ya comvertido con todos sus datos (Datos de usuario)
4.	Opportunity posoble cliente el cual falta informacion para transformar en contacto(Datos de usuario)
5.	Product Producto que la empresa comercia (Datos de producto)
6.	PriceBook lista de productos con sus respectivos precios (Datos de producto)
7.	Quote items conciderados como oportunidad (Datos de producto)
8.	Asset Representa un objeto con valor comercial (Datos de producto)
9.	Case es una pregunta,un feedback o una recomencdacion del cliente 
10.	Article Descipcion en salesforce

EJERCICIO 6
1.![2fb5f9f4-ddab-4a61-bcce-9d52f5083741](https://user-images.githubusercontent.com/86447218/123357157-afd33b00-d52e-11eb-8a90-7d48f7b86304.jpg)


2.![Screen Shot 2021-06-24 at 21 34 07](https://user-images.githubusercontent.com/86447218/123361211-46562b00-d534-11eb-8fba-f4fd62c6284d.png)
![Screen Shot 2021-06-24 at 21 35 08](https://user-images.githubusercontent.com/86447218/123361218-481fee80-d534-11eb-82c9-87e1542c6249.png)
![Screen Shot 2021-06-24 at 21 35 12](https://user-images.githubusercontent.com/86447218/123361223-49e9b200-d534-11eb-93a5-a6b938f4e4df.png)

3. trigger PC on Contact(after insert, after update) {
    List<Opportunity> oppList = new List<Opportunity>();
    
    
    Map<Id,Contact> acctsWithOpps = new Map<Id,Contact>(
        [SELECT Id,(SELECT Id FROM Opportunities) FROM Contact WHERE Id IN :Trigger.New]);
    
   
    for(Contact a : Trigger.New) {
        System.debug('acctsWithOpps.get(a.Id).Opportunities.size()=' + acctsWithOpps.get(a.Id).Opportunities.size());
        
        if (acctsWithOpps.get(a.Id).Opportunities.size() == 0) {
         
            oppList.add(new Opportunity(Name=a.Name + ' Opportunity',
                                       StageName='Prospecting',
                                       CloseDate=System.today().addMonths(1),
                                       Contact Id=a.Id));
        }           
    }
    if (oppList.size() > 0) {
        insert oppList;
    }
}

![Screen Shot 2021-06-24 at 21 52 09](https://user-images.githubusercontent.com/86447218/123362566-83bbb800-d536-11eb-9489-1dadffa791f3.png)


EJERCICIO 7
Responder las siguientes preguntas brevemente sobre:
Soluciones de Salesforce
A.	¿Qué es Salesforce?

Salesforce es una solución de gestión de relaciones con clientes que une empresas y clientes. Es una plataforma CRM integrada que brinda a todos sus departamentos, incluidos marketing, ventas, comercio y servicios, una vista única y compartida de cada cliente.

B.	¿Qué es Sales Cloud?
Sales Cloud es parte del creciente número de paquetes de productos Salesforce que están literalmente 'en la nube'. Estos incluyen Service Cloud, Chatter Cloud, Data Cloud, CRM Social, etc.
C.	¿Qué es Service Cloud?
es la aplicación para atención al cliente número uno del mercado. Implantada directamente en la plataforma de Salesforce CRM

D.	¿Qué es Health Cloud?
Health Cloud permite una conversación personalizada entre el paciente y las entidades sanitarias asociadas.

E.	¿Qué es Marketing Cloud?
es un proveedor de software y servicios de análisis y automatización de marketing digital.
Funcionalidades de Salesforce
A.	¿Qué es un RecordType?
Te permite definir diferentes conjuntos de valores de lista de selección para listas de selección estándar y personalizadas
Los tipos de registro lo ayudan a implementar sus procesos comerciales personalizados

B.	¿Qué es un ReportType?
Un tipo de informe es una plantilla que define los objetos y campos que estarán disponibles para usar en el informe que cree.

C.	¿Qué es un Page Layout?
Diseño de página en Salesforce nos permite personalizar el diseño y organización de detalles y editar páginas de registros en Salesforce. Los diseños de página se pueden utilizar para controlar la apariencia de campos, listas relacionadas y enlaces personalizados en la página de edición y detalle de objetos estándar y personalizados.

D.	¿Qué es un Compact Layout?
El diseño compacto determina qué campos aparecen en el elemento de noticias en tiempo real de Chatter que aparece después de que un usuario crea un registro con una acción rápida.
E.	¿Qué es un Perfil?
Definen cómo acceden los usuarios a objetos y datos y qué pueden hacer en la aplicación
F.	¿Qué es un Rol?
Controlan el nivel de visibilidad que un usuario tiene sobre los datos de su organización.

G.	¿Qué es un Validation Rule?
Contiene una fórmula o expresiones que evalúan los datos en uno o más campos en un registro para cumplir con los estándares y devuelve un valor "Verdadero" o "Falso".

H.	¿Qué diferencia hay entre una relación Master Detail y Lookup?

Master detail: objeto maestro controla ciertos comportamientos del objeto de detalle. Cuando se elimina un registro del objeto maestro, también se eliminan sus registros de detalles relacionados.
Lookup: conecta dos objetos entre sí sin afectar la seguridad y las propiedades de eliminación. Es posible crear una relación intermedia entre objetos agregando relaciones de búsqueda a objetos estándar, personalizados y externos.

La diferencia entre ellos es que master detail controla alobjeto que designamos y look up solo crea una realcion entre ellos

I.	¿Qué es un Sandbox?
Una copia de su base de datos que puede utilizar para probar nuevas ideas.

J.	¿Que es un ChangeSet?
Es cuando se ha iniciado sesión y desea enviarlo a otra organización. Por lo general, usa un conjunto de cambios salientes para las personalizaciones creadas y probadas en un espacio aislado y que luego se envían a una organización de producción.

K.	¿Para qué sirve el import Wizard de Salesforce?
le proporciona cargar los datos en Salesforce. Al usar este asistente, podemos insertar, actualizar y actualizar los registros.

L.	¿Para qué sirve la funcionalidad Web to Lead?
capturar información de los visitantes y almacenar esa información como un nuevo cliente potencial en Salesforce.

M.	¿Para qué sirve la funcionalidad Web to Case?
es un medio por el cual puede publicar una página web simple y no autenticada que permite a sus clientes

N.	¿Para qué sirve la funcionalidad Omnichannel?
es una herramienta que se encuentra dentro de la Consola de Ventas o de Servicio que, una vez habilitada y configurada, envía automáticamente el trabajo a sus usuarios en tiempo real.

O.	¿Para qué sirve la funcionalidad Chatter?
plicación de colaboración en tiempo real de Salesforce que permite a sus usuarios trabajar juntos, comunicarse y compartir información.
Conceptos generales
A.	¿Qué significa SaaS? ¿Salesforce es Saas?
SaaS, o Software as a Service, es una forma de disponibilizar softwares y soluciones de tecnología por medio de la internet, como un servicio. Con ese modelo, su empresa no necesita instalar, mantener y actualizar hardwares y softwares. El acceso es fácil y simples: solo es necesario conexión con la internet.

Salesforces es un Saas 
 

B.	¿Que significa que una solución sea Cloud?
La operacion a ejecutar es meramente en la nube 

C.	¿Que significa que una solución sea On-Premise?
la empresa es la responsable de la seguridad, disponibilidad y gestión del software.

D.	¿Que es un pipeline de ventas?
Es el sistema que produce una fuente de oportunidades comerciales de calidad para que tu equipo pueda convertirlas en clientes reales y así incrementar las ganancias de tu empresa.

E.	¿Que es un funnel de ventas?
forma en que una empresa planea y establece procesos para ponerse en contacto con los diferentes usuarios

F.	¿Qué significa Customer Experience?
Conocimiento del Cliente. Desarrollar herramientas y metodologías para comprender a los diferentes tipos de clientes y analizar la experiencia que estos viven con la compañía.

G.	¿Qué significa omnicanalidad?
es una estrategia que utiliza todos los canales de comunicación de una empresa de forma integrada y sincrónica.

H.	¿Qué significa que un negocio sea B2B?
transacciones comerciales entre empresas, es decir, a aquellas que típicamente se establecen entre un fabricante y el distribuidor de un producto, o entre un distribuidor y un comercio minorista.

I.	¿Qué significa que un negocio sea B2C?
es empleada por firmas comerciales que persiguen llegar de manera directa a un cliente o consumidor final.

J.	¿Qué es un KPI?
es una medida del nivel del rendimiento de un proceso

K.	¿Qué es una API y en qué se diferencia de una Rest API?

API: se utiliza para desarrollar e integrar el software de las aplicaciones
Rest API: significa utilizar una API para acceder a aplicaciones back-end, de manera que esa comunicación se realice con los estándares definidos por el estilo de arquitectura Rest.

La diferencia esque una ocupa el protocolo de Rest mientras que el otro aun no lo involucra


L.	¿Qué es un Proceso Batch?
la ejecución de un programa sin el control o supervisión directa del usuario que se denomina.

M.	¿Qué es Kanban?
es un sistema de información que controla de modo armónico la fabricación de los productos necesarios en la cantidad y tiempo necesarios

N.	¿Qué es un ERP? ¿Salesforce es un ERP?
son los sistemas de información gerenciales que integra
n y manejan muchos de los negocios asociados con las operaciones de producción y de los aspectos de distribución de una compañía en la producción de bienes o servicios.

Salesforce es un ERP






Imagenes
![Screen Shot 2021-06-24 at 19 11 12](https://user-images.githubusercontent.com/86447218/123350152-008f6780-d520-11eb-8579-b24375a35a09.png)
![93351ee2-f5a4-4c50-9cbd-368444c01f56](https://user-images.githubusercontent.com/86447218/123357159-b06bd180-d52e-11eb-8838-f4e16d453496.jpg)
![28ca060d-b723-4db9-a55d-3cd7ff05e15b](https://user-images.githubusercontent.com/86447218/123357160-b06bd180-d52e-11eb-993c-b0b3a333a7ad.jpg)
![08a124e9-3b40-4120-b452-d48f37c303ae](https://user-images.githubusercontent.com/86447218/123357161-b1046800-d52e-11eb-9a0e-21e8b6411114.jpg)
![2fb5f9f4-ddab-4a61-bcce-9d52f5083741-1](https://user-images.githubusercontent.com/86447218/123357164-b19cfe80-d52e-11eb-8967-196de93c98f6.jpg)
![Screen Shot 2021-06-24 at 9 58 21](https://user-images.githubusercontent.com/86447218/123357261-d42f1780-d52e-11eb-902c-9a04729c980e.png)



