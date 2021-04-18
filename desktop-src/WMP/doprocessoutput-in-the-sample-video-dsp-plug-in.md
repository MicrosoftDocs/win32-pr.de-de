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
# <a name="doprocessoutput-in-the-sample-video-dsp-plug-in"></a><span data-ttu-id="0485c-108">DoProcess Output im Beispiel-Video-DSP-Plug-in</span><span class="sxs-lookup"><span data-stu-id="0485c-108">DoProcessOutput in the Sample Video DSP Plug-in</span></span>

<span data-ttu-id="0485c-109">Da ein Video DSP-Plug-in in der Regel mehrere Videoformate unterstützt, ist es praktisch, den Verarbeitungs Implementierungs Code in eine separate Funktion für jedes Format zu unterteilen.</span><span class="sxs-lookup"><span data-stu-id="0485c-109">Because a video DSP plug-in typically supports several video formats, it is convenient to separate the processing implementation code into a separate function for each format.</span></span> <span data-ttu-id="0485c-110">Dies bedeutet, dass die Implementierung von **DoProcess Output** für Video DSP-Plug-ins relativ einfach ist.</span><span class="sxs-lookup"><span data-stu-id="0485c-110">This means that the implementation of **DoProcessOutput** for video DSP plug-ins is relatively simple.</span></span>

<span data-ttu-id="0485c-111">Die-Implementierung im Sample-Plug-in testet zunächst, ob der Benutzer das Plug-in aktiviert hat.</span><span class="sxs-lookup"><span data-stu-id="0485c-111">The implementation in the sample plug-in first tests whether the user has enabled the plug-in.</span></span> <span data-ttu-id="0485c-112">Wenn das Plug-in deaktiviert ist, kopiert der Code die im Eingabepuffer bereitgestellten Daten in den Ausgabepuffer, ohne ihn zu ändern, wie im folgenden Code veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="0485c-112">If the plug-in is disabled, the code copies the data provided in the input buffer to the output buffer without changing it, as the following code demonstrates:</span></span>


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



<span data-ttu-id="0485c-113">Wenn das Plug-in aktiviert ist, führt der Code einfach eine Reihe von Überprüfungen für den untergeordneten **Typ** des Eingabemedien Typs aus, um das aktuelle Videoformat zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="0485c-113">If the plug-in is enabled, the code simply performs a series of checks on the input media type **subtype** member to determine the current video format.</span></span> <span data-ttu-id="0485c-114">Wenn eine Entsprechung gefunden wird, ruft der Code die entsprechende Verarbeitungs Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="0485c-114">When a match is found, the code calls the appropriate processing function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0485c-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0485c-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0485c-116">**Implementieren eines Video DSP-Plug-ins**</span><span class="sxs-lookup"><span data-stu-id="0485c-116">**Implementing a Video DSP Plug-in**</span></span>](implementing-a-video-dsp-plug-in.md)
</dt> </dl>

 

 




