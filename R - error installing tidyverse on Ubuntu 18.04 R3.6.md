**Environment:** Ubuntu 18.04 / R version 3.6
Error occurs when install package "tidyverse" because there are issues installing dependencies:
* curl
* openssl
* xml2

**Troubleshooting**
1. In R run `install.packages("RCurl")`
2. In terminal run the command `sudo apt-get install openssl libssl-dev`
3. In terminal run the command `sudo apt-get install libxml2-dev`
4. In R run `install.packages("tidyverse")`

problem solved :)
