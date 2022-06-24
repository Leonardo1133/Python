![speedd](https://user-images.githubusercontent.com/42939877/175611520-2757e76d-fabc-4aaa-b431-20edbd731214.jpg)


# appSpeed
Es una aplicacion en python para crear un pandas dataframe con datos de nuestra conexion a internet.

Usaremos la libreria **speedtest** para medir:

- **Download Speed**
- **Upload Speed**
- **Ping**

Luego con todos estos datos crearemos un pandas dataframe, al cual le agregaremos tambien el **datetime** para cada sample de velocidad.

### Step 1: Install speedtest
Insalamos la libreria de speedtest para hacer el test de nuestra conexion. En mi caso hice el download de speedtest en ubuntu con el sig comando:

`sudo apt install speedtest-cli`

### Step 2: Create a loop.
Creamos un bucle para ejecutar los metodos que hacen el test de nuestra conexion durante un determinado tiempo, por ej. un dia entero. Esto esta en el script de `appSpeed.py`.

### Step 3: Create a pandas Dataframe.
Con todos los datos obtenidos del bucle anterior, vamos crear un dataframe para almacenarlos. guardamos una copia de los datos como `data.csv` en el directorio `data`

### Step 4: Run appSpeed.py
Ejecutamos el script appSpeed.py en nuestra terminal de ubuntu con el siguiente comando:

`python3 appSpeed.py`

Y obtenemos por terminal los datos de la siguiente manera:

![speedNet](https://user-images.githubusercontent.com/42939877/175649326-eb6b7a0b-bc46-4730-a3b9-9ad27e70f2ed.png)

### Next Step: Run with Docker
El próximo nivel para esta aplicación es implementar la ejecución del monitoreo de la conexión a internet con un contenedor de docker. Esto permitirá aislar la aplicación de nuestro sistema, y dejarla ejecutando durante todo el día. Esta implementacion estara disponible en el [repo de Docker](https://github.com/Leonardo1133/Docker).

