# Docker Laravel Template

Szablon do szybkiego uruchomienia projektu Laravel w kontenerach Docker.

## Zawartość
- PHP 8.2 FPM
- Nginx
- MySQL
- Wszystkie potrzebne rozszerzenia PHP dla Laravel
- Composer
- Prawidłowo skonfigurowane uprawnienia dla nginx

## Jak używać

1. Skopiuj zawartość tego katalogu do nowego projektu
2. Dostosuj nazwy kontenerów w `docker-compose.yml` (zamień "app", "webserver", "db" na nazwę swojego projektu)
3. Zmień hasło do bazy danych w `docker-compose.yml`
4. Zmień port w `docker-compose.yml` jeśli potrzebne (domyślnie 8081)
5. Uruchom kontenery:
   ```bash
   docker compose up -d
   ```

## Struktura
- `Dockerfile` - konfiguracja PHP i zależności
- `docker-compose.yml` - definicja usług (PHP, Nginx, MySQL)
- `nginx/` - konfiguracja Nginx
- `php/` - konfiguracja PHP
- `mysql/` - konfiguracja MySQL

## Uwagi
- Upewnij się, że porty 8081 i 3306 są wolne
- Wszystkie pliki projektu powinny być w katalogu głównym
- Uprawnienia są już skonfigurowane dla użytkownika nginx 