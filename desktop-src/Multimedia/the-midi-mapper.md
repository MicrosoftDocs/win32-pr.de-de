---
title: DER MAPPER
description: DER MAPPER
ms.assetid: 92cffc67-b4a4-4807-94d2-02fbbdba5abf
keywords:
- Windows Multimedia, MAPPER
- Multimedia, MULTIMEDIA-Mapper
- Multimediaaudio, MAPPER
- Audio, MAPPER
- Instruments Instrument Digital Interface (INSTRUMENTS), MAPPer
- INSTRUMENTS (Digitale Schnittstelle des Instrumentierers), MAPPER
- MAPPer, About
- MAPPer, Source
- MAPPer, Destination
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a5becc117668964a584f29c311c3e3ac477f672085e837e28d7eecc595658d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805100"
---
# <a name="the-midi-mapper"></a>DER MAPPER

Die Standardpatchdienste des MAPPER-Mappers bieten geräteunabhängige WIEDERGABE von DATEIEN für Anwendungen. Die MAPPER-Datei KANN mit dem MCI-SEQUENCER oder mit low-level-OUTPUT-Diensten verwendet werden.

Sofern nicht anders angegeben, verwenden alle Verweise auf DIE CHANNEL-Nummern die logischen Kanalnummern 1 bis 16. Diese logischen Kanalnummern entsprechen den physischen Kanalnummern 0 bis 15, die tatsächlich Teil der SMS-Nachricht sind. Alle Verweise auf DIE PROGRAMMÄNDERUNG und Schlüsselwerte verwenden die physischen Werte 0 bis 127. Alle Zahlen sind dezimal, sofern nicht das Präfix "0x" vorangestellt ist. In diesem Fall sind sie hexadezimal.

In der Erläuterung des MAPPer-Ausdrucks verweist der Begriff *source* auf die Eingabeseite des MAPPer-Mappers. Der Begriff *Ziel* bezieht sich auf die Ausgabeseite des MAPPER-Mappers. Ein Quellkanal ist z. B. der CHANNELS-Kanal einer Nachricht, die an den CSV-Mapper gesendet wird, und ein Zielkanal der CHANNELS-Kanal einer Nachricht, die von der MAPPer-Datei an ein Ausgabegerät gesendet wird.

-   [MAPPer und Windows](the-midi-mapper-and-windows.md)
-   [DIE MAPPER-Architektur](the-midi-mapper-architecture.md)
-   [Die Kanalzuordnung](the-channel-map.md)
-   [Patch Karten](patch-maps.md)
-   [Der Volumeskalar](the-volume-scalar.md)
-   [Key Karten](key-maps.md)
-   [Zusammenfassung der Karten und MELDUNGEN](summary-of-maps-and-midi-messages.md)

 

 




