# Base de datos de pacientes infectados por corona virus en Guatemala

Descripcion: Esta es un dataset ***no oficial***, recopilado de fuentes oficiales, de los casos confirmados de Corona Virus en Guatemala.

Descargo de Responsabilidad: Esta base de datos ha sido recopilada por voluntarios. Hacemos el mejor esfuerzo por recolectar informacion confiable y certera, pero no proveemos ninguna garantia.

Proposito: 
- Recolectar informacion confiable y amplia de fuentes oficiales y/o medios sobre pacientes confirmados de corona virus
- Que otras personas utilicen esta base de datos para desarrollar y publicar sus propias visualizaciones de datos y, asi, informar a la poblacion
- Dejar un registro de la evolucion del corona virus en Guatemala 
- Atacar la desinformacion

***Licencia: [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)***


# Descripcion de campos

## pacientes.csv

Contine la informacion disponible de los casos confirmados de corona virus en Guatemala.

- id: numero de paciente (numerico, entero)
- sex: m: masculino, f: femenino, x: desconocido (string)
- birth_date: yy-mm-dd, ano de nacimiento. Se calcula como: fecha = 2020 - Edad, por tanto el dia y mes no se registran y se utiliza un valor por defecto 01-01(string), o campo vacio
- age: edad del paciente (numerico, entero), -99: desconocido
- country: pais de origen/nacionalidad (string) o campo vacio
- department: Region donde tuvo mayor actividad (string)
- illness: condicion medica previa o desconocido (string)
- group: relacion con algun grupo especifico, -99: desconocido, no aplica (numerico, entero)
	- 1: vuelo 11 de marzo aeromexico
	- 2: vuelo 6 de marzo iberia
	- 3: contacto directo o indirecto con paciente 2 (primer fallecido)
	- 4: vuelo de rescate 26 de marzo, de Espana a Guatemala
- infection_cause: causa de la infeccion (viaje, visita a familiar, visita a hospital, contacto con paciente, etc) (string)
- infected_by: id del paciente que transmitio, -99: desconocido (numerico, entero)
- confirmation_date: aa-mm-dd fecha en la que se confirmo la infeccion, o campo vacio si es desconocido (string)
- recovery_date: aa-mm-dd fecha en la que el paciente se recupero, o campo vacio si es desconocido (string)
- deceased_date: aa-mm-dd fecha en que el paciente fallecio, o campo vacio (string)
- status: 0: aislado  1: recuperado  2: fallecido (numerico, entero)
- source: enlace a la fuente de la noticia en wayback machine. Cuando se consultaron varias fuentes, los enlaces se separan con asterisco "*" (ver abajo) (string)




### [Wayback Machine](https://archive.org/web/)?

Es una organizacion que almacena el internet. A este proyecto, sirve dos propositos:
1) Que la fuente de informacion quede almacenada permanentemente
2) Evitar que malos actores utilicen este espacio para distribuir desinformacion o contenido peligroso

Para crear un hipervinculo en wayback machine:

a) Ir a https://archive.org/web/:

b) Copiar el enlace a la fuente y pegarlo en la casilla "Save Page Now"

c) Click en el boton "Save Page"

d) Copiar el enlace a la nueva pagina. Este enlace inicia con https://web.archive.org: 
	- Ejemplo: https://web.archive.org/web/20200315072155/https://www.prensalibre.com/guatemala/comunitario/coronavirus-alejandro-giammattei-confirma-el-primer-caso-de-covid-19-en-guatemala/

Contacto: utiliza la pestana [issues](https://github.com/ncovgt2020/ncovgt2020/issues) para hacer sugerencias/comentarios, notificar sobre nuevos casos. Haz un pull request para contribuir. Escribe un correo a ncovgt2020[arroba]hotmail.com.
