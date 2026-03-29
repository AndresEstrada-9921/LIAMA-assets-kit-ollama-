# LIAMA-assets-kit-ollama-
Binarios optimizados y kits de aceleración (GPU/NPU) para despliegues de Ollama en el ecosistema LIAMA. Máximo rendimiento para modelos locales.
LIAMA-assets: Kit de Aceleración para Ollama

Este repositorio contiene el Kit de Aceleración y Binarios Optimizados para el ecosistema LIAMA. El objetivo de este conjunto de archivos es permitir que Ollama aproveche al máximo el hardware del usuario, ya sea mediante GPU dedicada (NVIDIA/AMD) o mediante instrucciones específicas de CPUs modernas y antiguas, optimizando así el rendimiento de inferencia de modelos.

Contenido del Kit de Binarios

El kit está organizado para ofrecer la mayor compatibilidad de hardware posible.

Aceleración por GPU (Gráficas)
cuda_v12 y cuda_v13: Soporte nativo para tarjetas NVIDIA modernas (series 30 y 40).
mlx_cuda_v13: Optimizaciones de memoria para entornos de alta carga.
rocm: Soporte para tarjetas AMD Radeon.
vulkan: Aceleración universal para gráficas integradas y hardware diverso.
ggml-cuda.dll: Librería principal de enlace para núcleos CUDA.
Optimización por CPU (Procesadores)

Incluye librerías ggml compiladas para arquitecturas específicas de Intel y AMD, permitiendo una inferencia más rápida en sistemas sin GPU dedicada:

alderlake: Intel Core de 12.ª generación en adelante.
icelake y skylakex: Procesadores de alto rendimiento y estaciones de trabajo.
haswell y sandybridge: Compatibilidad con CPUs de generaciones anteriores de alto rendimiento.
sse42 y x64: Compatibilidad universal para procesadores antiguos o configuraciones estándar.
Ejecutable Central
ollama.exe: Binario principal configurado para reconocer y cargar estas librerías dinámicas según el entorno de hardware.
Instrucciones de Uso
Identifique su hardware: Verifique si dispone de una GPU dedicada o determine la generación de su procesador Intel o AMD.
Descarga: Diríjase a la sección de Releases del repositorio y descargue el paquete correspondiente a su hardware.
Instalación:
Coloque los archivos .dll en la ruta de instalación de su instancia de Ollama.
Asegúrese de que el ejecutable ollama.exe tenga los permisos necesarios para acceder a los controladores de la GPU si aplica.
Verificación: Ejecute un modelo y supervise el uso de CPU/GPU desde el administrador de tareas para confirmar que la aceleración está activa.
Notas Importantes
Privacidad: Todo el procesamiento se realiza de forma local en la máquina del usuario.
Compatibilidad: Si no está seguro de su arquitectura, utilice las versiones x64 o vulkan para mayor estabilidad.
Descargo de responsabilidad: Este es un proyecto independiente. Utilícelo bajo su propio riesgo y asegúrese de mantener los controladores de video actualizados.

Desarrollado para el ecosistema LIAMA, basado en tecnologías de código abierto.
