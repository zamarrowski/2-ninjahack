### Descripción

Para este ninjahack se ha creado un mundo virtual que genera actividad financiera. Esta actividad es la 
que se va a publicar en los streams de SeMaaS. 
  
### Características

### Datos físicos

* Número de personas: 10000.
* Número de compaías: 550.
* Unidad minima del tiempo: 1 día.
* Geolocalizado: Madrid.
* Fecha de inicio: 5/10/2017

### Datos económicos 

* La cantidad de dinero total del mundo es fija, no se crea ni se destruye dinero.
* Todos los servicios son privados, no existe un estado central.
* Hay pleno empleo
  * Las personas pueden perder su empleo de forma puntual si la empresa no puede pagar pero encuentran inmediatamente.
* Todas las compañias ofrecen todos los servicios, no hay segmentación por sector.
* El único medio de pago es la tarjeta de crédito.
* Cada año de este mundo corresponde a media hora del mundo real, los datos serán casi siempre del futuro. 
* Los tipos de pagos son siempre el mismo tipo, no hay que hacer procesado del lenguaje natural para adivinar el concepto.

### Tipos de gastos

Cada uno de estos gastos tiene una recurrencia lógica acorde a su naturaleza y que intenta correspond

* mortgage, pagos de hipoteca, simula cualquier gasto financiero recurrente
* power_supply, gastos de electricidad. 
* water_supply, gastos de luz.
* meal, gastos de comida.
* entertainment, gastos en entretenimiento, salir con los amigos, pequeñas vacaciones, etc.
* internet, gastos por tener conexión a internet, tv por cable, teléfono
* gas, Gastos de combustible para las personas que tengan coche.
* medical_costs, costes por problemas de salud de las personas.
* car_fault, costes por averías imprevistas en el coche.
* public_transport, gastos en transporte público. Todo el mundo tiene tarjeta de transportes.
* electronic_device, compras en aparatos electrónicos.
* holidays, gastos en vacaciones.
* luxury, gastos en articulos del lujo.
* new_car, compra de un nuevo vehiculo.

###Ticks

El mundo evoluciona siguiendo un reloj único. Cada tick de ese reloj es un día de calendario.

Cada 30 ticks, se publican balances, tanto de las empresas como de las 