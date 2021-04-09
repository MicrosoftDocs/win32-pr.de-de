---
title: Audiodaten und Videostreams
description: Audiodaten und Videostreams
ms.assetid: 809e5bb6-2bc4-4022-9117-a2be5418d7d1
keywords:
- Windows Media-Format-SDK, Audiodatenströme
- Advanced Systems Format (ASF), Audiostreams
- ASF (Advanced Systems Format), Audiostreams
- Windows Media-Format-SDK, Videostreams
- Advanced Systems Format (ASF), Videostreams
- ASF (Advanced Systems Format), Videostreams
- Windows Media-Format-SDK, Streams
- Advanced Systems Format (ASF), Streams
- ASF (Advanced Systems Format), Streams
- Audiodatenströme, Informationen
- Videostreams, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d72eb46a6fb19129da2b9a841eab1710da47013
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036893"
---
# <a name="audio-and-video-streams"></a><span data-ttu-id="24e05-114">Audiodaten und Videostreams</span><span class="sxs-lookup"><span data-stu-id="24e05-114">Audio and Video Streams</span></span>

<span data-ttu-id="24e05-115">Die gängigsten Typen von Streams, die in Dateien verwendet werden, die mit dem Windows Media-Format-SDK erstellt wurden, sind Audio-und Videostreams.</span><span class="sxs-lookup"><span data-stu-id="24e05-115">The most common types of streams used in files created by using the Windows Media Format SDK are audio and video streams.</span></span> <span data-ttu-id="24e05-116">Digitale Darstellungen von Audiodaten und Videodaten sind komplex und belegen große Mengen an Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="24e05-116">Digital representations of audio and video data are complex and take up large amounts of memory.</span></span> <span data-ttu-id="24e05-117">In den meisten Fällen werden sowohl Audiodaten als auch Videos komprimiert, bevor Sie zu einer ASF-Datei hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="24e05-117">Under most circumstances, both audio and video are compressed before being added to an ASF file.</span></span> <span data-ttu-id="24e05-118">Die Komprimierung wird mithilfe von "Kompressor/Debug (Codec)" durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="24e05-118">Compression is accomplished using a compressor/decompressor (codec).</span></span>

<span data-ttu-id="24e05-119">In diesem SDK sind mehrere Windows Media Codecs enthalten, die eine hervorragende Qualitäts Komprimierung für digitale Medien bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="24e05-119">Several Windows Media codecs are included with this SDK, and they provide excellent quality compression for digital media.</span></span> <span data-ttu-id="24e05-120">Weitere Informationen zu den Windows Media-Codecs finden Sie unter [Codec-Features](codec-features.md).</span><span class="sxs-lookup"><span data-stu-id="24e05-120">For more information about the Windows Media codecs, see [Codec Features](codec-features.md).</span></span> <span data-ttu-id="24e05-121">Viele andere Codecs sind aus verschiedenen Quellen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="24e05-121">Many other codecs are available from various sources.</span></span> <span data-ttu-id="24e05-122">Beim Erstellen von ASF-Dateien können Sie die gewünschten Codecs verwenden, aber nur die Windows Media-Codecs werden direkt von den Objekten dieses SDK unterstützt.</span><span class="sxs-lookup"><span data-stu-id="24e05-122">You can use whatever codecs you like when creating ASF files, but only the Windows Media codecs are directly supported by the objects of this SDK.</span></span> <span data-ttu-id="24e05-123">Um andere Codecs verwenden zu können, müssen Sie die Beispiele komprimieren und Sie als beliebige Daten an das Writer-Objekt übergeben.</span><span class="sxs-lookup"><span data-stu-id="24e05-123">To use other codecs, you must compress samples and pass them to the writer object as arbitrary data.</span></span>

<span data-ttu-id="24e05-124">Der wichtigste Unterschied zwischen Audio-oder Videostreams und beliebigen Streams besteht darin, dass Datenströme, die Windows Media-Audiodaten oder Videodaten enthalten, von den Objekten des Windows Media Format SDK überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="24e05-124">The most important distinction between audio or video streams and arbitrary streams is that streams containing Windows Media audio or video data are validated by the objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="24e05-125">Beliebige Datenströme werden nicht automatisch überprüft und sollten von Ihrer Anwendung auf Integrität überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="24e05-125">Arbitrary data streams are not validated automatically, and should be checked for integrity by your application.</span></span>

<span data-ttu-id="24e05-126">Die Eigenschaften eines Audiostreams oder Videostreams werden im Profil beschrieben, das zum Erstellen der Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="24e05-126">The properties of an audio or video stream are described in the profile used to create the file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="24e05-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="24e05-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24e05-128">**Beliebige Streams**</span><span class="sxs-lookup"><span data-stu-id="24e05-128">**Arbitrary Streams**</span></span>](arbitrary-streams.md)
</dt> <dt>

[<span data-ttu-id="24e05-129">**Funktionen der ASF-Datei**</span><span class="sxs-lookup"><span data-stu-id="24e05-129">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="24e05-130">**Arbeiten mit Profilen**</span><span class="sxs-lookup"><span data-stu-id="24e05-130">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 

 




