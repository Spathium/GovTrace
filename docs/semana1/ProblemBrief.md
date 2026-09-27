# Problem Brief

## Decisión del problema

### Problema elegido

La opacidad y manipulación administrativa de registros en obras públicas permite que megaproyectos abandonados figuren como "al día" en los sistemas del Estado mediante actas retroactivas, encubriendo el despilfarro y bloqueando la auditoría ciudadana. (Propuesto por: Cristhian Barros).

### Por qué elegimos este

Este reto ataca directamente una crisis de confianza estructural: el Estado monopoliza tanto la ejecución como el registro digital de sus propios proyectos. Elegimos este problema porque requiere un registro histórico con marca de tiempo inalterable para romper la asimetría de poder, evitando que los actores institucionales puedan maquillar la verdad administrativa antes de una intervención fiscal.

### Propuestas descartadas

1. **Billetera virtual de microcréditos:** (Propuesta por Brian Henao). Descartada por su altísima fricción regulatoria (Superintendencia Financiera) y requisitos normativos (KYC/AML) que inviabilizan un MVP ágil de 5 semanas.
2. **Inmutabilidad en votos electorales:** (Propuesta por Meliza Posada). Descartada por el conflicto constitucional insalvable entre el derecho al voto secreto y la transparencia inherente de un libro mayor distribuido público.
3. **Trazabilidad de artículos de segunda mano:** (Propuesta por Camilo Hernández). Descartada por el "problema del oráculo": la dificultad técnica de vincular un objeto físico común a un gemelo digital inmutable sin depender de hardware costoso, lo que diluye el valor real de usar blockchain.

### Cómo tomamos la decisión

Llegamos a un consenso tras evaluar el impacto sociopolítico y la viabilidad técnica. GovTrace ganó porque utiliza Datos Abiertos existentes (API SECOP) y resuelve un dolor tangible (la corrupción en infraestructura) con una arquitectura B2B2C altamente escalable y demostrable a corto plazo.

---

## Problem Brief

### Encabezado

**GovTrace**: El notario descentralizado que transforma las denuncias ciudadanas sobre elefantes blancos en pruebas matemáticas irrefutables.

### Equipo y roles

* **Cristhian Barros** : Ingeniero de Software.
* **Brian Henao** : Por definir.
* **Meliza Posada** : Por definir.
* **Camilo Hernández** : Analista de datos e integración SECOP II.
* **Canal de coordinación:** Google Meets.

### Problema y evidencia

En Colombia, la corrupción en infraestructura prospera en la sombra de las bases de datos centralizadas. La evidencia de este problema es cotidiana: al cruzar la API oficial del SECOP II, encontramos sistemáticamente fechas de entrega y actas de avance que contradicen la realidad de obras físicas abandonadas (los llamados "elefantes blancos"). El fallo crítico del sistema actual no radica en brechas de ciberseguridad tradicionales ni en hackeos informáticos, sino en la **discrecionalidad administrativa**: el Estado y los contratistas pueden generar actas de suspensión o informes de avance con fechas retroactivas (*backdating*) y subirlas tardíamente a los servidores centralizados para encubrir retrasos justo antes de las auditorías de la Contraloría. Cuando las veedurías intentan actuar, sus denuncias fracasan porque los expedientes oficiales han sido "maquillados" digitalmente, dejando el desfalco en la impunidad.

### Usuario y actores

El usuario principal es el veedor ciudadano, el periodista de investigación y la ONG anticorrupción. Hoy, estos actores intentan combatir el abandono de infraestructura exponiendo fotos en redes sociales o radicando lentos derechos de petición. Esto se traduce en años de desgaste burocrático y frustración, ya que sus pruebas (archivos JPG/PDF comunes) son rutinariamente desestimadas por los abogados de los contratistas bajo el argumento de que carecen de validez técnica o pudieron ser editadas.
El ecosistema incluye al *Estado* (que contrata y controla la base de datos oficial), el *Contratista* (que ejecuta la obra), el *Interventor* (el intermediario privado que aprueba los pagos), y la *Contraloría* (que audita, pero depende ciegamente de la información que le entrega la misma entidad que está investigando).

### Flujo actual de valor

1. El Estado adjudica una obra pública y la registra en la plataforma SECOP II, cumpliendo la normatividad vigente.
2. El Contratista inicia (o simula iniciar) los trabajos en terreno.
3. El Interventor técnico certifica el progreso mediante "actas de avance" cargadas al sistema.
4. La entidad desembolsa los recursos públicos basándose exclusivamente en lo que dictan estas actas institucionales.
5. El Veedor detecta que la obra está paralizada, toma fotografías como evidencia y radica una denuncia ante la Contraloría.
6. La Contraloría notifica a la entidad para auditar el contrato. En esta ventana de tiempo, actores con privilegios de escritura en el sistema centralizado suben actas con fechas retroactivas o alteran el expediente digital para encubrir el retraso, entregando un reporte "limpio" que neutraliza la investigación.

### Fricciones identificadas

* **Fricción 1: El Monopolio de la Verdad (Paso 6).** El Estado y sus contratistas controlan tanto la ejecución física como el registro digital. La centralización permite el "maquillaje retroactivo": la subida de documentos con fechas falsas y la aprobación digital de avances ficticios sin que exista una marca de tiempo criptográfica inalterable. Esto ciega a los entes de control, que terminan auditando expedientes digitales limpios que no reflejan la realidad del terreno.
* **Fricción 2: La Fragilidad Probatoria (Paso 5).** La evidencia recolectada por el ciudadano carece de un sello de tiempo confiable e independiente. Esto afecta directamente al veedor, cuyo esfuerzo queda invalidado en los estrados judiciales por tecnicismos legales, perpetuando la impunidad y la apatía cívica.

### Oportunidad e hipótesis

Nuestra oportunidad de mayor impacto radica en destruir la "Fragilidad Probatoria" (Fricción 2) para neutralizar el "Monopolio de la Verdad" (Fricción 1). 
**Hipótesis:** Si GovTrace actúa como un notario automático que cruza los datos oficiales del SECOP con la evidencia fotográfica comunitaria, y sella ambas partes criptográficamente en una red pública en tiempo real, le entregaremos al ciudadano un certificado matemático de inmutabilidad temporal. Esto cambia las reglas del juego: transforma una simple foto en una prueba con línea de tiempo blindada. Si el Estado o el contratista intentan alterar o antedatar documentos en el futuro, el sistema demostrará matemáticamente la discrepancia temporal, haciendo imposible encubrir el fraude mediante actas retroactivas.

### Criterio de pertinencia

Este desafío exige categóricamente un registro distribuido (Blockchain) y descarta el uso de bases de datos tradicionales. En la contratación pública conviven partes con intereses opuestos y una desconfianza absoluta (Ciudadanía vs. Contratistas y funcionarios). Si GovTrace utilizara un servidor centralizado (ej. PostgreSQL), nos convertiríamos simplemente en otro intermediario vulnerable; los ciudadanos tendrían que confiar ciegamente en que nosotros no fuimos coaccionados para alterar la base de datos. Blockchain elimina la necesidad de confiar en personas. Al registrar el hash de los documentos y su marca de tiempo en una red pública global, garantizamos una inmutabilidad histórica que ni siquiera los creadores de GovTrace pueden corromper, arrebatándole el monopolio de la línea de tiempo temporal al Estado.

### Supuestos y riesgos

* **Supuesto 1:** El marco jurídico colombiano (Ley 527 de 1999 sobre mensajes de datos) y la jurisprudencia de las altas cortes avalarán el uso de hashes criptográficos y sellos de tiempo descentralizados como material probatorio pleno (equivalencia funcional).
* **Supuesto 2:** Entidades de cooperación internacional (BID, USAID), ONGs y Cámaras de Comercio tienen la disposición estratégica y financiera para adoptar soluciones GovTech SaaS que modernicen la vigilancia ciudadana.
* **Riesgos:** La principal amenaza es el rechazo institucional: que la Contraloría se niegue por dogmatismo burocrático a aceptar plataformas de auditoría externas, o que el Estado restrinja repentinamente el acceso a las APIs de Datos Abiertos para evitar el escrutinio automatizado.