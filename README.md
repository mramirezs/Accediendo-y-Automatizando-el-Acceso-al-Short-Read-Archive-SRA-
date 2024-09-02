# Accediendo y Automatizando el Acceso al Short Read Archive (SRA)

## Objetivos de la Clase

- Comprender qué es el Short Read Archive (SRA) y su importancia en la bioinformática.
- Aprender a descargar y gestionar datos de SRA utilizando diferentes herramientas.
- Automar la descarga y filtrado de datos de SRA mediante scripts.
- Aplicar conocimientos prácticos en la descarga y procesamiento de datos SRA.

## Contenido

### 1. ¿Qué es el Short Read Archive (SRA)?

El Short Read Archive (SRA) es una base de datos pública que almacena secuencias de lectura corta generadas por tecnologías de secuenciación de alto rendimiento. Es un recurso crucial para los investigadores que necesitan acceder a datos genómicos y transcriptómicos.

### 2. Esquemas de Nomenclatura en SRA

Los datos en SRA se organizan con identificadores específicos como:

- **SRR**: Identificador para un run de secuenciación.
- **SRS**: Identificador para un set de muestras.
- **SRP**: Identificador para un proyecto de secuenciación.

### 3. ¿Cómo Descargar Datos de SRA?

Existen varias maneras de descargar datos desde SRA:

1. **sratoolkit**: Un conjunto de herramientas proporcionado por NCBI para interactuar con SRA.
   - Comando básico: `fastq-dump --split-3 SRR1234567`
2. **NCBI Entrez Direct**: Utilizado para hacer consultas y descargas mediante línea de comandos.

### 4. Alternativas al SRA

- **ENA (European Nucleotide Archive)**: Similar a SRA, pero gestionado por el EBI.
- **DDBJ (DNA Data Bank of Japan)**: Archivo japonés que también tiene secuencias de lectura corta.

### 5. Documentación del SRA

La documentación completa para trabajar con SRA está disponible en el [sitio web de NCBI](https://www.ncbi.nlm.nih.gov/sra/docs/).

### 6. ¿Cómo Funciona sratoolkit?

`sratoolkit` permite convertir los datos descargados en diferentes formatos, por ejemplo, `fastq-dump` convierte archivos `.sra` en archivos `.fastq`.

### 7. Consultas Simples en SRA

Utiliza Entrez Direct para hacer consultas simples:

```bash
esearch -db sra -query "SRR1234567" | efetch -format runinfo
