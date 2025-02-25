---
title: Control de versions
icon: material/source-branch-check
alias: control-versions
---

# :material-source-branch-check: Control de versions
Utilitzar un __sistema de control de versions__ d'una manera estructurada i ordenada
és una pràctica imprescindible per a qualsevol projecte de programació,
sobretot si participen més d'una persona.


## Ferramentes
En aquest projecte utilitzarem les següents ferramentes per al control de versions:

- [:simple-git: Git][git]: sistema de control de versions distribuït.
- [:simple-github: GitHub][github]: plataforma d'allotjament de repositoris de Git.

[git]: https://git-scm.com/
[github]: https://github.com/


## Estratègia de ramificació
El desenvolupament del projecte es farà seguint una estratègia de ramificació
que proporcionarà un flux de treball ordenat i estructurat.

Aquesta estratègia es basa en la creació de branques per a diferents propòsits:

- __Branca principal `main`__: Conté el codi estable que ha segut publicat.
- __Branca de desenvolupament `develop`__: Conté la versió més actualitzada del codi,
    però que encara no ha sigut publicada.
- __Branques de funcionalitats `feature/*`__: Cada funcionalitat nova es desenvolupa en una branca pròpia.

    Depenent de la naturalesa del canvis, es pot optar per utilitzar diferents prefixes: `feature/`, `fix/`, etc.

- __Branques de publicació `release/*`__: Branca temporal per a preparar la publicació d'una nova versió.

[estrategies-ramificacio]: https://joapuiib.github.io/curs-git/apunts/05_estrategies/01_estrategies_ramificacio/

El mètode per integrar les branques de funcionalitats es realitzarà mitjançant
un `merge --squash` per a mantenir l'historial de commits net i ordenat.

![Fusió de branques en un sol commit](./img/merge_squash.png)
/// figure-caption
Fusió de branques mitjançant `merge --squash`.
///

Podeu consultar el flux de treball complet en els apunts [Estratègies de ramificació][estrategies-ramificacio].


## Pull Requests
Dins de l'àmbit de gestió del projectes, :simple-github: GitHub proporciona una eina
anomenada __:material-source-pull: Pull Request__ que permet sol·licitar la integració de canvis d'una branca
a una altra.

Podeu consultar els apunts [Forks i Pull Requests][forks-pull-requests] per a més informació.

[forks-pull-requests]: https://joapuiib.github.io/curs-git/apunts/06_projectes/02_forks/#pull-requests

!!! tip
    És recomanable configurar el repositori per a requerir els següents aspectes:

    - __Pull Request requerida__: No es permetrà fer commits directament a la branca principal ni de desenvolupament,
        que sols podran integrar canvis mitjançant Pull Requests.
    - __Història lineal__: No es permetran commits amb història no lineal.
    - __Integració `merge --squash`__: Deshabilitar els altres mètodes d'integració en les Pull Requests.

