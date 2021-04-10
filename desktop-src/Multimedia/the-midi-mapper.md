---
title: Der MIDI-Mapper
description: Der MIDI-Mapper
ms.assetid: 92cffc67-b4a4-4807-94d2-02fbbdba5abf
keywords:
- Windows Multimedia, MIDI-Mapper
- Multimedia, MIDI-Mapper
- Multimedia-Audiodatei, MIDI-Mapper
- Audiodatei, MIDI-Mapper
- Digital Instrumentation Digital Interface (MIDI), MIDI-Mapper
- MIDI (Digital Instrumentation Digital Interface), MIDI-Mapper
- MIDI-Mapper, Informationen
- MIDI-Mapper, Quelle
- MIDI-Mapper, Ziel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b360148c994c0ee6434fdf097ca5f393b23d49
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036788"
---
# <a name="the-midi-mapper"></a>Der MIDI-Mapper

Die Standard-patchdienste des MIDI-Mappers stellen eine geräteunabhängige Wiedergabe von MIDI-Dateien für-Anwendungen bereit. Der MIDI-Mapper kann mit dem MCI-System-und-System-oder-Ausgabe Dienst auf niedriger Ebene verwendet werden.

Sofern nicht anders angegeben, verwenden alle Verweise auf die-Nummer des-MIDI-Kanals die logischen Kanalzahlen 1 bis 16. Diese logischen channelnummern entsprechen den physischen Kanalzahlen 0 bis 15, die tatsächlich Teil der MIDI-Nachricht sind. Alle Verweise auf die Werte von "MIDI-Programm-ändern" und "Schlüssel" verwenden die physischen Werte 0 bis 127. Alle Zahlen sind Decimal, es sei denn, es ist ein Präfix "0x" vorangestellt. in diesem Fall sind Sie Hexadezimal

In der Erörterung der MIDI-Mapper bezieht sich der Begriff *Quelle* auf die Eingabe Seite des MIDI-Mappers. Der Begriff *Ziel* verweist auf die Ausgabe Seite des MIDI-Mappers. Ein quellchannel ist beispielsweise der MIDI-Kanal einer Nachricht, die an den MIDI-Mapper gesendet wird, und ein Zielchannel ist der MIDI-Kanal einer Nachricht, die von der MIDI-Mapper an ein Ausgabegerät gesendet wird.

-   [Der MIDI-Mapper und Windows](the-midi-mapper-and-windows.md)
-   [Die Architektur der MIDI-Mapper](the-midi-mapper-architecture.md)
-   [Die Kanal Zuordnung](the-channel-map.md)
-   [Patchzuordnungen](patch-maps.md)
-   [Volumeskalar](the-volume-scalar.md)
-   [Schlüssel Zuordnungen](key-maps.md)
-   [Zusammenfassung der Maps-und MIDI-Meldungen](summary-of-maps-and-midi-messages.md)

 

 




