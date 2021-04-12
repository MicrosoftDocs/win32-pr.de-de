---
description: Anzeigen von World Standard-Teletext
ms.assetid: 99b3395b-8775-4fe8-b173-187fa359978f
title: Anzeigen von World Standard-Teletext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f9b0885c08403de9578a8dee1eca6e000408ee5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344378"
---
# <a name="viewing-world-standard-teletext"></a><span data-ttu-id="df43b-103">Anzeigen von World Standard-Teletext</span><span class="sxs-lookup"><span data-stu-id="df43b-103">Viewing World Standard Teletext</span></span>

> [!Note]  
> <span data-ttu-id="df43b-104">Diese Funktion wurde aus Windows Vista und höheren Betriebssystemen entfernt.</span><span class="sxs-lookup"><span data-stu-id="df43b-104">This functionality has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="df43b-105">Es ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="df43b-105">It is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span>

 

<span data-ttu-id="df43b-106">Der Standard-Teletext (WST) ist im vertikalen Auslassungs Intervall (VBI) des analogen Fernsehsignals codiert.</span><span class="sxs-lookup"><span data-stu-id="df43b-106">World Standard Teletext (WST) is encoded in the vertical blanking interval (VBI) of the analog television signal.</span></span> <span data-ttu-id="df43b-107">Das Filter Diagramm für die Vorschau von Teletext ähnelt dem Diagramm, das zum Anzeigen von Untertiteln verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="df43b-107">The filter graph for previewing teletext is similar to the graph used to view closed captions.</span></span> <span data-ttu-id="df43b-108">Dieses Diagramm wird im folgenden Diagramm veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="df43b-108">The following diagram illustrates this graph.</span></span>

![WST-Vorschau Diagramm](images/vidcap10.png)

<span data-ttu-id="df43b-110">In diesem Diagramm werden die folgenden Filter für die WST-Anzeige verwendet:</span><span class="sxs-lookup"><span data-stu-id="df43b-110">This graph uses the following filters for WST display:</span></span>

-   <span data-ttu-id="df43b-111">[Tee/Sink-zu-Sink-Konverter](tee-sink-to-sink-converter.md).</span><span class="sxs-lookup"><span data-stu-id="df43b-111">[Tee/Sink-to-Sink Converter](tee-sink-to-sink-converter.md).</span></span> <span data-ttu-id="df43b-112">Akzeptiert die VBI-Informationen aus dem Erfassungs Filter und teilt Sie für jeden der Datendienste, die im Signal vorhanden sind, in separate Streams auf.</span><span class="sxs-lookup"><span data-stu-id="df43b-112">Accepts the VBI information from the capture filter and splits it into separate streams for each of the data services present on the signal.</span></span>
-   <span data-ttu-id="df43b-113">[WST-Codec](wst-codec-filter.md).</span><span class="sxs-lookup"><span data-stu-id="df43b-113">[WST Codec](wst-codec-filter.md).</span></span> <span data-ttu-id="df43b-114">Decodiert die Teletextdaten aus den VBI-Beispielen.</span><span class="sxs-lookup"><span data-stu-id="df43b-114">Decodes the Teletext data from the VBI samples.</span></span>
-   <span data-ttu-id="df43b-115">[WST-Decoder](wst-decoder-filter.md).</span><span class="sxs-lookup"><span data-stu-id="df43b-115">[WST Decoder](wst-decoder-filter.md).</span></span> <span data-ttu-id="df43b-116">Übersetzt Teletextdaten und zeichnet den Text auf Bitmaps.</span><span class="sxs-lookup"><span data-stu-id="df43b-116">Translates teletext data and draws the text onto bitmaps.</span></span> <span data-ttu-id="df43b-117">Der Downstream-Filter (in diesem Fall der Überlagerungs-Mixer) überlagert die Bitmaps auf dem Video.</span><span class="sxs-lookup"><span data-stu-id="df43b-117">The downstream filter (in this case the Overlay Mixer) overlays the bitmaps onto the video.</span></span>

<span data-ttu-id="df43b-118">Die **RenderStream** -Methode des Capture Graph-Generators unterstützt die WST-Filter nicht direkt, sodass Ihre Anwendung einige zusätzliche Aufgaben ausführen muss.</span><span class="sxs-lookup"><span data-stu-id="df43b-118">The Capture Graph Builder's **RenderStream** method does not support the WST filters directly, so your application must do some extra work.</span></span>

1.  <span data-ttu-id="df43b-119">Fügen Sie den Filter für den Overlay-Mixer dem Filter Diagramm hinzu.</span><span class="sxs-lookup"><span data-stu-id="df43b-119">Add the Overlay Mixer filter to the filter graph.</span></span> <span data-ttu-id="df43b-120">Der folgende Code verwendet die addfilterbyclsid-Funktion, die unter [Hinzufügen eines Filters nach CLSID beschrieben wird](add-a-filter-by-clsid.md).</span><span class="sxs-lookup"><span data-stu-id="df43b-120">The following code uses the AddFilterByCLSID function described in [Add a Filter by CLSID](add-a-filter-by-clsid.md).</span></span> <span data-ttu-id="df43b-121">(Addfilterbyclsid ist keine DirectShow-API.)</span><span class="sxs-lookup"><span data-stu-id="df43b-121">(AddFilterByCLSID is not a DirectShow API.)</span></span>
    ```C++
    IBaseFilter *pOvMix = NULL;  // Pointer to the Overlay Mixer filter.
    hr = AddFilterByCLSID(pGraph, CLSID_OverlayMixer, L"OVMix", &pOvMix);
    if (FAILED(hr)) 
    {
        // Handle the error ...
    }
    ```

    

2.  <span data-ttu-id="df43b-122">Verbinden Sie die Vorschau-PIN mit dem Videorendererfilter über den Überlagerungs-Mixer.</span><span class="sxs-lookup"><span data-stu-id="df43b-122">Connect the preview pin to the Video Renderer filter through the Overlay Mixer.</span></span> <span data-ttu-id="df43b-123">Sie können die **RenderStream** -Methode wie folgt verwenden:</span><span class="sxs-lookup"><span data-stu-id="df43b-123">You can use the **RenderStream** method, as follows:</span></span>
    ```C++
    hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, 
        pCap, pOvMix, 0);
    ```

    

3.  <span data-ttu-id="df43b-124">Fügen Sie dem Filter Diagramm den Filter Tee/Sink-to-Sink Converter hinzu.</span><span class="sxs-lookup"><span data-stu-id="df43b-124">Add the Tee/Sink-to-Sink Converter filter to the filter graph.</span></span> <span data-ttu-id="df43b-125">Der folgende Code verwendet die Funktion "-Funktion", die unter [Erstellen von Kernel-Mode filtern](creating-kernel-mode-filters.md)beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="df43b-125">The following code uses the CreateKernelFilter function described in [Creating Kernel-Mode Filters](creating-kernel-mode-filters.md).</span></span> <span data-ttu-id="df43b-126">(Bei "kreatekernelfilter" handelt es sich nicht um eine DirectShow-API.)</span><span class="sxs-lookup"><span data-stu-id="df43b-126">(CreateKernelFilter is not a DirectShow API.)</span></span>
    ```C++
    IBaseFilter* pKernelTee = NULL;
    hr = CreateKernelFilter(AM_KSCATEGORY_SPLITTER, 
        OLESTR("Tee/Sink-to-Sink Converter"), &pKernelTee);
    if (SUCCEEDED(hr))
    {
        hr = pGraph->AddFilter(pKernelTee, L"Kernel Tee");
    }
    ```

    

4.  <span data-ttu-id="df43b-127">Fügen Sie den WST-Codec-Filter dem Filter Diagramm hinzu:</span><span class="sxs-lookup"><span data-stu-id="df43b-127">Add the WST Codec filter to the filter graph:</span></span>
    ```C++
    IBaseFilter* pWstCodec = NULL;
    hr = CreateKernelFilter(AM_KSCATEGORY_VBICODEC, 
        OLESTR("WST Codec"), &pWstCodec);
    if (SUCCEEDED(hr))
    {
        hr = pGraph->AddFilter(pWstCodec, L"WST Codec");
    }
    ```

    

5.  <span data-ttu-id="df43b-128">Nennen Sie **RenderStream** , um die VBI-PIN des Erfassungs Filters mit dem "Tee/Sink-to-Sink Converter" und dem "Tee/Sink-to-Sink Converter" an den WST-Codec-Filter zu verbinden:</span><span class="sxs-lookup"><span data-stu-id="df43b-128">Call **RenderStream** to connect the capture filter's VBI pin to the Tee/Sink-to-Sink Converter, and the Tee/Sink-to-Sink Converter to the WST Codec filter:</span></span>
    ```C++
    hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 
        pKernelTee, pWstCodec);
    ```

    

6.  <span data-ttu-id="df43b-129">**RenderStream** erneut aufgerufen, um den WST-Codec-Filter mit dem Überlagerungs-Mixer zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="df43b-129">Call **RenderStream** again to connect the WST Codec filter to the Overlay Mixer.</span></span> <span data-ttu-id="df43b-130">Der WST-Decoderfilter wird automatisch in das Diagramm eingefügt.</span><span class="sxs-lookup"><span data-stu-id="df43b-130">The WST Decoder filter is automatically brought into the graph.</span></span>
    ```C++
    hr = pBuild->RenderStream(0, 0, pWstCodec, 0, pOvMix);
    ```

    

7.  <span data-ttu-id="df43b-131">Denken Sie daran, alle Filter Schnittstellen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="df43b-131">Remember to release all of the filter interfaces.</span></span>
    ```C++
    pOvMix->Release();
    pKernelTee->Release();
    pWstCodec->Release();
    ```

    

> [!Note]  
> <span data-ttu-id="df43b-132">Der WST-Decoderfilter unterstützt derzeit keine Verbindungen mit dem Filter für den Video Mischungs-Renderer (VMR).</span><span class="sxs-lookup"><span data-stu-id="df43b-132">Currently, the WST Decoder filter does not support connections to the Video Mixing Renderer (VMR) filter.</span></span> <span data-ttu-id="df43b-133">Daher müssen Sie den Legacy-Videorenderer-Filter verwenden, um Teletext anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="df43b-133">Therefore, you must use the legacy Video Renderer filter to view teletext.</span></span>

 

<span data-ttu-id="df43b-134">Wenn der Erfassungs Filter eine Video Port-VBI-PIN (PIN \_ CATEGPORY \_ Videoport \_ VBI) aufweist, verbinden Sie ihn mit dem [VBI-Oberflächen zuordnerfilter](vbi-surface-allocator.md) .</span><span class="sxs-lookup"><span data-stu-id="df43b-134">If the capture filter has a video port VBI pin (PIN\_CATEGPORY\_VIDEOPORT\_VBI), connect it to the [VBI Surface Allocator](vbi-surface-allocator.md) filter.</span></span> <span data-ttu-id="df43b-135">Andernfalls wird das Diagramm nicht ordnungsgemäß ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="df43b-135">The graph will not run correctly otherwise.</span></span> <span data-ttu-id="df43b-136">Im folgenden Codebeispiel wird die addfilterbyclsid-Funktion verwendet, die unter " [Hinzufügen eines Filters nach CLSID](add-a-filter-by-clsid.md)" und die Funktion "findpinbycategory" beschrieben wird. diese Funktion wird in verwenden [von PIN-Kategorien](working-with-pin-categories.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="df43b-136">The following code example uses the AddFilterByCLSID function, described in [Add a Filter by CLSID](add-a-filter-by-clsid.md), and the FindPinByCategory function, described in [Working with Pin Categories](working-with-pin-categories.md).</span></span> <span data-ttu-id="df43b-137">(Keine der Funktionen ist eine DirectShow-API.)</span><span class="sxs-lookup"><span data-stu-id="df43b-137">(Neither function is a DirectShow API.)</span></span>


```C++
// Look for a video port VBI pin on the capture filter.
IPin *pVPVBI = NULL;
hr = FindPinByCategory(pCap, PINDIR_OUTPUT, 
    PIN_CATEGORY_VIDEOPORT_VBI, &pVPVBI);
if (FAILED(hr))
{
    // No video port VBI pin; nothing else to do. OK to run the graph.
}
else
{
    // Found one. Connect it to the VBI Surface Allocator.
    IBaseFilter *pSurf = NULL;
    hr = AddFilterByCLSID(pGraph, CLSID_VBISurfaces, L"VBI Surf", &pSurf);
    if (SUCCEEDED(hr))
    {
        hr = pBuild->RenderStream(NULL, NULL, pVPVBI, 0, pSurf);
        pSurf->Release();
    }
    if (FAILED(hr))
    {
        // Handle the error (not shown). It is probably not safe to 
        // run the graph at this point.
    }
    pVPVBI->Release();
}
```



## <a name="related-topics"></a><span data-ttu-id="df43b-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="df43b-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df43b-139">Untertitel und Teletext</span><span class="sxs-lookup"><span data-stu-id="df43b-139">Closed Captions and Teletext</span></span>](closed-captions-and-teletext.md)
</dt> </dl>

 

 



