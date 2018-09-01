# Journal
## 20/05/18
- Ricerca del modello 3D nel sito [Sketchfab](https://sketchfab.com/).
- Scelto modello 3D di [chitarra elettrica](https://sketchfab.com/models/a998917d451b4b67ad402b1793c7b6c2#) da usare in formato glTF.
- Caricato modello usando come codice di partenza l'[esempio di loader glTF](https://github.com/mrdoob/three.js/blob/master/examples/webgl_loader_gltf.html) di three.js.

## 24/05/18
- Testati diversi shader sul modello per verificarne il funzionamento.

## 25/05/18
- Analisi interna della geometria del modello per comprendere la struttura gerarchica dei suoi componenti.

## 26/05/18 
- Il modello scelto presenta diversi problemi di modellazione e nella mappatura delle UV: modello scartato. 
- Scelto nuovo modello di [chitarra elettrica](https://sketchfab.com/models/7ab6e59ba93b46bd8afa981fef92f114).
- Analisi interna della geometria del nuovo modello per comprendere la sua struttura gerarchica.
- Prova di caricamento di una texture da utilizzare come materiale. 
- Prova di scrittura del fragment shader per parti metalliche.

## 27/05/18
- Provati diversi valori cspec nella BRDF per i metalli.
- Prova di aggiunta normal map alle texture: non funziona. 
- Inserita nuova cubemap presa da questo [link](https://reije081.home.xs4all.nl/skyboxes/).
- Iniziata stesura del codice partendo dal vertex e dal fragment shader per materiali metallici.
- Confrontate tecniche di reflection map e specular reflection per i metalli: risultato quasi identico, mantenuto reflection map.
- Inseriti shader per il materiale plastico.

## 28/05/18
- Inserito shader per il materiale in legno.
- Inserita normal map per la texture del legno.
- Inseriti due nuove varianti di legno.
- Inizio scrittura del form per la personalizzazione del prodotto prendendo spunto da questo [sito](https://threekit.com/3d-product-demos/mens-polo-shirt-clothing/).

## 29/05/18
- Ricerca su possibili form da utilizzare. 

## 30/05/18
- Ridimensionata finestra di rendering 
- Inserito menù per personalizzare il tipo di legno del corpo della chitarra.

## 31/05/18
- Inserito menù per personalizzare il tipo di metallo della chitarra.
- Il materiale metallico non è soddisfacente: sostituita reflection map con specular reflection.
- Sostituita la cubemap con un'altra presa a questo [link](http://www.humus.name/index.php?page=Cubemap&item=Yokohama)
- Aggiunta seconda luce. 
- Migliorato l'aspetto della pagina web in cui verrà visualizzato il modello.
- Disabilitato il pan della camera.
- Modificati i limiti dello zoom minimo e massimo in modo da evitare la penetrazione dell'oggetto.
- Inserito menù e migliorato pannello di personalizzazione dei materiali nella pagina web.

## 1/06/18
- Creati vertex e fragment shader per materiale lambertiano da assegnare al manico e al bordo del corpo della chitarra.
- Scelta posizione delle luci in modo da esaltare la tridimensionalità delle forme del modello.
- Aggiunta terza luce e riposizionate tutte le luci: due ai lati, una sopra leggermente dietro

## 3/06/18
- Tentativo di inserimento delle ombre nel modello: non riuscito.
- Corretta illuminazione e modificate nuovamente la posizione delle luci: una centrale davanti all'oggetto, due posteriori ai lati, sopra l'oggetto. 

## 4/06/18 
- Refactoring del codice. 

## 8/06/18
- Refactoring del codice.