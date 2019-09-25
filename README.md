### WEMOS D1 R1 WIFI PROJECT EN VSCODE CON PLATFORMIO Y QNAP QIoT: DHT11 + I2C
Visualización de los datos de temperatura y humedad sobre una pantalla LCD con Wemos D1 R1 
y envio de datos por WIFI a la plataforma QIoT Suite de QNAP 

![](images/20190925_100459.jpg)

![](images/QIoT_results.png)

##### Elementos necesarios:
- NAS QNAP compatible con QioT Suite
- Wemos D1 R1 Wifi
- Protoboard
- Sensor DHT11 de temperatura y humedad
- Pantalla LCD con acople I2C
- Cables

##### Software necesario:
- Visual Studio Code
- Plugin PlatformIO IDE para VSCode
  Ref: http://docs.platformio.org/en/latest/ide/pioide.html
- Plataforma QNAP QIoT Suite configurada https://www.qnap.com/solution/qiot-suite-platform/es-es/

##### Configuración de sensores:
- DHT11 - PIN 7 DIGITAL
- I2C   - PINES D15 (SCL) Y D14 (SDA)

#####  Referencias:
Codigo fuente DTH: https://programarfacil.com/blog/arduino-blog/sensor-dht11-temperatura-humedad-arduino/
Codigo fuente I2C: http://educ8s.tv/arduino-20x4-character-lcd/

Libreria DHT:      https://github.com/adafruit/DHT-sensor-library
Libreria LCD:      https://bitbucket.org/fmalpartida/new-liquidcrystal/downloads

##### Programacion con platformIO en VSCode:

- Configuración librerias:
	![](images/platformIO_libraries.png)

- Configuración placa:
	![](images/platformIO_config.png)

- Salida de la ejecución en el monitor serie:
	![](images/platformIO_serialMonitor.png)

##### Visualizacion en QIoT Suite Lite de QNAP:
Configurar QNAP QIoT Suite Lite paso a paso by @QNAPespana:: https://www.youtube.com/watch?v=Ha2brZSmKJI

##### Configuración en QIoT Suite:
1. Loguearse en el QIoT de QNAP
	<img src="./images/QIoT_login.png" width="60%" height="60%"><br/><br/>

2. Configurar una nueva aplicación IoT
	<img src="./images/QIoT_addApp.png" width="60%" height="60%"><br/><br/>

3. Configurar una nueva Thing de tipo Arduino Yun
	<img src="./images/QIoT_addThing.png" width="60%" height="60%"><br/><br/>

4. Añadir los recursos Temperatura y Humedad al Thing
	<img src="./images/QIoT_addResources.png" width="60%" height="60%"><br/><br/>

5. Añadir una regla para mostrar los valores en el dashboard
	<img src="./images/QIoT_addRules.png" width="60%" height="60%"><br/><br/>

6. Configurar el dashboard
	<img src="./images/QIoT_configureDashboard.png" width="60%" height="60%"><br/><br/>	

7. Configurar la conexión al dispositivo mediante protocolo MQTT
	<img src="./images/QIoT_configureConnection.png" width="60%" height="60%"><br/><br/>


##### Enlaces interesantes de programacion con WEMOS D1:
WiFi ESP8266 Development Board WEMOS D1: 	https://alselectro.wordpress.com/2018/04/14/wifi-esp8266-development-board-wemos-d1/
ESP8266 WEMOS D1 With I2C Serial LCD: 		https://alselectro.wordpress.com/2018/04/16/esp8266-wemos-d1-with-i2c-serial-lcd/
