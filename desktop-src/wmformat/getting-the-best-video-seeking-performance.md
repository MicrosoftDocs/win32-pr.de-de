---
title: Erzielen Sie das beste Video für die Suche nach Leistung
description: Erzielen Sie das beste Video für die Suche nach Leistung
ms.assetid: 21269f0c-fc3a-46fc-88b4-f71828b5d5a7
keywords:
- Windows Media-Format-SDK, beste Video Suchleistung
- Advanced Systems Format (ASF), beste Videosuche Leistung
- ASF (Advanced Systems Format), beste Video Suchleistung
- Advanced Systems Format (ASF), Videosuche Leistung
- ASF (Advanced Systems Format), Videosuche Leistung
- Advanced Systems Format (ASF), Leistung
- ASF (Advanced Systems Format), Leistung
- Videosuche
- Leistung, Videosuche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c95feb9158bbab09ce28024100f3ebbffb56ad9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341461"
---
# <a name="getting-the-best-video-seeking-performance"></a><span data-ttu-id="1cbc7-112">Erzielen Sie das beste Video für die Suche nach Leistung</span><span class="sxs-lookup"><span data-stu-id="1cbc7-112">Getting the Best Video Seeking Performance</span></span>

<span data-ttu-id="1cbc7-113">Das Suchen nach Inhalten in einer Datei ist ein sehr gängiger Vorgang, bei dem es sich um ein potenziell Leistungsproblem handelt.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-113">Seeking to content in a file is a very common operation that is potentially a performance issue.</span></span> <span data-ttu-id="1cbc7-114">Das mit dem Windows Media Video 9-Codec codierte Video besteht hauptsächlich aus Delta Frames, die nur die Änderungen in Bezug auf den vorherigen Frame aufzeichnen.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-114">Video encoded with the Windows Media Video 9 codec is made up primarily of delta frames, which only record the changes in relation to the previous frame.</span></span> <span data-ttu-id="1cbc7-115">Das erneute Erstellen von Delta Frames nimmt Zeit in Frage, insbesondere, wenn die Keyframes weit voneinander entfernt sind.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-115">Reconstructing delta frames takes time, particularly if the key frames are far apart.</span></span> <span data-ttu-id="1cbc7-116">Weitere Informationen zum Konfigurieren von Keyframes für die effiziente Suche finden Sie unter [Konfigurieren von Videostreams zum Suchen der Leistung](configuring-video-streams-for-seeking-performance.md).</span><span class="sxs-lookup"><span data-stu-id="1cbc7-116">For more information about configuring key frames for efficient seeking, see [Configuring Video Streams for Seeking Performance](configuring-video-streams-for-seeking-performance.md).</span></span>

<span data-ttu-id="1cbc7-117">Zusätzlich zur ordnungsgemäßen Konfiguration können Sie die Suchleistung verbessern, indem Sie die Frame Indizierung für den Videostream verwenden.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-117">In addition to proper configuration, you can improve seeking performance by using frame indexing for the video stream.</span></span> <span data-ttu-id="1cbc7-118">Es ist in der Regel schneller, eine Frame Nummer zu suchen, als eine Präsentationszeit zu suchen.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-118">Seeking to a frame number is typically faster than seeking to a presentation time.</span></span>

<span data-ttu-id="1cbc7-119">Wenn Sie in einer Datei mit mehreren Streams suchen, sollten Sie nur die benötigten Streams auswählen.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-119">If seeking in a file with multiple streams, you should select only the streams that are needed.</span></span> <span data-ttu-id="1cbc7-120">Jeder für das Lesen konfigurierte Stream wirkt sich auf die Leistung der Suche aus, da alle ausgewählten Streams synchronisiert werden, wenn Sie zu einem Punkt in einer Datei suchen.</span><span class="sxs-lookup"><span data-stu-id="1cbc7-120">Each stream configured for reading will affect the performance of seeking, because all selected streams are synchronized when you seek to a point in a file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1cbc7-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1cbc7-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1cbc7-122">**Lesen von ASF-Dateien**</span><span class="sxs-lookup"><span data-stu-id="1cbc7-122">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> <dt>

[<span data-ttu-id="1cbc7-123">**So suchen Sie nach der Frame Nummer mithilfe des asynchronen Readers**</span><span class="sxs-lookup"><span data-stu-id="1cbc7-123">**To Seek By Frame Number Using the Asynchronous Reader**</span></span>](to-seek-by-frame-number-using-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="1cbc7-124">**So suchen Sie nach Frame Nummer mithilfe des synchronen Readers**</span><span class="sxs-lookup"><span data-stu-id="1cbc7-124">**To Seek By Frame Number Using the Synchronous Reader**</span></span>](to-seek-by-frame-number-using-the-synchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="1cbc7-125">**So suchen Sie nach Zeit mithilfe des asynchronen Readers**</span><span class="sxs-lookup"><span data-stu-id="1cbc7-125">**To Seek By Time Using the Asynchronous Reader**</span></span>](to-seek-by-time-using-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="1cbc7-126">**So suchen Sie nach Zeit mithilfe des synchronen Readers**</span><span class="sxs-lookup"><span data-stu-id="1cbc7-126">**To Seek By Time Using the Synchronous Reader**</span></span>](to-seek-by-time-using-the-synchronous-reader.md)
</dt> </dl>

 

 




