---
description: Listet die Zertifikat- und Zertifikatvertrauens-Rückgabewerte auf. Diese Werte sind in der Headerdatei Winerror.h enthalten.
ms.assetid: f7d1bdcb-8e4f-493f-ad3c-9d4b9d21436b
title: Rückgabewerte für Zertifikate und Vertrauensstellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf575df785160682c132f38ccc280bb8b9377b15b64ed3efda163c68c1ef52e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127240"
---
# <a name="certificate-and-trust-return-values"></a>Rückgabewerte für Zertifikate und Vertrauensstellungen

In der folgenden Tabelle sind die Rückgabewerte für zertifikats- und zertifikatvertrauensstellung aufgeführt. Diese Werte sind in der Headerdatei Winerror.h enthalten.



| Name                            | Beschreibung                                                                                                                    | Wert      |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------|------------|
| CERT \_ E \_ CRITICAL               | Ein Zertifikat enthält eine unbekannte Erweiterung, die als "kritisch" gekennzeichnet ist.                                                         | 0x800B0105 |
| ZERTIFIKAT \_ E \_ UNGÜLTIGER \_ NAME          | Das Zertifikat hat einen ungültigen Namen. Der Name ist entweder nicht in der Liste zulässiger Namen enthalten, oder er wurde explizit ausgeschlossen. | 0x800B0114 |
| ZERTIFIKAT \_ E \_ UNGÜLTIGE \_ RICHTLINIE        | Das Zertifikat verfügt über eine ungültige Richtlinie.                                                                                | 0x800B0113 |
| CERT \_ E \_ ISSUERCHAINING         | Ein übergeordnetes Element eines bestimmten Zertifikats hat dieses untergeordnete Zertifikat nicht ausgestellt.                                                  | 0x800B0107 |
| ZERTIFIKAT \_ E \_ FALSCH FORMATIERT              | Ein Zertifikat fehlt oder enthält einen leeren Wert für ein wichtiges Feld, z. B. einen Betreff- oder Ausstellernamen.                       | 0x800B0108 |
| CERT \_ E \_ PATHLENCONST           | Eine Pfadlängeneinschränkung in der Zertifizierungskette wurde nicht eingehalten.                                                         | 0x800B0104 |
| CERT \_ E \_ UNTRUSTEDCA            | Eine Zertifizierungskette wurde ordnungsgemäß verarbeitet, aber eines der Zertifizierungsstellenzertifikate wird vom Richtlinienanbieter nicht als vertrauenswürdig eingestuft.               | 0x800B0112 |
| VERSCHLÜSSELUNG \_ E \_ KEINE \_ \_ SPERRPRÜFUNG | Die Sperrfunktion konnte die Sperrung für das Zertifikat nicht überprüfen.                                                    | 0x80092012 |
| TRUST \_ E \_ BAD \_ DIGEST           | Die digitale Signatur des Objekts konnte nicht überprüft werden.                                                                            | 0x80096010 |
| TRUST \_ E \_ \_ BASIC-EINSCHRÄNKUNGEN    | Die Basiseinschränkungserweiterung eines Zertifikats wurde nicht beachtet.                                                         | 0x80096019 |
| \_ \_ E-ZERTIFIKATSIGNATUR \_ VERTRAUEN       | Die Signatur des Zertifikats kann nicht überprüft werden.                                                                           | 0x80096004 |
| TRUST \_ E \_ COUNTER \_ SIGNER       | Eine der Zählersignaturen war ungültig.                                                                                   | 0x80096003 |
| TRUST \_ E \_ EXPLICIT \_ DISTRUST    | Das Zertifikat wurde vom Benutzer explizit als nicht vertrauenswürdig gekennzeichnet.                                                                | 0x800B0111 |
| VERTRAUEN \_ E \_ FINANZIELLE \_ KRITERIEN   | Das Zertifikat erfüllt die Authenticode-Finanzerweiterungen nicht oder enthält sie nicht.                                                | 0x8009601E |
| TRUST \_ E \_ NO \_ SIGNER \_ CERT      | Das Zertifikat für den Signator der Nachricht ist ungültig oder wurde nicht gefunden.                                                       | 0x80096002 |
| TRUST \_ E \_ SYSTEM \_ ERROR         | Während der Überprüfung der Vertrauenswürdigkeit ist ein Fehler auf Systemebene aufgetreten.                                                                           | 0x80096001 |
| TRUST \_ E \_ TIME \_ STAMP           | Die Zeitstempelsignatur bzw. das Zertifikat konnte nicht überprüft werden oder ist fehlerhaft.                                                 | 0x80096005 |



 

 

 



