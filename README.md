# Postman API Testing

Esta carpeta contiene un proyecto de prueba basado en una colección de Postman.

## Estructura

```text
postman/
  collections/           # colecciones exportadas (.json)
  environments/          # entornos exportados (opcional)
  package.json           # dependencias y scripts de ejecución
  .gitignore             # archivos a ignorar
  README.md              # este archivo
```

## Uso

1. **Importar colección**: en la app de Postman, selecciona *Import* y elige `postman/collections/example-collection.json`.
2. **(Opcional) Importar entorno**: si tienes un archivo en `postman/environments`.
3. **Ejecutar con Newman** desde la línea de comandos:

   ```bash
   npm install
   npm run newman
   ```

   Esto ejecuta la colección con los valores de entorno por defecto.

4. Para especificar un entorno manualmente:

   ```bash
   npx newman run postman/collections/example-collection.json \
     --environment postman/environments/dev.postman_environment.json
   ```

5. Si actualizas la colección en Postman, expórtala de nuevo (`...` > *Export*) y reemplaza el fichero JSON en `postman/collections`.

## Configuración optional

- Puedes crear scripts adicionales en `package.json` para diferentes entornos o reportes.
- Agrega un workflow de GitHub Actions para ejecutar Newman automáticamente en cada push.

## .gitignore

Asegúrate de tener estas entradas para no subir dependencias ni datos sensibles:

```
node_modules/
*.postman_environment.json
```
