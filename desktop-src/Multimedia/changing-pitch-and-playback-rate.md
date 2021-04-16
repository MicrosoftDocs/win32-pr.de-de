---
title: Ändern der Tonhöhe und der Wiedergabe Rate
description: Ändern der Tonhöhe und der Wiedergabe Rate
ms.assetid: f0f5249b-ae2a-4f17-80ee-575f9f7963a7
keywords:
- Wellenform-Audiodaten, Tonhöhe
- Waveform-Audioschnittstelle, Tonhöhe
- Wellenform-Audiodatei, Wiedergabe Rate
- Waveform-Audioschnittstelle, Wiedergabe Rate
- Wellenform-Audiodaten, Ändern der Tonhöhe
- Waveform-Audioschnittstelle, Ändern der Tonhöhe
- Wellenform-Audiodatei, Ändern der Wiedergabe Rate
- Waveform-Audioschnittstelle, Ändern der Wiedergabe Rate
- Ändern der Geschwindigkeit der Waveform-Audiowiedergabe
- Ändern der Waveform-audiotonhöhe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99eec4e29ec1c38cddb5a5f92f27643e2c9c3e6c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104473124"
---
# <a name="changing-pitch-and-playback-rate"></a>Ändern der Tonhöhe und der Wiedergabe Rate

Einige Waveform-Audioausgabegeräte können die Tonhöhe und die Wiedergabe Rate von Waveform-Audiodaten variieren. Nicht alle Waveform-Audiogeräte unterstützen Änderungen an der Tonhöhe und der Wiedergabe Rate. Informationen dazu, wie Sie feststellen können, ob ein bestimmtes Waveform-Audiogerät Änderungen an der Tonhöhe und Wiedergabe Rate unterstützt, finden Sie unter [Geräte und Datentypen](devices-and-data-types.md).

Die Unterschiede zwischen dem Ändern der Tonhöhe und der Wiedergabe Rate lauten wie folgt:

-   Das Ändern der Wiedergabe Rate wird vom Gerätetreiber durchgeführt, und es ist keine spezielle Hardware erforderlich. Die Samplingrate wird nicht geändert, aber der Treiber interpoliert, indem er Beispiele übersprungen oder synthegiert. Wenn die Wiedergabe Rate z. b. um den Faktor 2 geändert wird, überspringt der Treiber alle anderen Stichproben.
-   Zum Ändern der Tonhöhe ist spezielle Hardware erforderlich. Die Wiedergabe Rate und die Stichprobenrate werden nicht geändert.

Windows stellt die folgenden Funktionen zum Abfragen und Festlegen von Waveform-Audiodarstellung und Wiedergabe Raten bereit.



| Funktion                                                 | BESCHREIBUNG                                                                 |
|----------------------------------------------------------|-----------------------------------------------------------------------------|
| [**waveoutgetpitch**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetpitch)               | Ruft die Tonhöhe für das angegebene Waveform-Audioausgabegerät ab.         |
| [**waveoutgetplaybackrate**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetplaybackrate) | Ruft die Wiedergabe Rate für das angegebene Waveform-Audioausgabegerät ab. |
| [**waveoutsetpitch**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetpitch)               | Legt die Tonhöhe für das angegebene Waveform-Audioausgabegerät fest.              |
| [**waveoutsetplaybackrate**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetplaybackrate) | Legt die Wiedergabe Rate für das angegebene Waveform-Audioausgabegerät fest.      |



 

Die Tonhöhe und die Wiedergabe Raten werden um einen Faktor geändert, der durch eine in einen Double Word-Wert gepackte fest Komma Zahl angegeben ist. Die oberen 16 Bits geben den ganzzahligen Teil der Zahl an. die unteren 16 Bits geben den Bruch Teil an. Beispielsweise wird der Wert 1,5 als 0x00018000l dargestellt. Der Wert 0,75 wird als 0x0000c000l dargestellt. Der Wert 1,0 (0x00010000 bis) bedeutet, dass die Tonhöhe oder Wiedergabe Rate unverändert ist.

 

 