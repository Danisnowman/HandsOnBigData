# HandsOnBigData
------------------

![InfluxDB](https://miro.medium.com/max/2560/1*QePvkDVkr7bcdgnOzeYyAQ.jpeg)

Como parte del ejercicio, vamos a:
1. Configurar rápidamente el InfluxDB2.0 en nuestra máquina local
2. Llenar algunos datos de muestra
3. Consultar con Flux

## Pasos: 

### 1. Crear un servicio utilizando docker-compose 

1.1 Creamos el archivo docker-compose.yml


```yaml
version: "2.1"

services:

  influxdb:
    hostname: influxdb
    image: quay.io/influxdb/influxdb:v2.0.3
    container_name: influxdb
    ports:
        - 8099:8086
```

1.2 Luego corremos el docker-compose


```bash
docker-compose up
```

1.3 Chequeamos que el servicio esté funcionando bien
Para eso abrimos el siguiente url: [http://localhost:8099](http://localhost:8099)

Debería aparecer lo siguiente:

![get started](src/1.png)

1.4 Hacemos click en "Get Started"

### 2. Ingresamos la configuración del usuario

2.1 Luego ingresamos los datos correspondientes:

# Organization Name: ufm
# Bucket Name: test

![setup initial user](src/2.png)

2.2 Después de dar click en "Continue", se nos pedirá que completemos la configuración.

2.3 Seleccionar la opción "Quick Start" para realizar la configuración rápida y omitir complejidades.

![quick start](src/3.png)

2.4 Cuando la configuración este lista, nos mostrará la siguiente página de control:

![dashboard page](src/4.png)

### 3. Comprobar los Buckets disponibles

'Un bucket es una ubicación con nombre donde se almacenan los datos de las series temporales. Todos los buckets tienen una política de retención, una duración de tiempo que cada punto de datos persiste. Un bucket pertenece a una organización.'


#### 4. Cargar data en el bucket







