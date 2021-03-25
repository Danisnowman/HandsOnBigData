# HandsOnBigData
------------------

![InfluxDB](https://miro.medium.com/max/2560/1*QePvkDVkr7bcdgnOzeYyAQ.jpeg)

Como parte del ejercicio de este artículo, vamos a:
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

Luego ingresamos los datos correspondientes
![setup initial user](src/2.png)



