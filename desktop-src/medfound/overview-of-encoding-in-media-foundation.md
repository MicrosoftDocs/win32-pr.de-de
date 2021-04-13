---
description: Dieses Thema bietet einen Überblick über die Datei Codierungs-APIs, die in Microsoft Media Foundation bereitgestellt werden.
ms.assetid: 69dbef63-e272-4ad2-8d04-ae9366f79b33
title: Übersicht über die Codierung in Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81882bd6da43f4040614347b662d988844c7b7a6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104559991"
---
# <a name="overview-of-encoding-in-media-foundation"></a><span data-ttu-id="f3539-103">Übersicht über die Codierung in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f3539-103">Overview of Encoding in Media Foundation</span></span>

<span data-ttu-id="f3539-104">Dieses Thema bietet einen Überblick über die Datei Codierungs-APIs, die in Microsoft Media Foundation bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="f3539-104">This topic is an overview of the file encoding APIs provided in Microsoft Media Foundation.</span></span>

## <a name="terminology"></a><span data-ttu-id="f3539-105">Begriff</span><span class="sxs-lookup"><span data-stu-id="f3539-105">Terminology</span></span>

<span data-ttu-id="f3539-106">Die *Codierung* ist ein allgemeiner Begriff, der mehrere verschiedene Prozesse abdeckt:</span><span class="sxs-lookup"><span data-stu-id="f3539-106">*Encoding* is a general term that covers several distinct processes:</span></span>

1.  <span data-ttu-id="f3539-107">Codieren eines Audiodaten-oder Videodaten Stroms in komprimierte Formate</span><span class="sxs-lookup"><span data-stu-id="f3539-107">Encoding an audio or video stream into a compressed formats.</span></span> <span data-ttu-id="f3539-108">Beispiel: Codieren eines Videodaten Stroms in H. 264-Video.</span><span class="sxs-lookup"><span data-stu-id="f3539-108">For example, encoding a video stream to H.264 video.</span></span>
2.  <span data-ttu-id="f3539-109">Multiplexing ("muxing") eines oder mehrerer Streams in einen einzelbytestream.</span><span class="sxs-lookup"><span data-stu-id="f3539-109">Multiplexing ("muxing") one or more streams into a single byte stream.</span></span> <span data-ttu-id="f3539-110">In der Regel werden die eingehenden Datenströme zuerst codiert.</span><span class="sxs-lookup"><span data-stu-id="f3539-110">Typically, the incoming streams are encoded first.</span></span> <span data-ttu-id="f3539-111">Dieser Schritt kann die packetisierung der codierten Streams einschließen.</span><span class="sxs-lookup"><span data-stu-id="f3539-111">This step might involve packetizing the encoded streams.</span></span>
3.  <span data-ttu-id="f3539-112">Schreiben eines Multiplex-Bytestreams in eine Datei, z. b. eine MP4-Datei oder eine ASF-Datei (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="f3539-112">Writing a multiplexed byte stream to a file, such as an MP4 or Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="f3539-113">Alternativ kann der Multiplex-Stream über das Netzwerk gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="f3539-113">Alternatively, the multiplexed stream can be sent over the network.</span></span>

<span data-ttu-id="f3539-114">Das folgende Diagramm zeigt diese drei Prozesse:</span><span class="sxs-lookup"><span data-stu-id="f3539-114">The following diagram shows these three processes:</span></span>

![Diagramm mit den Codierungs-und Multiplexing-Prozessen](images/encoding03.png)

<span data-ttu-id="f3539-116">Zu den Variationen dieses Prozesses zählen Transcodierung und remuxing:</span><span class="sxs-lookup"><span data-stu-id="f3539-116">Variations of this process include transcoding and remuxing:</span></span>

-   <span data-ttu-id="f3539-117">*Transcoding* bedeutet, dass eine vorhandene Datei decodiert, die Streams neu codiert und die codierten Streams erneut Multiplexing werden.</span><span class="sxs-lookup"><span data-stu-id="f3539-117">*Transcoding* means decoding an existing file, re-encoding the streams, and re-multiplexing the encoded streams.</span></span> <span data-ttu-id="f3539-118">Die Transcodierung kann durchgeführt werden, um eine Datei von einem Codierungstyp in einen anderen zu konvertieren. So konvertieren Sie z. b. das H. 264-Video in Windows Media Video (WMV).</span><span class="sxs-lookup"><span data-stu-id="f3539-118">Transcoding might be done to convert a file from one encoding type to another; for example, to convert H.264 video to Windows Media Video (WMV).</span></span> <span data-ttu-id="f3539-119">Außerdem kann die codierte Bitrate geändert werden. die Video Frame Größe; die Framerate. oder andere Format Parameter.</span><span class="sxs-lookup"><span data-stu-id="f3539-119">It can also be done to change the encoded bit rate; the video frame size; the frame rate; or other format parameters.</span></span>
-   <span data-ttu-id="f3539-120">*Remultiplexing* oder *remuxing* bedeutet, dass eine Datei Demultiplexing und die Streams erneut Multiplexing werden, ohne den Schritt "decodieren/codieren" zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="f3539-120">*Remultiplexing* or *remuxing* means demultiplexing a file and re-multiplexing the streams, with no decode/encode step.</span></span> <span data-ttu-id="f3539-121">Dies kann durchgeführt werden, um zu ändern, wie die Audiodateien bzw. Video Pakete mit einem multiplext versehen werden, um einen Stream zu entfernen oder um Streams aus zwei verschiedenen Quelldateien zu kombinieren</span><span class="sxs-lookup"><span data-stu-id="f3539-121">This might be done to change how the audio/video packets are multiplexed, to remove a stream, or to combine streams from two different source files.</span></span>
-   <span data-ttu-id="f3539-122">*Transrating* ist ein Sonderfall von Transcoding, bei dem die Bitrate geändert wird, ohne den Komprimierungstyp zu ändern.</span><span class="sxs-lookup"><span data-stu-id="f3539-122">*Transrating* is a special case of transcoding, where the bit-rate is changed without changing the compression type.</span></span> <span data-ttu-id="f3539-123">Beispielsweise können Sie eine Datei mit hoher Bitrate in eine niedrigere Bitrate konvertieren.</span><span class="sxs-lookup"><span data-stu-id="f3539-123">For example, you might convert a high-bit-rate file to a lower bit-rate.</span></span> <span data-ttu-id="f3539-124">Ein typisches Szenario, in dem die transbewertung verwendet werden kann, ist die Synchronisierung von Medieninhalten von einem PC mit einem tragbaren Gerät.</span><span class="sxs-lookup"><span data-stu-id="f3539-124">A typical scenario in which transrating might be used is when synchronizing media content from a PC to a portable device.</span></span> <span data-ttu-id="f3539-125">Wenn das portable Gerät keine hohe Bitrate unterstützt, wird die Datei möglicherweise vor dem Kopieren auf das portable Gerät abgehandelt.</span><span class="sxs-lookup"><span data-stu-id="f3539-125">If the portable device does not support a high bit rate, the file might be transrated before it is copied to the portable device.</span></span>

<span data-ttu-id="f3539-126">Das folgende Blockdiagramm zeigt den transcodierungsprozess.</span><span class="sxs-lookup"><span data-stu-id="f3539-126">The following block diagram shows the transcoding process.</span></span>

![Diagramm mit dem Transcodierungs Prozess](images/encoding05.png)

<span data-ttu-id="f3539-128">Das folgende Blockdiagramm zeigt den remuxing-Prozess.</span><span class="sxs-lookup"><span data-stu-id="f3539-128">The following block diagram shows the remuxing process.</span></span>

![Diagramm, das den remuxing-Prozess anzeigt](images/encoding06.png)

<span data-ttu-id="f3539-130">In dieser Dokumentation wird manchmal der Begriff *Codierung* verwendet, um sowohl Transcodierung als auch remuxing einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="f3539-130">This documentation sometimes uses the term *encoding* to include both transcoding and remuxing.</span></span> <span data-ttu-id="f3539-131">Wenn es wichtig ist, zwischen diesen zu unterscheiden, wird der Unterschied in der Dokumentation festzustellen.</span><span class="sxs-lookup"><span data-stu-id="f3539-131">When it is important to distinguish between them, the documentation will note the difference.</span></span>

<span data-ttu-id="f3539-132">Siehe auch: [Media Foundation: grundlegende Konzepte](media-foundation-programming--essential-concepts.md).</span><span class="sxs-lookup"><span data-stu-id="f3539-132">See also: [Media Foundation: Essential Concepts](media-foundation-programming--essential-concepts.md).</span></span>

## <a name="media-foundation-encoding-architecture"></a><span data-ttu-id="f3539-133">Media Foundation Codierungs Architektur</span><span class="sxs-lookup"><span data-stu-id="f3539-133">Media Foundation Encoding Architecture</span></span>

<span data-ttu-id="f3539-134">Auf der untersten Ebene der Media Foundation-Architektur werden die folgenden Typen von Komponenten für die Codierung verwendet:</span><span class="sxs-lookup"><span data-stu-id="f3539-134">At the lowest layer of the Media Foundation architecture, the following types of component are used for encoding:</span></span>

-   <span data-ttu-id="f3539-135">Für die Transcodierung werden [Medienquellen](media-sources.md) verwendet, um die Quelldatei zu dekodieren.</span><span class="sxs-lookup"><span data-stu-id="f3539-135">For transcoding, [Media Sources](media-sources.md) are used to demultiplex the source file.</span></span>
-   <span data-ttu-id="f3539-136">Beim Codierungsprozess werden [Media Foundation Transformationen](media-foundation-transforms.md) zum Decodieren und Codieren von Streams verwendet.</span><span class="sxs-lookup"><span data-stu-id="f3539-136">For the encoding process, [Media Foundation Transforms](media-foundation-transforms.md) are used to decode and encode streams.</span></span>
-   <span data-ttu-id="f3539-137">Für den Multiplexing-Prozess werden [Medien senken](media-sinks.md) verwendet, um die Streams zu Multiplexen und den Multiplexen Stream in eine Datei oder ein Netzwerk zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="f3539-137">For the multiplexing process, [Media Sinks](media-sinks.md) are used to multiplex the streams and write the multiplexed stream to a file or network.</span></span>

<span data-ttu-id="f3539-138">Das folgende Diagramm zeigt den Datenfluss zwischen diesen Komponenten in einem Transcodierungs Szenario:</span><span class="sxs-lookup"><span data-stu-id="f3539-138">The following diagram shows the data flow between these components in a transcoding scenario:</span></span>

![Diagramm mit den Komponenten, die bei der Transcodierung verwendet werden](images/encoding04.png)

<span data-ttu-id="f3539-140">Diese Komponenten werden von den meisten Anwendungen nicht direkt verwendet.</span><span class="sxs-lookup"><span data-stu-id="f3539-140">Most applications will not use these components directly.</span></span> <span data-ttu-id="f3539-141">Stattdessen werden von einer Anwendung APIs auf höherer Ebene verwendet, die diese untergeordneten Komponenten verwalten.</span><span class="sxs-lookup"><span data-stu-id="f3539-141">Instead, an application will use higher-level APIs that manage these lower-level components.</span></span> <span data-ttu-id="f3539-142">Media Foundation bietet zwei APIs auf höherer Ebene für die Codierung:</span><span class="sxs-lookup"><span data-stu-id="f3539-142">Media Foundation provides two higher-level APIs for encoding:</span></span>

<dl> <dt>

<span data-ttu-id="f3539-143"><span id="Media_Session"></span><span id="media_session"></span><span id="MEDIA_SESSION"></span>[Medien Sitzung](media-session.md)</span><span class="sxs-lookup"><span data-stu-id="f3539-143"><span id="Media_Session"></span><span id="media_session"></span><span id="MEDIA_SESSION"></span>[Media Session](media-session.md)</span></span>
</dt> <dd>

<span data-ttu-id="f3539-144">Die Medien Sitzung bietet eine End-to-End-Pipeline, mit der Daten aus der Medienquelle, über die Codecs und schließlich in die Medien Senke verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="f3539-144">The Media Session provides an end-to-end pipeline that moves data from the media source, through the codecs, and finally to the media sink.</span></span> <span data-ttu-id="f3539-145">Die Anwendung steuert die Medien Sitzung und empfängt Statusereignisse von der Medien Sitzung.</span><span class="sxs-lookup"><span data-stu-id="f3539-145">The application controls the Media Session and receives status events from the Media Session.</span></span>

</dd> <dt>

<span data-ttu-id="f3539-146"><span id="Source_Reader_plus_Sink_Writer"></span><span id="source_reader_plus_sink_writer"></span><span id="SOURCE_READER_PLUS_SINK_WRITER"></span>[Quell Leser](source-reader.md) Plus [Senke Writer](sink-writer.md)</span><span class="sxs-lookup"><span data-stu-id="f3539-146"><span id="Source_Reader_plus_Sink_Writer"></span><span id="source_reader_plus_sink_writer"></span><span id="SOURCE_READER_PLUS_SINK_WRITER"></span>[Source Reader](source-reader.md) plus [Sink Writer](sink-writer.md)</span></span>
</dt> <dd>

<span data-ttu-id="f3539-147">Der Quell Leser umschließt die Medienquelle und optional die Decoders.</span><span class="sxs-lookup"><span data-stu-id="f3539-147">The Source Reader wraps the media source and optionally the decoders.</span></span> <span data-ttu-id="f3539-148">Die Anwendung übermittelt entweder codierte oder decodierte Stichproben.</span><span class="sxs-lookup"><span data-stu-id="f3539-148">It delivers either encoded or decoded samples the application.</span></span> <span data-ttu-id="f3539-149">Der Senke-Writer umschließt die Medien Senke und optional die Encoder.</span><span class="sxs-lookup"><span data-stu-id="f3539-149">The Sink Writer wraps the media sink and optionally the encoders.</span></span> <span data-ttu-id="f3539-150">Die Anwendung übergibt Beispiele an den Senke-Writer.</span><span class="sxs-lookup"><span data-stu-id="f3539-150">The application passes samples to the Sink Writer.</span></span>

</dd> </dl>

<span data-ttu-id="f3539-151">Das folgende Diagramm zeigt die Medien Sitzung:</span><span class="sxs-lookup"><span data-stu-id="f3539-151">The following diagram shows the Media Session:</span></span>

![Diagramm, das zeigt, wie die Medien Sitzung die Transcodierung durchführt](images/encoding01.png)

<span data-ttu-id="f3539-153">Die [transcode-API](transcode-api.md) (das blaue schattierte Feld) ist ein Satz von APIs, die in Windows 7 eingeführt wurden, um die Konfiguration der Medien Sitzung für die Codierung zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="f3539-153">The [Transcode API](transcode-api.md) (the blue shaded box) is a set of APIs introduced in Windows 7, which make it easier to configure the Media Session for encoding.</span></span>

<span data-ttu-id="f3539-154">Das nächste Diagramm zeigt den Quell Reader und den Senke-Writer:</span><span class="sxs-lookup"><span data-stu-id="f3539-154">The next diagram shows the Source Reader and Sink Writer:</span></span>

![Diagramm, das die Transcodierung mit dem Quell-und senderwriter zeigt](images/encoding02.png)

## <a name="related-topics"></a><span data-ttu-id="f3539-156">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f3539-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3539-157">Codierung und Dateierstellung</span><span class="sxs-lookup"><span data-stu-id="f3539-157">Encoding and File Authoring</span></span>](encoding-and-file-authoring.md)
</dt> <dt>

[<span data-ttu-id="f3539-158">Media Foundation Programmierung: grundlegende Konzepte</span><span class="sxs-lookup"><span data-stu-id="f3539-158">Media Foundation Programming: Essential Concepts</span></span>](media-foundation-programming--essential-concepts.md)
</dt> </dl>

 

 



