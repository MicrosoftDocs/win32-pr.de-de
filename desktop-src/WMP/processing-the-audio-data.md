---
title: Verarbeiten der Audiodaten
description: Verarbeiten der Audiodaten
ms.assetid: ba41e3f4-d991-4da6-9091-7a7e42622e76
keywords:
- Windows Media Player-Plug-Ins,Echo-Beispiel-DoProcessOutput-Methode
- Plug-Ins,Echo-Beispielmethode "DoProcessOutput"
- Plug-Ins für die digitale Signalverarbeitung,Echo-Beispielmethode "DoProcessOutput"
- DSP-Plug-Ins,Echo-Beispielmethode "DoProcessOutput"
- Echo DSP-Plug-In-Beispiel, DoProcessOutput-Methode
- Echo DSP-Plug-In-Beispiel, Audiodaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678e1debd586017bfbe748d4f2bed6d17607afcbe2719b5e3ecba8cabf667af6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118334483"
---
# <a name="processing-the-audio-data"></a>Verarbeiten der Audiodaten

Die Standardimplementierung von **DoProcessOutput** beginnt mit dem Abrufen eines Zeigers auf eine gültige **WAVEFORMATEX-Struktur,** genau wie in **AllocateStreamingResources.** Anschließend werden die Informationen in dieser Struktur verwendet, um die Anzahl der Stichproben im Eingabepuffer zu berechnen, die auf die Verarbeitung warten. Der folgende Code ist aus der Standardimplementierung:


```C++
// Get a pointer to the valid WAVEFORMATEX structure
// for the current media type.
WAVEFORMATEX *pWave = ( WAVEFORMATEX * ) m_mtInput.pbFormat;

// Calculate the number of samples to process.
DWORD dwSamplesToProcess = (*cbBytesProcessed / pWave->nBlockAlign) * pWave->nChannels;

```



Anschließend überprüft der Code den **wBitsPerSample-Member,** um die Bittiefe der Audiodatei zu bestimmen. Dieser Wert wird in einer switch-Anweisung verwendet, um eine separate Verarbeitung für 8-Bit- und 16-Bit-Audio zu ermöglichen.

## <a name="differences-between-8-bit-and-16-bit-audio"></a>Unterschiede zwischen 8-Bit- und 16-Bit-Audio

Es gibt wichtige Unterschiede zwischen 8-Bit- und 16-Bit-Audio. Daher unterscheiden sich die Verarbeitungsroutinen zum Erstellen des Echoeffekts. Die beiden Formate unterscheiden sich auf folgende Weise:

-   Jedes Format hat eine andere Stichprobengröße: 8-Bit-Stichproben belegen jeweils ein Byte Arbeitsspeicher, während 16-Bit-Stichproben jeweils zwei Bytes belegen.
-   Jedes Format stellt die Audioamplitude unterschiedlich dar. 8-Bit-Audio wird durch eine ganze Zahl ohne Vorzeichen mit einem Bereich von 0 bis 255 dargestellt. Der Wert 128 stellt die Stille dar. 16-Bit-Audio wird durch eine ganze Zahl mit Vorzeichen mit einem Bereich von -32768 bis 32767 dargestellt. Der Wert 0 (null) stellt die Stille dar.

Während der Prozess der Erstellung des Echoeffekts für jedes Format grundsätzlich identisch ist, müssen sich die Details geringfügig unterscheiden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren von CEcho::D oProcessOutput**](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




