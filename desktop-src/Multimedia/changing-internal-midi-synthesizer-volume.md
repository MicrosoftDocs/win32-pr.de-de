---
title: Ändern des internen MIDI-synthesizervolumes
description: Ändern des internen MIDI-synthesizervolumes
ms.assetid: 75ab7ff5-f394-4a79-8dcc-f4eef434a36e
keywords:
- Digital Instrumentation Digital Interface (MIDI), interne Synthesizer
- MIDI (Digital Instrumentation Digital Interface), interne Synthesizer
- Abspielen von MIDI-Dateien, internen Synthesizern
- Interne MIDI-Synthesizer
- Digital Instrumentation Digital Interface (MIDI), Ändern des Volumes
- MIDI (Digital Instrumentation Digital Interface), Ändern des Volumes
- Abspielen von MIDI-Dateien, Ändern des Volumes
- Ändern des MIDI-Volumes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2369b13483ce6fa45d82ee177282a0de5e86538e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948711"
---
# <a name="changing-internal-midi-synthesizer-volume"></a>Ändern des internen MIDI-synthesizervolumes

Windows stellt die folgenden Funktionen zum Abrufen und Festlegen der Volumeebene interner Geräte mit dem Typ "MIDI" bereit:



| Wert                                        | Bedeutung                                                                       |
|----------------------------------------------|-------------------------------------------------------------------------------|
| [**midioutgetvolume**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetvolume) | Ruft die Volumeebene des angegebenen internen MIDI-Synthesizer-Geräts ab. |
| [**midioutsetvolume**](/windows/win32/api/mmeapi/nf-mmeapi-midioutsetvolume) | Legt die Volumeebene des angegebenen internen MIDI-Synthesizer-Geräts fest.      |



 

Nicht alle auf den Geräten mit der Ausgabe von "MIDI" ausgebene Einige Geräte können Änderungen einzelner Volumes sowohl auf dem linken als auch auf dem rechten Kanal unterstützen. Informationen dazu, wie Sie feststellen können, ob ein bestimmtes Gerät volumeänderungen unterstützt, finden Sie unter [Abfragen von MIDI-Ausgabegeräten](querying-midi-output-devices.md).

Sie sollten ein Audiogerät öffnen, bevor Sie das Volume ändern können, es sei denn, Ihre Anwendung ist als Master-Volumen Steuerungsanwendung konzipiert (bietet dem Benutzer eine volumesteuerung für alle Audiogeräte in einem System). Sie sollten auch die Volumeebene überprüfen, bevor Sie Sie ändern und die Volumeebene so bald wie möglich auf die vorherige Ebene wiederherstellen.

Das Volume wird als Double Word-Wert angegeben. Die oberen 16 Bits geben das relative Volume des rechten Kanals an, und die unteren 16 Bits geben das relative Volume des linken Kanals an.

Bei Geräten, die keine einzelnen volumeänderungen auf dem linken und rechten Kanal unterstützen, geben die unteren 16 Bits die Volumeebene an, und die oberen 16 Bits werden ignoriert. Werte für die Volumeebene liegen zwischen 0x0 (Ruhe) und 0xFFFF (maximales Volume) und werden logarithmisch interpretiert. Die wahrgenommene Volumenzunahme ist gleich, wenn die Volumeebene von 0x5.000 auf 0x6000 erhöht wird, da Sie zwischen 0x4000 und 0x5.000 liegt.

 

 