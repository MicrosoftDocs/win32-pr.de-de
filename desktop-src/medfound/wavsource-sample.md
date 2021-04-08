---
description: Wavsource-Beispiel
ms.assetid: 905fbba5-0a04-4048-80bd-f8707c4879da
title: Wavsource-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 050edb9df75032384f93c6e1f37c52e89f14a748
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863923"
---
# <a name="wavsource-sample"></a><span data-ttu-id="463d0-103">Wavsource-Beispiel</span><span class="sxs-lookup"><span data-stu-id="463d0-103">WavSource Sample</span></span>

<span data-ttu-id="463d0-104">Zeigt, wie eine benutzerdefinierte Medienquelle in Microsoft Media Foundation erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="463d0-104">Shows how to create a custom media source in Microsoft Media Foundation.</span></span> <span data-ttu-id="463d0-105">Im Beispiel wird eine Medienquelle implementiert, mit der WAV-Audiodateien analysiert werden.</span><span class="sxs-lookup"><span data-stu-id="463d0-105">The sample implements a media source that parses .wav audio files.</span></span>

<span data-ttu-id="463d0-106">Dieses Beispiel ist ein relativ einfaches Beispiel für eine Medienquelle:</span><span class="sxs-lookup"><span data-stu-id="463d0-106">This sample is a relatively simple example of a media source:</span></span>

-   <span data-ttu-id="463d0-107">Es ist nur ein Stream vorhanden, sodass kein Code zum Implementieren der Streamauswahl vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="463d0-107">There is only one stream, so there is no code to implement stream selection.</span></span>
-   <span data-ttu-id="463d0-108">Die Medienquelle implementiert nicht die Raten Kontrolle (d. h. die schnelle vorwärts-oder rückwärts Wiedergabe).</span><span class="sxs-lookup"><span data-stu-id="463d0-108">The media source does not implement rate control (that is, fast forward or reverse playback).</span></span>
-   <span data-ttu-id="463d0-109">Alle Quell-und Datenstrom Methoden werden als synchrone Methoden implementiert.</span><span class="sxs-lookup"><span data-stu-id="463d0-109">All source and stream methods are implemented as synchronous methods.</span></span>
-   <span data-ttu-id="463d0-110">Da es sich bei dem Datenteil einer WAV-Datei um einen einzelnen Block nicht komprimierter PCM-Audiodaten handelt, muss die Medienquelle keine Paket Header lesen oder den Stream bei der Wiedergabe anderweitig analysieren, außer wenn der anfängliche [**wellenformat**](/windows/win32/api/mmreg/ns-mmreg-waveformat) -Header gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="463d0-110">Because the data portion of a .wav file is a single block of uncompressed PCM audio, the media source does not need to read packet headers or otherwise parse the stream during playback, other than reading the initial [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) header.</span></span>

<span data-ttu-id="463d0-111">Ein erweitertes Beispiel für eine Medienquelle finden Sie im [MPEG1Source](mpeg1source-sample.md)-Beispiel.</span><span class="sxs-lookup"><span data-stu-id="463d0-111">For a more advanced example of a media source, see the [MPEG1Source Sample](mpeg1source-sample.md).</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="463d0-112">Gezeigte APIs</span><span class="sxs-lookup"><span data-stu-id="463d0-112">APIs Demonstrated</span></span>

<span data-ttu-id="463d0-113">In diesem Beispiel werden die folgenden Media Foundation Schnittstellen veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="463d0-113">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="463d0-114">**IMF bytestreamhandler**</span><span class="sxs-lookup"><span data-stu-id="463d0-114">**IMFByteStreamHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)
-   [<span data-ttu-id="463d0-115">**Imfmediasource**</span><span class="sxs-lookup"><span data-stu-id="463d0-115">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
-   [<span data-ttu-id="463d0-116">**IMF Media Stream**</span><span class="sxs-lookup"><span data-stu-id="463d0-116">**IMFMediaStream**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)

## <a name="usage"></a><span data-ttu-id="463d0-117">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="463d0-117">Usage</span></span>

<span data-ttu-id="463d0-118">Das wavsource-Beispiel erstellt eine DLL, bei der es sich um einen com-Server für den bytestreamhandler der Medienquelle und der Medienquelle handelt.</span><span class="sxs-lookup"><span data-stu-id="463d0-118">The WavSource sample builds a DLL that is a COM server for both the media source and media source's byte-stream handler.</span></span> <span data-ttu-id="463d0-119">Vor der Verwendung der Medienquelle müssen Sie die dll registrieren.</span><span class="sxs-lookup"><span data-stu-id="463d0-119">Before using the media source, you must register the DLL.</span></span>

<span data-ttu-id="463d0-120">Wenn Sie die Medienquelle verwenden möchten, können Sie die [basicplayback](/previous-versions//bb970475(v=vs.85))ausführen.</span><span class="sxs-lookup"><span data-stu-id="463d0-120">To use the media source, you can run the [BasicPlayback](/previous-versions//bb970475(v=vs.85)).</span></span> <span data-ttu-id="463d0-121">Der quellresolver lädt automatisch die Medienquelle, wenn Sie eine WAV-Datei für die Wiedergabe auswählen.</span><span class="sxs-lookup"><span data-stu-id="463d0-121">The source resolver will automatically load the media source if you select a .wav file for playback.</span></span> <span data-ttu-id="463d0-122">(Wenn ein Fehler auftritt, stellen Sie sicher, dass Sie die wavsource-dll erfolgreich registriert haben.)</span><span class="sxs-lookup"><span data-stu-id="463d0-122">(If an error occurs, make sure that you successfully registered the WavSource DLL.)</span></span>

<span data-ttu-id="463d0-123">Sie können auch das Tool topoedit verwenden, um eine Wiedergabe Topologie zu erstellen, die die Medienquelle enthält.</span><span class="sxs-lookup"><span data-stu-id="463d0-123">You can also use the TopoEdit tool to build a playback topology that contains the media source.</span></span> <span data-ttu-id="463d0-124">Weitere Informationen zu topoedit finden Sie unter [topoedit](topoedit.md).</span><span class="sxs-lookup"><span data-stu-id="463d0-124">For more information about TopoEdit, see [TopoEdit](topoedit.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="463d0-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="463d0-125">Requirements</span></span>



| <span data-ttu-id="463d0-126">Produkt</span><span class="sxs-lookup"><span data-stu-id="463d0-126">Product</span></span>                                                        | <span data-ttu-id="463d0-127">Version</span><span class="sxs-lookup"><span data-stu-id="463d0-127">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="463d0-128">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="463d0-128">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="463d0-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="463d0-129">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="463d0-130">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="463d0-130">Downloading the Sample</span></span>

<span data-ttu-id="463d0-131">Dieses Beispiel ist im [GitHub-Repository für klassische Windows-Beispiele](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsource)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="463d0-131">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsource).</span></span>

## <a name="related-topics"></a><span data-ttu-id="463d0-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="463d0-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="463d0-133">Media Foundation-SDK-Beispiele</span><span class="sxs-lookup"><span data-stu-id="463d0-133">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="463d0-134">Medienquellen</span><span class="sxs-lookup"><span data-stu-id="463d0-134">Media Sources</span></span>](media-sources.md)
</dt> <dt>

[<span data-ttu-id="463d0-135">MPEG1Source-Beispiel</span><span class="sxs-lookup"><span data-stu-id="463d0-135">MPEG1Source Sample</span></span>](mpeg1source-sample.md)
</dt> <dt>

[<span data-ttu-id="463d0-136">Schema Handler und Byte-Stream Handler</span><span class="sxs-lookup"><span data-stu-id="463d0-136">Scheme Handlers and Byte-Stream Handlers</span></span>](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[<span data-ttu-id="463d0-137">Schreiben einer benutzerdefinierten Medienquelle</span><span class="sxs-lookup"><span data-stu-id="463d0-137">Writing a Custom Media Source</span></span>](writing-a-custom-media-source.md)
</dt> </dl>

 

 
