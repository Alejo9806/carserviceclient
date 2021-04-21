# CarServiceClient

Para realizar el trebajo empece creando dos componentes owner-edit y owner-list y tambien cree un servicio donde 
consumiria las api relacionadas con los owners este servicio se llama owner. Lo primero fue crear el metodo getAll() en el servicio owner este metodo me devolveria todos los owners de la api "https://thawing-chamber-47973.herokuapp.com/owners", luego en el componente owner-list importe el servicio owner y utilice el metodo getAll()
con esto obtenia todos los owners los organice en un vector y lo muestro en pantalla en una lista.

Luego cree el metodo getOwner() el cual sirve para obtener un owner en especifico y consumia la api
"https://thawing-chamber-47973.herokuapp.com/owners/search/findByDni/?dni=" con este le mandaba el dni como parametro al metodo y obtenia el owner. Este metodo fue usado en el compente edit para actualizar un owner me llenaba el formulario con sus datos tambien fue usado en el componente car-list para poder hacer una relacion entre el carro y owner. 

Para guardar y actualizar se creo un metodo save el cual si recibe un parametro "href" actualizara el owner por el contrario si no lo recibe es porque va a crear un nuevo usuario, este meetodo fue utilizado en el componente owner-edit para la creacion y actualizacion de owners.

Por ultimo el metodo remove del servicio owner borrara el owner seleccionado el cual recibe un parametro "href" para realizar esta accion, este metodo fue utilizado en el componente owner-edit con un boton llamado Delete.

Se utilizaron comprobaciones para verificar si el dni que tiene el carro existe, si el dni no existe este arrojara que el no existe un owner con ese dni.