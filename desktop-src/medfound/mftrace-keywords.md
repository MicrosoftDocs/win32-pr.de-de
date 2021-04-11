---
description: Mithilfe von MF Trace können Sie die Ablauf Verfolgungs Ergebnisse filtern, indem Sie eine Liste von Schlüsselwörtern angeben.
ms.assetid: e7c382cb-94ac-4f90-a3dd-32f94c538396
title: MF Trace-Schlüsselwörter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6d18a91aede8692209b9d5b7a2759c460e44043
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130500"
---
# <a name="mftrace-keywords"></a><span data-ttu-id="4a165-103">MF Trace-Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="4a165-103">MFTrace Keywords</span></span>

<span data-ttu-id="4a165-104">Mithilfe von [MF Trace](mftrace.md)können Sie die Ablauf Verfolgungs Ergebnisse filtern, indem Sie eine Liste von Schlüsselwörtern angeben.</span><span class="sxs-lookup"><span data-stu-id="4a165-104">Using [MFTrace](mftrace.md), you can filter the trace results by specifying a list of keywords.</span></span> <span data-ttu-id="4a165-105">Verwenden Sie in der Befehlszeile das Befehlszeilenargument **-k** .</span><span class="sxs-lookup"><span data-stu-id="4a165-105">At the command line, use the **-k** command-line argument.</span></span> <span data-ttu-id="4a165-106">Alternativ können Sie das- [**Schlüsselwort**](keyword.md) Element in der Konfigurationsdatei angeben.</span><span class="sxs-lookup"><span data-stu-id="4a165-106">Alternatively, specify the [**keyword**](keyword.md) element in the configuration file.</span></span> <span data-ttu-id="4a165-107">Weitere Informationen finden Sie unter [Verwenden von MF Trace](using-mftrace.md).</span><span class="sxs-lookup"><span data-stu-id="4a165-107">For more information, see [Using MFTrace](using-mftrace.md).</span></span>

<span data-ttu-id="4a165-108">MF-Trace unterstützt die folgenden Schlüsselwörter.</span><span class="sxs-lookup"><span data-stu-id="4a165-108">MFTrace supports the following keywords.</span></span> <span data-ttu-id="4a165-109">Die meisten verweisen auf bestimmte Schnittstellen oder Bibliotheks Exporte.</span><span class="sxs-lookup"><span data-stu-id="4a165-109">Most refer to particular interfaces or library exports.</span></span>

-   <span data-ttu-id="4a165-110">All</span><span class="sxs-lookup"><span data-stu-id="4a165-110">"All"</span></span>
-   <span data-ttu-id="4a165-111">Vorgegebene</span><span class="sxs-lookup"><span data-stu-id="4a165-111">"Default"</span></span>
-   <span data-ttu-id="4a165-112">Umleitungen</span><span class="sxs-lookup"><span data-stu-id="4a165-112">"Detours"</span></span>
-   <span data-ttu-id="4a165-113">"Ifiltergraph"</span><span class="sxs-lookup"><span data-stu-id="4a165-113">"IFilterGraph"</span></span>
-   <span data-ttu-id="4a165-114">"Igraphbuilder"</span><span class="sxs-lookup"><span data-stu-id="4a165-114">"IGraphBuilder"</span></span>
-   <span data-ttu-id="4a165-115">"IMediaControl"</span><span class="sxs-lookup"><span data-stu-id="4a165-115">"IMediaControl"</span></span>
-   <span data-ttu-id="4a165-116">"Imediaobject"</span><span class="sxs-lookup"><span data-stu-id="4a165-116">"IMediaObject"</span></span>
-   <span data-ttu-id="4a165-117">"IMemInputPin"</span><span class="sxs-lookup"><span data-stu-id="4a165-117">"IMemInputPin"</span></span>
-   <span data-ttu-id="4a165-118">"Imfaktivate"</span><span class="sxs-lookup"><span data-stu-id="4a165-118">"IMFActivate"</span></span>
-   <span data-ttu-id="4a165-119">"Imfattributes"</span><span class="sxs-lookup"><span data-stu-id="4a165-119">"IMFAttributes"</span></span>
-   <span data-ttu-id="4a165-120">IMFByteStream</span><span class="sxs-lookup"><span data-stu-id="4a165-120">"IMFByteStream"</span></span>
-   <span data-ttu-id="4a165-121">"IMF bytestreamhandler"</span><span class="sxs-lookup"><span data-stu-id="4a165-121">"IMFByteStreamHandler"</span></span>
-   <span data-ttu-id="4a165-122">"IMF"</span><span class="sxs-lookup"><span data-stu-id="4a165-122">"IMFClock"</span></span>
-   <span data-ttu-id="4a165-123">"IMF Media Event Generator"</span><span class="sxs-lookup"><span data-stu-id="4a165-123">"IMFMediaEventGenerator"</span></span>
-   <span data-ttu-id="4a165-124">"Imfmediasession"</span><span class="sxs-lookup"><span data-stu-id="4a165-124">"IMFMediaSession"</span></span>
-   <span data-ttu-id="4a165-125">"Imfmediasink"</span><span class="sxs-lookup"><span data-stu-id="4a165-125">"IMFMediaSink"</span></span>
-   <span data-ttu-id="4a165-126">"Imfmediasource"</span><span class="sxs-lookup"><span data-stu-id="4a165-126">"IMFMediaSource"</span></span>
-   <span data-ttu-id="4a165-127">"IMF Media Stream"</span><span class="sxs-lookup"><span data-stu-id="4a165-127">"IMFMediaStream"</span></span>
-   <span data-ttu-id="4a165-128">"Imfpmediaitem"</span><span class="sxs-lookup"><span data-stu-id="4a165-128">"IMFPMediaItem"</span></span>
-   <span data-ttu-id="4a165-129">"Imfpmediaplayer"</span><span class="sxs-lookup"><span data-stu-id="4a165-129">"IMFPMediaPlayer"</span></span>
-   <span data-ttu-id="4a165-130">"Imfpmediaplayercallback"</span><span class="sxs-lookup"><span data-stu-id="4a165-130">"IMFPMediaPlayerCallback"</span></span>
-   <span data-ttu-id="4a165-131">"IMF presentationclock"</span><span class="sxs-lookup"><span data-stu-id="4a165-131">"IMFPresentationClock"</span></span>
-   <span data-ttu-id="4a165-132">"Imberqualityrat"</span><span class="sxs-lookup"><span data-stu-id="4a165-132">"IMFQualityAdvise"</span></span>
-   <span data-ttu-id="4a165-133">"IMFQualityAdvise2"</span><span class="sxs-lookup"><span data-stu-id="4a165-133">"IMFQualityAdvise2"</span></span>
-   <span data-ttu-id="4a165-134">"IMF qualitymanager"</span><span class="sxs-lookup"><span data-stu-id="4a165-134">"IMFQualityManager"</span></span>
-   <span data-ttu-id="4a165-135">"Imfreadschreiteclassfactory"</span><span class="sxs-lookup"><span data-stu-id="4a165-135">"IMFReadWriteClassFactory"</span></span>
-   <span data-ttu-id="4a165-136">"IMF Sample"</span><span class="sxs-lookup"><span data-stu-id="4a165-136">"IMFSample"</span></span>
-   <span data-ttu-id="4a165-137">"IMF Schema Handler"</span><span class="sxs-lookup"><span data-stu-id="4a165-137">"IMFSchemeHandler"</span></span>
-   <span data-ttu-id="4a165-138">"Imbersink Writer"</span><span class="sxs-lookup"><span data-stu-id="4a165-138">"IMFSinkWriter"</span></span>
-   <span data-ttu-id="4a165-139">IMFSourceReader</span><span class="sxs-lookup"><span data-stu-id="4a165-139">"IMFSourceReader"</span></span>
-   <span data-ttu-id="4a165-140">"IMF sourcereadercallback"</span><span class="sxs-lookup"><span data-stu-id="4a165-140">"IMFSourceReaderCallback"</span></span>
-   <span data-ttu-id="4a165-141">"IMF sourceresolver"</span><span class="sxs-lookup"><span data-stu-id="4a165-141">"IMFSourceResolver"</span></span>
-   <span data-ttu-id="4a165-142">"IMF streamsink"</span><span class="sxs-lookup"><span data-stu-id="4a165-142">"IMFStreamSink"</span></span>
-   <span data-ttu-id="4a165-143">"Imftopoloader"</span><span class="sxs-lookup"><span data-stu-id="4a165-143">"IMFTopoLoader"</span></span>
-   <span data-ttu-id="4a165-144">"Imftopology"</span><span class="sxs-lookup"><span data-stu-id="4a165-144">"IMFTopology"</span></span>
-   <span data-ttu-id="4a165-145">"Imftopologynode"</span><span class="sxs-lookup"><span data-stu-id="4a165-145">"IMFTopologyNode"</span></span>
-   <span data-ttu-id="4a165-146">"IMF Transform"</span><span class="sxs-lookup"><span data-stu-id="4a165-146">"IMFTransform"</span></span>
-   <span data-ttu-id="4a165-147">"Iwmreader"</span><span class="sxs-lookup"><span data-stu-id="4a165-147">"IWMReader"</span></span>
-   <span data-ttu-id="4a165-148">"Kernel32Export"</span><span class="sxs-lookup"><span data-stu-id="4a165-148">"Kernel32Export"</span></span>
-   <span data-ttu-id="4a165-149">"MF-Export"</span><span class="sxs-lookup"><span data-stu-id="4a165-149">"MFExport"</span></span>
-   <span data-ttu-id="4a165-150">"MF-Export"</span><span class="sxs-lookup"><span data-stu-id="4a165-150">"MFPlatExport"</span></span>
-   <span data-ttu-id="4a165-151">"MF playexport"</span><span class="sxs-lookup"><span data-stu-id="4a165-151">"MFPlayExport"</span></span>
-   <span data-ttu-id="4a165-152">"MF Public"</span><span class="sxs-lookup"><span data-stu-id="4a165-152">"MFPublic"</span></span>
-   <span data-ttu-id="4a165-153">"Mfreadschreiteexport"</span><span class="sxs-lookup"><span data-stu-id="4a165-153">"MFReadWriteExport"</span></span>
-   <span data-ttu-id="4a165-154">"Ole32Export"</span><span class="sxs-lookup"><span data-stu-id="4a165-154">"Ole32Export"</span></span>
-   <span data-ttu-id="4a165-155">"wmvcoreexport"</span><span class="sxs-lookup"><span data-stu-id="4a165-155">"wmvCoreExport"</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a165-156">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4a165-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a165-157">MF-Ablauf Verfolgung</span><span class="sxs-lookup"><span data-stu-id="4a165-157">MFTrace</span></span>](mftrace.md)
</dt> <dt>

[<span data-ttu-id="4a165-158">Verwenden von MF Trace</span><span class="sxs-lookup"><span data-stu-id="4a165-158">Using MFTrace</span></span>](using-mftrace.md)
</dt> </dl>

 

 



