---
title: So verwenden Sie die Writer-Postview
description: So verwenden Sie die Writer-Postview
ms.assetid: 9da3c749-f6bd-43b5-9eff-3a637ddef048
keywords:
- Advanced Systems Format (ASF), Writer-Postview
- ASF (Advanced Systems Format), Writer-Postview
- Advanced Systems Format (ASF), nach Anzeige
- ASF (Advanced Systems Format), Post View
- Writer-Postview
- nach Anzeige
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abb3c1c83ebd38ff04c2022e529693d3d43b8b35
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104516670"
---
# <a name="to-use-writer-postview"></a><span data-ttu-id="59936-109">So verwenden Sie die Writer-Postview</span><span class="sxs-lookup"><span data-stu-id="59936-109">To Use Writer Postview</span></span>

<span data-ttu-id="59936-110">Das Writer-Objekt bietet Funktionen für die Post Anzeige, sodass Sie geschriebene Inhalte überprüfen können, ohne das Reader-Objekt einrichten zu müssen.</span><span class="sxs-lookup"><span data-stu-id="59936-110">The writer object provides postviewing capabilities so that you can verify written content without having to set up the reader object.</span></span> <span data-ttu-id="59936-111">Das Writer-Objekt unterstützt keine Postview für Audioinhalte.</span><span class="sxs-lookup"><span data-stu-id="59936-111">The writer object does not support postviewing for audio content.</span></span>

<span data-ttu-id="59936-112">Der Writer-postviewer funktioniert auf die gleiche Weise wie das asynchrone Reader-Objekt, nur mit weniger Features.</span><span class="sxs-lookup"><span data-stu-id="59936-112">The writer postviewer works in much the same way as the asynchronous reader object, only with fewer features.</span></span> <span data-ttu-id="59936-113">Ausführliche Informationen zum Lesen digitaler Medien finden Sie unter [Lesen von ASF-Dateien](reading-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="59936-113">For detailed information about reading digital media, see [Reading ASF Files](reading-asf-files.md).</span></span>

<span data-ttu-id="59936-114">Führen Sie die folgenden Schritte aus, um den postviewer zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="59936-114">To implement the postviewer, perform the following steps.</span></span>

1.  <span data-ttu-id="59936-115">Implementieren Sie den-Rückruf [**iwmschreiterpostviewcallback:: onpostviewsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostviewcallback-onpostviewsample) .</span><span class="sxs-lookup"><span data-stu-id="59936-115">Implement the [**IWMWriterPostViewCallback::OnPostViewSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostviewcallback-onpostviewsample) callback.</span></span> <span data-ttu-id="59936-116">Diese Methode ist im Grunde mit [**iwmreadercallback:: onsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) identisch, mit der Ausnahme, dass Sie streamnummern anstelle von Ausgaben angibt.</span><span class="sxs-lookup"><span data-stu-id="59936-116">This method is essentially the same as [**IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) except that it specifies stream numbers instead of outputs.</span></span>
2.  <span data-ttu-id="59936-117">Richten Sie wie gewohnt zum Schreiben ein.</span><span class="sxs-lookup"><span data-stu-id="59936-117">Set up for writing as usual.</span></span>
3.  <span data-ttu-id="59936-118">Abrufen eines Zeigers auf die [**iwmschreiterpostview**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview) -Schnittstelle des Writer-Objekts durch Aufrufen von **iwmwriter:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="59936-118">Obtain a pointer to the [**IWMWriterPostView**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview) interface of the writer object by calling **IWMWriter::QueryInterface**.</span></span>
4.  <span data-ttu-id="59936-119">Legen Sie den Rückruf für den postviewer fest, der durch Aufrufen von [**iwmschreiterpostview:: setpostviewcallback**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setpostviewcallback)verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="59936-119">Set the callback for the postviewer to use by calling [**IWMWriterPostView::SetPostViewCallback**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setpostviewcallback).</span></span>
5.  <span data-ttu-id="59936-120">Für jeden Datenstrom, für den Sie Postview-Beispiele erhalten möchten, nennen Sie [**iwmschreiterpostview:: setreceivepostviewsamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setreceivepostviewsamples).</span><span class="sxs-lookup"><span data-stu-id="59936-120">For each stream for which you want to receive postview samples, call [**IWMWriterPostView::SetReceivePostViewSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setreceivepostviewsamples).</span></span> <span data-ttu-id="59936-121">Sie können überprüfen, ob ein Stream zum Empfangen von Postview-Beispielen festgelegt ist, indem Sie [**iwmschreiterpostview:: getreceivepostviewsamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-getreceivepostviewsamples)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="59936-121">You can check to see whether a stream is set to receive postview samples by calling [**IWMWriterPostView::GetReceivePostViewSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-getreceivepostviewsamples).</span></span>
6.  <span data-ttu-id="59936-122">Sie können die Beispiel Formate genau wie die Ausgabeformate im Reader-Objekt oder im synchronen Reader-Objekt bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="59936-122">You can manipulate the sample formats, just like you would the output formats in the reader object or synchronous reader object.</span></span>
7.  <span data-ttu-id="59936-123">Wenn Sie mit dem Schreiben der Datei beginnen, beginnen Sie mit dem Empfang von Beispielen in der Implementierung der **onpostviewsample** -Rückruf Methode.</span><span class="sxs-lookup"><span data-stu-id="59936-123">When you start writing the file, you will begin to receive samples in your implementation of the **OnPostViewSample** callback method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="59936-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="59936-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59936-125">**Iwmschreiterpostviewcallback-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="59936-125">**IWMWriterPostViewCallback Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostviewcallback)
</dt> <dt>

[<span data-ttu-id="59936-126">**Schreiben von ASF-Dateien**</span><span class="sxs-lookup"><span data-stu-id="59936-126">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




