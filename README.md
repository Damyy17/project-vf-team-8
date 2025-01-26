# Evaluarea MiniSat: Performanță și Provocări în Rezolvarea Problemelor SAT

## Autorii : 
- **Grosu Damian**
- **Scoropad Iulian**
- **Daniel Dobrescu**
- **Anton Constantin-Adrian**

  Raportul dat se concentrează pe analiza problemei satisfiabilității booleene (SAT), prima problemă recunoscută ca NP-completă, și pe aplicabilitatea acesteia în diverse domenii. Documentul prezintă în detaliu funcționarea și îmbunătățirile aduse MiniSat, un solver SAT minimalist și eficient,dezvoltat de Niklas Eén și Niklas Sörensson. Raportul include o descriere a structurilor și algoritmilor MiniSat, ghiduri pentru instalare, precum și metodologia utilizată pentru testarea performantelor acestuia.
  Deasemenea MiniSat va fi  testat pe un set de benchmark-uri din competiția SAT 2024, analizănd performanța MiniSat în termeni de satisfiabilitate, relevând constrângerile de timp, hardware și discutând eficiența acestuia în diferite scenarii. Concluziile subliniază succesul în rezolvarea problemelor simple, dar și dificultățile întâlnite în cazuri complexe, oferind perspective asupra îmbunătățirilor viitoare.
  Concluziile care le vom sublinia în urma realizării proiectului vor arăta atât succesul în rezolvarea problemelor simple, dar și dificultățile întâlnite în cazuri complexe, oferind perspective asupra îmbunătățirilor viitoare.
  
## Instalare MiniSat
### Pe Windows
1. Activează WSL:
 ```bash
    wsl --install
```
2. Instalează o distribuție Linux (precum Ubuntu) din Microsoft Store.
3. După instalare, deschide terminalul Linux și urmează pașii pentru Linux.

### Pe Linux
1. Instalează compilatorul și uneltele de build:
```bash
    sudo apt update
    sudo apt install g++ make
    sudo apt install git build −essential
    sudo apt install zlib1g-dev
```
    
2. Clonează repository-ul MiniSat:
```bash
    git clone https://github.com/niklasso/minisat.git
```
3. În fisierul Makefile adaugăm următorul cod pentru setarea flag-urilor compilatorului C++ și pentru a spune compilatorui să fie mai permisiv:
```bash
    CXXFLAGS += -std=c++11 -fperfmissive
```
4. Salvăm si închidem fisierul Makefile, recompilăm Minisat
```bash
    make r
    make cr
```
Prima comandă este pentru versiunea standart a MiniSat, a doua comandă este pentru a impune MiniSat să ruleze Main.cc din fisierul core.
5. Verificăm instalarea
```bash
    . /minisat
    . /minisat_core
```
   
### Pe macOS
1. Asigură-te că Homebrew este instalat:
```
    /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
 ```
2. Instalează MiniSat folosind Homebrew:
```
    brew install minisat
```
   
## Contribuțiile proprii
- 17/11/2024 -> Damian Grosu -> Urcare cod MiniSat
- 07/12/2024 -> Daniel Dobrescu -> Creare fisier README si LICENSE  
- 08/12/2024 -> Damian Grosu -> Urcare rezultate de la rularea benchmarkului familiei Miter (in fisierul benchmark-results)
- 08/12/2024 -> Daniel Dobrescu -> Modificare fisier README
- 08/12/2024 -> Scoropad Iulian -> Adaugare fisier "raport text", unde va fi localizat versiunea actualizată a textului si linkul catre proiectul overleaf. Analizare feedback de la versiunea draft, modificare text unde era necesar, modificare fisier README. 
- 06.01.2025 - 23.01.2025 -> Scoropad Iulian, Dobrescu Daniel, Grosu Damian -> Analizare si documentare cod minisat
- 23.01.2025 - 25.01.2025 -> Scoropad Iulian, Dobrescu Daniel, Grosu Damian ->Proiectarea si realizarea experimentului cu ulterioare modificari si testari pe codul minisat.
- 26.01.2025 -> Scoropad Iulian -> Updatarea raportului final cu contributiile colegilor.
- 26.01.2025 -> Daniel Dobrescu, Grosu Damian -> crearea clipului video si editarea lui


