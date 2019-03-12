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

Now we will get to know JSX, the syntax in React. As mentioned before, *create-react-app* has already bootstrapped a basic application for you, and all files come with their own default implementations. For now, the only file we will modify is the *src/App.js* file.

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

Don't worry if you're confused by the import/export statements and class declaration now. These are features of JavaScript ES6 we will revisit in a later chapter.

In the file you should see a **React ES6 class component** with the name App. This is a component declaration. After you have declared a component, you can use it as an element anywhere in your application. It will produce an **instance** of your **component** or, in other words, the component gets instantiated.

{title="Code Playground",lang="javascript"}
~~~~~~~~
// component declaration
class App extends Component {
  ...
}

// component usage (also called instantiation for a class)
// creates an instance of the component
<App />
~~~~~~~~

The returned **element** is specified in the `render()` method. The components you instantiated earlier are made up of elements, so it is important to understand the differences between a component, an instance of a component, and an element.

You should see where the App component is instantiated, else you couldn't see the rendered output in a browser. The App component is only the declaration, but not the usage. You can instantiate the component anywhere in your JSX with `<App />`. You will see later where this happens in this application.

The content in the render block may look similar to HTML, but it is actually JSX. JSX allows you to mix HTML and JavaScript. It is powerful, but it can be confusing when you are used to separating the two languages. It is a good idea to start by using basic HTML in your JSX. Open the `App.js` file and remove all unnecessary HTML code as shown:

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

Now, you only return HTML in your `render()` method without any JavaScript. Let's define the "Welcome to the Road to learn React" as a variable. A variable is set in JSX by curly braces.

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

Start your application on the command line with `npm start` to verify the changes you've made.

You might have noticed the `className` attribute. It reflects the standard `class` attribute in HTML. JSX had replaced a handful of internal HTML attributes, but you can find all the [supported HTML attributes in React's documentation](https://reactjs.org/docs/dom-elements.html#all-supported-html-attributes), which all follow the camelCase convention. On your way to learn React, expect to run across more JSX specific attributes.

### Exercises:

* Define more variables and render them in JSX
  * Use a complex object to represent a user with a first name and last name
  * Render the user properties in JSX
* Read about [JSX](https://reactjs.org/docs/introducing-jsx.html)
* Read about [React components, elements and instances](https://reactjs.org/blog/2015/12/18/react-components-elements-and-instances.html)

## ES6 const and let

Notice that we declared the variable `helloWorld` with a `var` statement. JavaScript ES6 comes with two more ways to declare variables: `const` and `let`. In JavaScript ES6, you will rarely find `var` anymore. A variable declared with `const` cannot be re-assigned or re-declared, and cannot be changed or modified. Once the variable is assigned, you cannot change it:

{title="Code Playground",lang="javascript"}
~~~~~~~~
// not allowed
const helloWorld = 'Welcome to the Road to learn React';
helloWorld = 'Bye Bye React';
~~~~~~~~

Conversely, a variable declared with `let` can be modified:

{title="Code Playground",lang="javascript"}
~~~~~~~~
// allowed
let helloWorld = 'Welcome to the Road to learn React';
helloWorld = 'Bye Bye React';
~~~~~~~~

**TIP:** Declare variables with `let` if you think you'll want to re-assign it later on.

Note that a variable declared directly with `const` cannot be modified. However, when the variable is an array or object, the values it holds can get updated through indirect means:

{title="Code Playground",lang="javascript"}
~~~~~~~~
// allowed
const helloWorld = {
  text: 'Welcome to the Road to learn React'
};
helloWorld.text = 'Bye Bye React';
~~~~~~~~

There are varying opinions about when to use *const* and when to use *let*. I would recommend using `const` whenever possible to show the intent of keeping your data structures immutable, so you only have to worry about the values contained in objects and arrays. Immutability is embraced in the React ecosystem, so `const` should be your default choice when you define a variable, though it's not really about immutability, but about assigning variables only once. It shows the intent of not changing (re-assigning) the variable even though its content can be changed.

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

In your application, we will use `const` and `let` over `var` for the rest of the book.

### Exercises:

* Read about [ES6 const](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/const)
* Read about [ES6 let](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let)
* Gain an understanding of immutable data structures:
  * Why do they make sense in programming?
  * Why are they embraced in React and its ecosystem?

## ReactDOM

The App component is located in your entry point to the React world: the *src/index.js* file.

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

`ReactDOM.render()` uses a DOM node in your HTML to replace it with JSX. It's a way to integrate React in any foreign application easily, and you can use `ReactDOM.render()` multiple times across your application. You can use it to bootstrap simple JSX syntax, a React component, multiple React components, or an entire application. In a plain React application, you would only use it once to bootstrap the component tree.

`ReactDOM.render()` expects two arguments. The first argument is for rendering the JSX. The second argument specifies the place where the React application hooks into your HTML. It expects an element with an `id='root'`, found in the *public/index.html* file.

{title="Code Playground",lang="javascript"}
~~~~~~~~
ReactDOM.render(
  <h1>Hello React World</h1>,
  document.getElementById('root')
);
~~~~~~~~

During implementation, `ReactDOM.render()` takes your App component, though it can also pass simple JSX. It doesn't require a component instance.

### Exercises:

* Open the *public/index.html* to see where the React application hooks into your HTML
* Read about [rendering elements in React](https://reactjs.org/docs/rendering-elements.html)

## Hot Module Replacement

Hot Module Replacement can be used in the *src/index.js* file to improve your experience as a developer. By default, *create-react-app* will cause the browser to refresh the page whenever its source code is modified. Try it by changing the `helloWorld` variable in your *src/App.js* file, which should cause the browser to refresh the page. There is a better way of handling source code changes during development, however.

Hot Module Replacement (HMR) is a tool for reloading your application in the browser without the page refresh. You can activate it in *create-react-app* by adding the following configuration to your *src/index.js* file:

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

Again, change the `helloWorld` variable in your *src/App.js* file. The browser shouldn't refresh, but the application will reload and show the correct output. HMR comes with multiple advantages:

Imagine you are debugging your code with `console.log()` statements. These statements will stay in your developer console, even though you changed your code, because the browser doesn't refresh the page anymore. In a growing application, page refreshes delay productivity; HMR removes this obstacle by eliminating the incremental time loss it takes for a browser to reload.

The most useful benefit of HMR is that you can keep the application state after the application reloads. For instance, assume you have a dialog or wizard in your application with multiple steps, and you are on step 3. Without HMR, you make changes to the source code and your browser refreshes the page. You would then have to open the dialog again and navigate from step 1 to step 3 each time. With HMR your dialog stays open at step 3, so you can debug from the exact point you're working on. With the time saved from page loads, this makes HMR an invaluable tool for React developers.

### Exercises:

* Change your *src/App.js* source code a few times to see HMR in action
* Watch the first 10 minutes of [Live React: Hot Reloading with Time Travel](https://www.youtube.com/watch?v=xsSnOQynTHs) by Dan Abramov

## Complex JavaScript in JSX

So far, you have rendered a few primitive variables in your JSX. Now, we will render a list of items. The list will contain sample data in the beginning, but later we will learn how to fetch the data from an external API.

First you have to define the list of items:

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

The sample data represents information we will fetch from an API later on. Items in this list each have a title, a url, and an author, as well an identifier, points (which indicate how popular an article is), and a count of comments.

Now you can use the [built-in JavaScript map functionality](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map) in JSX, which iterates over a list of items to display them according to specific attributes. Again, we use curly braces to encapsulate the JavaScript expression in JSX:

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

Using JavaScript alongside HTML in JSX is very powerful. For a different task you may have used `map` to convert one list of items to another. This time, we used `map` to convert a list of items to HTML elements.

{title="Code Playground",lang="javascript"}
~~~~~~~~
const array = [1, 4, 9, 16];

// pass a function to map
const newArray = array.map(function (x) { return x * 2; });

console.log(newArray);
// expected output: Array [2, 8, 18, 32]
~~~~~~~~

So far, only the `title` is displayed for each item. Let's experiment with more of the item's properties:

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

Note how the `map` function is inlined in your JSX. Each item property is displayed with a `<span>` tag, and the url property of the item is in the `href` attribute of the anchor tag.

React will display each item, but you can still do more to help React embrace its full potential. By assigning a key attribute to each list element, React can identify modified items when the list changes. These sample list items come with an identifier:

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

Make sure that the key attribute is a stable identifier. Avoid using the index of the item in the array, because the array index is not stable. If the list changes its order, for example, React will not be able to identify the items properly.

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

Start your app in a browser, and you should see both items of the list displayed.

### Exercises:

* Read about [React lists and keys](https://reactjs.org/docs/lists-and-keys.html)
* Recap the [standard built-in array functionalities in JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/)
* Use more JavaScript expressions on your own in JSX

## ES6 Arrow Functions

JavaScript ES6 introduced arrow functions expressions, which are shorter than a function expressions.

{title="Code Playground",lang="javascript"}
~~~~~~~~
// function declaration
function () { ... }

// arrow function declaration
() => { ... }
~~~~~~~~

You can remove the parentheses in an arrow function expression if it only has one argument, but you have to keep the parentheses if it gets multiple arguments:

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

You can also write `map` functions more concisely with an ES6 arrow function:

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

You can remove the *block body*, the curly braces, with the ES6 arrow function. In a *concise body*, an implicit return is attached; thus, you can remove the `return` statement. This will happen often in this book, so be sure to understand the difference between a block body and a concise body when using arrow functions.

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

Your JSX should look more concise and readable now, as it omits the `function` statement, the curly braces, and the return statement.

### Exercises:

* Read about [ES6 arrow functions](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Functions/Arrow_functions)

## ES6 Classes

JavaScript ES6 introduced classes, which are commonly used in object-oriented programming languages. JavaScript, always flexible in its programming paradigms, allows functional programming and object-oriented programming to work side-by-side.

While React embraces functional programming, e.g. immutable data structures and function compositions, classes are used to declare ES6 class components. React mixes the good parts of both programming paradigms.

Consider the following Developer class to examine a JavaScript ES6 class without a component.

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

A class has a constructor to make it instantiable. The constructor takes arguments and assigns them to the class instance. A class can also define functions. Because the function is associated with a class, it is called a method, or a class method.

The Developer class is the only class declaration we use here, as you can create multiple instances of a class by invoking it. It is similar to the ES6 class component, which has a declaration, but you have to use it somewhere else to instantiate it:

{title="Code Playground",lang="javascript"}
~~~~~~~~
const robin = new Developer('Robin', 'Wieruch');
console.log(robin.getName());
// output: Robin Wieruch
~~~~~~~~

React uses JavaScript ES6 classes for ES6 class components, which you have already used at least once so far:

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

When you declare the App component it extends from another component. In object-oriented programming, the term "extends" refers to the principle of inheritance, which means that functionality can be passed from one class to another. The App class extends from the Component class, meaning it inherits functionality from the Component class. The Component class is used to extend a basic ES6 class to a ES6 component class. It has all the functionalities that a component in React needs. The render method is one function you have already used. You will learn about other component class methods as we move along.

The `Component` class encapsulates all the implementation details of a React component, which allows developers to use classes as components in React.

Methods exposed by a React `Component` are its public interface. One of these methods must be overridden, while the others don't need to be overridden. You will learn about these when we discuss lifecycle methods later. The `render()` method has to be overridden, because it defines the output of a React `Component`, so it must be defined. These are the basics of JavaScript ES6 classes, and how they are used in React to extend them to components.

### Exercises:

* Read about [JavaScript fundamentals before learning React](https://www.robinwieruch.de/javascript-fundamentals-react-requirements/)
* Read about [ES6 classes](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Classes)

{pagebreak}

Congratulations, you have learned to bootstrap your first React application! Let's recap:

* **React**
  * Create-react-app bootstraps a React application
  * JSX mixes up HTML and JavaScript to define the output of React components in their render methods
  * Components, instances, and elements are different items in React
  * `ReactDOM.render()` is an entry point for a React application to hook React into the DOM
  * Built-in JavaScript functionalities can be used in JSX
  * Map can be used to render a list of items as HTML elements
* **ES6**
  * Variable declarations with `const` and `let` can be used for specific use cases
  * Use const over let in React applications
  * Arrow functions can be used to keep your functions concise
  * Classes are used to define components in React by extending them

Now that you've completed the first chapter, it's advisable to experiment with the source code you have written so far and see what changes you can make on your own. You can find the source code in the [official repository](https://github.com/the-road-to-learn-react/hackernews-client/tree/5.1).
