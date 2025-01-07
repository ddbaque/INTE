## **1. Protocolo IP (Internet Protocol)**  

### **1.1 Filosofía de Trabajo del Protocolo IP**  
- **Protocolo de nivel de red:** Permite el envío de datos entre redes distintas, independientemente del hardware o tecnología utilizada.  
- **Escalabilidad:** Está diseñado para que la red pueda crecer sin interrupciones.  
- **Flexibilidad:** Puede operar en cualquier host, router o red.  
- **No orientado a conexión:** Los paquetes (datagramas) son enviados de forma independiente, sin establecer previamente una conexión entre el origen y el destino.  
- **Best Effort:** IP hace lo posible para entregar los paquetes, pero no garantiza entrega ni orden.  
- **Fiabilidad en niveles superiores:** Los protocolos de nivel de transporte (ej. TCP) son los que aseguran la fiabilidad de la comunicación.  

---

### **1.2 Características del Datagram IP**  
- **Unidad mínima de transferencia (PDU):** El datagrama es la unidad básica que utiliza IP para enviar información.  
- **Capas superiores:** Los datos enviados provienen de niveles superiores (aplicación y transporte).  
- **Sin conexión:** Cada datagrama es independiente, sin información de estado previa.  

---

### **1.3 Encapsulamiento IP**  
- Los datagramas IP son encapsulados dentro de una trama de nivel de enlace (ej. Ethernet, X.25).  
- **Encapsulación en Ethernet:** Se añaden cabeceras específicas a nivel de enlace.  
- **Compatibilidad con otras tecnologías:** IP puede operar sobre diferentes tipos de redes físicas (ej. X.25, Frame Relay).  

---

## **2. Función de Encaminamiento IP**  

### **2.1 Enrutamiento de Datagramas**  
- La función principal de IP es aceptar datos de TCP o UDP, crear datagramas y enviarlos al destino adecuado a través de la red.  
- **Herramientas clave:**  
   - **Máscara de subred:** Permite determinar si una dirección IP de destino está en la misma subred.  
   - **Tablas de encaminamiento:** Dictan la ruta que debe seguir un datagrama.  

---

### **2.2 Máscara de Subred**  
- **Función principal:** Determinar si una dirección IP de destino pertenece a la misma red que la dirección IP de origen.  
- **Ejemplo práctico:**  
   - IP: 147.083.140.091 / Máscara: 255.255.255.000 → Red: 147.083.140.000.  

---

### **2.3 Tabla de Encaminamiento**  
- **Estructura:** Cada dispositivo (host o router) tiene una tabla de encaminamiento.  
- **Reglas básicas:**  
   1. Buscar una coincidencia exacta con la dirección IP de destino.  
   2. Buscar una coincidencia con la subred de destino.  
   3. Utilizar la ruta por defecto si no hay coincidencias.  
- **Filosofías de gestión:**  
   - **Vector de distancia:** Calcula rutas en función de la cantidad de saltos.  
   - **Estado de enlace:** Evalúa dinámicamente el estado de los enlaces para determinar la mejor ruta.  

---

## **3. Fragmentación y Reensamblaje de Datagramas IP**  

### **3.1 Fragmentación de Datagramas**  
- Cuando un datagrama IP supera el tamaño máximo de transmisión (MTU), se fragmenta en múltiples paquetes más pequeños.  
- **Parámetros importantes:**  
   - **Offset:** Indica la posición de un fragmento en relación al datagrama original.  
   - **Flag MF (More Fragments):** Indica si hay más fragmentos por venir.  

---

### **3.2 Reensamblaje de Fragmentos**  
- Se realiza únicamente en el destino final.  
- **Parámetros de reensamblaje:**  
   - Identificador único para cada datagrama.  
   - Adresas IP de origen y destino.  
- **Problemas comunes:**  
   - Pérdida de fragmentos.  
   - Falta de información sobre el tamaño total del datagrama.  

---

## **4. Formato del Datagram IP**  

### **4.1 Componentes Principales:**  
- **Versión:** IPv4 o IPv6.  
- **Longitud de la cabecera:** Indica el tamaño de la cabecera.  
- **Tipo de servicio (TOS):** Define prioridades para la entrega de paquetes.  
- **Tiempo de vida (TTL):** Limita la permanencia de un paquete en la red.  
- **Checksum:** Detecta errores en la cabecera.  

### **4.2 Opciones Especiales:**  
- **Encaminamiento de fuente:** Define una ruta específica para los datagramas.  
- **Registro de ruta:** Almacena las direcciones IP por las que pasa el datagrama.  
- **Timestamp:** Registra la hora exacta en cada nodo.  

---

## **5. Protocolo ICMP (Internet Control Message Protocol)**  

### **5.1 Función Principal:**  
- Informa errores relacionados con la transmisión de datagramas.  
- Facilita el descubrimiento de rutas y la resolución de problemas.  

### **5.2 Tipos de Mensajes ICMP:**  
- **Error:**  
   - Destino inalcanzable.  
   - Tiempo de vida agotado.  
   - Problema en los parámetros.  
- **Consulta:**  
   - Ping (eco).  
   - Timestamp.  

---

## **6. IPv6 (IP Versión 6)**  

### **6.1 Mejoras sobre IPv4:**  
- Espacio de direcciones más amplio (128 bits).  
- Simplificación del formato de cabecera.  
- Seguridad integrada (IPSec).  
- Gestión más eficiente de la fragmentación.  

### **6.2 Fragmentación:**  
- Se realiza únicamente en el origen.  
- Uso de *Path MTU Discovery* para evitar fragmentaciones innecesarias.  

---

## **7. Protocolo IPSec (IP Security Protocol)**  

### **7.1 Objetivo:**  
- Proporcionar seguridad a nivel de red (autenticación, confidencialidad e integridad).  
- Se implementa tanto en IPv4 como en IPv6.  

### **7.2 Modos de Operación:**  
- **Transporte:** Protege únicamente los datos.  
- **Túnel:** Protege todo el paquete IP.  

---

## **8. Conclusión**  
- **IP:** Facilita la comunicación entre redes heterogéneas.  
- **ICMP:** Proporciona información de control y errores.  
- **IPv6:** Soluciona limitaciones de IPv4.  
- **IPSec:** Proporciona una capa adicional de seguridad.  

