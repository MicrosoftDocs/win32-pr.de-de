---
description: Listet die Rückgabewerte für Zertifikat-und Zertifikats Vertrauensstellungen auf. Diese Werte sind in der Header Datei Winerror. h enthalten.
ms.assetid: f7d1bdcb-8e4f-493f-ad3c-9d4b9d21436b
title: Rückgabewerte für Zertifikate und Vertrauens Stellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e17f170c7c3aa1ac0839323b9a52767a101dd3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751073"
---
# <a name="certificate-and-trust-return-values"></a>Rückgabewerte für Zertifikate und Vertrauens Stellungen

In der folgenden Tabelle sind die Rückgabewerte für Zertifikats-und Zertifikat Vertrauensstellungen aufgeführt. Diese Werte sind in der Header Datei Winerror. h enthalten.



| Name                            | BESCHREIBUNG                                                                                                                    | Wert      |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------|------------|
| Zertifikat \_ E \_ kritisch               | Ein Zertifikat enthält eine unbekannte Erweiterung, die als "kritisch" gekennzeichnet ist.                                                         | 0x800b0105 |
| \_ \_ Ungültiger Name für CERT E \_          | Der Name des Zertifikats ist ungültig. Der Name ist entweder nicht in der Liste zulässiger Namen enthalten, oder er wurde explizit ausgeschlossen. | 0x800b0114 |
| \_ \_ ungültige \_ Richtlinie für CERT E        | Das Zertifikat weist eine ungültige Richtlinie auf.                                                                                | 0x800b0113 |
| CERT \_ E \_ issuerchaining         | Ein übergeordnetes Element eines bestimmten Zertifikats hat dieses untergeordnete Zertifikat tatsächlich nicht ausgestellt.                                                  | 0x800b0107 |
| Zertifikat \_ E \_ falsch formatiert              | Ein Zertifikat fehlt oder hat einen leeren Wert für ein wichtiges Feld, z. b. einen Antragsteller-oder Aussteller Namen.                       | 0x800b0108 |
| Zertifikat- \_ E \_ pathlenconst           | Eine Pfadlängeneinschränkung in der Zertifizierungskette wurde nicht eingehalten.                                                         | 0x800b0104 |
| Zertifikat \_ E \_ nicht treudca            | Eine Zertifizierungs Kette wurde ordnungsgemäß verarbeitet, aber eines der Zertifizierungsstellen Zertifikate wird vom Richtlinien Anbieter nicht als vertrauenswürdig eingestuft.               | 0x800b0112 |
| Crypt \_ E \_ keine \_ Sperr \_ Überprüfung | Die Sperrfunktion konnte die Sperrung für das Zertifikat nicht überprüfen.                                                    | 0x80092012 |
| fehlerhafter \_ \_ \_ Digest           | Die digitale Signatur des Objekts konnte nicht überprüft werden.                                                                            | 0x80096010 |
| Trust \_ E \_ Basic- \_ Einschränkungen    | Die Basiseinschränkungserweiterung eines Zertifikats wurde nicht beachtet.                                                         | 0x80096019 |
| Trust- \_ E- \_ CERT- \_ Signatur       | Die Signatur des Zertifikats kann nicht überprüft werden.                                                                           | 0x80096004 |
| \_e- \_ counter- \_ Signatur Geber Vertrauen       | Eine der gegen Signaturen war nicht gültig.                                                                                   | 0x80096003 |
| \_ \_ explizites \_ Misstrauen Vertrauen    | Das Zertifikat wurde vom Benutzer explizit als nicht vertrauenswürdig gekennzeichnet.                                                                | 0x800b0111 |
| \_ \_ Finanz \_ Kriterium Vertrauen   | Das Zertifikat entspricht nicht oder enthält die Authenticode-Finanz Erweiterungen.                                                | 0x8009601e |
| Trust \_ E \_ No \_ Signatur Geber \_ CERT      | Das Zertifikat für den Signatur Geber der Nachricht ist ungültig oder wurde nicht gefunden.                                                       | 0x80096002 |
| \_ \_ System \_ Fehler bei Vertrauensstellung         | Während der Überprüfung der Vertrauenswürdigkeit ist ein Fehler auf Systemebene aufgetreten.                                                                           | 0x80096001 |
| Vertrauensstellung \_ E \_ Zeit \_ Stempel           | Die Zeitstempelsignatur bzw. das Zertifikat konnte nicht überprüft werden oder ist fehlerhaft.                                                 | 0x80096005 |



 

 

 



