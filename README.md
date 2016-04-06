# Ricochet Bracelet Vibrant

Retour vibrant des sons joués avec les cubes Ricochets. 



## UML



## Functionnalities

#### Arduino
- `Setup()`
    - call `connectToServer()`

- `Loop()`
    - Test vibration force for decrement it `decrement()`.
    - Test LED status (`BLINK`, `FAST_BLINK`, `ON`).
    - checkConnection. If disconnected `onDisconnected()`


#### Connection
- `connectToServer()` 
    - LED status to `BLINK`
    - Connextion
    - setTimeout 15 sec before `turnOff()`

- `onConnected()`
    - LED status to `ON`

- `onDisconnected()`
    - call `connectToServer()`


#### DataReceived
- `onDataReceived(float mLeftValue, float mLeftVel, float mRightValue, float mRightVel)`
    - update variables.


#### Private
- `decrement(float value, float vel)`
    - return value decremented by vel.

- `turnOff()`
    - Turn off the bracelet.




## Important Components

- **1 ESP8266 :** Module wifi pour la connection permettant aussi le contrôle des deux vibreurs grâce à ses deux sorties Digitas. Voir aussi [Ricochet_test_wifi](https://github.com/ricochetGobz/ricochet_test_wifi)

- **2 Vibro motors :** Ces deux moteurs traduisent le son en vibration. Un vibreur pour les sons graves. Un second pour les notes aiguës.

- **1 Batterie OU piles boutons :** 3.3V pour alimenter le tout. 


## Temporary Cabling

<img alt="Cabling"" src="https://github.com/ricochetGobz/ricochet_bracelet/blob/master/imgs/cabling_bracelet.png?raw=true">


## Fabrication

Pistes : Impression 3D OU Brassard tissus.

