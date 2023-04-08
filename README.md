# Arq-TPI

* **Grupo 09**
* **Bari Gonzalo - Bouillín Ferri Benjamín - Gamietea Julián - Iviglia Juan José - Paz Gonzalo - Franco Siciliano**

## Requisitos

* AWS CLI
* Terraform
* OpenLens

## Set Up

### AWS CLI

* Abrir la consola de Lab en AWS Academy e iniciar el laboratorio.
* Copiar las credenciales de AWS CLI y pegarlas dentro de ~/./aws/credentials

### Terraform

1. Verificar que el "profile" en las primeras líneas del archivo `main.tf` coincida con el nombre del perfil importado en pasos anteriores (debería llamarse `default`).
2. Verificar que LabRole dentro del mismo archivo contiene el ARN correspondiente a su cuenta de AWS (este cambio es necesario solamente la primera vez que se corren los archivos).
    * Para verificar lo anterior, desde la consola de AWS ir a `IAM -> Roles` y buscar LabRole. Dentro de allí, verificar el ARN.
3. Abrir una sesión de terminal y dirigirse al directorio `terraform/modules/eks` dentro del repositorio.
4. Correr el comando `terraform init` para inicializar los módulos, proveedores y actualizar dependencias.
5. Correr el comando `terraform plan` para visualizar el plan de la configuración que va a aplicarse.
6. Correr el comando `terraform apply -auto-approve` para aplicar la configuración directamente.

### OpenLens

1. Abrir una sesión de terminal y correr el comando `aws eks update-kubeconfig --name "Arquitectura-cluster" --profile "default" --region "us-east-1"`.
    * El comando anterior obtiene el archivo de configuración de Kubernetes y lo coloca dentro de la carpeta `~/.kube/config`.
2. Dirigirse al directorio antes mencionado, abrir el archivo y copiar su contenido.
3. Abrir OpenLens y seleccionar la opción para crear un nuevo clúster (dentro de la barra superior).
4. Pegar el código antes obtenido y darle a aceptar.
5. Conectarse al clúster desde OpenLens haciéndole clic.

