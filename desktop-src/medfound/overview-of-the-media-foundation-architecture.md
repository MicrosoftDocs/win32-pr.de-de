---
description: In diesem Thema wird der allgemeine Entwurf von Microsoft Media Foundation beschrieben. Weitere Informationen zum Verwenden von Media Foundation für bestimmte Programmieraufgaben finden Sie unter Media Foundation Programming Guide.
ms.assetid: DEA2B19A-CF15-4BF4-84C3-9A6417C942E2
title: Übersicht über die Media Foundation-Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0944eae1a74c1a5ba3dda8d94b69088128237f1
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104562529"
---
# <a name="overview-of-the-media-foundation-architecture"></a><span data-ttu-id="3ac70-104">Übersicht über die Media Foundation-Architektur</span><span class="sxs-lookup"><span data-stu-id="3ac70-104">Overview of the Media Foundation Architecture</span></span>

<span data-ttu-id="3ac70-105">In diesem Thema wird der allgemeine Entwurf von Microsoft Media Foundation beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3ac70-105">This topic describes the general design of Microsoft Media Foundation.</span></span> <span data-ttu-id="3ac70-106">Weitere Informationen zum Verwenden von Media Foundation für bestimmte Programmieraufgaben finden Sie unter [Media Foundation Programming Guide](media-foundation-programming-guide.md).</span><span class="sxs-lookup"><span data-stu-id="3ac70-106">For information about using Media Foundation for specific programming tasks, see [Media Foundation Programming Guide](media-foundation-programming-guide.md).</span></span>

<span data-ttu-id="3ac70-107">Das folgende Diagramm zeigt eine allgemeine Übersicht über die Media Foundation Architektur.</span><span class="sxs-lookup"><span data-stu-id="3ac70-107">The following diagram shows a high-level view of the Media Foundation architecture.</span></span>

![das Diagramm zeigt eine allgemeine Übersicht über die Media Foundation-Architektur.](images/mfarch01.png)

<span data-ttu-id="3ac70-109">Media Foundation bietet zwei unterschiedliche Programmier Modelle.</span><span class="sxs-lookup"><span data-stu-id="3ac70-109">Media Foundation provides two distinct programming models.</span></span> <span data-ttu-id="3ac70-110">Das erste Modell, das auf der linken Seite des Diagramms angezeigt wird, verwendet eine End-to-End-Pipeline für Mediendaten.</span><span class="sxs-lookup"><span data-stu-id="3ac70-110">The first model, shown on the left side of the diagram, uses an end-to-end pipeline for media data.</span></span> <span data-ttu-id="3ac70-111">Die Anwendung initialisiert die Pipeline – beispielsweise durch Bereitstellen der URL einer wieder zugebende Datei – und ruft dann Methoden zum Steuern des Streamings auf.</span><span class="sxs-lookup"><span data-stu-id="3ac70-111">The application initializes the pipeline—for example, by providing the URL of a file to play—and then calls methods to control streaming.</span></span> <span data-ttu-id="3ac70-112">Im zweiten Modell, das auf der rechten Seite des Diagramms angezeigt wird, ruft die Anwendung Daten entweder aus einer Quelle ab oder schiebt sie an ein Ziel (oder beides).</span><span class="sxs-lookup"><span data-stu-id="3ac70-112">In the second model, shown on the right side of the diagram, the application either pulls data from a source, or pushes it to a destination (or both).</span></span> <span data-ttu-id="3ac70-113">Dieses Modell ist besonders nützlich, wenn Sie die Daten verarbeiten müssen, da die Anwendung direkten Zugriff auf den Datenstrom hat.</span><span class="sxs-lookup"><span data-stu-id="3ac70-113">This model is particularly useful if you need to process the data, because the application has direct access to the data stream.</span></span>

### <a name="primitives-and-platform"></a><span data-ttu-id="3ac70-114">Primitive und Plattform</span><span class="sxs-lookup"><span data-stu-id="3ac70-114">Primitives and Platform</span></span>

<span data-ttu-id="3ac70-115">Beginnend am unteren Rand des Diagramms sind die *primitiven* Hilfsobjekte, die in der Media Foundation-API verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="3ac70-115">Starting from the bottom of the diagram, the *primitives* are helper objects used throughout the Media Foundation API:</span></span>

-   <span data-ttu-id="3ac70-116">[Attribute](attributes-and-properties.md) sind eine generische Methode zum Speichern von Informationen in einem Objekt als Liste von Schlüssel-Wert-Paaren.</span><span class="sxs-lookup"><span data-stu-id="3ac70-116">[Attributes](attributes-and-properties.md) are a generic way to store information inside an object, as a list of key/value pairs.</span></span>
-   <span data-ttu-id="3ac70-117">[Medientypen](media-types.md) beschreiben das Format eines Mediendaten Stroms.</span><span class="sxs-lookup"><span data-stu-id="3ac70-117">[Media Types](media-types.md) describe the format of a media data stream.</span></span>
-   <span data-ttu-id="3ac70-118">[Medien Puffer](media-buffers.md) enthalten Blöcke von Mediendaten, z. b. Video Frames und Audiobeispiele, und werden zum Transportieren von Daten zwischen Objekten verwendet.</span><span class="sxs-lookup"><span data-stu-id="3ac70-118">[Media Buffers](media-buffers.md) hold chunks of media data, such as video frames and audio samples, and are used to transport data between objects.</span></span>
-   <span data-ttu-id="3ac70-119">[Medien Beispiele](media-samples.md) sind Container für Medien Puffer.</span><span class="sxs-lookup"><span data-stu-id="3ac70-119">[Media Samples](media-samples.md) are containers for media buffers.</span></span> <span data-ttu-id="3ac70-120">Sie enthalten außerdem Metadaten zu den Puffern, z. b. Zeitstempel.</span><span class="sxs-lookup"><span data-stu-id="3ac70-120">They also contain metadata about the buffers, such as time stamps.</span></span>

<span data-ttu-id="3ac70-121">Die [Media Foundation Plattform-APIs](media-foundation-platform-apis.md) stellen einige Kernfunktionen bereit, die von der Media Foundation Pipeline verwendet werden, wie z. b. asynchrone Rückrufe und Arbeits Warteschlangen.</span><span class="sxs-lookup"><span data-stu-id="3ac70-121">The [Media Foundation Platform APIs](media-foundation-platform-apis.md) provide some core functionality that is used by the Media Foundation pipeline, such as asynchronous callbacks and work queues.</span></span> <span data-ttu-id="3ac70-122">Bestimmte Anwendungen müssen diese APIs möglicherweise direkt aufzurufen. Sie benötigen Sie auch, wenn Sie eine benutzerdefinierte Quelle, eine Transformation oder eine Senke für Media Foundation implementieren.</span><span class="sxs-lookup"><span data-stu-id="3ac70-122">Certain applications might need to call these APIs directly; also, you will need them if you implement a custom source, transform, or sink for Media Foundation.</span></span>

### <a name="media-pipeline"></a><span data-ttu-id="3ac70-123">Medien Pipeline</span><span class="sxs-lookup"><span data-stu-id="3ac70-123">Media Pipeline</span></span>

<span data-ttu-id="3ac70-124">Die Medien Pipeline enthält drei Typen von Objekten, die Mediendaten generieren oder verarbeiten:</span><span class="sxs-lookup"><span data-stu-id="3ac70-124">The media pipeline contains three types of object that generate or process media data:</span></span>

-   <span data-ttu-id="3ac70-125">[Medienquellen](media-sources.md) stellen Daten in die Pipeline ein.</span><span class="sxs-lookup"><span data-stu-id="3ac70-125">[Media Sources](media-sources.md) introduce data into the pipeline.</span></span> <span data-ttu-id="3ac70-126">Eine Medienquelle erhält möglicherweise Daten aus einer lokalen Datei, z. b. einer Videodatei. aus einem Netzwerkstream oder von einem Hardware Erfassungsgerät aus.</span><span class="sxs-lookup"><span data-stu-id="3ac70-126">A media source might get data from a local file, such as a video file; from a network stream; or from a hardware capture device.</span></span>
-   <span data-ttu-id="3ac70-127">[Media Foundation Transformationen](media-foundation-transforms.md) (MFTs) verarbeiten von Daten aus einem Stream.</span><span class="sxs-lookup"><span data-stu-id="3ac70-127">[Media Foundation Transforms](media-foundation-transforms.md) (MFTs) process data from a stream.</span></span> <span data-ttu-id="3ac70-128">Encoder und Decoder werden als MFTs implementiert.</span><span class="sxs-lookup"><span data-stu-id="3ac70-128">Encoders and decoders are implemented as MFTs.</span></span>
-   <span data-ttu-id="3ac70-129">[Medien senken](media-sinks.md) nutzen die Daten. beispielsweise durch das Anzeigen von Videos in der Anzeige, das Abspielen von Audiodaten oder das Schreiben der Daten in eine Mediendatei.</span><span class="sxs-lookup"><span data-stu-id="3ac70-129">[Media Sinks](media-sinks.md) consume the data; for example, by showing video on the display, playing audio, or writing the data to a media file.</span></span>

<span data-ttu-id="3ac70-130">Drittanbieter können Ihre eigenen benutzerdefinierten Quellen, senken und MFTs implementieren. beispielsweise, um neue Mediendatei Formate zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="3ac70-130">Third parties can implement their own custom sources, sinks, and MFTs; for example, to support new media file formats.</span></span>

<span data-ttu-id="3ac70-131">Die [Medien Sitzung](media-session.md) steuert den Datenfluss über die Pipeline und behandelt Aufgaben wie die Qualitätskontrolle, die Audio-/Videosynchronisierung und die Reaktion auf Formatänderungen.</span><span class="sxs-lookup"><span data-stu-id="3ac70-131">The [Media Session](media-session.md) controls the flow of data through the pipeline, and handles tasks such as quality control, audio/video synchronization, and responding to format changes.</span></span>

### <a name="source-reader-and-sink-writer"></a><span data-ttu-id="3ac70-132">Quell Lese-und Senke-Writer</span><span class="sxs-lookup"><span data-stu-id="3ac70-132">Source Reader and Sink Writer</span></span>

<span data-ttu-id="3ac70-133">Der [Quell Reader](source-reader.md) und der [senkenwriter](sink-writer.md) bieten eine alternative Möglichkeit, die grundlegenden Media Foundation Komponenten (Medienquellen, Transformationen und Medien senken) zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="3ac70-133">The [Source Reader](source-reader.md) and [Sink Writer](sink-writer.md) provide an alternative way to use the basic Media Foundation components (media sources, transforms, and media sinks).</span></span> <span data-ttu-id="3ac70-134">Der Quell Leser hostet eine Medienquelle und NULL oder mehr Decoders, während der Senke Writer eine Medien Senke und NULL oder mehr Encoder hostet.</span><span class="sxs-lookup"><span data-stu-id="3ac70-134">The source reader hosts a media source and zero or more decoders, while the sink writer hosts a media sink and zero or more encoders.</span></span> <span data-ttu-id="3ac70-135">Sie können den Quell Reader verwenden, um komprimierte oder unkomprimierte Daten aus einer Medienquelle zu erhalten, und den sendenden Writer verwenden, um Daten zu codieren und die Daten an eine Medien Senke zu senden.</span><span class="sxs-lookup"><span data-stu-id="3ac70-135">You can use the source reader to get compressed or uncompressed data from a media source, and use the sink writer to encode data and send the data to a media sink.</span></span>

> [!Note]  
> <span data-ttu-id="3ac70-136">Der Quell Reader und der Senke Writer sind in Windows 7 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3ac70-136">The source reader and sink writer are available in Windows 7.</span></span>

 

<span data-ttu-id="3ac70-137">Dieses Programmiermodell ermöglicht der Anwendung eine bessere Kontrolle über den Datenfluss. Außerdem erhält die Anwendung direkten Zugriff auf die Daten aus der Quelle.</span><span class="sxs-lookup"><span data-stu-id="3ac70-137">This programming model gives the application more control over the flow of data, and also gives the application direct access to the data from the source.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ac70-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3ac70-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ac70-139">Media Foundation: Grundlegende Konzepte</span><span class="sxs-lookup"><span data-stu-id="3ac70-139">Media Foundation: Essential Concepts</span></span>](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[<span data-ttu-id="3ac70-140">Media Foundation-Architektur</span><span class="sxs-lookup"><span data-stu-id="3ac70-140">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> </dl>

 

 



