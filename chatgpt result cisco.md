---
marp: true
theme: uncover
paginate: true
size: 16:9
class: invert
---

# Recuperar el acceso restaurando la contrase帽a en un Router de Cisco 馃捇

Brizuela Juan Eduardo
Interconexi贸n de Redes

---

##### 1. Lo primero que tenemos que hacer, es apagar y encender nuestro Router.

![bg right:50% 100%](images/on-off.png)

---

### 2. Entrar a la CLI de Cisco.

<div>
    <img src="images/cli.png" style="width: 30rem" />
</div>

---

##### 3. Mientras est谩 en el proceso de "booteo" o de inicializaci贸n, presionar el comando `CTRL + C`. Con esto, entraremos en el modo `rommon 1`. El modo "rommon", es el modo de recuperaci贸n.

---

#### 4. Estando en este modo, tendremos que introducir el siguiente comando `confreg 0x2142`.

Con este comando el router omite la configuraci贸n de inicio almacenada en NVRAM durante su secuencia de inicio.

Esta funci贸n se utiliza normalmente durante un procedimiento de recuperaci贸n de contrase帽a.

---

### 5. Posteriormente, introducimos en la CLI: `reset`

---

#### 6. Esperamos a que vuelva a inicializarse el router, y con esto, podremos iniciar al router con su configuraci贸n de f谩brica.

---

#### 7. Para verificar esto, entramos al modo global del router con `ena`, despu茅s hacemos un `show run`, y claramente podemos ver que el router est谩 vac铆o.

---

#### 8. No hay porqu茅 preocuparse. Si se desea restaurar la informaci贸n del router sin la contrase帽a asignada, se introduce el comando: `copy start run`

---

### 9. Con base en lo aprendido en la clase, pueden establecer su nueva password/secret.

---

### 10. Sin embargo, no hemos terminado porque la configuraci贸n sigue en 0x2142.

As铆 que, entrando al modo de configuraci贸n `copy start run`, introducimos el siguiente comando: `config-register 0x2102`. La configuraci贸n predeterminada de f谩brica para el registro de la configuraci贸n.

---

#### 11. Finalmente, hacemos un `do reload` o `exit` && `do reload` para iniciar de nuevo el router. Para asegurarnos de la configuraci贸n, hacemos un `do show version`

---

# <!--fit--> 隆Gracias!
