

![Captura de pantalla actualizada](https://github.com/abbaselmas/tradingview-indicator-combination/assets/28142617/fc8b3058-6743-4eb6-be19-50fd95a90e13)

![Captura de pantalla de ejemplo](https://github.com/abbaselmas/tradingview-indicator-combination/assets/28142617/e5908ea5-1aa1-417f-b44c-4a85ac541030)

# Suite de Indicadores de TradingView

Una colección profesional de indicadores optimizados en Pine Script v6 para un análisis integral del mercado. Esta suite combina múltiples herramientas de trading potentes, diseñadas para traders serios que necesitan niveles precisos, estructura de mercado y análisis de volumen.

---

## 📊 Abbas1 - Sistema de Trading Multindicador

**Range | Blocks | NYOpens | Weekendicator | CME | BPR**

### Descripción general
Un indicador integral todo en uno que combina 6 potentes herramientas de trading para un análisis de mercado mejorado. Perfecto para traders que desean niveles clave, estructura de mercado y rangos de precio en un único indicador limpio.

### Características

#### 1. 📈 Bandas de Bollinger
- Configuración personalizable de BB (longitud: 21, multiplicador: 2.8)
- Cálculos ajustables de fuente y desviación
- Línea base visual con bandas superior e inferior
- Identifica la volatilidad y zonas de reversión potencial

#### 2. 📅 Weekendicator
- Herramienta de proyección de precios para fines de semana con detección automática
- Extiende los niveles de precio durante el sábado/domingo
- Multiplicador ajustable (0-10%) para el rango de proyección
- Anticipa los huecos de apertura del lunes utilizando ratios de máximos/mínimos

#### 3. 📦 Range Blocks (Estructura de Mercado)
Visualización avanzada del flujo de órdenes que incluye:
- **Order Blocks**: Zonas de oferta/demanda sin probar y probadas con codificación de colores
- **Breaker Blocks**: Order blocks fallidos que indican reversiones
- **MSB Lines**: Líneas de ruptura de estructura de mercado para cambios de tendencia
- **Range Detection**: Identifica rangos de consolidación con niveles 0.25, 0.5, 0.75
- Seguimiento en tiempo real de máximos/mínimos pivot
- Limpieza automática de bloques invalidados

#### 4. 🗽 New York Opens
Dos marcadores críticos de la sesión de Nueva York:
- **Midnight Open (00:00 EST)**: Precio de apertura de futuros del CME
- **8:30 AM Open**: Precio de apertura pre-mercado de la NYSE
- Estilos de línea personalizables (Sólida, Punteada, Discontinua)
- Etiquetas opcionales y líneas históricas
- Configuración de colores individual y configuración de sesión

#### 5. 🎯 Balanced Price Range (BPR)
- Análisis de Fair Value Gap (FVG) para rangos de precio equilibrados
- Detecta zonas de BPR alcistas y bajistas
- Filtro BPR "Clean" (el precio no interfiere antes de la finalización)
- Umbral ajustable para el tamaño mínimo del rango
- Período de retrovisión configurable (predeterminado: 50 velas)
- Seguimiento de extensión en tiempo real

#### 6. 📈 CME Gap Show & Fill
Detección de huecos de futuros de Bitcoin del CME con 3 modos:
1. Cierre del símbolo actual con horarios de negociación del CME
2. Precio de cierre original directo del CME
3. Precio de liquidación del CME
- Rastrea el cierre del viernes y monitorea el estado de llenado del hueco
- Relleno visual de fondo (verde = llenado al alza, rojo = llenado a la baja)
- Detección automática de huecos de fin de semana
- Manejo correcto de la zona horaria (GMT-5)

### Configuración y personalización

**Grupos de entrada:**
- **BB**: Longitud, Fuente, Multiplicador
- **Weekend**: Porcentaje del multiplicador
- **Range Blocks**: Interruptores para líneas MSB, Order Blocks, Breaker Blocks, líneas de rango, personalización de colores
- **New York Opens**: Configuración separada para aperturas de Medianoche y 8:30 AM, interruptores de visualización, estilos de línea
- **Balanced Price Range**: Umbral, período de retrovisión, filtro BPR "clean", opción para eliminar BPR antiguos
- **CME Gap**: Selección de modo, seguimiento automático de huecos

### Rendimiento
- **Pine Script v6** con sintaxis moderna optimizada
- Cálculos en caché para reducir operaciones redundantes
- Operaciones de matrices optimizadas con caché de tamaño
- Salidas anticipadas de bucles para mejorar la eficiencia
- Código limpio y organizado con encabezados de sección

### Consejos de uso
- **Day Traders**: Concéntrate en NY Opens y BPR para configuraciones intradía
- **Swing Traders**: Usa Range Blocks y Bandas de Bollinger para estructura
- **Weekend Planning**: Monitorea Weekendicator y huecos del CME
- **Order Flow**: Combina Order Blocks con zonas de BPR para entradas de alta probabilidad
- Se usa mejor en marcos temporales de 15m-1H para señales más limpias

### Especificaciones técnicas
- **Versión**: Pine Script v6
- **Superposición**: Verdadero
- **Precisión**: 4 decimales
- **Max Bars Back**: 1000
- **Max Líneas**: 500

---

## 📊 Abbas3 - Sistema de Perfil de Volumen y Niveles Clave

**PVP | nPOCs | Key Levels | Fair Value Gaps | Smart Money Concepts**

### Descripción general
Un indicador avanzado que combina el Perfil de Volumen Periódico (PVP), niveles clave en múltiples marcos temporales, Fair Value Gaps (FVG) y Smart Money Concepts (SMC) para un análisis de mercado de nivel institucional. Perfecto para traders que necesitan niveles precisos basados en volumen y estructura de mercado.

### Características

#### 1. 📊 Periodic Volume Profile (PVP)
- **Períodos en múltiples marcos temporales**: Intradía, Diario, Semanal, Mensual, Trimestral (3M), Semestral (6M), Anual
- **Análisis dinámico de volumen** con niveles de perfil personalizables (predeterminado: 24)
- **Point of Control (POC)**: Nivel de precio con mayor volumen
- **Value Area High (VAH)** y **Value Area Low (VAL)**: 70% de concentración de volumen
- **Opciones de colocación del perfil**: Izquierda, Derecha o Centro del período
- **Personalización visual**: Ancho del perfil, colores para volumen total y área de valor
- Opción de **Background fill** (relleno de fondo) para mejorar la visibilidad
- **Actualizaciones del perfil en tiempo real** a medida que se forman nuevas velas

#### 2. 🎯 Key Levels - Multi-Timeframe
Seguimiento integral de niveles en todos los marcos temporales principales:

**Niveles de 4 horas:**
- Máximo, Mínimo, Apertura y Punto Medio de 4H anteriores

**Rango de Lunes:**
- Máximo, Mínimo y Punto Medio de Lunes (enfoque de sesión especial)

**Niveles Diarios:**
- Máximo del Día Anterior (PDH), Mínimo del Día Anterior (PDL)
- Apertura Diaria (DO), Punto Medio del Día Anterior (PDM)

**Niveles Semanales:**
- Máximo de la Semana Anterior (PWH), Mínimo de la Semana Anterior (PWL)
- Apertura Semanal (WO), Punto Medio de la Semana Anterior (PWM)

**Niveles Mensuales:**
- Máximo del Mes Anterior (PMH), Mínimo del Mes Anterior (PML)
- Apertura Mensual (MO), Punto Medio del Mes Anterior (PMM)

**Niveles Anuales:**
- Máximo del Año Actual (CYH), Mínimo del Año Actual (CYL)
- Apertura Anual (YO), Punto Medio del Año Actual (CYM)

**Características de los Niveles Clave:**
- Interruptores individuales para cada marco temporal
- Estilos de línea personalizables (Sólida, Discontinua, Punteada)
- Ancho de línea ajustable (Pequeño, Medio, Grande)
- Etiquetas de texto con dos opciones de formato (Compacto: "PDH" o Completo: "Prev Day High")
- Opción de anulación global de color para una apariencia unificada
- Colocación anclada a la derecha o basada en tiempo
- Fusión automática de niveles cuando los precios se superponen
- Configuración de distancia de visualización (velas para extender a la derecha)

#### 3. 📉 Fair Value Gaps (FVG)
- **Detección de FVG alcistas y bajistas** utilizando patrones de 3 velas
- **Umbral automático (Auto Threshold)**: Filtra huecos insignificantes automáticamente
- **Soporte para marco temporal personalizado**: Analiza FVG en cualquier marco temporal
- **Visualización en caja**: FVG dibujados como cajas con transparencia
- **Seguimiento de auto-mitigación**: Las cajas se eliminan cuando el hueco se llena
- **Extend FVG**: Configura cuántas velas extender las cajas (predeterminado: 50)
- Codificación por colores: Verde para FVG alcistas, Rojo para bajistas

#### 4. 🧠 Smart Money Concepts (SMC)
Conceptos avanzados de trading institucional:

**Estructura de Mercado:**
- **Estructura Interna**: Roturas de estructura más rápidas y sensibles
- **Swing Structure**: Roturas de estructura de tendencia principal
- **BOS (Break of Structure)**: Señales de continuación de tendencia
- **CHoCH (Change of Character)**: Señales de reversión de tendencia
- Controles separados para estructura alcista y bajista
- Filtro de confluencia para estructura interna (reduce señales falsas)

**Detección de Puntos Swing:**
- Longitud swing configurable (predeterminado: 50)
- Etiquetas de pivote Máximo/Mínimo en el gráfico
- Identificación de Máximos y Mínimos Fuertes/Débiles
- Seguimiento swing en tiempo real

**Coloreado de Tendencia:**
- Colorea las velas según la tendencia actual
- Dos opciones de estilo: Coloreado o Monocromático
- Ayuda a identificar la tendencia de un vistazo

#### 5. ⚙️ Personalización Avanzada

**Configuración del Perfil de Volumen:**
- Niveles de perfil, tipo de período, opciones de colocación
- Color y ancho de POC, colores de VAH/VAL
- Porcentaje del área de valor, opciones de fondo
- Interruptor del perfil de volumen diario

**Configuración de Niveles Clave:**
- Habilitación/deshabilitación de marcos temporales individuales
- Coloreado global vs individual
- Opciones de formato y tamaño de etiquetas de texto
- Estilo de línea, ancho y distancia de extensión
- Estilo de visualización (Anclado a la derecha o basado en tiempo)
- Opción de fusión de niveles

**Configuración de Fair Value Gaps:**
- Interruptor de visualización de FVG
- Umbral automático o filtrado manual
- Selección de marco temporal personalizado
- Personalización de colores alcista/bajista
- Configuración de velas de extensión

**Configuración de Smart Money Concepts:**
- Modo: Histórico o Presente (opción de gráfico limpio)
- Estilo: Temas coloreados o monocromáticos
- Interruptores de visualización de estructura (Interna/Swing)
- Filtros de estructura alcista/bajista (Todos, solo BOS, solo CHoCH)
- Opciones de tamaño de etiqueta (Muy pequeño, Pequeño, Normal)
- Longitud swing y sensibilidad de detección

### Optimizaciones de rendimiento
- Cumplimiento con **Pine Script v6** y la última sintaxis
- **Declaraciones de tipo** para todas las variables y funciones
- **Cálculos en caché** para minimizar operaciones redundantes
- **Operaciones de matrices optimizadas** con tamaños precalculados
- **Condiciones de salida anticipada** en bucles y funciones
- **Solicitudes de seguridad eficientes** para datos de múltiples marcos temporales
- **Valores basados en tiempo precalculados** para mejorar el rendimiento
- **Encabezados de sección** para una organización limpia del código

### Consejos de uso
- **Traders de Volumen**: Usa PVP para identificar nodos de alto volumen y áreas de valor para soporte/resistencia
- **Traders de Niveles**: Los niveles clave proporcionan puntos de entrada/salida precisos en todos los marcos temporales
- **Seguidores de Smart Money**: Las características SMC revelan el flujo de órdenes institucional y la estructura
- **Traders de Huecos**: Las cajas de FVG muestran huecos no llenados a los que el precio tiende a regresar
- **Análisis Multi-Marco Temporal**: Combina niveles diarios con semanales/mensuales para confluencia
- Se usa mejor en 5m-1H para intradía, 4H-D para swing trading

### Aplicaciones de Trading
1. **Soporte/Resistencia**: Usa POC, VAH, VAL y niveles clave como zonas de S/R
2. **Configuraciones de Entrada**: Busca confluencia de FVG + Nivel Clave para entradas de alta probabilidad
3. **Confirmación de Tendencia**: Las roturas de estructura SMC confirman cambios de tendencia
4. **Nodos de Volumen**: Las líneas de POC muestran dónde se realizó la mayor parte del trading (S/R fuerte)
5. **Llenado de Huecos**: Opera los llenados de FVG con confluencia de niveles clave
6. **Trading de Rango**: Usa los límites del área de valor para estrategias de rango

### Especificaciones técnicas
- **Versión**: Pine Script v6
- **Superposición**: Verdadero
- **Precisión**: 4 decimales
- **Max Bars Back**: 5000
- **Max Líneas**: 500
- **Max Cajas**: 500
- **Max Etiquetas**: 500

---

## 🚀 Instalación

1. Abre un gráfico de TradingView
2. Haz clic en "Indicadores" en la parte superior
3. Haz clic en "Editor Pine" en la parte inferior
4. Copia el código desde `Abbas1.pine` o `Abbas3.pine`
5. Pégalo en el editor
6. Haz clic en "Añadir al gráfico"
7. Configura la configuración según tu preferencia

## 📝 Notas

- Ambos indicadores están completamente optimizados para Pine Script v6
- Todos los cálculos están en caché para un rendimiento máximo
- El código está bien organizado con encabezados de sección claros
- Colores, tamaños y opciones de visualización totalmente personalizables
- Apto para todos los mercados: Criptomonedas, Forex, Acciones, Materias Primas
- Pueden usarse juntos o por separado dependiendo de tu estilo de trading

## ⚠️ Descargo de responsabilidad

Estos indicadores son solo con fines educativos. Practica siempre una gestión adecuada del riesgo y realiza tu propio análisis antes de operar. El rendimiento pasado no garantiza resultados futuros.

## 👨‍💻 Autor

**Abbas Elmas**
- Repository: [tradingview-indicator-combination](https://github.com/abbaselmas/tradingview-indicator-combination)

## 📄 Licencia

Código abierto - Siéntete libre de modificar y usar para trading personal.
