# Simple Calculations!

# Hilfreiche Links:

Dokumentation zum Erstellen von Python Paketen
- https://packaging.python.org/tutorials/packaging-projects/

Ich empfehle den Sphinx Quickstart durchzuführen, da damit eine conf.py mit den ersten wichtigen Informationen.
Hier kann man bereits Autor usw. erfassen. Desweiteren kann man entscheiden ob build und source
getrennt voneinander erstellt werden sollen.
- sphinx-quickstart

# Hier noch eine Installationen die gemacht werden müssen:

In der Python Umgebung muss noch eine Verlinkung zum Paket erstellt werden.
- python setup.py develop

Sphinx wandelt reStructredText in HTML-Seiten um.
- pip install sphinx

DocStrings werden automatisch via Sphinx auf HTML-Seite erfasst.
- pip install autodoc

Das Sphinx-rtd-theme stellt die HTML-Seite im ReadTheDocs Format dar. Es gibt auch andere Themes die man sich auf der
Website von Sphinx anschauen kann.
- pip install sphinx-rtd-theme

Zum erstellen des HTML-Dokuments muss man sich im docs Ordner befinden.
Dort sollten auch der build und source Ordner liegen:
- sphinx-apidoc -o source / ../calculation_pkg
- make html

Die html Dateien liegen nach Erstellung im Ordner docs/build/html.
