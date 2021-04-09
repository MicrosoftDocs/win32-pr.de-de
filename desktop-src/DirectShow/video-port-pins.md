---
description: VideoPort-Pins
ms.assetid: a6be24e5-7937-48f1-abeb-3f29c3deeafd
title: VideoPort-Pins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d13ab4ad63995dd38460bf29064035c9c1802dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866435"
---
# <a name="video-port-pins"></a><span data-ttu-id="94daf-103">VideoPort-Pins</span><span class="sxs-lookup"><span data-stu-id="94daf-103">Video Port Pins</span></span>

<span data-ttu-id="94daf-104">Ein Erfassungsgerät mit einem Hardware Videoport verwendet möglicherweise die Video Port Erweiterungen (VPE) in Microsoft® DirectX®.</span><span class="sxs-lookup"><span data-stu-id="94daf-104">A capture device with a hardware video port might use the video port extensions (VPE) in Microsoft® DirectX®.</span></span> <span data-ttu-id="94daf-105">Wenn dies der Fall ist, hat der Erfassungs Filter eine videolport-PIN (VP).</span><span class="sxs-lookup"><span data-stu-id="94daf-105">If so, the capture filter will have a video port (VP) pin.</span></span> <span data-ttu-id="94daf-106">Keine Videodaten werden von der VP-Pin über das Filter Diagramm übertragen.</span><span class="sxs-lookup"><span data-stu-id="94daf-106">No video data travels from the VP pin through the filter graph.</span></span> <span data-ttu-id="94daf-107">Stattdessen werden Video Frames in der Hardware erstellt und direkt an den Videospeicher gesendet.</span><span class="sxs-lookup"><span data-stu-id="94daf-107">Instead, video frames are produced in hardware and sent directly to video memory.</span></span> <span data-ttu-id="94daf-108">Die VP-Pin ermöglicht das Senden von Steuerungs Nachrichten an die Hardware.</span><span class="sxs-lookup"><span data-stu-id="94daf-108">The VP pin allows control messages to be sent to the hardware.</span></span>

<span data-ttu-id="94daf-109">Es ist wichtig, dass Sie die VP-Pin verbinden, auch wenn Ihre Anwendung nur die Datei Erfassung ohne Vorschau ausführt.</span><span class="sxs-lookup"><span data-stu-id="94daf-109">It is important to connect the VP pin, even if your application only performs file capture with no preview.</span></span> <span data-ttu-id="94daf-110">Wenn Sie die PIN nicht verbunden lassen, wird das Diagramm nicht ordnungsgemäß ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="94daf-110">If you leave the pin unconnected, the graph will not run correctly.</span></span> <span data-ttu-id="94daf-111">Dies unterscheidet sich von Vorschau Pins, die nicht verbunden werden müssen.</span><span class="sxs-lookup"><span data-stu-id="94daf-111">This is different from preview pins, which do not have to be connected.</span></span>

<span data-ttu-id="94daf-112">Die verschiedenen DirectShow-Videorenderer stellen unterschiedliche Unterstützung für VP Pins bereit:</span><span class="sxs-lookup"><span data-stu-id="94daf-112">The different DirectShow video renderers provide varying support for VP pins:</span></span>

-   <span data-ttu-id="94daf-113">Videorenderer: Verbinden Sie die VP-PIN mit PIN 0 auf dem [Überlagerungs Mischungs](overlay-mixer-filter.md) Filter, und verbinden Sie den Überlagerungs Filter Filter mit dem Videorenderer.</span><span class="sxs-lookup"><span data-stu-id="94daf-113">Video Renderer: Connect the VP pin to pin 0 on the [Overlay Mixer](overlay-mixer-filter.md) filter, and connect the Overlay Mixer filter to the Video Renderer.</span></span>
-   <span data-ttu-id="94daf-114">VMR-7: Verbinden Sie die VP-PIN mit dem [Video Port-Manager](video-port-manager.md) -Filter, und verbinden Sie den Videoport-Manager mit VMR-7.</span><span class="sxs-lookup"><span data-stu-id="94daf-114">VMR-7: Connect the VP pin to the [Video Port Manager](video-port-manager.md) filter, and connect the Video Port Manager to the VMR-7.</span></span>
-   <span data-ttu-id="94daf-115">VMR-9: Sie können VMR-9 nicht verwenden, wenn das Gerät über eine VP-Pin verfügt, da Direct3D 9 keine videports unterstützt.</span><span class="sxs-lookup"><span data-stu-id="94daf-115">VMR-9: You cannot use the VMR-9 if the device has a VP pin, because Direct3D 9 does not support video ports.</span></span> <span data-ttu-id="94daf-116">Verwenden Sie entweder den Videorenderer oder VMR-7.</span><span class="sxs-lookup"><span data-stu-id="94daf-116">Use either the Video Renderer or the VMR-7.</span></span>

<span data-ttu-id="94daf-117">Für Video Port Szenarios werden der Überlagerungs-und Videorenderer über Video Port Manager und VMR-7 empfohlen, da nicht alle Treiber den Videoport-Manager unterstützen.</span><span class="sxs-lookup"><span data-stu-id="94daf-117">For video port scenarios, the Overlay Mixer and Video Renderer are recommended over the Video Port Manager and VMR-7, because not all drivers support the Video Port Manager.</span></span> <span data-ttu-id="94daf-118">Im Allgemeinen ist der Überlagerungs Mixer die zuverlässigste Option für videports.</span><span class="sxs-lookup"><span data-stu-id="94daf-118">In general, the Overlay Mixer is the most reliable option for video ports.</span></span>

<span data-ttu-id="94daf-119">Mit der [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) -Methode wird der Überlagerungs-Mixer automatisch eingefügt, wenn eine VP-Pin vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="94daf-119">The [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method automatically inserts the Overlay Mixer if there is a VP pin.</span></span> <span data-ttu-id="94daf-120">Wenn Sie das Diagramm erstellen, ohne diese Methode zu verwenden, sollten Sie überprüfen, ob im Erfassungs Filter eine Videoport-Pin vorhanden ist. ist dies der Fall, stellen Sie eine Verbindung mit dem Filter für den Überlagerungs Filter her, wie im folgenden Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="94daf-120">If you are building the graph without using this method, you should check for a video port pin on the capture filter, and if one is present, connect it to the Overlay Mixer filter, as shown in the following diagram.</span></span>

![Verbinden einer Videoport-PIN mit dem Überlagerungs-Mischungs Filter.](images/vidcap11.png)

<span data-ttu-id="94daf-122">Sie können die [**ICaptureGraphBuilder2:: findpin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) -Methode verwenden, um nach einer VP-PIN im Erfassungs Filter zu suchen:</span><span class="sxs-lookup"><span data-stu-id="94daf-122">You can use the [**ICaptureGraphBuilder2::FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) method to search for a VP pin on the capture filter:</span></span>


```C++
hr = pBuild->FindPin(
    pCap,                    // Pointer to the capture filter.
    PINDIR_OUTPUT,           // Look for an output pin.
    &PIN_CATEGORY_VIDEOPORT, // Look for a video port pin.
    NULL,                    // Any media type.
    FALSE,                   // Pin can be connected.
    0,                       // Retrieve the first matching pin.
    &pVPPin                  // Receives a pointer to the pin.
);
```



<span data-ttu-id="94daf-123">Nachdem Sie den Overlay-Mixer dem Diagramm hinzugefügt haben, können Sie **findpin** erneut ausführen, um PIN 0 auf dem Überlagerungs Mixer zu suchen.</span><span class="sxs-lookup"><span data-stu-id="94daf-123">After you add the Overlay Mixer to the graph, call **FindPin** again to find pin 0 on the Overlay Mixer.</span></span> <span data-ttu-id="94daf-124">PIN 0 ist immer die erste Eingabe-PIN für den Filter.</span><span class="sxs-lookup"><span data-stu-id="94daf-124">Pin 0 is always the first input pin on the filter.</span></span>


```C++
pBuild->FindPin(pOvMix, PINDIR_INPUT, NULL, NULL, TRUE, 0, &pOVPin);
```



<span data-ttu-id="94daf-125">Verbinden Sie die beiden Pins durch Aufrufen von [**igraphbuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect).</span><span class="sxs-lookup"><span data-stu-id="94daf-125">Connect the two pins by calling [**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect).</span></span>


```C++
pGraph->Connect(pVPPin, pOvPin);
```



<span data-ttu-id="94daf-126">Verbinden Sie anschließend die Ausgabe-PIN des Overlay-Handlers mit dem Videorendererfilter.</span><span class="sxs-lookup"><span data-stu-id="94daf-126">Then connect the Overlay Mixer's output pin to the Video Renderer filter.</span></span> <span data-ttu-id="94daf-127">Sie können das Video ausblenden, indem Sie die sichtbaren Methoden [**IVideoWindow::p UT \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) und [**IVideoWindow::p UT \_**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) im Filter Graph-Manager aufrufen.</span><span class="sxs-lookup"><span data-stu-id="94daf-127">You can hide the video by calling the [**IVideoWindow::put\_AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) and [**IVideoWindow::put\_Visible**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) methods on the Filter Graph Manager.</span></span>

<span data-ttu-id="94daf-128">Bei TV-Tuners kann der Erfassungs Filter auch eine Video Port-VBI-PIN (PIN- \_ Kategorie \_ Videoport \_ VBI) enthalten.</span><span class="sxs-lookup"><span data-stu-id="94daf-128">For TV tuners, the capture filter might also have a video port VBI pin (PIN\_CATEGORY\_VIDEOPORT\_VBI).</span></span> <span data-ttu-id="94daf-129">Wenn dies der Fall ist, verbinden Sie diese PIN mit dem [VBI-Oberflächen zuordnerfilter](vbi-surface-allocator.md) .</span><span class="sxs-lookup"><span data-stu-id="94daf-129">If so, connect that pin to the [VBI Surface Allocator](vbi-surface-allocator.md) filter.</span></span> <span data-ttu-id="94daf-130">Weitere Informationen finden Sie unter [anzeigen](viewing-closed-captions.md)von Untertiteln.</span><span class="sxs-lookup"><span data-stu-id="94daf-130">For more information, see [Viewing Closed Captions](viewing-closed-captions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="94daf-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="94daf-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94daf-132">Erweiterte Erfassungs Themen</span><span class="sxs-lookup"><span data-stu-id="94daf-132">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> <dt>

[<span data-ttu-id="94daf-133">Verwenden des Overlay-Mischers bei der Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="94daf-133">Using the Overlay Mixer in Video Capture</span></span>](using-the-overlay-mixer-in-video-capture.md)
</dt> </dl>

 

 



