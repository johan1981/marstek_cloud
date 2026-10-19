# AGENTS.md — Marstek Cloud Home Assistant-integratie

## Werkwijze voor AI-assistenten

Bij **ieder ontwikkelverzoek**, ook in een nieuwe chat:

1. Controleer de actuele standaardbranch, relevante code en tests van deze repository.
2. Lees [de gedeelde AI-samenwerkingsstandaard](docs/AI_COLLABORATION_STANDARD.md) en [de repository-workflow](docs/DEVELOPMENT_WORKFLOW.md).
3. Lees de hieronder genoemde **inhoudelijke projectbronnen**; die gaan boven de generieke samenwerkingstekst voor productinhoud, beveiliging en canon.
4. Maak geen ongevraagde setup, reset, migratie, package-installatie, productie-deploy of ingrijpende refactor.
5. Voor wijzigingen: featurebranch, upstream/tracking, kleine diff, gerichte tests en **geen PR/merge zonder expliciete toestemming van Johan**.
6. Geef de benodigde commando's per werkelijk gebruikte omgeving: lokale Git-terminal, eventuele server, browser/game/testomgeving. Geen stappen verzinnen.

**Belangrijk:** workflow van Livome Intern (PhpStorm op Windows → SFTP → Ubuntu) is **niet automatisch** de workflow van deze repo. Controleer de eigen workflow; onbekende onderdelen blijven te verifiëren.

## Projectspecifiek

- [README.md](README.md) en `custom_components/marstek_cloud/` vormen de huidige technische basis.
- Publieke Home Assistant/Python-integratie, **geen PHP-project**.
- Nooit credentials/tokens/serials in code, voorbeelden of commits.
- Een echte Home Assistant-herstart, cloud-authenticatie, servicecall of configuratiewijziging vereist expliciete afstemming.
