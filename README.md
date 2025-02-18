# diagrama-
tarea 2
```mermaid
classDiagram
class Dispositivo {
  +String nombre
}

class Impresora {
  +float probabilidadAveria
  +int tiempoReparacion
}

class Computadora {
  +enviarMensaje()
}

class PC {
  +conectarHub()
}

class Servidor {
  +conectarHub()
}

class Hub {
  +int numPuertos
  +float probabilidadPerdida
  +conectarHub()
}

class CableRed

class Mensaje {
  +int longitud
}

Dispositivo <|-- Impresora
Dispositivo <|-- Computadora
Dispositivo <|-- Hub
Computadora <|-- PC
Computadora <|-- Servidor

PC --o Hub : conecta
Servidor --o Hub : conecta




Computadora --o Mensaje : genera


