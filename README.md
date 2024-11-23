# Valheim Worlds Sharing Repository

Witamy w repozytorium służącym do wymiany zapisów świata gry **Valheim**! Ten przewodnik krok po kroku pokaże Ci, jak pobierać zmiany z repozytorium, wypychać swoje zmiany oraz upewnić się, że wszystko działa poprawnie.

---

## Wymagania wstępne

1. **Zainstalowany Git**:
   - Pobierz i zainstaluj Git z [git-scm.com](https://git-scm.com/).
   - Podczas instalacji wybierz opcję "Git from the command line and also from 3rd-party software".

2. **Konto GitHub**:
   - Jeśli jeszcze nie masz konta GitHub, załóż je na [github.com](https://github.com/).

3. **Gra Valheim**:
   - Gra musi być zainstalowana na Twoim komputerze.
   - Świat, który chcesz współdzielić, powinien być zapisany lokalnie na Twojej maszynie.

4. **Folder lokalny gry**:
   - Repozytorium **musi być zlokalizowane w folderze**:
     ```
     ~/AppData/LocalLow/IronGate/Valheim/worlds_local
     ```

---

## Instrukcja krok po kroku

### 1. Klonowanie repozytorium (pierwsze pobranie)

1. **Znajdź folder gry Valheim**:
   - Otwórz Eksplorator plików (Windows).
   - Wpisz w pasku adresu:
     ```
     %AppData%/../LocalLow/IronGate/Valheim/worlds_local
     ```
   - Upewnij się, że znajdujesz się w folderze `worlds_local`.

2. **Otwórz terminal w tym folderze**:
   - Kliknij prawym przyciskiem myszy w folderze `worlds_local` i wybierz **Otwórz w terminalu** (lub uruchom terminal i przejdź do tego folderu poleceniem `cd`).

3. **Sklonuj repozytorium**:
   - W terminalu wpisz:
     ```bash
     git clone git@github.com:<TwojaNazwaUżytkownika>/<NazwaRepozytorium>.git .
     ```
     **Uwaga**: Kropka (`.`) na końcu oznacza, że repozytorium zostanie pobrane do aktualnego folderu.

4. **Sprawdź, czy pliki się pobrały**:
   - Po wykonaniu polecenia powinieneś zobaczyć pliki repozytorium w folderze `worlds_local`.

---

### 2. Pobieranie zmian z repozytorium

1. **Upewnij się, że jesteś w folderze `worlds_local`**:
   ```bash
   cd ~/AppData/LocalLow/IronGate/Valheim/worlds_local
2. **Pobierz najnowsze zmiany z GitHub**:
   ```bash
   git pull origin master
   ```
  **Uwaga**: Polecenie to aktualizuje Twój lokalny folder o najnowsze zmiany przesłane przez innych.

  ### 3. Wypychanie własnych zmian

1. **Zagraj w grę i zapisz świat**:
   - Po grze zapisz swój świat w Valheim.
   - Upewnij się, że zapisy zostały zaktualizowane w folderze `worlds_local`.

2. **Dodaj swoje zmiany do Git**:
   - W terminalu wpisz:
     ```bash
     git add .
     ```

3. **Zatwierdź zmiany**:
   - Wpisz:
     ```bash
     git commit -m "Opis zmian, np. Aktualizacja świata"
     ```

4. **Wypchnij zmiany na GitHub**:
   - Wpisz:
     ```bash
     git push origin master
     ```

   Twoje zmiany zostaną przesłane do zdalnego repozytorium i będą dostępne dla innych graczy.

## Najczęstsze problemy

1. **Brak uprawnień do wypychania zmian**:
   - Upewnij się, że Twój klucz SSH został poprawnie skonfigurowany. Instrukcję znajdziesz tutaj: [Adding an SSH key to GitHub](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account).

2. **"Permission denied (publickey)"**:
   - Sprawdź, czy masz skonfigurowany klucz SSH:
     ```bash
     ssh -T git@github.com
     ```
   - Jeśli klucz nie działa, dodaj go zgodnie z instrukcjami GitHub.

3. **Zły folder repozytorium**:
   - Upewnij się, że repozytorium znajduje się w folderze:
     ```
     ~/AppData/LocalLow/IronGate/Valheim/worlds_local
     ```

---

## Uwagi

- **Nie usuwaj plików ignorowanych przez `.gitignore`**, ponieważ mogą być potrzebne lokalnie.
- **Pamiętaj o synchronizacji zmian**, aby uniknąć konfliktów z innymi graczami.
- Jeśli potrzebujesz pomocy, skontaktuj się z administratorem repozytorium.

Miłej gry! 🎮🌍
