---
title: Zusammenfassung der Karten und MELDUNGEN
description: Zusammenfassung der Karten und MELDUNGEN
ms.assetid: cd0ec7b0-2ba1-4e75-b85c-f5b95ac9dfeb
keywords:
- Instruments Instrument Digital Interface (INSTRUMENTS), MAPPer
- INSTRUMENTS (Digitale Schnittstelle des Instrumentierers), MAPPER
- MAPPer, Kanalzuordnung
- MAPPer, Patch maps
- MAPPer, Schlüsselzuordnungen
- Kanalzuordnung
- Patch maps (Patchzuordnungen)
- Schlüsselzuordnungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a89c23d6326e19cb5680906155d5ee2e8dbcc32735fabd8625658410ef4ddfa0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781850"
---
# <a name="summary-of-maps-and-midi-messages"></a>Zusammenfassung der Karten und MELDUNGEN

Im Folgenden sind die Statusbytes für DIE MELDUNGEN und die Zuordnungstypen angegeben, die sich auf jede Nachricht auswirken.



| STATUS VON STATUS | Beschreibung               | Kartentypen                |
|-------------|---------------------------|--------------------------|
| 0x80-0x8F   | Hinweis deaktiviert                  | Kanalzuordnungen, Schlüsselzuordnungen   |
| 0x90-0x9F   | Hinweis zu                    | Kanalzuordnungen, Schlüsselzuordnungen   |
| 0xA0-0xAF   | Polyphone-key aftertouch | Kanalzuordnungen, Schlüsselzuordnungen   |
| 0xB0-0xBF   | Steuern der Änderung            | Kanalzuordnungen, Patch maps |
| 0xC0-0xCF   | Programmänderung            | Kanalzuordnungen, Patch maps |
| 0xD0-0xDF   | Channel aftertouch        | Kanalzuordnungen             |
| 0xE0-0xEF   | Tonhöhenänderung         | Kanalzuordnungen             |
| 0xF0-0xFF   | System                    | Nicht zugeordnet               |



 

-   Die vier Bits mit hoher Ordnung stellen den Statuswert dar. Die vier Bits mit niedriger Reihenfolge stellen die Kanalinformationen dar.
-   Patch Maps wirken sich nur auf Controller 7 (Hauptvolume) aus.
-   Systemmeldungen werden an alle Geräte gesendet, die in einer Kanalzuordnung aufgeführt sind.

 

 




