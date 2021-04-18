---
description: In diesem Tutorial wird gezeigt, wie Mediendateien mithilfe des Medien Sitzungs Objekts wiedergegeben werden.
ms.assetid: cdd67082-8153-4f48-abc5-278be82ae082
title: Wiedergeben von Mediendateien mit Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 163dba2f9f67139ce7477470889e13a54e2c8b5d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104558835"
---
# <a name="how-to-play-media-files-with-media-foundation"></a><span data-ttu-id="4091a-103">Wiedergeben von Mediendateien mit Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4091a-103">How to Play Media Files with Media Foundation</span></span>

<span data-ttu-id="4091a-104">In diesem Tutorial wird gezeigt, wie Mediendateien mithilfe des [Medien Sitzungs](media-session.md) Objekts wiedergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4091a-104">This tutorial shows how to play media files using the [Media Session](media-session.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="4091a-105">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="4091a-105">Prerequisites</span></span>

<span data-ttu-id="4091a-106">Bevor Sie dieses Thema lesen, sollten Sie sich mit den folgenden Media Foundation Konzepten vertraut machen:</span><span class="sxs-lookup"><span data-stu-id="4091a-106">Before reading this topic, you should be familiar with the following Media Foundation concepts:</span></span>

-   [<span data-ttu-id="4091a-107">Medien Sitzung</span><span class="sxs-lookup"><span data-stu-id="4091a-107">Media Session</span></span>](media-session.md)
-   [<span data-ttu-id="4091a-108">Quellresolver</span><span class="sxs-lookup"><span data-stu-id="4091a-108">Source Resolver</span></span>](source-resolver.md)
-   [<span data-ttu-id="4091a-109">Topologien</span><span class="sxs-lookup"><span data-stu-id="4091a-109">Topologies</span></span>](topologies.md)
-   [<span data-ttu-id="4091a-110">Medienereignis Generatoren</span><span class="sxs-lookup"><span data-stu-id="4091a-110">Media Event Generators</span></span>](media-event-generators.md)
-   [<span data-ttu-id="4091a-111">Präsentations Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="4091a-111">Presentation Descriptors</span></span>](presentation-descriptors.md)

> [!Note]  
> <span data-ttu-id="4091a-112">In diesem Thema wird nicht beschrieben, wie Dateien wiedergegeben werden, die durch Digital Rights Management (DRM) geschützt sind.</span><span class="sxs-lookup"><span data-stu-id="4091a-112">This topic does not describe how to play files that are protected by digital rights management (DRM).</span></span> <span data-ttu-id="4091a-113">Weitere Informationen zu DRM in Microsoft Media Foundation finden Sie unter Wiedergeben [geschützter Mediendateien](how-to-play-protected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="4091a-113">For information about DRM in Microsoft Media Foundation, see [How to Play Protected Media Files](how-to-play-protected-media-files.md).</span></span>

 

## <a name="overview"></a><span data-ttu-id="4091a-114">Übersicht</span><span class="sxs-lookup"><span data-stu-id="4091a-114">Overview</span></span>

<span data-ttu-id="4091a-115">Die folgenden Objekte werden verwendet, um eine Mediendatei mit der Medien Sitzung wiederzugeben:</span><span class="sxs-lookup"><span data-stu-id="4091a-115">The following objects are used to play a media file with the Media Session:</span></span>

-   <span data-ttu-id="4091a-116">Eine *Medienquelle* ist ein Objekt, das eine Mediendatei oder eine andere Quelle von Mediendaten analysiert.</span><span class="sxs-lookup"><span data-stu-id="4091a-116">A *media source* is an object that parses a media file or other source of media data.</span></span> <span data-ttu-id="4091a-117">Die Medienquelle erstellt *Streamobjekte* für jeden Audiostream oder Videostream in der Datei.</span><span class="sxs-lookup"><span data-stu-id="4091a-117">The media source creates *stream* objects for each audio or video stream in the file.</span></span> <span data-ttu-id="4091a-118">*Decoders* konvertieren codierte Mediendaten in unkomprimierte Videos und Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="4091a-118">*Decoders* convert encoded media data into uncompressed video and audio.</span></span>
-   <span data-ttu-id="4091a-119">Der *Quell Löser* erstellt eine Medienquelle aus einer URL.</span><span class="sxs-lookup"><span data-stu-id="4091a-119">The *Source Resolver* creates a media source from a URL.</span></span>
-   <span data-ttu-id="4091a-120">Der [Erweiterte Videorenderer](enhanced-video-renderer.md) (EVR) rendert Videos auf dem Bildschirm.</span><span class="sxs-lookup"><span data-stu-id="4091a-120">The [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR) renders video to the screen.</span></span>
-   <span data-ttu-id="4091a-121">Der [streamingaudiorenderer](streaming-audio-renderer.md) (SAR) rendert Audiodaten auf einem Redner oder einem anderen Audioausgabegerät.</span><span class="sxs-lookup"><span data-stu-id="4091a-121">The [Streaming Audio Renderer](streaming-audio-renderer.md) (SAR) renders audio to a speaker or other audio output device.</span></span>
-   <span data-ttu-id="4091a-122">Eine *Topologie* definiert den Datenfluss von der Medienquelle zum EVR und SAR.</span><span class="sxs-lookup"><span data-stu-id="4091a-122">A *topology* defines the flow of data from the media source to the EVR and SAR.</span></span>
-   <span data-ttu-id="4091a-123">Die *Medien Sitzung* steuert den Datenfluss und sendet Statusereignisse an die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="4091a-123">The *Media Session* controls the data flow and sends status events to the application.</span></span> <span data-ttu-id="4091a-124">Dieser Prozess wird anhand des folgenden Diagramms veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="4091a-124">The following diagram illustrates this process.</span></span>

![Darstellung der Wiedergabe mithilfe der Medien Sitzung](images/session-playback.gif)

<span data-ttu-id="4091a-126">Im folgenden finden Sie eine allgemeine Übersicht über die Schritte, die zum Wiedergeben einer Mediendatei mithilfe der Medien Sitzung erforderlich sind:</span><span class="sxs-lookup"><span data-stu-id="4091a-126">The following is a general outline of the steps needed to play a media file using the Media Session:</span></span>

1.  <span data-ttu-id="4091a-127">Ruft die [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) -Funktion auf, um die Media Foundation Plattform zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="4091a-127">Call the [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) function to initialize the Media Foundation platform.</span></span>
2.  <span data-ttu-id="4091a-128">Rufen Sie [**mfkreatemediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) auf, um eine neue Instanz der Medien Sitzung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4091a-128">Call [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) to create a new instance of the Media Session.</span></span>
3.  <span data-ttu-id="4091a-129">Verwenden Sie den quellresolver, um eine Medienquelle zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4091a-129">Use the source resolver to create a media source.</span></span> <span data-ttu-id="4091a-130">Weitere Informationen finden Sie unter [using the Source Resolver](using-the-source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="4091a-130">For more information, see [Using the Source Resolver](using-the-source-resolver.md).</span></span>
4.  <span data-ttu-id="4091a-131">Erstellen Sie eine Topologie, die die Medienquelle mit dem EVR und SAR verbindet.</span><span class="sxs-lookup"><span data-stu-id="4091a-131">Create a topology that connects the media source to the EVR and SAR.</span></span> <span data-ttu-id="4091a-132">In diesem Schritt erstellt die Anwendung eine *partielle* Topologie, in der die Decoders nicht enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="4091a-132">In this step, the application creates a *partial* topology that does not include the decoders.</span></span> <span data-ttu-id="4091a-133">Weitere Informationen finden Sie unter [Erstellen von Wiedergabe Topologien](creating-playback-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="4091a-133">For more information, see [Creating Playback Topologies](creating-playback-topologies.md).</span></span>
5.  <span data-ttu-id="4091a-134">Wenden Sie [**imfmediasession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) an, um die Topologie für die Medien Sitzung festzulegen.</span><span class="sxs-lookup"><span data-stu-id="4091a-134">Call [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) to set the topology on the Media Session.</span></span>
6.  <span data-ttu-id="4091a-135">Verwenden Sie die [**imfmediaeventgenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) -Schnittstelle, um Ereignisse aus der Medien Sitzung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4091a-135">Use the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface to get events from the Media Session.</span></span>
7.  <span data-ttu-id="4091a-136">[**Imfmediasession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) wird aufgerufen, um die Wiedergabe zu starten.</span><span class="sxs-lookup"><span data-stu-id="4091a-136">Call [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) to start playback.</span></span> <span data-ttu-id="4091a-137">Nachdem die Wiedergabe gestartet wurde, können Sie Sie anhalten, indem Sie [**imfmediasession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause)aufrufen, oder Sie durch Aufrufen von [**imfmediasession:: stoppen**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop)anhalten.</span><span class="sxs-lookup"><span data-stu-id="4091a-137">After playback starts, you can pause it by calling [**IMFMediaSession::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause), or stop it by calling [**IMFMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).</span></span>
8.  <span data-ttu-id="4091a-138">Wenn die Anwendung beendet wird, geben Sie Ressourcen frei:</span><span class="sxs-lookup"><span data-stu-id="4091a-138">When the application exits, release resources:</span></span>

    1.  <span data-ttu-id="4091a-139">[**Imfmediasession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) wird aufgerufen, um die Medien Sitzung zu schließen.</span><span class="sxs-lookup"><span data-stu-id="4091a-139">Call [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) to close the Media Session.</span></span> <span data-ttu-id="4091a-140">Diese Methode ist asynchron.</span><span class="sxs-lookup"><span data-stu-id="4091a-140">This method is asynchronous.</span></span> <span data-ttu-id="4091a-141">Wenn der Vorgang abgeschlossen ist, sendet die Medien Sitzung ein [mesessionclosed](mesessionclosed.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="4091a-141">When it completes, the Media Session sends an [MESessionClosed](mesessionclosed.md) event.</span></span> <span data-ttu-id="4091a-142">Anschließend ist es sicher, die verbleibenden Schritte auszuführen.</span><span class="sxs-lookup"><span data-stu-id="4091a-142">Then it is safe to perform the remaining steps.</span></span>
    2.  <span data-ttu-id="4091a-143">Wenden Sie [**imfmediasource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) an, um die Medienquelle zu schließen.</span><span class="sxs-lookup"><span data-stu-id="4091a-143">Call [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) to shut down the media source.</span></span>
    3.  <span data-ttu-id="4091a-144">Wenden Sie [**imfmediasession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown) an, um die Medien Sitzung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="4091a-144">Call [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown) to shut down the Media Session.</span></span>
    4.  <span data-ttu-id="4091a-145">Zum Herunterfahren der Media Foundation Plattform wird [**mfshutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="4091a-145">Call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) to shut down the Media Foundation platform.</span></span>

<span data-ttu-id="4091a-146">In den folgenden Abschnitten wird ein umfassendes Codebeispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="4091a-146">The following sections show a complete code example:</span></span>

-   [<span data-ttu-id="4091a-147">Schritt 1: Deklarieren der cplayer-Klasse</span><span class="sxs-lookup"><span data-stu-id="4091a-147">Step 1: Declare the CPlayer Class</span></span>](step-1--declare-the-cplayer-class.md)
-   [<span data-ttu-id="4091a-148">Schritt 2: Erstellen des cplayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="4091a-148">Step 2: Create the CPlayer Object</span></span>](step-2--create-the-cplayer-object.md)
-   [<span data-ttu-id="4091a-149">Schritt 3: Öffnen einer Mediendatei</span><span class="sxs-lookup"><span data-stu-id="4091a-149">Step 3: Open a Media File</span></span>](step-3--open-a-media-file.md)
-   [<span data-ttu-id="4091a-150">Schritt 4: Erstellen der Medien Sitzung</span><span class="sxs-lookup"><span data-stu-id="4091a-150">Step 4: Create the Media Session</span></span>](step-4--create-the-media-session.md)
-   [<span data-ttu-id="4091a-151">Schritt 5: Behandeln von Medien Sitzungs Ereignissen</span><span class="sxs-lookup"><span data-stu-id="4091a-151">Step 5: Handle Media Session Events</span></span>](step-5--handle-media-session-events.md)
-   [<span data-ttu-id="4091a-152">Schritt 6: Wiedergabe von Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="4091a-152">Step 6: Control Playback</span></span>](step-6--control-playback.md)
-   [<span data-ttu-id="4091a-153">Schritt 7: Herunterfahren der Medien Sitzung</span><span class="sxs-lookup"><span data-stu-id="4091a-153">Step 7: Shut Down the Media Session</span></span>](step-7--shut-down-the-media-session.md)
-   [<span data-ttu-id="4091a-154">Beispiel für Medien Sitzungs Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="4091a-154">Media Session Playback Example</span></span>](media-session-playback-example.md)

## <a name="related-topics"></a><span data-ttu-id="4091a-155">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4091a-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4091a-156">Medien Sitzung</span><span class="sxs-lookup"><span data-stu-id="4091a-156">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="4091a-157">Audio-/Videowiedergabe</span><span class="sxs-lookup"><span data-stu-id="4091a-157">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> </dl>

 

 



