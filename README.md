#README 
#TRABAJO INDIVIDUAL-DIA1-

- Nombre: Darlyn Alejandra veliz Mamani
- NroCel: 77433898
- Correo: darlinalejandra87@gmail.com

##Clase1
# que es GIT ?

bueno git es un controlador de versiones  eso se podria decir en resumen 

## Como nacio GIT ?

bueno git basicamente nacio en abril de 2005  fue creado por linus torvalds
en si git nacio por qeu  pues  su creador se enojo por que   habian cosas inefficientes y se puso a crear git 

### Como instalar GIT ?

- primero  se debe ir ala pagina oficial de git para descargarlo una vez descargado para 
tu sistema operativo que tengas  
lo instalas  despues  abres ya tu gitbash  y lo configuras con los siguientes comandos


git config --global user.name "Adriana"

git config --global user.email "adriana88@gmail.com" 

 asi usas tu nombre de tu correo y tu correo  de github  eso basicamente  en resumen
 
#//////--------///////----------//////----------////////--------/////////-----#

#clase 2 

continuando  aprendiendo git 
- continuando en la clase de hoy se avanzo lo siguiente

### comandos para guardar y para restaurar un archivo en git 

el comando  git add . que guarda todos los cambios que realizaste  despues de modificar
 un archivo o crearlo desde cero 

tambien se hablo de como modificar un archivo y como se muestra cuando lo modificas
 lo guardas y lo borras y ,despues lo restauras  con el comando 
 
git restore nombre del archivo 
 tambien s ehablo del comando del  git reset 
-tambien se hablo de buenas practicas de como hacer  commits correctamente
-tamnbien  otras buenas practicas  como hacer commits en ingles  basicamente
 eso  se iso en la clase2 

-#-------#-----------#-----------#----------------#-----------#------------------#-----------------#------------
## Clase 3 

# como crear cuenta en github

-primero busco  en el buscador git hub  y se registro con una cuenta normal 
una vez registrado ya y verificado  configurarlo poner el nombreque se vera en
 los commits
 que aras y los cambios que subiras a los repositorios
 con los cuales trabajaras  

## como crear un repositorio en github  
- primero entro  a Github y hago login  con mi cuenta 
- luego busco el boton  que dice (New o nuevo  repositorio) 
- escribo el nombre de mi repositorio por ejemplo (nuevo proyecto )
- puedo agregare una descripcion corta opcional 
-  elijo  si quiero que sea publico o  privado 
- marco la opcion de README  si quiero que se cree un archivo inicial 
-  finalmente ago clik en crear el repositorio 
### comandos basicos de git crear ramas subir cambios clonar repsoitorio 
- basicamente  explico como  crear uan rama con el siguiente comando ejemplo 
git checkout -b nueva-funcion
- despues como clonar el repositorio con 
git clone enlace del repositorio
- tambien como  sunnbir cambios despues de hacer commit  para subir cambios ala rama 
git push 
y git pull para traer los cambios de develop a tu rama 
basicamente eso 
## clase 5
#Bifurcaciones (ramas) en Git – mis apuntes
- En Git, una bifurcación o rama es cuando el proyecto se divide en otro camino para poder trabajar sin afectar el principal.
Sirve para probar cosas nuevas, hacer cambios o avanzar en una parte del trabajo sin arruinar lo que ya funciona.

La rama principal se llama main y ahí va el proyecto que ya está listo o en producción.
La rama develop se usa para ir probando los cambios antes de pasarlos a main, por eso se considera pre-producción.

Para crear una rama puedo usar git branch, que solo crea la rama, pero no me cambia a ella.
Si quiero crear la rama y cambiarme de una vez, uso git checkout -b.

Para moverme entre ramas puedo usar git checkout, que es el comando clásico, o git switch
 que es más nuevo y solo sirve para cambiar de rama.

Cuando ya terminé de usar una rama y no la necesito más, la puedo borrar con git branch -d.

En clase vimos que es mejor trabajar en develop, hacer los cambios ahí con el editor de código 
(como Visual Studio Code, NetBeans o BlueJ), y cuando todo está bien, unirlo a main.

Este modo de trabajar se conoce como Git Flow, y ayuda a tener el proyecto ordenado y sin errores.
##Clase 6
 
### Apuntes de Git (ramas, merge y comandos)

Hoy vimos cómo trabajar mejor con ramas en Git, especialmente usando `main` y `develop`.

Primero entendí que:

* **main** es la rama principal donde debe estar todo ya funcionando bien (como versión final)
* **develop** es donde se va trabajando y probando antes de pasar a main

O sea, no se trabaja directo en main, todo pasa primero por develop.

---

Después vimos un comando para ver los commits:

```bash
git log --graph --oneline --all
```

Esto sirve para ver todo el historial pero de forma más clara.
Muestra como un dibujo de las ramas, los commits en una sola línea 
y todo lo que hay en el proyecto.
Me ayuda a entender cómo se unieron las ramas y qué cambios hubo.

---

Luego empezamos con el **merge**.

El profe dijo que merge significa **fusionar**, o sea unir ramas.
Sirve para juntar los cambios de una rama con otra.

---

Para hacer merge primero hizo esto:

```bash
git checkout develop
```

Con esto se cambia a la rama develop.

Luego dijo que **ANTES de trabajar o subir cambios siempre hay que hacer esto**:

```bash
git fetch
```

Esto trae los cambios del repositorio remoto pero no los mezcla todavía.

Después:

```bash
git pull origin develop
```

Esto ya trae los cambios y los mezcla con mi rama develop local.
O sea, con esto ya estoy actualizado.

---

Después de eso ya se puede hacer merge de otra rama, algo así:

```bash
git merge nombre-rama
```

Esto lo que hace es juntar los cambios de esa rama con develop.

---

También vimos cómo borrar una rama:

```bash
git branch -D nombre-rama
```

Sirve para eliminar ramas que ya no se necesitan.

---

Luego hablamos de los **conflictos**.

Esto pasa cuando dos ramas modifican lo mismo.
Entonces Git no sabe cuál cambio dejar.

Para arreglarlo:

1. Se editan los archivos manualmente
2. Se guarda lo correcto
3. Luego:

```bash
git add .
git commit
```

El commit puede hacerse sin mensaje, Git abre uno automático.

---

También vimos algunos comandos útiles:

```bash
git remote -v
```

Esto muestra a qué repositorio remoto está conectado.

```bash
git config --list
```

Muestra toda la configuración de Git.

```bash
git config user.name "Mi Nombre"
git config user.email "miemail@gmail.com"
```

Esto sirve para configurar mi nombre y correo, que salen en los commits.

---

Con esto ya entiendo mejor cómo trabajar con ramas y merges en Git.

