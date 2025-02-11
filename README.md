# Máquinas-Virtuales-Amazon-EC2
## Informe
#### INTRODUCCIÓN

A medidad que la tegnología avanza, se crean constantemente nuevos sistemas operativos cada uno con caracterìsticas propias y mejores a las ya existentes, por tal motivo se   busca siempre estar al dìa con ello porque resultarìa incomodo adquirir  varios dispositivos con el fin de probar cada sistema es ahí en donde se genera la idea de utilizar **Máquinas Virtuales**, ya que son versatiles al momento de trabajar en ellas, permite trabajar con varios sistemas operativos en un mismos ordenador, ejecutar un  programa antiguo utilizar aplicaciones que no sean permitidas en el sistema  operativo propio entre otras cosas, en ese sentido este tutorial  busca  es investigar la generación de 
**Máquinas Virtuales** en la plataforma Amazon EC2  pues funciona como nube en la que se puede almacenar varias máquinas virtuales de varios sistemas operativos para  hacer   uso de ellas en cualquier momento y desde cuaqluier lugar. 

#### OBJETIVOS
**Objetivo general**

Generar máquinas virtuales, mediante la plataforma Amazon EC2,utilizando esta herramienta de manera adecuada con la finalidad de tener en esta plataforma, otro sistema operativo y usarlo en cualquier momento y desde cualquier parte del mundo.

**Objetivos Especifícos**

* Crear una cuenta en la plataforma Amazon Ec2, conocer todos los beneficios que ofrece y hacer uso de ella
* Desarrollar máquinas virtuales en Amazon EC2, con la finalidad de generar un nuevo sistema operativo  y utilizarlo en cualquier momento y parte del mundo.

## Tutorial para Crear Máquinas Vrtuales con Amazon EC2 

**Máquina Virtual**

 Es un software que permite emular el funcionamiento de un ordenador dentro de otro mendiante el encapsulamiento que aísla a ambos.Puede ejecutar cualquier sistema operativo o programa, sin que nada de lo que suceda en el interior de esa ventana afecte al ordenador que la ejecuta.
Se puede trabajar con varios sistemas operativos al mismo tiempo en un mismo ordenador por ejemplo se podria usar Linux y windows.

   ![Img3MaquinaVirtual.png](https://github.com/CFernanda/Maquinas-Virtuales-Amazon-Ec2/blob/master/imagenenes/Img3MaquinaVirtual.png)  

**CLOUD COMPUTING**

  Cloud computing, o computación en nube, se define como una tecnología que ofrece servicios a través de la plataforma de internet.Se puede acceder a este tipo de serviciosde 
forma  gratuita o de pago, según las necesidades que tenga uno. Este modelo está inspirado en los cajeros automáticos, los que permiten acceder al dinero y servicios disponibles desde cualquier terminal habilitado. Luego esa idea se llevó a la red internet, y es lo que conocemos actualmente como cloud computing. Esta tecnología se destaca por ofrecer todos sus servicios de forma remota a través de esta analogía de "nube virtual", y uno como usuario de este servicio no necesita un dispositivo de última generación para utilizar los servicios de esta nube, ya que todo se ejecuta desde la misma, lo que se traduce en la ausencia de descarga y actualización de software. (Leyton & Fernández, 2010)
                        
   ![Imagen1%20Cloud%20Company.png](https://github.com/CFernanda/Maquinas-Virtuales-Amazon-Ec2/blob/master/imagenenes/Imagen1%20Cloud%20Company.png)  

**Amazon Elastic Compute Cloud Amazon Ec2**

Proporciona capacidad de computación escalable en la nube de Amazon Web Services (AWS). El uso de Amazon EC2 elimina la necesidad de invertir inicialmente en hardware, de manera que  puede desarrollar e   implementar aplicaciones en menos  tiempo. Puede usar Amazon EC2 para lanzar tantos servidores virtuales como  necesite, configurar la seguridad y las redes y administrar   el almacenamiento. Amazon Elastic Compute Cloud  Amazon EC2  le permite escalar hacia arriba o hacia abajo para controlar cambios en los requisitos o picos de popularidad, con lo que se reduce la necesidad de prever el tráfico. (Amazon, 2020)   
            
   ![imagen2AWS.png](https://github.com/CFernanda/Maquinas-Virtuales-Amazon-Ec2/blob/master/imagenenes/imagen2AWS.png) 

**¿Para qué sirve Amazon EC2?**

Amazon EC2 ofrece a sus usuarios la posibilidad de crear entornos informáticos virtuales en la nube. Esto se consigue a través de una interfaz web que se conecta a una imagen de máquina de Amazon. La AMI suele corresponder al sistema operativo que queramos que se ejecute en la máquina virtual o instancia según la terminología usada en Amazon EC2. 

##### Características
* Entornos informáticos virtuales, conocidos como instancias
* Plantillas preconfiguradas para las instancias, conocidas como imágenes de máquina de Amazon (AMI), que empaquetan las partes que necesita para el servidor (incluido el    sistema operativo y el software adicional)
* Varias configuraciones de CPU, memoria, almacenamiento y capacidad de red de las instancias, conocidos como tipos de instancias
* Información de inicio de sesión segura para las instancias con pares de claves (AWS almacena la clave pública y usted guarda la clave privada en un lugar seguro)
* Volúmenes de almacenamiento para datos temporales que se eliminan cuando detiene o termina la instancia, conocidos como volúmenes de almacén de instancias
* Volúmenes de almacenamiento persistente para los datos usando Amazon Elastic Block Store (Amazon EBS), conocidos como volúmenes de Amazon EBS
* Varias ubicaciones físicas para los recursos, como las instancias y los volúmenes de Amazon EBS, conocidas como regiones y zonas de disponibilidad
* Redes virtuales que puede crear que están aisladas lógicamente del resto de la nube de AWS y que, opcionalmente, puede conectar a su propia red, conocidas como nubes privadas   virtuales (VPC)

##### Precios de Amazon EC2

Existen cinco modelos de compra de instancias de Amazon EC2:

* Bajo demanda: Con las instancias bajo demanda, paga por la capacidad informática por hora o por segundo, según las instancias que use.            
* Savings Plans: Es un modelo de precios flexible que ofrece precios económicos por el uso de EC2 y Fargate, a cambio de comprometerse a una cantidad constante de uso (medida en USD/hora) durante el término de 1 o 3 años.
* Instancias reservadas:Las instancias reservadas ofrecen un descuento importante (de hasta el 75 %) en comparación con los precios de las instancias bajo demanda.  
* Instancias de spot: Permiten solicitar capacidad informática sobrante de Amazon EC2 con descuentos de hasta el 90% en comparación con el precio de las instancias bajo demanda. 
* Alojamientos dedicados:Un host dedicado es un servidor físico de EC2 exclusivo para su uso. Los hosts dedicados pueden ayudarle a reducir costos porque le permiten usar sus licencias existentes de software enlazado al servidor, incluidos Windows Server, SQL Server y SUSE Linux Enterprise Server (en función de los términos de su licencia). 

***CAPA GRATUITA***

**12 meses gratis:** Exclusiva para los nuevos clientes de AWS y solo durante doce meses a partir de la fecha de inscripción en AWS. Cuando finalicen los 12 meses de uso gratuito o si el uso de su aplicación supera las capas, tendrá que pagar las tarifas de servicio estándar.

**Gratis para siempre:** No vencen automáticamente al finalizar los 12 meses de la capa gratuita de AWS, sino que están disponibles tanto para clientes ya existentes como para nuevos clientes de AWS de forma indefinida.

**Pruebas:** Son ofertas de pruebas a corto plazo que comienzan desde el momento en que comienza el primer uso. Una vez que vence el plazo, simplemente tendrá que pagar las tarifas del servicio estándar según el uso (consulte la página de cada servicio para obtener información completa sobre los precios).

#### MANUAL DE USUARIO

 Para la Generación de una máquina virtual en la plataforma Amazon EC2  se deben seguir ciertos pasos:
 
 **1) Crear una cuenta en Amazon EC2**
 
 * Se ingresa en  Amazon EC2,  https://aws.amazon.com/es/ec2/., donde aparecerá la siguiente pantalla. 
 
 ![Img4IngresoAmazonEC2.png]( https://github.com/CFernanda/Maquinas-Virtuales-Amazon-Ec2/blob/master/imagenenes/Img4IngresoAmazonEC2.png) 

* En la pantalla anterior damos click en el botón tomate "**Inicie sesion en la consola**", y aparecerá una nueva ventana que nos permitirá ingresar si ya se tiene una cuenta o  crear  nueva, para el caso damos click en "**Crear una cuenta de AWS** "

![Img5IngresoConsola.pn]( https://github.com/CFernanda/Maquinas-Virtuales-Amazon-Ec2/blob/master/imagenenes/Img5IngresoConsola.png) 


* Una vez que se dio click en ese botón se abren 5 tipos de formularios donde pide varios datos que son necesarios para crear la cuenta;
  - **Crear cuenta de AWS** Se ingresa los datos de la cuenta que se creara

  - **Información de contacto** se debe escoger personal, si no perteneces a alguna empresa.
  
  - **Información de pago** se necesita el ingreso de un número de Tarjeta de Crédito, Amazon Ec2 lo útiliza solo para verificar la cuenta, por tal motivo se descuentan $1 sin       embargo a los dos días como máximo se reembolsa ese dinero y de ahí en adelante se puede usar durante 12 meses de forma gratuita. 
  
  - En los dos últimos se realiza la verificación y da el resultado si la creación fue exitosa o no.

 ![Img6formulariocrearcuenta.png]( https://github.com/CFernanda/Maquinas-Virtuales-Amazon-Ec2/blob/master/imagenenes/Img6formulariocrearcuenta.png) 

 ![Img7formularioScrearcuenta.png]( https://github.com/CFernanda/Maquinas-Virtuales-Amazon-Ec2/blob/master/imagenenes/Img7formularioScrearcuenta.png) 

Una vez  creada la cuenta se debe ingresar con el correo y la clave a la plataforma Amazon EC2.
 ![Img8entradaconsola.png]( https://github.com/CFernanda/Maquinas-Virtuales-Amazon-Ec2/blob/master/imagenenes/Img8entradaconsola.png)

**2) Crear una clave de acceso**

 Una vez en la consola se dirige al Botón **Servicios** y ahi escogemos **EC2**
 
  ![Img9Servicios.png]( https://github.com/CFernanda/Maquinas-Virtuales-Amazon-Ec2/blob/master/imagenenes/Img9Servicios.png)
  
  Creamos la Clave de acceso en la sección **Network & Security**, en la pestaña **Keir pairs** se abrira una ventana con las claves ya cradas y para crear una nueva se ingresa   en el botón naranja **Create Key Pair**
  
   ![Img10NetworkSecurity.png]( https://github.com/CFernanda/Maquinas-Virtuales-Amazon-Ec2/blob/master/imagenenes/Img10NetworkSecurity.png)
   
   Se crea una nueva tipo Pem y con el nombre, se descarga un archivo con la clave que se la ocupará para la generación de las Máquinas Virtuales, 
   
   ![Img11CreateKey%20Pair.]( https://github.com/CFernanda/Maquinas-Virtuales-Amazon-Ec2/blob/master/imagenenes/Img11CreateKey%20Pair.png)
   
 **3) Crear la Máquina**
 
 - En la Sección **INSTANCES**, escoger la pestaña Instance y se abrira la ventana con las máquinas ya creadas y para crear una nueva se debe dar click en el botón **"Launch Instance"**
 
 ![Img12Instancias.png](  https://github.com/CFernanda/Maquinas-Virtuales-Amazon-Ec2/blob/master/imagenenes/Img12Instancias.png)
 
- Para crear la nueva Máquina el primer paso es escoger Tipo se distema operativo que necesitemos.

 ![Img13tipoMaquina.png](  https://github.com/CFernanda/Maquinas-Virtuales-Amazon-Ec2/blob/master/imagenenes/Img13tipoMaquina.png)
 
- Se abren ventanas para configurar la máquina virtual como sea de su preferencia.

- Una vez escogidas las características se abre una nueva ventana donde ingresaremos la clave creada en el paso 2.
 Escogemos el nombre de la clave que fue creada,aceptamos los terminos y condiciones y damos click en **Launch Instances**
 
 ![Img14Ingresar%20Key.png]( https://github.com/CFernanda/Maquinas-Virtuales-Amazon-Ec2/blob/master/imagenenes/Img14Ingresar%20Key.png)
 
 - Se abrirá una nueva ventana indicando si fue creada con éxito.
 ![Img15Launch.png]( https://github.com/CFernanda/Maquinas-Virtuales-Amazon-Ec2/blob/master/imagenenes/Img15Launch.png)
 
 - Al terminar se abrirá la ventana  de las características  y nombres de las máquina tanto las creadas como la que recién se creó, en esta verificaremos el estado de la máquina y de aquí se puede  prednerla, detenerla o apagarla.
 
  ![Img16Caracteristicas.png](  https://github.com/CFernanda/Maquinas-Virtuales-Amazon-Ec2/blob/master/imagenenes/Img16Caracteristicas.png )

- La máquina ya esta creada ahora debemos entrar en ella para eso sobre la máquina que deseemos entrar debemos dar click derecho y escoger la opcion **Get Windows Password**
 
 ![Img17Caracteristicas.png](  https://github.com/CFernanda/Maquinas-Virtuales-Amazon-Ec2/blob/master/imagenenes/Img17IngresoMaquina.png )
 
 - Lo siguiente será ingresar la clave de Acceso para la maquina que se vay a ocupar, damos Click en el botón **Descrypt Password** 
 
   ![Img18AccesoconClave.png](  https://github.com/CFernanda/Maquinas-Virtuales-Amazon-Ec2/blob/master/imagenenes/Img18AccesoconClave.png )
  
 -Adicional a eso se debe descargar la Máquina se debe presionar el botón **Connect**, se abrirá otra pantalla y ahí presionar **Download Remote Desktop File** y se descargará la máquina.
 
 ![Img19%20Descargar.PNG ](   https://github.com/CFernanda/Maquinas-Virtuales-Amazon-Ec2/blob/master/imagenenes/Img19%20Descargar.PNG )

- Una vez realizados los anteriores pasos se abrirá una ventana con la contraseña y el usuario para ingresarlos en la Máquina descargada, ambas ventanas se muestran en la siguiente imagen.

![Img20IngresarCreedenciales.png](   https://github.com/CFernanda/Maquinas-Virtuales-Amazon-Ec2/blob/master/imagenenes/Img20IngresarCreedenciales.png)

El sistema operativo en la nueva máquina virtual se carga por no más de 2 minutos.

![Img21conexionescritorioremoto.jpg]( https://github.com/CFernanda/Maquinas-Virtuales-Amazon-Ec2/blob/master/imagenenes/Img21conexionescritorioremoto.jpg)

- Finalmente se ingresa a la máquina virtual como se muestra a continuación.
![Maquina%20Virtual%20Creada.png]( https://github.com/CFernanda/Maquinas-Virtuales-Amazon-Ec2/blob/master/imagenenes/Maquina%20Virtual%20Creada.png)

![PantallaMaquinaVirtual.png)]( https://github.com/CFernanda/Maquinas-Virtuales-Amazon-Ec2/blob/master/imagenenes/PantallaMaquinaVirtual.png)

### BIBLIOGRAFÍA
 * Amazon Web Services. (2020).Recuperado de:[https://docs.aws.amazon.com/es_es/AWSEC2/latest/UserGuide/concepts.html]
 * Microsoft Azure. (2020). Azure. Recuperado de:https://azure.microsoft.com/es-es/overview/
 * Ramirez, I. (25 de Julio de 2016). Xataka. Obtenido de Máquinas virtuales: qué son, cómo funcionan y cómo utilizarlas: https://www.xataka.com/especiales/maquinas-virtuales-que-son-como-funcionan-y-como-utilizarlas
 * Leyton, J., & Fernández, V. (14 de Julio de 2010). Cloud Computing. Obtenido de http://profesores.elo.utfsm.cl/~agv/elo322/1s10/project/reports/cloudcomputing-10s01.pdf


