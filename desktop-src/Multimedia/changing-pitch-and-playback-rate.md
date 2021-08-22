---
title: Ändern der Tonhöhe und Wiedergaberate
description: Ändern der Tonhöhe und Wiedergaberate
ms.assetid: f0f5249b-ae2a-4f17-80ee-575f9f7963a7
keywords:
- Waveform-Audio, Tonhöhe
- Waveform-Audioschnittstelle, Tonhöhe
- Waveform-Audio, Wiedergaberate
- Waveform-Audioschnittstelle, Wiedergaberate
- Waveform-Audio, Ändern der Tonhöhe
- Waveform-Audio-Schnittstelle, Ändern der Tonhöhe
- Waveform-Audio, Ändern der Wiedergaberate
- Waveform-Audioschnittstelle, Ändern der Wiedergaberate
- Ändern der Wiedergaberate von Waveform-Audio
- Ändern der Tonhöhe von Waveform-Audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 006788c286476434a7ca2a3d5b79dbd6c4d8af431d74ffb4a00e03a7357777f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941278"
---
# <a name="changing-pitch-and-playback-rate"></a>Ändern der Tonhöhe und Wiedergaberate

Einige Waveform-Audio-Ausgabegeräte können die Tonhöhe und die Wiedergaberate von Waveform-Audiodaten variieren. Nicht alle Waveform-Audiogeräte unterstützen Änderungen an Tonhöhe und Wiedergaberate. Informationen dazu, wie Sie bestimmen können, ob ein bestimmtes Waveform-Audio-Gerät Änderungen an Tonhöhe und Wiedergaberate unterstützt, finden Sie unter [Geräte und Datentypen.](devices-and-data-types.md)

Die Unterschiede zwischen der Änderung der Tonhöhe und der Wiedergaberate lauten wie folgt:

-   Die Wiedergaberate wird vom Gerätetreiber geändert und erfordert keine spezielle Hardware. Die Abtastrate wird nicht geändert, aber der Treiber interpoliert, indem Stichproben übersprungen oder synthetisiert werden. Wenn die Wiedergaberate beispielsweise um den Faktor 2 geändert wird, überspringt der Treiber alle anderen Stichproben.
-   Zum Ändern der Tonhöhe ist spezielle Hardware erforderlich. Die Wiedergaberate und die Abtastrate werden nicht geändert.

Windows stellt die folgenden Funktionen zum Abfragen und Festlegen von Waveform-Audio-Tonhöhe und Wiedergaberaten zur Verfügung.



| Funktion                                                 | Beschreibung                                                                 |
|----------------------------------------------------------|-----------------------------------------------------------------------------|
| [**waveOutGetPitch**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetpitch)               | Ruft die Tonhöhe für das angegebene Waveform-Audio-Ausgabegerät ab.         |
| [**waveOutGetPlaybackRate**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetplaybackrate) | Ruft die Wiedergaberate für das angegebene Waveform-Audio-Ausgabegerät ab. |
| [**waveOutSetPitch**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetpitch)               | Legt die Tonhöhe für das angegebene Waveform-Audio-Ausgabegerät fest.              |
| [**waveOutSetPlaybackRate**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetplaybackrate) | Legt die Wiedergaberate für das angegebene Waveform-Audio-Ausgabegerät fest.      |



 

Die Tonhöhen- und Wiedergaberaten werden durch einen Faktor geändert, der mit einer festen Punktzahl angegeben wird, die in einen Doublewordwert gepackt ist. Die oberen 16 Bits geben den ganzzahligen Teil der Zahl an. Die unteren 16 Bits geben den Bruchteil an. Beispielsweise wird der Wert 1.5 als 0x00018000L dargestellt. Der Wert 0,75 wird als 0x0000C000L dargestellt. Der Wert 1,0 (0x00010000) bedeutet, dass die Tonhöhe oder Wiedergaberate unverändert bleibt.

 

 