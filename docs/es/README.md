# Este repositorio todavía esta en desarrollo.

# Taller de Django + React + Redux
Este repositorio va a ser usado en la PyconAr2017 para dar el paso a paso del taller
"Django + React + Redux".

## Modalidades del repositorio
Para poder ir aprendiendo el repositorio hace el paso a paso para generar una
proyecto productivo con estas tecnologías.
Cada paso esta en una rama aparte con los archivos correspondiente del proyecto
en ese paso determinado.
Las ramas (pasos):
- Paso 1: [Crear proyecto de Django](https://gitlab.com/FedeG/django-react-workshop/tree/step1_create_project)
- Paso 2: [Crear aplicación de Django](https://gitlab.com/FedeG/django-react-workshop/tree/step2_create_django_app)
- Paso 3: [Agregar una vista sin React](https://gitlab.com/FedeG/django-react-workshop/tree/step3_add_non_react_views)
- Paso 4: [Agregar modelo de Django](https://gitlab.com/FedeG/django-react-workshop/tree/step4_add_django_models)
- Paso 5: [Agregar django_webpack_loader](https://gitlab.com/FedeG/django-react-workshop/tree/step5_add_django_webpack_loader)
- Paso 6: [Crear la primer componente de React](https://gitlab.com/FedeG/django-react-workshop/tree/step6_create_first_react_component)
- Paso 7: [Usar el paquete con React](https://gitlab.com/FedeG/django-react-workshop/tree/step7_use_the_bundle)
- Paso 8: [Recarga automática](https://gitlab.com/FedeG/django-react-workshop/tree/step8_hot_reloading)
- Paso 9: [Python linter](https://gitlab.com/FedeG/django-react-workshop/tree/step9_python_linter)
- Paso 10: [React linter](https://gitlab.com/FedeG/django-react-workshop/tree/step10_react_linter)
- Paso 11: [Python testing](https://gitlab.com/FedeG/django-react-workshop/tree/step11_python_testing)
- Paso 12: [React testing](https://gitlab.com/FedeG/django-react-workshop/tree/step12_react_testing)
- Paso 13: [Enviar contexto de Django en React](https://gitlab.com/FedeG/django-react-workshop/tree/step13_django_context_in_react)
- Paso 14: [Api rest y fetch de datos](https://gitlab.com/FedeG/django-react-workshop/tree/step14_api_rest)
- Paso 15: [Django channels y websockets](https://gitlab.com/FedeG/django-react-workshop/tree/step15_websockets_and_channels)
- Paso 16: [Entorno de producción](https://gitlab.com/FedeG/django-react-workshop/tree/step16_going_to_production)
- Paso 17: [Agregar Redux](https://gitlab.com/FedeG/django-react-workshop/tree/step17_add_redux)
- Paso 18: [Css y scss en React](https://gitlab.com/FedeG/django-react-workshop/tree/step18_inline_styles)

Cada rama tiene la documentación en español (`README-es.md`) y en ingles (`README.md`).

## Requirimientos del proyecto
Los requerimientos van variando a lo largo del proyecto, como este repositorio todavía
puede que alguno todavía no esten.
Mi recomendación para hacer el curso rápido es que te instales de antemano los mas posible.
En mi caso me gusta usar docker como se puede ver en cada paso pero también esta la
opción sin docker para la gente que no lo usa.

#### Instalación previa con Docker
```bash
# Clonar el repositorio
git clone https://gitlab.com/FedeG/django-react-workshop.git
cd django-react-workshop

# Python y Django
docker run -d -it --name workshop -v $PWD:/src -p 8000:8000 --workdir /src python:3.6 bash
docker exec -it workshop pip install -r requirements.txt
docker exec -it workshop pip install -r requirements-doc.txt
docker exec -it workshop pip install -r requirements-dev.txt

# Node y React
docker run -d -it --name workshopjs -v $PWD:/src -p 3000:3000 --workdir /src/workshop/front node:8 bash
docker exec -it workshopjs npm install yarn --global
docker exec -it workshopjs yarn install
```
##### Nota: el dia del evento ya va a existir una imagen con todo incluido en el caso de que alguien no tenga red

#### Instalación previa sin Docker
```bash
# Clonar el repositorio
git clone https://gitlab.com/FedeG/django-react-workshop.git
cd django-react-workshop

# Python y Django
## Instalar python 3 (3.5 o 3.6 idealmente)
pip install -r requirements.txt
pip install -r requirements-doc.txt
pip install -r requirements-dev.txt

# Node y React
curl -sL https://deb.nodesource.com/setup_8.x | sudo -E bash -
sudo apt-get install -y build-essential nodejs
npm install yarn --global
cd workshop/front
yarn install
```