# MathType On-Premises Backend (Docker)

## Services configuration

A full MathType integration depends on 3 services:

1. **MathType Editor Services**:  
These serve the editor API for rendering and conversion features.
2. **MathType Integration Services**:  
These handle the MathType integration global configuration, the front-back communication and the rendering cache.
3. **MathType Handwriting Services**:  
These serve the handwriting recognition feature.

It is required to configure their setting files in this repository configurations folder. These will be automatically placed in their working location when the MathType Docker image of the services is built.

- **editor-web.xml**:  
Holds the parameters that configure the MathType Editor Services Java servlet and license.
- **configuration.ini**:  
Holds the parameters of the MathType Integration Services, such as the settings for MathType Editor Services connectivity, export, caching, etc.
- **hand-web.xml**:  
Holds the parameters that configure the MathType Handwriting Services Java servlet.

## Placeholder replacement

The *mathtype-wars* folder in this repository is to hold the MathType Services WAR files needed to create the MathType Docker image of the services.

The current *.placeholder* extension WAR files are just placeholders to show where to place the real services WARs. They need to be replaced before initiating the MathType Docker image of the services.

The real files can be downloaded right after purchasing your license. Please, contact your Key Account Manager if you need help finding them. You can also send us an email to *support@wiris.com*.

## Docker image instantiation

This repository has been built using Docker Compose. The docker-compose.yml and the Dockerfile.mathtype are configured to deploy the MathType On-Premises Backend using the configuration and WAR files mentioned before.

Additionally, the entrypoint.sh script holds the necessary instructions to be run on image creation to install and run the MathType Services.

> ⚠️ The configuration and WAR files need to be configured and replaced as explained in the previous sections before instantiating a new MathType Docker image of the services.

To initiate the MathType on-premises backend Docker instance run the following command in the project root:

```
docker compose up
```
## Support

For issues or questions regarding this repository, MathType, its services or any other question regarding Wiris or its products, please, contact us at:  
*support@wiris.com*




