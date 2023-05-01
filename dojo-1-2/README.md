# DOJO - 1-1 

![LOGO TINKERCAD](https://github.com/iagovalverde/EjemploDocumentacion/blob/main/img/ArduinoTinkercad.jpg)

## INTEGRANTES
* Iago Valverde Pachiani
* Lucas Gabriél Sigüenza
* Victoria Rodriguez  
* Enzo Pose
* Nicolás Velazquez


## PROYECTO: DOJO 1-1

![IMAGEN DEL PROYECTO](https://i.im.ge/2023/04/25/LbqHzC.dojo-1-1-tinkercad.jpg)

## DESCRIPCIÓN

El proyecto es un semáforo con 2 lámparas led (de cada color). <br/>
El verde dura 5 segundos. <br/>
El amarillo dura 3 segundos. <br/>
Rojo dura 5 segundos.<br/>
Además posee señalización para personas no videntes, que suena durante la luz roja dos veces a cada segundo.

## FUNCIÓN PRINCIPAL

La función principal se encarga de prender y apagar los leds del semáforo, se utilizando de las funciones encender y apagar, respectivamente. <br/>
Además, mientras el rojo está prendido, suena el piezo 2 veces por segundo. <br/>
Los leds y el piezo son asignados a través del hashtag define a los pines a los cuales están conectados.

```C++ 
void loop()
{
  Serial.println("Se prende y apaga el verde");
  encender(LED_VERDE_A,LED_VERDE_B,5000);
  apagar(LED_VERDE_A,LED_VERDE_B,100);
  
  Serial.println("Se prende y apaga el amarillo");
  encender(LED_AMARILLO_A,LED_AMARILLO_B,3000);
  apagar(LED_AMARILLO_A,LED_AMARILLO_B,100);
  
  Serial.println("Se prende el rojo y suena el piezo 10x");
  for(int i = 0; i < 10; i++)
  {
    encender(LED_ROJO_A,LED_ROJO_B,500);
    tone(PIEZO,700,250);
  }
  Serial.println("Se apaga el rojo");
  apagar(LED_ROJO_A,LED_ROJO_B, 100);
  
  Serial.println("Se prende y apaga el amarillo");
  encender(LED_AMARILLO_A,LED_AMARILLO_B,3000);
  apagar(LED_AMARILLO_A,LED_AMARILLO_B,100);
}
```

## LINK AL PROYECTO

* [proyecto](https://www.tinkercad.com/things/76dDInoYdJ1-copy-of-iago-valverde-pachiani-dojo-1-1-div-1d-/editel?sharecode=cDfIfj1akZQv_q2SjwpW7svFTyuQVZkX2JxDTUFSXeo)

