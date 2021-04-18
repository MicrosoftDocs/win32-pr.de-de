---
title: DoProcess Output im Beispiel-Video-DSP-Plug-in
description: DoProcess Output im Beispiel-Video-DSP-Plug-in
ms.assetid: 67536e35-a049-49c8-bd89-fad1fab37e6c
keywords:
- Windows Media Player-Plug-ins, videodsp
- Plug-ins, videodsp
- Plug-Ins für die digitale Signalverarbeitung, DoProcess Output
- DSP-Plug-ins, DoProcess Output
- Video DSP-Plug-ins, DoProcess Output
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff3bc844890930209a1c6007213d3c466f0cd15b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340413"
---
# <a name="doprocessoutput-in-the-sample-video-dsp-plug-in"></a>DoProcess Output im Beispiel-Video-DSP-Plug-in

Da ein Video DSP-Plug-in in der Regel mehrere Videoformate unterstützt, ist es praktisch, den Verarbeitungs Implementierungs Code in eine separate Funktion für jedes Format zu unterteilen. Dies bedeutet, dass die Implementierung von **DoProcess Output** für Video DSP-Plug-ins relativ einfach ist.

Die-Implementierung im Sample-Plug-in testet zunächst, ob der Benutzer das Plug-in aktiviert hat. Wenn das Plug-in deaktiviert ist, kopiert der Code die im Eingabepuffer bereitgestellten Daten in den Ausgabepuffer, ohne ihn zu ändern, wie im folgenden Code veranschaulicht:


```C++
// Test whether the plug-in has been disabled by the user.
if (!m_bEnabled)
{
    // Just copy the data without changing it. You should
    // also do any necessary format conversion here.
    memcpy(pbOutputData, pbInputData, m_dwBufferSize);
    *cbBytesProcessed = m_dwBufferSize;

    return S_OK;
}

```



Wenn das Plug-in aktiviert ist, führt der Code einfach eine Reihe von Überprüfungen für den untergeordneten **Typ** des Eingabemedien Typs aus, um das aktuelle Videoformat zu bestimmen. Wenn eine Entsprechung gefunden wird, ruft der Code die entsprechende Verarbeitungs Funktion auf.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren eines Video DSP-Plug-ins**](implementing-a-video-dsp-plug-in.md)
</dt> </dl>

 

 




