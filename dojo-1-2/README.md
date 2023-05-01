# DOJO - 1-1 

![LOGO TINKERCAD](https://github.com/iagovalverde/EjemploDocumentacion/blob/main/img/ArduinoTinkercad.jpg)

## INTEGRANTES
* Iago Valverde Pachiani
* Lucas Gabriél Sigüenza
* Victoria Rodriguez  
* Enzo Pose
* Nicolás Velazquez


## PROYECTO: DOJO 1-2

![IMAGEN DEL PROYECTO](https://i.im.ge/2023/04/25/LbqHzC.dojo-1-1-tinkercad.jpg)

## DESCRIPCIÓN

El proyecto es un semáforo con 2 lámparas led (de cada color). <br/>
El verde dura 5 segundos. <br/>
El amarillo dura 3 segundos. <br/>
Rojo dura 5 segundos. <br/>
Al cambiar de un color a otro, la luz que se va a apagar titila 3 veces antes de apagarse. <br/>
Además posee señalización para personas no videntes, que suena durante la luz roja dos veces a cada segundo en tono fuerte, y durante la luz amarilla suena una vez a cada segundo en tono suave.



## FUNCIÓN PRINCIPAL

La función principal se encarga de prender, apagar y titilar los leds del semáforo, se utilizando de las funciones encender, apagar y titilar respectivamente. <br/>
Además, mientras el rojo está prendido, suena el piezo 2 veces por segundo en tono fuerte. <br/>
Ya en el amarillo, el piezo suena 1 vez por segundo, en tono suave. <br/>
Los leds y el piezo son asignados a través del hashtag define a los pines a los cuales están conectados.

```C++ 
void loop()
{
  Serial.println("Se prende y apaga el verde");
  encender(LED_VERDE_A,LED_VERDE_B,5000);
  titilar(LED_VERDE_A, LED_VERDE_B,150);
  apagar(LED_VERDE_A,LED_VERDE_B, 100);
  
  Serial.println("Se prende el amarillo y suena el piezo 3x");
  for(int i = 0; i < 3; i++)
  {
  	encender(LED_AMARILLO_A,LED_AMARILLO_B,1000);
    tone(PIEZO,1300,250);
  }
  titilar(LED_AMARILLO_A, LED_AMARILLO_B,150);
  Serial.println("Se apaga el amarillo");
  apagar(LED_AMARILLO_A,LED_AMARILLO_B,100);
  
  Serial.println("Se prende el rojo y suena el piezo 10x");
  for(int i = 0; i < 10; i++)
  {
    encender(LED_ROJO_A,LED_ROJO_B,500);
    tone(PIEZO,700,250);
  }
  titilar(LED_ROJO_A, LED_ROJO_B,150);
  Serial.println("Se apaga el rojo");
  apagar(LED_ROJO_A,LED_ROJO_B, 100);
  
  Serial.println("Se prende el amarillo y suena el piezo 3x");
  for(int i = 0; i < 3; i++)
  {
  	encender(LED_AMARILLO_A,LED_AMARILLO_B,1000);
    tone(PIEZO,1300,250);
  }
  titilar(LED_AMARILLO_A, LED_AMARILLO_B,150);
  Serial.println("Se apaga el amarillo");
  apagar(LED_AMARILLO_A,LED_AMARILLO_B,100);
}

```

## LINK AL PROYECTO

* [proyecto](https://www.tinkercad.com/things/bSodF9HUHMo-copy-of-iago-valverde-pachiani-dojo-1-1-div-1d-/editel?sharecode=5ifOxkhpneCqJQT8QICxtyKw2u61xc9nHbyFyQQ5LXA)

