![Banner](https://github.com/IsuiLugo/EscaneoActivoDeVulnerabilidades/blob/main/Images/Banner%20de%20LinkedIn%20%20Azul%20Ilustrado%20Tecnolog%C3%ADa.gif?raw=true)
# Escaneo Activo y Análisis de vulnerabilidades
## Tools for Scanning
- **IP Loogger:**
  > Un IP Loogger es un servicio online que permite registrar datos de un usuario, cuando este hace uso de un enlace (link)(pulsa clic, abre el link)
    este en enlace no tiene que ser malicioso, sino más bien es parte de la etapa de inteligencia de la investigación.
    Datos que puede mostrar un IP Logger:
    - IP Addres
    - Country
    - ISP
    - Operating System
- **Banner Grabbing:**
  > Es el proceso/técnica de obtener información de la infraestructura tecnológica de una organización.
    Se logra mendiante la REQUEST de un servicio.
    Una herramienta para ello es Netcat, pero requiere de parametros
    ~~~ sh
      netcat dominio.com 80
      HEAD / HTTP /1.1
    ~~~
- **Sublist3r:**
  > Sublist3r es una herramienta para la enumeración de subdominios. Un subdominio es la parte previa a un dominio, y existe la posibilidad (es lo más común) de usar otro subdominio para configurar una aplicación en cada subdomino. Sublist3r se puede descargar [aquí](https://github.com/aboul3la/Sublist3r) o como el comando
  ~~~ sh
    sudo apt install sublist3r
  ~~~
  pero por lo general ya lo tiene instalado Kali o Parrot.
  
- **Fingerprinting de Web Apps:**
  > El fingerprinting es un tipo de huella digital, y es el más común, consiste en enviar paquetes a una víctima y esperar a la respuesta para analizar los resultados, para ello la herramienta es [Whatweb](https://morningstarsecurity.com/research/whatweb), y es muy fácil de usar, solo escribir el comando:
  ~~~ sh
    whatweb dominio.com
  ~~~
  Esto nos mostrara una lista de tecnológias que emplea la organización.

- **WAF: Web Aplication Firewall:**
  > Es un sistema que protege de mpultiples ataques al sevidor de aplicaiones web (del lado del Backend), analiza los paquetes HTTP y HTTPS. Pero no todas las organizaciones, hacen de un WAF, lo que las vuelve más vulnerables, y algunos WAF, tienen historial de vulnerabilidades criticas, de modos que si la organización no ha actualizado su Sistema, el atacante puede buscar facilmente con Google Dorks [Google Hacking](https://www.exploit-db.com/google-hacking-database) un exploit para el WAF.
  Se puede saber si un dominio hace uso de un WAF, con la herramienta waf00f, con el comando:
  ~~~ sh
    wafwoof domino.com, dominio2.com
  ~~~
  Esta herramienta ya se incluye en Kali y Parrot.
