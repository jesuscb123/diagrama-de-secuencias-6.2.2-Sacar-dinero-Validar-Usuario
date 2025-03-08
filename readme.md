## Diagrama de secuencias.
### Validar usuario.
- PlantUML:
@startuml
        actor usuario
        participant "interfaz" as in
        participant "control" as con
        participant "entidad" as en

        usuario -> in: introduce tarjeta
        in -> con: tarjeta
        con --> en: tarjeta
        en --> con: tarjeta validada
        in --> usuario: preguntar pin
        usuario -> in: introduce pin
        in -> con: pin
        con -> en: pin
        en -> con: pin validado
        @enduml
    
![image](https://github.com/user-attachments/assets/bab8fce4-9da0-49da-a065-9471ebd4b345)

#### Interpretación del programa.
- Usuario introduce la tarjeta.
- La tarjeta para a control para verificar si es correcta.
- La tarjeta llega a entidad para comprobar que la tarjeta es del banco que corresponde y es válida.
- Entidad valida la tarjeta, se la pasa a control y es correcto.
- Luego le pide el pin al usuario.
- Usuario introduce el pin, control obtiene el pin y se lo pasa a la entidad para comprobar si es correcto.
- El pin es validado por la entidad y se lo comunica a control.


### Sacar dinero:
        @startuml
        actor usuario
        participant "interfaz" as in
        participant "control" as con
        participant "entidad" as en

        usuario -> in: cantidad a sacar
        in -> con: cantidad
        con -> en: cantidad
        en -> con: cantidad aceptada
        @enduml
        
![image](https://github.com/user-attachments/assets/8d872930-3c11-4212-a775-bc0a30c2007e)


#### Interpretación del programa.
- Usuario introduce la cantidad a sacar.
- Control pasa la cantidad a la entidad para verificar si puede sacar esa cantidad de dinero.
- Como el usuario tiene suficiente para sacar, acepta la cantidad y lo se lo comunica a control.
- El dinero ya puede recogerlo el usuario.

Responde a la pregunta: ¿De que manera te ayuda un diagrama de secuencias durante el proceso de desarrollo del software? (Entrega: Respuesta)

Los diagrama de secuencia es muy útil para el desarrollo debido a que puedes ver de manera clara, los pasos que dará el programa durante su ejecución durante el tiempo.
