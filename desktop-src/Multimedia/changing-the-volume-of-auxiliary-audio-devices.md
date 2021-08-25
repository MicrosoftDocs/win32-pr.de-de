---
title: Ändern des Volume of Auxiliary Audio-Devices
description: Ändern des Volume of Auxiliary Audio-Devices
ms.assetid: d7357900-132c-4758-8bc2-a890aead01c3
keywords:
- Waveformaudio, Ändern der Zusätzlichen Audiogerätelautstärke
- Ändern der Zusätzlichen Audiogerätelautstärke
- Zusatzaudio, Gerätevolume ändern
- Zusätzliche Audioschnittstelle
- Zusätzliche Audiogeräte, Lautstärke ändern
- Zusatzaudio, Schnittstelle
- Hilfsaudio, Geräte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e02ca4ceaf8e8a8b2f84ea69be437145f0f92b375904a0121c17abc7870fa831
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808110"
---
# <a name="changing-the-volume-of-auxiliary-audio-devices"></a>Ändern des Volume of Auxiliary Audio-Devices

Windows bietet die folgenden Funktionen zum Abfragen und Festlegen des Volumes für zusätzliche Audiogeräte.



| Funktion                             | Beschreibung                                                                    |
|--------------------------------------|--------------------------------------------------------------------------------|
| [**auxGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetvolume) | Ruft die aktuelle Volumeeinstellung des angegebenen zusätzlichen Ausgabegeräts ab. |
| [**auxSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-auxsetvolume) | Legt das Volume des angegebenen Hilfsausgabegeräts fest.                      |



 

Nicht alle zusätzlichen Audiogeräte unterstützen Volumeänderungen. Einige Geräte können einzelne Volumeänderungen sowohl auf dem linken als auch auf dem rechten Kanal unterstützen.

Die Lautstärke wird in einem Doubleword-Wert angegeben, wie bei den Waveform-Audio- und DEN VOLUME CONTROL-Funktionen. Wenn das Audioformat Stereo ist, geben die oberen 16 Bits die relative Lautstärke des rechten Kanals und die unteren 16 Bits das relative Volumen des linken Kanals an. Für Geräte, die die Lautstärkesteuerung des linken und rechten Kanals nicht unterstützen, geben die unteren 16 Bits die Volumeebene an, und die oberen 16 Bits werden ignoriert.

Werte auf Volumeebene reichen von 0x0 (Stille) bis zu 0xFFFF (maximales Volumen) und werden logarithmisch interpretiert. Die wahrgenommene Volumeerhöhung ist identisch, wenn die Volumeebene von 0x5000 auf 0x6000 erhöht wird, wie von 0x4000 auf 0x5000.

 

 