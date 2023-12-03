# Link Download Doc Codelab

![enter image description here](https://raw.githubusercontent.com/RayCatcherS/CodelabFlutterUni/main/media/repository_codelab1.png)

# 

# (Lezione 1)

# Flutter

Flutter è un framework open-source di Google per creare User Interface native su un'unica unica code base, unico codice e possiamo compilare applicazioni su più piattaforme(Android, iOS, Windows, macOS, Linux, Web).

### Vantaggi:

#### Prestazioni e compatibilità

- Le applicazioni sviluppate con Flutter girano nativamente sui dispositivi, questo vuol dire che le prestazioni sono elevate(frame rate elevato), il rendering è a basso livello e utilizzando la libreria grafica di Google, Skia.
- Flutter si interfaccia con gli SDK del sistema operativo su cui gira(Android o iOS) quindi è anche possibile creare funzionalità specifiche rispetto al sistema su cui l'applicazione gira.

#### Debug

- In Flutter, il Debug è molto semplice, durante lo sviluppo è possibile visualizzare ed eseguire l'applicazione in modalità **debug mode**
- **Flutter inspector**, è uno strumento potente per visualizzare il layout della vostra applicazione in sviluppo, oltre che per visualizzare il layout è molto utile per diagnosticare e intercettare problemi di layout dell'app. 
- Una funzionalità apprezzata dagli sviluppatori è "l'**hot-reload**" che consente di iniettare e visualizzare istantaneamente le modifiche fatte dall'editor  sull'esecuzione dell'app, senza dover ricompilare l'intero codice. Questo ne ottimizza il workflow dello sviluppatore e le varie fasi di debug.

#### Curva di apprendimento

- Flutter è molto più **facile da imparare**(Dart) rispetto ad altri frameworks in cui si usa javascript come linguaggio per React Native
- Il linguaggio Dart è un linguaggio molto più **intuitivo** e anche **più vicino ai paradigmi di programmazione** ed è molto simile ai linguaggi di programmazione usati nello sviluppo di app mobili native(Java o Kotlin)

#### Popolarità e community

- La popolarità di Flutter è in continua **crescita** da quando è disponibile per tutti gli sviluppatori infatti è possibile constatare da sondaggi fatti su Stack Overflow che l'interesse da parte degli sviluppatori è in continua crescita:
  
  > Source: Stack Overflow Survey 2019
  > ![enter image description here](https://assets-global.website-files.com/5c95072393140f36ecc22e60/62dffd4949fd4431fc61af6e_stackoverflowdeveloper.png)

>  Stack Overflow Survey 2021![enter image description here](https://assets-global.website-files.com/5c95072393140f36ecc22e60/61a88d171443ca70ce8f5e6e_image_2021-12-02_100839.png)

Nell'ultimo sondaggio su Stack Overflow notiamo che Flutter e React Native sono in stretta competizione 

> Stack Overflow Survey 2023![enter image description here](https://assets-global.website-files.com/5c95072393140f36ecc22e60/63f524b9f421c14106114339_Screen%20Shot%202023-02-21%20at%2020.38.40%20%281%29.png)

- Essendo anche la Community di Flutter in costante crescita dalla sua uscita, è possibile ritrovare sul web una vasta community di sviluppatori e librerie da integrare per i progetti Flutter

# Installazione e configurazione

Probabilmente questa sarà la parte più difficile di questo codelab, ovvero installare tutto e assicurarsi che funzioni. È l'unica cosa meno divertente ma è importante per iniziare a sviluppare applicazioni in Flutter.

### 2) Installazione di Flutter

Per prima cosa scarichiamo l'sdk di flutter da [questo indirizzo](https://docs.flutter.dev/get-started/install). Una volta scaricato, estrarre il contenuto dell'archivo in:  

> C:\SDKs

Creare una cartella SDK per posizionare l'SDK di Flutter. La posizione finale sarà: 

>  C:\SDKs\flutter

### 3) Configurare Path di sistema

È estremamente importante aggiornare il PATH nelle variabili di sistema.
Per eseguire i comandi Flutter attraverso la console di Windows sarà necessario aggiungere al PATH la variabile di ambiente. Nella barra di ricerca di Windows inserisci "**env**" e seleziona "**Modifica variabili di ambiente**" e aggiungi questo percorso: 

>  C:\SDKs\flutter\bin

![](https://raw.githubusercontent.com/RayCatcherS/CodelabFlutterUni/main/media/steps/flutter_path.png)
Per verificare che tutto funzioni, chiudere tutte i terminali Windows eventualmente aperti, aprire un Terminale ed eseguire il comando:

> flutter doctor

Se si dovesse verificare un errore con codice **"Error: Unable to find git in your PATH."** segui la guida chiamata "gitError/GitError.pdf" all'interno della cartella "CodelabFlutterUni-main".

### 4) Installazione Tool Sviluppo Windows

In questo Codelab scriveremo una piccola app per Windows e Flutter per compilare la base di codice avrà bisogno del kit di sviluppo Windows.
Scaricare il setup del kit di sviluppo windows Visual Studio 2022, [Scaricabile da qui.](https://visualstudio.microsoft.com/it/thank-you-downloading-visual-studio/?sku=Community&channel=Release&version=VS2022&source=VSLandingPage&cid=2030&passive=false) **Attenzione non stiamo parlando dell'editor Visual Studio Code!**. 
Una volta scaricato il **setup di Visual Studio 2022** bisogna verificare nelle impostazioni di installazione che “Desktop development with C++” sia selezionato, incluse tutte le componenti di default. 
![desc](https://raw.githubusercontent.com/RayCatcherS/CodelabFlutterUni/main/media/steps/visual_studio_desktop_Develpment_with_C%2B%2B.png)

### 5) Installazione di Visual Studio Code

Useremo Visual Studio Code perchè è semplice, affidabile e lo usano molte persone. Chiaramente è gratis.
[Link installazione](https://code.visualstudio.com/#alt-downloads)

### 6) Installazione Plugin Flutter

Apri l'editor di Visual Studio Code e Installa il plugin flutter 
![desc](https://raw.githubusercontent.com/RayCatcherS/CodelabFlutterUni/main/media/steps/flutter_plugin.png)

# Codelab di oggi

Questo corso accelerato è una rielaborazione di un Codelab(Tutorial) di Google ([Fonte codelab](https://codelabs.developers.google.com/codelabs/flutter-codelab-first#0))  di cui oggi vedremo: 

- Creare la prima app
- Capire le basi del funzionamento di Flutter
- Creare un layout per la nostra prima app
- Collegare le interazioni dell'utente al comportamento dell'app(usando ad esempio un pulsante e visualizzando il risultato a schermo)
- Organizzare il codice Flutter
- Gestire gli stati dell'applicazione(dati)

### Considerazioni sviluppo con Flutter

Quando svilupperete un'app spesso non la svilupperete per tutte le piattaforme, ma è importante scegliere una piattaforma target iniziale su cui sviluppare e magari in seguito adattare l'app per tutte le altre piattaforme. 

In questo caso sceglieremo Windows come **Target Device** e **Development Device**.

Un altro suggerimento è che se state sviluppando un'app per computer Windows allora usate un sistema operativo Windows per farlo. Questo rende alcune cose più facili e veloci.

> Esempio **Development Device** e **Target Device**
> ![enter link description here](https://codelabs.developers.google.com/static/codelabs/flutter-codelab-first/img/e4ee01184acbb3d1_856.png)

> Esempio **Development Device** usato sia per lo sviluppo che come **Target Device**
> ![enter link description here](https://codelabs.developers.google.com/static/codelabs/flutter-codelab-first/img/bf1a99846427bafc_856.png)

# Nuovo progetto

## Creiamo un nuovo progetto

Avvia Visual Studio Code, aprire la command palette (con F1 o Ctrl+Shift+P o Shift+Cmd+P). Digitare "**flutter new**" e selezionare il comando "**Flutter: New Project**"
![desc](https://raw.githubusercontent.com/RayCatcherS/CodelabFlutterUni/main/media/steps/command_pallet.png)
Dopo selezionare "**Application**", seleziona ora una cartella in cui creare un nuovo progetto. Per comodità nella cartella Documenti Creiamo una cartella chiamata Flutter e la selezioniamo.
Infine dai un nome alla tua app come `flutter_app`o `flutter_application_1`.

A questo punto flutter procederà con la creazione del progetto. Ci potrebbero volere alcuni minuti. Appena il progetto sarà creato VS lo aprirà.

> **Nota:** VS Code mostrerà una finestra chiedendo se può considerare attendibile il contenuto della cartella. Selezionare Si. Se premi no verrà disabilitata la possibilità di usare Flutter nella cartella.
> ![desc](https://codelabs.developers.google.com/static/codelabs/flutter-codelab-first/img/e0b422065b6ea4c5_856.png)
> Se non appare la voce **Flutter: New Project** consultare https://code.visualstudio.com/docs/editor/workspace-trust

## Selezioniamo il Target Device

Per selezionare il **target device**, (1) premere nell'angolo in basso a destra di VS Code. (2) Selezionare quindi **Windows - desktop** che dovrebbe comparire tra i device disponibili.
![desc](https://raw.githubusercontent.com/RayCatcherS/CodelabFlutterUni/main/media/steps/set_target_device.png)

## Avviamo l'app(Debug)

Per avviare l'app in modalità Debug assicurarsi che sia aperto il file `lib/main.dart` e premere il pulsante in alto a destra della finestra di VS Code o premere F5
![desc](https://raw.githubusercontent.com/RayCatcherS/CodelabFlutterUni/main/media/steps/run_app.png)
Dopo circa un minuto l'app verrà avviata l'app in modalità debug. Potremo visualizzare quindi la demo Flutter preimpostata mentre viene eseguita nella finestra.
![desc](https://raw.githubusercontent.com/RayCatcherS/CodelabFlutterUni/main/media/steps/flutter_app.png)

# Idea dell'app e codice partenza

Oggi vogliamo creare un'app in cui se si preme un pulsante viene generata una stringa di caratteri formata da due parole del dizionario inglese.  

## Prepariamo i file del progetto

Ora sovrascriveremo il contenuto di 3 file con del codice di partenza per l'app.

## pubspec.yaml

Iniziamo sostituendo il contenuto del file pubspec.yaml con il codice sotto:  
![desc](https://codelabs.developers.google.com/static/codelabs/flutter-codelab-first/img/ac32a9e0158125e3_856.png)

```yaml
name: namer_app
description: A new Flutter project.

publish_to: 'none' # Remove this line if you wish to publish to pub.dev

version: 0.0.1+1

environment:
  sdk: ^3.1.1

dependencies:
  flutter:
    sdk: flutter

  english_words: ^4.0.0
  provider: ^6.0.0

dev_dependencies:
  flutter_test:
    sdk: flutter

  flutter_lints: ^2.0.0

flutter:
  uses-material-design: true
```

Il file `pubspec.yaml` contiene le informazioni di base sulla tua app, come la versione corrente, le dipendenze con le loro versioni in uso e varie cose che non vedremo. Le dipendenze si potranno importare in un progetto semplicemente inserendo il nome e la versione di fianco. 

Una volta sostituito il contenuto salvare.

## analysis_options.yaml

Successivamente, apriamo l'altro file di configurazione nel progetto, `analysis_options.yaml`.
![desc](https://codelabs.developers.google.com/static/codelabs/flutter-codelab-first/img/c0c6edae8ea73b23_856.png)

E sostituiamo il contenuto del file con questo.

```yaml
include: package:flutter_lints/flutter.yaml

linter:
  rules:
    avoid_print: false
    prefer_const_constructors_in_immutables: false
    prefer_const_constructors: false
    prefer_const_literals_to_create_immutables: false
    prefer_final_fields: false
    unnecessary_breaks: true
    use_key_in_widget_constructors: false
```

Quello che abbiamo fatto con questa configurazione è sviluppare con Flutter in modo più rilassato senza che  l'analizzatore statico del codice usi delle regole troppo restrittive. (A differenza dei test dinamici che vengono eseguiti) Sappiamo che gli analizzatori statici nel testing software vengono anche spesso usati per migliorare la qualità del codice, identificare bug e applicare migliori pratiche di programmazione, e che questi agiscono senza che venga eseguito il programma/codice.
Essendo un primo progetto di prova quindi sarà rilassare questo analizzatore. Semmai doveste produrre un software e questo fosse scritto per essere pubblicato in modo vero e proprio allora potete rendere l'analizzatore più rigoroso di come abbiamo fatto.  

Una volta sostituito il contenuto salvare.

Adesso apriamo il file `main.dart` nella cartella `lib`
![desc](https://codelabs.developers.google.com/static/codelabs/flutter-codelab-first/img/47c646911d89fed5_856.png)

E anche qui sostituiamo il contenuto di questo file con il codice seguente e salviamo il file

```dart
import 'package:english_words/english_words.dart';
import 'package:flutter/material.dart';
import 'package:provider/provider.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  @override
  Widget build(BuildContext context) {
    return ChangeNotifierProvider(
      create: (context) => MyAppState(),
      child: MaterialApp(
        title: 'Namer App',
        theme: ThemeData(
          useMaterial3: true,
          colorScheme: ColorScheme.fromSeed(seedColor: Colors.deepOrange),
        ),
        home: MyHomePage(),
      ),
    );
  }
}

// Classe che rappresenta lo stato dell'app(Dati) 
class MyAppState extends ChangeNotifier {
  // questo metodo restituisce la stringa della coppia di parole
  var current = WordPair.random();
}

class MyHomePage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    var appState = context.watch<MyAppState>();

    return Scaffold(
      body: Column(
        children: [
          Text('A random idea:'),
          Text(appState.current.asLowerCase),
        ],
      ),
    );
  }
}
```

Queste 50 righe di codice rappresentano l'intera app di partenza.

# Sviluppiamo l'app

## Primo Hot Reload

Avviamo nuovamente l'applicazione tramite l'icona in alto a destra o premiamo F5 per avviare l'app e aspettiamo qualche secondo prima che si avvi. Per testare questa funzionalità famosa di Flutter, ovvero l'**hot reload** modifichiamo il parametro dell'oggetto Text() in una nuova stringa

```dart
// ...

    return Scaffold(
      body: Column(
        children: [
          Text('A random AWESOME idea:'),  // ← Example change.
          Text(appState.current.asLowerCase),
        ],
      ),
    );

// ...
```

dopo aver modificato la stringa nell'oggetto del primo `Text()` se salverete il file (con `Ctrl+S` o `Cmd+S`) noteremo come l'app cambia immediatamente ma la parola casuale rimane la stessa. Quindi viene iniettata esattamente solo la modifica del widget modificato e gli stati del resto degli altri widget resta invariato. Come notiamo la parola non cambia e questo significa che non viene ricompilato tutto il codice(la parola viene generata nello stato dell'app definito con MyAppState ). Notiamo quindi che questa funzionalità per i programmatori è un'ottimo modo per aumentare di molto il workflow dello sviluppo di un'app.

## Aggiungiamo un Pulsante

Sempre nel main aggiungiamo il bottone nella parte inferiore del Widget Column(il widget che incolonna una lista di Widget).

```dart
// ...

    return Scaffold(
      body: Column(
        children: [
          Text('A random AWESOME idea:'),
          Text(appState.current.asLowerCase),

          // ↓ Aggiungi questo.
          ElevatedButton(
            onPressed: () {
              print('button pressed!');
            },
            child: Text('Next'),
          ),

        ],
      ),
    );

// ...
```

Salvando la modifica, l'app si aggiorna nuovamente: viene visualizzato un pulsante e, quando fai clic su di esso, la _console di debug_ in VS Code mostra un **button pressed!** come stampa di debug.

## Corso accelerato ma capiamo bene

Per quanto questo sia un piccolo corso accelerato di Flutter è importante dare un'occhiata al codice

```dart
// ...

void main() {
  runApp(MyApp());
}

// ...
```

Nella parte superiore del file troveremo la funzione `main()`. Che dice a Flutter solo di eseguire l'app definita in `MyApp` che è un Widget.

```dart
// ...

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  @override
  Widget build(BuildContext context) {
    return ChangeNotifierProvider(
      create: (context) => MyAppState(),
      child: MaterialApp(
        title: 'Namer App',
        theme: ThemeData(
          useMaterial3: true,
          colorScheme: ColorScheme.fromSeed(seedColor: Colors.deepOrange),
        ),
        home: MyHomePage(),
      ),
    );
  }
}

// ...
```

La classe `MyApp`estende `StatelessWidget` che è il modo per caratterizzare una classe in modo che sia visto come un Widget da Flutter. I widget sono gli elementi da cui crei ogni app Flutter. Come puoi vedere, anche _MyApp _ è un widget.

Il codice `MyApp`configura l'intera app ed è abbastanza standard. Qui dentro solitamente viene creato lo stato dell'app (di cui parleremo dopo), gerarchicamente questo è la radice di tutti gli altri Widget(L'app non è altro che un albero di Widget).  In`MyApp` si assegna un nome all'app, si definisce il tema visivo e si imposta il widget "home", come il punto di partenza della tua app. Ad esempio come punto di partenza ci possiamo inserire un Widget Homepage che abbiamo creato.

## Stato app

Lo stato dell'app(business logic) è contenuto in: 

```dart
// Classe che rappresenta lo stato dell'app(Dati) 
class MyAppState extends ChangeNotifier {
  // questo metodo restituisce la stringa della coppia di parole
  var current = WordPair.random(); 
}
```

Noi che siamo programmatori sappiamo che per il bene del software, della sua gestione e manutenzione dovremmo separare la logica di business (business logic) dalla presentazione (layout).

Questa dimostrazione a cui partecipate resterà molto semplice ma sappiate che ci sono molti modi per gestire lo stato di un'app in flutter (solitamente le aziende o i gruppi di sviluppatori ne stabiliscono uno da usare)

Noi useremo`ChangeNotifier` che è uno dei più facili da spiegare

- In questo momento la classe `MyAppState`definisce i dati necessari per il funzionamento dell'app. Al momento contiene solo una singola variabile con l'attuale coppia di parole casuali.
- La classe `MyAppState` estende `ChangeNotifier`, il che significa che può _notificare_ ad altri i propri _cambiamenti_ . Ad esempio, se la coppia di parole corrente cambia, alcuni widget nell'app che noi scegliamo vogliamo che lo sappiano.
- Lo stato viene creato e fornito all'intera app utilizzando un `ChangeNotifierProvider`(vedere il codice sopra in `MyApp`). Ciò consente a qualsiasi widget innestato nell'app di accedere ai dati dello stato dell'app.

![desc](https://codelabs.developers.google.com/static/codelabs/flutter-codelab-first/img/1a5afe9cfec75b3a_856.png)

## Widget Homepage

```dart
// ...

class MyHomePage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {           // ← 1
    var appState = context.watch<MyAppState>();  // ← 2

    return Scaffold(                             // ← 3
      body: Column(                              // ← 4
        children: [
          Text('A random AWESOME idea:'),        // ← 5
          Text(appState.current.asLowerCase),    // ← 6
          ElevatedButton(
            onPressed: () {
              print('button pressed!');
            },
            child: Text('Next'),
          ),
        ],                                       // ← 7
      ),
    );
  }
}

// ...
```

Abbiamo `MyHomePage`che è il widget che abbiamo creato e che abbiamo scelto come punto di partenza della nostra app. Ogni riga numerata sottostante corrisponde a un commento con numero di riga nel codice sopra:

1. Ogni widget definisce un `build()`metodo che viene chiamato automaticamente ogni volta che le circostanze del widget cambiano in modo che il widget sia sempre aggiornato.
2. `MyHomePage` il Widget che stiamo creando vogliamo che osservi le modifiche che vengono effettuate sullo stato utilizzando il metodo `watch()` per farlo teniamo traccia di queste modifiche in questo modo.
3. Ogni widget, in questo caso `MyHomePage` ha un metodo `build` che deve restituire un widget o (più tipicamente) un _albero_ annidato di widget. In questo caso, il widget di livello superiore è `Scaffold`. Non useremo lo `Scaffold`in questo codelab, ma è un widget utile e si trova nella stragrande maggioranza delle app Flutter.
4. `Column`è uno dei widget di layout più basilari in Flutter. Prende un numero qualsiasi di figli e li incolonna in una tutti dall'alto verso il basso. Ovviamente potremo modificare i parametri del widget che spesso sono progettati per modificare la visualizzazione del widget, ad esempio potremmo cambiare il modo in cui la colonna è centrata.
5. `Text` è quello che abbiamo modificato prima.
6. Questo secondo `Text`widget come parametro prende `appState`e accede all'unico membro di quella classe, ovvero `current` che per ora è l'unica variabile dello stato della nostra app in Flutter. Utilizza un getter  `asLowerCase`(il getter è come un metodo che restituisce un tipo di dato) che restituisce la stringa della coppia di parole in minuscolo.
7. Notiamo come il codice Flutter fa un uso molto massiccio di virgole finali. Non è necessario che questa particolare virgola sia qui, perché button è l'ultimo elemento della lista dei figli di `Column`. Tuttavia è generalmente buona norma utilizzare le virgole finali.

## Primo comportamento

Adesso, collegheremo il pulsante allo stato dell'app, facendone cambiare i valori dello stato e ridisegnando i Widget che osservano lo stato dell'app.
Torniamo nella sezione di codice che rappresenta lo stato dell'app ovvero all'interno di `MyAppState` e aggiungiamo questa porzione di codice

```dart
// ...

class MyAppState extends ChangeNotifier {
  var current = WordPair.random();

  // ↓ Add this.
  void getNext() {
    current = WordPair.random();
    notifyListeners();
  }
}

// ...
```

Il nuovo `getNext()`metodo riassegna alla variabile `current`una nuova parola  casuale `WordPair`. 
Una volta assegnata la parola chiama anche `notifyListeners()`(un metodo `ChangeNotifier)`che garantisce che chiunque guardi `MyAppState`venga avvisato. In questo caso chi osserva `MyAppState` è la variabile `var appState = context.watch<MyAppState>();` che verrà avvisata.
Subito dopo verrà ridisegnata l'app a partire dal Widget radice, scendendo fino ai Widget foglia. E in questo caso verranno ridisegnati i Widget con le nuove modifiche osservate nello stato dell'app `MyAppState`.

Tornando al nostro bottone quello che facciamo adesso in questo piccolo pezzo di codice sarà chiamare il metodo `getNext` dal parametro di tipo callback del pulsante .
In Flutter, il parametro `onPressed` nei widget dei bottoni è utilizzato per specificare la funzione o il blocco di codice che deve essere eseguito quando il pulsante viene premuto (cliccato).

```dart
// ...

    ElevatedButton(
      onPressed: () {
        appState.getNext();  // ← This instead of print().
      },
      child: Text('Next'),
    ),

// ...
```

# (Lezione 2)

# Rapido riassunto

rapido riassunto sui widget e sulla gestione dello stato dell'app

# Breve excursus

Breve excursus su aspetti che avremmo dovuto completare nello scorso codelab

#### Stateless widget

Ci sono due tipi di widget(stateless widget e stateful widget) e per ora stiamo usando uno stateless widget. Sono entrambi widget, non cambia nulla. Ne vedremo la differenza dei due più avanti

#### Accedere ai dati degli stati in un widget generico

Non portare dietro per il widget l'intero stato ma estrarre le variabili nel metodo build prima di usarle nel widget.

```dart
// ...

// widget che stiamo implementando
class MyHomePage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {

    // Avere widget separati per parti logiche separate della tua interfaccia
    // utente è un modo importante per gestire la complessità in Flutter.
    MyAppState appState = context.watch<MyAppState>();
    // dichiaro qui sopra l'oggetto che mi serve senza portare dietro per tutto 
    // il widget l'intero appState
    WordPair pair = appState.current; 

// resto del codice ...
```

#### Refactoring

##### Wrap

Per innestare agilmente i widget con il fine di creare il layout che desideriamo, usiamo gli strumenti forniti dall'editor VS Code, il Refactoring(Wrap)

[qui video](https://www.youtube.com/watch?v=zPklkjwUsFc&t)

##### Extract Widget

costruire layout

```dart
// ...
Column(
    children: [
        Container(
            color: Colors.red,
            child: Row(Text("titolo"))
        )
        Container(
            child: Row(
                children: [
                    Container(
                        color: Colors.blue
                        Text("titolo")
                    ),
                    Container(
                        color: Colors.yellow
                        Text("titolo")
                    )
                ]
            )
        )

    ]
) 
// ... 
```

come già visto i layout crescono velocemente in lunghezza o per vari motivi può essere utile "esportare" un albero di widget estraendolo come un widget

[Qui video](https://www.youtube.com/watch?v=9BhqIPMOEIM)

#### Widget Primitivi layout

##### Padding

aggiungere widget padding, cosa fa.

##### Layout, stili e tema

Sappiamo bene anche rispetto al corso che state seguendo che la consistenza di stili e colori all'interno dell'app è importante

- **Personalizzare stile usando il tema**: Ad esempio nell'utilizzo nel widget BigCard, usiamo come colore il valore usato dal tema corrente nell'app.

- **Modifiche tema**: Puoi modificare questo colore e altro del tema dell'intera app scorrendo verso l'alto `MyApp`e modificando il colore per `ColorScheme`.

```dart
MaterialApp(
    title: 'Namer App',
    theme: ThemeData(
        useMaterial3: true,
        colorScheme: ColorScheme.fromSeed(seedColor: Colors.deepOrange),
    ),
    home: MyHomePage(),
),
```

- **Personalizzare stile testo**: Anche rispetto al corso che state facendo, sappiamo che il testo deve essere sempre leggibile e che deve avere determinate caratteristiche in base al contesto. 
  Estraiamo anche qui le informazioni dal tema e le usiamo per personalizzare il testo(potreste creare un oggetto textStyle ad hoc ma in questo caso seguiamo le best practices)
  
  ```dart
  // ... 
      @override
      Widget build(BuildContext context) {
       final theme = Theme.of(context); 
      final TextStyle textStyle = theme.textTheme.displayMedium!.copyWith(
          color: theme.colorScheme.onPrimary,
      ); 
  // ...
  // ... 
  child: Text(pair.asLowerCase, style: textStyle), 
  // ...
  ```
  
  - Utilizzando `theme.textTheme,`accedi al tema dei caratteri dell'app. Questa classe include membri come `bodyMedium`(per testo standard di medie dimensioni), `caption`(per didascalie di immagini) o `headlineLarge`(per titoli di grandi dimensioni).
  
  - La proprietà del tema `displayMedium`potrebbe teoricamente essere `null`. Dart, il linguaggio di programmazione in cui stai scrivendo questa app, è null-safe, quindi non ti consentirà di chiamare metodi di oggetti potenzialmente `null`. In questo caso, però, puoi utilizzare l' `!`operatore ("operatore bang") per assicurarti che Dart sappia cosa stai facendo. (`displayMedium` non è nullo in questo caso)
  
  - La chiamata `copyWith()`a `displayMedium`restituisce una *copia* dello stile di testo *con* le modifiche definite. In questo caso, stai solo cambiando il colore del testo.
  
  - `onPrimary` è il colore usato dal tema per rendere un elemento leggibile se il widget si trova su un colore ad esempio Per ottenere il nuovo colore, accedi al widget tema dell'app nel main(widget root `ThemeData`). Modifica la proprietà `onPrimary`.
  
  - Per ottenere l'elenco completo delle proprietà che puoi modificare, posiziona il cursore in un punto qualsiasi all'interno `copyWith()`delle parentesi e premi `Ctrl+Shift+Space`(Win/Linux)  o `Cmd+Shift+Space`(Mac), per ottenere suggerimenti sull'auto-completamento e su altri parametri modificabili

- **Centrare l'interfaccia**: Nel widget `MyHomePage` per centrare gli elementi figli di un `Column` usare all'interno di Column `mainAxisAlignment: MainAxisAlignment.center` in questo modo:
  
  ```dart
  // ...
  
  Column(
      mainAxisAlignment: MainAxisAlignment.center,
      children: [
  
  // ...
  ```
  
  Per centrare invece l'intero Widget `Column` rispetto alla pagina usare

- **Widget Inspector** possiamo utilizzare questo potente strumento per visualizzare il layout creato nella nostra applicazione e modificarne gli effetti visualizzandone il risultato in tempo reale sulla schermata di debug. 
  Per attivare il Widget Inspector, avviare l'emulazione o l'esecuzione dell'app(F5 o da icona per avviare il debug). Clicca poi sull'iconcina della lente di ingradimento.
  
  [Video qui](https://www.youtube.com/watch?v=v0KWdBaoark)
  
  - Per visualizzare come i widget si adattano al layout cliccare sulla voce "Toggle select widget mode". Ora potremo selezionare i Widget nella **debug session** o nel **widget inspector** per visualizzare come questi si adattano al layout.
    
    - notare come nella visualizzazione del widget inspector abbiamo le informazioni sulle dimensioni del widget:
      
      - w = lunghezza widget, questo è compreso tra 0 <= w <= e una certa lunghezza del widget padre
  
  - Sempre nel widget `MyHomepage`, Wrappiamo ora il widget `Column` con `Center` cliccando con il tasto destro sul widget `Center`,
    clicca su "Refactor" --> "Wrap with Center" per centro

## Aggiungere funzionalità(Business logic)

Vogliamo salvare la parola generata usando un pulsante(button) "Mi piace".
Quindi torniamo nella classe che rappresenta lo stato dell'app `MyAppState` e aggiungiamo questo codice

```dart
// ...

class MyAppState extends ChangeNotifier {
  var current = WordPair.random();

  void getNext() {
    current = WordPair.random();
    notifyListeners();
  }

  // ↓ Add the code below.
  List<WordPair> favorites = <WordPair>[];

  void toggleFavorite() {
    if (favorites.contains(current)) {
      favorites.remove(current);
    } else {
      favorites.add(current);
    }
    notifyListeners();
  }
}

// ...
```

Quindi aggiungiamo la sita di parole che conterrà quelle preferite(su cui premiamo like). Abbiamo anche inserito il metodo `toggleFavorite` che aggiunge una parola in lista se non è presente, altrimenti la elimina.

## Colleghiamo l'interfaccia alla nuova funzionalità

Torniamo in `MyHomePage` e aggiungiamo un bottone per attivare la nuova funzionalità. Aggiungiamo il bottone sulla stessa riga usando `Row` in questo modo:

- Usiamo il Refactor per innestare il widget Row.

- Settiamo l'ampiezza della Row in base alla grandezza dei figli con `mainAxisSize: MainAxisSize.min`

- Inseriamo un nuovo `ElevatedButton.icon` questo bottone predefinito di flutter richiede che tra i parametri sia passata un'icona(`IconData`) che come già sappiamo è anch'essa un widget

- Creiamo un po' di spazio tra i due bottoni con il Widget `SizedBox(width: 10)` inserendolo tra i due bottoni (figli di Row)

- nel parametro `onPressed:` del nuovo bottone inseriamo il metodo `appState.toggleFavorite();` che abbiamo creato precedentemente nello state dell'app.

- Creiamo una variabile `IconData icon` e assegnamo un'icona differente in base al fatto che la parola generata sia all'interno o meno della lista, controllando appunto con una condizione se `if(appState.favorites.contains(pair))`. 
  Se la parola è contenuta istanziamo un Widget Icona con simbolo di un cuore pieno, altrimenti istanziamo un Widget Icona con simbolo di un cuore vuoto.

```dart
class MyHomePage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {

    // Avere widget separati per parti logiche separate della tua interfaccia
    // utente è un modo importante per gestire la complessità in Flutter.
    MyAppState appState = context.watch<MyAppState>();
    // dichiaro qui sopra l'oggetto che mi serve senza portare dietro per tutto 
    // il widget l'intero appState
    WordPair pair = appState.current; 


    IconData icon;
    if (appState.favorites.contains(pair)) {
      icon = Icons.favorite;
    } else {
      icon = Icons.favorite_border;
    }

    return Scaffold(
      body: Center(
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: [
            BigCard(pair: pair),
            SizedBox(height: 10),
            Row(
              mainAxisSize: MainAxisSize.min,
              children: [
                ElevatedButton.icon(
                  onPressed: () {
                    appState.toggleFavorite();
                  },
                  icon: Icon(icon),
                  label: Text('Like'),
                ),
                SizedBox(width: 10),
                ElevatedButton(
                  onPressed: () {
                    appState.getNext();
                  },
                  child: Text('Next'),
                ),
              ],
            ),
          ],
        ),
      ),
    );
  }
}
```

Quindi a questo punto possiamo aggiungere le nostre parole preferite all'interno di una lista.

## NavigationBar

Sappiamo che un'app non può contenere tutto in un unica schermata. Quindi abbiamo bisogno di un widget che ci permetta di visualizzare e navigare all'interno dell'app. Uno dei modi possibili può essere utilizzare il widget **`Navigationbar()`**. 

Quindi creaiamo un widget che andrà a gestire la navigazione tra le pagine principali della nostra app e lo chiamiamo `Navigation`. Questo sarà uno `StatefulWidget`.

Man mano che l'app diventa più grande e bisogna tenere traccia degli stati dei singoli widget, non sarà una buona pratica tenere traccia degli stati di tutti i widget in un unico app state in questo caso `MyAppState`, questo perchè non è necessario che gli altri widget possano accedere agli stati degli altri widget. 
Ad esempio agli altri widget non interessa sapere l'index  della pagina visualizzata usato nella Navigationbar. Quindi gli stati di alcuni widget non sono utili ad altri widget.

#### Utilizzo Stateful widget

- Gli `StatefulWidget` sono widget che contengono il loro stato all'interno dello stesso widget(ad esempio l'index della pagina da visualizzare) e sono in grado di cambiare uno stato di se stessi per poi ricostruirsi(chiamata al metodo build) sulla base del loro stato.

- Quindi gli `StatefulWidget` contengono uno stato che è solo loro, non viene condiviso con nessun altro. Loro gestiscono il loro stato, e quando il loro stato cambia, si ricostruiscono(chiamata al metodo build). 

- Nel nostro caso lo `StatefulWidget` `Navigation` che abbiamo creato, contiene lo stato della sua navigation bar(l'index), e ogni volta che l'index della **`Navigationbar()`** cambierà, allora ricostruirà la sua visualizzazione.

- Nel caso del nostro `Navigation` widget, il suo stato `currentPageIndex`, quando verrà cambiato con l'evento `onDestinationSelected` andrà a chiamare la ricostruzione del widget `Navigation` in questo modo:

```dart
//...

onDestinationSelected: (int index) {

    // in setState va cambiato lo stato del widget(currentPageIndex)
    // setState andrà a ridisegnare l'intero widget
    setState(() {
        currentPageIndex = index;
    });
},

//...
```

#### Organizzazione del codice

Quando il progetto cresce è necesario organizzare il codice. Ho organizzato il codice per voi, ho utilizzato questa fonte: [code organization](https://medium.com/@patthipati/code-organization-with-provider-state-management-for-flutter-ae2a77b63718), per chi ha voglia di approfondire come organizzare un progetto in Flutter.

#### Rimozione delle favorite word

Ho inserito il tasto Remove in ogni elemento della lista preferiti `FavoriteTile` chiedendo di rimuovere dallo stato dell'app la parola da rimuovere, vedere `appState.removeFavorite(pair);`. Possiamo aggiungere e rimuovere parole. I widget in ascolto sullo stato `MyAppState` si ricostruirando con coerenza per tutta l'app in modo coerente e consistente. 

Esempio in javascript-html, svantaggio del dover elencare tutti i componenti html che devono visualizzare un determinato dato.  

## Fine codelab

Questo sarà il progetto di partenza per il prossimo codelab in cui implementeremo l'autenticazione tramite servizi cloud Firebase. Utilizzeremo il database del servizio Firebase per memorizzare delle strutture dati sul database e useremo dei metodi per ottenere i dati dal database.
Il codice di partenza e il secondo codelab a questo [link](https://github.com/RayCatcherS/Codelab2FlutterCasoStudioIUMUni) 
