
### Namespace

SeMaaS proporciona un namespace donde van a estar todos los streams de eventos del ninjahack:

```
https://upsilon.play.global.semaas-spot.com/v1/ns/ninjahack.events.madrid

```

### Streams

Existen 3 streams de datos. Antes de usarlos es **necesario** hablar con los facilitares para que
os den permisos de seguridad para acceder a los mismos.


### Stream de datos de personas

En este stream se encuentran los datos personales públicos de la persona.

Entre ellos para este ninjahack hemos incluido el pan, este pan esta cifrado, en nuestro modelo es sustituido por un 
número secuencial para evitar que los datos de tarjetas de las personas se vean comprometidos.

Estos datos se publican de forma periódica y son una foto de como evoluciona el balance de la persona en el tiempo.

Los datos de geolocalización son en un area de unos 50 km alrededor del centro de Madrid.

#### Stream

```
 
 https://upsilon.play.global.semaas-spot.com/v1/ns/ninjahack.events.madrid/streams/personEventStream:getRecords

```

#### Mensaje

```
{
    _id: 'personEvent',
    description: 'Event when a person event changes.',
    protoSpec: {
        person: 'string',//Identificador únino de la persona
        name: 'string',
        cellPhone: 'string',
        geolocationType: {
            message: {
                latitude: 'string',
                longitude: 'string'
            }
        },
        addressType: {
            message: {
        ``````        full: 'string',
                zipCode: 'string',
                geolocation: 'geolocationType'
            }
        },
        address: 'addressType',
        balance: 'double',// Dinero que tiene la persona en la cuenta
        currency: 'string',
        date: 'string',
        pan: 'string'
    }
}
 ``` 
      
### Stream de datos de compañias      
     
Es este stream se encuentran los datos personales públicos de las compañias.

Estos datos se publican de forma periódica y son una foto de como evoluciona el balance de la compañia en el tiempo.      
           
Los datos de geolocalización son en un area de unos 50 km alrededor del centro de Madrid.
              
#### Stream

```
 
 https://upsilon.play.global.semaas-spot.com/v1/ns/ninjahack.events.madrid/streams/companyEventStream:getRecords

```

#### Mensaje     
      
```
{
    _id: 'companyEvent',
    description: 'Event when a company status changes.',
    protoSpec: {
      company: 'string',//Identificador único de la persona
      name: 'string',
      geolocationType: {
          message: {
              latitude: 'string',
              longitude: 'string'
          }
      },
      addressType: {
              message: {
                  full: 'string',
                  zipCode: 'string',
                  geolocation: 'geolocationType'
              }
          },
          address: 'addressType',
          balance: 'double',
          currency: 'string',
          date: 'string'
    }
}
 ```     

### Stream de movimientos de tarjetas

Movimientos de cada una de los pagos que se han realizado con la tarjeta de crédito.

El pan, al igual que en personas, esta cifrado, en nuestro modelo es sustituido por un 
número secuencial para evitar que los datos de tarjetas de las personas se vean comprometidos.

La geolocalización corresponde a la de la empresa en la que se realizo el pago, con variaciones de segundos debido
al GPS.


#### Stream

```

 https://upsilon.play.global.semaas-spot.com/v1/ns/ninjahack.events-test20/streams/cardMovementEventStream:getRecords

```

#### Mensaje

```
{
    _id: 'cardMovement',
    description: 'Event when a card movements occurs.',
    protoSpec: {
        pan: 'string', //Pan que ha realizado la operación
        amount: 'double',
        currency: 'string',
        company: 'string',// Identificador del compañia donde se realizo el pago
        date: 'string',
        details: 'string',//tipo de pago que se ha realizado
        geolocationType: {
            message: {
                latitude: 'string',
                longitude: 'string'
            }
        },
        geolocation: 'geolocationType'
    }
}
        
```