# **.projectCommitPlace**
Miejsce do commitowania notatek i zdjec tego co zrobilismy

**Projekt oprogramowania**
Aplikacja: API Tool
Metodyka: Waterfall


### Wymagania funkcjonalne

1. **Tworzenie nowych modułów**
   - Komenda: `apitool create <module_name>`
     - Opis: Tworzy nowy moduł o nazwie `<module_name>`.
     - Przykład: `apitool create mysqlconnection`

2. **Tworzenie szablonów kodu dla różnych typów modułów**
   - Komenda: `apitool create <module_type> <module_name>`
     - Opis: Tworzy moduł o określonym typie z wstępnym szablonem kodu.
     - Przykład: `apitool create mysqlconnection dbConnector`
     - Typy modułów:
       - `dbConnector` - moduł do połączeń z bazą danych
       - `apiHandler` - moduł do obsługi żądań API
       - `authModule` - moduł do zarządzania autoryzacją

3. **Lista dostępnych typów modułów**
   - Komenda: `apitool list types`
     - Opis: Wyświetla listę dostępnych typów modułów.
     - Przykład: `apitool list types`

4. **Pomoc i dokumentacja**
   - Komenda: `apitool help`
     - Opis: Wyświetla pomoc i dostępne komendy.
     - Przykład: `apitool help`

5. **Konfiguracja modułów**
   - Komenda: `apitool configure <module_name> <setting> <value>`
     - Opis: Konfiguruje istniejący moduł.
     - Przykład: `apitool configure mysqlconnection timeout 30`

### Wymagania niefunkcjonalne

1. **Wydajność**
   - Aplikacja powinna tworzyć nowe moduły w czasie nie dłuższym niż 2 sekundy.
   - Aplikacja powinna działać bez zauważalnych opóźnień na standardowych komputerach.

2. **Skalowalność**
   - Aplikacja powinna być w stanie obsługiwać tworzenie wielu modułów jednocześnie bez degradacji wydajności.

3. **Użyteczność**
   - Aplikacja powinna posiadać intuicyjny interfejs użytkownika.
   - Dokumentacja i pomoc powinna być czytelna i łatwo dostępna.

4. **Bezpieczeństwo**
   - Aplikacja powinna sprawdzać poprawność danych wejściowych, aby zapobiec wprowadzeniu niepoprawnych lub złośliwych danych.
   - Aplikacja powinna zapewniać, że wszystkie pliki tworzone są z odpowiednimi uprawnieniami, aby zapobiec nieautoryzowanemu dostępowi.

5. **Kompatybilność**
   - Aplikacja powinna działać na najpopularniejszych systemach operacyjnych: Windows, macOS, Linux.
   - Aplikacja powinna być zgodna z najnowszymi wersjami popularnych interpreterów CLI (np. Bash, Zsh, CMD, PowerShell).

6. **Rozszerzalność**
   - Aplikacja powinna umożliwiać łatwe dodawanie nowych typów modułów w przyszłości.
   - Kod aplikacji powinien być modularny, aby umożliwić łatwe aktualizacje i modyfikacje.

### Przykłady użycia

1. **Tworzenie nowego modułu połączenia z bazą danych MySQL**
   ```
   apitool create mysqlconnection dbConnector
   ```

2. **Konfiguracja czasu oczekiwania dla modułu MySQLConnection**
   ```
   apitool configure mysqlconnection timeout 30
   ```

3. **Wyświetlenie dostępnych typów modułów**
   ```
   apitool list types
   ```

4. **Wyświetlenie pomocy**
   ```
   apitool help
   ```
