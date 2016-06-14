# Sensebox-Brotbox
DigiCarto 16-2

  
<img src="https://github.com/sensebox/OER/raw/master/senseBox_edu/images/sensebox_logo_neu.png" width="200">
<br>
<h1>Brotbox</h1>
<br>
<table border="0">
      <tr>
        <td>Eine Sensebox zum messen von:    </td>
        <td>UV Intensität</td>
      </tr>
       <tr>
        <td></td>
        <td>Luftfeuchtigkeit</td>
      </tr>
       <tr>
        <td></td>
        <td>NH3 Gehalt</td>
      </tr>
       <tr>
        <td></td>
        <td>CO Gehalt</td>
      </tr>
       <tr>
        <td></td>
        <td>NO2 Konzentration</td>
      </tr>
       <tr>
        <td></td>
        <td>H2 Gehalt</td>
      </tr>
       <tr>
        <td></td>
        <td>C2H5OH Gehalt</td>
      </tr>
</table>
<br>
<h2>Ziel</h2>
<p>Die Brotbox soll einfache Wetterdaten sammeln und diese über die openSenseMap für alle bereitstellen.</p>
<p>Zusätzlich wurde sie mit einem sehr einfachen Multichannel Gas Sensor ausgestattet.
<br>
<br>
<h2>Materialien</h2>
<h4>Aus der senseBox:edu</h4>
<br>
<ul>
<li>Genuino UNO</li>
<li><a href="https://github.com/watterott/VEML6070-Breakout">VEML6070</a></li>
<li><a href="https://github.com/watterott/HDC100X-Breakout">HDC1000</a></li>
<li><a href="https://github.com/watterott/SenseBox-Shield">Sensebox-Shield</a></li>
<li><a href="https://www.arduino.cc/en/Main/ArduinoEthernetShield">W5500 Ethernet-Shield</a></li>
<li>Breadbord</li>
<li>Jumper Wires</li>
<li>Genuino UNO Netzteil</li>
</ul>
<br>
<h4>Zusätzliche Hardware</h4>
<br>
<ul>
<li>Flachband Ethernetkabel</li>
<li>PoE (Power over Ethernet) Adapter</li>
<li>Grove - Multichannel Gas Sensor</li>
<li>Kabel</li>
<li>120mm FAN</li>
<li>Plastikdose</li>
<li>Luftfilter</li>
<li>Schrauben</li>
<li>Plastikplatte</li>
<li>Plastikschlauch</li>
<li>Tape</li>
<li>Heißkleber</li>
<li>Kleines Glas</li>
<li>Dremel</li>
</ul>
<br>
<h2>Setup Beschreibung</h2>
<br>
<h3>Hardwarekonfiguration</h3>
<br>
<p>Auf den Genuino Uno wurden das Ethernet-Shield als auch das Sensebox-Shield aufgesteckt. Der Genuino Uno blieb mit dem Breadbord verschraubt. Zur Stromversorgung wurde ein PoE Adapter an beiden Enden des Flachband Ethernetkabels angebracht. Die Internetverbindung wird über das Ethernetkabel, welches am lokalen Router hängt hergestellt. Alle Sensoren wie auch der Fan sind über das Breadboard an das Sensebox-Shield angeschlossen. 
<br>
<br>
<img src="https://yz51mg-bn1306.files.1drv.com/y3mdv578rou0ycNKLmDZhIrxu9Z5q0ua4xMatvSJnXFR7JlFkECB7pTQisDZJsIT3nTEPosxqg1qQ7xFVvd0YLgTCzOCO4W6m7sLs1ZAxfbElF5ZNkAYreIzT1CjLi-ADcW5Ejfw-ceOmXdD5KkML7spQ?width=1024&height=576&cropmode=none" width="1024" height="576" />
<br>
<br>
Das Breadboard liegt lose auf dem Boden der Dose. Der Boden ist zusätzlich mit einer weitern Plastikplatte beschwert. Das Ethernetkabel wird durch ein, mit Tape abgedichtetes Loch nach außen geführt.
<br>
Um für eine ausreichende und Konstante Luftzufuhr zu sorgen, wurde ein Lüfter an der Oberseite der Dose angebracht, hierzu musste ein Ausschnitt in die Dose gemacht werden, dazu, wie auch zu allen weitern Arbeiten wurde ein Dremel verwendet. Damit trotz des Ausschnittes nicht unmittelbar Wasser von oben in die Dose dringen kann, bekam der Lüfter ein Dach. Um nicht zuviel Dreck mit ein zu saugen wurden an den extra dafür gefrästen Lüftungsschlitzen ein Luftfilter angebracht. 
<br>
<br>
<img src="https://bfphag-bn1306.files.1drv.com/y3meNyhh4UfixvL6Bq9vJChLf2HL1n6s0igSn5BWGERJspBVc6HLIGu7hYf9uac6pcguHuG675o7U_l3WfzD65DGcfRIRSj3qfrLwFI-X6Ww0ma3eZPpcSAP5e2uwVK-Ta0dSWfUTQxhXBSwWLfHK-uEg?width=1024&height=576&cropmode=none" width="1024" height="576" />
<br>
<br>
Damit der UV Sensor etwas bessere Daten liefern konnte bekam er einen Anbau aus Glas, welcher etwas mehr UV Licht an den Sensor lässt.
<br>
<br>
<img src="https://qric1q-bn1306.files.1drv.com/y3m6p3SbrQUgt-WjlP_cx4xT7Jfvi53sV7dIMBmFbwxOlNrJmHzd10Bv7zQ4J6saNsMLUqwWbsg0BVc6eF0Yucrf4R06Nd_j6wl49lBNqnZGJENuQLZGqzEXWjOCRdgkuccyv4O-0tsYJPxNWgxVCv50A?width=1024&height=576&cropmode=none" width="1024" height="576" />
</p>
<br>
<p>Schwierigkeiten traten mit dem Multichannel Gas Sensor auf. Leider sind die Bereichen in denen dieser erst zuverlässig messen kann in einer "normalen" Umgebung unerreichbar, weswegen leider diese Daten nahezu nutzlos sind. Dies sind hardwarespezifische Einschränkungen welche sich nicht umgehen ließen. Um möglichst keine falschen Daten mehr zu senden wurde der Code angepasst.</p>
<br>
<h3>Softwaresketch</h3>
<br>
<p>Der vorgegebene Code der openSenseMap wurde noch durch die Sensoren und ihre IDs (hier nicht erkenntlich) ergänzt und dann auf die Brotbox geladen.
<br>
Beim Auslesen des Multichannel Gas Sensors wurden noch Bedingungen gestellt, bevor Daten übermittelt werden. Leider ist der Sensor nicht in der Lage sinnvolle Werte zu ermitteln.</p>
<br>
```javascript
#include <SPI.h>
#include <Ethernet.h>

//GAS
#include "MutichannelGasSensor.h"

//UV
#define I2C_ADDR 0x38

//TEMP HUM
#include <HDC100X.h>
HDC100X HDC1(0x43);
 
//SenseBox ID
#define SENSEBOX_ID ""

//Sensor IDs
#define SENSOR1_ID "" // C2H5OH 
#define SENSOR2_ID "" // H2 
#define SENSOR6_ID "" // NO2 
#define SENSOR7_ID "" // CO 
#define SENSOR8_ID "" // NH3 
#define TEMPSENSOR_ID ""
#define SENSOR9_ID "" // Luftfeuchtigkeit 
#define UVSENSOR_ID ""

//Ethernet-Parameter
char server[] = "www.opensensemap.org";
byte mac[] = { 0xDE, 0xAD, 0xBE, 0xEF, 0xFE, 0xED };
// Diese IP Adresse nutzen falls DHCP nicht möglich
IPAddress myIP(192, 168, 0, 42);
EthernetClient client;

//Messparameter
int postInterval = 10000; //Uploadintervall in Millisekunden
long oldTime = 0;


void setup()
{
  Serial.begin(9600); 
  Serial.print("Starting network...");
  //Ethernet Verbindung mit DHCP ausführen..
  if (Ethernet.begin(mac) == 0) 
  {
    Serial.println("DHCP failed!");
    //Falls DHCP fehltschlägt, mit manueller IP versuchen
    Ethernet.begin(mac, myIP);
  }
  Serial.println("done!");
  delay(1000);

//UV
  Wire.begin();

  Wire.beginTransmission(I2C_ADDR);
  Wire.write((IT_1<<2) | 0x02);
  Wire.endTransmission();

//GAS
    mutichannelGasSensor.begin(0x04);
    mutichannelGasSensor.powerOn();

//TEMP HUM
HDC1.begin(HDC100X_TEMP_HUMI,HDC100X_14BIT,HDC100X_14BIT,DISABLE);  

  Serial.println("Starting loop.");
}
  


void loop()
{
  //Upload der Daten mit konstanter Frequenz
  if (millis() - oldTime >= postInterval)
  {
    oldTime = millis();
    
//TEMP HUM

float temp = HDC1.getTemp();
float hum = HDC1.getHumi();

    Serial.print(" Humidity: ");
    Serial.print(hum); 
    Serial.print("% Temperature: ");    
    Serial.print(temp);
    Serial.print("C");

     postFloatValue(temp, 1, TEMPSENSOR_ID);
     postFloatValue(hum, 1, SENSOR9_ID);
     
//GAS
    float c;

    c = mutichannelGasSensor.measure_NH3();
    Serial.print("The concentration of NH3 is ");
    if(c>=0) Serial.print(c);
    else Serial.print("invalid");
    Serial.println(" ppm");
    if(c>=1){
    postFloatValue(c,1,SENSOR8_ID);
    }

    c = mutichannelGasSensor.measure_CO();
    Serial.print("The concentration of CO is ");
    if(c>=0) Serial.print(c);
    else Serial.print("invalid");
    Serial.println(" ppm");
    if(c>=1){
    postFloatValue(c,1,SENSOR7_ID);
    }

    c = mutichannelGasSensor.measure_NO2();
    Serial.print("The concentration of NO2 is ");
    if(c>=0) Serial.print(c);
    else Serial.print("invalid");
    Serial.println(" ppm");
    if(c>=0.05){
    postFloatValue(c*1250,1,SENSOR6_ID);
    }
    
    c = mutichannelGasSensor.measure_H2();
    Serial.print("The concentration of H2 is ");
    if(c>=0) Serial.print(c);
    else Serial.print("invalid");
    Serial.println(" ppm");
        if(c>=1){
    postFloatValue(c,1,SENSOR2_ID);
        }
    c = mutichannelGasSensor.measure_C2H5OH();
    Serial.print("The concentration of C2H5OH is ");
    if(c>=0) Serial.print(c);
    else Serial.print("invalid");
    Serial.println(" ppm");
        if(c>=10){
    postFloatValue(c,1,SENSOR1_ID);
        }

//UV
   byte msb=0, lsb=0;
  uint16_t uv;

  Wire.requestFrom(I2C_ADDR+1, 1); //MSB
  delay(1);
  if(Wire.available())
    msb = Wire.read();

  Wire.requestFrom(I2C_ADDR+0, 1); //LSB
  delay(1);
  if(Wire.available())
    lsb = Wire.read();

  uv = (msb<<8) | lsb;

    Serial.print(" UV: ");    
    Serial.println(uv, DEC);

     postFloatValue(uv, 1, UVSENSOR_ID);    
     
  }
}

void postFloatValue(float measurement, int digits, String sensorId)
{ 
  //Float zu String konvertieren
  char obs[10]; 
  dtostrf(measurement, 5, digits, obs);
  //Json erstellen
  String jsonValue = "{\"value\":"; 
  jsonValue += obs; 
  jsonValue += "}";  
  //Mit OSeM Server verbinden und POST Operation durchführen
  Serial.println("-------------------------------------"); 
  Serial.print("Connectingto OSeM Server..."); 
  if (client.connect(server, 8000)) 
  {
    Serial.println("connected!");
    Serial.println("-------------------------------------");     
    //HTTP Header aufbauen
    client.print("POST /boxes/");client.print(SENSEBOX_ID);client.print("/");client.print(sensorId);client.println(" HTTP/1.1");
    client.println("Host: www.opensensemap.org"); 
    client.println("Content-Type: application/json"); 
    client.println("Connection: close");  
    client.print("Content-Length: ");client.println(jsonValue.length()); 
    client.println(); 
    //Daten senden
    client.println(jsonValue);
  }else 
  {
    Serial.println("failed!");
    Serial.println("-------------------------------------"); 
  }
  //Antwort von Server im seriellen Monitor anzeigen
  waitForServerResponse();
}

void waitForServerResponse()
{ 
  //Ankommende Bytes ausgeben
  boolean repeat = true; 
  do{ 
    if (client.available()) 
    { 
      char c = client.read();
      Serial.print(c); 
    } 
    //Verbindung beenden 
    if (!client.connected()) 
    {
      Serial.println();
      Serial.println("--------------"); 
      Serial.println("Disconnecting.");
      Serial.println("--------------"); 
      client.stop(); 
      repeat = false; 
    } 
  }while (repeat);
}

```

<h2>OpenSenseMap Registrierung</h2>
<br>
<p>Die Sensebox wurde mit dem Namen Brotbox registriert, ihre Gruppenkennzeichnung ist DigiCarto16-2. Die Sensoren wurden manuell eingerichtet </p>
<br>
<ul>
<li>VEML6070	UV-Intensität in µW/cm²</li>
<li>HDC1000	Luftfeuchtigkeit in %</li>
<li>HDC1000	Temperatur	in °C</li>
<li>Multi Gas Sensor NH3 in ppm</li>
<li>Multi Gas Sensor CO in ppm</li>
<li>Multi Gas Sensor NO2 in µg/m³</li>
<li>Multi Gas Sensor H2 in ppm</li>
<li>Multi Gas Sensor C2H5OH in ppm</li>
</ul>
<br>
Die Station findet man unter diesem Link: 
<br>
<h2>Stationsaufbau</h2>
<br>
<p>Die Station wurde auf einem Balkon zur Ostseite in der Von Esmarchstraße 10 aufgestellt. Dort steht sie relativ geschützt vom Wetter, aber auch von direkter Sonneneinstrahlung.</p>
<br>
<p></p>
<br>
<br>
<h2>Kontakt</h2>
<br>
<a href="mailto:Jan_PatrickBollow@hotmail.com">Jan-Patrick Bollow</a>
Münster, Juni 2016


