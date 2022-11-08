# Estructura-de-computadores
Asignatura de tercer curso en el Doble grado de Ingeniería informática y ADE
ETSIINF
# Practica ensamblador 2021
La herramienta que se utiliza en la realización de este proyecto es el simulador del MC88110.
El MC88110 es un microprocesador RISC superescalar que forma parte de la familia 88000 de Motorola. Es capaz de iniciar dos instrucciones cada ciclo de reloj, respetando siempre la apariencia de ejecución secuencial del programa a través del mecanismo de pipeline del secuenciador. Las instrucciones se despachan hacia diez unidades funcionales que trabajan en paralelo.

El simulador del MC88110 que se utiliza en este proyecto permite configurar distintos parámetros de la memoria principal, de las memorias cache de instrucciones y datos y de la CPU.

El proyecto se realizará utilizando el ensamblador nativo del 88110 y empleando la configuración del fichero serie que se incluye en la distribución. Este fichero configura la CPU según los siguientes parámetros:

Cache de datos e instrucciones inhibidas
Memoria de un solo bloque con tiempo de acceso de 10 ciclos.
Ejecución serie.
Ordenamiento de bytes en memoria little-endian.
Modo de redondeo al más cercano.
Este modo de ejecución se invoca en Linux o en Solaris mediante el shellscript mc88100 de la distribución. En el caso de sistemas basados en Windows, se facilita el archivo de órdenes de ejecución mc88100.bat para realizar esa misma labor.
Distribuciones
A continuación se listan las distribuciones disponibles del simulador. Todas ellas contienen los siguientes ficheros:
88110e / 88110e.exe : Programa ensamblador. Permite ensamblar un fichero con un programa ensamblador a un fichero binario que puede leer el simulador.
em88110 / 88110.exe : Simulador del MC88110. Al invocarlo se le deben pasar dos parámetros: el fichero de configuración de la máquina y el fichero que contiene el programa compilado.
serie: Fichero de configuración de un computador serie sin memorias caché.
Además, las versiones para sistemas Linux también contienen:
88110ins: Programa que permite generar o modificar un fichero de configuración.
paralelo: Fichero de configuración de un computador superescalar con memorias caché de instrucciones y datos.
INSTALL: ShellScript que instala la aplicación. Además genera el script mc88110 que invoca al emulador con el fichero de configuración serie. Se invoca con ./INSTALL ó sh INSTALL.
Las distribuciones disponibles del simulador son las siguientes (octubre-2022):
Linux. Versión 1.10 compilada con librerías estáticas para: Linux 64 bits.
Windows. Versión 1.11. Para su ejecución en una ventana MS-DOS: Windows 64b.
