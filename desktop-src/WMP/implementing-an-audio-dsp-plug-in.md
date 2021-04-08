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
# <a name="implementing-an-audio-dsp-plug-in"></a><span data-ttu-id="4a8fd-113">Implementieren eines audiodsp-Plug-ins</span><span class="sxs-lookup"><span data-stu-id="4a8fd-113">Implementing an Audio DSP Plug-in</span></span>

<span data-ttu-id="4a8fd-114">Zum Erstellen eines Windows Media Player DSP-Plug-ins, das Audiodaten verarbeitet, müssen Sie den Beispielcode in der Funktion mit dem Namen " **DoProcess Output**" ändern.</span><span class="sxs-lookup"><span data-stu-id="4a8fd-114">To create a Windows Media Player DSP plug-in that processes audio, you'll need to modify the sample code in the function named **DoProcessOutput**.</span></span> <span data-ttu-id="4a8fd-115">" **DoProcess Output** " wird jedes Mal aufgerufen, wenn Windows Media Player " **imediaobject" (:P rocess Output**) erfolgreich aufruft.</span><span class="sxs-lookup"><span data-stu-id="4a8fd-115">**DoProcessOutput** is called each time Windows Media Player successfully calls **IMediaObject::ProcessOutput**.</span></span> <span data-ttu-id="4a8fd-116">Dabei handelt es sich um die Funktion, die die Verarbeitungs Tasks für digitales Signal ausführt, die das akustische Ergebnis liefern, das das DSP-Plug-in erzeugt.</span><span class="sxs-lookup"><span data-stu-id="4a8fd-116">It is the function that performs the digital signal processing tasks that produce the audible result that the DSP plug-in is intended to produce.</span></span>

<span data-ttu-id="4a8fd-117">Die Verarbeitung eines Audiostreams ähnelt der Behandlung eines zeitlich festgelegten Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="4a8fd-117">Processing an audio stream is like handling a timed event.</span></span> <span data-ttu-id="4a8fd-118">" **DoProcess Output** " wird wiederholt und in bestimmten Intervallen aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="4a8fd-118">**DoProcessOutput** will be called repeatedly and at specific intervals.</span></span> <span data-ttu-id="4a8fd-119">Jedes Mal, wenn der Code ausgeführt wird, muss eine bestimmte Anzahl von Daten Bytes verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="4a8fd-119">Each time your code executes, it will need to process a specific number of bytes of data.</span></span> <span data-ttu-id="4a8fd-120">" **DoProcess Output** " enthält die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="4a8fd-120">**DoProcessOutput** contains the following parameters:</span></span>



| <span data-ttu-id="4a8fd-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a8fd-121">Parameter</span></span>          | <span data-ttu-id="4a8fd-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4a8fd-122">Description</span></span>                                                                                                             |
|--------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a8fd-123">*pboutputdata*</span><span class="sxs-lookup"><span data-stu-id="4a8fd-123">*pbOutputData*</span></span>     | <span data-ttu-id="4a8fd-124">Dies ist ein **Byte** Zeiger auf den Puffer, in dem Ihre Implementierung von **DoProcess Output** die verarbeiteten Daten kopieren muss.</span><span class="sxs-lookup"><span data-stu-id="4a8fd-124">This is a **BYTE** pointer to the buffer where your implementation of **DoProcessOutput** must copy its processed data.</span></span> |
| <span data-ttu-id="4a8fd-125">*pbinputdata*</span><span class="sxs-lookup"><span data-stu-id="4a8fd-125">*pbInputData*</span></span>      | <span data-ttu-id="4a8fd-126">Dies ist ein konstanter **Byte** Zeiger auf den Puffer, der die zu verarbeitenden Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="4a8fd-126">This is a constant **BYTE** pointer to the buffer that contains the data to be processed.</span></span>                               |
| <span data-ttu-id="4a8fd-127">*cbbytestoprocess*</span><span class="sxs-lookup"><span data-stu-id="4a8fd-127">*cbBytesToProcess*</span></span> | <span data-ttu-id="4a8fd-128">Dies ist ein **DWORD** -Wert, der die Anzahl der Bytes im zu verarbeitenden Eingabepuffer enthält.</span><span class="sxs-lookup"><span data-stu-id="4a8fd-128">This is a **DWORD** value that contains a count of the number of bytes in the input buffer to be processed.</span></span>             |



 

<span data-ttu-id="4a8fd-129">Die folgenden Abschnitte enthalten ausführliche Informationen dazu, wie Sie den vom Windows Media Player-Plug-in-Assistenten generierten Code ändern können, um ein eigenes audiodsp-Plug-in zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="4a8fd-129">The following sections provide details about how to modify the code generated by the Windows Media Player Plug-in Wizard to create your own audio DSP plug-in:</span></span>

-   [<span data-ttu-id="4a8fd-130">Implementieren von DoProcess Output</span><span class="sxs-lookup"><span data-stu-id="4a8fd-130">Implementing DoProcessOutput</span></span>](implementing-doprocessoutput.md)
-   [<span data-ttu-id="4a8fd-131">Hinzufügen von Eigenschaften zum Sample audiodsp-Plug-in</span><span class="sxs-lookup"><span data-stu-id="4a8fd-131">Adding Properties to the Sample Audio DSP Plug-in</span></span>](adding-properties-to-the-sample-audio-dsp-plug-in.md)
-   [<span data-ttu-id="4a8fd-132">Implementieren der Eigenschaften Seite für ein DSP-Plug-in</span><span class="sxs-lookup"><span data-stu-id="4a8fd-132">Implementing the Property Page for a DSP Plug-in</span></span>](implementing-the-property-page-for-a-dsp-plug-in.md)
-   [<span data-ttu-id="4a8fd-133">Ändern der Sample audiodsp-Plug-in-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4a8fd-133">Changing the Sample Audio DSP Plug-in Property</span></span>](changing-the-sample-audio-dsp-plug-in-property.md)
-   [<span data-ttu-id="4a8fd-134">Informationen über Diskontinuität</span><span class="sxs-lookup"><span data-stu-id="4a8fd-134">About Discontinuity</span></span>](about-discontinuity.md)
-   [<span data-ttu-id="4a8fd-135">Informationen zum Zuordnen von Streamingressourcen</span><span class="sxs-lookup"><span data-stu-id="4a8fd-135">About Allocating Streaming Resources</span></span>](about-allocating-streaming-resources.md)

## <a name="related-topics"></a><span data-ttu-id="4a8fd-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4a8fd-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a8fd-137">**Informationen zu DSP-Plug-ins**</span><span class="sxs-lookup"><span data-stu-id="4a8fd-137">**About DSP Plug-ins**</span></span>](about-dsp-plug-ins.md)
</dt> </dl>

 

 




