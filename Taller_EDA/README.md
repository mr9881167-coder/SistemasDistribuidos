# Taller EDA — Dinámicas Salariales en Ciencia de Datos e IA

## Contenido

- `Taller_EDA.Rmd` — archivo fuente reproducible (RMarkdown) con las 6 actividades del taller.
- `Taller_EDA.pdf` — informe final compilado (cuerpo analítico ≤ 10 páginas + anexo técnico de código).
- `data/ds_salaries.csv` — conjunto de datos utilizado (Data Science / AI Job Salaries).

## Paquetes requeridos

```r
install.packages(c("rmarkdown", "knitr", "dplyr", "ggplot2", "e1071", "tidyr", "scales"))
```

En Ubuntu/Debian también se pueden instalar vía apt:

```bash
sudo apt-get install r-base r-cran-knitr r-cran-rmarkdown r-cran-dplyr \
  r-cran-ggplot2 r-cran-e1071 r-cran-tidyr r-cran-scales pandoc \
  texlive-latex-base texlive-latex-recommended texlive-latex-extra \
  texlive-fonts-recommended lmodern
```

## Cómo compilar el informe

Desde esta carpeta (`Taller_EDA/`), en R o RStudio:

```r
rmarkdown::render("Taller_EDA.Rmd")
```

**Nota sobre codificación (Linux/servidores sin locale configurado):** si el
sistema usa el locale `C`/`POSIX` (sin soporte UTF-8), los caracteres
acentuados pueden mostrarse incorrectamente en tablas y gráficos. En ese caso,
compilar forzando un locale UTF-8, por ejemplo:

```bash
LANG=C.utf8 LC_ALL=C.utf8 Rscript -e 'rmarkdown::render("Taller_EDA.Rmd")'
```

En Windows/RStudio con configuración regional estándar esto no es necesario.
