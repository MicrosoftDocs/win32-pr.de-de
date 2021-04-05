---
title: Variablen zum Durchführen der Verarbeitung
description: Variablen zum Durchführen der Verarbeitung
ms.assetid: 02f194ea-cac0-410f-886f-2894dd6971c8
keywords:
- Windows Media Player-Plug-ins, Echo Sample DoProcess Output-Methode
- Plug-ins, Echo Sample DoProcess Output-Methode
- Plug-Ins für die digitale Signalverarbeitung, Echo Sample DoProcess Output-Methode
- DSP-Plug-ins, Echo Sample DoProcess Output-Methode
- Echo DSP-Plug-in-Beispiel, DoProcess Output-Methode
- Echo DSP-Plug-in-Beispiel, Verarbeiten von Variablen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e44f044aee6d893fba97cf921360444ec43db871
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711106"
---
# <a name="variables-to-perform-processing"></a>Variablen zum Durchführen der Verarbeitung

Die Element Variablen zur Behandlung des Verzögerungs Puffers mit **Byte** Mengen. Dabei handelt es sich um **Byte** Zeiger und eine ganze Zahl, die die Anzahl von Bytes speichert. Dies eignet sich ideal für die Verarbeitung von 8-Bit-Audiodaten, da eine 8-Bit-Stichprobe problemlos in ein Byte Arbeitsspeicher passt. Bei der Verarbeitung von 16-Bit-Audiodaten ist es jedoch bequemer, diese in **kurze** Zeiger zu konvertieren, sodass die Verarbeitung zwei Bytes gleichzeitig durchführen kann.

Im folgenden Beispielcode werden die neuen 16-Bit-Zeiger zugeordnet und eine Zeiger Variable hinzugefügt, in der die Adresse des Endes des Verzögerungs Puffers gespeichert wird. Fügen Sie Sie direkt vor dem Einstiegspunkt der Schleife in den Abschnitt "Case 16" ein:


```C++
// Store local pointers to the delay buffer.
short    *pwDelayPointer = (short *)m_pbDelayPointer;
short    *pwDelayBuffer = (short *) m_pbDelayBuffer;
// Store the address of the last word of the delay buffer.
short    *pwEOFDelayBuffer = (short *)(m_pbDelayBuffer + m_cbDelayBuffer - sizeof(short)); 

```



Der Code für die 8-Bit-Verarbeitung weist auch eine Variable zu, in der die Adresse des Endes des Verzögerungs Puffers gespeichert wird. Durch das Speichern dieses Werts können Sie leicht testen, ob der Puffer Zeiger für verschiebbare Verzögerung das Ende des Verzögerungs Puffers erreicht hat. Der folgende Beispielcode berechnet den-Wert:


```C++
// Store the address of the end of the delay buffer.
BYTE * pbEOFDelayBuffer = (m_pbDelayBuffer + m_cbDelayBuffer - sizeof(BYTE));

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren von Cecho::D oprocess Output**](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




