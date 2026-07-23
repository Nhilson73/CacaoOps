# Plan de adaptación: CafeOps → CacaoOps

**Entidad gestora:** Cafelium Foundation  
**Autoría original:** *CafeOps — Coffee Operating System*, publicado por Cafelium Foundation bajo CC BY-SA 4.0.  
**Objetivo:** Adaptar la arquitectura conceptual y operacional del libro CafeOps al cacao, generando el manuscrito CacaoOps (*Cacao Operating System*) como marco abierto para el sector cacaotero mundial.

---

## 1. Diagnóstico de partida

- `CafeOps` contiene un manuscrito de ~130.000 palabras y 18 capítulos distribuidos en 6 partes, más un sitio estático (`index.html`, `assets/`).
- `CacaoOps` es un repositorio vacío, por lo que se puede construir desde cero conservando la misma estructura técnica y editorial.
- Aproximadamente 1.500+ instancias de términos específicos del café deben revisarse de forma controlada, no con reemplazo masivo.

## 2. Lo que se conserva casi intacto

La columna vertebral conceptual de CafeOps es agnóstica del cultivo y se reutiliza directamente en CacaoOps:

- **Digital Terroir** (filosofía, principios, capítulo 0).
- **TraceOps** (trazabilidad verificable, identificadores de lote, soberanía de datos, capítulos 8, 9, 10).
- **Capas de integración** (Parte V: dimensión económica, humana, cooperación regional).
- **Visión 2035** (Parte VI).
- **Esquema de tres niveles** de implementación: Esencial, Intermedio, Avanzado.
- **Tipología de evidencia**: captura, memoria operacional, evidencia defendible.

## 3. Lo que se debe reescribir o adaptar

### 3.1 Terminología general

| Café | Cacao |
|------|-------|
| Café / café de especialidad | Cacao / cacao fino de aroma / cacao de especialidad |
| Sector cafetero | Sector cacaotero |
| Caficultor / productor de café | Cacaocultor / cacaotero / productor de cacao |
| Cereza | Mazorca (o vaina) |
| Mucílago | Pulpa (o mucílago/miel de cacao) |
| Grano (de café) | Grano (de cacao) / semilla de cacao |
| Pergamino | Testa / cáscara del grano (en fermentación) |
| Taza / catación protocolizada | Licor de cacao / cata de cacao / evaluación sensorial del licor |
| Tostado / tueste | Tueste del cacao (evitar "torrefacción"; usar "tueste" como sustantivo del proceso) |
| Tostador / chocolatero | Tostador de cacao / chocolatero |
| SCA (Specialty Coffee Association) | ICCO / WCF / paneles de cata de cacao |
| Beneficio | Centro de fermentación / post-cosecha del cacao |
| Tanque de fermentación | Cajón fermentador / saco de yute / caja / tina / montón |
| Agua de proceso / mosto | Miel de cacao / jugo de pulpa / mosto fermentante |

### Nota de estilo para capítulos nuevos

- **Tueste, no torrefacción.** En CacaoOps se prefiere el término "tueste" como sustantivo del proceso de tostar el cacao. "Torrefacción" se evita en los nuevos capítulos. El verbo es "tostar"; el resultado puede llamarse "grano tostado" o "licor de cacao tostado".
- **Cacao fino de aroma.** Se usa como equivalente de "café de especialidad" cuando se habla del segmento premium del cacao.
- **Mazorca y pulpa.** Se reemplazan "cereza" y "mucílago" por "mazorca" y "pulpa" respectivamente. El jugo fermentable de la pulpa puede llamarse "miel de cacao" o "mosto de pulpa".
- **Volteos, no recirculación.** En cacao la manipulación típica es el volteo para reoxigenar y homogeneizar la masa, no la recirculación de mosto que es más propia de tanques de café. El drenaje de la miel de cacao puede hacerse, pero no se presenta como recirculación continua salvo en sistemas específicos.

### 3.2 Ajustes por capítulo

#### Parte I: Comprender el sistema cacaotero

- **Cap 1: La taza y la finca** → *La barra y la finca*: reemplazar cadena de taza por cadena del grano al chocolate/licor; actores: cacaocultor, acopio, exportador, importador, chocolatero/tostador, consumidor.
- **Cap 2: Del café commodity a la complejidad de la especialidad** → historia del cacao commodity vs cacao fino de aroma; variedades (Criollo, Forastero, Trinitario, CCN-51, Nacional); mercado de origen.
- **Cap 3: Problema de coherencia** → los cuatro huecos se mantienen, pero con ejemplos del cacao: fermentación sin gobernanza, trazabilidad sin validación, tostado sin información ascendente, precio sin defensibilidad.

#### Parte II: FermentOps

- **Cap 5: La fermentación como sistema biológico** → reescribir con bioquímica del cacao: sustrato (pulpa), familias microbianas propias, fases cinéticas de 5-7 días, volteos, métodos de fermentación cacaoteros (cajones, sacos, tinas, inoculación), defectos del cacao.
- **Cap 6: Implementando FermentOps** → instrumentos adaptados (sonda de temperatura de masa, pH de pulpa, Brix de pulpa, volteos, registros de volteos).
- **Cap 7: De los datos a la evidencia defendible** → adaptar identificadores de lote, sellos de cierre, dossier técnico del lote de cacao.

#### Parte IV: RoastOps

- **Cap 11: El tueste como sistema técnico documentable** → *El tostado del cacao como sistema técnico documentable*: fases (secado, desarrollo, Maillard, punto de descarga), perfiles de torrefacción, curvas de temperatura.
- **Cap 12: Implementando RoastOps** → instrumentación para tostado de cacao, perfiles objetivo, biblioteca de curvas.

#### Parte V/VI

- Mantener estructura, cambiar ejemplos a cacao y referencias a ICCO/WCF.

## 4. Elementos nuevos a considerar

- **Secado como etapa crítica:** en el cacao, el secado al sol o en secadores es una fase determinante del sabor y la seguridad microbiológica. Evaluar crear un apartado específico (DryOps/CuringOps) o integrarlo en FermentOps.
- **Variedades y genética:** el cacao es más diverso en tipos genéticos y tiene un vocabulario propio (clones, híbridos, criollo, trinitario).
- **Fermentación con box/sacos/tinas:** los tres contenedores principales requieren descripción propia.
- **Cata de cacao (cutting test / liquor evaluation):** la evaluación sensorial del cacao no es *cupping* de café; es corte de grano y cata de licor.
- **Trazabilidad del grano vs del chocolate:** distinguir entre lote de grano seco y lote de chocolate.

## 5. Decisiones de marca y atribución

- **CacaoOps** es el acrónimo de *Cacao Operating System*, al igual que CafeOps.
- Se mantienen: **FermentOps**, **TraceOps**, **RoastOps**, **Digital Terroir** como marcas/familia conceptual de Cafelium Foundation.
- Referencias institucionales: incluir ICCO (Organización Internacional del Cacao) y WCF (Fundación Mundial del Cacao) como entidades de referencia global en capítulos de contexto sectorial, sostenibilidad y visión 2035.
- Atribución a Cafelium Foundation como acuñadora; licencia CC BY-SA 4.0 para contenido editorial; política de marca abierta en tres niveles, análoga a CafeOps.

## 6. Riesgos y recomendaciones

- **No usar reemplazo masivo de términos.** Palabras como *mucílago*, *pergamino* o *cereza* tienen análogos cacao pero con bioquímica distinta.
- **Priorizar capítulo piloto.** El Capítulo 5 (FermentOps) es el más denso y el mejor termómetro del esfuerzo de adaptación. Si este capítulo funciona, el resto es principalmente reescritura mecánica y validación técnica.
- **Validar con fuentes cacaoteras.** Se recomienda contrastar con publicaciones de ICCO, WCF, investigadores como R. F. Schwan (también activo en cacao) y literatura de fermentación de cacao (ICCO, Chocolate Manufacturers Association, centros de investigación latinoamericanos y africanos).
- **Conservar el tono institucional y la estructura de niveles.** El valor del libro no es la ciencia primaria, sino la traducción a un marco operacional adoptable por operaciones de distinta escala.

## Estado actual del borrador

- **v0.2 · julio 2026** — Se entregan el **Capítulo 5 · La fermentación como sistema biológico** y el **Capítulo 6 · De la captura a la cultura: implementando FermentOps en operaciones reales**, junto con `PLAN_CACAO.md` y el sitio estático adaptado.
- Ambos capítulos han sido verificados localmente y renderizan correctamente en el sitio estático.
- Se añadió al plan la nota de estilo: **tueste, no torrefacción**.
- Los siguientes capítulos deberán adaptarse siguiendo el glosario y los ajustes descritos en este plan.

## 7. Próximos pasos sugeridos

1. Validar este plan y el Capítulo 5 piloto.
2. Adaptar la Parte I (contexto sectorial cacaotero).
3. Desarrollar Parte II completa: Capítulos 6 (implementación operacional) y 7 (evidencia defendible).
4. Adaptar Parte IV (tostado del cacao / RoastOps).
5. Revisar Parte III (TraceOps), Parte V (capas de integración) y Parte VI (Visión 2035), mayoritariamente reemplazos de terminología y ejemplos.
