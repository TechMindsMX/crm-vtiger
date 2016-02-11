# Cambiar un usuario de una empresa a otra

//Seleccionar los campos clabe de usuarios de la base de datos
select id, user_name, enterpriseid from vtiger_users;

//Los registros que nos interesan son los siguientes
 10 | rosaana@eficazz.com                |         3703
 18 | fernanda@eficazz.com               |         3703 
 35 | rosaana@eficazz.com.mx             |         7506

//Los que identifico que hay que cambiar son los que corresponden a la 3703

//Seleccionar los campos representativos de enterprises
select enterprisesid, title from vtiger_enterprises;

//Los registros que nos interesan son los siguientes
3703 | CCRC   
7506 | Eficazz   

//Cambiando los registros del ownerid 
update vtiger_crmentity set enterpriseid=7506 where enterpriseid=3703 and smownerid=10;
update vtiger_crmentity set enterpriseid=7506 where enterpriseid=3703 and smownerid=18;

//Cambiar los registros Pasa del usuario: 

Al Brun
abvarios@gmail.com
En la empresa CCRC

Al usuario:
Alexis A Brunel
abrunel@grupoaleol.com
En la empresa GAO


