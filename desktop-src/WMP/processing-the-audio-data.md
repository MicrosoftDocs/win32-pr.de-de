---
title: Verarbeiten der Audiodaten
description: Verarbeiten der Audiodaten
ms.assetid: ba41e3f4-d991-4da6-9091-7a7e42622e76
keywords:
- Windows Media Player-Plug-ins, Echo Sample DoProcess Output-Methode
- Plug-ins, Echo Sample DoProcess Output-Methode
- Plug-Ins für die digitale Signalverarbeitung, Echo Sample DoProcess Output-Methode
- DSP-Plug-ins, Echo Sample DoProcess Output-Methode
- Echo DSP-Plug-in-Beispiel, DoProcess Output-Methode
- Echo DSP-Plug-in-Beispiel, Audiodaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc14acb99aed20825ff970025363c6a795a0c8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337596"
---
# <a name="processing-the-audio-data"></a>Verarbeiten der Audiodaten

Die Standard Implementierung von " **DoProcess Output** " beginnt mit dem Abrufen eines Zeigers auf eine gültige **WaveFormatEx** -Struktur, wie dies in "" von "" in "" von "" **zugeordnet** wurde. Anschließend werden die Informationen in dieser Struktur verwendet, um die Anzahl der Stichproben im Eingabepuffer zu berechnen, die auf die Verarbeitung warten. Der folgende Code ist aus der Standard Implementierung:


```C++
// Get a pointer to the valid WAVEFORMATEX structure
// for the current media type.
WAVEFORMATEX *pWave = ( WAVEFORMATEX * ) m_mtInput.pbFormat;

// Calculate the number of samples to process.
DWORD dwSamplesToProcess = (*cbBytesProcessed / pWave->nBlockAlign) * pWave->nChannels;

```



Anschließend überprüft der Code den **wbitspersample** -Member, um die Bittiefe der Audiodatei zu bestimmen. Dieser Wert wird in einer Switch-Anweisung verwendet, um eine separate Verarbeitung für 8-Bit-und 16-Bit-Audiodaten bereitzustellen.

## <a name="differences-between-8-bit-and-16-bit-audio"></a>Unterschiede zwischen 8-Bit-und 16-Bit-Audiodaten

Es gibt wichtige Unterschiede zwischen 8-Bit-und 16-Bit-Audiodaten. Daher unterscheiden sich die Verarbeitungs Routinen zum Erstellen des Echo Effekts. Die beiden Formate unterscheiden sich wie folgt:

-   Jedes Format hat eine andere Stichprobengröße: 8-Bit-Samplings belegen jeweils ein Byte Arbeitsspeicher, während 16-Bit-Stichproben jeweils zwei Bytes belegen.
-   Jedes Format repräsentiert die Audioamplitude anders. 8-Bit-Audiodaten werden durch eine Ganzzahl ohne Vorzeichen mit einem Bereich von 0 bis 255 dargestellt. der Wert 128 stellt den Ruhe Wert dar. die 16-Bit-Audiodaten werden durch eine ganze Zahl mit Vorzeichen und einen Bereich von-32768 bis 32767 dargestellt. der Wert 0 (null) stellt den Ruhe Wert dar.

Während der Vorgang zum Erstellen des Echo Effekts für jedes Format grundsätzlich identisch ist, müssen sich die Details leicht unterscheiden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren von Cecho::D oprocess Output**](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




