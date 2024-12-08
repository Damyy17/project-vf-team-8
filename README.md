**Proiect MiniSat**

# Introducere
  Acest proiect se concentrează pe utilizarea și analizarea modului de funcționare al solverului MiniSat, un program eficient pentru rezolvarea problemelor de satisfiabilitate booleeană (SAT). MiniSat este utilizat pentru a determina dacă există o asignare de valori adevărat/fals care face ca o formulă logică să fie satisfăcută.

# Descrierea problemei
  Satisfiabilitatea booleeană (SAT) este o problemă fundamentală în domeniul informaticii, cu aplicații importante în verificarea modelelor, în bioinformatică și criptografie. Solverele SAT, precum MiniSat, sunt utilizate pentru a evalua dacă o formulă booleeană în formă normală conjunctivă (CNF) are o soluție.

# Instalare MiniSat
# Pe Windows
1. Activează WSL:
    bash
    wsl --install
2. Instalează o distribuție Linux (precum Ubuntu) din Microsoft Store.
3. După instalare, deschide terminalul Linux și urmează pașii pentru Linux.

# Pe Linux
1. Instalează compilatorul și uneltele de build:
    bash
    sudo apt install g++ make
2. Clonează repository-ul MiniSat:
    bash
    git clone https://github.com/nikivazou/minisat.git
    cd minisat/core
    make
3. Compilează proiectul:
    bash
    ./minisat
   
# Pe macOS
1. Asigură-te că Homebrew este instalat:
    bash
    /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
2. Instalează MiniSat folosind Homebrew:
    bash
    brew install minisat
   
# Algoritmi 
# Algoritmul DPLL
# Algoritmul CDCL

# Structura și modul de lucru al MiniSat pe scurt
  MiniSat este un solver SAT eficient, implementat într-un program secvențial care urmează mai mulți pași pentru a rezolva formulele SAT. Acesta include inițializarea solverului, citirea fișierelor de intrare, propagarea unității, decizia asupra variabilelor, analiza conflictelor și învățarea clauzelor.
Pașii executați în programul MiniSat:
  1. **Inițializarea și setarea opțiunilor**: Configurarea solverului prin funcțiile `setUsageHelp` și `parseOptions`.
  2. **Citirea și parsarea fișierului de intrare**: Citirea fișierului care conține formula logică, utilizând funcția `parse_DIMACS`.
  3. **Propagarea unității și simplificarea**: Deducerea valorilor variabilelor și simplificarea clauzelor pentru optimizarea căutării.
  4. **Decizia și crearea nivelelor de decizie**: Selectarea variabilelor pentru a explora soluțiile posibile.
  5. **Detectarea și analiza conflictelor**: Analizarea conflictelor pentru a genera clauze învățate.
  6. **Backtracking și restarturi**: Reîntoarcerea la nivele anterioare de decizie și aplicarea restarturilor pentru a îmbunătăți eficiența.

# Contribuții
- **Grosu Damian**: S-a ocupat de rularea benchmarkurilor și raportul în LaTeX.
- **Scoropad Iulian**: S-a ocupat dee documentarea algoritmilor DPLL și CDCL.
- **Daniel Dobrescu**: A explicat modul de funcționare al programului MiniSat.
- **Anton Constantin-Adrian**: S-a ocupat de introducerea și descrierea problemei proiectului.


