[Uploading README.md…]()

## Funcionalidades

1. Listar todas las tareas
2. Agregar una tarea (título y descripción opcional)
3. Marcar una tarea como completada o pendiente
4. Editar el título y/o la descripción de una tarea
5. Eliminar una tarea
6. Listar únicamente las tareas pendientes

Las tareas se guardan automáticamente en `data/tasks.json` cada vez que se
agregan, editan o eliminan, por lo que persisten entre ejecuciones.

## Cómo abrir el proyecto en Android Studio

1. Instalar el plugin **Dart** (Android Studio lo pedirá automáticamente al
   detectar el `pubspec.yaml`, o se instala desde
   `Settings > Plugins > Marketplace > Dart`).
2. Descomprimir el archivo `todo_console.zip`.
3. En Android Studio: `File > Open...` y seleccionar la carpeta `todo_console`.
4. Cuando Android Studio detecte el `pubspec.yaml`, ejecutar `pub get`
   (aparece un banner arriba del editor, o desde la terminal integrada:
   `dart pub get`).
5. Abrir `bin/main.dart` y ejecutar con el botón de "Run" (▶), o desde la
   terminal:

   ```bash
   dart run bin/main.dart
   ```

## Requisitos

- Dart SDK >= 3.0.0 (incluido en Flutter, o instalable de forma independiente
  desde https://dart.dev/get-dart).
- No requiere dependencias externas (solo `dart:io` y `dart:convert`, que
  vienen incluidas en el SDK).

## Notas de diseño

- Se separó el modelo (`Task`), la lógica de negocio (`TodoService`) y la
  interfaz de usuario (`main.dart`) siguiendo el principio de responsabilidad
  única, tal como se aborda en las asignaturas de Programación Orientada a
  Objetos.
- La persistencia se implementó manualmente con `dart:convert` (JSON) para
  reforzar el manejo de archivos y serialización sin depender de paquetes
  externos.
