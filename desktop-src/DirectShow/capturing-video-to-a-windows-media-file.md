---
description: Aufzeichnen von Videos in einer Windows Media-Datei
ms.assetid: cc23bfce-34b9-4976-8602-e0602c7da2af
title: Aufzeichnen von Videos in einer Windows Media-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6442c1cf3751beac8d4eba751452d9573e9eede
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104218996"
---
# <a name="capturing-video-to-a-windows-media-file"></a><span data-ttu-id="afc65-103">Aufzeichnen von Videos in einer Windows Media-Datei</span><span class="sxs-lookup"><span data-stu-id="afc65-103">Capturing Video to a Windows Media File</span></span>

<span data-ttu-id="afc65-104">Um Videos aufzuzeichnen und in eine Windows Media Video Datei (WMV) zu codieren, verbinden Sie die Erfassungs-PIN mit dem [WM-ASF-Writer](wm-asf-writer-filter.md) -Filter, wie im folgenden Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="afc65-104">To capture video and encode it to a Windows Media Video (WMV) file, connect the capture pin to the [WM ASF Writer](wm-asf-writer-filter.md) filter, as shown in the following diagram.</span></span>

![Windows Media Capture-Diagramm](images/vidcap03.png)

<span data-ttu-id="afc65-106">Die einfachste Möglichkeit zum Erstellen dieses Diagramms besteht darin, mediasubtype \_ ASF in der [**ICaptureGraphBuilder2:: setoutputfilename**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) -Methode anzugeben:</span><span class="sxs-lookup"><span data-stu-id="afc65-106">The easiest way to build this graph is by specifing MEDIASUBTYPE\_Asf in the [**ICaptureGraphBuilder2::SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) method:</span></span>


```C++
IBaseFilter* pASFWriter = 0;
hr = pBuild->SetOutputFileName(
    &MEDIASUBTYPE_Asf,   // Create a Windows Media file.
    L"C:\\VidCap.wmv",   // File name.
    &pASFWriter,         // Receives a pointer to the filter.
    NULL);  // Receives an IFileSinkFilter interface pointer (optional).
```



<span data-ttu-id="afc65-107">Der Wert mediasubtype \_ ASF weist den Erfassungs Diagramm-Generator an, den WM-ASF-Writer-Filter als Datei-Senke zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="afc65-107">The value MEDIASUBTYPE\_Asf tells the Capture Graph Builder to use the WM ASF Writer filter as the file sink.</span></span> <span data-ttu-id="afc65-108">Mit dem Erfassungs Diagramm-Generator wird der Filter erstellt, dem Diagramm hinzugefügt und [**ifilesink Filter:: setFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) aufgerufen, um den Namen der Ausgabedatei festzulegen.</span><span class="sxs-lookup"><span data-stu-id="afc65-108">The Capture Graph Builder creates the filter, adds it to the graph, and calls [**IFileSinkFilter::SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) to set the name of the output file.</span></span> <span data-ttu-id="afc65-109">Er gibt einen Zeiger auf den Filter als ausgehenden Parameter zurück (</span><span class="sxs-lookup"><span data-stu-id="afc65-109">It returns a pointer to the filter as an outgoing parameter (</span></span>


```
pASFWriter
```



<span data-ttu-id="afc65-110">im vorherigen Beispiel).</span><span class="sxs-lookup"><span data-stu-id="afc65-110">in the previous example).</span></span>

<span data-ttu-id="afc65-111">Verwenden Sie die [**iconfigasfwriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) -Schnittstelle auf dem WM-ASF-Writer, um das Windows Media-Profil festzulegen.</span><span class="sxs-lookup"><span data-stu-id="afc65-111">Use the [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) interface on the WM ASF Writer to set the Windows Media profile.</span></span> <span data-ttu-id="afc65-112">Dies müssen Sie tun, bevor Sie eine Verbindung mit Pins im WM-ASF-Writer herstellen.</span><span class="sxs-lookup"><span data-stu-id="afc65-112">You must do this before you connect any pins on the WM ASF Writer.</span></span>


```C++
IConfigAsfWriter *pConfig = 0;
hr = pASFWriter->QueryInterface(IID_IConfigAsfWriter, (void**)&pConfig);
if (SUCCEEDED(hr))
{
     // Configure the ASF Writer filter.
    pConfig->Release();
}
```



<span data-ttu-id="afc65-113">Weitere Informationen zum Festlegen des Profils finden Sie unter [Erstellen von ASF-Dateien in DirectShow](creating-asf-files-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="afc65-113">For more information about setting the profile, see [Creating ASF Files in DirectShow](creating-asf-files-in-directshow.md).</span></span>

<span data-ttu-id="afc65-114">Nennen Sie [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) , um den Erfassungs Filter mit dem ASF-Writer zu verbinden:</span><span class="sxs-lookup"><span data-stu-id="afc65-114">Call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) to connect the capture filter to the ASF Writer:</span></span>


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_CAPTURE,   // Capture pin.
    &MEDIATYPE_Video,        // Video. Use MEDIATYPE_Audio for audio.
    pCap,                    // Pointer to the capture filter. 
    0, 
    pASFWriter);             // Pointer to the sink filter (ASF Writer).
```



<span data-ttu-id="afc65-115">Jede Eingabe-PIN für den WM-ASF-Writer-Filter entspricht einem Stream im Windows Media-Profil.</span><span class="sxs-lookup"><span data-stu-id="afc65-115">Each input pin on the WM ASF Writer filter corresponds to a stream in the Windows Media profile.</span></span> <span data-ttu-id="afc65-116">Sie müssen jede Pin verbinden, damit der Inhalt der Datei mit dem Profil übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="afc65-116">You must connect every pin, so that the file content matches the profile.</span></span>

## <a name="related-topics"></a><span data-ttu-id="afc65-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="afc65-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="afc65-118">Aufzeichnen von Videos in einer Datei</span><span class="sxs-lookup"><span data-stu-id="afc65-118">Capturing Video to a File</span></span>](capturing-video-to-a-file.md)
</dt> </dl>

 

 



