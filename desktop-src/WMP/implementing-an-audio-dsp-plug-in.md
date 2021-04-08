---
title: Implementieren eines audiodsp-Plug-ins
description: Implementieren eines audiodsp-Plug-ins
ms.assetid: 93ff0c45-f418-443d-8fba-c0a62f6e4e80
keywords:
- Windows Media Player-Plug-ins, audiodsp
- Plug-ins, audiodsp
- Plug-Ins für die digitale Signalverarbeitung, Implementieren von Code
- DSP-Plug-ins, Implementieren von Code
- Plug-Ins für die digitale Signalverarbeitung, Ändern von Beispielcode
- DSP-Plug-ins, Ändern von Beispielcode
- Plug-Ins für die digitale Signalverarbeitung, audioimplementierung
- DSP-Plug-ins, audioimplementierung
- audiodsp-Plug-ins, Implementieren von Code
- audiodsp-Plug-ins, Ändern von Beispielcode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdde8e7f00fc9ea3ad9bb8b7adb2d0a8bfba6b32
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037279"
---
# <a name="implementing-an-audio-dsp-plug-in"></a>Implementieren eines audiodsp-Plug-ins

Zum Erstellen eines Windows Media Player DSP-Plug-ins, das Audiodaten verarbeitet, müssen Sie den Beispielcode in der Funktion mit dem Namen " **DoProcess Output**" ändern. " **DoProcess Output** " wird jedes Mal aufgerufen, wenn Windows Media Player " **imediaobject" (:P rocess Output**) erfolgreich aufruft. Dabei handelt es sich um die Funktion, die die Verarbeitungs Tasks für digitales Signal ausführt, die das akustische Ergebnis liefern, das das DSP-Plug-in erzeugt.

Die Verarbeitung eines Audiostreams ähnelt der Behandlung eines zeitlich festgelegten Ereignisses. " **DoProcess Output** " wird wiederholt und in bestimmten Intervallen aufgerufen. Jedes Mal, wenn der Code ausgeführt wird, muss eine bestimmte Anzahl von Daten Bytes verarbeitet werden. " **DoProcess Output** " enthält die folgenden Parameter:



| Parameter          | BESCHREIBUNG                                                                                                             |
|--------------------|-------------------------------------------------------------------------------------------------------------------------|
| *pboutputdata*     | Dies ist ein **Byte** Zeiger auf den Puffer, in dem Ihre Implementierung von **DoProcess Output** die verarbeiteten Daten kopieren muss. |
| *pbinputdata*      | Dies ist ein konstanter **Byte** Zeiger auf den Puffer, der die zu verarbeitenden Daten enthält.                               |
| *cbbytestoprocess* | Dies ist ein **DWORD** -Wert, der die Anzahl der Bytes im zu verarbeitenden Eingabepuffer enthält.             |



 

Die folgenden Abschnitte enthalten ausführliche Informationen dazu, wie Sie den vom Windows Media Player-Plug-in-Assistenten generierten Code ändern können, um ein eigenes audiodsp-Plug-in zu erstellen:

-   [Implementieren von DoProcess Output](implementing-doprocessoutput.md)
-   [Hinzufügen von Eigenschaften zum Sample audiodsp-Plug-in](adding-properties-to-the-sample-audio-dsp-plug-in.md)
-   [Implementieren der Eigenschaften Seite für ein DSP-Plug-in](implementing-the-property-page-for-a-dsp-plug-in.md)
-   [Ändern der Sample audiodsp-Plug-in-Eigenschaft](changing-the-sample-audio-dsp-plug-in-property.md)
-   [Informationen über Diskontinuität](about-discontinuity.md)
-   [Informationen zum Zuordnen von Streamingressourcen](about-allocating-streaming-resources.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zu DSP-Plug-ins**](about-dsp-plug-ins.md)
</dt> </dl>

 

 




