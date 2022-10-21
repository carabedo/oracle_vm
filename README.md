# ORACLE Virtual Machines (gratis por siempre*)


Ejemplo en oracle:

Creamos una vm [aca](https://cloud.oracle.com/compute/instances?region=sa-vinhedo-1)

### setear flask en una vm:

https://developer.oracle.com/oracle-cloud-infrastructure/compute-vm-simple-tutorial/
https://docs.oracle.com/es-ww/iaas/developer-tutorials/tutorials/flask-on-ubuntu/01oci-ubuntu-flask-summary.html

### instalar conda en oracle linux 7

https://deeplearning.lipingyang.org/2018/12/24/install-miniconda-on-centos-7-redhat-7/


## Oracle

### Instalamos conda: 

es una VM vacia, necesitamos instalar todas las librerias que vamos a usar

`wget https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh`

`sh Miniconda3-latest-Linux-x86_64.sh`


# Flask en una vm (oracle)

* levantemos un servidor de flask en nuestra vm, guardamos el codigo en `app.py`.

`flask run --host=0.0.0.0`

* abrimos el puerto donde esta flask:

`sudo iptables -I INPUT 6 -m state --state NEW -p tcp --dport 5000 -j ACCEPT`

* agregamos una `Ingress Rules` en la `Security List` de la subnet asociada a nuestra VM desde la pagina de oracle.


ahora nuestra 'app' es accesible desde cualquier maquina




* http://193.123.110.190:5002/?a=4

