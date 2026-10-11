# Portada i tema dels apunts de Bases de dades

Aquest repo fa dues coses:

1. Publica la portada a <https://bases-de-dades-26-27.github.io/>.
2. Defineix l'aspecte comú de tots els apunts (carpetes `_layouts`, `_includes` i `assets`). Si canvies el disseny aquí, canvia a totes les BA.

## Editar la portada

- Nom, curs, mòdul i institut: `_config.yml`.
- Llista de blocs: `_data/blocs.yml`. Per obrir una BA, posa l'adreça del seu repo a `url` (per exemple `url: /disseny/`). Si `url` està buit, surt com a "Properament".

## Afegir una BA nova

1. Crea un repo públic a l'organització (per exemple `disseny`) amb un `README.md` que faci d'índex i els apunts a `teoria/`.
2. Afegeix-hi un fitxer `_config.yml` com aquest:

   ```yaml
   remote_theme: bases-de-dades-26-27/bases-de-dades-26-27.github.io
   plugins:
     - jekyll-remote-theme

   ba: BA1
   ba_nom: Disseny de bases de dades relacionals
   ba_ra: RA1 i RA6
   ba_hores: 24
   lang: ca
   ```

3. Al repo nou: `Settings > Pages > Deploy from a branch`, branca `main`, carpeta `/ (root)`.
4. A `_data/blocs.yml` d'aquest repo, posa `url: /disseny/` a la BA corresponent.

## Consells per als fitxers .md

GitHub Pages és més estricte que la vista de GitHub:

- Deixa sempre una línia en blanc abans i després de cada taula.
- Deixa una línia en blanc abans de `---` (si no, el text de sobre es converteix en títol).
- Deixa una línia en blanc abans de `<!--` quan amaguis temes de l'índex.
