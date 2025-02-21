# V5: Wymagania dotyczące Komunikacji Sieciowej

## Cele Kontrolne

Celami kontrolnymi wymienionych w tej sekcji jest zapewnienie poufności i integralności informacji wymienianych między aplikacją mobilną a punktami końcowymi usługi zdalnej. Aplikacja mobilna musi przynajmniej ustanawiać bezpieczny, szyfrowany kanał komunikacji sieciowej przy użyciu protokołu TLS z odpowiednimi ustawieniami. Poziom 2 zawiera dodatkowe szczegółowe środki ochrony, takie jak SSL Pinning.

## Wymagania Dotyczące Weryfikacji Bezpieczeństwa

| # | MSTG-ID | Description | L1 | L2 |
| -- | ---------- | ---------------------- | - | - |
| **5.1** | MSTG-NETWORK-1 | Dane są szyfrowane w sieci za pomocą TLS. Bezpieczny kanał jest konsekwentnie używany w całej aplikacji. | x | x |
| **5.2** | MSTG-NETWORK-2 | Ustawienia TLS są zgodne z aktualnymi najlepszymi praktykami lub jak najbardziej zbliżone, jeśli mobilny system operacyjny nie obsługuje zalecanych standardów. | x | x |
| **5.3** | MSTG-NETWORK-3 | Aplikacja weryfikuje certyfikat X.509 zdalnego punktu końcowego po ustanowieniu bezpiecznego kanału. Akceptowane są tylko certyfikaty podpisane przez zaufany urząd certyfikacji. | x | x |
| **5.4** | MSTG-NETWORK-4 | Aplikacja używa własnego magazynu certyfikatów lub stosuje SSL Pinning dla punktu końcowego lub klucza publicznego, a następnie nie nawiązuje połączeń z punktami końcowymi obsługującymi inny certyfikat lub klucz, nawet jeśli jest podpisany przez zaufany urząd certyfikacji. |   | x |
| **5.5** | MSTG-NETWORK-5 | Aplikacja nie opiera się na jednym niezabezpieczonym kanale komunikacji (e-mail lub SMS) w przypadku krytycznych operacji, takich jak rejestracje i odzyskiwanie konta. |  | x |
| **5.6** | MSTG-NETWORK-6 | Aplikacja zależna jest od aktualnych bibliotek połączeniowych i zabezpieczeń |  | x |

## Bibliografia

Przewodnik testowania zabezpieczeń mobilnych OWASP zawiera szczegółowe instrukcje dotyczące weryfikacji wymagań wymienionych w tej sekcji.

- General: Testing Network Communication - <https://github.com/OWASP/owasp-mstg/blob/master/Document/0x04f-Testing-Network-Communication.md>
- Android: Testing Network Communication - <https://github.com/OWASP/owasp-mstg/blob/master/Document/0x05g-Testing-Network-Communication.md>
- iOS: Testing Network Communication - <https://github.com/OWASP/owasp-mstg/blob/master/Document/0x06g-Testing-Network-Communication.md>

Aby uzyskać więcej informacji, zobacz także:

- OWASP Mobile Top 10: M3 (Insecure Communication) - <https://owasp.org/www-project-mobile-top-10/2016-risks/m3-insecure-communication>
- CWE 295 (Improper Certificate Validation) - <https://cwe.mitre.org/data/definitions/295.html>
- CWE 296 (Improper Following of a Certificate's Chain of Trust) - <https://cwe.mitre.org/data/definitions/296.html>
- CWE 297 (Improper Validation of Certificate with Host Mismatch) - <https://cwe.mitre.org/data/definitions/297.html>
- CWE 298 (Improper Validation of Certificate Expiration) - <https://cwe.mitre.org/data/definitions/298.html>
- CWE 308 (Use of Single-factor Authentication) - <https://cwe.mitre.org/data/definitions/308.html>
- CWE 319 (Cleartext Transmission of Sensitive Information) - <https://cwe.mitre.org/data/definitions/319.html>
- CWE 326 (Inadequate Encryption Strength) - <https://cwe.mitre.org/data/definitions/326.html>
- CWE 327 (Use of a Broken or Risky Cryptographic Algorithm) - <https://cwe.mitre.org/data/definitions/327.html>
- CWE 780 (Use of RSA Algorithm without OAEP) - <https://cwe.mitre.org/data/definitions/780.html>
- CWE 940 (Improper Verification of Source of a Communication Channel) - <https://cwe.mitre.org/data/definitions/940.html>
- CWE 941 (Incorrectly Specified Destination in a Communication Channel) - <https://cwe.mitre.org/data/definitions/941.html>
