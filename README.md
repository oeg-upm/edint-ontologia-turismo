# Ontología EDINT Turismo (EDINT Tourism Ontology)
Este repositorio reutiliza algunas clases y propiedades de la Ontología SEGITTUR (Sociedad Mercantil Estatal para la Gestión de la Innovación y las Tecnologías Turísticas en España), un modelo para el desarrollo de una Red de Ontologías del Sector Turístico. La reutilización de la ontología de SEGITTUR comprende las siguientes clases y propiedades:
## Clase AccomodationEstablishment
Los tipos de alojamiento son subclases: Hotel, Hostal, Hostel, Aparthotel, Vacation Rentals.
### Propiedades:
- accomodationRating (object property) entre AccomodationEstablishment y Rating
- numberOfAccomodationUnits (data property) xsd:int
- numberOfBeds (data property) xsd:int
- registrationNumber es identificador(data property) string
- hasDescription (object property) entre TourismEntity (superclase) y Description
- name (data property) xsd:string
- hasLocation (object property) entre Place (superclase) y Location 
- hasContactPoint (object property) entre Place (superclase) y ContactPoint

## Clase ContactPoint
### Propiedades:
- email (data property) xsd:string
- telephone (data property) xsd:string
- url (data property) xsd:string

## Clase Rating
### Propiedades:
- ratingUnit (data property) xsd:string. por ejemplo "stars"
- ratingValue (data property) xsd:string. por ejemplo "3"

## Clase Description
### Propiedades:
- longDescription (data property) xsd:string
- shortDescription (data property) xsd:string

## Clase Location
### Propiedades:
- autonomousCommunity (data property) xsd:string
- country (data property) xsd:string
- county (data property) xsd:string (comarca)
- province (data property) xsd:string
- locality (data property) xsd:string
- postal code (data property) xsd:string
- street address (data property) xsd:string 
- gsp:lat y gsp:long (subclase de gsp:Feature)

## Clase: HistoricalOrCulturalResource
Los tipos de alojamiento son subclases: Alcazar, Amphiteatre, Acueduct, etc.

### Propiedades:
- name (data property) xsd:string
- hasLocation (object property) entre Place (superclase) y Location 
- hasDescription: (object property) entre TourismEntity (superclase) y Description

# Propósito y alcance de la ontología (Purpose and scope of the ontology)

El propósito de esta ontología es el de proporcionar un vocabulario común para la representación de las entidades y datos principales de los alojamientos y puntos de interés turísticos de un municipio para que luego se pueda realizar su explotación turística a través de la Ontología de Cubos de Turismo. Su alcance cubre los datos que pueden ser utilizados con los propósitos de conocer y gestionar el turismo dentro del municipio que es parte de las funciones habituales de las entidades locales.

# Prefijo y espacio de nombres (Prefix and namespace)

El prefijo de la ontología es: `edinttur` y se encuentra publicada en el espacio de nombres: [https://ontologia.segittur.es/turismo/def/core#)](https://ontologia.segittur.es/turismo/def/core#)

# Estructura del repositorio (Repository structure)

El repositorio contiene las siguientes carpetas

| Carpeta | Descripción |
|--------|--------------|
| **examples/** | Contiene las fuentes de datos y los ejemplos en RDF generados con la ontología a partir de estas fuentes. |
| **mappings/** | Contiene los ficheros de los mappings (reglas de correspondencia) utilizados para generar los ejemplos en RDF.  |

# Mantenimiento y evolución (Maintenance and evolution)

Para manejar las incidencias o mejoras sugeridas con respecto a la ontología, recomendamos seguir las guías proporcionadas en ([Issues Management](./ISSUES.md)) para generar una incidencia.

# Financiación (Funding)

Esta ontología ha sido desarrollada en el contexto del Espacio de Datos para las Infraestructuras Urbanas Inteligentes ([EDINT](https://edint.es)).

![Logos](./resources/EDINT_UE_V-Color.png)
