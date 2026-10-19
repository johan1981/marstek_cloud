# Development workflow — Marstek Cloud Home Assistant integratie

**Repository:** `johan1981/marstek_cloud` (**publiek**)  
**Standaardbranch:** `main` (GitHub, 19 oktober 2026)

## Technische basis
- `README.md`: custom Home Assistant-integratie die via een externe Marstek-cloud-API sensoren voedt.
- `custom_components/marstek_cloud/manifest.json`: Home Assistant-domein `marstek_cloud`, Python/async en `aiohttp`.
- Dit is **geen PHP-, Laravel- of Ubuntu-webapp-project**. Geen `php artisan`, Composer of SFTP-workflow verzinnen.

## Werkomgeving
| Onderdeel | Afspraken |
|---|---|
| Git en ontwikkelmap | Lokale ontwikkelmachine/pad **te verifiëren**; branches vanaf `main`, daarna lokale tracking en `git pull`. |
| Runtime/test | Home Assistant; daadwerkelijke testinstallatie/versie en validatieprocedure per opdracht bevestigen. |
| Deploy/install | README noemt kopiëren naar `custom_components` en integratie-herstart bij installatie; **niet automatisch** reboot/reload/reconfigure van een werkend Home Assistant-systeem. |
| Publieke repository | Geen tokens, wachtwoorden, accountgegevens, apparaatserienummers of privélogbestanden committen. |

## Algemene afspraken

Lees vóór iedere ontwikkeltaak [de Livome AI-samenwerkingsstandaard](AI_COLLABORATION_STANDARD.md), dit document en de bestaande projectbronnen. Eerst huidige default branch, code, tests, implementatie en eventuele openstaande wijzigingen onderzoeken.

- Werk voor nieuwe wijzigingen op een eigen `feature/...`- of `fix/...`-branch vanaf de actuele default branch. Remote featurebranches lokaal met upstream/tracking ophalen; daarna is op de juiste getrackte branch normaal `git pull` voldoende.
- Git in de **daadwerkelijk gebruikte lokale ontwikkelterminal**. Git op een server alleen als deze repository aantoonbaar zo is ingericht; kopieer niet automatisch de Livome Intern PhpStorm/SFTP-werkwijze.
- AI kan, indien toegestaan, op de remote featurebranch committen. **Geen PR of merge zonder uitdrukkelijke toestemming van Johan.**
- Geen ongevraagde dependencies, resets, schemawijzigingen, service-restarts, credentials of deployacties. Projectgegevens en reeds goedgekeurde assets beschermen.
- Geef Johan precies de noodzakelijke commando's met het juiste omgevingslabel, niet universeel Laravel/Ubuntu-commando's.
- Doe of vraag passende regressie- en functionele tests. Vermeld onbevestigde omgevingsinformatie expliciet als **nog te verifiëren**.

## Eerste lokale checkout van nieuwe remote branch
`git fetch origin` en `git switch --track origin/<featurebranch>` in de juiste lokale Git-terminal; daarna alleen `git pull`. Na geautoriseerde merge: `git switch main`, `git pull`.

## Testinvariant
Test foutafhandeling zonder live systemen ongevraagd te verstoren. Een echte Home Assistant-herstart of herauthenticatie alleen als expliciet afgestemd.
