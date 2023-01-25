# CentOS8-VagrantFile
Vagrantfile para crear máquinas virtuales con SO CentOS/8.

Con el vagrantfile de la carpeta "master" se creará una única máquina, en el script de aprovisionamiento hay varios comandos que se ejecutarán automáticamente sobre dicho host. Uno de ellos instalará la herramienta Ansible.

Con el Vagrantfile de la carpeta "clients" se crearán 4 máquinas, nuevamente en el script de aprovisionamiento podemos ver que comandos se ejecutarán sobre dichos hosts en su creación.

La idea es, desde la máquina "master" controlar los 4 hosts "clients" a través de Ansible. Para poder ejecutar correctamente algín playbook de Ansible, deberemos crear un par de claves ssh públca-privada en la máquina máster, y compartir dicha clave con los hosts clientes.

Se pueden modificar los scripts de aprovisionamiento si quieres agregar o eliminar algún comando. También se pueden cambiar algunos valores del vagrantfile, como la cantidad de memoria RAM, el número de núcleos de CPU, o las direcciones IP.

El usuario de las máquinas será "vagrant" con contraseña "vagrant".
La contraseña del usuario "root" será "toor" (se puede cambiar esto en el script de aprovisionamiento).
