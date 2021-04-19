---
description: MPEG1Source-Beispiel
ms.assetid: c9f131ff-0b79-487c-9a46-a9b1350553a1
title: MPEG1Source-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c71bd541a7bd01621ca7359eb9e229a08e91a04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359937"
---
# <a name="mpeg1source-sample"></a><span data-ttu-id="de980-103">MPEG1Source-Beispiel</span><span class="sxs-lookup"><span data-stu-id="de980-103">MPEG1Source Sample</span></span>

<span data-ttu-id="de980-104">Zeigt, wie Sie eine benutzerdefinierte Medienquelle in Microsoft Media Foundation schreiben.</span><span class="sxs-lookup"><span data-stu-id="de980-104">Shows how to write a custom media source in Microsoft Media Foundation.</span></span> <span data-ttu-id="de980-105">Im Beispiel wird eine Medienquelle implementiert, die MPEG-1-System Schicht-Streams analysiert und Beispiele generiert, die MPEG-1-Nutzlasten enthalten.</span><span class="sxs-lookup"><span data-stu-id="de980-105">The sample implements a media source that parses MPEG-1 systems-layer streams and generates samples that contain MPEG-1 payloads.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="de980-106">Gezeigte APIs</span><span class="sxs-lookup"><span data-stu-id="de980-106">APIs Demonstrated</span></span>

<span data-ttu-id="de980-107">In diesem Beispiel werden die folgenden Media Foundation Schnittstellen veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="de980-107">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="de980-108">**IMF bytestreamhandler**</span><span class="sxs-lookup"><span data-stu-id="de980-108">**IMFByteStreamHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)
-   [<span data-ttu-id="de980-109">**Imfmediasource**</span><span class="sxs-lookup"><span data-stu-id="de980-109">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
-   [<span data-ttu-id="de980-110">**IMF Media Stream**</span><span class="sxs-lookup"><span data-stu-id="de980-110">**IMFMediaStream**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)

<span data-ttu-id="de980-111">Bevor Sie dieses Beispiel untersuchen, sollten Sie sich das [Beispiel für wavsource](wavsource-sample.md)ansehen, das eine einfachere Implementierung einer Medienquelle ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="de980-111">Before examining this sample, you might want to review the [WavSource Sample](wavsource-sample.md), which provides a simpler implementation of a media source.</span></span> <span data-ttu-id="de980-112">Im MPEG1Source-Beispiel werden einige Features hinzugefügt, die in den meisten realen Implementierungen einer Medienquelle zu finden sind:</span><span class="sxs-lookup"><span data-stu-id="de980-112">The MPEG1Source sample adds some features that would be found in most real-world implementations of a media source:</span></span>

-   <span data-ttu-id="de980-113">Mehrere Datenströme</span><span class="sxs-lookup"><span data-stu-id="de980-113">Multiple streams</span></span>
-   <span data-ttu-id="de980-114">Asynchrone Methoden</span><span class="sxs-lookup"><span data-stu-id="de980-114">Asynchronous methods</span></span>
-   <span data-ttu-id="de980-115">Asynchrone e/a</span><span class="sxs-lookup"><span data-stu-id="de980-115">Asynchronous I/O</span></span>

<span data-ttu-id="de980-116">Im Windows SDK für Windows Server 2008 enthält dieses Beispiel auch einen MPEG-1-Beispiel Video Decoder, der den Zeit Code für jeden Videorahmen anzeigt.</span><span class="sxs-lookup"><span data-stu-id="de980-116">In the Windows SDK for Windows Server 2008, this sample also includes a sample MPEG-1 video decoder that displays the time code for each video frame.</span></span> <span data-ttu-id="de980-117">(In diesem Fall wird der MPEG-1-Bitstream nicht decodiert.)</span><span class="sxs-lookup"><span data-stu-id="de980-117">(It does not actually decode the MPEG-1 bitstream.)</span></span>

<span data-ttu-id="de980-118">Ab dem Windows SDK für Windows 7 wurde der Decoder in ein separates Beispiel verschoben.</span><span class="sxs-lookup"><span data-stu-id="de980-118">Starting in the Windows SDK for Windows 7, the decoder has been moved to a separate sample.</span></span> <span data-ttu-id="de980-119">Siehe [Decoder-Beispiel](decoder-sample.md).</span><span class="sxs-lookup"><span data-stu-id="de980-119">See [Decoder Sample](decoder-sample.md).</span></span>

## <a name="usage"></a><span data-ttu-id="de980-120">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="de980-120">Usage</span></span>

<span data-ttu-id="de980-121">Im MPEG1Source-Beispiel wird eine DLL erstellt, bei der es sich um einen com-Server für die Medienquelle, den bytestreamhandler der Medienquelle und den Decoder-MFT handelt.</span><span class="sxs-lookup"><span data-stu-id="de980-121">The MPEG1Source sample builds a DLL that is a COM server for the media source, media source's byte-stream handler, and the decoder MFT.</span></span> <span data-ttu-id="de980-122">Vor der Verwendung der Medienquelle müssen Sie die dll registrieren.</span><span class="sxs-lookup"><span data-stu-id="de980-122">Before using the media source, you must register the DLL.</span></span>

<span data-ttu-id="de980-123">Wenn Sie die Medienquelle verwenden möchten, können Sie das [basicplayback-Beispiel](/previous-versions//bb970475(v=vs.85))ausführen.</span><span class="sxs-lookup"><span data-stu-id="de980-123">To use the media source, you can run the [BasicPlayback Sample](/previous-versions//bb970475(v=vs.85)).</span></span> <span data-ttu-id="de980-124">Der quellresolver lädt automatisch die Medienquelle, wenn Sie eine MPEG-1-Datei für die Wiedergabe auswählen.</span><span class="sxs-lookup"><span data-stu-id="de980-124">The source resolver will automatically load the media source if you select an MPEG-1 file for playback.</span></span> <span data-ttu-id="de980-125">(Wenn ein Fehler auftritt, stellen Sie sicher, dass Sie die MPEG1Source-dll erfolgreich registriert haben.)</span><span class="sxs-lookup"><span data-stu-id="de980-125">(If an error occurs, make sure that you successfully registered the MPEG1Source DLL.)</span></span>

<span data-ttu-id="de980-126">Sie können auch das Tool topoedit verwenden, um eine Wiedergabe Topologie zu erstellen, die die Medienquelle enthält.</span><span class="sxs-lookup"><span data-stu-id="de980-126">You can also use the TopoEdit tool to build a playback topology that contains the media source.</span></span> <span data-ttu-id="de980-127">Weitere Informationen zu topoedit finden Sie unter [topoedit](topoedit.md).</span><span class="sxs-lookup"><span data-stu-id="de980-127">For more information about TopoEdit, see [TopoEdit](topoedit.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="de980-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de980-128">Requirements</span></span>



| <span data-ttu-id="de980-129">Produkt</span><span class="sxs-lookup"><span data-stu-id="de980-129">Product</span></span>                                                        | <span data-ttu-id="de980-130">Version</span><span class="sxs-lookup"><span data-stu-id="de980-130">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="de980-131">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="de980-131">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="de980-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="de980-132">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="de980-133">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="de980-133">Downloading the Sample</span></span>

<span data-ttu-id="de980-134">Dieses Beispiel ist im [GitHub-Repository für klassische Windows-Beispiele](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mpeg1source)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="de980-134">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mpeg1source).</span></span>

## <a name="related-topics"></a><span data-ttu-id="de980-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="de980-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de980-136">Media Foundation-SDK-Beispiele</span><span class="sxs-lookup"><span data-stu-id="de980-136">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="de980-137">Medienquellen</span><span class="sxs-lookup"><span data-stu-id="de980-137">Media Sources</span></span>](media-sources.md)
</dt> <dt>

[<span data-ttu-id="de980-138">Schema Handler und Byte-Stream Handler</span><span class="sxs-lookup"><span data-stu-id="de980-138">Scheme Handlers and Byte-Stream Handlers</span></span>](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[<span data-ttu-id="de980-139">Tutorial: Schreiben einer benutzerdefinierten Medienquelle</span><span class="sxs-lookup"><span data-stu-id="de980-139">Tutorial: Writing a Custom Media Source</span></span>](tutorial--writing-a-custom-media-source.md)
</dt> <dt>

[<span data-ttu-id="de980-140">Wavsource-Beispiel</span><span class="sxs-lookup"><span data-stu-id="de980-140">WavSource Sample</span></span>](wavsource-sample.md)
</dt> </dl>

 

 
