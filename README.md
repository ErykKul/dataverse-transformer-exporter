# Transformer Exporter
This Dataverse exporter allows you to have up to a 100 exporters using one single pre-built jar. All you need to do is to download that jar into your exporters directory and create an other directory within the exporters directory (up to 100 of them) containing at least a `config.json` and a `transformer.json` files. Edit these files to achieve the exporter you need. Use the provided [examples](/examples/) and the developer guide section as inspiration.

## Installation

If not yet configured, set the [dataverse-spi-exporters-directory](https://guides.dataverse.org/en/latest/installation/config.html#dataverse-spi-exporters-directory) configuration value first. Then `cd` into that directory you configured and download the [jar file](https://repo1.maven.org/maven2/io/github/erykkul/dataverse-transformer-exporter/1.0.1/dataverse-transformer-exporter-1.0.1-jar-with-dependencies.jar) together with the examples you want to try out:

```shell
# download the jar
wget -O transformer-exporter-1.0.1.jar https://repo1.maven.org/maven2/io/github/erykkul/dataverse-transformer-exporter/1.0.1/dataverse-transformer-exporter-1.0.1-jar-with-dependencies.jar
# download the hello-world example
mkdir hello-world
wget -O hello-world/config.json https://raw.githubusercontent.com/erykkul/dataverse-transformer-exporter/main/examples/hello-world/config.json
wget -O hello-world/transformer.json https://raw.githubusercontent.com/erykkul/dataverse-transformer-exporter/main/examples/hello-world/transformer.json
# download the debug example
mkdir debug
wget -O debug/config.json https://raw.githubusercontent.com/erykkul/dataverse-transformer-exporter/main/examples/debug/config.json
wget -O debug/transformer.json https://raw.githubusercontent.com/erykkul/dataverse-transformer-exporter/main/examples/debug/transformer.json
# download the short-example example
mkdir short-example
wget -O short-example/config.json https://raw.githubusercontent.com/erykkul/dataverse-transformer-exporter/main/examples/short-example/config.json
wget -O short-example/transformer.json https://raw.githubusercontent.com/erykkul/dataverse-transformer-exporter/main/examples/short-example/transformer.json
# download the javascript-transformer example
mkdir javascript-transformer
wget -O javascript-transformer/config.json https://raw.githubusercontent.com/erykkul/dataverse-transformer-exporter/main/examples/javascript-transformer/config.json
wget -O javascript-transformer/transformer.json https://raw.githubusercontent.com/erykkul/dataverse-transformer-exporter/main/examples/javascript-transformer/transformer.json
mkdir javascript-transformer/js
wget -O javascript-transformer/js/short_example.js https://raw.githubusercontent.com/erykkul/dataverse-transformer-exporter/main/examples/javascript-transformer/js/short_example.js
# download the croissant example
mkdir croissant
wget -O croissant/config.json https://raw.githubusercontent.com/erykkul/dataverse-transformer-exporter/main/examples/croissant/config.json
wget -O croissant/transformer.json https://raw.githubusercontent.com/erykkul/dataverse-transformer-exporter/main/examples/croissant/transformer.json
mkdir croissant/js
wget -O croissant/js/croissant.js https://raw.githubusercontent.com/erykkul/dataverse-transformer-exporter/main/examples/croissant/js/croissant.js
# download the basic-ro-crate example
mkdir basic-ro-crate
wget -O basic-ro-crate/config.json https://raw.githubusercontent.com/erykkul/dataverse-transformer-exporter/main/examples/basic-ro-crate/config.json
wget -O basic-ro-crate/transformer.json https://raw.githubusercontent.com/erykkul/dataverse-transformer-exporter/main/examples/basic-ro-crate/transformer.json
# download the generated-with-python example
mkdir generated-with-python
wget -O generated-with-python/config.json https://raw.githubusercontent.com/erykkul/dataverse-transformer-exporter/main/examples/generated-with-python/config.json
wget -O generated-with-python/transformer.json https://raw.githubusercontent.com/erykkul/dataverse-transformer-exporter/main/examples/generated-with-python/transformer.json
```

After restarting the Dataverse, you should be able to use the newly installed exporters (next to the internal exporters):

![image](https://github.com/ErykKul/dataverse-transformer-exporter/assets/101262459/57241319-ce45-40b4-8777-401252f6c4d4)

Each exporter will have at least these files after starting:

![image](https://github.com/ErykKul/dataverse-transformer-exporter/assets/101262459/837405e1-4abe-4470-a9fe-0af3d1ee727d)

All of these files can be edited, if needed. Typically you will only need to edit the `config.json` and the `transformation.json` files.

## Examples

## Developer guide
