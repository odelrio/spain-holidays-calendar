(Work in progress)

# Spain Holidays Calendar

Colección de ficheros iCalendar con los festivos de distintos municipios de España.

## English (TL;DR)

Collection of iCalendar files with holidays in many different Spanish cities.

## Añádelo a tu calendario

### Apple Calendar app

### Google Calendar

### Office 365

## Cómo contribuir

### Sobre este repositorio

### Formato iCalendar

Los calendarios siguen el formato iCalendar.

### Calendarios

Los calendarios son ficheros con extensión `*.ics` que representan los festivos de un municipio mediante eventos.

Utiliza cualquier editor de texto plano para crear un nuevo calendario o editar uno ya existente. Sírvete de la plantilla de la región en la que se encuentre el municipio.

El nombre del calendario debe seguir el formato `<municipality_name>_<country_code>-<language_code>`, siendo:

 - `<municipality_name>` el nombre oficial del municipio:
   - En minúsculas
   - Con guión bajo (`_`) en lugar de espacios y apóstrofes (`'`)
   - Sin tildes
   - Reemplazando eñes (`ñ`) por enes (`n`)
   - Reemplazando ces cedilla (`ç`) por ces (`c`)
   
 - `<country_code>` el código del país del idioma:
   - Según ISO 3166-1
   - En minúsculas
  
 - `<language_code>` el código del idioma:
   - Según ISO 3166-1
   - En minúsculas

Coloca el calendario en la ruta `<region_name>/<province_name>/`, siendo `<region_name>` y `<province_name>` los nombres de la región (Comunidad o Ciudad Autónoma) y de la provincia respectivamente, en inglés y siguiendo las mismas reglas que `<municipality_name>`.

### Eventos

Los eventos deben ser de un día completo. Para ello establece un valor `DTSTART` y no indiques `DTEND`. Por ejemplo:

```
BEGIN:VEVENT
SUMMARY:Viernes Santo
DTSTART;VALUE=DATE:20200410
END:VEVENT
```

### Plantillas

En el directorio `.templates` se ubican plantillas a partir de las cuales pueden escribirse nuevos calendarios. Para crear una nueva plantilla, copia la plantilla `national` al directorio `.templates/regional/` y edítala. Nombra el fichero con el nombre de la región en inglés siguiendo las mismas reglas del `<minicipality_name>` de los calendarios.

### Mantenimiento

Los gobiernos autonómicos y locales pueden cambiar de fecha algunos festivos cuando coincidan con domingo. 
