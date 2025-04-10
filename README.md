<p align="center"><img src="https://i.postimg.cc/YCw50nSn/borg.png" width="600px" height="250px"></p>
<h3>📥 Script para realizar copias de seguridad de tus archivos</h3>
<p>Este script es un ejemplo para que puedas realizar backups de tus archivos utilizando la utilidad BorgBackup en Linux.</p>
<p>Está adaptado para que haga una copia de dos directorios personales y una base de datos. Pero puedes readaptarlo de la manera que mejor te vaya.</p>
<p>El script está pensado para que funcione conjuntamente con la utilidad Cron de Linux.</p>
<br>
<h3>❗Detalles a tener en cuenta para adaptar el script❗</h3>
<ul>
  <li>El script espera que el repositorio donde guardas tus backups de Borg esté cifrado, es decir, que cuente con contraseña.</li>
  <li>Necesitarás crear un archivo ".borg-passphrase" donde guardarás únicamente la contraseña de tu repositorio de backups de Borg.</li>
  <li>Escribe la ruta absoluta en la variable PASSPHRASE_FILE donde se sitúa el archivo ".borg-passphrase".</li>
  <li>Escribe la ruta absoluta del repositorio Borg.</li>
  <li>Escribe las rutas absolutas de los directorios que quieres hacer backup.</li>
  <li>Escribe la ruta donde quieres que se guarde el dump de la base de datos temporal mientras funciona el script.</li>
  <li>Crea el archivo ".my.cnf" en la carpeta /home/$USER. Este archivo será de utilidad para el comando "mysqldump".</li>
  <li>En el comando "mysqldump", "borg create" y "rm" debes especificar el nombre de tu base de datos.</li>
</ul>
<br>
<h3>🚀 Procedimiento para darle uso</h3>
<ol>
  <li>Instalar borgbackup en tu sistemas: apt install borgbackup</li>
  <li>Iniciar el script de la siguiente manera: ./initbackup o bash initbackup</li>
</ol>
