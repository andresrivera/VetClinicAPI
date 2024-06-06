# VetClinicAPI

En una clínica veterinaria, la gestión eficiente de la información es crucial para ofrecer un servicio de calidad a los clientes y sus mascotas. Actualmente, muchas clínicas veterinarias aún utilizan métodos manuales o sistemas fragmentados para gestionar la información de sus pacientes (Excel), lo que puede llevar a errores y pérdida de datos importantes. Es necesario un sistema centralizado y automatizado que permita gestionar la información de manera eficiente y segura.

## Objetivo

Desarrollar servicios web que permitan gestionar de manera integral la información de una clínica veterinaria, incluyendo la administración de mascotas, dueños, veterinarios y
citas. Este sistema debe facilitar el almacenamiento, consulta y actualización de datos, así como mantener la integridad de las relaciones entre las diferentes entidades.

## Entidades principales:
### ● Mascotas: 
Información sobre las mascotas, incluyendo nombre, especie, raza, edad y su dueño.
### ● Dueño: 
Información sobre los dueños de las mascotas, incluyendo nombre, dirección, teléfono y email.
### ● Veterinario: 
Información sobre los veterinarios, incluyendo nombre, teléfono ,años de experiencia y Correo (Deben crear 2 registros quemados en la base de datos)
### ● Cita: 
Información sobre las citas programadas, incluyendo fecha y hora, mascota, veterinaria y descripción de la cita.

```bash
http://localhost:5087/api/
```

## Usage

```python
# clonar git en escritorio local
git clone https://github.com/andresrivera/VetClinicAPI.git

# Correr comando en carpeta
dotnet watch run

```
## EndPoints

### Mascota
#### HU-1	Listar Mascotas	COMO USUARIO DEL SIS	
ver la lista de todas las mascotas 
```python
GET	/pets/
```
#### HU-2	Crear una Mascota		
registrar una nueva mascota en el sistema
```python
POST	/pets/
```
#### HU-3	Ver detalles de una Mascota		
ver los detalles de una mascota específica 	
```python
GET	/pets/{id} 
```
#### HU-4	Actualizar una Mascota		
actualizar la información de una mascota específica.	
```python
PUT	/pets/{id} 
```
### Dueño
#### HU-5	Dueño	Listar Dueños		
ver la lista de todos los dueños	
```python
GET	 /owners/ 
```
#### HU-6	Crear un Dueño		Q
registrar un nuevo dueño en el sistema.	
```python
POST	 /owners/ 
```
#### HU-7	Ver detalles de un Dueño		
ver los detalles de un dueño específico 	
```python
GET	 /owners/{id} 
```
#### HU-8	Actualizar un Dueño		
actualizar la información de un dueño específico	
```python
PUT	/owners/{id}
```
### Veterinario
#### HU-9	Listar Veterinarios		
ver la lista de todos los veterinarios 	
```python
GET	/vets/
```
#### HU-10	Ver detalles de un Veterinario		
er los detalles de un veterinario específico	
```python
GET	/vets/{id}
```
### Citas
#### HU-11	Listar Citas		
ver la lista de todas las citas programadas 	
```python
GET	/quotes/
```
#### HU-12	Programar una Cita		
programar una nueva cita en el sistema 	
```python
POST	/quotes/
```
#### HU-13	Ver detalles de una Cita		
ver los detalles de una cita específica	
```python
GET	/quotes/{id}
```
#### HU-14	Actualizar una Cita		
actualizar la información de una cita específica.	
```python
PUT	/quotes/{id}
```

### EndPoints Medios
#### HU-15	Listar citas en una fecha especifica	
ver la lista de citas que estan agendadas para una fecha en especifico	
```python
GET	/quotes/{date}/date
```
#### HU-16	Listar todas las mascotas de un dueño		
ver la lista de las mascotas que tiene una persona	
```python
GET	/pets/{id}/owner
```
#### HU-17	Listar todas las citas que ha tenido o va a tener un veterinario		
ver el listado de citas que tiene un veterinario 	
```python
GET	/quotes/{id}/vets
```
#### HU-18	Listar mascotas por fecha de cumpleaños		
ver la lista de mascotas y sus dueños para enviarles promociones y mensajes de felicitacion	
```python
GET	/pets/{date}/birthday
```


## Contributing

For major changes, please open an issue first
to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License

[MIT](https://choosealicense.com/licenses/mit/)
