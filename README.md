# Simple Calculations!

Step 1: Dokumentation zum Erstellen von Python Paketen
https://packaging.python.org/tutorials/packaging-projects/

Hier einfach an die Ordnerstruktur halten (zusätzlichen einen docs Ordner erstellen). 
In die setup.py kommt einfach der Code aus dem Tutorial. Diesen kann man später noch genauer anpassen.

Step 2: Sphinx-Dokumentation
https://www.sphinx-doc.org/en/master/usage/quickstart.html
- pip install sphinx
In den docs Ordner navigieren und hier folendes ausfüllen:
- sphinx-quickstart
Quickstart erstellt und build und source Ordner.
Die Eingabe der Befehle lautet: y, Projectname, Authorname, Projectrelease und Sprache.
Danach sollten ein build Ordner und ein Source Ordner innerhalb der Baumstruktur des Überordners vorhanden sein.


# Hier noch einige Installationen die gemacht werden müssen:

Step 3: In der Python Umgebung muss noch eine Verlinkung zum Paket erstellt werden, dafür wieder in den Überordner navigieren:
- python setup.py develop

Step 4: DocStrings werden automatisch via Sphinx auf HTML-Seite erfasst.
- pip install autodoc
Das Sphinx-rtd-theme stellt die HTML-Seite im ReadTheDocs Format dar. Es gibt auch andere Themes die man sich auf der
Website von Sphinx anschauen kann.
- pip install sphinx-rtd-theme

Step 5: In die conf.py Datei im Ordner ../docs/source das html_theme aus "sphinx-rtd-theme"
und unter extensions "sphinx.ext.autodoc" eintragen.

Step 6: HTML erstellen
Zum erstellen des HTML-Dokuments muss man sich im docs Ordner befinden.
Dort sollten auch der build und source Ordner liegen.
Mit dem folgenden Befehl wird die Datei modules.rst erzeugt:
- sphinx-apidoc -o source / ../calculation_pkg
- make html

Die html Dateien liegen nach Erstellung im Ordner docs/build/html.

Step 7: Falls zusätzliche Dokumentation erstellt werden soll, kann man einfach neue .rst Dateien einfügen.
Hier ist es wichtig, noch die calculation_pkg.rst Datei zu erstellen, da diese dann die Funktionen und deren Doctstrings
auf der html-Seite erfasst!

Weitere Darstellungen (hier z.B. die Ordner Guidelines und Options) können jederzeit eingefügt werden und mit
übersichtlichen Baumstrukturen auf der Website dargestellt werden. Siehe dazu die jeweiligen .rst Dateien in den Ordnern.
Wichtig hierbei ist, die Ordner und Dateien mit der index.rst zu verbinden.

