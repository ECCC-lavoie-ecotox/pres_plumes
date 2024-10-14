# :loudspeaker: PLUMES Talk

### Install deps

Install the following packages:

```R
install.packages(c('countdown','rmarkdown','xaringan'))
devtools::install_github("ropenscilabs/icon")
```

Once the `ìcon` package has been installed, you will have to download icons libraries.

```R
icons::download_ionicons()
icons::download_fontawesome()
```

Be aware that the package is named `icon` on github but uses the namespace `icons`.


### How to get a pdf version

Use [`pagedown`](https://github.com/rstudio/pagedown) as suggested in https://github.com/yihui/xaringan/issues/168 :

```R
install.packages('pagedown')
pagedown::chrome_print('index.html')
```

## Convert PlantUML to PNG

```bash
mkdir bin
wget -P bin/ https://github.com/plantuml/plantuml/releases/download/v1.2024.7/plantuml-1.2024.7.jar
java -jar bin/plantuml.jar hygge/img/db.puml
java -jar bin/plantuml.jar hygge/img/system.puml
```


