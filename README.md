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

Este es un repositorio de Git alojado en GitHub. Los ficheros que contiene son de dominio público (véase la licencia MIT). El trabajo aquí recogido es aportado y mantenido públicamente de forma totalmente altruista y no remunerada. 

Si no estás familiarizado con Git y quieres contribuir con un nuevo calendario, envíalo a `example@example.org` en el formato descrito a continuación.

### Formato iCalendar

Los calendarios que aquí se recogen siguen el formato [iCalendar](https://icalendar.org/RFC-Specifications/iCalendar-RFC-5545/). No obstante, se omiten reglas y propiedades del formato para facilitar la confección de calendarios sin que eso afecte a la integridad de los mismos.

Todos los calendarios comienzan con un encabezado y siguen con una serie de eventos. Echa un vistazo a alguno de los calentarios existentes en el repositorio.

### Calendarios

Estos calendarios son ficheros con extensión `*.ics` que representan los festivos de un único municipio mediante eventos.

Utiliza cualquier editor de texto plano para crear un nuevo calendario o editar uno ya existente. Sírvete de la [plantilla](.templates) de la región en la que se encuentre el municipio.

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

En el directorio [`.templates`](.templates) se ubican plantillas a partir de las cuales pueden escribirse nuevos calendarios. Para crear una nueva plantilla, copia la plantilla `national` al directorio `.templates/regional/` y edítala. Nombra el fichero con el nombre de la región en inglés siguiendo las mismas reglas del `<minicipality_name>` de los calendarios.

### Mantenimiento

Los calendarios requieren de un mantenimiento periódico dado que no se pueden conocer con exactitud los festivos de los años venideros. Los gobiernos autonómicos y locales pueden cambiar de fecha algunos festivos cuando coincidan con domingo. 
