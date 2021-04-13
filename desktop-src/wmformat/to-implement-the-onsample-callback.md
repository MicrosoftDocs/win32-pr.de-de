---
title: So implementieren Sie den onsample-Rückruf
description: So implementieren Sie den onsample-Rückruf
ms.assetid: 83bce8ee-6ce8-4079-9c87-2314824b1946
keywords:
- Advanced Systems Format (ASF), Implementieren von OnStatus-Rückruf
- ASF (Advanced Systems Format), Implementieren von OnStatus-Rückruf
- Advanced Systems Format (ASF), OnStatus-Rückruf
- ASF (Advanced Systems Format), OnStatus-Rückruf
- Advanced Systems Format (ASF), asynchrone Leser
- ASF (Advanced Systems Format), asynchrone Leser
- asynchrone Leser, Implementieren des OnStatus-Rückrufs
- OnStatus-Rückruf Methode, implementieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2f19e81df5ee4769e1353c299a14626cb1a9aed
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104314513"
---
# <a name="to-implement-the-onsample-callback"></a><span data-ttu-id="f6384-111">So implementieren Sie den onsample-Rückruf</span><span class="sxs-lookup"><span data-stu-id="f6384-111">To Implement the OnSample Callback</span></span>

<span data-ttu-id="f6384-112">Der asynchrone Reader stellt Beispiele für die steuernde Anwendung in der Präsentationszeit-Reihenfolge bereit, indem Aufrufe an die [**iwmreadercallback:: onsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) -Rückruf Methode erfolgt.</span><span class="sxs-lookup"><span data-stu-id="f6384-112">The asynchronous reader delivers samples to the controlling application in presentation-time order by making calls to the [**IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) callback method.</span></span> <span data-ttu-id="f6384-113">Wenn Sie eine Anwendung mit dem asynchronen Reader erstellen, müssen Sie **onsample** implementieren, um nicht komprimierte Beispiele zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="f6384-113">When you create an application using the asynchronous reader, you must implement **OnSample** to deal with uncompressed samples.</span></span> <span data-ttu-id="f6384-114">Funktionen oder Methoden, die zum Rendering von Inhalten erstellt werden, werden in der Regel innerhalb von " **onsample**" aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f6384-114">Typically, functions or methods created to render content will be called from within **OnSample**.</span></span>

<span data-ttu-id="f6384-115">Die typische Implementierung des **onsample** -Rückrufs umfasst die folgenden Schritte.</span><span class="sxs-lookup"><span data-stu-id="f6384-115">Typical implementation of the **OnSample** callback includes the following steps.</span></span>

1.  <span data-ttu-id="f6384-116">Rufen Sie den Speicherort und die Größe des Puffers ab, der das Beispiel enthält, indem Sie [**inssbuffer:: getbufferandlength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength) für den als *psample* übergebenen Puffer aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f6384-116">Retrieve the location and size of the buffer containing the sample by calling [**INSSBuffer::GetBufferAndLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength) on the buffer passed as *pSample*.</span></span>
2.  <span data-ttu-id="f6384-117">Verzweigen Sie Ihre Logik abhängig von der Ausgabe Nummer.</span><span class="sxs-lookup"><span data-stu-id="f6384-117">Branch your logic depending upon the output number.</span></span> <span data-ttu-id="f6384-118">Die Ausgabe Nummer wird als *dwoutputnumber* an **onsample** übermittelt.</span><span class="sxs-lookup"><span data-stu-id="f6384-118">The output number is passed to **OnSample** as *dwOutputNumber*.</span></span>
3.  <span data-ttu-id="f6384-119">Schließen Sie Renderinglogik für jede Ausgabe Nummer ein, die Sie unterstützen möchten.</span><span class="sxs-lookup"><span data-stu-id="f6384-119">Include rendering logic for each output number you want to support.</span></span> <span data-ttu-id="f6384-120">Wenn Sie Beispiele aus mehreren Ausgaben rendern, müssen Sie möglicherweise Ihr Rendering synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="f6384-120">If you are rendering samples from multiple outputs, you may need to synchronize your rendering.</span></span>

<span data-ttu-id="f6384-121">Anwendungen, die komprimierte Beispiele aus den ASF-Dateien bereitstellen, müssen die " [**iwmreadercallbackadvanced:: onstreamsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) "-Rückruf Methode implementieren.</span><span class="sxs-lookup"><span data-stu-id="f6384-121">Applications that deliver compressed samples from ASF files need to implement the [**IWMReaderCallbackAdvanced::OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) callback method.</span></span> <span data-ttu-id="f6384-122">**Onstreamsample** funktioniert beinahe identisch mit **onsample**, mit der Ausnahme, dass es komprimierte Stichproben nach streamnummer anstelle von nicht komprimierten Beispielen nach Ausgabe Nummer empfängt.</span><span class="sxs-lookup"><span data-stu-id="f6384-122">**OnStreamSample** functions almost identically to **OnSample**, except that it receives compressed samples by stream number instead of uncompressed samples by output number.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f6384-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f6384-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6384-124">**Iwmreadercallback-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="f6384-124">**IWMReaderCallback Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback)
</dt> <dt>

[<span data-ttu-id="f6384-125">**Iwmreadercallbackadvanced-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="f6384-125">**IWMReaderCallbackAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced)
</dt> <dt>

[<span data-ttu-id="f6384-126">**Lesen von Dateien mit dem asynchronen Reader**</span><span class="sxs-lookup"><span data-stu-id="f6384-126">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="f6384-127">**Verwenden der Rückruf Methoden**</span><span class="sxs-lookup"><span data-stu-id="f6384-127">**Using the Callback Methods**</span></span>](using-the-callback-methods.md)
</dt> </dl>

 

 




