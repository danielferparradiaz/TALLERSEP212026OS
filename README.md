<div align="center">

# 🐧 Taller de Scripting con la Shell de Bash

**Sistemas Operativos · Septiembre 2026**

![Bash](https://img.shields.io/badge/Hecho%20con-Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white)
![Linux](https://img.shields.io/badge/OS-Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![Ejercicios](https://img.shields.io/badge/ejercicios-27-0078D4?style=flat-square)
![Estado](https://img.shields.io/badge/estado-completado-2EA44F?style=flat-square)

```
          .--.
         |o_o |
         |:_/ |
        //   \ \
       (|     | )
      /'\_   _/`\
      \___)=(___/
   ~ Tux aprueba este taller ~
```

**Estudiante:** Daniel Fernando Parra Diaz· **Correo:** danielferparradiaz@gmail.com · **Código:** 2246997
</div>

---

## 📖 Descripción

Colección de los **27 ejercicios** del taller de Shell Scripting con Bash, orientados a familiarizarse con la shell y, en los ejercicios finales, a usar scripts como **herramientas de gestión de procesos y del sistema operativo**.

Cada script fue renombrado con un nombre descriptivo según lo que hace, conservando su número original de la guía (`guia.txt`) para trazabilidad.

---

## 🗂️ Índice de ejercicios

### Nivel 1 · Fundamentos 🟢

| # | Script | Qué hace |
|---|--------|----------|
| 1 | `ej01_variables.sh` | Declara variables (`name`, `age`) y las muestra con `echo` |
| 2 | `ej02_leer_numero.sh` | Lee un número del usuario con `read` y lo muestra |
| 3 | `ej03_concatenar.sh` | Concatena dos cadenas dentro de una variable |
| 4 | `ej04_suma.sh` | Suma dos números con aritmética `$(( ))` |
| 5 | `ej05_resta.sh` | Calcula la diferencia de dos números |
| 6 | `ej06_aleatorio.sh` | Genera un número aleatorio entre 1 y 50 con `$RANDOM` |
| 7 | `ej07_calculadora.sh` | Calculadora: suma, resta, multiplicación y división de dos números |

### Nivel 2 · Lógica: condicionales, bucles y arrays 🟡

| # | Script | Qué hace |
|---|--------|----------|
| 8 | `ej08_par_impar.sh` | Determina si un número es par o impar (`if` + módulo) |
| 9 | `ej09_pares.sh` | Imprime los números pares del 1 al 10 con un bucle `for` |
| 10 | `ej10_tabla_multiplicar.sh` | Muestra la tabla de multiplicar de un número (1 al 10) |
| 11 | `ej11_suma_digitos.sh` | Suma los dígitos de un número con un bucle `while` |
| 12 | `ej12_factorial.sh` | Calcula el factorial de un número |
| 13 | `ej13_suma_naturales.sh` | Suma los primeros N números naturales |
| 14 | `ej14_min_max.sh` | Encuentra el menor y el mayor elemento de un array |
| 15 | `ej15_promedio.sh` | Calcula el promedio de un array leído por teclado (`read -a`) |

### Nivel 3 · Sistema operativo, archivos y red 🟠

| # | Script | Qué hace |
|---|--------|----------|
| 16 | `ej16_copiar_archivo.sh` | Copia un archivo a una ruta destino validando que exista (`cp`, `readlink`) |
| 17 | `ej17_ping.sh` | Verifica si un host remoto está activo usando `ping` |
| 18 | `ej18_puerto.sh` | Verifica si un puerto TCP está abierto o cerrado con `nc` (netcat) |
| 19 | `ej19_internet.sh` | Comprueba si hay conexión a Internet |
| 20 | `ej20_proceso.sh` | Indica si un proceso está corriendo o no con `pgrep` |
| 21 | `ej21_top_cpu.sh` | Top 10 de procesos que más CPU consumen (`ps`, `sort`, `head`) |
| 22 | `ej22_top_memoria.sh` | Top 10 de procesos que más memoria consumen |
| 23 | `ej23_usuarios.sh` | Cuenta los usuarios con sesión iniciada (`who`) |
| 24 | `ej24_info_os.sh` | Muestra nombre, versión, release y arquitectura del SO |
| 25 | `ej25_uso_memoria.sh` | Muestra el porcentaje de memoria RAM en uso (`free`, `awk`) |

### Nivel 4 · Herramientas completas 🔴

| # | Script | Qué hace |
|---|--------|----------|
| 26 | `ej26_menu.sh` | Menú interactivo de información del sistema (info, disco, espacio home) con `case` |
| 27 | `ej27_reporte_red.sh` | **Requiere root.** Genera `network.<fecha>.info.txt` con toda la configuración de red (distro, PCI, rutas, DNS, firewall, netstat, sysctl) |

---

## 🚀 Cómo ejecutar

```bash
# Opción 1: dar permiso de ejecución
chmod +x ej01_variables.sh
./ej01_variables.sh

# Opción 2: ejecutar directamente con bash
bash ej01_variables.sh
```

### Pruebas rápidas (sin escribir a mano)

```bash
printf '8\n'          | bash ej08_par_impar.sh      # -> even
printf '7\n'          | bash ej12_factorial.sh      # -> 5040
printf '24 27 84\n'   | bash ej15_promedio.sh       # -> 45
printf 'bash\n'       | bash ej20_proceso.sh        # -> Process is running.
```

> 💡 En Windows puedes ejecutarlos desde **WSL** o **Git Bash**. Los ejercicios 17–27 son específicos de Linux (`ping`, `nc`, `ps`, `free`, etc.).

---

## 📦 Requisitos

- Linux (o WSL/Git Bash) con **Bash 4+**
- Herramientas estándar: `ping`, `nc`, `ps`, `free`, `who`, `uname`, `awk`, `sort`
- El ejercicio 27 además necesita `iptables`, `lspci`, `route`, `netstat`, `lsb_release` y **permisos de root**

---

## 🐄 Bonus: la terminal también es divertida

```bash
# La vaca más sabia del universo
sudo apt install cowsay fortune-mod
fortune -s | cowsay

# Tux te da la respuesta a todo
echo "¿Debo entregar el taller a tiempo?" | cowsay -f tux

# El tren que aparece cuando escribes mal 'ls'
sudo apt install sl
sl

# Matrix en tu terminal
sudo apt install cmatrix
cmatrix
```

> ⚠️ Regla no escrita de Linux: si algo se rompe, primero revisa que no hayas escrito `sl` queriendo escribir `ls`. 🚂

---

## 📝 Notas y correcciones
- `ej27`: genera el archivo `network.<dd-mm-yy>.info.txt` — **ese es el adjunto que se envía con el taller resuelto**.
- La guía original del taller está en [`guia.txt`](guia.txt).
