---
description: Aufzeichnen von Videos in einer AVI-Datei
ms.assetid: 0f5f4a82-4a2e-4c48-b201-bda641cb8619
title: Aufzeichnen von Videos in einer AVI-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86504e9ce149f495e1ea31664f56382340d33887
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104568390"
---
# <a name="capturing-video-to-an-avi-file"></a><span data-ttu-id="3ad04-103">Aufzeichnen von Videos in einer AVI-Datei</span><span class="sxs-lookup"><span data-stu-id="3ad04-103">Capturing Video to an AVI File</span></span>

<span data-ttu-id="3ad04-104">Die folgende Abbildung zeigt das einfachste mögliche Diagramm für die Erfassung von Videos in einer AVI-Datei.</span><span class="sxs-lookup"><span data-stu-id="3ad04-104">The following illustration shows the simplest possible graph for capturing video to an AVI file.</span></span>

![AVI-Video Erfassungs Diagramm](images/vidcap02.png)

<span data-ttu-id="3ad04-106">Der [AVI MUX](avi-mux-filter.md) -Filter nimmt den Videostream aus der Erfassungs-PIN und verpackt ihn in einen AVI-Stream.</span><span class="sxs-lookup"><span data-stu-id="3ad04-106">The [AVI Mux](avi-mux-filter.md) filter takes the video stream from the capture pin and packages it into an AVI stream.</span></span> <span data-ttu-id="3ad04-107">Ein Audiodatenstrom kann auch mit dem AVI MUX-Filter verbunden werden. in diesem Fall würde die MUX die beiden Streams überlassen.</span><span class="sxs-lookup"><span data-stu-id="3ad04-107">An audio stream could also be connected to the AVI Mux filter, in which case the mux would interleave the two streams.</span></span> <span data-ttu-id="3ad04-108">Der [dateiwriter](file-writer-filter.md) -Filter schreibt den AVI-Stream auf den Datenträger.</span><span class="sxs-lookup"><span data-stu-id="3ad04-108">The [File Writer](file-writer-filter.md) filter writes the AVI stream to disk.</span></span>

<span data-ttu-id="3ad04-109">Um das Diagramm zu erstellen, rufen Sie zunächst die [**ICaptureGraphBuilder2:: setoutputfilename**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) -Methode wie folgt auf:</span><span class="sxs-lookup"><span data-stu-id="3ad04-109">To build the graph, start by calling the [**ICaptureGraphBuilder2::SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) method, as follows:</span></span>


```C++
IBaseFilter *pMux;
hr = pBuild->SetOutputFileName(
    &MEDIASUBTYPE_Avi,  // Specifies AVI for the target file.
    L"C:\\Example.avi", // File name.
    &pMux,              // Receives a pointer to the mux.
    NULL);              // (Optional) Receives a pointer to the file sink.
```



<span data-ttu-id="3ad04-110">Der erste Parameter gibt den Dateityp an – in diesem Fall AVI.</span><span class="sxs-lookup"><span data-stu-id="3ad04-110">The first parameter specifies the file type — in this case, AVI.</span></span> <span data-ttu-id="3ad04-111">Der zweite Parameter gibt den Dateinamen an.</span><span class="sxs-lookup"><span data-stu-id="3ad04-111">The second parameter gives the file name.</span></span> <span data-ttu-id="3ad04-112">Für AVI erstellt die setoutputfilename-Methode den AVI MUX-Filter und den dateiwriter-Filter und fügt Sie dem Diagramm hinzu.</span><span class="sxs-lookup"><span data-stu-id="3ad04-112">For AVI, the SetOutputFileName method cocreates the AVI Mux filter and the File Writer filter and adds them to the graph.</span></span> <span data-ttu-id="3ad04-113">Außerdem wird der Dateiname im Datei Schreiber Filter festgelegt, indem die [**ifilesink Filter:: setFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) -Methode aufgerufen und die beiden Filter miteinander verbunden werden.</span><span class="sxs-lookup"><span data-stu-id="3ad04-113">It also sets the file name on the File Writer filter, by calling the [**IFileSinkFilter::SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) method, and connects the two filters.</span></span> <span data-ttu-id="3ad04-114">Die-Methode gibt einen Zeiger auf die AVI MUX im dritten Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="3ad04-114">The method returns a pointer to the AVI Mux in the third parameter.</span></span> <span data-ttu-id="3ad04-115">Optional wird ein Zeiger auf die [**ifilesinkfilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) -Schnittstelle im vierten Parameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3ad04-115">Optionally, it returns a pointer to the [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) interface in the fourth parameter.</span></span> <span data-ttu-id="3ad04-116">Wenn Sie diese Schnittstelle nicht benötigen, können Sie diesen Parameter auf **null** festlegen, wie im vorherigen Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="3ad04-116">If you don't need this interface, you can set this parameter to **NULL**, as shown in the previous example.</span></span>

<span data-ttu-id="3ad04-117">Als nächstes wird die [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) -Methode aufgerufen, um den Erfassungs Filter wie folgt mit der AVI-MUX-Datei zu verbinden:</span><span class="sxs-lookup"><span data-stu-id="3ad04-117">Next, call the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method to connect the capture filter to the AVI Mux, as follows:</span></span>


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_CAPTURE, // Pin category.
    &MEDIATYPE_Video,      // Media type.
    pCap,                  // Capture filter.
    NULL,                  // Intermediate filter (optional).
    pMux);                 // Mux or file sink filter.

// Release the mux filter.
pMux->Release();
```



<span data-ttu-id="3ad04-118">Der erste Parameter gibt die PIN-Kategorie an, die PIN- \_ kategorieerfassung \_ für die Erfassung ist.</span><span class="sxs-lookup"><span data-stu-id="3ad04-118">The first parameter gives the pin category, which is PIN\_CATEGORY\_CAPTURE for capture.</span></span> <span data-ttu-id="3ad04-119">Der zweite Parameter gibt den Medientyp an.</span><span class="sxs-lookup"><span data-stu-id="3ad04-119">The second parameter gives the media type.</span></span> <span data-ttu-id="3ad04-120">Der dritte Parameter ist ein Zeiger auf die [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) -Schnittstelle des Erfassungs Filters.</span><span class="sxs-lookup"><span data-stu-id="3ad04-120">The third parameter is a pointer to the capture filter's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span> <span data-ttu-id="3ad04-121">Der vierte Parameter ist optional. Sie können den Videostream über einen zwischen Filter, z. b. einen Encoder, weiterleiten, bevor Sie ihn an den MUX-Filter übergeben.</span><span class="sxs-lookup"><span data-stu-id="3ad04-121">The fourth parameter is optional; it lets you route the video stream through an intermediate filter, such as an encoder, before passing it to the mux filter.</span></span> <span data-ttu-id="3ad04-122">Andernfalls legen Sie diesen Parameter auf **null** fest, wie im vorherigen Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="3ad04-122">Otherwise, set this parameter to **NULL**, as shown in the previous example.</span></span> <span data-ttu-id="3ad04-123">Der fünfte Parameter ist der Zeiger auf den MUX-Filter.</span><span class="sxs-lookup"><span data-stu-id="3ad04-123">The fifth parameter is the pointer to the mux filter.</span></span> <span data-ttu-id="3ad04-124">Dieser Zeiger wird durch Aufrufen der setoutputfilename-Methode abgerufen.</span><span class="sxs-lookup"><span data-stu-id="3ad04-124">This pointer is obtained by calling the SetOutputFileName method.</span></span>

<span data-ttu-id="3ad04-125">Um Audiodaten aufzuzeichnen, nennen Sie RenderStream mit dem Medientyp MediaType \_ -Audiodatei.</span><span class="sxs-lookup"><span data-stu-id="3ad04-125">To capture audio, call RenderStream with the media type MEDIATYPE\_Audio.</span></span> <span data-ttu-id="3ad04-126">Wenn Sie Audiodaten und Videos von zwei separaten Geräten erfassen, empfiehlt es sich, den Audiostream in den Masterstream zu legen.</span><span class="sxs-lookup"><span data-stu-id="3ad04-126">If you are capturing audio and video from two separate devices, it is a good idea to make the audio stream the master stream.</span></span> <span data-ttu-id="3ad04-127">Dadurch wird die Abweichung zwischen den beiden Streams verhindert, da der AVI MUX-Filter die Wiedergabe Rate für den Videostream entsprechend dem Audiostream anpasst.</span><span class="sxs-lookup"><span data-stu-id="3ad04-127">This helps to prevent drift between the two streams, because the AVI Mux filter adjust the playback rate on the video stream to match the audio stream.</span></span> <span data-ttu-id="3ad04-128">Um den Masterstream festzulegen, müssen Sie die [**iconfigavimux:: setmasterstream**](/windows/desktop/api/Strmif/nf-strmif-iconfigavimux-setmasterstream) -Methode für den AVI MUX-Filter aufrufen:</span><span class="sxs-lookup"><span data-stu-id="3ad04-128">To set the master stream, call the [**IConfigAviMux::SetMasterStream**](/windows/desktop/api/Strmif/nf-strmif-iconfigavimux-setmasterstream) method on the AVI Mux filter:</span></span>


```C++
IConfigAviMux *pConfigMux = NULL;
hr = pMux->QueryInterface(IID_IConfigAviMux, (void**)&pConfigMux);
if (SUCCEEDED(hr))
{
    pConfigMux->SetMasterStream(1);
    pConfigMux->Release();
}
```



<span data-ttu-id="3ad04-129">Der Parameter für setmasterstream ist die streamnummer, die durch die Reihenfolge bestimmt wird, in der Sie RenderStream aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3ad04-129">The parameter to SetMasterStream is the stream number, which is determined by the order in which you call RenderStream.</span></span> <span data-ttu-id="3ad04-130">Wenn Sie z. b. RenderStream zuerst für Video und dann für Audiodaten aufzurufen, ist das Video Stream 0 und das Audioformat Stream 1.</span><span class="sxs-lookup"><span data-stu-id="3ad04-130">For example, if you call RenderStream first for video and then for audio, the video is stream 0 and the audio is stream 1.</span></span>

<span data-ttu-id="3ad04-131">Sie können auch festlegen, wie der AVI MUX-Filter die Audio-und Videostreams interverlässt, indem Sie die [**iconfiginterleaving::p UT \_ Mode**](/windows/desktop/api/Strmif/nf-strmif-iconfiginterleaving-put_mode) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3ad04-131">You may also want to set how the AVI Mux filter interleaves the audio and video streams, by calling the [**IConfigInterleaving::put\_Mode**](/windows/desktop/api/Strmif/nf-strmif-iconfiginterleaving-put_mode) method.</span></span>


```C++
IConfigInterleaving *pInterleave = NULL;
hr = pMux->QueryInterface(IID_IConfigInterleaving, (void**)&pInterleave);
if (SUCCEEDED(hr))
{
    pInterleave->put_Mode(INTERLEAVE_CAPTURE);
    pInterleave->Release();
}
```



<span data-ttu-id="3ad04-132">Mit dem Interleave- \_ Erfassungs Kennzeichen führt der AVI MUX eine Überlappungs Rate mit einer Rate aus, die für die Video Erfassung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="3ad04-132">With the INTERLEAVE\_CAPTURE flag, the AVI Mux performs interleaving at a rate that is suitable for video capture.</span></span> <span data-ttu-id="3ad04-133">Sie können auch Interleave \_ None verwenden, was bedeutet, dass kein Austausch erfolgt – die AVI-MUX schreibt die Daten einfach in der Reihenfolge, in der Sie ankommt.</span><span class="sxs-lookup"><span data-stu-id="3ad04-133">You can also use INTERLEAVE\_NONE, which means no interleaving — the AVI Mux will simply write the data in the order that it arrives.</span></span> <span data-ttu-id="3ad04-134">Das Interleave- \_ vollständige Flag bedeutet, dass die AVI-MUX vollständige überlappende Vorgänge ausführt. dieser Modus ist jedoch für die Video Erfassung weniger geeignet, da er die am meisten übergefasste erfordert.</span><span class="sxs-lookup"><span data-stu-id="3ad04-134">The INTERLEAVE\_FULL flag means the AVI Mux performs full interleaving; however, this mode is less suitable for video capture because it requires the most overheard.</span></span>

<span data-ttu-id="3ad04-135">Codieren des Video Datenstroms</span><span class="sxs-lookup"><span data-stu-id="3ad04-135">Encoding the Video Stream</span></span>

<span data-ttu-id="3ad04-136">Sie können den Videostream codieren, indem Sie einen encoderfilter zwischen dem Erfassungs Filter und dem AVI MUX-Filter einfügen.</span><span class="sxs-lookup"><span data-stu-id="3ad04-136">You can encode the video stream by inserting an encoder filter between the capture filter and the AVI Mux filter.</span></span> <span data-ttu-id="3ad04-137">Verwenden Sie den [Enumerator für System Geräte](system-device-enumerator.md) oder den [Filter-Mapper](filter-mapper.md) , um einen encoderfilter auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="3ad04-137">Use the [System Device Enumerator](system-device-enumerator.md) or the [Filter Mapper](filter-mapper.md) to select an encoder filter.</span></span> <span data-ttu-id="3ad04-138">(Weitere Informationen finden Sie unter Auflisten von [Geräten und Filtern](enumerating-devices-and-filters.md).)</span><span class="sxs-lookup"><span data-stu-id="3ad04-138">(For more information, see [Enumerating Devices and Filters](enumerating-devices-and-filters.md).)</span></span>

<span data-ttu-id="3ad04-139">Geben Sie den encoderfilter als vierten Parameter für RenderStream an, wie im folgenden Beispiel fett dargestellt:</span><span class="sxs-lookup"><span data-stu-id="3ad04-139">Specify the encoder filter as the fourth parameter to RenderStream, shown in bold in the following example:</span></span>


```C++
IBaseFilter *pEncoder;
/* Create the encoder filter (not shown). */
// Add it to the filter graph.
pGraph->AddFilter(pEncoder, L"Encoder");

/* Call SetOutputFileName as shown previously. */

// Render the stream.
hr = pBuild->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, 
    pCap, 
pEncoder, pMux);
pEncoder->Release();
```



<span data-ttu-id="3ad04-140">Der Encoder-Filter unterstützt möglicherweise [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) oder andere Schnittstellen zum Festlegen der Codierungs Parameter.</span><span class="sxs-lookup"><span data-stu-id="3ad04-140">The encoder filter might support [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) or other interfaces for setting the encoding parameters.</span></span> <span data-ttu-id="3ad04-141">Eine Liste möglicher Schnittstellen finden Sie unter [Schnittstellen für die Datei Codierung und-Decodierung](file-encoding-and-decoding-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="3ad04-141">For a list of possible interfaces, see [File Encoding and Decoding Interfaces](file-encoding-and-decoding-interfaces.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ad04-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3ad04-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ad04-143">Aufzeichnen von Videos in einer Datei</span><span class="sxs-lookup"><span data-stu-id="3ad04-143">Capturing Video to a File</span></span>](capturing-video-to-a-file.md)
</dt> </dl>

 

 



