---
title: Zusammenfassung der Maps-und MIDI-Meldungen
description: Zusammenfassung der Maps-und MIDI-Meldungen
ms.assetid: cd0ec7b0-2ba1-4e75-b85c-f5b95ac9dfeb
keywords:
- Digital Instrumentation Digital Interface (MIDI), MIDI-Mapper
- MIDI (Digital Instrumentation Digital Interface), MIDI-Mapper
- MIDI-Mapper, Kanal Zuordnung
- MIDI-Mapper, patchmaps
- MIDI-Mapper, Schlüssel Zuordnungen
- Kanal Zuordnung
- patchzuordnungen
- Schlüssel Zuordnungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd962f848343ea493204d494943a99eedcc56a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713302"
---
# <a name="summary-of-maps-and-midi-messages"></a>Zusammenfassung der Maps-und MIDI-Meldungen

Im folgenden finden Sie die Status Bytes für MIDI-Nachrichten und die Zuordnungs Typen, die jede Nachricht beeinflussen.



| Status von MIDI | BESCHREIBUNG               | Kartentypen                |
|-------------|---------------------------|--------------------------|
| 0x80-0x8F   | Notiz aus                  | Kanal Zuordnungen, Schlüssel Zuordnungen   |
| 0x90-0x9F   | Hinweis zu                    | Kanal Zuordnungen, Schlüssel Zuordnungen   |
| 0xa0-0xaf   | Polyonic-Schlüssel-afterberührungs | Kanal Zuordnungen, Schlüssel Zuordnungen   |
| 0xb0-0xBF   | Steuerelement Änderung            | Kanal Zuordnungen, patchmaps |
| 0xc0-0xCF   | Programmänderung            | Kanal Zuordnungen, patchmaps |
| 0xd0-0xDF   | Kanal-afterberührungs        | Kanal Zuordnungen             |
| 0xe0-0xEF   | Änderung der ebenumkurve         | Kanal Zuordnungen             |
| 0xF 0-0xFF   | System                    | Nicht zugeordnet               |



 

-   Die hochwertigen vier Bits stellen den Statuswert dar. Die nieder wertigen vier Bits stellen die Kanalinformationen dar.
-   Patchmaps wirken sich nur auf Controller 7 (Haupt Volume) aus.
-   System Meldungen werden an alle Geräte gesendet, die in einer Kanal Zuordnung aufgeführt sind.

 

 




