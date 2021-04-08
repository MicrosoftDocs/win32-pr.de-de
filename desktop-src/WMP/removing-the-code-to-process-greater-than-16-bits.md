---
title: Entfernen des Codes für die Verarbeitung von mehr als 16 Bits
description: Entfernen des Codes für die Verarbeitung von mehr als 16 Bits
ms.assetid: 90c165e1-bc77-42a5-878d-056762c62991
keywords:
- Windows Media Player-Plug-ins, Echo Sample DoProcess Output-Methode
- Plug-ins, Echo Sample DoProcess Output-Methode
- Plug-Ins für die digitale Signalverarbeitung, Echo Sample DoProcess Output-Methode
- DSP-Plug-ins, Echo Sample DoProcess Output-Methode
- Echo DSP-Plug-in-Beispiel, DoProcess Output-Methode
- Echo DSP-Plug-in-Beispiel, Verarbeitung von mehr als 16 Bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec33332ee332d0ca7b615844ba8ad5cd7b00eb2f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856183"
---
# <a name="removing-the-code-to-process-greater-than-16-bits"></a>Entfernen des Codes für die Verarbeitung von mehr als 16 Bits

Da in diesem Beispiel nur 8-Bit-oder 16-Bit-Audiodaten verarbeitet werden, müssen Sie den Code in **Cecho:: validatemediatype** so ändern, dass der DMO \_ E- \_ Typ \_ \_ für Medientypen mit mehr als 16 Bits nicht akzeptiert wird. Um dies zu erreichen, müssen Sie den Code im switch-Block ändern, der Formate von Type Wave \_ Format \_ Extensible testet. Ersetzen Sie den Assistenten Code durch den folgenden Beispielcode:


```C++
case WAVE_FORMAT_EXTENSIBLE:
    {
         // Sample size is greater than 16-bit or is multichannel.
        WAVEFORMATEXTENSIBLE *pWaveXT = (WAVEFORMATEXTENSIBLE *) pWave;

        if (KSDATAFORMAT_SUBTYPE_PCM != pWaveXT->SubFormat)
        {
            return DMO_E_TYPE_NOT_ACCEPTED;
        }
    }
    break;

```



Als nächstes löschen oder kommentieren Sie die Code Abschnitte in **DoProcess Output** aus, die High-Bit-Auflösungs Audiodaten verarbeiten. Dabei handelt es sich um die Abschnitte, die mit Groß-/Kleinschreibung und 32 beginnen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren von Cecho::D oprocess Output**](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




