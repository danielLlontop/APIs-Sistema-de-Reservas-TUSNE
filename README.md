# Documentación de APIs del Sistema de Reservas TUSNE

## Introducción

Este documento describe los endpoints disponibles para el sistema de reservas TUSNE. Incluye APIs para la gestión de ambientes, usuarios y reservas. Cada endpoint incluye detalles sobre los métodos HTTP, URL y parámetros esperados.

## API de Ambientes

Gestión de los ambientes disponibles para reservas.

### Obtener Todos los Ambientes

Descripción: Permite obtener todos los ambientes registrados. Devuelve un array de objetos.

Método: GET

URL: <https://api-x0nz.onrender.com/v1/ambientes/>

Cuerpo de la respuesta (JSON):

{  
"denominacion_ambi": Canchita Skate", (string)  
"capacidad_ambi": 100, (integer)  
"direccion_ambi": "Calle 123", (string)  
"precioporhora_ambi": 60.0, (float)  
"estado_ambi": "Activo" (string)  
}

### Crear Ambiente

Descripción: Permite crear un nuevo ambiente.

Método: POST

URL: <https://api-x0nz.onrender.com/v1/ambientes/>

Cuerpo de la solicitud (JSON):

{  
"denominacion_ambi": "Canchita Skate", (string)  
"capacidad_ambi": 100, (integer)  
"direccion_ambi": "Calle 123", (string)  
"precioporhora_ambi": 60.0, (float)  
"estado_ambi": "Activo" (string)  
}

### Actualizar Ambiente

Descripción: Permite actualizar un ambiente.

Método: PUT

URL: <https://api-x0nz.onrender.com/v1/ambientes/>

Cuerpo de la solicitud (JSON):

{

"id": "642695e7-5a9d-4158-a2e0-550e3840c2bc", (string/UUID)  
"denominacion_ambi": "Canchita Skate", (string)  
"capacidad_ambi": 100, (integer)  
"direccion_ambi": "Calle 123", (string)  
"precioporhora_ambi": 60.0, (float)  
"estado_ambi": "Activo" (string)  
}

### Eliminar Ambiente

Descripción: Permite eliminar un ambiente. Recibe por parámetro el id del ambiente (/id)

Método: DELETE

URL: <https://api-x0nz.onrender.com/v1/ambientes/id>

URL Ejemplo: <https://api-x0nz.onrender.com/v1/ambientes/fbbc35a5-1832-449f-8854-052f250eebd2>

Cuerpo de la respuesta (TEXT):

“Registro Eliminado”

## API de Usuarios

Gestión de los usuarios registrados en el sistema.

### Obtener Usuarios

Descripción: Permite obtener todos los usuarios registrados.

Método: GET

URL: <https://api-x0nz.onrender.com/v1/personas/>

Cuerpo de la respuesta (JSON):

{

"id": "3f6f22b3-fd3f-4210-a479-99538fd4db56", (String/UUID)

"rolId": "c8d4e2f5-414c-41b5-be94-6fa80930736a", (String/UUID)

"nombrePers": "CRISTHYN OFELIA", (String)

"dniPers": "75007454", (String)

"cargoPers": "jefe", (String)

"denominacionPers": "Persona Jurídica", (String)

"asociacionPers": "Negocios SAC", (String)

"apellido_patPers": "CORREA", (String)

"apellido_matPers": "OCMIN", (String)

"correoPers": "<user@gmail.com>", (String)

"telefonoPers": 927994593, (integer)

"fecha_registroPers": "21-11-2024", (Date: DD/MM/YY)

"fecha_actualizacionPers": "21-11-2024", (Date: DD/MM/YY)

"clavePers": "USUARIO123", (String)

"estadoPers": "Activo", (String)

"nombre_rol": “Operador”, (String)

"codigoBoletaPers": “C07845” (String)

}

### Obtener Usuarios ordenados por Rol

Descripción: Permite obtener todos los usuarios registrados ordenados por Rol.

Método: GET

URL: <https://api-x0nz.onrender.com/v1/personas/rol>

Cuerpo de la respuesta (JSON):

{

"id": "3f6f22b3-fd3f-4210-a479-99538fd4db56", (String/UUID)

"rolId": "c8d4e2f5-414c-41b5-be94-6fa80930736a", (String/UUID)

"nombrePers": "CRISTHYN OFELIA", (String)

"dniPers": "75007454", (String)

"cargoPers": "jefe", (String)

"denominacionPers": "Persona Jurídica", (String)

"asociacionPers": "Negocios SAC", (String)

"apellido_patPers": "CORREA", (String)

"apellido_matPers": "OCMIN", (String)

"correoPers": "<user@gmail.com>", (String)

"telefonoPers": 927994593, (integer)

"fecha_registroPers": "21-11-2024", (Date: DD/MM/YY)

"fecha_actualizacionPers": "21-11-2024", (Date: DD/MM/YY)

"clavePers": "USUARIO123", (String)

"estadoPers": "Activo", (String)

"nombre_rol": “Operador”, (String)

"codigoBoletaPers": “C07845” (String)

}

### Registrar Usuario

Descripción: Permite registrar un nuevo usuario.

Método: POST

URL: <https://api-x0nz.onrender.com/v1/personas/>

Cuerpo de la solicitud (JSON):

{

"rolId": "c8d4e2f5-414c-41b5-be94-6fa80930736a", (String/UUID)

"nombrePers": "CRISTHYN OFELIA", (String)

"dniPers": "75007454", (String)

"cargoPers": "jefe", (String)

"denominacionPers": "Persona Jurídica", (String)

"asociacionPers": "Negocios SAC", (String)

"apellido_patPers": "CORREA", (String)

"apellido_matPers": "OCMIN", (String)

"correoPers": "<user@gmail.com>", (String)

"telefonoPers": 927994593, (integer)

"fecha_registroPers": "21-11-2024", (Date: DD/MM/YY)

"fecha_actualizacionPers": "21-11-2024", (Date: DD/MM/YY)

"clavePers": "USUARIO123", (String)

"estadoPers": "Activo", (String)

"nombre_rol": “Operador”, (String)

"codigoBoletaPers": “C07845” (String)

}

### Actualizar Usuario

Descripción: Permite actualizar un usuario.

Método: PUT

URL: <https://api-x0nz.onrender.com/v1/personas/>

Cuerpo de la solicitud (JSON):

{

"id": "3f6f22b3-fd3f-4210-a479-99538fd4db56", (String/UUID)

"rolId": "c8d4e2f5-414c-41b5-be94-6fa80930736a", (String/UUID)

"nombrePers": "CRISTHYN OFELIA", (String)

"dniPers": "75007454", (String)

"cargoPers": "jefe", (String)

"denominacionPers": "Persona Jurídica", (String)

"asociacionPers": "Negocios SAC", (String)

"apellido_patPers": "CORREA", (String)

"apellido_matPers": "OCMIN", (String)

"correoPers": "<user@gmail.com>", (String)

"telefonoPers": 927994593, (integer)

"fecha_registroPers": "21-11-2024", (Date: DD/MM/YY)

"fecha_actualizacionPers": "21-11-2024", (Date: DD/MM/YY)

"clavePers": "USUARIO123", (String)

"estadoPers": "Activo", (String)

"nombre_rol": “Operador”, (String)

"codigoBoletaPers": “C07845” (String)

}

### Eliminar Usuario

Descripción: Permite eliminar un usuario. Recibe por parámetro el id del usuario (/id)

Método: DELETE

URL: <https://api-x0nz.onrender.com/v1/personas/id>

URL Ejemplo: <https://api-x0nz.onrender.com/v1/personas/ee550587-02e0-45d8-bd59-6b34eb648f93>

Cuerpo de la respuesta (TEXT):

“Registro Eliminado”

### Login Usuario

Descripción: Permite logear un usuario.

Método: POST

URL: <https://api-x0nz.onrender.com/v1/personas/login>

Cuerpo de la solicitud (JSON):

{

"user": "<carlos@gmail.com>", (String)

"clave": "123456" (String)

}

Cuerpo de la respuesta (JSON):

{

&nbsp;   "codigo": 200,

&nbsp;   "mensaje": "Inicio de Sesión Satisfactorio",

&nbsp;   "token":"aWQ9OTkwZTU5ZTgtN2E4My00NWI0LTk1YmQtZTgzMjk0YmI5NzNhIT0hdXN1YXJpbz1jYXJsb3NAZ21haWwuY29tIT0hcGFzc3dvcmQ9MTIzNDU2IT0hcm9sPUFkbWluaXN0cmFkb3IhPSFwZXJzb25hPUp1YW5jaXRvIGNhcmxvcyBUZXJyb25lcyE9IWZlY2hheWhvcmE9MjAyNC0xMi0wOFQwNDo1NDozMy43NTcyMzIyMTM="

}

## API de Reservas

Gestión de las reservas realizadas por los usuarios.

### Obtener Reservas

Descripción: Permite obtener todas las reservas realizadas.

Método: GET

URL: <https://api-x0nz.onrender.com/v1/reservas/>

Cuerpo de la respuesta (JSON):

&nbsp;{

&nbsp;       "id": "6fd21535-eefb-46d7-8f06-2aa533dcaa6d",

&nbsp;       "personaId": “004c4f09-ab28-4820-ac24-d7b775e92cc4”,

&nbsp;       "ambienteId": "dab0cb27-3a09-4aa1-861b-84249405e835",

&nbsp;       "fechaReserva": "22-11-2024",

&nbsp;       "fechaSolicitud": "20-11-2024",

&nbsp;       "fechaActualizacion": "22-11-2024",

&nbsp;       "totalRese": 225,

&nbsp;       "pago_estadoRese": "Pendiente",

&nbsp;       "horaInicio": "00:41:23",

&nbsp;       "horaFin": "03:41:23",

&nbsp;       "denominacion_ambi": “Parque Infantil”,

&nbsp;       "dniPers": “78720904”

&nbsp;   }

### Obtener Reservas ordenados por Ambiente

Descripción: Permite obtener todas las reservas realizadas ordenados por Ambiente.

Método: GET

URL: <https://api-x0nz.onrender.com/v1/reservas/persona_ambiente>

Cuerpo de la respuesta (JSON):

&nbsp;{

&nbsp;       "id": "6fd21535-eefb-46d7-8f06-2aa533dcaa6d",

&nbsp;       "personaId": “004c4f09-ab28-4820-ac24-d7b775e92cc4”,

&nbsp;       "ambienteId": "dab0cb27-3a09-4aa1-861b-84249405e835",

&nbsp;       "fechaReserva": "22-11-2024",

&nbsp;       "fechaSolicitud": "20-11-2024",

&nbsp;       "fechaActualizacion": "22-11-2024",

&nbsp;       "totalRese": 225,

&nbsp;       "pago_estadoRese": "Pendiente",

&nbsp;       "horaInicio": "00:41:23",

&nbsp;       "horaFin": "03:41:23",

&nbsp;       "denominacion_ambi": “Parque Infantil”,

&nbsp;       "dniPers": “78720904”

&nbsp;   }

### Crear Reserva

Descripción: Permite registrar una nueva reserva.

Método: POST

URL: <https://api-x0nz.onrender.com/v1/reservas/>

Cuerpo de la solicitud (JSON):

{

"personaId": "004c4f09-ab28-4820-ac24-d7b775e92cc4", (String/UUID)

"ambienteId": "828cf164-8963-4754-9617-5b605545d80a", (String/UUID)

"fechaReserva": "28-12-2024", (Date: DD/MM/YY)

"fechaSolicitud": "06-12-2024", (Date: DD/MM/YY)

"totalRese": 40, (integer)

"pago_estadoRese": "Pendiente", (String)

"horaInicio": "17:54:57", (Date: HH:mm:ss)

"horaFin": "19:54:57", (Date: HH:mm:ss)

"denominacion_ambi": "Canchita Fútbol 1", (String)

"dniPers": "78720903" (String)

}

### Actualizar Reserva

Descripción: Permite actualizar una nueva reserva.

Método: PUT

URL: <https://api-x0nz.onrender.com/v1/reservas/>

Cuerpo de la solicitud (JSON):

{

"id": "993c999b-3bdf-4474-9fab-73b8509b61be", (String/UUID)

"personaId": "004c4f09-ab28-4820-ac24-d7b775e92cc4", (String/UUID)

"ambienteId": "828cf164-8963-4754-9617-5b605545d80a", (String/UUID)

"fechaReserva": "28-12-2024", (Date: DD/MM/YY)

"fechaSolicitud": "06-12-2024", (Date: DD/MM/YY)

"totalRese": 40, (integer)

"pago_estadoRese": "Pendiente", (String)

"horaInicio": "17:54:57", (Date: HH:mm:ss)

"horaFin": "19:54:57", (Date: HH:mm:ss)

"denominacion_ambi": "Canchita Fútbol 1", (String)

"dniPers": "78720903" (String)

}

### Eliminar Reserva

Descripción: Permite eliminar una reserva. Recibe el id por parámetro (/id)

Método: DELETE

URL: <https://api-x0nz.onrender.com/v1/personas/id>

URL Ejemplo: <https://api-x0nz.onrender.com/v1/personas/ee550587-02e0-45d8-bd59-6b34eb648f93>

Cuerpo de la respuesta (TEXT):

“Registro Eliminado”

# Pruebas de Servicio

Coleccion de pruebas de servicio del Sistema de Reservas TUSNE

Incluye:

\-Coleccion de Tests para ser importado en POSTMAN

\-HTML con el resultado de las pruebas ejecutadas
