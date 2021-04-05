---
title: Ändern der Menge an zusätzlichen Audio-Devices
description: Ändern der Menge an zusätzlichen Audio-Devices
ms.assetid: d7357900-132c-4758-8bc2-a890aead01c3
keywords:
- Wellenform-Audiodatei, Ändern des zusätzlichen audiogerätevolumes
- Ändern des Volumes mit zusätzlichen Audiogeräten
- zusätzliches Audiomaterial, Ändern des Geräte Volumes
- hilfsaudioschnittstelle
- zusätzliche Audiogeräte, Ändern des Volumes
- zusätzliches Audiomaterial, Schnittstelle
- zusätzliches Audiogerät, Geräte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f80c499f18b60f0919214c91eeec834ed72c3e1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103727320"
---
# <a name="changing-the-volume-of-auxiliary-audio-devices"></a>Ändern der Menge an zusätzlichen Audio-Devices

Windows stellt die folgenden Funktionen zum Abfragen und Festlegen des Volumes für hilfaudiogeräte bereit.



| Funktion                             | BESCHREIBUNG                                                                    |
|--------------------------------------|--------------------------------------------------------------------------------|
| [**"auxgetvolume"**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetvolume) | Ruft die aktuelle volumeeinstellung des angegebenen zusätzlichen Ausgabegeräts ab. |
| [**"auxsetvolume"**](/windows/win32/api/mmeapi/nf-mmeapi-auxsetvolume) | Legt das Volume des angegebenen zusätzlichen Ausgabegeräts fest.                      |



 

Nicht alle zusätzlichen Audiogeräte unterstützen volumeänderungen. Einige Geräte können Änderungen einzelner Volumes sowohl auf der linken Seite als auch auf den rechten Kanälen unterstützen.

Das Volume wird in einem Double Word-Wert angegeben, wie mit den volumesteuerungfunktionen Waveform-Audiofunktionen und MIDI. Wenn das Audioformat Stereo ist, geben die oberen 16 Bits das relative Volume des rechten Kanals und die unteren 16 Bits das relative Volume des linken Kanals an. Bei Geräten, die die volumesteuerung auf der linken und rechten Channel nicht unterstützen, geben die unteren 16 Bits die Volumeebene an, und die oberen 16 Bits werden ignoriert.

Werte auf Volumeebene reichen von 0x0 (Ruhe) bis 0xFFFF (maximales Volume) und werden logarithmisch interpretiert. Die wahrgenommene Volumenzunahme ist gleich, wenn die Volumeebene von 0x5.000 auf 0x6000 erhöht wird, da Sie zwischen 0x4000 und 0x5.000 liegt.

 

 