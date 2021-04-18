---
title: Ändern der Größe von Videos
description: Ändern der Größe von Videos
ms.assetid: 38ecb729-68eb-4452-8389-cabe987fb8b6
keywords:
- Windows Media-Format-SDK, Videogröße ändern
- Windows Media-Format-SDK, Ändern der Größe von Videos
- Advanced Systems Format (ASF), Video-Größe ändern
- ASF (Advanced Systems Format), Video-Größe ändern
- Advanced Systems Format (ASF), Ändern der Größe von Videos
- ASF (Advanced Systems Format), Ändern der Größe von Videos
- Ändern der Größe von Videos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b200496b1dead3abacfbfad7674519e0cf7ce4f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206537"
---
# <a name="video-resizing"></a><span data-ttu-id="5146a-110">Ändern der Größe von Videos</span><span class="sxs-lookup"><span data-stu-id="5146a-110">Video Resizing</span></span>

<span data-ttu-id="5146a-111">Wenn Sie die Einstellungen für einen Videostream definieren, müssen Sie eine Breite und Höhe für die Videorahmen angeben.</span><span class="sxs-lookup"><span data-stu-id="5146a-111">When you define the settings for a video stream, you must specify a width and height for the video frames.</span></span> <span data-ttu-id="5146a-112">Diese Videogröße bestimmt die Größe der Video Frames, die im Daten Abschnitt der Datei codiert sind.</span><span class="sxs-lookup"><span data-stu-id="5146a-112">This video size determines the size of the video frames encoded in the data section of the file.</span></span> <span data-ttu-id="5146a-113">Die Videogröße in einem Profil bestimmt jedoch weder die Größe des Eingabe Mediums, das Sie an den Writer übermitteln, noch die Größe des Ausgabe Mediums, das Sie vom Reader erhalten.</span><span class="sxs-lookup"><span data-stu-id="5146a-113">However, the video size in a profile does not determine, or limit, the size of the input media that you deliver to the writer, or the size of the output media you receive from the reader.</span></span> <span data-ttu-id="5146a-114">Der Writer kann die Größe der Video Frames an die Anforderungen Ihrer Anwendung anpassen.</span><span class="sxs-lookup"><span data-stu-id="5146a-114">The writer can resize the video frames to suit the needs of your application.</span></span>

<span data-ttu-id="5146a-115">Die Video Bildgröße kann sich als dreistufige Vorgehensweise vorstellen: Eingabe Videogröße, streamvideo Größe und Ausgabevideo Größe.</span><span class="sxs-lookup"><span data-stu-id="5146a-115">Video image size can be thought of as going through three stages: input video size, stream video size, and output video size.</span></span>

<span data-ttu-id="5146a-116">Die Eingabe Videogröße ist die Größe der Frames, die Sie als Stichproben an das Writer-Objekt übergeben.</span><span class="sxs-lookup"><span data-stu-id="5146a-116">Input video size is the size of the frames that you pass as samples to the writer object.</span></span> <span data-ttu-id="5146a-117">Diese Größe wird als eine der erforderlichen Videoeingabe Eigenschaften definiert.</span><span class="sxs-lookup"><span data-stu-id="5146a-117">You define this size as one of the required video input properties.</span></span> <span data-ttu-id="5146a-118">Weitere Informationen zu Eingabe Eigenschaften finden [Sie unter Auflisten von Eingabe Formaten](to-enumerate-input-formats.md).</span><span class="sxs-lookup"><span data-stu-id="5146a-118">For more information about input properties, see [To Enumerate Input Formats](to-enumerate-input-formats.md).</span></span>

<span data-ttu-id="5146a-119">Stream Video size ist die Größe der Frames im Daten Abschnitt der ASF-Datei.</span><span class="sxs-lookup"><span data-stu-id="5146a-119">Stream video size is the size of the frames in the data section of the ASF file.</span></span> <span data-ttu-id="5146a-120">Sie definieren diese Größe als eine der erforderlichen Datenstrom-Konfigurationseinstellungen im Profil.</span><span class="sxs-lookup"><span data-stu-id="5146a-120">You define this size as one of the required stream configuration settings in the profile.</span></span> <span data-ttu-id="5146a-121">Wenn Sie eine Datei schreiben und die Eingabe Videogröße von der Größe des Stream-Videos abweicht, ändert der Writer die Rahmen der Codierung.</span><span class="sxs-lookup"><span data-stu-id="5146a-121">If you are writing a file and the input video size is different from the stream video size, the writer resizes the frames while encoding.</span></span> <span data-ttu-id="5146a-122">Weitere Informationen zu den Eigenschaften von Videostreams finden Sie unter [Konfigurieren von Videostreams](configuring-video-streams.md).</span><span class="sxs-lookup"><span data-stu-id="5146a-122">For more information about video stream properties, see [Configuring Video Streams](configuring-video-streams.md).</span></span>

<span data-ttu-id="5146a-123">Die Größe des Ausgabevideos ist die Größe der Frames, die vom Reader oder dem synchronen Reader bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="5146a-123">Output video size is the size of the frames delivered by the reader or synchronous reader.</span></span> <span data-ttu-id="5146a-124">Diese Größe wird als eine der erforderlichen Videoausgabe Eigenschaften definiert.</span><span class="sxs-lookup"><span data-stu-id="5146a-124">You define this size as one of the required video output properties.</span></span> <span data-ttu-id="5146a-125">Wenn Sie eine Datei lesen und sich die Ausgabevideo Größe von der Größe des Stream-Videos unterscheidet, ändert der Reader die Rahmen beim Decodieren.</span><span class="sxs-lookup"><span data-stu-id="5146a-125">If you are reading a file and the output video size is different from the stream video size, the reader resizes the frames while decoding.</span></span>

<span data-ttu-id="5146a-126">Sie können die Größe eines streamvideos nicht auf eine ungerade Anzahl von Pixel Breite festlegen.</span><span class="sxs-lookup"><span data-stu-id="5146a-126">You cannot set a stream video size to an odd number of pixels wide.</span></span> <span data-ttu-id="5146a-127">Wenn Sie die Breite eines Videostreams auf einen ungeraden Wert festlegen, wird das Profil entweder nicht vom Writer akzeptiert, oder das resultierende Video wird mit einer schwarzen Zeile nach unten codiert, um den Unterschied zu bilden.</span><span class="sxs-lookup"><span data-stu-id="5146a-127">If you set the width of a video stream to an odd value, either the profile will not be accepted by the writer, or the resulting video will be encoded with a black line down one side to make up the difference.</span></span>

<span data-ttu-id="5146a-128">Beim Ändern der Größe des Videos sollten Sie sorgfältig vorgehen.</span><span class="sxs-lookup"><span data-stu-id="5146a-128">You should take care when resizing video.</span></span> <span data-ttu-id="5146a-129">Images werden bei ihrer ursprünglichen Auflösung tendenziell am besten aussehen.</span><span class="sxs-lookup"><span data-stu-id="5146a-129">Images tend to look their best at their original resolution.</span></span> <span data-ttu-id="5146a-130">Das Ändern der Größe von Bildern kann häufig zu einer Verzerrung und zum Durchführen von Text führen.</span><span class="sxs-lookup"><span data-stu-id="5146a-130">Resizing images can often cause distortion and make text illegible.</span></span> <span data-ttu-id="5146a-131">Wenn Sie Video auf eine niedrige Bitrate komprimieren, werden Sie auch feststellen, dass die Änderung der Größe der Größe zu schwerwiegenden Komprimierungs Artefakten führen kann.</span><span class="sxs-lookup"><span data-stu-id="5146a-131">If you are compressing video to a low bit rate, you will also find that resizing distortions can lead to severe compression artifacts.</span></span>

<span data-ttu-id="5146a-132">Der Windows Media Video 9-Bildschirm Codec unterstützt das Ändern der Größe nicht.</span><span class="sxs-lookup"><span data-stu-id="5146a-132">The Windows Media Video 9 Screen codec does not support resizing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5146a-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5146a-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5146a-134">**Funktionen zum Schreiben von Dateien**</span><span class="sxs-lookup"><span data-stu-id="5146a-134">**File Writing Features**</span></span>](file-writing-features.md)
</dt> <dt>

[<span data-ttu-id="5146a-135">**Arbeiten mit Eingaben**</span><span class="sxs-lookup"><span data-stu-id="5146a-135">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> <dt>

[<span data-ttu-id="5146a-136">**Arbeiten mit Ausgaben**</span><span class="sxs-lookup"><span data-stu-id="5146a-136">**Working with Outputs**</span></span>](working-with-outputs.md)
</dt> </dl>

 

 




