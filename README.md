# ExploradorInicioSueldos

## Instalación

Descargar y ejecutar **`ExploradorSueldos-win-Setup.exe`** desde
[la última release](https://github.com/desadpi2026/ExploradorSueldos/releases/latest).
No requiere tener .NET instalado. La aplicación busca actualizaciones al iniciar y
ofrece instalarlas automáticamente (Velopack). También hay una versión portable
(`ExploradorSueldos-win-Portable.zip`) que no se instala ni se auto-actualiza.

Este repositorio distribuye únicamente los ejecutables.

**ExploradorInicioSueldos** es una herramienta de escritorio desarrollada en **VB.NET** utilizando **Windows Forms** y la biblioteca **Renci.SshNet**. Funciona como un cliente y explorador SFTP especializado para la administración, visualización y migración de componentes legacy de sistemas mainframe o Unix vinculados al sistema de sueldos.

## Características Principales

*   **Explorador SFTP Multiconexión:** Gestor de perfiles y conexiones simultáneas a múltiples servidores SSH/SFTP, permitiendo comparar e interactuar de forma paralela.
*   **Clasificación Dinámica de Componentes:** Mapea y clasifica automáticamente los archivos del servidor de acuerdo a su ubicación y contenido según la taxonomía del sistema (e.g., *Inicios*, *Jobs*, *Programas*, *Sorts*, *Rebuilds*, *Variables*, *Archivos de Datos*, *Listados*, *Tarjetas* y *Escalas*).
*   **Visualizador Avanzado con Soporte Legacy:**
    *   Previsualización directa de archivos de texto estándar (ASCII / UTF-8).
    *   **Decodificador EBCDIC** integrado con selección manual o automática de ancho de registro (Auto, 80, 128, 160).
    *   Soporte experimental para visualización de campos numéricos empaquetados **COMP-3**.
    *   Control y avisos de rendimiento para la descarga de archivos de gran tamaño.
*   **Edición Externa Fluida:** Integración de estilo "WinSCP" que permite abrir archivos remotos de forma local en **Notepad++**. Monitorea los cambios automáticamente a través de un `FileSystemWatcher` para resincronizar y subir las modificaciones al servidor en tiempo real.
*   **Motor de Duplicación Inteligente:** Copia recursiva de archivos y directorios directamente de un servidor SFTP a otro, administrando colisiones mediante diálogos interactivos y asegurando la preservación exacta de permisos (chmod) y marcas de tiempo (touch) originales.
*   **Interfaz Gráfica Personalizable:** 
    *   Soporte para tema claro y tema oscuro (VS 2022 Dark).
    *   Iconos vectoriales dinámicos dibujados en tiempo real con GDI+ que representan la taxonomía de cada componente visualmente.
