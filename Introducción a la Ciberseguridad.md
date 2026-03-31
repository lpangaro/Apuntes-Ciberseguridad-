# 🛡️ Fundamentos de Seguridad Informática

## 1. Definiciones Principales

* **💻 Seguridad Informática:** Conjunto de prácticas, técnicas y herramientas diseñadas para proteger los sistemas informáticos y la información almacenada en ellos.
* **🌐 Ciberseguridad:** Conjunto de estrategias, tecnologías y prácticas diseñadas para **defender** los sistemas en los que guardamos información. Incluye tecnología, ejercicios ofensivos y defensa activa.
* **📄 Seguridad de la Información:** Conjunto de medidas preventivas, de detección y corrección destinadas a proteger la **integridad, confidencialidad y disponibilidad** de la información. Funciona como el marco que unifica a las otras dos.

---

## 🛠️ Tipos de Medidas de Seguridad

| Tipo | Momento de Aplicación | Objetivo | Ejemplo |
| :--- | :--- | :--- | :--- |
| **Preventivas** | Antes de un evento. | Evitar una vulnerabilidad | Configurar un *firewall* para evitar un *flurrer*. |
| **Detectivas** | Mientras ocurre el evento. | Permiten bloquear o no el ataque en el momento | Antivirus o IDS (*Intrusion Detection System*). |
| **Correctivas** | Después del evento. | Intentan minimizar el daño de lo 	que sucedió | Uso de *backups* tras un *ransomware* o parchar un problema detectado. |

---

# 📐 La Tríada de la Seguridad (CIA)

## 🤐 Confidencialidad
Asegura que la información sea accedida únicamente por sujetos autorizados (personas o APIs).
* **Pilares:** Identificación, Autenticación y Autorización.
* **Clasificación:** Ligada a si la info es secreta, clasificada o pública.

> [!IMPORTANT]
> **Identificación:** Protege la confidencialidad.
> 
> **Autenticación:** Asegura que el sujeto es quien dice ser.
> 
> **Autorización:** Determina a qué recursos tiene acceso el sujeto identificado.

### 🗂️ Niveles de Clasificación
1.  **Estrictamente Secreto y Confidencial** (Top Secret - Clasificación en Argentina).
2.  **Secreto**.
3.  **Confidencial**.

#### 🚦 Protocolo TLP (Traffic Light Protocol)
* 🔴 **Rojo:** Información para compartir oralmente en círculos íntimos; no debe salir de allí.
* 🟡 **Amarillo:** Solo miembros de la misma organización.
* ⚠️ **Amarillo Restringido:** Miembros de la organización + clientes.
* 🟢 **Verde:** Miembros de la comunidad.
* ⚪ **Blanco/Clear:** Sin restricciones, pero sujeto a normas de *copyright*.

#### ⚠️ Amenazas a la Confidencialidad
* **Accesos no autorizados:** Explotación de vulnerabilidades o errores humanos (*"la cadena es tan fuerte como su eslabón más débil"*).
* **Phishing y Spearphishing:** Correos maliciosos (el *spearphishing* es personalizado y más creíble).
* **Fuga de datos:** Uso de dispositivos no seguros (pendrives).
* **Malware:** Virus, troyanos, *spyware*.
* **Sniffing:** Interceptar datos en tránsito en una red.
* **Insiders:** Amenazas internas (empleados descontentos).
* **Trashing:** Recolección de información de la basura física.

---

## 🛡️ Integridad
La información solo debe ser modificada por sujetos autorizados. Lo enviado por el emisor debe ser idéntico a lo recibido.
* **Hashing:** Identificador unívoco que se calcula al enviar y recibir para verificar que coincidan.

#### ⚠️ Amenazas a la Integridad
* **Modificaciones no autorizadas:** Inyección de código.
* **Man in the Middle (MitM):** El atacante modifica los datos (a diferencia del *sniffing* donde solo los ve).
* **Corrupción y eliminación:** Errores de hardware/software o *wipers* (borrado de datos).
* **Malware específico:** Virus que alteran programas o RATs (control remoto).

#### 🛡️ Protección de la Integridad
* **Menor privilegio:** Acceso solo a lo indispensable.
* **Segregación de funciones:** Dividir tareas para evitar que una persona haga todo.
* **Pentest:** Pruebas de penetración para detectar fallas antes que el atacante.
* **Redundancia:** Varias copias alineadas y sincronizadas.

---

## 🕒 Disponibilidad
La información debe estar accesible siempre que se necesite.

#### ⚠️ Amenazas a la Disponibilidad
* **DoS y DDoS:** Ataques de denegación de servicio (usando múltiples máquinas).
* **Desastres naturales y fallos físicos:** Problemas de hardware/software.
* **Ransomware:** Cifrado de archivos que impide el acceso.
* **Worms (Gusanos):** Se replican por la red consumiendo recursos.

#### 🛡️ Protección de la Disponibilidad
* **Tolerancia a fallos:** Mecanismos para que el sistema siga operando.
* **Seguridad Física:** Suministro eléctrico extra, ventilación, molinetes.
* **Plan de Contingencia:** Procedimientos operativos estándar (SOP) paso a paso.

---

## 🧅 Estrategia de Defensa en Profundidad
Es una estrategia que emplea controles en **capas** (como una cebolla). Si una capa es vulnerada, otras protegen la información.

---

## 📜 Principios de Seguridad

### 🔑 Mínimo Privilegio (PoLP) y Need to Know
* **PoLP (Principle of Least Privilege):** Asignar permisos mínimos para trabajar. Es la base del modelo **Zero Trust**. Aplica a todos los recursos y acciones.
* **Need to Know:** El acceso se limita estrictamente a la información que el trabajo requiere y debe estar justificado. Se enfoca en las **personas** y su rol.

### 🔄 Rotación de Tareas y Segregación de Funciones
* **Rotación:** Evita que un empleado haga siempre lo mismo. Previene fraudes, abusos de poder y asegura que el conocimiento no dependa de una sola persona.
* **Segregación:** Divide responsabilidades.
    1.  Armado de matriz de incompatibilidades.
    2.  Ejecución de reglas.
    3.  Identificación de usuarios con funciones incompatibles.
    4.  Plan de acción correctivo.

### ✍️ No Repudio
Asegura que una persona no pueda negar haber realizado una acción. Fundamental en criptografía y auditoría.

### 🏗️ Seguridad por Defecto y Simplicidad
* **Seguridad por Defecto:** Minimizar riesgos desde el diseño y desarrollo del software.
* **Minimización de Superficie de Ataque:** Exponer solo lo indispensable. Dar de baja servidores en desuso y reducir activos digitales expuestos.
* **Simplicidad:** Reduce errores humanos. Incluye automatización, código limpio e interfaces intuitivas.



# 🤔Cuestionario
---

### **Cuestionario - Introducción a la Ciberseguridad**

#### **Pregunta 1**
**¿Cuáles son algunas amenazas a la integridad?**

* [ ] a. Phishing
* [x] **b. Remplazo de archivos**
* [ ] c. Sniffing
* [x] **d. Inyección de código**

> *Nota: La integridad se refiere a que la información no sea alterada de forma no autorizada. El reemplazo de archivos y la inyección de código modifican los datos o el comportamiento del sistema.*

---

#### **Pregunta 2**
**¿Qué tipos de medidas están destinadas a proteger la triada?**

* [x] **a. Preventivas, Detectivas, Correctivas**
* [ ] b. Preventivas, Directas, Correctivas
* [ ] c. Posibles, Detectivas, Certificables
* [ ] d. Posibles, Directas, Certificables

---

#### **Pregunta 3**
**¿Cuál es la diferencia entre el principio de mínimo privilegio (PoLP) y el concepto Need to Know (NTK)?**

* [ ] a. PoLP aplica a algunos recursos. NTK se enfoca en los procesos.
* [x] **b. PoLP aplica a todos los recursos y acciones de un sistema. NTK se enfoca en las personas y su acceso a la información según su rol.**
* [ ] c. NTK aplica a algunos recursos. PoLP se enfoca en los procesos.
* [ ] d. NTK aplica a todos los recursos y acciones de un sistema. PoLP se enfoca en las personas y su acceso a la información según su rol.

---

#### **Pregunta 4**
**Segregar funciones implica cambiarle a un empleado sus funciones para evitar que una sola persona mantenga control exclusivo sobre una actividad.**

* [ ] Verdadero
* [x] **Falso**

> *Corrección: La descripción dada corresponde a la **Rotación de Puestos**. La Segregación de Funciones (SoD) consiste en desglosar una tarea en varios pasos para que no sea ejecutada por una misma persona desde el inicio hasta el fin.*

---

#### **Pregunta 5**
**¿Qué significa la "C" en la triada?**

* [x] **a. Confidencialidad**
* [ ] b. Credenciales
* [ ] c. Claves
* [ ] d. Certificación

---
