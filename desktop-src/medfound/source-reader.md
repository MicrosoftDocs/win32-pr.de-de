---
description: Der Quell Leser ist eine Alternative zur Verwendung der Medien Sitzung und der Microsoft Media Foundation Pipeline zum Verarbeiten von Mediendaten.
ms.assetid: 8a17a754-53ef-4c05-9189-7978d864b17a
title: Quell Leser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ba67b32fba7fcf899f339e9e2d0512d2574bad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527830"
---
# <a name="source-reader"></a><span data-ttu-id="219d5-103">Quell Leser</span><span class="sxs-lookup"><span data-stu-id="219d5-103">Source Reader</span></span>

<span data-ttu-id="219d5-104">Der Quell Leser ist eine Alternative zur Verwendung der [Medien Sitzung](media-session.md) und der Microsoft Media Foundation Pipeline zum Verarbeiten von Mediendaten.</span><span class="sxs-lookup"><span data-stu-id="219d5-104">The Source Reader is an alternative to using the [Media Session](media-session.md) and the Microsoft Media Foundation pipeline to process media data.</span></span>

## <a name="why-use-the-source-reader"></a><span data-ttu-id="219d5-105">Gründe für die Verwendung des Quell Readers</span><span class="sxs-lookup"><span data-stu-id="219d5-105">Why Use the Source Reader?</span></span>

<span data-ttu-id="219d5-106">Media Foundation eine Pipeline bereitstellt, die für die Wiedergabe optimiert ist.</span><span class="sxs-lookup"><span data-stu-id="219d5-106">Media Foundation provides a pipeline that is optimized for playback.</span></span> <span data-ttu-id="219d5-107">Die Pipeline ist End-to-End, d. h., Sie verarbeitet den Datenfluss von der Quelle (z. b. eine Videodatei) bis zum Ziel (z. b. die Grafik Anzeige).</span><span class="sxs-lookup"><span data-stu-id="219d5-107">The pipeline is end-to-end, meaning it handles data flow from the source (such as a video file) all the way to the destination (such as the graphics display).</span></span> <span data-ttu-id="219d5-108">Wenn Sie jedoch die Daten beim Durchlaufen der Pipeline lesen oder ändern möchten, müssen Sie ein benutzerdefiniertes Plug-in schreiben.</span><span class="sxs-lookup"><span data-stu-id="219d5-108">However, if you want to read or modify the data as it goes through the pipeline, you must write a custom plug-in.</span></span> <span data-ttu-id="219d5-109">Dies erfordert eine recht tiefe Kenntnis der Media Foundation Pipeline.</span><span class="sxs-lookup"><span data-stu-id="219d5-109">That requires a fairly deep knowledge of the Media Foundation pipeline.</span></span> <span data-ttu-id="219d5-110">Für bestimmte Aufgaben ist das Erstellen eines neuen Plug-ins zu viel mehr Aufwand.</span><span class="sxs-lookup"><span data-stu-id="219d5-110">For certain tasks, creating a new plug-in is too much overhead.</span></span> <span data-ttu-id="219d5-111">Der Quell Leser ist für diese Art von Situation konzipiert, wenn Sie die Rohdaten aus einer Quelle ohne den Aufwand der gesamten Pipeline erhalten möchten.</span><span class="sxs-lookup"><span data-stu-id="219d5-111">The source reader is designed for this type of situation, when you want to get the raw data from a source without the overhead of the entire pipeline.</span></span>

<span data-ttu-id="219d5-112">Intern enthält der Quell Leser einen Zeiger auf eine Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="219d5-112">Internally, the source reader holds a pointer to a media source.</span></span> <span data-ttu-id="219d5-113">Eine *Medienquelle* ist ein Media Foundation Objekt, das Mediendaten aus einer externen Quelle, z. b. einer Mediendatei oder einem Video Erfassungsgerät, generiert.</span><span class="sxs-lookup"><span data-stu-id="219d5-113">A *media source* is a Media Foundation object that generates media data from an external source, such as a media file or video capture device.</span></span> <span data-ttu-id="219d5-114">Der Quell Leser verwaltet alle Methodenaufrufe der Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="219d5-114">The source reader manages all of the method calls to the media source.</span></span> <span data-ttu-id="219d5-115">(Weitere Informationen zu Medienquellen finden Sie unter [Medienquellen](media-sources.md).)</span><span class="sxs-lookup"><span data-stu-id="219d5-115">(For more information about media sources, see [Media Sources](media-sources.md).)</span></span>

<span data-ttu-id="219d5-116">Wenn die Medienquelle komprimierte Daten bereitstellt, können Sie die Daten mithilfe des Quell Readers decodieren.</span><span class="sxs-lookup"><span data-stu-id="219d5-116">If the media source delivers compressed data, you can use the source reader to decode the data.</span></span> <span data-ttu-id="219d5-117">In diesem Fall lädt der Quell Leser den richtigen Decoder und verwaltet den Datenfluss zwischen der Medienquelle und dem Decoder.</span><span class="sxs-lookup"><span data-stu-id="219d5-117">In that case, the source reader will load the correct decoder and manage the data flow between the media source and the decoder.</span></span> <span data-ttu-id="219d5-118">Der Quell Leser kann auch eine begrenzte Videoverarbeitung durchführen: Farbkonvertierung von YUV zu RGB-32 und Software Deinterlacing, obwohl diese Vorgänge für Video Rendering in Echtzeit nicht empfohlen werden.</span><span class="sxs-lookup"><span data-stu-id="219d5-118">The source reader can also perform some limited video processing: color conversion from YUV to RGB-32, and software deinterlacing, although these operations are not recommended for real-time video rendering.</span></span> <span data-ttu-id="219d5-119">Dieses Verfahren wird in der folgenden Abbildung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="219d5-119">The following image illustrates this process.</span></span>

![Diagramm des Quell Readers](images/sourcereader.png)

<span data-ttu-id="219d5-121">Der Quell Leser sendet die Daten nicht an ein Ziel. die Anwendung kann die Daten nutzen.</span><span class="sxs-lookup"><span data-stu-id="219d5-121">The source reader does not send the data to a destination; it is up to the application to consume the data.</span></span> <span data-ttu-id="219d5-122">Der Quell Leser kann z. b. eine Videodatei lesen, aber das Video wird nicht auf dem Bildschirm angezeigt.</span><span class="sxs-lookup"><span data-stu-id="219d5-122">For example, the source reader can read a video file, but it will not render the video to the screen.</span></span> <span data-ttu-id="219d5-123">Außerdem verwaltet der Quell Leser keine Präsentations Uhr, behandelt Zeit Steuerungsprobleme oder synchronisiert Videos mit Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="219d5-123">Also, the source reader does not manage a presentation clock, handle timing issues, or synchronize video with audio.</span></span>

<span data-ttu-id="219d5-124">Verwenden Sie ggf. den Quell Leser:</span><span class="sxs-lookup"><span data-stu-id="219d5-124">Consider using the source reader when:</span></span>

-   <span data-ttu-id="219d5-125">Sie möchten Daten aus einer Mediendatei erhalten, ohne sich Gedanken über die zugrunde liegende Dateistruktur machen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="219d5-125">You want to get data from a media file without worrying about the underlying file structure.</span></span>
-   <span data-ttu-id="219d5-126">Sie möchten Daten von einem Audiogerät oder Video Erfassungsgerät erhalten.</span><span class="sxs-lookup"><span data-stu-id="219d5-126">You want to get data from an audio or video capture device.</span></span>
-   <span data-ttu-id="219d5-127">Ihre Datenverarbeitungs Aufgaben sind nicht Zeit empfindlich, oder Sie benötigen keine Präsentations Uhr.</span><span class="sxs-lookup"><span data-stu-id="219d5-127">Your data-processing tasks are not time sensitive, or you do not require a presentation clock.</span></span>
-   <span data-ttu-id="219d5-128">Sie verfügen bereits über eine Medien Pipeline, die nicht auf Media Foundation basiert, und Sie möchten die Media Foundation Medienquellen in Ihre eigene Pipeline integrieren.</span><span class="sxs-lookup"><span data-stu-id="219d5-128">You already have a media pipeline that is not based on Media Foundation, and you want to incorporate the Media Foundation media sources into your own pipeline.</span></span>

<span data-ttu-id="219d5-129">Der Quell Leser wird in den folgenden Situationen nicht empfohlen:</span><span class="sxs-lookup"><span data-stu-id="219d5-129">The source reader is not recommended in the following situations:</span></span>

-   <span data-ttu-id="219d5-130">Für geschützten Inhalt.</span><span class="sxs-lookup"><span data-stu-id="219d5-130">For protected content.</span></span> <span data-ttu-id="219d5-131">Der Quell Leser unterstützt Digital Rights Management (DRM) nicht.</span><span class="sxs-lookup"><span data-stu-id="219d5-131">The source reader does not support digital rights management (DRM).</span></span>
-   <span data-ttu-id="219d5-132">Wenn Sie sich für die Details der zugrunde liegenden Dateistruktur interessieren.</span><span class="sxs-lookup"><span data-stu-id="219d5-132">If you care about the details of the underlying file structure.</span></span> <span data-ttu-id="219d5-133">Der Quell Reader verbirgt diese Art von Details.</span><span class="sxs-lookup"><span data-stu-id="219d5-133">The source reader hides that type of detail.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="219d5-134">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="219d5-134">In this section</span></span>



| <span data-ttu-id="219d5-135">Thema</span><span class="sxs-lookup"><span data-stu-id="219d5-135">Topic</span></span>                                                                                                        | <span data-ttu-id="219d5-136">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="219d5-136">Description</span></span>                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="219d5-137">Verwenden des Quell Readers zum Verarbeiten von Mediendaten</span><span class="sxs-lookup"><span data-stu-id="219d5-137">Using the Source Reader to Process Media Data</span></span>](processing-media-data-with-the-source-reader.md)<br/> | <span data-ttu-id="219d5-138">In diesem Thema wird beschrieben, wie Sie den Quell Leser zum Verarbeiten von Mediendaten verwenden können.</span><span class="sxs-lookup"><span data-stu-id="219d5-138">This topic describes how to use the Source Reader to process media data.</span></span><br/>                                               |
| [<span data-ttu-id="219d5-139">Verwenden des Quell Readers im asynchronen Modus</span><span class="sxs-lookup"><span data-stu-id="219d5-139">Using the Source Reader in Asynchronous Mode</span></span>](using-the-source-reader-in-asynchronous-mode.md)<br/>  | <span data-ttu-id="219d5-140">In diesem Thema wird beschrieben, wie der Quell Leser im asynchronen Modus verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="219d5-140">This topic describes how to use the Source Reader in asynchronous mode.</span></span><br/>                                                |
| [<span data-ttu-id="219d5-141">Tutorial: Decodieren von Audiodaten</span><span class="sxs-lookup"><span data-stu-id="219d5-141">Tutorial: Decoding Audio</span></span>](tutorial--decoding-audio.md)<br/>                                          | <span data-ttu-id="219d5-142">In diesem Tutorial wird gezeigt, wie Sie den Quell Leser zum Decodieren von Audiodaten aus einer Mediendatei und zum Schreiben der Audiodatei in eine Wave-Datei verwenden.</span><span class="sxs-lookup"><span data-stu-id="219d5-142">This tutorial shows how to use the Source Reader to decode audio from a media file and write the audio to a WAVE file.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="219d5-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="219d5-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="219d5-144">Media Foundation-Architektur</span><span class="sxs-lookup"><span data-stu-id="219d5-144">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> <dt>

[<span data-ttu-id="219d5-145">Media Foundation-Programmier Handbuch</span><span class="sxs-lookup"><span data-stu-id="219d5-145">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="219d5-146">**IMFSourceReader**</span><span class="sxs-lookup"><span data-stu-id="219d5-146">**IMFSourceReader**</span></span>](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)
</dt> </dl>

 

 




