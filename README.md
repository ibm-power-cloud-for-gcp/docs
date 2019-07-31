# docs

Documents, artifacts, diagrams, etc for the IBM Power in GCP

## Directory layout

* `/configuration.yaml` - contains the metadata used for templating
* `/devops` - location for devops tools
  * `/tools` - marked-it-cli installation location
* `/format` - support javascript used to convert markdown to html
* **`/markdown`** - location for documentation files

## Building manually

1. Install nodejs. \[ [Mac OS](https://nodejs.org/en/download/package-manager/#macos) | [Windows 10](https://nodejs.org/en/download/package-manager/#windows) \]
1. Install packages in `devops/tools`

    ```shell
    cd devops/tools
    npm install
    ```

1. Run the marked-it-cli to generate the output

    ```shell
    devops/tools/node_modules/.bin/marked-it-cli markdown --output=./html --extension-file=./format/headerFooterExt.js --conref-file=./configuration.yml
    ```

    This will build the markdown files in the `markdown` directory and output it to
    the `html` directory.


    `configuration.yml` contain any metadata variables that can be included in
    the markdown. See: [GitHub](https://github.com/ibm/marked-it-cli)
