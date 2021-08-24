---
title: Ändern des internen SYNTHESIZER-Volumes
description: Ändern des internen SYNTHESIZER-Volumes
ms.assetid: 75ab7ff5-f394-4a79-8dcc-f4eef434a36e
keywords:
- Instrument Digital Interface (KEYBOARD), interne Synthesizer
- KEYBOARD (Keyboard Instrument Digital Interface), interne Synthesizer
- Wiedergeben von WAVE-Dateien, interne Synthesizer
- interne SYNTHESIZE-Synthesizer
- Instrument Digital Interface (KEYBOARD), Ändern der Lautstärke
- SIGNATURE (Keyboard Instrument Digital Interface), Ändern der Lautstärke
- Wiedergeben vonUMK-Dateien, Ändern des Volumes
- Ändern desUMK-Volumes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 646c7e17a7e8c0a6902e26dd8bbfdf8eb89c39297fdacdf062749d8c47a3d487
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808210"
---
# <a name="changing-internal-midi-synthesizer-volume"></a>Ändern des internen SYNTHESIZER-Volumes

Windows stellt die folgenden Funktionen zum Abrufen und Festlegen der Volumeebene interner SYNTHESIZEr-Geräte zur Verfügung:



| Wert                                        | Bedeutung                                                                       |
|----------------------------------------------|-------------------------------------------------------------------------------|
| [**ohneGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetvolume) | Ruft die Volumeebene des angegebenen internen SYNTHESIZER-Geräts ab. |
| [**ohneSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-midioutsetvolume) | Legt die Volumeebene des angegebenen internen SYNTHESIZER-Geräts fest.      |



 

Nicht alle DEST-Ausgabegeräte unterstützen Volumeänderungen. Einige Geräte können einzelne Volumeänderungen sowohl im linken als auch im rechten Kanal unterstützen. Informationen zum Bestimmen, ob ein bestimmtes Gerät Volumeänderungen unterstützt, finden Sie unter [Abfragen von OUTPUT-Ausgabegeräten.](querying-midi-output-devices.md)

Sofern Ihre Anwendung nicht als Masteranwendung zur Volumesteuerung konzipiert ist (stellt dem Benutzer die Lautstärkesteuerung für alle Audiogeräte in einem System zur Verfügung), sollten Sie ein Audiogerät öffnen, bevor Sie dessen Lautstärke ändern. Sie sollten auch die Volumeebene überprüfen, bevor Sie sie ändern, und die Volumeebene so bald wie möglich auf die vorherige Ebene wiederherstellen.

Volume wird als Doublewordwert angegeben. Die oberen 16 Bits geben das relative Volumen des rechten Kanals an, und die unteren 16 Bits geben das relative Volumen des linken Kanals an.

Für Geräte, die keine einzelnen Volumeänderungen sowohl im linken als auch im rechten Kanal unterstützen, geben die unteren 16 Bits die Volumeebene an, und die oberen 16 Bits werden ignoriert. Die Werte für die Volumeebene reichen von 0x0 (Stille) bis 0xFFFF (maximale Lautstärke) und werden logarithmisch interpretiert. Der wahrgenommene Anstieg des Volumens ist identisch, wenn die Volumeebene von 0x5000 auf 0x6000 erhöht wird, wie von 0x4000 auf 0x5000.

 

 