---
title: Implementieren eines Audio-DSP-Plug-Ins
description: Implementieren eines Audio-DSP-Plug-Ins
ms.assetid: 93ff0c45-f418-443d-8fba-c0a62f6e4e80
keywords:
- Windows Media Player-Plug-Ins,Audio-DSP
- Plug-Ins, Audio-DSP
- Plug-Ins für die digitale Signalverarbeitung, Implementieren von Code
- DSP-Plug-Ins, Implementieren von Code
- Plug-Ins für die digitale Signalverarbeitung, Ändern des Beispielcodes
- DSP-Plug-Ins, Ändern von Beispielcode
- Plug-Ins für die digitale Signalverarbeitung, Audioimplementierung
- DSP-Plug-Ins, Audioimplementierung
- Audio-DSP-Plug-Ins, Implementieren von Code
- Audio-DSP-Plug-Ins, Ändern von Beispielcode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f18ca0aada7072ca7cd1c0796c3cd6770a9b45340a4d9f67a342944f4c22887
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118338641"
---
# <a name="implementing-an-audio-dsp-plug-in"></a>Implementieren eines Audio-DSP-Plug-Ins

Zum Erstellen eines Windows Media Player DSP-Plug-Ins, das Audiodaten verarbeitet, müssen Sie den Beispielcode in der Funktion **doProcessOutput ändern.** **DoProcessOutput** wird jedes Mal aufgerufen, wenn Windows Media Player **IMediaObject::P rocessOutput aufruft.** Es ist die Funktion, die die Verarbeitungsaufgaben für digitale Signale ausführt, die das akustische Ergebnis erzeugen, das das DSP-Plug-In erzeugen soll.

Die Verarbeitung eines Audiodatenstroms ist mit der Verarbeitung eines zeitierten Ereignisses gleich. **DoProcessOutput** wird wiederholt und in bestimmten Intervallen aufgerufen. Jedes Mal, wenn Ihr Code ausgeführt wird, muss er eine bestimmte Anzahl von Datenbytes verarbeiten. **DoProcessOutput enthält** die folgenden Parameter:



| Parameter          | BESCHREIBUNG                                                                                                             |
|--------------------|-------------------------------------------------------------------------------------------------------------------------|
| *pbOutputData*     | Dies ist ein **BYTE-Zeiger** auf den Puffer, in den Ihre Implementierung von **DoProcessOutput** die verarbeiteten Daten kopieren muss. |
| *pbInputData*      | Dies ist ein konstanter **BYTE-Zeiger** auf den Puffer, der die zu verarbeitenden Daten enthält.                               |
| *cbBytesToProcess* | Dies ist ein **DWORD-Wert,** der die Anzahl der Bytes im zu verarbeitenden Eingabepuffer enthält.             |



 

In den folgenden Abschnitten erfahren Sie, wie Sie den vom Windows Media Player-Plug-In-Assistenten generierten Code ändern, um Ihr eigenes Audio-DSP-Plug-In zu erstellen:

-   [Implementieren von DoProcessOutput](implementing-doprocessoutput.md)
-   [Hinzufügen von Eigenschaften zum Beispiel-Audio-DSP-Plug-In](adding-properties-to-the-sample-audio-dsp-plug-in.md)
-   [Implementieren der Eigenschaftenseite für ein DSP-Plug-In](implementing-the-property-page-for-a-dsp-plug-in.md)
-   [Ändern der Beispieleigenschaft des Audio-DSP-Plug-Ins](changing-the-sample-audio-dsp-plug-in-property.md)
-   [Informationen zur Diskontinuität](about-discontinuity.md)
-   [Informationen zum Zuordnen von Streamingressourcen](about-allocating-streaming-resources.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zu DSP-Plug-Ins**](about-dsp-plug-ins.md)
</dt> </dl>

 

 




