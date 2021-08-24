---
title: Ändern des Volumens der Waveform-Audio Wiedergabe
description: Ändern des Volumens der Waveform-Audio Wiedergabe
ms.assetid: 814daa35-7905-47a2-ab08-29f20493af1e
keywords:
- Waveform-Audio, Ändern der Wiedergabemenge
- Waveform-Audio-Schnittstelle, Ändern der Wiedergabemenge
- Waveform-Audio, Wiedergabevolumen
- Waveform-Audio-Schnittstelle, Wiedergabevolumen
- Ändern des Wiedergabevolumens von Waveform-Audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e59bca6dbc168d2c327c46e4d934d4abb3afa73cc8ef2cae8b1a6c283bd92c81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807990"
---
# <a name="changing-the-volume-of-waveform-audio-playback"></a>Ändern des Volumens der Waveform-Audio Wiedergabe

Windows stellt die folgenden Funktionen zum Abfragen und Festlegen der Lautstärkeebene von Waveform-Audio-Ausgabegeräten zur Verfügung.



| Funktion                                     | Beschreibung                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------|
| [**waveOutGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetvolume) | Ruft die aktuelle Lautstärkeebene des angegebenen Waveform-Audio-Ausgabegeräts ab. |
| [**waveOutSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetvolume) | Legt die Lautstärkeebene des angegebenen Waveform-Audio-Ausgabegeräts fest.              |



 

Nicht alle Waveform-Audiogeräte unterstützen Volumeänderungen. Einige Geräte unterstützen die individuelle Volumesteuerung sowohl im linken als auch im rechten Kanal. Informationen zum Bestimmen der Lautstärkesteuerungsfunktionen von Waveform-Audiogeräten finden Sie unter [Geräte und Datentypen.](devices-and-data-types.md)

Einige Anwendungen ermöglichen es dem Benutzer, das Volume für alle Audiogeräte in einem System zu steuern. (Viele Anwendungen dieses Typs verwenden die Audiomixerdienste. Weitere Informationen finden Sie unter [Audiomixer.)](audio-mixers.md) Sofern Ihre Anwendung nicht in der Lage ist, diese Art von Master-Volumesteuerung zu verwenden, sollten Sie ein Audiogerät öffnen, bevor Sie das Volume ändern. Sie sollten auch die Volumeebene abfragen, bevor Sie sie ändern, und die Volumeebene so bald wie möglich auf die vorherige Ebene wiederherstellen.

Volume wird in einem Doublewordwert angegeben. Wenn das Audioformat Stereo ist, geben die oberen 16 Bits das relative Volumen des rechten Kanals und die unteren 16 Bits die relative Lautstärke des linken Kanals an. Für Geräte, die die Lautstärkesteuerung nach links und rechts nicht unterstützen, geben die unteren 16 Bits die Volumeebene an, und die oberen 16 Bits werden ignoriert.

Werte auf Volumeebene reichen von 0x0 (Stille) bis 0xFFFF (maximale Lautstärke) und werden logarithmisch interpretiert. Der wahrgenommene Volumenanstieg ist identisch, wenn die Volumeebene von 0x5000 auf 0x6000 erhöht wird, wie von 0x4000 auf 0x5000.

 

 