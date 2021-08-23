---
title: DoProcessOutput im Beispielvideo-DSP-Plug-In
description: DoProcessOutput im Beispielvideo-DSP-Plug-In
ms.assetid: 67536e35-a049-49c8-bd89-fad1fab37e6c
keywords:
- Windows Media Player-Plug-Ins,Video-DSP
- Plug-Ins, Video-DSP
- Plug-Ins für die digitale Signalverarbeitung, DoProcessOutput
- DSP-Plug-Ins, DoProcessOutput
- Video-DSP-Plug-Ins, DoProcessOutput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b031ecddc4f7a1e4a83d4f8a7d8db3b975957789d7f887bf8b12438407624205
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680600"
---
# <a name="doprocessoutput-in-the-sample-video-dsp-plug-in"></a>DoProcessOutput im Beispielvideo-DSP-Plug-In

Da ein Video-DSP-Plug-In in der Regel mehrere Videoformate unterstützt, ist es praktisch, den Code für die Verarbeitungsimplementierung in eine separate Funktion für jedes Format zu trennen. Dies bedeutet, dass die Implementierung **von DoProcessOutput** für Video-DSP-Plug-Ins relativ einfach ist.

Die Implementierung im Beispiel-Plug-In testet zunächst, ob der Benutzer das Plug-In aktiviert hat. Wenn das Plug-In deaktiviert ist, kopiert der Code die im Eingabepuffer bereitgestellten Daten in den Ausgabepuffer, ohne sie zu ändern. Dies wird im folgenden Code veranschaulicht:


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



Wenn das Plug-In aktiviert ist, führt der Code einfach  eine Reihe von Überprüfungen für den Untertyp des Eingabemedientyps durch, um das aktuelle Videoformat zu bestimmen. Wenn eine Übereinstimmung gefunden wird, ruft der Code die entsprechende Verarbeitungsfunktion auf.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren eines Video-DSP-Plug-Ins**](implementing-a-video-dsp-plug-in.md)
</dt> </dl>

 

 




