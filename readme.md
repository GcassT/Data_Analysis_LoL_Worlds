# Análisis y Clasificación de Campeones de League of Legends para el Mundial

## Objetivo General

El objetivo de este proyecto es identificar y clasificar los campeones más efectivos de *League of Legends* en función de sus características y rendimiento. Usando datos recientes, entrenaremos un modelo de *Regresión Logística* para predecir si un campeón será "Óptimo" o "No Óptimo" en el meta actual, con el propósito de proyectar qué campeones podrían tener un mejor desempeño en el próximo Mundial.

## Algoritmo Utilizado

Para este análisis, se utiliza el algoritmo de *Regresión Logística*, que es ideal para tareas de clasificación binaria, en este caso, "Óptimo" (1) o "No Óptimo" (0). La Regresión Logística permite interpretar el impacto de cada característica en la probabilidad de que un campeón sea clasificado como óptimo, lo que facilita la comprensión de los factores clave que contribuyen al rendimiento de cada campeón.

## Instalación y Configuración de Kaggle para Descargar el Dataset

Para quienes quieran replicar el proyecto, el dataset utilizado está alojado en *Kaggle*. Sigue estos pasos para configurar Kaggle y descargar el archivo:

### 1. Configurar el Acceso a la API de Kaggle

Para utilizar la API de Kaggle, primero necesitas descargar tus credenciales de acceso:

1. Ve a [https://www.kaggle.com](https://www.kaggle.com) y accede a tu cuenta.
2. Dirígete a la sección *Account* de tu perfil.
3. En la parte inferior, en la sección *API, selecciona **Create New API Token*.
4. Se descargará un archivo llamado kaggle.json que contiene tu clave de API.

Guarda este archivo en el directorio adecuado:

- En *Linux/macOS*, colócalo en la carpeta ~/.kaggle.
- En *Windows*, guárdalo en el mismo directorio donde ejecutarás el notebook o en C:\Users\TuUsuario\.kaggle.

Asegúrate de que el archivo tenga los permisos adecuados (solo lectura) para proteger tu clave de API.

### 2. Instala la biblioteca Kaggle

1. *Ejecuta el comando para instalar*
   ```bash
   pip install kaggle

2. *Descarga el archivo de Kaggle*:
     ```bash
     kaggle datasets download -d anmatngu/league-of-legends-worlds-2024-swiss-stage-stats

# Columnas y su Descripción

- **Champion**: Nombre del campeón.
- **Picks**: Número de veces que fue seleccionado.
- **Bans**: Número de veces que fue bloqueado.
- **Presence**: Porcentaje de presencia en partidas.
- **Wins**: Número de victorias.
- **Losses**: Número de derrotas.
- **Winrate**: Porcentaje de victorias.
- **KDA**: Proporción de asesinatos, muertes y asistencias.
- **Avg BT**: Tiempo promedio en minutos.
- **GT**: Duración promedio de la partida.
- **CSM**: Minions eliminados por minuto.
- **DPM**: Daño por minuto.
- **GPM**: Oro ganado por minuto.
- **CSD@15**: Diferencia de minions a los 15 minutos.
- **GD@15**: Diferencia de oro a los 15 minutos.
- **XPD@15**: Diferencia de experiencia a los 15 minutos.

### Explicación de Cada Sección

1. *Objetivo General*: Resume el propósito del análisis y lo que esperamos lograr con el modelo.
2. *Algoritmo Utilizado*: Breve descripción de la regresión logística y por qué es adecuada para esta tarea.
3. *Instalación y Configuración de Kaggle*: Guía paso a paso para instalar Kaggle, configurar las credenciales, y descargar el dataset.
4. *Descripción de las Columnas del Dataset*: Explica cada columna para que el lector comprenda qué representa cada métrica y cómo se utiliza en el análisis.