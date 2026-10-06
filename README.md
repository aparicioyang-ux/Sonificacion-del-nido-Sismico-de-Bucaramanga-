# Sonificación del Nido Sísmico de Bucaramanga

Este proyecto explora la intersección entre la sismología y la composición musical mediante el análisis espectral de eventos sísmicos registrados en el Nido Sísmico de Bucaramanga, Colombia. 

## Descripción del Proyecto
El código procesa sismogramas (convertidos previamente a formato de audio WAV) y aplica la Transformada Rápida de Fourier (FFT) para aislar la energía y las frecuencias dominantes de la onda elástica. Estas frecuencias, que componen la huella acústica del sismo, son traducidas matemáticamente a notas musicales en la escala MIDI estándar, permitiendo su posterior secuenciación y análisis en Estaciones de Trabajo de Audio Digital (DAWs).

## Metodología
1. **Preprocesamiento:** Lectura y normalización de la amplitud de la señal del sismograma.
2. **Análisis Espectral:** Implementación de `np.fft.rfft` para aislar el espectro de frecuencias reales, utilizando una suma acumulada de energía para enmarcar el rango acústico útil.
3. **Extracción de Picos:** Identificación de las frecuencias armónicas principales e independientes mediante `scipy.signal.find_peaks`, filtrando el componente DC.
4. **Traducción Musical:** Conversión logarítmica de las frecuencias dominantes (Hz) a notas musicales exactas (referencia A4 = 440 Hz).

## Tecnologías y Librerías
* Python 3
* NumPy
* SciPy
* Matplotlib

## Datos de Audio y Sismogramas
Debido a los límites de tamaño de GitHub, los archivos `.wav` de alta resolución utilizados en este análisis están alojados en una carpeta externa. Puedes descargar los audios para reproducir el código o escucharlos directamente aquí:
[Haz clic aquí para acceder a los audios]https://drive.google.com/drive/folders/150PK9NawuWqnN93f2TkcByDwMtVyb9Kc?usp=sharing 
