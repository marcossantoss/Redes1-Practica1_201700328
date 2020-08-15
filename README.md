# Redes1-Practica1_201700328
##### Practica no. 1 de redes 1
##### Marcos Alberto Santos Aquino 

Software utilizado para la simulación de red: GNS3

    - Flujo de aplicación drag and drop

VMware Workstation como cliente virtualizado con SO tiny core
    
    - link descarga ISO: https://distro.ibiblio.org/tinycorelinux/downloads.html

###### Creacion de la red 
    La red construida queda de la siguiente manera.
    -Topología de red de estrella o jerarquica
![Red construida](http://imgfz.com/i/Ig6LvmQ.png)

Para crear la red se escogen los elementos que la componen, mediante la acción de darg and drop.

![Router](http://imgfz.com/i/gQEKtLO.png)

Se continua arrastrando los componentes para ir construyendo la red, para posteriormente ir configurando estos componentes

![Switch](http://imgfz.com/i/rdhtMRC.png)

Se arma mejor la red

![Continuacion](http://imgfz.com/i/ixybDGT.png)

Se presiona en el cable de la parte izquierda, para hacer la conexión entre los dispositivos 

![Conexion](http://imgfz.com/i/Ml4oq9Y.png)


###### Configuración con la maquina virtual

      Se agrega la maquina virtual a GNS3
      Se posiciona en la seccion de VMware
      Por ultimo se le da en la opcion de add
      Le apareceran las maquinas vituales asociadas con VMware
![Conexion](http://imgfz.com/i/Hw8fzWq.png)
     
![Conexion](http://imgfz.com/i/bcMpRhX.png)
       
     
##### Configuración de maquina virtual desde VMware Workstation

       Se dirige a la maquina virtual y se debe colocar en Machine Setting
       Luego busca la seccion de Netwrok adapter
       Selecciona la opción Custom para elegir un adaptador de red virtual local 
    
![Conexion](http://imgfz.com/i/O1k4aIp.png)


###### **Configuracion de red**

    1) Encender los dispositivos para configurar
    2) Configuración de router

    Se verifica con el comando:

    -	Sh ip interface brief

    Para visualizar el estado actual de la configuración de del router
    -	Configure t
    Para indicar que se configurará el router
    -	Interfaz “nombre de la interface”, en mi caso interface FastEthernet0/0
    Para especificar la interfaz a modificar
        Una vez adentro se escribe
    -	Speed 100
    -	Duplex full
    -	Ip address 192.168.18.254 255.255.255.0
    Aquí se asigna la velocidad de transmisión, la comunicación y la ip que tendrá como Gateway.
    
    -   luego exit
    -   exit
    Y Lo MAS IMPORTANTE ES GUARDAR con el comando write
    
    -   write
#### configuracion de router en consola
![Conexion](http://imgfz.com/i/mzSIrvt.png)
  
###### Configuracion de la maquina virtual

    - Se abre una terminal
    - Se consulta mediante ifconfig, para verificar el estado de la configuración
    - Se procede hacer el clic en el panel de control, -> network -> se ingresa la ip
    - Se presiona aply
    - ifconfig nuevamente para verificar que se haya realizado correctamente
  
![Conexion](http://imgfz.com/i/2LcVYnI.png)


#### ** Configuracion de las VPCs **

    Para las configuraciones de las vpc se ingresan:
    Show para observar el estado de configuración

    Show
    ip 192.168.18.30 255.255.255.0 192.168.18.254

    Para configurar una nueva ip a la vpc

    Por utlimo se escribe 
    save
    
    por ultimo se hace ping con las diferentes ips
   
       hacer ping con:

      - ping 192.168.18.30 a 192.168.12.15
      - ping 192.168.18.30 a 192.168.12.30
      - ping 192.168.18.30 a 192.168.18.15

      - ping 192.168.18.15 a 192.168.12.15
      - ping 192.168.18.15 a 192.168.12.30
      - ping 192.168.18.15 a 192.168.18.30
      
      - ping 192.168.12.15 a 192.168.12.30
      - ping 192.168.12.15 a 192.168.18.30
      - ping 192.168.12.15 a 192.168.18.15
      
      - ping 192.168.12.30 a 192.168.12.30
      - ping 192.168.12.30 a 192.168.12.30
      - ping 192.168.12.30 a 192.168.18.15
   
   ![Conexion](http://imgfz.com/i/jPXVT3O.png)
   ![Conexion](http://imgfz.com/i/JQDlE80.png)  
   ![Conexion](http://imgfz.com/i/fjVcXUz.png)  
    



