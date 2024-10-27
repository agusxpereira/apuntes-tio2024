## Sistema de control de versiones:
- Registra *cambios realizados en archivos*
- Visualizar *que* se modificó
- Identificar *quien* realizo los cambios y cuales
- Registrar *cuando* se realizao una modificacion
- *Volver a versiones anteriores*

### Ventajas:
- Posee un registro historico del proyecto (desde la primer version)
- flexibilidad ante modificaciones
- Generar estadisticas
- Facilita el trabajo e equipo
- Facilita la administracion del proyecto
- Mejora el compromiso del equipo

### Desventajas:
- Curva de aprendizaje elevada


Hay distintos tipo de estos sistemas, que pueden ser "centralizados" o "distribuidos"

### Centralizados

Un único servidor contiene los archivos versionados. Los clientes descargan la última versión y cargan archivos en dicho servidor. Para realizar nuevos registros, se requiere una coneccion con dicho servidor. Pero tiene sus desventajas, como: recuperacion compleja y baja tolerancia a fallos.

### Distribuidos

Los clientes no sólo descargan la última copia, sino que en sí descarga el repositorio entero. Se pueden registrar cambios aun sin conexion. Luego estos cambios pueden ser enviados al servidor cuando hay conexion. Aumenta la tolerancia a fallos. Si un servidor deja de funcionar, cualquier de las copias de los clientes puede usarse para restaurar el repositorio en el servidor.

## Git
Tiene un fuerte apoyo al desarrollo no lineal, permitiendo tener ramas paralelas. Es completamente distribuido y permite manejar grandes proyectos de manera eficiente.

- Conserva una única versión de cada archivo.
- Toma una "foto" de los cambios periodicamente (con ***commit***)
- Estas "fotos o instantaneas" quedan registradas en un **historial de cambios**.

### Flujo de trabajo:

Git tiene un flujo de trabajo, que se divide en 3 areas principales

[ Working Directory ] [ Staging Area ] [ Repositorio ]

Órdenes Básicas

- git init Iniciar un repositorio vacío en unas carpeta específica
- git status Revisamos el estado de los archivos
- git add ‘nombre_de_archivo’ Añadir un archivo específico al área de preparación
- git add . Añadir todos los archivos del directorio
- git commit –m “mensaje” Confirmar los cambios realizados
- git log Muestra el historial de confirmaciones
- git diff Muestra los cambios del working directory con respecto a la última versión guardada en el repositorio


[Bibliografia](https://git-scm.com/book/es/v2)
Leer:
1.3 Empezando - Fundamentos de Git
1.5 Empezando
1.6 Empezando - Obteniendo ayuda
2.1 - 2.4 Fundamentos de Git