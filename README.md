Pasos para probar el Pipiline

1.Clonar repo
2.agregar llaves con acceso de administrador de AWS en el vaul de Github

3.aplicar cambios en la rama Test
4. aplicar pull request , cuando este se aplica corre el flujo del github action el cual tiene 2 pasos una primera 
etapa en la que hace una terraform plan y valida que este ok , una vez este esta ok corre el gitaction para aplicar el terraform y hace el despliegue
5.aqui debes abrir la VM y entrar por SSH por ssh conect y correr el comando docker network inspect monitoring
6. con este comando sacas la ip privada que tiene el contenedor de prometheus para luego enlazarlo como data principal en el grafana
7 acceder al  grafana por la ip publica y el puerto 3000, y alli ir a conection y seleccionar data sources, escojes prometheus
8. colocas la url de prometheus: http://x.x.x.x:9090
le das tes conection y si todo va bien puedes  ya tienes conexion ok con el data sources
9 crear dashboard y le das import y colocas el ID 893 o la siguiente url https://grafana.com/grafana/dashboards/893-main/
10. ya con esto tendras en dahsboard que monitorea los contenedores
11. para aplicar el terraform destroy se hace de manera manuel debes ir action y seleccionar el yaml destroy.
