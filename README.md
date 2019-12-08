 Das Netzwerk der Toolbox Bodensee e.V.
==============================

**Entwicklung nur auf [GitLab](https://gitlab.com/ToolboxBodensee/toolbox-infrastructure/toolbox-netzwerk). Auf GitHub befindet sich lediglich ein Mirror**

# Git Hinweis

**Achtung**, dieses git repository enthält submodule. Diese können wie folgt runtergeladen werden:

```bash
# clone the git inclusive submodules
git clone --recursive https://gitlab.com/ToolboxBodensee/toolbox-infrastructure/toolbox-netzwerk.git

cd toolbox-netzwerk/
# clone and pull the submodules
git submodule update --init --recursive
```

## Protipp:
Der Befehl  ``git status`` ist immer gut um eine Übersicht zu bekommen, was in dem git momentan so los ist.<br/>
Wenn du keine Erfahrungen mit git hast ist im Zweifelsfall ein neu clonen mit submodulen die richtige Wahl.


 Mithelfen
------------

**Mitarbeit** ist hier gerne gesehen. Bei Fragen gerne einfach ein Issue öffnen oder komme Donnerstagsabends zum wöchentlichen Toolbox-Meeting in das Vereinsheim!
Wie du Zugänge bekommst, erfährst du in [ZUGANG.md](https://gitlab.com/ToolboxBodensee/toolbox-infrastructure/toolbox-netzwerk/tree/master/doc/ZUGANG.md)

 Netzwerk Setup
------------------
Wir haben einen Großteil des Netzwerkes auch per ansible deployed und damit für jeden einsehbar und anpassbar gemacht.
Eine grundlegende Übersicht dazu gibt es in der [NETZWERK.md](https://gitlab.com/ToolboxBodensee/toolbox-infrastructure/toolbox-netzwerk/tree/master/doc/NETZWERK.md).

 Doku
------
Für nützliche Hinweise gibt es das ``doc/`` Directory.

 Weitere Infos
----------------
Ein erste Ansible-Grundlagen-Crashkurs lässt sich u.a. auf media.ccc.de aufrufen:
* [Ansible-Crashkurs](https://media.ccc.de/v/gpn16-7574-ansible_crashkurs)

 Error Handling
-------------------------
Hinweise zu Fehlern der laufenden Services (zB. Strichlistenzertifikat ist abgelaufen) bitte ausschließlich per Gitlab Issue eintragen!)
Am besten direkt mit fixenden Pull-Request. Dann wird sich sicher ein IT-Arbeitsgruppenmitglied melden.
Du hast Lust bei uns mitzuarbeiten? Sprich das im Vereinsmeeting, jeden Donnerstagabend in der Toolbox, an!
