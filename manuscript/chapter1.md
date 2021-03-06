# Hyrje n&euml; React

Ky kapitull &euml;sht&euml; nj&euml; hyrje n&euml; React, nj&euml; librari e JavaScript p&euml;r renderimin e nd&euml;rfaqeve n&euml; nj&euml; faqe t&euml; vetme dhe aplikacioneve mobile, ku shpjegohet pse zhvilluesit duhet t&euml; marrin parasysh shtimin e libraris&euml; React si mjet t&euml; tyrin. Ne do t&euml; zhytemi n&euml; ekosistemin React, duke krijuar aplikacionin tuaj t&euml; par&euml; React nga zeroja pa konfigurim. S&euml; bashku, ne do t&euml; prezantojm&euml;  **JSX** , sintaks&euml;n p&euml;r React dhe  **ReactDOM** , k&euml;shtu q&euml; ju do t&euml; keni nj&euml; kuptim t&euml; p&euml;rdorimeve praktike t&euml; React n&euml; aplikimet moderne t&euml; internetit .

## P&euml;rsh&euml;ndetje, emri im &euml;sht&euml; React.

Aplikacionet për një faqe të vetme  ([SPA](https://en.wikipedia.org/wiki/Single-page_application)) janë bërë gjithnjë e më popullore në vitet e fundit, pasi framework si Angular, Ember dhe Backbone lejojnë zhvilluesit JavaScript për të ndërtuar aplikacione moderne të uebit duke përdorur teknika përtej JavaScript dhe jQuery. Të treja të lartpërmendurat janë ndër SPA-të e para, secila prej tyre vjen në vetvete ndërmjet 2010 dhe 2011, por ka shumë e më shumë opsione për zhvillimin e faqeve në një të vetme. Gjenerata e parë e SPA framework arriti në nivelin enterprise, prandaj framework i tyre është më i ngurtë. React, nga ana tjetër, mbetet një librari inovative që është adoptuar nga shumë liderë teknologjikë si [Airbnb, Netflix, dhe Facebook](https://github.com/facebook/react/wiki/Sites-Using-React).

React u publikua nga ekipi i zhvillimit të rrjetit të Facebook në 2013 si një librari pamore, e cila e bën atë 'V' në  [MVC](https://en.wikipedia.org/wiki/Model–view–controller) (model view controller).  Si pamje, ajo ju lejon të renditni përbërësit si elementë të dukshëm në një browser, ndërsa ekosistemi i tij na lejon të ndërtojmë aplikacione me faqe të vetme. Ndërsa gjenerata e parë e framework-ut u përpoq për të zgjidhur shumë gjëra në të njëjtën kohë, React përdoret vetëm për të ndërtuar shtresën tuaj pamore; në mënyrë specifike, ajo është një librari ku pamja është një hierarki e komponentëve përbërës. Nëse nuk keni dëgjuar për MVC më parë, mos u mërzitni për këtë, sepse është vetëm aty për ta vënë React historikisht në kontekst për njerëzit që vijnë nga gjuhët e tjera programuese.

Në React, fokusi mbetet në shtresën pamore derisa më shumë aspekte të futen në aplikacion. Këto janë blloqet ndërtuese për një SPA, të cilat janë thelbësore për të ndërtuar një aplikim të maturuar. Ata vijnë me dy përparësi:

* Ju mund të mësoni blloqet e ndërtimit një nga një, pa pasur nevojë t'i kuptoni ato krejtësisht. Në të kundërt, një framework SPA ju jep çdo bllok ndërtimi që nga fillimi. Ky libër përqëndrohet në React si bllokun e parë të ndërtimit. Në fund do të ndjekim më shumë blloqe ndërtimi.

* Të gjitha blloqet e ndërtimit janë të këmbyeshme, gjë që e bën ekosistemin rreth React shumë inovativ. Zgjidhje të shumëfishta mund të konkurrojnë me njëri-tjetrin dhe ju mund të zgjidhni zgjidhjen më tërheqëse për çdo sfidë të dhënë.

React është një nga zgjedhjet më të mira për ndërtimin e aplikacioneve të internetit moderne. Përsëri, ajo jep vetëm shtresën pamore, por ekosistemi përreth përbën një framework krejtësisht fleksibël dhe të këmbyeshëm. React ka një API të hollë, një ekosistem të fuqishëm dhe evolues, dhe një komunitet të mrekullueshëm.

### Ushtrime

Nëse dëshironi të dini më shumë për arsyen pse zgjodha React ose për të gjetur një vështrim më të thellë në temat e përmendura më lart, këto artikuj japin një perspektivë më të thellë:

* [Pse u zhvendosa nga Angular në React](https://www.robinwieruch.de/reasons-why-i-moved-from-angular-to-react/)
* [Ekosistemi fleksibel React](https://www.robinwieruch.de/essential-react-libraries-framework/)
* [Si të mësoni një framework](https://www.robinwieruch.de/how-to-learn-framework/)

## Kërkesat

Për të ndjekur këtë libër, duhet të njiheni me bazat e zhvillimit të uebit, dmth. si të përdorni HTML, CSS dhe JavaScript. Gjithashtu ka sens të kuptojmë se si funksionojnë [APIs] (https://www.robinwieruch.de/what-is-an-api-javascript/), pasi ato do të mbulohen tërësisht. Gjithashtu, ju inkurajoj që të bashkoheni në grupin zyrtar [Slack Group] (https://slack-the-road-to-learn-react.wieruch.com/) të jeni pjesë e një komuniteti në rritje React ku mund të mësoni nga dhe të ndihmoni të tjeret.

### Editor dhe Terminal

Për mësimet, do t'ju duhet një editor teksti ose IDE dhe terminali (command line tool). Unë kam dhënë [një udhëzues setup] (https://www.robinwieruch.de/developer-setup/) nëse keni nevojë për ndihmë shtesë. Opsionale, ne ju rekomandojmë që të mbani projektet tuaja në GitHub gjatë kryerjes së ushtrimeve në këtë libër. Ekziston një [udhëzues i shkurtër] (https://www.robinwieruch.de/git-essential-commands/) për mënyrën e përdorimit të këtyre mjeteve. Github ka kontroll të shkëlqyeshëm të versionit, kështu që mund të shihni se çfarë ndryshimesh janë bërë në qoftë se bëni një gabim ose thjesht dëshironi një mënyrë më të drejtpërdrejtë për të ndjekur së bashku.

### Node dhe NPM

Së fundi, do t'ju duhet një instalim i [node dhe npm] (https://nodejs.org/en/). Të dyja janë përdorur për të menaxhuar libraritë që do t'ju duhen përgjatë rrugës. Në këtë libër, ju do të instaloni paketa të node të jashtme nëpërmjet npm (menaxher i paketave të nodeve). Këto paketa nodesh mund të jenë librari ose framework të tëra.

Ju mund të verifikoni versionet tuaja të nodes dhe npm në rreshtin e komandave. Nëse nuk merrni ndonjë dalje në terminal, ju duhet të instaloni node dhe npm fillimisht. Këto janë versionet e mia në kohën e shkrimit të këtij libri:

{title="Command Line",lang="text"}
~~~~~~~~
node --version
*v10.11.0
npm --version
*v6.4.1
~~~~~~~~

Përmbajtja shtesë e këtij seksioni është një kurs i node dhe npm. Nuk është gjithëpërfshirës, por do të mbulojë të gjitha mjetet e nevojshme. Nëse jeni të njohur me të dy, ju mund të kaloni këtë seksion.

Menaxheri **i paketave të nodeve**(npm) instalon paketa të nodeve të jashtme nga command line. Këto paketa mund të jenë një sërë funksionesh të shërbimeve, librarive ose framework të tëra, dhe ato janë varësitë e aplikacionit tuaj. Ju mund të instaloni këto paketa në dosjen tuaj të paketës së paketave të nodeve ose në dosjen tuaj lokale të projektit.

Paketat e nodeve globale janë të arritshme nga kudo në terminal dhe vetëm një herë duhet të instalohen në direktorinë globale. Instaloni një paketë globale duke shtypur në vijim një terminal:

{title="Command Line",lang="text"}
~~~~~~~~
npm install -g <package>
~~~~~~~~

Flamuri `-g` tregon npm për të instaluar paketën globalisht. Paketat lokale përdoren në aplikacionin tuaj me parazgjedhje. Për qëllimet tona, ne do të instalojmë React në terminalin e drejtorisë lokale duke shtypur:

{title="Command Line",lang="text"}
~~~~~~~~
npm install react
~~~~~~~~

Paketa e instaluar do të shfaqet automatikisht në një dosje të quajtur * node_modules / * dhe do të renditet në skedarin * package.json * pranë varësive tuaja të tjera.

Për të inicializuar skedarin * node_modules / * dhe * package.json * për projektin tuaj, përdorni komandën e mëposhtme npm. Pastaj, ju mund të instaloni paketa të reja lokale nëpërmjet npm:

{title="Command Line",lang="text"}
~~~~~~~~
npm init -y
~~~~~~~~

Flamuri `-y` inicializon të gjitha parazgjedhjet në * package.json * tuaj. Pas fillimit të projektit tuaj npm, ju jeni gati për të instaluar paketa të reja nëpërmjet `npm install <package>`.

Paketa *package.json* ju lejon të ndani projektin tuaj me zhvilluesit e tjerë pa ndarë të gjitha paketat e nodeve. Do të përmbajë referenca për të gjitha paketat e nodeve të përdorura në projektin tuaj, të quajtura **dependencies**.Përdoruesit e tjerë mund të kopjojnë një projekt pa varësi duke përdorur referencat në * package.json *, ku referencat e bëjnë të lehtë instalimin e të gjitha paketave duke përdorur `npm install`.Skripti `npm install` do të marrë të gjitha varësitë e renditura në skedarin * package.json * dhe instaloni ato në dosjen * node_modules / *. 

Së fundi, ka një komandë tjetër për të mbuluar rreth npm:

{title="Command Line",lang="text"}
~~~~~~~~
npm install --save-dev <package>
~~~~~~~~

Flamuri `--Save-dev` tregon se paketa e nodeve përdoret vetëm në mjedisin e zhvillimit, që do të thotë se nuk do të përdoret kur aplikacioni të vendoset në një server ose të përdoret në production. Është e dobishme për testimin e një aplikacioni duke përdorur një paketë nodesh, por dëshironi ta përjashtoni atë nga mjedisi juaj i production.

Disa prej jush mund të duan të përdorin menaxherët e tjerë të paketave për të punuar me paketat e nodeve në aplikacionet tuaja. **Yarn** është një menaxher i varësisë që punon i ngjashëm me **npm**.  Ajo ka listën e vet të komandave, por ju ende keni akses në të njëjtin regjistër npm. Yarn u krijua për të zgjidhur çështjet që npm nuk mundet, por të dy mjetet kanë evoluar deri në atë pikë ku mjaftojnë sot.

### Ushtrime:

* Krijoni një projekt npm duke përdorur terminalin:
  * Krijo një folder të ri me `mkdir <folder_name>`
  * Shko në folder me `cd <folder_name>`
  * Exekuto `npm init -y` ose `npm init`
  * Instaloni një paketë lokale si React me `npm install react`
  * Kontrolloni file *package.json* dhe folder *node_modules/*
  * Përpiqu për të çinstaluar dhe instaluar paketën * react * node
* Lexoni rreth [npm](https://docs.npmjs.com/)
* Lexoni rreth menaxherit të paketave [yarn](https://yarnpkg.com/en/docs/) 

## Instalimi

Ka shumë rruge për ndërtimin e një aplikacioni React. E para që do të shqyrtojmë është një CDN, i shkurtër për [content delivery network](https://en.wikipedia.org/wiki/Content_delivery_network). Mos u shqetësoni shumë për CDN-të tani, sepse ju nuk do t'i përdorni ato në këtë libër, por ka kuptim t'i shpjegojmë shkurtimisht. Shumë kompani përdorin CDN-të për të depozituar filet publike për konsumatorët e tyre. Disa nga këto skedarë janë librari si React, pasi libraria lidhëse React është vetëm një skedar *react.js* JavaScript.

Për të filluar me React duke përdorur një CDN, gjeni tagun`<script>` në faqen tuaj HTML që tregon për një url CDN. Do t'ju duhen dy librari: * react * dhe * react-dom *.

{title="Code Playground",lang="javascript"}
~~~~~~~~
<script
  crossorigin
  src="https://unpkg.com/react@16/umd/react.development.js"
></script>

<script
  crossorigin
  src="https://unpkg.com/react-dom@16/umd/react-dom.development.js"
></script>
~~~~~~~~

Ju gjithashtu mund të merrni React në aplikimin tuaj duke inicializuar atë si node projekt. Me një skedar * package.json *, mund të instaloni * react * dhe * react-dom * nga vija e komandës. Megjithatë, folder duhet të fillohet si një projekt npm duke përdorur `npm init -y` me një skedar * package.json *. Ju mund të instaloni paketa të shumta node me npm:

{title="Command Line",lang="text"}
~~~~~~~~
npm install react react-dom
~~~~~~~~

Kjo rrugë shpesh përdoret për të shtuar React në një aplikacion ekzistues të menaxhuar me npm.

Ju gjithashtu mund të merreni me Babel për ta bërë aplikimin tuaj të vetëdijshëm për JSX (sintaksën React) dhe JavaScript ES6. Babel përkthen kodin tuaj - konverton atë në JavaScript - kështu që shfletuesit më moderne mund të interpretojnë JavaScript ES6 dhe JSX. Për shkak të këtij setupi të vështirë, Facebook prezantoi create-react-app si një zgjidhje zero-konfigurimi React. Seksioni i ardhshëm do t'ju tregojë se si ta konfiguroni aplikacionin tuaj duke përdorur këtë mjet bootstrap.

### Ushtrime:

* Lexoni rreth [React installations](https://reactjs.org/docs/getting-started.html)

## Setup me Zero-Configurim

Në Rrugën për të mësuar React, do të përdorim [create-react-app] (https://github.com/facebookincubator/create-react-app) për të nisur aplikimin tuaj. Është një kompozim i përshtatshëm i konfigurimit për React të prezantuar nga Facebook në 2016, [rekomandohet për fillestarët nga 96% e përdoruesve të React] (https://twitter.com/dan_abramov/status/806985854099062785). Në * create-react-app * përpunimi dhe konfigurimi evoluojnë në sfond, ndërsa fokusi është në zbatimin e aplikacionit.

Për të filluar, instaloni paketën në paketat tuaj të nodeve globale, në dispozicion në rreshtin e komandave për të nisur aplikacionet e reja React:

{title="Command Line",lang="text"}
~~~~~~~~
npm install -g create-react-app
~~~~~~~~

Ju mund të kontrolloni versionin e * create-react-app * për të verifikuar një instalim të suksesshëm në rreshtin tuaj të komandës:

{title="Command Line",lang="text"}
~~~~~~~~
create-react-app --version
*v2.0.2
~~~~~~~~

Tani ju jeni gati për të nisur aplikimin tuaj të parë React. Shembulli do të quhet * hackernews * , por ju mund të zgjidhni ndonjë emër që ju pëlqen. Së pari, shkojmë në folder :

{title="Command Line",lang="text"}
~~~~~~~~
create-react-app hackernews
cd hackernews
~~~~~~~~

Tani mund ta hapni aplikacionin në editorin tuaj. Struktura e mëposhtme e folderave * create-react-app * ,duhet të paraqitet tek ju:

{title="Folder Structure",lang="text"}
~~~~~~~~
hackernews/
  README.md
  node_modules/
  package.json
  .gitignore
  public/
    favicon.ico
    index.html
    manifest.json
  src/
    App.css
    App.js
    App.test.js
    index.css
    index.js
    logo.svg
    serviceWorker.js
~~~~~~~~

Ky është një ndarje e folderave dhe fileve:

* **README.md:** README.md: Prapashtesa .md tregon se skedari është një skedar markdown. Markdown është përdorur si një gjuhë markup me sintaksë të thjeshtë . Shumë projekte të kodit burimor vijnë me një skedar *README.md* për t'ju dhënë udhëzime fillestare rreth projektit. Kur kaloni projektin tuaj në një platformë të tillë si GitHub, skedari *README.md* zakonisht shfaq informacion rreth përmbajtjes së përmbajtjes në respository. Për shkak se keni përdorur *create-react-app*, *README.md* juaj duhet të jetë i njëjtë me [create-react-app GitHub repository](https://github.com/facebookincubator/create-react-app).

* **node_modules/:** Ky folder përmban të gjitha paketat e nodeve që janë instaluar përmes npm. Pasi keni përdorur * create-react-app * , duhet të jenë instaluar tashmë disa node module për ju. Ju rrallë do të prekni këtë folder, sepse paketat e nodeve përgjithësisht janë instaluar dhe çinstaluar me npm nga rreshti i komandës.

* **package.json:** Ky file ju tregon një listë të varësive të nodeve dhe konfigurimeve të tjera të projektit.

* **.gitignore:** Ky file shfaq të gjithë filet dhe folderat që nuk duhet të shtohen në repositorin tuaj git kur përdorni git; filet dhe folder të tillë duhet të gjenden vetëm në projektin tuaj lokal. Folderi * node_modules / * është një shembull. Mjafton të ndash file * package.json * me të tjerët, kështu që ata mund të instalojnë varësi në fundin e tyre me `npm install` pa folderin tuaj të varësisë.

* **public/:** Ky folder përmban file zhvillimi, të tillë si  *public/index.html*. Indeksi shfaqet në localhost: 3000 kur zhvilloni aplikacionin tuaj. Boilerplate kujdeset për të lidhur këtë indeks me të gjitha skriptet në *src/*.

* **build/** Ky folder krijohet kur ndërthurni projektin në production, pasi mban të gjithë production files. Kur ndërtoni projektin tuaj në production, të gjithë kodin në folderat  * src / * dhe * public / * bllokohet dhe vendoset në  folderin build.

* **manifest.json** dhe **serviceWorker.js:** Këto file nuk do të përdoren për këtë projekt, prandaj ju mund t'i injoroni ato për momentin.

Në fillim, gjithçka që ju nevojitet ndodhet në folderin  * src / *. Fokusi kryesor qëndron në file* src / App.js * i cili përdoret për të implementuar komponentët React. Do të përdoret për të implementuar aplikacionin tuaj, por më vonë ju mund të dëshironi të ndani komponentet tuaja në file të shumtë, ku secili file ruan një ose më shumë komponente më vete.

Përveç kësaj, do të gjeni një file * src / App.test.js * për testimet tuaja dhe një * src / index.js * si një pikë hyrje në botën React. Ju do të njihni të dy filet në mënyrë të imtësishme në një kapitull të mëvonshëm. Ekziston edhe një file * src / index.css * dhe një * src / App.css * për të dizenjuar aplikacionin tuaj të përgjithshëm dhe komponentët, e cila vjen me stilin default kur i hapni ato. Ju mund t'i modifikoni ato edhe më vonë.

Aplikimi * create-react-app * është një projekt npm që mund të përdorni për të instaluar dhe çinstaluar paketat e nodeve. Ajo vjen me skriptet e mëposhtme npm komand line:

{title="Command Line",lang="text"}
~~~~~~~~
# Ekzekuton aplikacionin në http://localhost:3000
npm start

# Ekzekuton testin
npm test

# Ndërton aplikacionin për production
npm run build
~~~~~~~~

Scriptet janë të përcaktuara në * package.json * tuaj, dhe aplikimi juaj bazë Reacteshte  bootstraped. Ushtrimet e mëposhtme më në fund do t'ju lejojnë të përdorni aplikacionin tuaj bootstrapped në browser.

### Ushtrime:

* `npm start` dhe vizitoni aplikacionin në browserin tuaj (Duke shtypur Control + C dil nga komand line)
* Ekzekuto kodin `npm test` 
* Ekzekuto kodin `npm run build`  dhe verifikoni që folderi   * build/ * u shtua në projektin tuaj (mund ta hiqni atë më pas.) Kini parasysh se folderi build  mund të përdoret më vonë në[deploy your application](https://www.robinwieruch.de/deploy-applications-digital-ocean/))
* Njihuni me strukturën e folderave
* Kontrolloni përmbajtjen e fileve
* Lexoni rreth [npm scripts and create-react-app](https://github.com/facebookincubator/create-react-app)

## Hyrje në JSX

Tani do të njohim JSX, sintaksën në React. Siç u përmend më parë, * create-react-app * ka nisur tashmë një aplikacion bazë për ju, dhe të gjitha filet vijnë me implementimet e tyre të paracaktuara. Tani për tani, file i vetëm që do të modifikojmë është *src/App.js* file.

{title="src/App.js",lang="javascript"}
~~~~~~~~
import React, { Component } from 'react';
import logo from './logo.svg';
import './App.css';

class App extends Component {
  render() {
    return (
      <div className="App">
        <header className="App-header">
          <img src={logo} className="App-logo" alt="logo" />
          <p>
            Edit <code>src/App.js</code> and save to reload.
          </p>
          <a
            className="App-link"
            href="https://reactjs.org"
            target="_blank"
            rel="noopener noreferrer"
          >
            Learn React
          </a>
        </header>
      </div>
    );
  }
}

export default App;
~~~~~~~~

Mos u shqetësoni nëse jeni të hutuar nga deklaratat e import / eksportit dhe deklarimit të klasës tani. Këto janë karakteristika të JavaScript ES6 ne do ti rishikojmë në një kapitull të mëvonshëm.

Në file duhet të shihni një ** React ES6 class component ** me emrin App. Ky është një deklarim komponenti. Pasi të keni deklaruar një komponent, mund ta përdorni si element kudo në aplikacionin tuaj. Ai do të prodhojë një ** instance** të ** komponentit tuaj ** ose, me fjalë të tjera, komponenti do të instanohet.


{title="Code Playground",lang="javascript"}
~~~~~~~~
// component declaration
class App extends Component {
  ...
}

// perdorimi i komponentit 
// krijon nje instance te komponentit
<App />
~~~~~~~~

**element** i kthyer është specifik për metodën `render()`.Është e rëndësishme të kuptojmë dallimet midis një komponenti, një instance të një komponenti dhe një elementi.

Duhet të shihni se ku komponenti i App instantohet, përndryshe nuk mund ta shihni produktin e dhënë në browser. Komponenti i App është vetëm deklarata, por jo përdorimi. Ju mund të instantoni komponentin kudo në JSX tuaj me `<App />`. Ju do të shihni më vonë kur kjo ndodh në këtë aplikacion.

Përmbajtja në bllokun e paraqitjes mund të duket ngjashëm me HTML, por në të vërtetë është JSX. JSX ju lejon të përzieni HTML dhe JavaScript. Është e fuqishme, por mund të jetë konfuze kur jeni mësuar ti ndani e dy gjuhët. Është një ide e mirë për të filluar duke përdorur HTML bazë në JSX tuaj. Hapni skedarin `App.js` dhe hiqni të gjithë kodin HTML të panevojshëm siç tregohet:

{title="src/App.js",lang="javascript"}
~~~~~~~~
import React, { Component } from 'react';
import './App.css';

class App extends Component {
  render() {
    return (
      <div className="App">
        <h2>Welcome to the Road to learn React</h2>
      </div>
    );
  }
}

export default App;
~~~~~~~~
Tani, vetëm ktheni HTML në metodën tuaj  `render () `  pa ndonjë JavaScript. Le të përkufizojmë "Welcome to the Road to learn Reac" si një variabel. Një variabel është vendosur në JSX nga kllapat gjarpërushe.


{title="src/App.js",lang="javascript"}
~~~~~~~~
import React, { Component } from 'react';
import './App.css';

class App extends Component {
  render() {
# leanpub-start-insert
    var helloWorld = 'Welcome to the Road to learn React';
# leanpub-end-insert
    return (
      <div className="App">
# leanpub-start-insert
        <h2>{helloWorld}</h2>
# leanpub-end-insert
      </div>
    );
  }
}

export default App;
~~~~~~~~

Nisni aplikacionin tuaj në command line me `npm start` për të verifikuar ndryshimet që keni bërë.

Ju mund të keni vënë re atributin `className`. Ai pasqyron atributin standard në HTML 'class' . JSX ka zëvendësuar një pjesë të vogël të atributeve të brendshme HTML, por mund të gjeni të gjitha [atributet HTML të mbështetura në dokumentacionin e React] (https://reactjs.org/docs/dom-elements.html#all-supported-html-attributes), të cilat të gjitha ndjekin konventën camelCase. Në rrugën tuaj për të mësuar React, prisni të shkoni në më shumë atribute të veçanta JSX.

### Ushtrime:

* Përcaktoni më shumë variabla dhe i bëni ato në JSX
  * Përdorni një objekt kompleks për të përfaqësuar një përdorues me një emër dhe mbiemër
  * Pasqyroni detajet e perdoruesit në JSX
* Lexoni rreth [JSX](https://reactjs.org/docs/introducing-jsx.html)
* Lexoni rreth [React components, elements and instances](https://reactjs.org/blog/2015/12/18/react-components-elements-and-instances.html)

## ES6 të kundërtat dhe pro-të

Vini re se ne e kemi deklaruar variablen `helloWorld` me një deklaratë ` var`. JavaScript ES6 vjen me dy mënyra të tjera për të deklaruar variablat: `const` dhe` let`. Në JavaScript ES6, rrallë do të gjeni më `var` . Një variabel e deklaruar me `const` nuk mund të ricaktohet ose ribotohet dhe nuk mund të ndryshohet ose modifikohet. Pasi të jetë caktuar variabli, nuk mund ta ndryshoni atë:

{title="Code Playground",lang="javascript"}
~~~~~~~~
// not allowed
const helloWorld = 'Welcome to the Road to learn React';
helloWorld = 'Bye Bye React';
~~~~~~~~

Në anën tjetër, një variabel i deklaruar me `let` mund të modifikohet:

{title="Code Playground",lang="javascript"}
~~~~~~~~
// allowed
let helloWorld = 'Welcome to the Road to learn React';
helloWorld = 'Bye Bye React';
~~~~~~~~

**TIP:** Shpallni variablat me `let` nëse mendoni se do të dëshironi ta ricaktoni më vonë.

Vini re se një variabel e deklaruar direkt me `const` nuk mund të modifikohet. Megjithatë, kur variabela është një array ose objekt, vlera që ajo mban mund të modifikohet indirekt:

{title="Code Playground",lang="javascript"}
~~~~~~~~
// allowed
const helloWorld = {
  text: 'Welcome to the Road to learn React'
};
helloWorld.text = 'Bye Bye React';
~~~~~~~~

Ka mendime të ndryshme rreth asaj se kur duhet përdorur *const* dhe kur duhet të përdorim *let*. Unë do të rekomandoja përdorimin e `const` sa herë që të jetë e mundur për të treguar qëllimin e mbajtjes së strukturave tuaja të të dhënave të pandryshueshme, kështu që ju duhet vetëm të shqetësoheni për vlerat që përmbahen në objekte dhe arrays. Pandryshueshmëria përqafohet në ekosistemin React, kështu që `const` duhet të jetë zgjedhja juaj e parazgjedhur kur përcaktoni një variabel, megjithëse nuk ka të bëjë me ndryshueshmërinë, por për caktimin e variablave vetëm një herë. Tregon qëllimin e mos ndryshimit (ri-caktimit) të variables edhe pse përmbajtja e tij mund të ndryshohet.

{title="src/App.js",lang="javascript"}
~~~~~~~~
import React, { Component } from 'react';
import './App.css';

class App extends Component {
  render() {
# leanpub-start-insert
    const helloWorld = 'Welcome to the Road to learn React';
# leanpub-end-insert
    return (
      <div className="App">
        <h2>{helloWorld}</h2>
      </div>
    );
  }
}

export default App;
~~~~~~~~

Në aplikimin tuaj, ne do të përdorim `const` dhe` let` mbi `var` për pjesën tjetër të librit.

### Ushtrime:

* Lexoni rreth [ES6 const](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/const)
* Lexoni rreth [ES6 let](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let)
* Gjeni një kuptim të strukturave të të dhënave të pandryshueshme:
  * Pse ata kanë kuptim në programim?
  * Pse janë përqafuar në React dhe në ekosistemin e saj?

## ReactDOM

Komponenti App ndodhet në pikën hyrëse të React file *src/index.js* .

{title="src/index.js",lang="javascript"}
~~~~~~~~
import React from 'react';
import ReactDOM from 'react-dom';
import App from './App';
import './index.css';

ReactDOM.render(
  <App />,
  document.getElementById('root')
);
~~~~~~~~

`ReactDOM.render()` përdor një nyje DOM në HTML tuaj për ta zëvendësuar atë me JSX. Kjo është një mënyrë për të integruar React në çdo aplikim të huaj lehtë, dhe ju mund të përdorni `ReactDOM.render()` disa herë në aplikacionin tuaj. Ju mund ta përdorni për të bootstrap sintaksë të thjeshtë JSX, një komponent React, komponente të shumta React ose një aplikacion të tërë. Në një aplikim të thjeshtë React, ju do ta përdorni vetëm një herë për të nisur pemën e komponentit.

`ReactDOM.render()` pret dy argumente. Argumenti i parë është për renderimin e JSX. Argumenti i dytë specifikon vendin ku aplikacioni React hyn në HTML tuaj. Ajo pret një element me një `id='root'`, gjetur në file  *public/index.html*.

{title="Code Playground",lang="javascript"}
~~~~~~~~
ReactDOM.render(
  <h1>Hello React World</h1>,
  document.getElementById('root')
);
~~~~~~~~

Gjatë implementimit, `ReactDOM.render()` merr komponentin tuaj të aplikacionit, dhe mund ti kalojë thjeshtë JSX . Nuk kërkon një instancë komponentësh.

### Ushtrime:

* Hapni *public/index.html* tpër të parë se ku aplikacioni React hyn në HTML tuaj
* Lexoni rreth  [rendering elements in React](https://reactjs.org/docs/rendering-elements.html)

## Hot Module Replacement (HMR)-Zëvendësimi i modulit 

HMR mund të përdoret në file *src/index.js* për të përmirësuar përvojën tuaj si zhvillues. Default, *create-react-app* do të bëjë që browseri të rifreskojë faqen sa herë që modifikohet kodit i tij burimor. Provoni duke ndryshuar variablin `helloWorld` në file *src/App.js*, i cili duhet të bëjë që shfletuesi të rifreskojë faqen. Megjithatë, ekziston një mënyrë më e mirë për të trajtuar ndryshimet e kodit burimor gjatë zhvillimit.

Hot Module Replacement (HMR) është një mjet për rifreskimin e aplikacionit tuaj në shfletues pa rifreskimin e faqes. Ju mund ta aktivizoni atë në *create-react-app* duke shtuar konfigurimin e mëposhtëm tek file juaj  *src/index.js* :

{title="src/index.js",lang="javascript"}
~~~~~~~~
import React from 'react';
import ReactDOM from 'react-dom';
import './index.css';
import App from './App';

ReactDOM.render(
  <App />,
  document.getElementById('root')
);

# leanpub-start-insert
if (module.hot) {
  module.hot.accept();
}
# leanpub-end-insert
~~~~~~~~

Përsëri, ndryshoni variablën `helloWorld` në file *src/App.js* . Shfletuesi nuk duhet të rifreskohet, por aplikacioni do të rifreskojë dhe do të tregojë daljen e saktë. HMR vjen me përparësi të shumëfishta:

Imagjinoni që po bëni debug kodin tuaj me statement `console.log()`. Këto statement do të qëndrojnë në developer console, edhe pse keni ndryshuar kodin tuaj, sepse shfletuesi nuk e rifreskon më faqen. HMR e eliminon humbjen e kohës në rritje që duhet për të rifreskuar një shfletues.

Përfitimi më i dobishëm i HMR është që ju të mund të mbani gjendjen e aplikimit pasi aplikacioni të rifreskohet. Për shembull, supozoni që keni një dialog ose wizard në aplikacionin tuaj me hapa të shumëfishta dhe jeni në hap 3. Pa HMR, bëni ndryshime në kodin burimor dhe shfletuesi juaj rifreskon faqen. Ju pastaj do të duhet të hapni përsëri dialogun dhe lundroni nga hapi 1 deri në hapin 3 çdo herë. Me HMR dialogu juaj mbetet i hapur në hapin 3, kështu që ju mund të debugoni nga pika e saktë në të cilën jeni duke punuar. Me kohën e ruajtur nga ngarkimet e faqes, kjo e bën HMR një mjet të paçmuar për zhvilluesit React.

### Ushtrime:

* Ndryshoni *src/App.js* kodin burim disa herë për të parë HMR në veprim
* Shikoni 10 minutat e para të [Live React: Hot Reloading with Time Travel](https://www.youtube.com/watch?v=xsSnOQynTHs) nga Dan Abramov

## JavaScript në JSX

Deri më tani, ju keni dhënë disa variabla primitivë në JSX tuaj. Tani, do të bëjmë një listë të artikujve. Lista do të përmbajë të dhënat e mostrës në fillim, por më vonë do të mësojmë se si të marrim të dhënat nga një API i jashtëm.

Së pari ju duhet të përcaktoni listën e artikujve:

{title="src/App.js",lang="javascript"}
~~~~~~~~
import React, { Component } from 'react';
import './App.css';

# leanpub-start-insert
const list = [
  {
    title: 'React',
    url: 'https://reactjs.org/',
    author: 'Jordan Walke',
    num_comments: 3,
    points: 4,
    objectID: 0,
  },
  {
    title: 'Redux',
    url: 'https://redux.js.org/',
    author: 'Dan Abramov, Andrew Clark',
    num_comments: 2,
    points: 5,
    objectID: 1,
  },
];
# leanpub-end-insert

class App extends Component {
  ...
}
~~~~~~~~

Të dhënat e mostrës përfaqësojnë informacionin që do të marrim nga një API më vonë. Artikujt në këtë listë secili kanë një titull, një url dhe një autor, si dhe një identifikues, pikat (të cilat tregojnë se si një artikull është i popullarizuar) dhe numërimin e komenteve.

Tani ju mund të përdorni [built-in JavaScript map functionality](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map) në JSX, e cila përsëritet mbi një listë të artikujve për t'i shfaqur ato sipas atributeve specifike. Përsëri, ne përdorim kllapat gjarpërushe për enkapsulimmin e shprehjeve JavaScript në JSX:

{title="src/App.js",lang="javascript"}
~~~~~~~~
class App extends Component {
  render() {
    return (
      <div className="App">
# leanpub-start-insert
        {list.map(function(item) {
          return <div>{item.title}</div>;
        })}
# leanpub-end-insert
      </div>
    );
  }
}

export default App;
~~~~~~~~

Përdorimi i JavaScript së bashku me HTML në JSX është shumë i fuqishëm. Për një detyrë tjetër ju mund të keni përdorur `map` për të kthyer një listë të artikujve në një tjetër. Këtë herë, ne përdorëm `map` për të kthyer një listë të artikujve në elementë HTML.

{title="Code Playground",lang="javascript"}
~~~~~~~~
const array = [1, 4, 9, 16];

// pass a function to map
const newArray = array.map(function (x) { return x * 2; });

console.log(newArray);
// expected output: Array [2, 8, 18, 32]
~~~~~~~~

Deri më tani, vetëm 'titulli' shfaqet për çdo artikull. Le të eksperimentojmë me më shumë nga item's properties:

{title="src/App.js",lang="javascript"}
~~~~~~~~
class App extends Component {
  render() {
    return (
      <div className="App">
# leanpub-start-insert
        {list.map(function(item) {
          return (
            <div>
              <span>
                <a href={item.url}>{item.title}</a>
              </span>
              <span>{item.author}</span>
              <span>{item.num_comments}</span>
              <span>{item.points}</span>
            </div>
          );
        })}
# leanpub-end-insert
      </div>
    );
  }
}

export default App;
~~~~~~~~

Vini re se funksioni `map` është i përvijuar në JSX tuaj. Secili element shfaqet me një tag `<span>` dhe prona e url e elementit është në atributin `href` të tagit të ankorimit.

React do të shfaqë çdo element, por përsëri mund të bëni më shumë për të ndihmuar React të përqafojë potencialin e tij të plotë. Duke caktuar një atribut kryesor në secilin element të listës, React mund të identifikojë elementët e modifikuar kur ndryshon lista. Këto elemente të listës së mostrës vijnë me një identifikues:

{title="src/App.js",lang="javascript"}
~~~~~~~~
{list.map(function(item) {
  return (
# leanpub-start-insert
    <div key={item.objectID}>
# leanpub-end-insert
      <span>
        <a href={item.url}>{item.title}</a>
      </span>
      <span>{item.author}</span>
      <span>{item.num_comments}</span>
      <span>{item.points}</span>
    </div>
  );
})}
~~~~~~~~

Sigurohuni që atributi kryesor është një identifikues i qëndrueshëm. Shmangni përdorimin e indeksit të elementit në grup, sepse indeksi i grupeve nuk është i qëndrueshëm. Nëse lista ndryshon rendin e saj, për shembull, React nuk do të jetë në gjendje të identifikojë elementet siç duhet.

{title="src/App.js",lang="javascript"}
~~~~~~~~
// don't do this
{list.map(function(item, key) {
  return (
    <div key={key}>
      ...
    </div>
  );
})}
~~~~~~~~

Nisni aplikacionin tuaj në një shfletues dhe duhet të shihni të dyja elementët e listës të shfaqur.

### Ushtrime:

* Lexoni rreth [React lists and keys](https://reactjs.org/docs/lists-and-keys.html)
* Lexoni rreth [standard built-in array functionalities in JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/)
* Përdorni më shumë shprehje JavaScript në JSX.

## Funksionet e shigjetave ES6

JavaScript ES6 prezantoi funksionet shprehje shigjetë , të cilat janë më të shkurtër se një funksion shprehje.

{title="Code Playground",lang="javascript"}
~~~~~~~~
// function declaration
function () { ... }

// arrow function declaration
() => { ... }
~~~~~~~~

Ju mund të hiqni kllapat në një shprehje të shigjetës së funksionit nëse ka vetëm një argument, por ju duhet të mbani kllapa nëse ai merr shumë argumente:

{title="Code Playground",lang="javascript"}
~~~~~~~~
// allowed
item => { ... }

// allowed
(item) => { ... }

// not allowed
item, key => { ... }

// allowed
(item, key) => { ... }
~~~~~~~~

Ju gjithashtu mund të shkruani funksione `hartë` në mënyrë më konçize me një funksion shigjetë ES6:

{title="src/App.js",lang="javascript"}
~~~~~~~~
# leanpub-start-insert
{list.map(item => {
# leanpub-end-insert
  return (
    <div key={item.objectID}>
      <span>
        <a href={item.url}>{item.title}</a>
      </span>
      <span>{item.author}</span>
      <span>{item.num_comments}</span>
      <span>{item.points}</span>
    </div>
  );
})}
~~~~~~~~

Ju mund ta hiqni * trupin e bllokut*, kllapa gjarpërushe, me funksionin shigjetë ES6. Në një * trup konciz*, një kthim i nënkuptuar është i bashkangjitur; kështu, ju mund të hiqni deklaratën `return`. Kjo do të ndodhë shpesh në këtë libër, prandaj sigurohuni që të kuptoni dallimin në mes të një trupi bllok dhe një trupi konciz kur përdorni funksione shigjetë.

{title="src/App.js",lang="javascript"}
~~~~~~~~
# leanpub-start-insert
{list.map(item =>
# leanpub-end-insert
  <div key={item.objectID}>
    <span>
      <a href={item.url}>{item.title}</a>
    </span>
    <span>{item.author}</span>
    <span>{item.num_comments}</span>
    <span>{item.points}</span>
  </div>
# leanpub-start-insert
)}
# leanpub-end-insert
~~~~~~~~

JSX-ja juaj duhet të duket më koncize dhe më e lexueshme tani, meqë nuk përmban deklaratën e "funksionit", kllapat gjarpërushe dhe deklaratën e kthimit.

### Ushtrime:

* Lexoni rreth [ES6 arrow functions](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Functions/Arrow_functions)

## ES6 Klasat

JavaScript ES6 prezantoi klasat, të cilat zakonisht përdoren në gjuhët e programimit të orientuara në objekte. JavaScript, gjithmonë fleksibël në paradigmat e tij të programimit, lejon programimin funksional dhe programimin e orientuar drejt objekteve për të punuar krah për krah.

Ndërsa React përfshin programimin funksional, p.sh. struktura të pandryshueshme të të dhënave dhe kompozime të funksioneve, klasat përdoren për të deklaruar komponentët e klasës ES6. React përzien pjesët e mira të të dy paradigmave të programimit.

Konsideroni klasën e mëposhtme të Zhvilluesit për të shqyrtuar një klasë JavaScript ES6 pa një komponent.

{title="Code Playground",lang="javascript"}
~~~~~~~~
class Developer {
  constructor(firstname, lastname) {
    this.firstname = firstname;
    this.lastname = lastname;
  }

  getName() {
    return this.firstname + ' ' + this.lastname;
  }
}
~~~~~~~~

Një klasë ka një konstruktor për ta bërë atë të menjëhershme. Konstruktori merr argumente dhe i cakton ato në instancën e klasës. Një klasë gjithashtu mund të përcaktojë funksionet. Për shkak se funksioni është i lidhur me një klasë, quhet një metodë ose një metodë klase.

Klasa e Zhvilluesit është e vetmja deklaratë e klasës që ne përdorim këtu, pasi që mund të krijosh raste të shumta të një klase duke u thirrur në të. Është e ngjashme me komponentën e klasës ES6, e cila ka një deklaratë, por ju duhet ta përdorni atë diku tjetër për ta nxjerrë atë:

{title="Code Playground",lang="javascript"}
~~~~~~~~
const robin = new Developer('Robin', 'Wieruch');
console.log(robin.getName());
// output: Robin Wieruch
~~~~~~~~

React përdor klasa JavaScript ES6 për komponentët e klasës ES6, të cilat ju keni përdorur tashmë të paktën një herë deri më tani:

{title="src/App.js",lang="javascript"}
~~~~~~~~
import React, { Component } from 'react';

...

class App extends Component {
  render() {
    ...
  }
}
~~~~~~~~

Kur deklaroni komponentin e APP ai shtrihet nga një komponent tjetër. Në programimin e orientuar drejt objektit, termi "shtrihet" i referohet parimit të trashëgimisë, që do të thotë se funksionaliteti mund të kalojë nga një klasë në tjetrën. Klasa e aplikacionit shtrihet nga klasa e komponentit, që do të thotë se trashëgon funksionalitetin nga klasa e komponentit. Klasa e Komponentit përdoret për të zgjeruar një klasë bazë ES6 në një klasë komponentësh ES6. Ajo ka të gjitha funksionalitetet që një komponent në React ka nevojë. Metoda e paraqitjes është një funksion që keni përdorur tashmë. Ju do të mësoni rreth metodave të tjera të klasës së komponentit teksa lëvizim së bashku.

Klasa 'Component' enkapsulon të gjitha detajet e implementimit të një komponenti React, i cili lejon zhvilluesit të përdorin klasat si komponente në React.

Metodat e ekspozuara nga React `Component` janë ndërfaqja e tij publike. Një nga këto metoda duhet të mbivendoset, ndërsa të tjerat nuk kanë nevojë të mbivendosen. Ju do të mësoni rreth këtyre kur ne diskutojmë metodat e ciklit të jetës më vonë. Metoda `render ()` duhet të mbivendoset, sepse ajo përcakton outputin e React `Component`, prandaj duhet të përcaktohet. Këto janë bazat e klasave JavaScript ES6, dhe se si ato përdoren në React për t'i zgjeruar ato tek komponentët.

### Ushtrime:

* Lexoni rreth  [JavaScript fundamentals before learning React](https://www.robinwieruch.de/javascript-fundamentals-react-requirements/)
* Lexoni rreth  [ES6 classes](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Classes)

{pagebreak}

Urime, ju keni mësuar të bootstrap aplikimin tuaj të parë React! Le të radhisim:

* **React**
  * Create-react-app bootstraps një aplikim React
  * JSX përzien HTML dhe JavaScript për të përcaktuar prodhimin e komponentëve të React në metodat e tyre të paraqitjes
  * Komponentët, instancat dhe elementet janë elemente gjëra të ndryshme në React
  * `ReactDOM.render()` është një pikë hyrjeje për një aplikim React për të lidhur React në DOM
  * Funksionet e integruara JavaScript mund të përdoren në JSX
  * Harta mund të përdoret për të paraqitur një listë të items si elementë HTML
* **ES6**
  * Deklarimi i variablave me `const` dhe` let` mund të përdoren për raste specifike përdorimi
  * Përdorni const mbi aplikacionet React
  * Funksionet e shigjetës mund të përdoren për të mbajtur funksionet tuaja në mënyrë koncize
  * Klasat përdoren për të përcaktuar komponentët në React duke i zgjeruar ato

Tani që keni përfunduar kapitullin e parë, është e këshillueshme që të eksperimentoni me kodin burimor që keni shkruar deri më tani dhe shihni se çfarë ndryshimesh mund të bëni vetë. Kodi burimor mund të gjendet në [official repository](https://github.com/the-road-to-learn-react/hackernews-client/tree/5.1).
