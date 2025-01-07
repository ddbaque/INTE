## **1. Conceptes Bàsics**  

### **1.1 Escenari i Elements Clau**  
Els conceptes fonamentals de la seguretat en xarxes es basen en diversos elements clau:  
- **Usuaris:** Qui envia i rep informació.  
- **Algorismes:** Mètodes utilitzats per a xifrar, desencriptar i protegir dades.  
- **Missatges:** La informació transmesa entre usuaris.  
- **Xarxes:** El mitjà pel qual es transmet la informació.  

### **1.2 Serveis de Seguretat**  
- **Autenticació:** Verifica la identitat dels usuaris.  
- **No Repudi:** Garanteix que cap de les parts pugui negar la seva participació en una transacció.  
   - **No repudi a l’origen:** L’emissor no pot negar haver enviat el missatge.  
   - **No repudi a la destinació:** El receptor no pot negar haver rebut el missatge.  
- **Confidencialitat:** Garanteix que només el destinatari pot entendre el missatge.  
- **Integritat:** Comprova que el missatge no ha estat alterat.  
- **Disponibilitat:** Assegura que els recursos estiguin disponibles quan es necessiten.  
- **Control d’Accés:** Limita l’accés als recursos a usuaris autoritzats.  

---

## **2. Xifratge**  

### **2.1 Concepte de Xifrat**  
El xifratge és un mecanisme de seguretat que modifica un missatge per fer-lo il·legible, excepte per al destinatari correcte.  
- **Xifratge Simètric (SKCS):** Utilitza una única clau per xifrar i desxifrar dades.  
   - **DES:** Claus de 56 bits, considerat insegur avui dia.  
   - **AES:** Claus de 128, 192 o 256 bits, considerat segur.  
   - **Triple-DES:** Aplica DES tres vegades amb 1, 2 o 3 claus independents.  
- **Xifratge Asimètric (PKCS):** Utilitza una parella de claus (pública i privada).  
   - **RSA:** Clauses de 2048, 3072 i 4096 bits.  
   - **Diffie-Hellman (DH):** Intercanvi segur de claus.  
   - **DSA i ECDSA:** Signatura digital basada en corbes el·líptiques.  

### **2.2 Empremta Digital i Funcions Hash**  
- **Empremta Digital:** Funció que converteix un missatge en un codi hash únic.  
- **Funcions Hash Populars:**  
   - **MD5:** Longitud de 128 bits, ja no és segur.  
   - **SHA-1:** Longitud de 160 bits, ja no és segur.  
   - **SHA-2:** Longitud de 224, 256, 384 i 512 bits, considerat segur.  

### **2.3 Signatura Digital**  
Garanteix:  
- **Autenticació:** Identitat de l’emissor.  
- **Integritat:** Que el missatge no ha estat alterat.  
- **No Repudi:** L’emissor no pot negar haver enviat el missatge.  

### **2.4 Certificat Digital**  
- Document emès per una **Autoritat de Certificació (CA)**.  
- Vincula una identitat amb una clau pública.  
- Es basa en l’estàndard **X.509**.  

---

## **3. Seguretat en Xarxes TCP/IP**  

### **3.1 Introducció**  
La seguretat en xarxes TCP/IP afecta tots els nivells: físic, enllaç, xarxa, transport i aplicació.  

### **3.2 Nivells de Seguretat**  
- **Nivell Físic:** Xarxes cablejades (fibra òptica) són més segures que les sense fils.  
- **Nivell d’Enllaç:** VLANs i xifratge per garantir la separació i seguretat del tràfic.  
- **Nivell de Xarxa:** IPSec protegeix el tràfic IP.  
- **Nivell de Transport:** Protecció de dades amb protocols com SSH, SFTP i HTTPS.  
- **Nivell d’Aplicació:** Protecció específica per aplicacions (SSL/TLS, PGP, S-MIME).  

### **3.3 Exemple d’Aplicació**  
- **Comerç Electrònic:** HTTPS protegeix les transaccions.  
- **Accés a Xarxa Corporativa:** VPNs garanteixen la seguretat en connexions remotes.  

---

## **4. Xarxes Privades Virtuals (VPN)**  

### **4.1 Concepte de VPN**  
Permeten crear connexions segures a través d’Internet per a xarxes corporatives.  

### **4.2 Tipus de VPN**  
- **VPN de Nivell 2:** Basades en PPTP i L2TP.  
- **VPN de Nivell 3:** Basades en IPSec.  

### **4.3 Protocols de Seguretat**  
- **AH (Authentication Header):** Autenticació i integritat.  
- **ESP (Encapsulation Security Payload):** Autenticació i confidencialitat.  

### **4.4 Components de VPN**  
- **Client VPN:** Inicia la connexió.  
- **Servidor VPN:** Punt final de la connexió.  
- **NAS (Network Access Server):** Punt d’accés a la xarxa de trànsit.  

---

## **5. Tallafocs (Firewalls)**  

### **5.1 Funcions Bàsiques**  
- Control d’accés entre xarxes públiques i privades.  
- Creació d’un **perímetre de seguretat**.  

### **5.2 Tipus de Tallafocs**  
- **Router de filtrat de paquets:** Analitza capçaleres IP, TCP i UDP.  
- **Gateway d’Aplicació (Proxy):** Actua com a intermediari entre el client i el servidor.  
- **Gateway de Nivell de Circuit:** Controla connexions TCP a nivell de circuit.  
- **Bastion Host:** Sistema central amb polítiques estrictes de seguretat.  
- **Filtres amb Estat:** Inspecciona l’estat de les connexions.  

### **5.3 Arquitectures de Tallafocs**  
- **Screened Host Firewall:** Router + Bastion Host.  
- **Screened Subnet Firewall:** DMZ afegeix una capa addicional de seguretat.  

---

## **6. Conclusions**  
- La seguretat en xarxes implica l’ús combinat de serveis, protocols i eines.  
- VPNs ofereixen seguretat en connexions remotes.  
- Els tallafocs són essencials per protegir xarxes contra atacs externs.  
- Els certificats i signatures digitals garanteixen la confiança i autenticitat de les comunicacions.  

---

Aquest resum proporciona una visió més detallada dels conceptes clau per preparar-te adequadament per l'examen final. Si necessites més informació sobre algun apartat específic, fes-m’ho saber! 😊
