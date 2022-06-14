![logo_ironhack_blau 7](https://user-images.githubusercontent.com/23629340/40541063-a07a0a8a-601a-11e8-91b5-2f13e4e6b441.png)

# LAB | Vue.js IronContacts

## Introducció

Després d'Ironhack, has decidit treballar a la indústria del cinema i has trobat una feina on has de gestionar els contactes d'un famós productor.

La vostra tasca és crear una aplicació de gestió de contactes per al productor mitjançant Vue.js.

## Configuració

- Bifurca aquest repo
- Clona aquest repo
- Obriu el LAB i comenceu:

  ```bash
   $ cd lab-vue-ironcontacts-cat
   $ npm install
   $ npm start
  ```

## Submissió

- En finalitzar, executeu les ordres següents:


  ```bash
  git add .
  git commit -m "done"
  git push origin main
  ```

- Creeu una sol·licitud d'extracció perquè els vostres TA puguin comprovar el vostre treball.

## Començant

Netegeu el component `App.js` perquè tingui l'estructura següent:

```js
// src/App.js
import "./App.css";

function App() {
  <template>
  <div id="app"></div>
</template>
}
export default App;
```

## Instruccions

### Iteració 1 | Mostra 5 contactes

Fem una ullada al codi d'inici.

Dins de la carpeta `src` tenim un fitxer `contacts.json` que conté els contactes del productor. Importeu el fitxer `contacts.json` a `App.vue` . Un cop fet, creeu una variable de referència anomenada `contacts` i deseu una **matriu que contingui els 5 primers contactes** .

Mostra aquesta matriu de 5 contactes com una llista en una `i mostra la picture , el name i la popularity de cada contacte.`

De moment, renderitzem el contingut a `App.vue` . Dit això, no procediu a crear un component dedicat per a la llista de contactes. El motiu serà una mica més clar més endavant quan afegim el botó d'eliminació al costat de cada contacte. Probablement encara no esteu familiaritzat amb el concepte d'"elevació de l'estat" i de passar les devolució de trucades com a accessoris. Per aquest motiu, és millor representar-ho tot en un component de moment.

Continuem.

Per importar `contacts.json` a `App.vue` , podeu utilitzar:

```js
import contacts from "./contacts.json";
```

Al final d'aquesta iteració, la vostra aplicació hauria de tenir aquest aspecte:

<details><summary> Comproveu la imatge a l'interior - Iteració 1 </summary>

![Captura de pantalla - Iteració 1](https://education-team-2020.s3.eu-west-1.amazonaws.com/web-dev/labs/lab-react-ironcontacts-1.png)

</details>

### Iteració 2 | Mostra condicionalment la informació dels premis

Al productor li agradaria veure la informació sobre els _premis_ que ha guanyat el contacte.

Actualitza la llista i afegeix dues columnes més "Won an Oscar" i "Won an Emmy", al final de la taula. Aleshores, depenent del valor `wonOscar` i `wonEmmy` de cada contacte, representa condicionalment una icona de trofeu que :trophy: o cap contingut.

Un cop feta, la vostra aplicació hauria de tenir aquest aspecte:

<details>

<summary> Comproveu la imatge a l'interior - Iteració 2</summary>

![Captura de pantalla: iteració 2](https://education-team-2020.s3.eu-west-1.amazonaws.com/web-dev/labs/lab-react-ironcontacts-2.png)

</details>

### Iteració 3 | Afegeix nous contactes aleatoris

A la vostra aplicació, creeu un botó _Afegeix un contacte aleatori_ . Cada vegada que feu clic a aquest botó, hauria d'afegir un nou contacte aleatori als `contacts` . Hauríeu d'obtenir contactes aleatoris dels contactes restants que encara no es mostren.

Primer, seleccioneu aleatòriament un contacte de la sèrie de contactes restants. A continuació, afegiu aquest contacte a la matriu que viu a la vostra referència de dades (és la matriu de 5 contactes creada anteriorment).

Al final d'aquesta iteració, el vostre lloc web probablement tindrà aquest aspecte:

<details><summary> Comproveu la imatge a l'interior - Iteració 3 </summary>

![Captura de pantalla: iteració 3](https://education-team-2020.s3.eu-west-1.amazonaws.com/web-dev/labs/lab-react-ironcontacts-3.png)

</details>

### Iteració 4 | Ordena els contactes per nom i popularitat

El productor us va demanar que afegiu dos botons nous per ajudar-los a ordenar els contactes. Quan feu clic a un dels botons, hauria d' **ordenar la taula per `name`** (alfabèticament), i quan feu clic a l'altre, hauria d' **ordenar per `popularity`** (el més alt primer).

Un cop hàgiu ordenat la matriu, recordeu actualitzar la variable d'estat que conté els contactes.

Això és el que hauríeu de tenir al final d'aquesta iteració:

<details><summary> Comproveu la imatge a l'interior - Iteració 4 </summary>

![Captura de pantalla: iteració 4](https://education-team-2020.s3.eu-west-1.amazonaws.com/web-dev/labs/lab-react-ironcontacts-4.png)

</details>

### Iteració 5 | Elimina els contactes

El productor també vol eliminar alguns dels seus contactes. Implementeu un botó Suprimeix a cada fila de la vostra `<taula>` que permetrà a l'usuari eliminar el contacte en què va fer clic.

Quan facin clic, hauríeu d'obtenir l' `id` d'aquest actor i utilitzar-lo per eliminar el contacte de la matriu. Recordeu actualitzar la variable d'estat que conté els contactes després d'eliminar el contacte!

Quan hagi acabat, la vostra aplicació hauria de tenir aquest aspecte (després de jugar una mica amb el botó _Suprimeix_ ):

<details><summary> Comproveu la imatge a l'interior - Iteració 5 </summary>

![Captura de pantalla: iteració 5](https://education-team-2020.s3.eu-west-1.amazonaws.com/web-dev/labs/lab-react-ironcontacts-5.png)

</details>

### Iteració 6 | Bonificació | Estilisme

Malauradament, aquesta llista de contactes no està preparada per a la producció. Estem al negoci del cinema! Ha de brillar! Afegiu una mica de CSS bonic per fer que l'aplicació "pop".

<br/>

**Feliç codificació!** :blue_heart: