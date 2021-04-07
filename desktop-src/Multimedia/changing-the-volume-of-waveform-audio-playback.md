---
title: Ändern des Umfangs der Waveform-Audio Wiedergabe
description: Ändern des Umfangs der Waveform-Audio Wiedergabe
ms.assetid: 814daa35-7905-47a2-ab08-29f20493af1e
keywords:
- Wellenform-Audiodatei, Ändern des Wiedergabe Volumens
- Waveform-Audioschnittstelle, Ändern des Wiedergabe Volumens
- Wellenform-Audiodatei, Wiedergabe Volume
- Waveform-Audioschnittstelle, Wiedergabe Volume
- Ändern des Waveform-Audiowiedergabe-Volumes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89f972b5bd8e6f0d4a0d7d5964f164429c5632b0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103727313"
---
# <a name="changing-the-volume-of-waveform-audio-playback"></a>Ändern des Umfangs der Waveform-Audio Wiedergabe

Windows stellt die folgenden Funktionen bereit, um die Volumeebene von Waveform-audioausgabegeräten abzufragen und festzulegen.



| Funktion                                     | BESCHREIBUNG                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------|
| [**waveoutgetvolume**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetvolume) | Ruft die aktuelle Volumeebene des angegebenen Waveform-Audioausgabegeräts ab. |
| [**waveoutsetvolume**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetvolume) | Legt die Volumeebene des angegebenen Waveform-Audioausgabegeräts fest.              |



 

Nicht alle Waveform-Audiogeräte unterstützen volumeänderungen. Einige Geräte unterstützen die einzelnen volumesteuerelemente sowohl im linken als auch im rechten Kanal. Informationen zum Bestimmen der volumesteuerungsfunktionen von Waveform-Audiogeräten finden Sie unter [Geräte und Datentypen](devices-and-data-types.md).

Einige Anwendungen ermöglichen es dem Benutzer, das Volume für alle Audiogeräte in einem System zu steuern. (Viele Anwendungen dieses Typs verwenden die Audiomixer-Dienste. Weitere Informationen finden Sie unter [Audiomixer](audio-mixers.md).) Wenn Ihre Anwendung nicht in der Lage ist, eine solche Art von Master Volume zu steuern, sollten Sie vor dem Ändern des Volumes ein Audiogerät öffnen. Sie sollten auch die Volumeebene Abfragen, bevor Sie Sie ändern und die Volumeebene so bald wie möglich auf die vorherige Ebene wiederherstellen.

Das Volume wird in einem Double Word-Wert angegeben. Wenn das Audioformat Stereo ist, geben die oberen 16 Bits das relative Volume des rechten Kanals und die unteren 16 Bits das relative Volume des linken Kanals an. Bei Geräten, die die volumesteuerung auf der linken und rechten Channel nicht unterstützen, geben die unteren 16 Bits die Volumeebene an, und die oberen 16 Bits werden ignoriert.

Werte auf Volumeebene reichen von 0x0 (Ruhe) bis 0xFFFF (maximales Volume) und werden logarithmisch interpretiert. Die wahrgenommene Volumenzunahme ist gleich, wenn die Volumeebene von 0x5.000 auf 0x6000 erhöht wird, da Sie zwischen 0x4000 und 0x5.000 liegt.

 

 