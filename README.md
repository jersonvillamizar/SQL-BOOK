### Bloque 1

##### Consultas

1. Listar los nombres de los usuarios

   ```sql
     SELECT nombre FROM tblusuarios;
   ```

2. Calcular el saldo máximo de los usuarios de sexo “Mujer”

     ```sql
     SELECT MAX(saldo) AS sueldo_max, nombre FROM tblusuarios WHERE sexo ='M';
     ```

3. Listar nombre y teléfono de los usuarios con teléfono NOKIA, BLACKBERRY o SONY

     ```sql
     SELECT nombre, telefono, marca FROM tblusuarios WHERE marca IN ('SONY', 'BLACKBERRY', 'NOKIA') ORDER BY marca;
     ```

4. Contar los usuarios sin saldo o inactivos

     ```sql
     SELECT SUM(activo = 0 OR saldo = 0) AS usuarios_sin_saldo_o_inactivos FROM tblusuarios;
     ```

5. Listar el login de los usuarios con nivel 1, 2 o 3

     ```sql
     SELECT usuario, email, nivel FROM tblusuarios WHERE nivel BETWEEN 1 AND 3 ORDER BY nivel;
     ```

6. Listar los números de teléfono con saldo menor o igual a 300

     ```sql
     SELECT telefono, saldo FROM tblusuarios WHERE saldo <= 300 ORDER BY saldo;
     ```

7. Calcular la suma de los saldos de los usuarios de la compañia telefónica NEXTEL

     ```sql
     SELECT SUM(saldo) AS saldo_total_NEXTEL FROM tblusuarios WHERE compañia = 'NEXTEL';
     ```

8. Contar el número de usuarios por compañía telefónica

     ```sql
     SELECT COUNT(usuario) AS numero_usuarios, compañia FROM tblusuarios GROUP BY compañia ORDER BY numero_usuarios;
     ```

9. Contar el número de usuarios por nivel

     ```sql
     SELECT COUNT(usuario) AS numero_usuarios, nivel FROM tblusuarios GROUP BY nivel ORDER BY nivel;
     ```

10. Listar el login de los usuarios con nivel 2

      ```sql
     SELECT usuario, email FROM tblusuarios WHERE nivel = 2;
      ```

11. Mostrar el email de los usuarios que usan gmail

      ```sql
     SELECT email FROM tblusuarios WHERE email LIKE '%@gmail.com';
      ```

12. Listar nombre y teléfono de los usuarios con teléfono LG, SAMSUNG o MOTOROLA

      ```sql
     SELECT nombre, telefono, marca FROM tblusuarios WHERE marca IN ('LG', 'SAMSUNG', 'MOTOROLA') ORDER BY marca;
      ```

------

### Bloque 2

##### Consultas

1. Listar nombre y teléfono de los usuarios con teléfono que no sea de la marca LG o SAMSUNG

     ```sql
     SELECT nombre, telefono, marca FROM tblusuarios WHERE marca NOT IN ('LG', 'SAMSUNG') ORDER BY marca;
     ```

2. Listar el login y teléfono de los usuarios con compañia telefónica IUSACELL

     ```sql
     SELECT nombre, email, telefono FROM tblusuarios WHERE compañia = 'IUSACELL';
     ```

3. Listar el login y teléfono de los usuarios con compañia telefónica que no sea TELCEL

     ```sql
     SELECT nombre, email, telefono, compañia FROM tblusuarios WHERE NOT compañia = 'TELCEL' ORDER BY compañia;
     ```

4. Calcular el saldo promedio de los usuarios que tienen teléfono marca NOKIA

     ```sql
     SELECT AVG(saldo) AS saldo_promedio FROM tblusuarios WHERE marca = 'NOKIA';
     ```

5. Listar el login y teléfono de los usuarios con compañia telefónica IUSACELL o AXEL

     ```sql
     SELECT nombre, email, telefono, compañia FROM tblusuarios WHERE compañia IN ('IUSACELL', 'AXEL');
     ```

6. Mostrar el email de los usuarios que no usan yahoo

     ```sql
     SELECT email FROM tblusuarios WHERE NOT email LIKE '%yahoo.com' ORDER BY SUBSTRING_INDEX(email, '@', -1);
     ```

7. Listar el login y teléfono de los usuarios con compañia telefónica que no sea TELCEL o IUSACELL

     ```sql
     SELECT nombre, email, telefono, compañia FROM tblusuarios WHERE NOT compañia IN ('TELCEL', 'IUSACELL') ORDER BY compañia;
     ```

8. Listar el login y teléfono de los usuarios con compañia telefónica UNEFON

     ```sql
     SELECT nombre, email, telefono FROM tblusuarios WHERE compañia = 'UNEFON';
     ```

9. Listar las diferentes marcas de celular en orden alfabético descendentemente

     ```sql
     SELECT DISTINCT marca FROM tblusuarios ORDER BY marca DESC;
     ```

10. Listar las diferentes compañias en orden alfabético aleatorio

      ```sql
     SELECT DISTINCT compañia FROM tblusuarios ORDER BY RAND();
      ```

11. Listar el login de los usuarios con nivel 0 o 2

      ```sql
     SELECT usuario, email, nivel FROM tblusuarios WHERE nivel IN (0, 2) ORDER BY nivel;
      ```

12. Calcular el saldo promedio de los usuarios que tienen teléfono marca LG

      ```sql
     SELECT AVG(saldo) AS saldo_LG FROM tblusuarios WHERE marca = 'LG';
      ```

------

### Bloque 3

##### Consultas

1. Listar el login de los usuarios con nivel 1 o 3

     ```sql
     SELECT usuario, email, nivel FROM tblusuarios WHERE nivel IN (1, 3) ORDER BY nivel;
     ```

2. Listar nombre y teléfono de los usuarios con teléfono que no sea de la marca BLACKBERRY

     ```sql
     SELECT nombre, telefono, marca FROM tblusuarios WHERE NOT marca = 'BLACKBERRY' ORDER BY marca;
     ```

3. Listar el login de los usuarios con nivel 3

     ```sql
     SELECT usuario, email FROM tblusuarios WHERE nivel = 3;
     ```

4. Listar el login de los usuarios con nivel 0

     ```sql
     SELECT usuario, email FROM tblusuarios WHERE nivel = 0;
     ```

5. Listar el login de los usuarios con nivel 1

     ```sql
     SELECT usuario, email FROM tblusuarios WHERE nivel = 1;
     ```

6. Contar el número de usuarios por sexo

     ```sql
     SELECT COUNT(usuario) AS cantidad_usuarios, sexo FROM tblusuarios GROUP BY sexo;
     ```

7. Listar el login y teléfono de los usuarios con compañia telefónica AT&T

     ```sql
     SELECT nombre, email, telefono FROM tblusuarios WHERE compañia = 'AT&T';
     ```

8. Listar las diferentes compañias en orden alfabético descendentemente

     ```sql
     SELECT DISTINCT compañia FROM tblusuarios ORDER BY compañia DESC;
     ```

9. Listar el logn de los usuarios inactivos

     ```sql
     SELECT usuario, email FROM tblusuarios WHERE activo = 0;
     ```

10. Listar los números de teléfono sin saldo

      ```sql
     SELECT telefono FROM tblusuarios WHERE saldo = 0;
      ```

11. Calcular el saldo mínimo de los usuarios de sexo “Hombre”

      ```sql
     SELECT MIN(saldo) FROM tblusuarios WHERE sexo = 'M';
      ```

12. Listar los números de teléfono con saldo mayor a 300

      ```sql
     SELECT telefono FROM tblusuarios WHERE saldo >= 300;
      ```

------

### Bloque 4

##### Consultas

1. Contar el número de usuarios por marca de teléfono

     ```sql
     SELECT COUNT(usuario) AS cantidad_de_usuarios, marca FROM tblusuarios GROUP BY marca;
     ```

2. Listar nombre y teléfono de los usuarios con teléfono que no sea de la marca LG

     ```sql
     SELECT nombre, telefono, marca FROM tblusuarios WHERE NOT marca = 'LG' ORDER BY marca;
     ```

3. Listar las diferentes compañias en orden alfabético ascendentemente

     ```sql
     SELECT DISTINCT compañia FROM tblusuarios ORDER BY compañia ASC;
     ```

4. Calcular la suma de los saldos de los usuarios de la compañia telefónica UNEFON

     ```sql
     SELECT SUM(saldo) FROM tblusuarios WHERE compañia = 'UNEFON';
     ```

5. Mostrar el email de los usuarios que usan hotmail

     ```sql
     SELECT email FROM tblusuarios WHERE email LIKE '%@hotmail.com';
     ```

6. Listar los nombres de los usuarios sin saldo o inactivos

     ```sql
     SELECT nombre FROM tblusuarios WHERE activo = 0 OR saldo = 0;
     ```

7. Listar el login y teléfono de los usuarios con compañia telefónica IUSACELL o TELCEL

     ```sql
     SELECT usuario, email, telefono, compañia FROM tblusuarios WHERE compañia IN ('IUSACELL', 'TELCEL') ORDER BY compañia;
     ```

8. Listar las diferentes marcas de celular en orden alfabético ascendentemente

     ```sql
     SELECT DISTINCT marca FROM tblusuarios ORDER BY marca ASC;
     ```

9. Listar las diferentes marcas de celular en orden alfabético aleatorio

     ```sql
     SELECT DISTINCT marca FROM tblusuarios ORDER BY RAND();
     ```

10. Listar el login y teléfono de los usuarios con compañia telefónica IUSACELL o UNEFON

      ```sql
     SELECT nombre, email, telefono, compañia FROM tblusuarios WHERE compañia IN ('IUSACELL', 'UNEFON');
      ```

11. Listar nombre y teléfono de los usuarios con teléfono que no sea de la marca MOTOROLA o NOKIA

      ```sql
     SELECT nombre, telefono, marca FROM tblusuarios WHERE NOT marca IN ('MOTOROLA', 'NOKIA') GROUP BY marca;
      ```

12. Calcular la suma de los saldos de los usuarios de la compañia telefónica TELCEL

      ```sql
     SELECT SUM(saldo) AS saldo_total_NEXTEL FROM tblusuarios WHERE compañia = 'TELCEL';
      ```