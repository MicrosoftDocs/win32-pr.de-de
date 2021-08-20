---
title: Audioanforderungen der Stufe 2
description: Audioanforderungen der Stufe 2
ms.assetid: 203648f2-9d20-438d-975b-b80e50b0fb9b
keywords:
- Multimedia-PC (MPC), Ebene 2
- MPC (Multimedia-PC), Ebene 2
- Multimedia PC Marketing Council, Ebene 2
- MPC Level 2, Audioanforderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a2bc9398a25ac916352f41ad2ddc2325820354d1c7beb511b03b27004fadd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118139831"
---
# <a name="level-2-audio-requirements"></a>Audioanforderungen der Stufe 2

Das Audiosubsystem eines PCs, der die Level 2-Spezifikation erfüllt, enthält folgende Elemente:

-   Ein CD-ROM-Treiber mit CD-DA-Ausgaben (Red Book-Audio) und Lautstärkeregler
-   Eine 16-Bit-DAC mit den folgenden Merkmalen:
    -   Lineare PCM-Stichprobenentnahme (Pulse Code Pulse)
    -   DMA- oder FIFO-Pufferübertragungsfunktion mit Interrupt bei leerem Puffer
    -   Obligatorische Stichprobenraten von 44,1, 22,05 und 11,025 kHz
    -   Stereokanäle
    -   CPU-Bandbreitenauslastung von 10 Prozent oder weniger bei der Ausgabe von Audiodaten mit einer Abtastrate von 22,05 oder 11,025 kHz oder eine CPU-Bandbreite von 15 Prozent oder weniger bei der Ausgabe von Audiodaten mit einer Abtastrate von 44,1 kHz

<!-- -->

-   Ein 16-Bit-ADC mit den folgenden Merkmalen:
    -   Lineare PCM-Stichprobenentnahme
    -   DMA- oder FIFO-Pufferübertragungsfunktion mit Interrupt bei leerem Puffer
    -   Obligatorische Stichprobenraten von 44,1, 22,05 und 11,025 kHz
    -   Mikrofoneingabe

<!-- -->

-   Interne Synthesizerfunktionen mit Multivoice, multitimbral, sechs gleichzeitigen Noten und zwei gleichzeitigen percussiven Notizen
-   Internes Kombinieren mit den folgenden Funktionen:
    -   Kann drei Audioquellen kombinieren und die Ausgabe als Stereosignal auf Zeilenebene im Hintergrundbereich darstellen.
    -   Bei der Kombination von Quellen handelt es sich um CD Red Book-Audio, Synthesizer und DAC.
    -   Jede Mischungsquelle verfügt über eine 3-Bit-Volumesteuerung mit einem logarithmischen Taper.

 

 




