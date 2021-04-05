---
title: Webstream-Wiedergabe in DirectShow
description: Webstream-Wiedergabe in DirectShow
ms.assetid: cc307c24-2bd2-43de-ba81-1cf5b05524b2
keywords:
- Windows Media-Format-SDK, DirectShow
- Windows Media-Format-SDK, Webstream-Wiedergabe
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- Advanced Systems Format (ASF), Wiedergabe von Webstreams
- ASF (Advanced Systems Format), Webstream-Wiedergabe
- DirectShow, Webstream-Wiedergabe
- Webstreams, DirectShow
- Webstreams, Wiedergabe in DirectShow
- Streams, Webstream-Wiedergabe in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a696e8184554195cf6e9c841b2fb59c4281e377a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947537"
---
# <a name="web-stream-playback-in-directshow"></a><span data-ttu-id="3f893-113">Webstream-Wiedergabe in DirectShow</span><span class="sxs-lookup"><span data-stu-id="3f893-113">Web Stream Playback in DirectShow</span></span>

<span data-ttu-id="3f893-114">Microsoft DirectShow unterstützt Webstreams (Weitere Informationen finden Sie unter [Webstreams](web-streams.md) ) in Dateiwiedergabe Szenarios über den [WM-ASF-Reader](wm-asf-reader-filter.md) -Filter. Sie müssen jedoch einen eigenen DirectShow-Filter schreiben, um den Stream zu erfassen und beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="3f893-114">Microsoft DirectShow supports Web streams (see [Web Streams](web-streams.md) for more information) in file playback scenarios through the [WM ASF Reader](wm-asf-reader-filter.md) filter, but you must write your own DirectShow filter to capture and persist the stream.</span></span>

> [!Note]  
> <span data-ttu-id="3f893-115">Um Webstreams in Inhalten wiederzugeben, die von einem Server mit Windows Media Services gestreamt werden, verwenden Sie die Windows Media Player 9-Reihe ActiveX®-Steuerelement, das in eine Webseite eingebettet ist.</span><span class="sxs-lookup"><span data-stu-id="3f893-115">To play back Web streams in content that is being streamed from a server running Windows Media Services, use the Windows Media Player 9 Series ActiveX® control embedded in a Web page.</span></span>

 

<span data-ttu-id="3f893-116">Wenn eine Datei mit Streams vom Typ "wmmediatype \_ Filetransfer" angegeben wird, erstellt der WM-ASF-Reader eine Ausgabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="3f893-116">When given a file containing streams of type WMMEDIATYPE\_FileTransfer, the WM ASF Reader will create an output pin for it.</span></span> <span data-ttu-id="3f893-117">Der Format Block ist eine [**WMT- \_ Webstream- \_ Format**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format) Struktur.</span><span class="sxs-lookup"><span data-stu-id="3f893-117">The format block will be a [**WMT\_WEBSTREAM\_FORMAT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format) structure.</span></span> <span data-ttu-id="3f893-118">Wenn kein downstreamfilter verfügbar ist, mit dem dieser Medientyp verarbeitet werden kann, bleibt die PIN unverändert, aber die Datei findet weiterhin die Audiodaten und/oder Videostreams.</span><span class="sxs-lookup"><span data-stu-id="3f893-118">If no downstream filter is available that can handle that media type, then the pin will remain unconnected, but the file will still play the audio and/or video streams.</span></span>

<span data-ttu-id="3f893-119">Es ist wichtig zu verstehen, dass jedes Medien Beispiel in einem Webstream eine [**WMT- \_ Webstream- \_ Beispiel \_ Header**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_sample_header) Struktur enthält, die abhängig von der Länge des **wszurl** -Members eine Variable Länge aufweist.</span><span class="sxs-lookup"><span data-stu-id="3f893-119">It is important to understand that each media sample in a Web stream contains a [**WMT\_WEBSTREAM\_SAMPLE\_HEADER**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_sample_header) structure, which has a variable length depending on the length of its **wszURL** member.</span></span> <span data-ttu-id="3f893-120">Der Zeiger auf die Beispiel Daten zeigt zunächst auf diese-Struktur, und Sie müssen den Zeiger hinter der-Struktur bewegen, um auf die eigentlichen Daten im Stream zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="3f893-120">The pointer to the sample data initially points to this structure, and you must advance the pointer past the structure in order to access the actual data in the stream.</span></span> <span data-ttu-id="3f893-121">Der Filter für den webstreamhandler sollte auf der **cbasererererklasse** basieren.</span><span class="sxs-lookup"><span data-stu-id="3f893-121">Your Web stream handler filter should be based on the **CBaseRenderer** class.</span></span> <span data-ttu-id="3f893-122">In der Methode " **dorendersample** " muss der Filter die Struktur nach Informationen über den Webstream analysieren und dann die entsprechende Aktion ausführen.</span><span class="sxs-lookup"><span data-stu-id="3f893-122">In the **DoRenderSample** method, the filter will need to parse the structure for information about the Web stream, and then perform the appropriate action.</span></span> <span data-ttu-id="3f893-123">In der Regel umfasst dies das Speichern der Datei auf dem Datenträger und das anschließende Aufrufen von " **commiturlcacheentry** " und " **createurlcacheentry** ", um die Dateien in den Internet Explorer-Cache zu platzieren.</span><span class="sxs-lookup"><span data-stu-id="3f893-123">Typically, this will involve saving the file to disk, and then calling **CommitUrlCacheEntry** and **CreateUrlCacheEntry** to place the files into the Internet Explorer cache.</span></span> <span data-ttu-id="3f893-124">Der Filter muss mehrteilige Dateien verarbeiten, d. h. Dateien, die größer als ein Beispiel sind, und auch Rendering-Befehle verarbeiten müssen, die vom **WMT- \_ Webstream \_ Sample \_ Header. wsampletype** -Member angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3f893-124">The filter must handle multipart files, that is, files that are larger than one sample, and also must handle render commands, which are specified by the **WMT\_WEBSTREAM\_SAMPLE\_HEADER.wSampleType** member.</span></span> <span data-ttu-id="3f893-125">Der Filter sendet ein **EC- \_ OLE- \_ Ereignis** zusammen mit dem Text der **WMT- \_ Webstream- \_ Beispiel \_ Kopfzeile. wszurl** -Zeichenfolge, die den Namen der Datei enthält, die gerendert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3f893-125">The filter sends an **EC\_OLE\_EVENT** to the application, along with the text of the **WMT\_WEBSTREAM\_SAMPLE\_HEADER.wszURL** string which contains the name of the file to be rendered.</span></span> <span data-ttu-id="3f893-126">Die Anwendung bewirkt dann, dass der Browser die angegebene Seite anzeigt.</span><span class="sxs-lookup"><span data-stu-id="3f893-126">The application then causes the browser to display the specified page.</span></span> <span data-ttu-id="3f893-127">Wenn der Webstream ordnungsgemäß erstellt wurde, sollte sich die Datei bereits im Cache befinden.</span><span class="sxs-lookup"><span data-stu-id="3f893-127">If the Web stream has been authored correctly, the file should already be in the cache.</span></span>

<span data-ttu-id="3f893-128">Weitere Informationen zu **cbaserderderer**, **dorendersample** und **EC \_ OLE \_ Event** finden Sie in der DirectShow SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="3f893-128">For more information on **CBaseRenderer**, **DoRenderSample**, and **EC\_OLE\_EVENT**, see the DirectShow SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f893-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3f893-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f893-130">**Webstreams**</span><span class="sxs-lookup"><span data-stu-id="3f893-130">**Web Streams**</span></span>](web-streams.md)
</dt> </dl>

 

 




