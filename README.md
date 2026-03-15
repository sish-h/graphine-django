# Graphine Django
A Django app for building and visualizing graph data structures.

## What it does
Graphine Django provides a simple and intuitive way to create, manipulate, and display graph data in your Django application. It uses a combination of Python and JavaScript libraries to render interactive graph visualizations.

## Installation
To get started, install the package using pip:
```bash
pip install graphine-django
```
Then, add 'graphine_django' to your INSTALLED_APPS in settings.py.

## Running the app
Run the following commands to create the database tables and start the development server:
```bash
python manage.py migrate
python manage.py runserver
```
## Example usage
Create a new graph node in your Django shell:
```python
from graphine_django.models import Node

node = Node.objects.create(name='My Node')
node.save()
```
Then, use the included template tags to display the graph in your Django template:
```django
{% load graphine_tags %}

{% graph my_graph %}
    {% node node %}
{% endgraph %}
```
Check out the docs for more information on how to use Graphine Django in your project.