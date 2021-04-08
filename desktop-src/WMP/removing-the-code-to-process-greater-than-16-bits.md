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
# <a name="removing-the-code-to-process-greater-than-16-bits"></a><span data-ttu-id="2dbb2-109">Entfernen des Codes für die Verarbeitung von mehr als 16 Bits</span><span class="sxs-lookup"><span data-stu-id="2dbb2-109">Removing the Code to Process Greater than 16 Bits</span></span>

<span data-ttu-id="2dbb2-110">Da in diesem Beispiel nur 8-Bit-oder 16-Bit-Audiodaten verarbeitet werden, müssen Sie den Code in **Cecho:: validatemediatype** so ändern, dass der DMO \_ E- \_ Typ \_ \_ für Medientypen mit mehr als 16 Bits nicht akzeptiert wird.</span><span class="sxs-lookup"><span data-stu-id="2dbb2-110">Because this sample only processes 8-bit or 16-bit audio, you need to modify the code in **CEcho::ValidateMediaType** to return DMO\_E\_TYPE\_NOT\_ACCEPTED for media types greater than 16 bits.</span></span> <span data-ttu-id="2dbb2-111">Um dies zu erreichen, müssen Sie den Code im switch-Block ändern, der Formate von Type Wave \_ Format \_ Extensible testet.</span><span class="sxs-lookup"><span data-stu-id="2dbb2-111">To accomplish this, you must change the code in the switch block that tests formats of type WAVE\_FORMAT\_EXTENSIBLE.</span></span> <span data-ttu-id="2dbb2-112">Ersetzen Sie den Assistenten Code durch den folgenden Beispielcode:</span><span class="sxs-lookup"><span data-stu-id="2dbb2-112">Replace the wizard code with the following example code:</span></span>


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



<span data-ttu-id="2dbb2-113">Als nächstes löschen oder kommentieren Sie die Code Abschnitte in **DoProcess Output** aus, die High-Bit-Auflösungs Audiodaten verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="2dbb2-113">Next, delete or comment out the sections of code in **DoProcessOutput** that handle high bit resolution audio.</span></span> <span data-ttu-id="2dbb2-114">Dabei handelt es sich um die Abschnitte, die mit Groß-/Kleinschreibung und 32 beginnen.</span><span class="sxs-lookup"><span data-stu-id="2dbb2-114">These are the sections that begin with case 24 and case 32.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2dbb2-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2dbb2-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2dbb2-116">**Implementieren von Cecho::D oprocess Output**</span><span class="sxs-lookup"><span data-stu-id="2dbb2-116">**Implementing CEcho::DoProcessOutput**</span></span>](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




