---
description: In diesem Artikel wird beschrieben, wie Sie einen benutzerdefinierten Presenter für den erweiterten Videorenderer (EVR) schreiben.
ms.assetid: 1135b309-b158-4b70-9f76-5c93d0ad3250
title: Schreiben von EVR Presenter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94933d9eb53b0b03105edc7056ace4fe73238d16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104557063"
---
# <a name="how-to-write-an-evr-presenter"></a><span data-ttu-id="4ea41-103">Schreiben von EVR Presenter</span><span class="sxs-lookup"><span data-stu-id="4ea41-103">How to Write an EVR Presenter</span></span>

<span data-ttu-id="4ea41-104">In diesem Artikel wird beschrieben, wie Sie einen benutzerdefinierten Presenter für den erweiterten Videorenderer (EVR) schreiben.</span><span class="sxs-lookup"><span data-stu-id="4ea41-104">This article describes how to write a custom presenter for the enhanced video renderer (EVR).</span></span> <span data-ttu-id="4ea41-105">Ein benutzerdefinierter Presenter kann sowohl mit DirectShow als auch mit Media Foundation verwendet werden. die Schnittstellen und das Objektmodell sind für beide Technologien identisch, obwohl die genaue Reihenfolge der Vorgänge variieren kann.</span><span class="sxs-lookup"><span data-stu-id="4ea41-105">A custom presenter can be used with both DirectShow and Media Foundation; the interfaces and object model are the same for both technologies, although the exact sequence of operations might vary.</span></span>

<span data-ttu-id="4ea41-106">Der Beispielcode in diesem Thema wird aus dem [evrpresenter](evrpresenter-sample.md)-Beispiel, das im Windows SDK bereitgestellt wird, angepasst.</span><span class="sxs-lookup"><span data-stu-id="4ea41-106">The example code in this topic is adapted from the [EVRPresenter Sample](evrpresenter-sample.md), which is provided in the Windows SDK.</span></span>

<span data-ttu-id="4ea41-107">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="4ea41-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="4ea41-108">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="4ea41-108">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="4ea41-109">Presenter-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="4ea41-109">Presenter Object Model</span></span>](#presenter-object-model)
    -   [<span data-ttu-id="4ea41-110">Datenfluss innerhalb des EVR</span><span class="sxs-lookup"><span data-stu-id="4ea41-110">Data Flow Inside the EVR</span></span>](#data-flow-inside-the-evr)
    -   [<span data-ttu-id="4ea41-111">Presenter-Zustände</span><span class="sxs-lookup"><span data-stu-id="4ea41-111">Presenter States</span></span>](#presenter-states)
    -   [<span data-ttu-id="4ea41-112">Presenter-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="4ea41-112">Presenter Interfaces</span></span>](#presenter-interfaces)
    -   [<span data-ttu-id="4ea41-113">Implementieren von IMF videode viceid</span><span class="sxs-lookup"><span data-stu-id="4ea41-113">Implementing IMFVideoDeviceID</span></span>](#implementing-imfvideodeviceid)
    -   [<span data-ttu-id="4ea41-114">Implementieren von imftopologyservicelookupclient</span><span class="sxs-lookup"><span data-stu-id="4ea41-114">Implementing IMFTopologyServiceLookupClient</span></span>](#implementing-imftopologyservicelookupclient)
    -   [<span data-ttu-id="4ea41-115">Implementieren von IMF videopresenter</span><span class="sxs-lookup"><span data-stu-id="4ea41-115">Implementing IMFVideoPresenter</span></span>](#implementing-imfvideopresenter)
    -   [<span data-ttu-id="4ea41-116">Implementieren von IMF-staatink</span><span class="sxs-lookup"><span data-stu-id="4ea41-116">Implementing IMFClockStateSink</span></span>](#implementing-imfclockstatesink)
    -   [<span data-ttu-id="4ea41-117">Implementieren von imfratesupport</span><span class="sxs-lookup"><span data-stu-id="4ea41-117">Implementing IMFRateSupport</span></span>](#implementing-imfratesupport)
    -   [<span data-ttu-id="4ea41-118">Senden von Ereignissen an den EVR</span><span class="sxs-lookup"><span data-stu-id="4ea41-118">Sending Events to the EVR</span></span>](#sending-events-to-the-evr)
-   [<span data-ttu-id="4ea41-119">Aushandeln von Formaten</span><span class="sxs-lookup"><span data-stu-id="4ea41-119">Negotiating Formats</span></span>](#negotiating-formats)
-   [<span data-ttu-id="4ea41-120">Verwalten des Direct3D-Geräts</span><span class="sxs-lookup"><span data-stu-id="4ea41-120">Managing the Direct3D Device</span></span>](#managing-the-direct3d-device)
    -   [<span data-ttu-id="4ea41-121">Zuordnen von Direct3D-Flächen</span><span class="sxs-lookup"><span data-stu-id="4ea41-121">Allocating Direct3D Surfaces</span></span>](#allocating-direct3d-surfaces)
    -   [<span data-ttu-id="4ea41-122">Überwachungsbeispiele</span><span class="sxs-lookup"><span data-stu-id="4ea41-122">Tracking Samples</span></span>](#tracking-samples)
-   [<span data-ttu-id="4ea41-123">Ausgabe wird verarbeitet</span><span class="sxs-lookup"><span data-stu-id="4ea41-123">Processing Output</span></span>](#processing-output)
    -   [<span data-ttu-id="4ea41-124">Neuzeichnen von Frames</span><span class="sxs-lookup"><span data-stu-id="4ea41-124">Repainting Frames</span></span>](#repainting-frames)
    -   [<span data-ttu-id="4ea41-125">Beispiele für Zeitplanung</span><span class="sxs-lookup"><span data-stu-id="4ea41-125">Scheduling Samples</span></span>](#scheduling-samples)
    -   [<span data-ttu-id="4ea41-126">Präsentieren von Beispielen</span><span class="sxs-lookup"><span data-stu-id="4ea41-126">Presenting Samples</span></span>](#presenting-samples)
    -   [<span data-ttu-id="4ea41-127">Quell-und Ziel Rechtecke</span><span class="sxs-lookup"><span data-stu-id="4ea41-127">Source and Destination Rectangles</span></span>](#source-and-destination-rectangles)
    -   [<span data-ttu-id="4ea41-128">Ende des Streams</span><span class="sxs-lookup"><span data-stu-id="4ea41-128">End of Stream</span></span>](#end-of-stream)
-   [<span data-ttu-id="4ea41-129">Frame Schritt Schritt</span><span class="sxs-lookup"><span data-stu-id="4ea41-129">Frame Stepping</span></span>](#frame-stepping)
    -   [<span data-ttu-id="4ea41-130">Implementieren von Frame-Stepping</span><span class="sxs-lookup"><span data-stu-id="4ea41-130">Implementing Frame Stepping</span></span>](#implementing-frame-stepping)
-   [<span data-ttu-id="4ea41-131">Festlegen des Präsentators für den EVR</span><span class="sxs-lookup"><span data-stu-id="4ea41-131">Setting the Presenter on the EVR</span></span>](#setting-the-presenter-on-the-evr)
    -   [<span data-ttu-id="4ea41-132">Festlegen des Präsentators in DirectShow</span><span class="sxs-lookup"><span data-stu-id="4ea41-132">Setting the Presenter in DirectShow</span></span>](#setting-the-presenter-in-directshow)
    -   [<span data-ttu-id="4ea41-133">Festlegen des Präsentators in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4ea41-133">Setting the Presenter in Media Foundation</span></span>](#setting-the-presenter-in-media-foundation)
-   [<span data-ttu-id="4ea41-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4ea41-134">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="4ea41-135">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="4ea41-135">Prerequisites</span></span>

<span data-ttu-id="4ea41-136">Bevor Sie einen benutzerdefinierten Presenter schreiben, sollten Sie mit den folgenden Technologien vertraut sein:</span><span class="sxs-lookup"><span data-stu-id="4ea41-136">Before writing a custom presenter, you should be familiar with the following technologies:</span></span>

-   <span data-ttu-id="4ea41-137">Der erweiterte Videorenderer.</span><span class="sxs-lookup"><span data-stu-id="4ea41-137">The enhanced video renderer.</span></span> <span data-ttu-id="4ea41-138">Siehe [verbesserter Videorenderer](enhanced-video-renderer.md).</span><span class="sxs-lookup"><span data-stu-id="4ea41-138">See [Enhanced Video Renderer](enhanced-video-renderer.md).</span></span>
-   <span data-ttu-id="4ea41-139">Direct3D-Grafiken.</span><span class="sxs-lookup"><span data-stu-id="4ea41-139">Direct3D graphics.</span></span> <span data-ttu-id="4ea41-140">Sie müssen keine 3D-Grafiken verstehen, um einen Presenter zu schreiben, aber Sie müssen wissen, wie Sie ein Direct3D-Gerät erstellen und Direct3D-Oberflächen verwalten.</span><span class="sxs-lookup"><span data-stu-id="4ea41-140">You don't need to understand 3-D graphics to write a presenter, but you must know how to create a Direct3D device and manage Direct3D surfaces.</span></span> <span data-ttu-id="4ea41-141">Wenn Sie mit Direct3D nicht vertraut sind, lesen Sie die Abschnitte "Direct3D Devices" und "Direct3D Resources" in der Dokumentation zum DirectX Graphics SDK.</span><span class="sxs-lookup"><span data-stu-id="4ea41-141">If you aren't familiar with Direct3D, read the sections "Direct3D Devices" and "Direct3D Resources" in the DirectX Graphics SDK documentation.</span></span>
-   <span data-ttu-id="4ea41-142">DirectShow-Filter Diagramme oder die Media Foundation Pipeline, abhängig von der Technologie, die Ihre Anwendung zum Rendering von Videos verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ea41-142">DirectShow filter graphs or the Media Foundation pipeline, depending on which technology your application will use to render video.</span></span>
-   <span data-ttu-id="4ea41-143">[Media Foundation Transformationen](media-foundation-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="4ea41-143">[Media Foundation Transforms](media-foundation-transforms.md).</span></span> <span data-ttu-id="4ea41-144">Der EVR-Mixer ist eine Media Foundation Transformation, und der Presenter ruft Methoden direkt auf dem Mixer auf.</span><span class="sxs-lookup"><span data-stu-id="4ea41-144">The EVR mixer is a Media Foundation transform, and the presenter calls methods directly on the mixer.</span></span>
-   <span data-ttu-id="4ea41-145">Implementieren von COM-Objekten.</span><span class="sxs-lookup"><span data-stu-id="4ea41-145">Implementing COM objects.</span></span> <span data-ttu-id="4ea41-146">Der Presenter ist ein Prozess interner, frei Thread-com-Objekt.</span><span class="sxs-lookup"><span data-stu-id="4ea41-146">The presenter is an in-process, free-threaded COM object.</span></span>

## <a name="presenter-object-model"></a><span data-ttu-id="4ea41-147">Presenter-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="4ea41-147">Presenter Object Model</span></span>

<span data-ttu-id="4ea41-148">Dieser Abschnitt enthält eine Übersicht über das Presenter-Objektmodell und Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-148">This section contains an overview the presenter object model and interfaces.</span></span>

### <a name="data-flow-inside-the-evr"></a><span data-ttu-id="4ea41-149">Datenfluss innerhalb des EVR</span><span class="sxs-lookup"><span data-stu-id="4ea41-149">Data Flow Inside the EVR</span></span>

<span data-ttu-id="4ea41-150">Der EVR verwendet zwei Plug-in-Komponenten, um das Video zu Rendering: den *Mixer* und den *Presenter*.</span><span class="sxs-lookup"><span data-stu-id="4ea41-150">The EVR uses two plug-in components to render video: the *mixer* and the *presenter*.</span></span> <span data-ttu-id="4ea41-151">Der Mixer mischt die Videostreams und deinstalmengt das Video bei Bedarf.</span><span class="sxs-lookup"><span data-stu-id="4ea41-151">The mixer blends the video streams and deinterlaces the video if needed.</span></span> <span data-ttu-id="4ea41-152">Der Presenter zeichnet das Video auf der Anzeige und plant, wenn jeder Frame gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="4ea41-152">The presenter draws (or *presents*) the video onto the display and schedules when each frame is drawn.</span></span> <span data-ttu-id="4ea41-153">Anwendungen können eines dieser Objekte durch eine benutzerdefinierte Implementierung ersetzen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-153">Applications can replace either of these objects with a custom implementation.</span></span>

<span data-ttu-id="4ea41-154">Der EVR verfügt über einen oder mehrere Eingabedaten Ströme, und der Mixer verfügt über eine entsprechende Anzahl von Eingabedaten strömen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-154">The EVR has one or more input streams, and the mixer has a corresponding number of input streams.</span></span> <span data-ttu-id="4ea41-155">Stream 0 ist immer der *Verweis Datenstrom*.</span><span class="sxs-lookup"><span data-stu-id="4ea41-155">Stream 0 is always the *reference stream*.</span></span> <span data-ttu-id="4ea41-156">Die anderen Streams sind *Substreams*, die der mischungsstream in den Verweis Datenstrom einfügt.</span><span class="sxs-lookup"><span data-stu-id="4ea41-156">The other streams are *substreams*, which the mixer alpha-blends onto the reference stream.</span></span> <span data-ttu-id="4ea41-157">Der Verweis Datenstrom bestimmt die Master Frame-Rate für das zusammengesetzte Video.</span><span class="sxs-lookup"><span data-stu-id="4ea41-157">The reference stream determines the master frame-rate for the composited video.</span></span> <span data-ttu-id="4ea41-158">Der Mixer nimmt für jeden Verweis Rahmen den neuesten Frame aus jedem substream, mischt sie in den Verweis Rahmen und gibt einen einzelnen zusammengesetzten Frame aus.</span><span class="sxs-lookup"><span data-stu-id="4ea41-158">For each reference frame, the mixer takes the most recent frame from each substream, alpha-blends them onto the reference frame, and outputs a single composited frame.</span></span> <span data-ttu-id="4ea41-159">Der Mixer führt bei Bedarf auch Deinterlacing-und Farb Konvertierungen von YUV in RGB aus.</span><span class="sxs-lookup"><span data-stu-id="4ea41-159">The mixer also performs deinterlacing and color conversion from YUV to RGB if needed.</span></span> <span data-ttu-id="4ea41-160">Der EVR fügt den Mixer immer in die Video Pipeline ein, unabhängig von der Anzahl der Eingabedaten Ströme oder des Video Formats.</span><span class="sxs-lookup"><span data-stu-id="4ea41-160">The EVR always inserts the mixer into the video pipeline, regardless of the number of input streams or the video format.</span></span> <span data-ttu-id="4ea41-161">Dieses Verfahren wird in der folgenden Abbildung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="4ea41-161">The following image illustrates this process.</span></span>

![das Diagramm zeigt den Verweis Datenstrom und den unter Datenstrom, der auf den Mixer zeigt, der auf den Presenter zeigt, der auf die Anzeige zeigt.](images/459338c4-cff8-4d20-bffd-ff1cbbe6f332.gif)

<span data-ttu-id="4ea41-163">Der Presenter führt die folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="4ea41-163">The presenter performs the following tasks:</span></span>

-   <span data-ttu-id="4ea41-164">Legt das Ausgabeformat auf dem Mixer fest.</span><span class="sxs-lookup"><span data-stu-id="4ea41-164">Sets the output format on the mixer.</span></span> <span data-ttu-id="4ea41-165">Bevor das Streaming beginnt, legt der Presenter einen Medientyp für den Ausgabestream des Mischers fest.</span><span class="sxs-lookup"><span data-stu-id="4ea41-165">Before streaming begins, the presenter sets a media type on the mixer's output stream.</span></span> <span data-ttu-id="4ea41-166">Dieser Medientyp definiert das Format des zusammengesetzten Bilds.</span><span class="sxs-lookup"><span data-stu-id="4ea41-166">This media type defines the format of the composited image.</span></span>
-   <span data-ttu-id="4ea41-167">Erstellt das Direct3D-Gerät.</span><span class="sxs-lookup"><span data-stu-id="4ea41-167">Creates the Direct3D device.</span></span>
-   <span data-ttu-id="4ea41-168">Weist Direct3D-Oberflächen zu.</span><span class="sxs-lookup"><span data-stu-id="4ea41-168">Allocates Direct3D surfaces.</span></span> <span data-ttu-id="4ea41-169">Der Mixer bliert die zusammengesetzten Frames auf diese Oberflächen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-169">The mixer blits the composited frames onto these surfaces.</span></span>
-   <span data-ttu-id="4ea41-170">Ruft die Ausgabe des Mischers ab.</span><span class="sxs-lookup"><span data-stu-id="4ea41-170">Gets the output from the mixer.</span></span>
-   <span data-ttu-id="4ea41-171">Plant, wann die Frames angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="4ea41-171">Schedules when the frames are presented.</span></span> <span data-ttu-id="4ea41-172">Der EVR stellt die Präsentationszeit bereit, und der Presenter plant Frames entsprechend dieser Uhr.</span><span class="sxs-lookup"><span data-stu-id="4ea41-172">The EVR provides the presentation clock, and the presenter schedules frames according to this clock.</span></span>
-   <span data-ttu-id="4ea41-173">Stellt jeden Frame mithilfe von Direct3D dar.</span><span class="sxs-lookup"><span data-stu-id="4ea41-173">Presents each frame using Direct3D.</span></span>
-   <span data-ttu-id="4ea41-174">Führt Frame-und Scrubbing aus.</span><span class="sxs-lookup"><span data-stu-id="4ea41-174">Performs frame stepping and scrubbing.</span></span>

### <a name="presenter-states"></a><span data-ttu-id="4ea41-175">Presenter-Zustände</span><span class="sxs-lookup"><span data-stu-id="4ea41-175">Presenter States</span></span>

<span data-ttu-id="4ea41-176">Der Presenter befindet sich jederzeit in einem der folgenden Zustände:</span><span class="sxs-lookup"><span data-stu-id="4ea41-176">At any time, the presenter is in one of following states:</span></span>

-   <span data-ttu-id="4ea41-177">*Gestartet*.</span><span class="sxs-lookup"><span data-stu-id="4ea41-177">*Started*.</span></span> <span data-ttu-id="4ea41-178">Die Präsentations Uhr der EVR wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4ea41-178">The EVR's presentation clock is running.</span></span> <span data-ttu-id="4ea41-179">Der Presenter plant Video Frames für die Präsentation, sobald sie eintreffen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-179">The presenter schedules video frames for presentation as they arrive.</span></span>
-   <span data-ttu-id="4ea41-180">*Angeh* alten.</span><span class="sxs-lookup"><span data-stu-id="4ea41-180">*Paused*.</span></span> <span data-ttu-id="4ea41-181">Die Präsentations Uhr ist angehalten.</span><span class="sxs-lookup"><span data-stu-id="4ea41-181">The presentation clock is suspended.</span></span> <span data-ttu-id="4ea41-182">Der Presenter zeigt keine neuen Beispiele an, behält jedoch die Warteschlange geplanter Beispiele bei.</span><span class="sxs-lookup"><span data-stu-id="4ea41-182">The presenter does not present any new samples but maintains its queue of scheduled samples.</span></span> <span data-ttu-id="4ea41-183">Wenn neue Beispiele empfangen werden, fügt der Presenter Sie der Warteschlange hinzu.</span><span class="sxs-lookup"><span data-stu-id="4ea41-183">If new samples are received, the presenter adds them to the queue.</span></span>
-   <span data-ttu-id="4ea41-184">*Stopped*(Beendet): Dies ist der anfängliche Status des Kanals nach seiner Erstellung (es sei denn, im Portal wurde das automatische Starten gewählt).</span><span class="sxs-lookup"><span data-stu-id="4ea41-184">*Stopped*.</span></span> <span data-ttu-id="4ea41-185">Die Präsentations Uhr wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="4ea41-185">The presentation clock is stopped.</span></span> <span data-ttu-id="4ea41-186">Der Presenter verwirft alle geplanten Beispiele.</span><span class="sxs-lookup"><span data-stu-id="4ea41-186">The presenter discards any samples that were scheduled.</span></span>
-   <span data-ttu-id="4ea41-187">*Herunterfahren.*</span><span class="sxs-lookup"><span data-stu-id="4ea41-187">*Shut down*.</span></span> <span data-ttu-id="4ea41-188">Der Presenter gibt alle Ressourcen im Zusammenhang mit dem Streaming frei, z. b. Direct3D</span><span class="sxs-lookup"><span data-stu-id="4ea41-188">The presenter releases any resources related to streaming, such as Direct3D surfaces.</span></span> <span data-ttu-id="4ea41-189">Dies ist der Anfangszustand des Presenter und der endgültige Zustand, bevor der Presenter zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="4ea41-189">This is the presenter's initial state, and the final state before the presenter is destroyed.</span></span>

<span data-ttu-id="4ea41-190">Im Beispielcode in diesem Thema wird der Presenter-Zustand durch eine Enumeration dargestellt:</span><span class="sxs-lookup"><span data-stu-id="4ea41-190">In the example code in this topic, the presenter state is represented by an enumeration:</span></span>


```C++
enum RENDER_STATE
{
    RENDER_STATE_STARTED = 1,
    RENDER_STATE_STOPPED,
    RENDER_STATE_PAUSED,
    RENDER_STATE_SHUTDOWN,  // Initial state.
};
```



<span data-ttu-id="4ea41-191">Einige Vorgänge sind ungültig, während sich der Presenter im Zustand "Herunterfahren" befindet.</span><span class="sxs-lookup"><span data-stu-id="4ea41-191">Some operations are not valid while the presenter is in the shutdown state.</span></span> <span data-ttu-id="4ea41-192">Im Beispielcode wird dieser Zustand durch Aufrufen einer Hilfsmethode überprüft:</span><span class="sxs-lookup"><span data-stu-id="4ea41-192">The example code checks for this state by calling a helper method:</span></span>


```C++
    HRESULT CheckShutdown() const
    {
        if (m_RenderState == RENDER_STATE_SHUTDOWN)
        {
            return MF_E_SHUTDOWN;
        }
        else
        {
            return S_OK;
        }
    }
```



### <a name="presenter-interfaces"></a><span data-ttu-id="4ea41-193">Presenter-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="4ea41-193">Presenter Interfaces</span></span>

<span data-ttu-id="4ea41-194">Ein Präsentator ist erforderlich, um die folgenden Schnittstellen zu implementieren:</span><span class="sxs-lookup"><span data-stu-id="4ea41-194">A presenter is required to implement the following interfaces:</span></span>



| <span data-ttu-id="4ea41-195">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="4ea41-195">Interface</span></span>                                                                | <span data-ttu-id="4ea41-196">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4ea41-196">Description</span></span>                                                                                                                                                         |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4ea41-197">**IMF-staatink**</span><span class="sxs-lookup"><span data-stu-id="4ea41-197">**IMFClockStateSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)                           | <span data-ttu-id="4ea41-198">Benachrichtigt den Presenter, wenn die Uhr die Uhr den Zustand ändert.</span><span class="sxs-lookup"><span data-stu-id="4ea41-198">Notifies the presenter when the EVR's clock changes state.</span></span> <span data-ttu-id="4ea41-199">Siehe [Implementieren von IMF-staatink](#implementing-imfclockstatesink).</span><span class="sxs-lookup"><span data-stu-id="4ea41-199">See [Implementing IMFClockStateSink](#implementing-imfclockstatesink).</span></span>                                   |
| [<span data-ttu-id="4ea41-200">**IMF-Dienst**</span><span class="sxs-lookup"><span data-stu-id="4ea41-200">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                                   | <span data-ttu-id="4ea41-201">Bietet eine Möglichkeit für die Anwendung und andere Komponenten in der Pipeline, Schnittstellen vom Präsentator zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4ea41-201">Provides a way for the application and other components in the pipeline to get interfaces from the presenter.</span></span>                                                       |
| [<span data-ttu-id="4ea41-202">**Imftopologyservicelookupclient**</span><span class="sxs-lookup"><span data-stu-id="4ea41-202">**IMFTopologyServiceLookupClient**</span></span>](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) | <span data-ttu-id="4ea41-203">Ermöglicht dem Presenter, Schnittstellen vom EVR oder dem Mixer zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4ea41-203">Enables the presenter to get interfaces from the EVR or the mixer.</span></span> <span data-ttu-id="4ea41-204">Weitere Informationen finden Sie unter [Implementieren von imftopologyservicelookupclient](#implementing-imftopologyservicelookupclient).</span><span class="sxs-lookup"><span data-stu-id="4ea41-204">See [Implementing IMFTopologyServiceLookupClient](#implementing-imftopologyservicelookupclient).</span></span> |
| [<span data-ttu-id="4ea41-205">**IMF videoabviceid**</span><span class="sxs-lookup"><span data-stu-id="4ea41-205">**IMFVideoDeviceID**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)                             | <span data-ttu-id="4ea41-206">Stellt sicher, dass der Presenter und der Mixer kompatible Technologien verwenden.</span><span class="sxs-lookup"><span data-stu-id="4ea41-206">Ensures that the presenter and the mixer use compatible technologies.</span></span> <span data-ttu-id="4ea41-207">Weitere Informationen finden Sie unter [Implementieren von IMF videode viceid](#implementing-imfvideodeviceid).</span><span class="sxs-lookup"><span data-stu-id="4ea41-207">See [Implementing IMFVideoDeviceID](#implementing-imfvideodeviceid).</span></span>                          |
| [<span data-ttu-id="4ea41-208">**IMF videopresenter**</span><span class="sxs-lookup"><span data-stu-id="4ea41-208">**IMFVideoPresenter**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopresenter)                           | <span data-ttu-id="4ea41-209">Verarbeitet Nachrichten aus dem EVR.</span><span class="sxs-lookup"><span data-stu-id="4ea41-209">Processes messages from the EVR.</span></span> <span data-ttu-id="4ea41-210">Weitere Informationen finden Sie unter [Implementieren von IMF videopresenter](#implementing-imfvideopresenter).</span><span class="sxs-lookup"><span data-stu-id="4ea41-210">See [Implementing IMFVideoPresenter](#implementing-imfvideopresenter).</span></span>                                                             |



 

<span data-ttu-id="4ea41-211">Die folgenden Schnittstellen sind optional:</span><span class="sxs-lookup"><span data-stu-id="4ea41-211">The following interfaces are optional:</span></span>



| <span data-ttu-id="4ea41-212">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="4ea41-212">Interface</span></span>                                                | <span data-ttu-id="4ea41-213">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4ea41-213">Description</span></span>                                                                                                                                                               |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4ea41-214">**Ievrtreuhändvideoplugin**</span><span class="sxs-lookup"><span data-stu-id="4ea41-214">**IEVRTrustedVideoPlugin**</span></span>](/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin) | <span data-ttu-id="4ea41-215">Ermöglicht dem Presenter, mit geschützten Medien zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="4ea41-215">Enables the presenter to work with protected media.</span></span> <span data-ttu-id="4ea41-216">Implementieren Sie diese Schnittstelle, wenn es sich bei dem Presenter um eine vertrauenswürdige Komponente handelt, die im geschützten Medien Pfad (PMP) funktionieren soll.</span><span class="sxs-lookup"><span data-stu-id="4ea41-216">Implement this interface if your presenter is a trusted component designed to work in the protected media path (PMP).</span></span> |
| [<span data-ttu-id="4ea41-217">**Imfratesupport**</span><span class="sxs-lookup"><span data-stu-id="4ea41-217">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)                 | <span data-ttu-id="4ea41-218">Meldet den Bereich der Wiedergabe Raten, die der Presenter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4ea41-218">Reports the range of playback rates that the presenter supports.</span></span> <span data-ttu-id="4ea41-219">Siehe [Implementieren von imfratesupport](#implementing-imfratesupport).</span><span class="sxs-lookup"><span data-stu-id="4ea41-219">See [Implementing IMFRateSupport](#implementing-imfratesupport).</span></span>                                         |
| [<span data-ttu-id="4ea41-220">**IMF videopositionmapper**</span><span class="sxs-lookup"><span data-stu-id="4ea41-220">**IMFVideoPositionMapper**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper) | <span data-ttu-id="4ea41-221">Ordnet die Koordinaten im Video Frame der Ausgabe den Koordinaten des eingabevideoframes zu.</span><span class="sxs-lookup"><span data-stu-id="4ea41-221">Maps coordinates on the output video frame to coordinates on the input video frame.</span></span>                                                                                       |
| [<span data-ttu-id="4ea41-222">**Iqualprop**</span><span class="sxs-lookup"><span data-stu-id="4ea41-222">**IQualProp**</span></span>](/previous-versions/windows/desktop/api/amvideo/nn-amvideo-iqualprop)                         | <span data-ttu-id="4ea41-223">Meldet Leistungsinformationen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-223">Reports performance information.</span></span> <span data-ttu-id="4ea41-224">Der EVR verwendet diese Informationen für die Verwaltung der Qualitätskontrolle.</span><span class="sxs-lookup"><span data-stu-id="4ea41-224">The EVR uses this information for quality-control management.</span></span> <span data-ttu-id="4ea41-225">Diese Schnittstelle ist im DirectShow SDK dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="4ea41-225">This interface is documented in the DirectShow SDK.</span></span>                        |



 

<span data-ttu-id="4ea41-226">Sie können auch Schnittstellen für die Anwendung bereitstellen, um mit dem Presenter zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="4ea41-226">You can also provide interfaces for the application to communicate with the presenter.</span></span> <span data-ttu-id="4ea41-227">Der Standard Presenter implementiert zu diesem Zweck die [**IMF videodisplaycontrol**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="4ea41-227">The standard presenter implements the [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface for this purpose.</span></span> <span data-ttu-id="4ea41-228">Sie können diese Schnittstelle implementieren oder eigene definieren.</span><span class="sxs-lookup"><span data-stu-id="4ea41-228">You can implement this interface or define your own.</span></span> <span data-ttu-id="4ea41-229">Die Anwendung erhält Schnittstellen vom Präsentator, indem [**imfgetservice:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) auf dem EVR aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="4ea41-229">The application obtains interfaces from the presenter by calling [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the EVR.</span></span> <span data-ttu-id="4ea41-230">Wenn die Dienst-GUID **MR_VIDEO_RENDER_SERVICE** ist, übergibt der EVR die **GetService** -Anforderung an den Presenter.</span><span class="sxs-lookup"><span data-stu-id="4ea41-230">When the service GUID is **MR_VIDEO_RENDER_SERVICE**, the EVR passes the **GetService** request to the presenter.</span></span>

### <a name="implementing-imfvideodeviceid"></a><span data-ttu-id="4ea41-231">Implementieren von IMF videode viceid</span><span class="sxs-lookup"><span data-stu-id="4ea41-231">Implementing IMFVideoDeviceID</span></span>

<span data-ttu-id="4ea41-232">Die [**IMF videodeviceid**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) -Schnittstelle enthält eine Methode, [**getdeviceid**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid), die eine Geräte-GUID zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="4ea41-232">The [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) interface contains one method, [**GetDeviceID**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid), which returns a device GUID.</span></span> <span data-ttu-id="4ea41-233">Die Geräte-GUID stellt sicher, dass der Presenter und der Mixer kompatible Technologien verwenden.</span><span class="sxs-lookup"><span data-stu-id="4ea41-233">The device GUID ensures that the presenter and the mixer use compatible technologies.</span></span> <span data-ttu-id="4ea41-234">Wenn die Geräte-GUIDs nicht stimmen, kann der EVR nicht initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="4ea41-234">If the device GUIDs do not match, the EVR fails to initialize.</span></span>

<span data-ttu-id="4ea41-235">Sowohl der Standard-Mixer als auch der Presenter verwenden Direct3D 9, wobei die Geräte-GUID gleich **IID_IDirect3DDevice9** ist.</span><span class="sxs-lookup"><span data-stu-id="4ea41-235">The standard mixer and presenter both use Direct3D 9, with the device GUID equal to **IID_IDirect3DDevice9**.</span></span> <span data-ttu-id="4ea41-236">Wenn Sie Ihren benutzerdefinierten Presenter mit dem Standard-Mixer verwenden möchten, muss die Geräte-GUID des Präsentators **IID_IDirect3DDevice9** werden.</span><span class="sxs-lookup"><span data-stu-id="4ea41-236">If you intend to use your custom presenter with the standard mixer, the presenter's device GUID must be **IID_IDirect3DDevice9**.</span></span> <span data-ttu-id="4ea41-237">Wenn Sie beide Komponenten ersetzen, können Sie eine neue Geräte-GUID definieren.</span><span class="sxs-lookup"><span data-stu-id="4ea41-237">If you replace both components, you could define a new device GUID.</span></span> <span data-ttu-id="4ea41-238">Im restlichen Teil dieses Artikels wird davon ausgegangen, dass der Presenter Direct3D 9 verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ea41-238">For the remainder of this article, it is assumed that the presenter uses Direct3D 9.</span></span> <span data-ttu-id="4ea41-239">Hier ist die Standard Implementierung von [**getdeviceid**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid):</span><span class="sxs-lookup"><span data-stu-id="4ea41-239">Here is the standard implementation of [**GetDeviceID**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid):</span></span>


```C++
HRESULT EVRCustomPresenter::GetDeviceID(IID* pDeviceID)
{
    if (pDeviceID == NULL)
    {
        return E_POINTER;
    }

    *pDeviceID = __uuidof(IDirect3DDevice9);
    return S_OK;
}
```



<span data-ttu-id="4ea41-240">Die Methode sollte auch dann erfolgreich sein, wenn der Presenter heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="4ea41-240">The method should succeed even when the presenter is shut down.</span></span>

### <a name="implementing-imftopologyservicelookupclient"></a><span data-ttu-id="4ea41-241">Implementieren von imftopologyservicelookupclient</span><span class="sxs-lookup"><span data-stu-id="4ea41-241">Implementing IMFTopologyServiceLookupClient</span></span>

<span data-ttu-id="4ea41-242">Die [**imftopologyservicelookupclient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) -Schnittstelle ermöglicht dem Presenter das erhalten von Schnittstellen Zeigern aus dem EVR und vom Mixer wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4ea41-242">The [**IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) interface enables the presenter to get interface pointers from the EVR and from the mixer as follows:</span></span>

1.  <span data-ttu-id="4ea41-243">Wenn der EVR den Presenter initialisiert, ruft er die [**imftopologyservicelookupclient:: initservicepointer**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) -Methode des Presenter auf.</span><span class="sxs-lookup"><span data-stu-id="4ea41-243">When the EVR initializes the presenter, it calls the presenter's [**IMFTopologyServiceLookupClient::InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) method.</span></span> <span data-ttu-id="4ea41-244">Das-Argument ist ein Zeiger auf die [**IMFTopologyServiceLookup**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookup) -Schnittstelle von EVR.</span><span class="sxs-lookup"><span data-stu-id="4ea41-244">The argument is a pointer to the EVR's [**IMFTopologyServiceLookup**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookup) interface.</span></span>
2.  <span data-ttu-id="4ea41-245">Der Presenter ruft [**IMFTopologyServiceLookup:: LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) auf, um Schnittstellen Zeiger aus dem EVR oder dem Mixer zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4ea41-245">The presenter calls [**IMFTopologyServiceLookup::LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) to get interface pointers from either the EVR or the mixer.</span></span>

<span data-ttu-id="4ea41-246">Die [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) -Methode ähnelt der [**imfgetservice:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) -Methode.</span><span class="sxs-lookup"><span data-stu-id="4ea41-246">The [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) method is similar to the [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) method.</span></span> <span data-ttu-id="4ea41-247">Beide Methoden übernehmen eine Dienst-GUID und eine Schnittstellen-ID (IID) als Eingabe, aber **LookupService** gibt ein Array von Schnittstellen Zeigern zurück, während **GetService** einen einzelnen Zeiger zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="4ea41-247">Both methods take a service GUID and an interface identifier (IID) as input, but **LookupService** returns an array of interface pointers, while **GetService** returns a single pointer.</span></span> <span data-ttu-id="4ea41-248">In der Praxis können Sie jedoch die Array Größe immer auf 1 festlegen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-248">In practice, however, you can always set the array size to 1.</span></span> <span data-ttu-id="4ea41-249">Das Objekt, das abgefragt wird, hängt von der Dienst-GUID ab:</span><span class="sxs-lookup"><span data-stu-id="4ea41-249">The object queried depends on the service GUID:</span></span>

-   <span data-ttu-id="4ea41-250">Wenn die Dienst-GUID **MR_VIDEO_RENDER_SERVICE** ist, wird der EVR abgefragt.</span><span class="sxs-lookup"><span data-stu-id="4ea41-250">If the service GUID is **MR_VIDEO_RENDER_SERVICE**, the EVR is queried.</span></span>
-   <span data-ttu-id="4ea41-251">Wenn die Dienst-GUID **MR_VIDEO_MIXER_SERVICE** ist, wird der Mixer abgefragt.</span><span class="sxs-lookup"><span data-stu-id="4ea41-251">If the service GUID is **MR_VIDEO_MIXER_SERVICE**, the mixer is queried.</span></span>

<span data-ttu-id="4ea41-252">Holen Sie in der Implementierung von [**initservicepointer**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers)die folgenden Schnittstellen aus dem EVR:</span><span class="sxs-lookup"><span data-stu-id="4ea41-252">In your implementation of [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers), get the following interfaces from the EVR:</span></span>



| <span data-ttu-id="4ea41-253">EVR-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="4ea41-253">EVR Interface</span></span>                                | <span data-ttu-id="4ea41-254">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4ea41-254">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4ea41-255">**Imediaeventsink**</span><span class="sxs-lookup"><span data-stu-id="4ea41-255">**IMediaEventSink**</span></span>](/windows/win32/api/strmif/nn-strmif-imediaeventsink) | <span data-ttu-id="4ea41-256">Bietet eine Möglichkeit für den Presenter, Nachrichten an den EVR zu senden.</span><span class="sxs-lookup"><span data-stu-id="4ea41-256">Provides a way for the presenter to send messages to the EVR.</span></span> <span data-ttu-id="4ea41-257">Diese Schnittstelle wird im DirectShow SDK definiert, sodass die Nachrichten dem Muster für DirectShow-Ereignisse, nicht Media Foundation Ereignissen folgen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-257">This interface is defined in the DirectShow SDK, so the messages follow the pattern for DirectShow events, not Media Foundation events.</span></span><br/>                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="4ea41-258">**IMF**</span><span class="sxs-lookup"><span data-stu-id="4ea41-258">**IMFClock**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfclock)                 | <span data-ttu-id="4ea41-259">Stellt die Uhr der EVR dar.</span><span class="sxs-lookup"><span data-stu-id="4ea41-259">Represents the EVR's clock.</span></span> <span data-ttu-id="4ea41-260">Der Presenter verwendet diese Schnittstelle, um Beispiele für die Präsentation zu planen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-260">The presenter uses this interface to schedule samples for presentation.</span></span> <span data-ttu-id="4ea41-261">Der EVR kann ohne eine Uhr ausgeführt werden, sodass diese Schnittstelle möglicherweise nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="4ea41-261">The EVR can run without a clock, so this interface might not be available.</span></span> <span data-ttu-id="4ea41-262">Wenn dies nicht der Wert ist, ignorieren Sie den Fehlercode von [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice).</span><span class="sxs-lookup"><span data-stu-id="4ea41-262">If not, ignore the error code from [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice).</span></span><br/> <span data-ttu-id="4ea41-263">Die Uhr implementiert auch die [**IMF Timer**](/windows/desktop/api/mfidl/nn-mfidl-imftimer) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="4ea41-263">The clock also implements the [**IMFTimer**](/windows/desktop/api/mfidl/nn-mfidl-imftimer) interface.</span></span> <span data-ttu-id="4ea41-264">In der Media Foundation Pipeline implementiert die Uhr die [**IMF presentationclock**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="4ea41-264">In the Media Foundation pipeline, the clock implements the [**IMFPresentationClock**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) interface.</span></span> <span data-ttu-id="4ea41-265">Diese Schnittstelle wird in DirectShow nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="4ea41-265">It does not implement this interface in DirectShow.</span></span><br/> |



 

<span data-ttu-id="4ea41-266">Holen Sie sich die folgenden Schnittstellen vom Mixer:</span><span class="sxs-lookup"><span data-stu-id="4ea41-266">Get the following interfaces from the mixer:</span></span>



| <span data-ttu-id="4ea41-267">Mixer-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="4ea41-267">Mixer Interface</span></span>                              | <span data-ttu-id="4ea41-268">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4ea41-268">Description</span></span>                                                |
|----------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="4ea41-269">**IMF-Transformation**</span><span class="sxs-lookup"><span data-stu-id="4ea41-269">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)         | <span data-ttu-id="4ea41-270">Ermöglicht es dem Presenter, mit dem Mixer zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="4ea41-270">Enables the presenter to communicate with the mixer.</span></span>       |
| [<span data-ttu-id="4ea41-271">**IMF videoabviceid**</span><span class="sxs-lookup"><span data-stu-id="4ea41-271">**IMFVideoDeviceID**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) | <span data-ttu-id="4ea41-272">Ermöglicht es dem Presenter, die Geräte-GUID des Mischers zu validieren.</span><span class="sxs-lookup"><span data-stu-id="4ea41-272">Enables the presenter to validate the mixer's device GUID.</span></span> |



 

<span data-ttu-id="4ea41-273">Der folgende Code implementiert die [**initservicepointer**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) -Methode:</span><span class="sxs-lookup"><span data-stu-id="4ea41-273">The following code implements the [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) method :</span></span>


```C++
HRESULT EVRCustomPresenter::InitServicePointers(
    IMFTopologyServiceLookup *pLookup
    )
{
    if (pLookup == NULL)
    {
        return E_POINTER;
    }

    HRESULT             hr = S_OK;
    DWORD               dwObjectCount = 0;

    EnterCriticalSection(&m_ObjectLock);

    // Do not allow initializing when playing or paused.
    if (IsActive())
    {
        hr = MF_E_INVALIDREQUEST;
        goto done;
    }

    SafeRelease(&m_pClock);
    SafeRelease(&m_pMixer);
    SafeRelease(&m_pMediaEventSink);

    // Ask for the clock. Optional, because the EVR might not have a clock.
    dwObjectCount = 1;

    (void)pLookup->LookupService(
        MF_SERVICE_LOOKUP_GLOBAL,   // Not used.
        0,                          // Reserved.
        MR_VIDEO_RENDER_SERVICE,    // Service to look up.
        IID_PPV_ARGS(&m_pClock),    // Interface to retrieve.
        &dwObjectCount              // Number of elements retrieved.
        );

    // Ask for the mixer. (Required.)
    dwObjectCount = 1;

    hr = pLookup->LookupService(
        MF_SERVICE_LOOKUP_GLOBAL, 0,
        MR_VIDEO_MIXER_SERVICE, IID_PPV_ARGS(&m_pMixer), &dwObjectCount
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Make sure that we can work with this mixer.
    hr = ConfigureMixer(m_pMixer);
    if (FAILED(hr))
    {
        goto done;
    }

    // Ask for the EVR's event-sink interface. (Required.)
    dwObjectCount = 1;

    hr = pLookup->LookupService(
        MF_SERVICE_LOOKUP_GLOBAL, 0,
        MR_VIDEO_RENDER_SERVICE, IID_PPV_ARGS(&m_pMediaEventSink),
        &dwObjectCount
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Successfully initialized. Set the state to "stopped."
    m_RenderState = RENDER_STATE_STOPPED;

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



<span data-ttu-id="4ea41-274">Wenn die von [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) erhaltenen Schnittstellen Zeiger nicht mehr gültig sind, ruft der EVR [**imftopologyservicelookupclient:: releaseservicezeigern**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers)auf.</span><span class="sxs-lookup"><span data-stu-id="4ea41-274">When the interface pointers obtained from [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) are no longer valid, the EVR calls [**IMFTopologyServiceLookupClient::ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers).</span></span> <span data-ttu-id="4ea41-275">Geben Sie in dieser Methode alle Schnittstellen Zeiger frei, und legen Sie den präsentatorzustand auf Herunterfahren fest:</span><span class="sxs-lookup"><span data-stu-id="4ea41-275">Inside this method, release all interface pointers and set the presenter state to shut down:</span></span>


```C++
HRESULT EVRCustomPresenter::ReleaseServicePointers()
{
    // Enter the shut-down state.
    EnterCriticalSection(&m_ObjectLock);

    m_RenderState = RENDER_STATE_SHUTDOWN;

    LeaveCriticalSection(&m_ObjectLock);

    // Flush any samples that were scheduled.
    Flush();

    // Clear the media type and release related resources.
    SetMediaType(NULL);

    // Release all services that were acquired from InitServicePointers.
    SafeRelease(&m_pClock);
    SafeRelease(&m_pMixer);
    SafeRelease(&m_pMediaEventSink);

    return S_OK;
}
```



<span data-ttu-id="4ea41-276">Der EVR ruft [**releaseservicepointer**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) aus verschiedenen Gründen auf, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="4ea41-276">The EVR calls [**ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) for various reasons, including:</span></span>

-   <span data-ttu-id="4ea41-277">Trennen oder erneutes Verbinden von Pins (DirectShow) oder hinzufügen oder Entfernen von streamsenken (Media Foundation).</span><span class="sxs-lookup"><span data-stu-id="4ea41-277">Disconnecting or reconnecting pins (DirectShow), or adding or removing stream sinks (Media Foundation).</span></span>
-   <span data-ttu-id="4ea41-278">Das Format wird geändert.</span><span class="sxs-lookup"><span data-stu-id="4ea41-278">Changing format.</span></span>
-   <span data-ttu-id="4ea41-279">Festlegen einer neuen Uhr.</span><span class="sxs-lookup"><span data-stu-id="4ea41-279">Setting a new clock.</span></span>
-   <span data-ttu-id="4ea41-280">Das abschließende Herunterfahren des EVR.</span><span class="sxs-lookup"><span data-stu-id="4ea41-280">Final shutdown of the EVR.</span></span>

<span data-ttu-id="4ea41-281">Während der Lebensdauer des Presenter kann der EVR mehrmals [**initservicepointer**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) und [**releaseservicepointer**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-281">During the lifetime of the presenter, the EVR might call [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) and [**ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) several times.</span></span>

### <a name="implementing-imfvideopresenter"></a><span data-ttu-id="4ea41-282">Implementieren von IMF videopresenter</span><span class="sxs-lookup"><span data-stu-id="4ea41-282">Implementing IMFVideoPresenter</span></span>

<span data-ttu-id="4ea41-283">Die [**IMF videopresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) -Schnittstelle erbt " [**IMF clockstaatink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) " und fügt zwei Methoden hinzu:</span><span class="sxs-lookup"><span data-stu-id="4ea41-283">The [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) interface inherits [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) and adds two methods:</span></span>



| <span data-ttu-id="4ea41-284">Methode</span><span class="sxs-lookup"><span data-stu-id="4ea41-284">Method</span></span>                                                               | <span data-ttu-id="4ea41-285">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4ea41-285">Description</span></span>                                            |
|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="4ea41-286">**Getcurrentmediatype**</span><span class="sxs-lookup"><span data-stu-id="4ea41-286">**GetCurrentMediaType**</span></span>](/windows/desktop/api/evr/nf-evr-imfvideopresenter-getcurrentmediatype) | <span data-ttu-id="4ea41-287">Gibt den Medientyp der zusammengesetzten Videorahmen zurück.</span><span class="sxs-lookup"><span data-stu-id="4ea41-287">Returns the media type of the composited video frames.</span></span> |
| [<span data-ttu-id="4ea41-288">**ProcessMessage**</span><span class="sxs-lookup"><span data-stu-id="4ea41-288">**ProcessMessage**</span></span>](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage)           | <span data-ttu-id="4ea41-289">Signalisiert dem Presenter, verschiedene Aktionen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-289">Signals the presenter to perform various actions.</span></span>      |



 

<span data-ttu-id="4ea41-290">Die [**getcurrentmediatype**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-getcurrentmediatype) -Methode gibt den Medientyp des Präsentators zurück.</span><span class="sxs-lookup"><span data-stu-id="4ea41-290">The [**GetCurrentMediaType**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-getcurrentmediatype) method returns the presenter's media type.</span></span> <span data-ttu-id="4ea41-291">(Ausführliche Informationen zum Festlegen des Medientyps finden Sie unter [Aushandeln von Formaten](#negotiating-formats).) Der Medientyp wird als [**IMF videomediatype**](/windows/desktop/api/mfobjects/nn-mfobjects-imfvideomediatype) -Schnittstellen Zeiger zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4ea41-291">(For details about setting the media type, see [Negotiating Formats](#negotiating-formats).) The media type is returned as an [**IMFVideoMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfvideomediatype) interface pointer.</span></span> <span data-ttu-id="4ea41-292">Im folgenden Beispiel wird davon ausgegangen, dass der Presenter den Medientyp als [**IMF MediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) -Zeiger speichert.</span><span class="sxs-lookup"><span data-stu-id="4ea41-292">The following example assumes that the presenter stores the media type as an [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) pointer.</span></span> <span data-ttu-id="4ea41-293">Um die **imfvideomediatype** -Schnittstelle aus dem Medientyp abzurufen, nennen Sie **QueryInterface**:</span><span class="sxs-lookup"><span data-stu-id="4ea41-293">To get the **IMFVideoMediaType** interface from the media type, call **QueryInterface**:</span></span>


```C++
HRESULT EVRCustomPresenter::GetCurrentMediaType(
    IMFVideoMediaType** ppMediaType
    )
{
    HRESULT hr = S_OK;

    if (ppMediaType == NULL)
    {
        return E_POINTER;
    }

    *ppMediaType = NULL;

    EnterCriticalSection(&m_ObjectLock);

    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    if (m_pMediaType == NULL)
    {
        hr = MF_E_NOT_INITIALIZED;
        goto done;
    }

    hr = m_pMediaType->QueryInterface(IID_PPV_ARGS(ppMediaType));

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



<span data-ttu-id="4ea41-294">Die [**ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) -Methode ist der primäre Mechanismus für die Kommunikation zwischen EVR und Presenter.</span><span class="sxs-lookup"><span data-stu-id="4ea41-294">The [**ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) method is the primary mechanism for the EVR to communicate with the presenter.</span></span> <span data-ttu-id="4ea41-295">Die folgenden Meldungen sind definiert.</span><span class="sxs-lookup"><span data-stu-id="4ea41-295">The following messages are defined.</span></span> <span data-ttu-id="4ea41-296">Weitere Informationen zum Implementieren der einzelnen Nachrichten finden Sie im weiteren Verlauf dieses Themas.</span><span class="sxs-lookup"><span data-stu-id="4ea41-296">The details of implementing each message are given in the remainder of this topic.</span></span>



| <span data-ttu-id="4ea41-297">`Message`</span><span class="sxs-lookup"><span data-stu-id="4ea41-297">Message</span></span>                                | <span data-ttu-id="4ea41-298">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4ea41-298">Description</span></span>                                                                                                                                                                                                                                        |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ea41-299">**MFVP_MESSAGE_INVALIDATEMEDIATYPE**</span><span class="sxs-lookup"><span data-stu-id="4ea41-299">**MFVP_MESSAGE_INVALIDATEMEDIATYPE**</span></span> | <span data-ttu-id="4ea41-300">Der Ausgabe Medientyp des Mischers ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="4ea41-300">The mixer's output media type is invalid.</span></span> <span data-ttu-id="4ea41-301">Der Presenter sollte mit dem Mixer einen neuen Medientyp aushandeln.</span><span class="sxs-lookup"><span data-stu-id="4ea41-301">The presenter should negotiate a new media type with the mixer.</span></span> <span data-ttu-id="4ea41-302">Siehe [Aushandeln von Formaten](#negotiating-formats).</span><span class="sxs-lookup"><span data-stu-id="4ea41-302">See [Negotiating Formats](#negotiating-formats).</span></span>                                                                                         |
| <span data-ttu-id="4ea41-303">**MFVP_MESSAGE_BEGINSTREAMING**</span><span class="sxs-lookup"><span data-stu-id="4ea41-303">**MFVP_MESSAGE_BEGINSTREAMING**</span></span>      | <span data-ttu-id="4ea41-304">Streaming wurde gestartet.</span><span class="sxs-lookup"><span data-stu-id="4ea41-304">Streaming has started.</span></span> <span data-ttu-id="4ea41-305">Eine bestimmte Aktion ist für diese Nachricht nicht erforderlich, Sie können Sie jedoch verwenden, um Ressourcen zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-305">No particular action is required by this message, but you can use it to allocate resources.</span></span>                                                                                                                                 |
| <span data-ttu-id="4ea41-306">**MFVP_MESSAGE_ENDSTREAMING**</span><span class="sxs-lookup"><span data-stu-id="4ea41-306">**MFVP_MESSAGE_ENDSTREAMING**</span></span>        | <span data-ttu-id="4ea41-307">Streaming wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="4ea41-307">Streaming has ended.</span></span> <span data-ttu-id="4ea41-308">Geben Sie alle Ressourcen frei, die Sie als Antwort auf die **MFVP_MESSAGE_BEGINSTREAMING** Nachricht zugeordnet haben.</span><span class="sxs-lookup"><span data-stu-id="4ea41-308">Release any resources that you allocated in response to the **MFVP_MESSAGE_BEGINSTREAMING** message.</span></span>                                                                                                                        |
| <span data-ttu-id="4ea41-309">**MFVP_MESSAGE_PROCESSINPUTNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="4ea41-309">**MFVP_MESSAGE_PROCESSINPUTNOTIFY**</span></span>  | <span data-ttu-id="4ea41-310">Der Mixer hat eine neue Eingabe Stichprobe erhalten und kann ggf. einen neuen Ausgabe Rahmen generieren.</span><span class="sxs-lookup"><span data-stu-id="4ea41-310">The mixer has received a new input sample and might be able to generate a new output frame.</span></span> <span data-ttu-id="4ea41-311">Der Presenter sollte [**imftransform::P rocess Output**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) auf dem Mixer aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-311">The presenter should call [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) on the mixer.</span></span> <span data-ttu-id="4ea41-312">Siehe [Verarbeitung der Ausgabe](#processing-output).</span><span class="sxs-lookup"><span data-stu-id="4ea41-312">See [Processing Output](#processing-output).</span></span> |
| <span data-ttu-id="4ea41-313">**MFVP_MESSAGE_ENDOFSTREAM**</span><span class="sxs-lookup"><span data-stu-id="4ea41-313">**MFVP_MESSAGE_ENDOFSTREAM**</span></span>         | <span data-ttu-id="4ea41-314">Die Präsentation wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="4ea41-314">The presentation has ended.</span></span> <span data-ttu-id="4ea41-315">Siehe [Ende des Datenstroms](#end-of-stream).</span><span class="sxs-lookup"><span data-stu-id="4ea41-315">See [End of Stream](#end-of-stream).</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="4ea41-316">**MFVP_MESSAGE_FLUSH**</span><span class="sxs-lookup"><span data-stu-id="4ea41-316">**MFVP_MESSAGE_FLUSH**</span></span>               | <span data-ttu-id="4ea41-317">Der EVR Leerung die Daten in seiner Renderingpipeline.</span><span class="sxs-lookup"><span data-stu-id="4ea41-317">The EVR is flushing the data in its rendering pipeline.</span></span> <span data-ttu-id="4ea41-318">Der Presenter sollte alle Video Frames verwerfen, die für die Präsentation geplant sind.</span><span class="sxs-lookup"><span data-stu-id="4ea41-318">The presenter should discard any video frames that are scheduled for presentation.</span></span>                                                                                                         |
| <span data-ttu-id="4ea41-319">**MFVP_MESSAGE_STEP**</span><span class="sxs-lookup"><span data-stu-id="4ea41-319">**MFVP_MESSAGE_STEP**</span></span>                | <span data-ttu-id="4ea41-320">Fordert den Presenter auf, einen Schritt vorwärts für N-Frames durchzusetzen</span><span class="sxs-lookup"><span data-stu-id="4ea41-320">Requests the presenter to step forward N frames.</span></span> <span data-ttu-id="4ea41-321">Der Presenter sollte die nächsten N-1-Frames verwerfen und den Nth-Frame anzeigen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-321">The presenter should discard the next N-1 frames and display the Nth frame.</span></span> <span data-ttu-id="4ea41-322">Siehe [Frame-Stepping](#frame-stepping).</span><span class="sxs-lookup"><span data-stu-id="4ea41-322">See [Frame Stepping](#frame-stepping).</span></span>                                                                                |
| <span data-ttu-id="4ea41-323">**MFVP_MESSAGE_CANCELSTEP**</span><span class="sxs-lookup"><span data-stu-id="4ea41-323">**MFVP_MESSAGE_CANCELSTEP**</span></span>          | <span data-ttu-id="4ea41-324">Bricht die Frame-Schritt Verarbeitung ab.</span><span class="sxs-lookup"><span data-stu-id="4ea41-324">Cancels frame stepping.</span></span>                                                                                                                                                                                                                            |



 

### <a name="implementing-imfclockstatesink"></a><span data-ttu-id="4ea41-325">Implementieren von IMF-staatink</span><span class="sxs-lookup"><span data-stu-id="4ea41-325">Implementing IMFClockStateSink</span></span>

<span data-ttu-id="4ea41-326">Der Presenter muss die [**imatclockstaatink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) -Schnittstelle als Teil der Implementierung von [**IMF videopresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter)implementieren, die **IMF-staatink** erbt.</span><span class="sxs-lookup"><span data-stu-id="4ea41-326">The presenter must implement the [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) interface as part of its implementation of [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter), which inherits **IMFClockStateSink**.</span></span> <span data-ttu-id="4ea41-327">Der EVR verwendet diese Schnittstelle, um den Presenter zu benachrichtigen, wenn sich der Zustand der EVR-Uhr ändert.</span><span class="sxs-lookup"><span data-stu-id="4ea41-327">The EVR uses this interface to notify the presenter whenever the EVR's clock changes state.</span></span> <span data-ttu-id="4ea41-328">Weitere Informationen zu den uhrzuständen finden Sie unter [Präsentations Uhr](presentation-clock.md).</span><span class="sxs-lookup"><span data-stu-id="4ea41-328">For more information about the clock states, see [Presentation Clock](presentation-clock.md).</span></span>

<span data-ttu-id="4ea41-329">Im folgenden finden Sie einige Richtlinien für die Implementierung der Methoden in dieser Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="4ea41-329">Here are some guidelines for implementing the methods in this interface.</span></span> <span data-ttu-id="4ea41-330">Alle Methoden sollten fehlschlagen, wenn der Presenter heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="4ea41-330">All of the methods should fail if the presenter is shut down.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4ea41-331"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>Onclockstart</strong></a></span><span class="sxs-lookup"><span data-stu-id="4ea41-331"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>OnClockStart</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="4ea41-332">Legen Sie den präsentatorstatus auf Started fest.</span><span class="sxs-lookup"><span data-stu-id="4ea41-332">Set the presenter state to started.</span></span></li>
<li><span data-ttu-id="4ea41-333">Wenn <em>llclockstarteset</em> nicht <strong>PRESENTATION_CURRENT_POSITION</strong>ist, leeren Sie die Warteschlange der Beispiele für den Presenter.</span><span class="sxs-lookup"><span data-stu-id="4ea41-333">If the <em>llClockStartOffset</em> is not <strong>PRESENTATION_CURRENT_POSITION</strong>, flush the presenter's queue of samples.</span></span> <span data-ttu-id="4ea41-334">(Dies entspricht dem Empfangen einer <strong>MFVP_MESSAGE_FLUSH</strong> Nachricht.)</span><span class="sxs-lookup"><span data-stu-id="4ea41-334">(This is equivalent to receiving an <strong>MFVP_MESSAGE_FLUSH</strong> message.)</span></span></li>
<li><span data-ttu-id="4ea41-335">Wenn eine vorherige Frame-Step-Anforderung noch aussteht, verarbeiten Sie die Anforderung (siehe <a href="#frame-stepping">Frame</a>-Step).</span><span class="sxs-lookup"><span data-stu-id="4ea41-335">If a previous frame-step request is still pending, process the request (see <a href="#frame-stepping">Frame Stepping</a>).</span></span> <span data-ttu-id="4ea41-336">Versuchen Sie andernfalls, die Ausgabe des Mischers zu verarbeiten (siehe <a href="#processing-output">Verarbeitung der Ausgabe</a>).</span><span class="sxs-lookup"><span data-stu-id="4ea41-336">Otherwise, try to process output from the mixer (see <a href="#processing-output">Processing Output</a>.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4ea41-337"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop"><strong>Onclockstoppt</strong></a></span><span class="sxs-lookup"><span data-stu-id="4ea41-337"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop"><strong>OnClockStop</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="4ea41-338">Legen Sie den präsentatorstatus auf beendet fest.</span><span class="sxs-lookup"><span data-stu-id="4ea41-338">Set the presenter state to stopped.</span></span></li>
<li><span data-ttu-id="4ea41-339">Leert die Warteschlange von Beispielen für den Presenter.</span><span class="sxs-lookup"><span data-stu-id="4ea41-339">Flush the presenter's queue of samples.</span></span></li>
<li><span data-ttu-id="4ea41-340">Abbrechen Sie alle ausstehenden Rahmen Schritt Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="4ea41-340">Cancel any pending frame-step operation.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4ea41-341"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockpause"><strong>Onclockpause</strong></a></span><span class="sxs-lookup"><span data-stu-id="4ea41-341"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockpause"><strong>OnClockPause</strong></a></span></span></td>
<td><span data-ttu-id="4ea41-342">Legen Sie den präsentatorstatus auf angehalten fest.</span><span class="sxs-lookup"><span data-stu-id="4ea41-342">Set the presenter state to paused.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4ea41-343"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart"><strong>Onclockrestart</strong></a></span><span class="sxs-lookup"><span data-stu-id="4ea41-343"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart"><strong>OnClockRestart</strong></a></span></span></td>
<td><span data-ttu-id="4ea41-344">Behandeln Sie das gleiche wie bei <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>onclockstart</strong></a> , aber lassen Sie die Warteschlange von Beispielen nicht leeren.</span><span class="sxs-lookup"><span data-stu-id="4ea41-344">Treat the same as <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>OnClockStart</strong></a> but do not flush the queue of samples.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4ea41-345"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate"><strong>Onclock-trate</strong></a></span><span class="sxs-lookup"><span data-stu-id="4ea41-345"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate"><strong>OnClockSetRate</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="4ea41-346">Wenn die Rate von 0 (null) in einen Wert ungleich 0 (null) wechselt, brechen Sie die Frame</span><span class="sxs-lookup"><span data-stu-id="4ea41-346">If the rate is changing from zero to nonzero, cancel frame stepping.</span></span></li>
<li><span data-ttu-id="4ea41-347">Speichern Sie die neue Taktrate.</span><span class="sxs-lookup"><span data-stu-id="4ea41-347">Store the new clock rate.</span></span> <span data-ttu-id="4ea41-348">Die Taktfrequenz wirkt sich auf die Anzeige von Beispielen aus.</span><span class="sxs-lookup"><span data-stu-id="4ea41-348">The clock rate affects when samples are presented.</span></span> <span data-ttu-id="4ea41-349">Weitere Informationen finden Sie unter <a href="#scheduling-samples">Beispiele</a>für die Planung.</span><span class="sxs-lookup"><span data-stu-id="4ea41-349">For more information, see <a href="#scheduling-samples">Scheduling Samples</a>.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="implementing-imfratesupport"></a><span data-ttu-id="4ea41-350">Implementieren von imfratesupport</span><span class="sxs-lookup"><span data-stu-id="4ea41-350">Implementing IMFRateSupport</span></span>

<span data-ttu-id="4ea41-351">Zur Unterstützung von Wiedergabe Raten mit Ausnahme von 1 × Geschwindigkeit muss der Presenter die [**imfratesupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="4ea41-351">To support playback rates other than 1× speed, the presenter must implement the [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) interface.</span></span> <span data-ttu-id="4ea41-352">Im folgenden finden Sie einige Richtlinien für die Implementierung der Methoden in dieser Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="4ea41-352">Here are some guidelines for implementing the methods in this interface.</span></span> <span data-ttu-id="4ea41-353">Alle Methoden sollten fehlschlagen, nachdem der Presenter heruntergefahren wurde.</span><span class="sxs-lookup"><span data-stu-id="4ea41-353">All of the methods should fail after the presenter is shut down.</span></span> <span data-ttu-id="4ea41-354">Weitere Informationen zu dieser Schnittstelle finden Sie unter [Raten Steuerung](rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="4ea41-354">For more information about this interface, see [Rate Control](rate-control.md).</span></span>



|                                                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4ea41-355">**Geort lowestrate**</span><span class="sxs-lookup"><span data-stu-id="4ea41-355">**GetSlowestRate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate)   | <span data-ttu-id="4ea41-356">Gibt 0 (null) zurück, um keine minimale Wiedergabe Rate anzugeben.</span><span class="sxs-lookup"><span data-stu-id="4ea41-356">Return zero to indicate no minimum playback rate.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="4ea41-357">**Getfastestrate**</span><span class="sxs-lookup"><span data-stu-id="4ea41-357">**GetFastestRate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate)   | <span data-ttu-id="4ea41-358">Bei einer nicht dünnen Wiedergabe sollte die Wiedergabe Rate nicht die Aktualisierungsrate des Monitors überschreiten: *Maximale Raten*  =  *Aktualisierungsrate* (Hz)/ *Video Frame Rate* (fps).</span><span class="sxs-lookup"><span data-stu-id="4ea41-358">For non-thinned playback, the playback rate should not exceed the refresh rate of the monitor: *maximum rate* = *refresh rate* (Hz) / *video frame rate* (fps).</span></span> <span data-ttu-id="4ea41-359">Die Video Frame Rate wird im Medientyp des Presenter angegeben.</span><span class="sxs-lookup"><span data-stu-id="4ea41-359">The video frame rate is specified in the presenter's media type.</span></span> <br/> <span data-ttu-id="4ea41-360">Bei der dünnen Wiedergabe ist die Wiedergabe Rate unbegrenzt. Gibt den Wert **FLT_MAX** zurück.</span><span class="sxs-lookup"><span data-stu-id="4ea41-360">For thinned playback, the playback rate is unbounded; return the value **FLT_MAX**.</span></span> <span data-ttu-id="4ea41-361">In der Praxis sind Quelle und Decoder die einschränkenden Faktoren bei der dünnen Wiedergabe.</span><span class="sxs-lookup"><span data-stu-id="4ea41-361">In practice, the source and the decoder will be the limiting factors during thinned playback.</span></span> <br/> <span data-ttu-id="4ea41-362">Geben Sie für die umgekehrte Wiedergabe den negativen Wert der maximalen Rate zurück.</span><span class="sxs-lookup"><span data-stu-id="4ea41-362">For reverse playback, return the negative of the maximum rate.</span></span><br/> |
| [<span data-ttu-id="4ea41-363">**Isratesupportiert**</span><span class="sxs-lookup"><span data-stu-id="4ea41-363">**IsRateSupported**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) | <span data-ttu-id="4ea41-364">Gibt **MF_E_UNSUPPORTED_RATE** zurück, wenn der absolute Wert von *flrate* die maximale Wiedergabe Rate des Presenter überschreitet.</span><span class="sxs-lookup"><span data-stu-id="4ea41-364">Return **MF_E_UNSUPPORTED_RATE** if the absolute value of *flRate* exceeds the presenter's maximum playback rate.</span></span> <span data-ttu-id="4ea41-365">Berechnen Sie die maximale Wiedergabe Rate, wie für [**getfastestrate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4ea41-365">Calculate the maximum playback rate as described for [**GetFastestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate).</span></span>                                                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="4ea41-366">Im folgenden Beispiel wird gezeigt, wie die [**getfastestrate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate) -Methode implementiert wird:</span><span class="sxs-lookup"><span data-stu-id="4ea41-366">The following example shows how to implement the [**GetFastestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate) method:</span></span>


```C++
float EVRCustomPresenter::GetMaxRate(BOOL bThin)
{
    // Non-thinned:
    // If we have a valid frame rate and a monitor refresh rate, the maximum
    // playback rate is equal to the refresh rate. Otherwise, the maximum rate
    // is unbounded (FLT_MAX).

    // Thinned: The maximum rate is unbounded.

    float   fMaxRate = FLT_MAX;
    MFRatio fps = { 0, 0 };
    UINT    MonitorRateHz = 0;

    if (!bThin && (m_pMediaType != NULL))
    {
        GetFrameRate(m_pMediaType, &fps);
        MonitorRateHz = m_pD3DPresentEngine->RefreshRate();

        if (fps.Denominator && fps.Numerator && MonitorRateHz)
        {
            // Max Rate = Refresh Rate / Frame Rate
            fMaxRate = (float)MulDiv(
                MonitorRateHz, fps.Denominator, fps.Numerator);
        }
    }

    return fMaxRate;
}
```



<span data-ttu-id="4ea41-367">Im vorherigen Beispiel wird die Hilfsmethode getmaxrate aufgerufen, um die maximale vorwärts Wiedergabe Rate zu berechnen:</span><span class="sxs-lookup"><span data-stu-id="4ea41-367">The previous example calls a helper method, GetMaxRate, to calculate the maximum forward playback rate:</span></span>

<span data-ttu-id="4ea41-368">Im folgenden Beispiel wird gezeigt, wie die [**isratesupportiert**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) -Methode implementiert wird:</span><span class="sxs-lookup"><span data-stu-id="4ea41-368">The following example shows how to implement the [**IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) method:</span></span>


```C++
HRESULT EVRCustomPresenter::IsRateSupported(
    BOOL bThin,
    float fRate,
    float *pfNearestSupportedRate
    )
{
    EnterCriticalSection(&m_ObjectLock);

    float   fMaxRate = 0.0f;
    float   fNearestRate = fRate;  // If we support fRate, that is the nearest.

    HRESULT hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    // Find the maximum forward rate.
    // Note: We have no minimum rate (that is, we support anything down to 0).
    fMaxRate = GetMaxRate(bThin);

    if (fabsf(fRate) > fMaxRate)
    {
        // The (absolute) requested rate exceeds the maximum rate.
        hr = MF_E_UNSUPPORTED_RATE;

        // The nearest supported rate is fMaxRate.
        fNearestRate = fMaxRate;
        if (fRate < 0)
        {
            // Negative for reverse playback.
            fNearestRate = -fNearestRate;
        }
    }

    // Return the nearest supported rate.
    if (pfNearestSupportedRate != NULL)
    {
        *pfNearestSupportedRate = fNearestRate;
    }

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



### <a name="sending-events-to-the-evr"></a><span data-ttu-id="4ea41-369">Senden von Ereignissen an den EVR</span><span class="sxs-lookup"><span data-stu-id="4ea41-369">Sending Events to the EVR</span></span>

<span data-ttu-id="4ea41-370">Der Presenter muss den EVR verschiedener Ereignisse benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-370">The presenter must notify the EVR of various events.</span></span> <span data-ttu-id="4ea41-371">Hierfür wird die [**imediaeventsink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) -Schnittstelle von EVR verwendet, die abgerufen wird, wenn der EVR die [**imftopologyservicelookupclient:: initservicepointer**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) -Methode des Presenter aufruft.</span><span class="sxs-lookup"><span data-stu-id="4ea41-371">To do so, it uses the EVR's [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) interface, obtained when the EVR calls the presenter's [**IMFTopologyServiceLookupClient::InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) method.</span></span> <span data-ttu-id="4ea41-372">(Die **imediaeventsink** -Schnittstelle ist ursprünglich eine DirectShow-Schnittstelle, wird aber sowohl in DirectShow EVR als auch in der Media Foundation verwendet.) Der folgende Code zeigt, wie ein Ereignis an den EVR gesendet wird:</span><span class="sxs-lookup"><span data-stu-id="4ea41-372">(The **IMediaEventSink** interface is originally a DirectShow interface, but is used in both the DirectShow EVR and the Media Foundation.) The following code shows how to send an event to the EVR:</span></span>


```C++
    // NotifyEvent: Send an event to the EVR through its IMediaEventSink interface.
    void NotifyEvent(long EventCode, LONG_PTR Param1, LONG_PTR Param2)
    {
        if (m_pMediaEventSink)
        {
            m_pMediaEventSink->Notify(EventCode, Param1, Param2);
        }
    }
```



<span data-ttu-id="4ea41-373">In der folgenden Tabelle werden die vom Presenter gesendeten Ereignisse zusammen mit den Ereignis Parametern aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="4ea41-373">The following table lists the events that the presenter sends, along with the event parameters.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4ea41-374">Ereignis</span><span class="sxs-lookup"><span data-stu-id="4ea41-374">Event</span></span></th>
<th><span data-ttu-id="4ea41-375">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4ea41-375">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4ea41-376"><a href="/windows/desktop/DirectShow/ec-complete"><strong>EC_COMPLETE</strong></a></span><span class="sxs-lookup"><span data-stu-id="4ea41-376"><a href="/windows/desktop/DirectShow/ec-complete"><strong>EC_COMPLETE</strong></a></span></span></td>
<td><span data-ttu-id="4ea41-377">Der Presenter hat das Rendern aller Frames nach der MFVP_MESSAGE_ENDOFSTREAM Meldung abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-377">The presenter has finished rendering all frames after the MFVP_MESSAGE_ENDOFSTREAM message.</span></span><br/>
<ul>
<li><span data-ttu-id="4ea41-378"><em>Param1</em>: HRESULT, das den Status des Vorgangs angibt.</span><span class="sxs-lookup"><span data-stu-id="4ea41-378"><em>Param1</em>: HRESULT indicating the status of the operation.</span></span></li>
<li><span data-ttu-id="4ea41-379"><em>Param2</em>: nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ea41-379"><em>Param2</em>: Not used.</span></span></li>
</ul>
<span data-ttu-id="4ea41-380">Weitere Informationen finden Sie unter <a href="#end-of-stream">Ende des Datenstroms</a>.</span><span class="sxs-lookup"><span data-stu-id="4ea41-380">For more information, see <a href="#end-of-stream">End of Stream</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4ea41-381"><a href="/windows/desktop/DirectShow/ec-display-changed"><strong>EC_DISPLAY_CHANGED</strong></a></span><span class="sxs-lookup"><span data-stu-id="4ea41-381"><a href="/windows/desktop/DirectShow/ec-display-changed"><strong>EC_DISPLAY_CHANGED</strong></a></span></span></td>
<td><span data-ttu-id="4ea41-382">Das Direct3D-Gerät wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="4ea41-382">The Direct3D device has changed.</span></span><br/>
<ul>
<li><span data-ttu-id="4ea41-383"><em>Param1</em>: nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ea41-383"><em>Param1</em>: Not used.</span></span></li>
<li><span data-ttu-id="4ea41-384"><em>Param2</em>: nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ea41-384"><em>Param2</em>: Not used.</span></span></li>
</ul>
<span data-ttu-id="4ea41-385">Weitere Informationen finden Sie unter <a href="#managing-the-direct3d-device">Verwalten des Direct3D-Geräts</a>.</span><span class="sxs-lookup"><span data-stu-id="4ea41-385">For more information, see <a href="#managing-the-direct3d-device">Managing the Direct3D Device</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4ea41-386"><a href="/windows/desktop/DirectShow/ec-errorabort"><strong>EC_ERRORABORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="4ea41-386"><a href="/windows/desktop/DirectShow/ec-errorabort"><strong>EC_ERRORABORT</strong></a></span></span></td>
<td><span data-ttu-id="4ea41-387">Ein Fehler ist aufgetreten, bei dem das Streaming beendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="4ea41-387">An error has occurred that requires streaming to stop.</span></span><br/>
<ul>
<li><span data-ttu-id="4ea41-388"><em>Param1</em>: <strong>HRESULT</strong> , das den Fehler angibt, der aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="4ea41-388"><em>Param1</em>: <strong>HRESULT</strong> indicating the error that occurred.</span></span></li>
<li><span data-ttu-id="4ea41-389"><em>Param2</em>: nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ea41-389"><em>Param2</em>: Not used.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4ea41-390"><a href="/windows/desktop/DirectShow/ec-processing-latency"><strong>EC_PROCESSING_LATENCY</strong></a></span><span class="sxs-lookup"><span data-stu-id="4ea41-390"><a href="/windows/desktop/DirectShow/ec-processing-latency"><strong>EC_PROCESSING_LATENCY</strong></a></span></span></td>
<td><span data-ttu-id="4ea41-391">Gibt die Zeitspanne an, die der Presenter zum Rendering der einzelnen Frames einnimmt.</span><span class="sxs-lookup"><span data-stu-id="4ea41-391">Specifies the amount of time that the presenter is taking to render each frame.</span></span> <span data-ttu-id="4ea41-392">(Optional.)</span><span class="sxs-lookup"><span data-stu-id="4ea41-392">(Optional.)</span></span><br/>
<ul>
<li><span data-ttu-id="4ea41-393"><em>Param1</em>: Zeiger auf einen Konstanten <strong>Longlong</strong> -Wert, der die Zeitspanne für die Verarbeitung des Frames in 100-Nanosecond-Einheiten enthält.</span><span class="sxs-lookup"><span data-stu-id="4ea41-393"><em>Param1</em>: Pointer to a constant <strong>LONGLONG</strong> value that contains the amount of time to process the frame, in 100-nanosecond units.</span></span></li>
<li><span data-ttu-id="4ea41-394"><em>Param2</em>: nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ea41-394"><em>Param2</em>: Not used.</span></span></li>
</ul>
<span data-ttu-id="4ea41-395">Weitere Informationen finden Sie unter <a href="#processing-output">Verarbeiten der Ausgabe</a>.</span><span class="sxs-lookup"><span data-stu-id="4ea41-395">For more information, see <a href="#processing-output">Processing Output</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4ea41-396"><a href="/windows/desktop/DirectShow/ec-sample-latency"><strong>EC_SAMPLE_LATENCY</strong></a></span><span class="sxs-lookup"><span data-stu-id="4ea41-396"><a href="/windows/desktop/DirectShow/ec-sample-latency"><strong>EC_SAMPLE_LATENCY</strong></a></span></span></td>
<td><span data-ttu-id="4ea41-397">Gibt die aktuelle Verzögerungszeit in renderingbeispielen an.</span><span class="sxs-lookup"><span data-stu-id="4ea41-397">Specifies the current lag time in rendering samples.</span></span> <span data-ttu-id="4ea41-398">Wenn der Wert positiv ist, werden die Beispiele hinter dem Zeitplan angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4ea41-398">If the value is positive, samples are behind schedule.</span></span> <span data-ttu-id="4ea41-399">Wenn der Wert negativ ist, werden die Beispiele vor dem Zeitplan angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4ea41-399">If the value is negative, samples are ahead of schedule.</span></span> <span data-ttu-id="4ea41-400">(Optional.)</span><span class="sxs-lookup"><span data-stu-id="4ea41-400">(Optional.)</span></span><br/>
<ul>
<li><span data-ttu-id="4ea41-401"><em>Param1</em>: Zeiger auf einen Konstanten <strong>Longlong</strong> -Wert, der die Verzögerungszeit in 100-Nanosecond-Einheiten enthält.</span><span class="sxs-lookup"><span data-stu-id="4ea41-401"><em>Param1</em>: Pointer to a constant <strong>LONGLONG</strong> value that contains the lag time, in 100-nanosecond units.</span></span></li>
<li><span data-ttu-id="4ea41-402"><em>Param2</em>: nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ea41-402"><em>Param2</em>: Not used.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4ea41-403"><a href="/windows/desktop/DirectShow/ec-scrub-time"><strong>EC_SCRUB_TIME</strong></a></span><span class="sxs-lookup"><span data-stu-id="4ea41-403"><a href="/windows/desktop/DirectShow/ec-scrub-time"><strong>EC_SCRUB_TIME</strong></a></span></span></td>
<td><span data-ttu-id="4ea41-404">Wird unmittelbar nach <strong>EC_STEP_COMPLETE</strong> gesendet, wenn die Wiedergabe Rate 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="4ea41-404">Sent immediately after <strong>EC_STEP_COMPLETE</strong> if the playback rate is zero.</span></span> <span data-ttu-id="4ea41-405">Dieses Ereignis enthält den Zeitstempel des Bilds, der angezeigt wurde.</span><span class="sxs-lookup"><span data-stu-id="4ea41-405">This event contains the time stamp of the frame that was displayed.</span></span><br/>
<ul>
<li><span data-ttu-id="4ea41-406"><em>Param1</em>: niedrigere 32 Bits des Zeitstempels.</span><span class="sxs-lookup"><span data-stu-id="4ea41-406"><em>Param1</em>: Lower 32 bits of the time stamp.</span></span></li>
<li><span data-ttu-id="4ea41-407"><em>Param2</em>: Obere 32 Bits des Zeitstempels.</span><span class="sxs-lookup"><span data-stu-id="4ea41-407"><em>Param2</em>: Upper 32 bits of the time stamp.</span></span></li>
</ul>
<span data-ttu-id="4ea41-408">Weitere Informationen finden Sie unter <a href="#frame-stepping">Frame Step Stepping</a>.</span><span class="sxs-lookup"><span data-stu-id="4ea41-408">For more information, see <a href="#frame-stepping">Frame Stepping</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4ea41-409"><a href="/windows/desktop/DirectShow/ec-step-complete"><strong>EC_STEP_COMPLETE</strong></a></span><span class="sxs-lookup"><span data-stu-id="4ea41-409"><a href="/windows/desktop/DirectShow/ec-step-complete"><strong>EC_STEP_COMPLETE</strong></a></span></span></td>
<td><span data-ttu-id="4ea41-410">Der Presenter hat einen Frame Schritt abgeschlossen oder abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-410">The presenter has completed or canceled a frame step.</span></span><br/>
<ul>
<li><span data-ttu-id="4ea41-411"><em>Param1</em>: nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ea41-411"><em>Param1</em>: Not used.</span></span></li>
<li><span data-ttu-id="4ea41-412"><em>Param2</em>: nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ea41-412"><em>Param2</em>: Not used.</span></span></li>
</ul>
<span data-ttu-id="4ea41-413">Weitere Informationen finden Sie unter <a href="#frame-stepping">Frame Step Stepping</a>.</span><span class="sxs-lookup"><span data-stu-id="4ea41-413">For more information, see <a href="#frame-stepping">Frame Stepping</a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4ea41-414">Eine frühere Version der beschriebenen Dokumentation <em>param1</em> falsch.</span><span class="sxs-lookup"><span data-stu-id="4ea41-414">A previous version of the documentation described <em>Param1</em> incorrectly.</span></span> <span data-ttu-id="4ea41-415">Dieser Parameter wird für dieses Ereignis nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ea41-415">This parameter is not used for this event.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="negotiating-formats"></a><span data-ttu-id="4ea41-416">Aushandeln von Formaten</span><span class="sxs-lookup"><span data-stu-id="4ea41-416">Negotiating Formats</span></span>

<span data-ttu-id="4ea41-417">Jedes Mal, wenn der Presenter eine **MFVP_MESSAGE_INVALIDATEMEDIATYPE** Nachricht vom EVR empfängt, muss er wie folgt das Ausgabeformat auf dem Mixer festlegen:</span><span class="sxs-lookup"><span data-stu-id="4ea41-417">Whenever the presenter receives an **MFVP_MESSAGE_INVALIDATEMEDIATYPE** message from the EVR, it must set the output format on the mixer, as follows:</span></span>

1.  <span data-ttu-id="4ea41-418">Wenn Sie [**imftransform:: getoutputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) auf dem Mixer aufrufen, erhalten Sie einen möglichen Ausgabetyp.</span><span class="sxs-lookup"><span data-stu-id="4ea41-418">Call [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) on the mixer to get a possible output type.</span></span> <span data-ttu-id="4ea41-419">Dieser Typ beschreibt ein Format, das der Mixer mithilfe der Eingabestreams und der Video Verarbeitungsfunktionen des Grafik Geräts erzeugt.</span><span class="sxs-lookup"><span data-stu-id="4ea41-419">This type describes a format that the mixer can produce given the input streams and the video processing capabilities of the graphics device.</span></span>
2.  <span data-ttu-id="4ea41-420">Überprüfen Sie, ob der Presenter diesen Medientyp als Renderingformat verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="4ea41-420">Check whether the presenter can use this media type as its rendering format.</span></span> <span data-ttu-id="4ea41-421">Im folgenden finden Sie einige Dinge, die Sie überprüfen müssen, obwohl ihre Implementierung möglicherweise eigene Anforderungen erfüllt:</span><span class="sxs-lookup"><span data-stu-id="4ea41-421">Here are some things to check, although your implementation might have its own requirements:</span></span>

    -   <span data-ttu-id="4ea41-422">Das Video muss nicht komprimiert werden.</span><span class="sxs-lookup"><span data-stu-id="4ea41-422">The video must be uncompressed.</span></span>
    -   <span data-ttu-id="4ea41-423">Das Video darf nur progressive Frames enthalten.</span><span class="sxs-lookup"><span data-stu-id="4ea41-423">The video must have progressive frames only.</span></span> <span data-ttu-id="4ea41-424">Überprüfen Sie, ob das [**MF_MT_INTERLACE_MODE**](mf-mt-interlace-mode-attribute.md) Attribut **MFVideoInterlace_Progressive** ist.</span><span class="sxs-lookup"><span data-stu-id="4ea41-424">Check that the [**MF_MT_INTERLACE_MODE**](mf-mt-interlace-mode-attribute.md) attribute equals **MFVideoInterlace_Progressive**.</span></span>
    -   <span data-ttu-id="4ea41-425">Das Format muss mit dem Direct3D-Gerät kompatibel sein.</span><span class="sxs-lookup"><span data-stu-id="4ea41-425">The format must be compatible with the Direct3D device.</span></span>

    <span data-ttu-id="4ea41-426">Wenn der Typ nicht zulässig ist, kehren Sie zu Schritt 1 zurück, und holen Sie den nächsten vorgeschlagenen Typ des Mischers.</span><span class="sxs-lookup"><span data-stu-id="4ea41-426">If the type is not acceptable, return to step 1 and get the mixer's next proposed type.</span></span>

3.  <span data-ttu-id="4ea41-427">Erstellen Sie einen neuen Medientyp, bei dem es sich um einen Klon des ursprünglichen Typs handelt, und ändern Sie dann die folgenden Attribute:</span><span class="sxs-lookup"><span data-stu-id="4ea41-427">Create a new media type that is a clone of the original type and then change the following attributes:</span></span>

    -   <span data-ttu-id="4ea41-428">Legen Sie für die Direct3D-Oberflächen, die Sie zuordnen möchten, das [**MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) -Attribut gleich der Breite und Höhe fest.</span><span class="sxs-lookup"><span data-stu-id="4ea41-428">Set the [**MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) attribute equal to the width and height that you want for the Direct3D surfaces you will allocate.</span></span>
    -   <span data-ttu-id="4ea41-429">Legen Sie das [**MF_MT_PAN_SCAN_ENABLED**](mf-mt-pan-scan-enabled-attribute.md) -Attribut auf " **false**" fest.</span><span class="sxs-lookup"><span data-stu-id="4ea41-429">Set the [**MF_MT_PAN_SCAN_ENABLED**](mf-mt-pan-scan-enabled-attribute.md) attribute to **FALSE**.</span></span>
    -   <span data-ttu-id="4ea41-430">Legen Sie das [**MF_MT_PIXEL_ASPECT_RATIO**](mf-mt-pixel-aspect-ratio-attribute.md) -Attribut auf das Par der Anzeige fest (in der Regel 1:1).</span><span class="sxs-lookup"><span data-stu-id="4ea41-430">Set the [**MF_MT_PIXEL_ASPECT_RATIO**](mf-mt-pixel-aspect-ratio-attribute.md) attribute equal to the PAR of the display (typically 1:1).</span></span>
    -   <span data-ttu-id="4ea41-431">Legen Sie die geometrische Aperture ([**MF_MT_GEOMETRIC_APERTURE**](mf-mt-geometric-aperture-attribute.md) -Attribut) auf ein Rechteck innerhalb der Direct3D-Oberfläche fest.</span><span class="sxs-lookup"><span data-stu-id="4ea41-431">Set the geometric aperture ([**MF_MT_GEOMETRIC_APERTURE**](mf-mt-geometric-aperture-attribute.md) attribute) equal to a rectangle within the Direct3D surface.</span></span> <span data-ttu-id="4ea41-432">Wenn der Mixer einen Ausgabe Rahmen generiert, wird das Quell Bild auf dieses Rechteck gebliert.</span><span class="sxs-lookup"><span data-stu-id="4ea41-432">When the mixer generates an output frame, it blits the source image onto this rectangle.</span></span> <span data-ttu-id="4ea41-433">Die geometrische Öffnung kann so groß wie die Oberfläche sein, oder es kann sich um ein unter Rechteck innerhalb der Oberfläche handeln.</span><span class="sxs-lookup"><span data-stu-id="4ea41-433">The geometric aperture can be as large as the surface, or it can be a subrectangle within the surface.</span></span> <span data-ttu-id="4ea41-434">Weitere Informationen finden Sie unter [Quell-und Ziel Rechtecke](#source-and-destination-rectangles).</span><span class="sxs-lookup"><span data-stu-id="4ea41-434">For more information, see [Source and Destination Rectangles](#source-and-destination-rectangles).</span></span>

4.  <span data-ttu-id="4ea41-435">Um zu testen, ob der Mixer den geänderten Ausgabetyp akzeptiert, müssen Sie [**imftransform:: setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) mit dem **MFT_SET_TYPE_TEST_ONLY** -Flag aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-435">To test whether the mixer will accept the modified output type, call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) with the **MFT_SET_TYPE_TEST_ONLY** flag.</span></span> <span data-ttu-id="4ea41-436">Wenn der Mixer den Typ ablehnt, kehren Sie zu Schritt 1 zurück, und rufen Sie den nächsten Typ ab.</span><span class="sxs-lookup"><span data-stu-id="4ea41-436">If the mixer rejects the type, go back to step 1 and get the next type.</span></span>
5.  <span data-ttu-id="4ea41-437">Ordnen Sie einen Pool mit Direct3D-Oberflächen zu, wie unter [Zuordnen von Direct3D-Oberflächen](#allocating-direct3d-surfaces)beschrieben</span><span class="sxs-lookup"><span data-stu-id="4ea41-437">Allocate a pool of Direct3D surfaces, as described in [Allocating Direct3D Surfaces](#allocating-direct3d-surfaces).</span></span> <span data-ttu-id="4ea41-438">Der Mixer verwendet diese Oberflächen, wenn die zusammengesetzten Video Frames gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="4ea41-438">The mixer will use these surfaces when it draws the composited video frames.</span></span>
6.  <span data-ttu-id="4ea41-439">Legen Sie den Ausgabetyp für den Mixer fest, indem Sie [**setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) ohne Flags aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-439">Set the output type on the mixer by calling [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) with no flags.</span></span> <span data-ttu-id="4ea41-440">Wenn der erste aufzurufende **setoutputtype** -Befehl in Schritt 4 erfolgreich war, sollte die-Methode erneut ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4ea41-440">If the first call to **SetOutputType** succeeded in step 4, the method should succeed again.</span></span>

<span data-ttu-id="4ea41-441">Wenn der Mixer nicht mehr über Typen verfügt, gibt die [**getoutputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) -Methode **MF_E_NO_MORE_TYPES** zurück.</span><span class="sxs-lookup"><span data-stu-id="4ea41-441">If the mixer runs out of types, the [**GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) method returns **MF_E_NO_MORE_TYPES**.</span></span> <span data-ttu-id="4ea41-442">Wenn der Presenter keinen geeigneten Ausgabetyp für den Mixer finden kann, kann der Stream nicht gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="4ea41-442">If the presenter cannot find a suitable output type for the mixer, the stream cannot be rendered.</span></span> <span data-ttu-id="4ea41-443">In diesem Fall kann DirectShow oder Media Foundation ein anderes Streamformat ausprobieren.</span><span class="sxs-lookup"><span data-stu-id="4ea41-443">In that case, DirectShow or Media Foundation might try another stream format.</span></span> <span data-ttu-id="4ea41-444">Aus diesem Grund kann der Presenter mehrere **MFVP_MESSAGE_INVALIDATEMEDIATYPE** Nachrichten in einer Zeile erhalten, bis ein gültiger Typ gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="4ea41-444">Therefore, the presenter might receive several **MFVP_MESSAGE_INVALIDATEMEDIATYPE** messages in a row until a valid type is found.</span></span>

<span data-ttu-id="4ea41-445">Der Mixer zieht das Video automatisch ein, wobei das Pixel Seitenverhältnis (par) der Quelle und des Ziels berücksichtigt wird.</span><span class="sxs-lookup"><span data-stu-id="4ea41-445">The mixer automatically letterboxes the video, taking into account the pixel aspect ratio (PAR) of the source and destination.</span></span> <span data-ttu-id="4ea41-446">Um optimale Ergebnisse zu erzielen, sollten die Breite und Höhe der Oberfläche und die geometrische Öffnung gleich der tatsächlichen Größe sein, die das Video in der Anzeige anzeigen soll.</span><span class="sxs-lookup"><span data-stu-id="4ea41-446">For best results, the surface width and height and the geometric aperture should be equal to the actual size that you want the video to appear on the display.</span></span> <span data-ttu-id="4ea41-447">Dieses Verfahren wird in der folgenden Abbildung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="4ea41-447">The following image illustrates this process.</span></span>

![Diagramm, das einen zusammengesetzten Fram anzeigt, der zu einer Direct3D-Oberfläche führt, die zu einem Fenster führt](images/b746edca-8830-4c88-aa59-0067b020d4af.gif)

<span data-ttu-id="4ea41-449">Der folgende Code zeigt die Gliederung des Prozesses.</span><span class="sxs-lookup"><span data-stu-id="4ea41-449">The following code shows the outline of the process.</span></span> <span data-ttu-id="4ea41-450">Einige der Schritte werden in Hilfsfunktionen platziert, die genaue Details, die von den Anforderungen Ihres Presenter abhängen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-450">Some of the steps are placed in helper functions, the exact details of which will depend on the requirements of your presenter.</span></span>


```C++
HRESULT EVRCustomPresenter::RenegotiateMediaType()
{
    HRESULT hr = S_OK;
    BOOL bFoundMediaType = FALSE;

    IMFMediaType *pMixerType = NULL;
    IMFMediaType *pOptimalType = NULL;
    IMFVideoMediaType *pVideoType = NULL;

    if (!m_pMixer)
    {
        return MF_E_INVALIDREQUEST;
    }

    // Loop through all of the mixer's proposed output types.
    DWORD iTypeIndex = 0;
    while (!bFoundMediaType && (hr != MF_E_NO_MORE_TYPES))
    {
        SafeRelease(&pMixerType);
        SafeRelease(&pOptimalType);

        // Step 1. Get the next media type supported by mixer.
        hr = m_pMixer->GetOutputAvailableType(0, iTypeIndex++, &pMixerType);
        if (FAILED(hr))
        {
            break;
        }

        // From now on, if anything in this loop fails, try the next type,
        // until we succeed or the mixer runs out of types.

        // Step 2. Check if we support this media type.
        if (SUCCEEDED(hr))
        {
            // Note: None of the modifications that we make later in CreateOptimalVideoType
            // will affect the suitability of the type, at least for us. (Possibly for the mixer.)
            hr = IsMediaTypeSupported(pMixerType);
        }

        // Step 3. Adjust the mixer's type to match our requirements.
        if (SUCCEEDED(hr))
        {
            hr = CreateOptimalVideoType(pMixerType, &pOptimalType);
        }

        // Step 4. Check if the mixer will accept this media type.
        if (SUCCEEDED(hr))
        {
            hr = m_pMixer->SetOutputType(0, pOptimalType, MFT_SET_TYPE_TEST_ONLY);
        }

        // Step 5. Try to set the media type on ourselves.
        if (SUCCEEDED(hr))
        {
            hr = SetMediaType(pOptimalType);
        }

        // Step 6. Set output media type on mixer.
        if (SUCCEEDED(hr))
        {
            hr = m_pMixer->SetOutputType(0, pOptimalType, 0);

            assert(SUCCEEDED(hr)); // This should succeed unless the MFT lied in the previous call.

            // If something went wrong, clear the media type.
            if (FAILED(hr))
            {
                SetMediaType(NULL);
            }
        }

        if (SUCCEEDED(hr))
        {
            bFoundMediaType = TRUE;
        }
    }

    SafeRelease(&pMixerType);
    SafeRelease(&pOptimalType);
    SafeRelease(&pVideoType);

    return hr;
}
```



<span data-ttu-id="4ea41-451">Weitere Informationen zu Video Medientypen finden Sie unter [Video Medientypen](video-media-types.md).</span><span class="sxs-lookup"><span data-stu-id="4ea41-451">For more information about video media types, see [Video Media Types](video-media-types.md).</span></span>

## <a name="managing-the-direct3d-device"></a><span data-ttu-id="4ea41-452">Verwalten des Direct3D-Geräts</span><span class="sxs-lookup"><span data-stu-id="4ea41-452">Managing the Direct3D Device</span></span>

<span data-ttu-id="4ea41-453">Der Presenter erstellt das Direct3D-Gerät und verarbeitet alle Geräte Verluste beim Streaming.</span><span class="sxs-lookup"><span data-stu-id="4ea41-453">The presenter creates the Direct3D device and handles any device loss during streaming.</span></span> <span data-ttu-id="4ea41-454">Außerdem hostet der Presenter den Direct3D-Geräte-Manager, der es anderen Komponenten ermöglicht, dasselbe Gerät zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="4ea41-454">The presenter also hosts the Direct3D device manager, which provides a way for other components to use the same device.</span></span> <span data-ttu-id="4ea41-455">Beispielsweise verwendet der Mixer das Direct3D-Gerät zum Mischen von Substreams, deinterlace und zum Durchführen von Farbanpassungen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-455">For example, the mixer uses the Direct3D device to mix substreams, deinterlace, and perform color adjustments.</span></span> <span data-ttu-id="4ea41-456">Decoderer können das Direct3D-Gerät für die Video beschleunigte Decodierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="4ea41-456">Decoders can use the Direct3D device for video-accelerated decoding.</span></span> <span data-ttu-id="4ea41-457">(Weitere Informationen zur Videobeschleunigung finden Sie unter [DirectX-Videobeschleunigung 2,0](directx-video-acceleration-2-0.md).)</span><span class="sxs-lookup"><span data-stu-id="4ea41-457">(For more information about video acceleration, see [DirectX Video Acceleration 2.0](directx-video-acceleration-2-0.md).)</span></span>

<span data-ttu-id="4ea41-458">Führen Sie die folgenden Schritte aus, um das Direct3D-Gerät einzurichten:</span><span class="sxs-lookup"><span data-stu-id="4ea41-458">To set up the Direct3D device, perform the following steps:</span></span>

1.  <span data-ttu-id="4ea41-459">Erstellen Sie das Direct3D-Objekt durch Aufrufen von **Direct3DCreate9** oder **Direct3DCreate9Ex**.</span><span class="sxs-lookup"><span data-stu-id="4ea41-459">Create the Direct3D object by calling **Direct3DCreate9** or **Direct3DCreate9Ex**.</span></span>
2.  <span data-ttu-id="4ea41-460">Erstellen Sie das Gerät durch Aufrufen von **IDirect3D9:: createdevice** oder **IDirect3D9Ex:: createdevice**.</span><span class="sxs-lookup"><span data-stu-id="4ea41-460">Create the device by calling **IDirect3D9::CreateDevice** or **IDirect3D9Ex::CreateDevice**.</span></span>
3.  <span data-ttu-id="4ea41-461">Erstellen Sie den Geräte-Manager durch Aufrufen von [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9).</span><span class="sxs-lookup"><span data-stu-id="4ea41-461">Create the device manager by calling [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9).</span></span>
4.  <span data-ttu-id="4ea41-462">Legen Sie das Gerät im Geräte-Manager durch Aufrufen von [**IDirect3DDeviceManager9:: ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice)fest.</span><span class="sxs-lookup"><span data-stu-id="4ea41-462">Set the device on the device manager by calling [**IDirect3DDeviceManager9::ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice).</span></span>

<span data-ttu-id="4ea41-463">Wenn eine andere Pipeline Komponente den Geräte-Manager benötigt, ruft Sie [**imfgetservice:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) auf dem EVR auf und gibt **MR_VIDEO_ACCELERATION_SERVICE** für die Dienst-GUID an.</span><span class="sxs-lookup"><span data-stu-id="4ea41-463">If another pipeline component needs the device manager, it calls [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the EVR, specifying **MR_VIDEO_ACCELERATION_SERVICE** for the service GUID.</span></span> <span data-ttu-id="4ea41-464">Der EVR übergibt die Anforderung an den Presenter.</span><span class="sxs-lookup"><span data-stu-id="4ea41-464">The EVR passes the request to the presenter.</span></span> <span data-ttu-id="4ea41-465">Nachdem das Objekt den [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) -Zeiger abgerufen hat, kann es durch Aufrufen von [**IDirect3DDeviceManager9:: opendevicehandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle)ein Handle für das Gerät abrufen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-465">After the object gets the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) pointer, it can get a handle to the device by calling [**IDirect3DDeviceManager9::OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle).</span></span> <span data-ttu-id="4ea41-466">Wenn das Objekt das Gerät verwenden muss, übergibt es das Geräte Handle an die [**IDirect3DDeviceManager9:: lockdevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) -Methode, die einen **IDirect3DDevice9** -Zeiger zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="4ea41-466">When the object needs to use the device, it passes the device handle to the [**IDirect3DDeviceManager9::LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) method, which returns an **IDirect3DDevice9** pointer.</span></span>

<span data-ttu-id="4ea41-467">Nachdem das Gerät erstellt wurde und der Presenter das Gerät zerstört und ein neues erstellt hat, muss der Presenter [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) erneut aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-467">After the device is created, if the presenter destroys the device and creates a new one, the presenter must call [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) again.</span></span> <span data-ttu-id="4ea41-468">Die **ResetDevice** -Methode macht alle vorhandenen Geräte Handles ungültig, was dazu führt, dass [**lockdevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) **DXVA2_E_NEW_VIDEO_DEVICE** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="4ea41-468">The **ResetDevice** method invalidates any existing device handles, which causes [**LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) to return **DXVA2_E_NEW_VIDEO_DEVICE**.</span></span> <span data-ttu-id="4ea41-469">Mit diesem Fehlercode wird anderen Objekten das Gerät signalisiert, dass ein neues Geräte Handle geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4ea41-469">This error code signals to other objects using the device that they should open a new device handle.</span></span> <span data-ttu-id="4ea41-470">Weitere Informationen zum Verwenden des Geräte-Managers finden Sie unter [Direct3D Device Manager](direct3d-device-manager.md).</span><span class="sxs-lookup"><span data-stu-id="4ea41-470">For more information about using the device manager, see [Direct3D Device Manager](direct3d-device-manager.md).</span></span>

<span data-ttu-id="4ea41-471">Der Presenter kann das Gerät im Fenstermodus oder im Vollbildmodus im exklusiven Modus erstellen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-471">The presenter can create the device in windowed mode or full-screen exclusive mode.</span></span> <span data-ttu-id="4ea41-472">Für den Fenstermodus sollten Sie eine Möglichkeit zur Angabe des Videofensters für die Anwendung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-472">For windowed mode, you should provide a way for the application to specify the video window.</span></span> <span data-ttu-id="4ea41-473">Der Standard Presenter implementiert zu diesem Zweck die [**IMF videodisplaycontrol:: setvideowindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) -Methode.</span><span class="sxs-lookup"><span data-stu-id="4ea41-473">The standard presenter implements the [**IMFVideoDisplayControl::SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) method for this purpose.</span></span> <span data-ttu-id="4ea41-474">Sie müssen das Gerät erstellen, wenn der Presenter erstmalig erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="4ea41-474">You must create the device when the presenter is first created.</span></span> <span data-ttu-id="4ea41-475">Normalerweise kennen Sie nicht alle Geräteparameter zu diesem Zeitpunkt, z. b. das Fenster oder das Hintergrund Puffer Format.</span><span class="sxs-lookup"><span data-stu-id="4ea41-475">Typically, you won't know all of the device parameters at this time, such as the window or the back buffer format.</span></span> <span data-ttu-id="4ea41-476">Sie können ein temporäres Gerät erstellen und es später&ersetzen \# . denken Sie daran, dass Sie [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) für den Geräte-Manager aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-476">You can create a temporary device and replace it later&\#;just remember to call [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) on the device manager.</span></span>

<span data-ttu-id="4ea41-477">Wenn Sie ein neues Gerät erstellen oder **IDirect3DDevice9:: Reset** oder **IDirect3DDevice9Ex:: reltex** auf einem vorhandenen Gerät aufzurufen, senden Sie ein [**EC_DISPLAY_CHANGED**](../directshow/ec-display-changed.md) Ereignis an den EVR.</span><span class="sxs-lookup"><span data-stu-id="4ea41-477">If you create a new device, or if you call **IDirect3DDevice9::Reset** or **IDirect3DDevice9Ex::ResetEx** on an existing device, send an [**EC_DISPLAY_CHANGED**](../directshow/ec-display-changed.md) event to the EVR.</span></span> <span data-ttu-id="4ea41-478">Dieses Ereignis benachrichtigt den EVR, dass er den Medientyp erneut aushandeln soll.</span><span class="sxs-lookup"><span data-stu-id="4ea41-478">This event notifies the EVR to renegotiate the media type.</span></span> <span data-ttu-id="4ea41-479">Der EVR ignoriert die Ereignis Parameter für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="4ea41-479">The EVR ignores the event parameters for this event.</span></span>

### <a name="allocating-direct3d-surfaces"></a><span data-ttu-id="4ea41-480">Zuordnen von Direct3D-Flächen</span><span class="sxs-lookup"><span data-stu-id="4ea41-480">Allocating Direct3D Surfaces</span></span>

<span data-ttu-id="4ea41-481">Nachdem der Presenter den Medientyp festgelegt hat, kann er die Direct3D-Oberflächen zuordnen, die der Mixer zum Schreiben der Video Frames verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ea41-481">After the presenter sets the media type, it can allocate the Direct3D surfaces, which the mixer will use to write the video frames.</span></span> <span data-ttu-id="4ea41-482">Die Oberfläche muss dem Medientyp des Presenter entsprechen:</span><span class="sxs-lookup"><span data-stu-id="4ea41-482">The surface must match the presenter's media type:</span></span>

-   <span data-ttu-id="4ea41-483">Das Oberflächen Format muss mit dem Medien Untertyp identisch sein.</span><span class="sxs-lookup"><span data-stu-id="4ea41-483">The surface format must match the media subtype.</span></span> <span data-ttu-id="4ea41-484">Wenn der Untertyp z. b. **MFVideoFormat_RGB24** ist, muss das Oberflächen Format **D3DFMT_X8R8G8B8** sein.</span><span class="sxs-lookup"><span data-stu-id="4ea41-484">For example, if the subtype is **MFVideoFormat_RGB24**, the surface format must be **D3DFMT_X8R8G8B8**.</span></span> <span data-ttu-id="4ea41-485">Weitere Informationen zu Untertypen und Direct3D-Formaten finden Sie unter [Video Untertyp-GUIDs](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="4ea41-485">For more information about subtypes and Direct3D formats, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>
-   <span data-ttu-id="4ea41-486">Die Breite und Höhe der Oberfläche muss den Dimensionen entsprechen, die im [**MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) -Attribut des Medientyps angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="4ea41-486">The surface width and height must match the dimensions given in the [**MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) attribute of the media type.</span></span>

<span data-ttu-id="4ea41-487">Die empfohlene Vorgehensweise zum Zuordnen von Oberflächen hängt davon ab, ob der Presenter im Fenster oder voll Bildschirm ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4ea41-487">The recommended way to allocate surfaces depends on whether the presenter runs windowed or full-screen.</span></span>

<span data-ttu-id="4ea41-488">Wenn das Direct3D-Gerät in einem Fenster angezeigt wird, können Sie mehrere Austausch Ketten erstellen, die jeweils über einen einzelnen Hintergrund Puffer verfügen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-488">If the Direct3D device is windowed, you can create several swap chains, each with a single back buffer.</span></span> <span data-ttu-id="4ea41-489">Bei diesem Ansatz können Sie jede Oberfläche unabhängig präsentieren, da die Darstellung einer Swapkette nicht die anderen Swapketten beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="4ea41-489">Using this approach, you can present each surface independently, because presenting one swap chain will not interfere with the other swap chains.</span></span> <span data-ttu-id="4ea41-490">Der Mixer kann Daten auf eine Oberfläche schreiben, während eine andere Oberfläche für die Präsentation geplant ist.</span><span class="sxs-lookup"><span data-stu-id="4ea41-490">The mixer can write data to a surface while another surface is scheduled for presentation.</span></span>

<span data-ttu-id="4ea41-491">Entscheiden Sie zuerst, wie viele Austausch Ketten erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-491">First, decide how many swap chains to create.</span></span> <span data-ttu-id="4ea41-492">Mindestens drei wird empfohlen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-492">A minimum of three is recommended.</span></span> <span data-ttu-id="4ea41-493">Gehen Sie für jede Austausch Kette wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="4ea41-493">For each swap chain, do the following:</span></span>

1.  <span data-ttu-id="4ea41-494">Rufen Sie **IDirect3DDevice9:: kreateadditionalswapchain** auf, um die Austausch Kette zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-494">Call **IDirect3DDevice9::CreateAdditionalSwapChain** to create the swap chain.</span></span>
2.  <span data-ttu-id="4ea41-495">Aufrufen von **IDirect3DSwapChain9:: GetBackBuffer** zum Abrufen eines Zeigers auf die Hintergrund Puffer Oberfläche der Austausch Kette.</span><span class="sxs-lookup"><span data-stu-id="4ea41-495">Call **IDirect3DSwapChain9::GetBackBuffer** to get a pointer to the swap chain's back buffer surface.</span></span>
3.  <span data-ttu-id="4ea41-496">Aufrufen von [**mfcreatevideosamplefromsurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) und übergeben eines Zeigers auf die-Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="4ea41-496">Call [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) and pass in a pointer to the surface.</span></span> <span data-ttu-id="4ea41-497">Diese Funktion gibt einen Zeiger auf ein Video Sample-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="4ea41-497">This function returns a pointer to a video sample object.</span></span> <span data-ttu-id="4ea41-498">Das Video Sample-Objekt implementiert die [**imfsample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) -Schnittstelle, und der Presenter verwendet diese Schnittstelle, um die Oberfläche an den Mixer zu übermitteln, wenn der Presenter die [**imftransform::P rocess Output**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) -Methode des Mischers aufruft.</span><span class="sxs-lookup"><span data-stu-id="4ea41-498">The video sample object implements the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, and the presenter uses this interface to deliver the surface to the mixer when the presenter calls the mixer's [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) method.</span></span> <span data-ttu-id="4ea41-499">Weitere Informationen zum Video Sample-Objekt finden Sie unter [Video Samples (Videobeispiele](video-samples.md)).</span><span class="sxs-lookup"><span data-stu-id="4ea41-499">For more information about the video sample object, see [Video Samples](video-samples.md).</span></span>
4.  <span data-ttu-id="4ea41-500">Speichert den [**IMF Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) -Zeiger in einer Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="4ea41-500">Store the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) pointer in a queue.</span></span> <span data-ttu-id="4ea41-501">Der Presenter Ruft bei der Verarbeitung Beispiele aus dieser Warteschlange ab, wie in [Verarbeiten der Ausgabe](#processing-output)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4ea41-501">The presenter will pull samples from this queue during processing as described in [Processing Output](#processing-output).</span></span>
5.  <span data-ttu-id="4ea41-502">Bewahren Sie einen Verweis auf den **IDirect3DSwapChain9** -Zeiger auf, damit die SwapChain nicht freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4ea41-502">Keep a reference to the **IDirect3DSwapChain9** pointer so the swap chain is not released.</span></span>

<span data-ttu-id="4ea41-503">Im Vollbildmodus (exklusiv) kann das Gerät nicht mehr als eine SwapChain aufweisen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-503">In full-screen exclusive mode, the device cannot have more than one swap chain.</span></span> <span data-ttu-id="4ea41-504">Diese austauschkette wird implizit erstellt, wenn Sie das voll Bild Gerät erstellen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-504">This swap chain is created implicitly when you create the full-screen device.</span></span> <span data-ttu-id="4ea41-505">Die SwapChain kann über mehr als einen Hintergrund Puffer verfügen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-505">The swap chain can have more than one back buffer.</span></span> <span data-ttu-id="4ea41-506">Wenn Sie jedoch einen backpuffer darstellen, während Sie in einen anderen Hintergrund Puffer in derselben Swapkette schreiben, gibt es keine einfache Möglichkeit, die beiden Vorgänge zu koordinieren.</span><span class="sxs-lookup"><span data-stu-id="4ea41-506">Unfortunately, however, if you present one back buffer while you write to another back buffer in the same swap chain, there is no easy way to coordinate the two operations.</span></span> <span data-ttu-id="4ea41-507">Dies liegt an der Art und Weise, in der Direct3D das Oberflächen Flipping implementiert.</span><span class="sxs-lookup"><span data-stu-id="4ea41-507">This is because of the way Direct3D implements surface flipping.</span></span> <span data-ttu-id="4ea41-508">Wenn Sie "Present" aufgerufen haben, aktualisiert der Grafiktreiber die Surface-Zeiger im Grafikspeicher.</span><span class="sxs-lookup"><span data-stu-id="4ea41-508">When you call Present, the graphics driver updates the surface pointers in graphics memory.</span></span> <span data-ttu-id="4ea41-509">Wenn Sie **IDirect3DSurface9** -Zeiger mit dem Befehl " **Present**" speichern, zeigen Sie auf verschiedene Puffer, nachdem der **aktuelle** Rückruf zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="4ea41-509">If you are holding any **IDirect3DSurface9** pointers when you call **Present**, they will point to different buffers after the **Present** call returns.</span></span>

<span data-ttu-id="4ea41-510">Die einfachste Möglichkeit besteht darin, ein Video Beispiel für die Swapkette zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-510">The simplest option is to create one video sample for the swap chain.</span></span> <span data-ttu-id="4ea41-511">Wenn Sie diese Option auswählen, führen Sie dieselben Schritte aus, die für den Fenstermodus ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4ea41-511">If you choose this option, follow the same steps given for windowed mode.</span></span> <span data-ttu-id="4ea41-512">Der einzige Unterschied besteht darin, dass die Beispiel Warteschlange ein einzelnes Video Beispiel enthält.</span><span class="sxs-lookup"><span data-stu-id="4ea41-512">The only difference is that the sample queue contains a single video sample.</span></span> <span data-ttu-id="4ea41-513">Eine andere Möglichkeit besteht darin, Offscreen-Oberflächen zu erstellen und Sie dann in den Hintergrund Puffer zu versetzen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-513">Another option is to create offscreen surfaces and then blit them to the back buffer.</span></span> <span data-ttu-id="4ea41-514">Die von Ihnen erstellten Oberflächen müssen die [**idirectxvideoprocessor:: videoprocessblt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) -Methode unterstützen, die der Mixer zum Zusammenführen der Ausgabe Frames verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ea41-514">The surfaces that you create must support the [**IDirectXVideoProcessor::VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) method, which the mixer uses to composite the output frames.</span></span>

### <a name="tracking-samples"></a><span data-ttu-id="4ea41-515">Überwachungsbeispiele</span><span class="sxs-lookup"><span data-stu-id="4ea41-515">Tracking Samples</span></span>

<span data-ttu-id="4ea41-516">Wenn der Presenter die Videobeispiele zuerst ordnet, werden diese in einer Warteschlange platziert.</span><span class="sxs-lookup"><span data-stu-id="4ea41-516">When the presenter first allocates the video samples, it places them in a queue.</span></span> <span data-ttu-id="4ea41-517">Der Presenter zeichnet sich aus dieser Warteschlange aus, wenn er einen neuen Frame vom Mixer erhalten muss.</span><span class="sxs-lookup"><span data-stu-id="4ea41-517">The presenter draws from this queue whenever it needs to get a new frame from the mixer.</span></span> <span data-ttu-id="4ea41-518">Nachdem der Mixer den Frame ausgegeben hat, verschiebt der Presenter das Beispiel in eine zweite Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="4ea41-518">After the mixer outputs the frame, the presenter moves the sample into a second queue.</span></span> <span data-ttu-id="4ea41-519">Die zweite Warteschlange ist für Beispiele, die auf Ihre geplanten Präsentations Zeiten warten.</span><span class="sxs-lookup"><span data-stu-id="4ea41-519">The second queue is for samples that are waiting for their scheduled presentation times.</span></span>

<span data-ttu-id="4ea41-520">Um die Nachverfolgung des Status der einzelnen Beispiele zu vereinfachen, implementiert das Video Sample-Objekt die [**imftrackedsample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="4ea41-520">To make it easier to track the status of each sample, the video sample object implements the [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) interface.</span></span> <span data-ttu-id="4ea41-521">Sie können diese Schnittstelle wie folgt verwenden:</span><span class="sxs-lookup"><span data-stu-id="4ea41-521">You can use this interface as follows:</span></span>

1.  <span data-ttu-id="4ea41-522">Implementieren Sie die [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) -Schnittstelle in Ihrem Presenter.</span><span class="sxs-lookup"><span data-stu-id="4ea41-522">Implement the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface in your presenter.</span></span>
2.  <span data-ttu-id="4ea41-523">Bevor Sie ein Beispiel in der geplanten Warteschlange platzieren, Fragen Sie das Video Sample-Objekt für die [**IMF trackedsample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="4ea41-523">Before you place a sample in the scheduled queue, query the video sample object for the [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) interface.</span></span>

3.  <span data-ttu-id="4ea41-524">Rufen Sie [**imftrackedsample:: abtallocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) mit einem Zeiger auf Ihre Rückruf Schnittstelle auf.</span><span class="sxs-lookup"><span data-stu-id="4ea41-524">Call [**IMFTrackedSample::SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) with a pointer to your callback interface.</span></span>
4.  <span data-ttu-id="4ea41-525">Wenn das Beispiel zur Präsentation bereit ist, entfernen Sie es aus der geplanten Warteschlange, stellen Sie es bereit, und geben Sie alle Verweise auf das Beispiel frei.</span><span class="sxs-lookup"><span data-stu-id="4ea41-525">When the sample is ready for presentation, remove it from the scheduled queue, present it, and release all references to the sample.</span></span>
5.  <span data-ttu-id="4ea41-526">Das Beispiel ruft den Rückruf auf.</span><span class="sxs-lookup"><span data-stu-id="4ea41-526">The sample invokes the callback.</span></span> <span data-ttu-id="4ea41-527">(Das Sample-Objekt wird in diesem Fall nicht gelöscht, da es einen Verweis Zähler auf sich selbst enthält, bis der Rückruf aufgerufen wird.)</span><span class="sxs-lookup"><span data-stu-id="4ea41-527">(The sample object is not deleted in this case because it holds a reference count on itself until the callback is invoked.)</span></span>
6.  <span data-ttu-id="4ea41-528">Geben Sie im Rückruf das Beispiel in die verfügbare Warteschlange ein.</span><span class="sxs-lookup"><span data-stu-id="4ea41-528">Inside the callback, return the sample to the available queue.</span></span>

<span data-ttu-id="4ea41-529">Zum Nachverfolgen von Beispielen ist kein Presenter erforderlich, um [**imftrackedsample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) zu verwenden. Sie können jede Technik implementieren, die für Ihren Entwurf am besten geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="4ea41-529">A presenter is not required to use [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) to track samples; you can implement any technique that works best for your design.</span></span> <span data-ttu-id="4ea41-530">Ein Vorteil von **imftrackedsample** besteht darin, dass Sie die Planungs-und Renderingfunktionen von Presenter in Hilfsobjekte verschieben können. diese Objekte benötigen keinen besonderen Mechanismus zum Rückrufe an den Presenter, wenn Sie Videobeispiele veröffentlichen, da das Beispiel Objekt diesen Mechanismus bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="4ea41-530">One advantage of **IMFTrackedSample** is that you can move the presenter's scheduling and rendering functions into helper objects, and these objects do not need any special mechanism for calling back to the presenter when they release video samples because the sample object provides that mechanism.</span></span>

<span data-ttu-id="4ea41-531">Der folgende Code zeigt, wie der Rückruf festgelegt wird:</span><span class="sxs-lookup"><span data-stu-id="4ea41-531">The following code shows how to set the callback:</span></span>


```C++
HRESULT EVRCustomPresenter::TrackSample(IMFSample *pSample)
{
    IMFTrackedSample *pTracked = NULL;

    HRESULT hr = pSample->QueryInterface(IID_PPV_ARGS(&pTracked));

    if (SUCCEEDED(hr))
    {
        hr = pTracked->SetAllocator(&m_SampleFreeCB, NULL);
    }

    SafeRelease(&pTracked);
    return hr;
}
```



<span data-ttu-id="4ea41-532">Rufen Sie im Rückruf [**imfasynkresult:: GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject) für das asynchrone Ergebnis Objekt auf, um einen Zeiger auf das Beispiel abzurufen:</span><span class="sxs-lookup"><span data-stu-id="4ea41-532">In the callback, call [**IMFAsyncResult::GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject) on the asynchronous result object to retrieve a pointer to the sample:</span></span>


```C++
HRESULT EVRCustomPresenter::OnSampleFree(IMFAsyncResult *pResult)
{
    IUnknown *pObject = NULL;
    IMFSample *pSample = NULL;
    IUnknown *pUnk = NULL;

    // Get the sample from the async result object.
    HRESULT hr = pResult->GetObject(&pObject);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pObject->QueryInterface(IID_PPV_ARGS(&pSample));
    if (FAILED(hr))
    {
        goto done;
    }

    // If this sample was submitted for a frame-step, the frame step operation
    // is complete.

    if (m_FrameStep.state == FRAMESTEP_SCHEDULED)
    {
        // Query the sample for IUnknown and compare it to our cached value.
        hr = pSample->QueryInterface(IID_PPV_ARGS(&pUnk));
        if (FAILED(hr))
        {
            goto done;
        }

        if (m_FrameStep.pSampleNoRef == (DWORD_PTR)pUnk)
        {
            // Notify the EVR.
            hr = CompleteFrameStep(pSample);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        // Note: Although pObject is also an IUnknown pointer, it is not
        // guaranteed to be the exact pointer value returned through
        // QueryInterface. Therefore, the second QueryInterface call is
        // required.
    }

    /*** Begin lock **_/

    EnterCriticalSection(&m_ObjectLock);

    UINT32 token = MFGetAttributeUINT32(
        pSample, MFSamplePresenter_SampleCounter, (UINT32)-1);

    if (token == m_TokenCounter)
    {
        // Return the sample to the sample pool.
        hr = m_SamplePool.ReturnSample(pSample);
        if (SUCCEEDED(hr))
        {
            // A free sample is available. Process more data if possible.
            (void)ProcessOutputLoop();
        }
    }

    LeaveCriticalSection(&m_ObjectLock);

    /_*_ End lock _*_/

done:
    if (FAILED(hr))
    {
        NotifyEvent(EC_ERRORABORT, hr, 0);
    }
    SafeRelease(&pObject);
    SafeRelease(&pSample);
    SafeRelease(&pUnk);
    return hr;
}
```



## <a name="processing-output"></a><span data-ttu-id="4ea41-533">Ausgabe wird verarbeitet</span><span class="sxs-lookup"><span data-stu-id="4ea41-533">Processing Output</span></span>

<span data-ttu-id="4ea41-534">Immer wenn der Mixer ein neues Eingabe Beispiel empfängt, sendet der EVR eine _ \*MFVP_MESSAGE_PROCESSINPUTNOTIFY\*\*-Meldung an den Presenter.</span><span class="sxs-lookup"><span data-stu-id="4ea41-534">Whenever the mixer receives a new input sample, the EVR sends an _ *MFVP_MESSAGE_PROCESSINPUTNOTIFY*\* message to the presenter.</span></span> <span data-ttu-id="4ea41-535">Diese Meldung gibt an, dass der Mixer möglicherweise über einen neuen Videorahmen verfügt.</span><span class="sxs-lookup"><span data-stu-id="4ea41-535">This message indicates that the mixer might have a new video frame to deliver.</span></span> <span data-ttu-id="4ea41-536">Als Antwort ruft der Presenter [**IMF Transform::P rocess Output**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) auf dem Mixer auf.</span><span class="sxs-lookup"><span data-stu-id="4ea41-536">In response, the presenter calls [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) on the mixer.</span></span> <span data-ttu-id="4ea41-537">Wenn die Methode erfolgreich ist, plant der Presenter das Beispiel für die Präsentation.</span><span class="sxs-lookup"><span data-stu-id="4ea41-537">If the method succeeds, the presenter schedules the sample for presentation.</span></span>

<span data-ttu-id="4ea41-538">Um die Ausgabe vom Mixer zu erhalten, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="4ea41-538">To get output from the mixer, perform the following steps:</span></span>

1.  <span data-ttu-id="4ea41-539">Überprüfen Sie den Uhrzustand.</span><span class="sxs-lookup"><span data-stu-id="4ea41-539">Check the clock state.</span></span> <span data-ttu-id="4ea41-540">Wenn die Uhr angehalten ist, ignorieren Sie die **MFVP_MESSAGE_PROCESSINPUTNOTIFY** Meldung, es sei denn, dies ist der erste Videoframe.</span><span class="sxs-lookup"><span data-stu-id="4ea41-540">If the clock is paused, ignore the **MFVP_MESSAGE_PROCESSINPUTNOTIFY** message unless this is the first video frame.</span></span> <span data-ttu-id="4ea41-541">Wenn die Uhr ausgeführt wird, oder wenn es sich um den ersten Videoframe handelt, fahren Sie fort.</span><span class="sxs-lookup"><span data-stu-id="4ea41-541">If the clock is running, or if this is the first video frame, continue.</span></span>
2.  <span data-ttu-id="4ea41-542">Holen Sie sich ein Beispiel aus der Warteschlange mit verfügbaren Beispielen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-542">Get a sample from the queue of available samples.</span></span> <span data-ttu-id="4ea41-543">Wenn die Warteschlange leer ist, bedeutet dies, dass alle zugeordneten Beispiele aktuell für die Darstellung geplant sind.</span><span class="sxs-lookup"><span data-stu-id="4ea41-543">If the queue is empty, it means that all allocated samples are currently scheduled for presenting.</span></span> <span data-ttu-id="4ea41-544">Ignorieren Sie in diesem Fall die **MFVP_MESSAGE_PROCESSINPUTNOTIFY** Meldung zu diesem Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="4ea41-544">In that case, ignore the **MFVP_MESSAGE_PROCESSINPUTNOTIFY** message at this time.</span></span> <span data-ttu-id="4ea41-545">Wenn das nächste Beispiel verfügbar wird, wiederholen Sie die hier aufgeführten Schritte.</span><span class="sxs-lookup"><span data-stu-id="4ea41-545">When the next sample becomes available, repeat the steps listed here.</span></span>
3.  <span data-ttu-id="4ea41-546">(Optional) Wenn die Uhr verfügbar ist, rufen Sie die aktuelle Uhrzeit (*T1*) ab, indem Sie [**imfclock:: getcorrelatedtime**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-546">(Optional.) If the clock is available, get the current clock time (*T1*) by calling [**IMFClock::GetCorrelatedTime**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime).</span></span>
4.  <span data-ttu-id="4ea41-547">Rückrufe [**imftransform::P rocess Output**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) auf dem Mixer.</span><span class="sxs-lookup"><span data-stu-id="4ea41-547">Call [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) on the mixer.</span></span> <span data-ttu-id="4ea41-548">Wenn **ProcessOutput** erfolgreich ist, enthält das Beispiel einen Videoframe.</span><span class="sxs-lookup"><span data-stu-id="4ea41-548">If **ProcessOutput** succeeds, the sample contains a video frame.</span></span> <span data-ttu-id="4ea41-549">Wenn die Methode fehlschlägt, überprüfen Sie den Rückgabecode.</span><span class="sxs-lookup"><span data-stu-id="4ea41-549">If the method fails, check the return code.</span></span> <span data-ttu-id="4ea41-550">Die folgenden Fehlercodes aus **ProcessOutput** sind keine kritischen Fehler:</span><span class="sxs-lookup"><span data-stu-id="4ea41-550">The following error codes from **ProcessOutput** are not critical failures:</span></span>

    

    | <span data-ttu-id="4ea41-551">Fehlercode</span><span class="sxs-lookup"><span data-stu-id="4ea41-551">Error code</span></span>                              | <span data-ttu-id="4ea41-552">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4ea41-552">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                    |
    |-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="4ea41-553">**MF_E_TRANSFORM_NEED_MORE_INPUT**</span><span class="sxs-lookup"><span data-stu-id="4ea41-553">**MF_E_TRANSFORM_NEED_MORE_INPUT**</span></span> | <span data-ttu-id="4ea41-554">Der Mixer benötigt mehr Eingaben, bevor er einen neuen Ausgabe Frame erzeugt.</span><span class="sxs-lookup"><span data-stu-id="4ea41-554">The mixer needs more input before it can produce a new output frame.</span></span><br/> <span data-ttu-id="4ea41-555">Wenn Sie diesen Fehlercode erhalten, überprüfen Sie, ob der EVR das Ende des Streams erreicht hat, und reagieren Sie entsprechend der Beschreibung am [Ende des Streams](#end-of-stream).</span><span class="sxs-lookup"><span data-stu-id="4ea41-555">If you get this error code, check whether the EVR has reached the end of the stream and respond accordingly, as described in [End of Stream](#end-of-stream).</span></span> <span data-ttu-id="4ea41-556">Andernfalls ignorieren Sie diese **MF_E_TRANSFORM_NEED_MORE_INPUT** Meldung.</span><span class="sxs-lookup"><span data-stu-id="4ea41-556">Otherwise, ignore this **MF_E_TRANSFORM_NEED_MORE_INPUT** message.</span></span> <span data-ttu-id="4ea41-557">Der EVR sendet einen weiteren, wenn der Mixer mehr Eingaben erhält.</span><span class="sxs-lookup"><span data-stu-id="4ea41-557">The EVR will send another one when the mixer gets more input.</span></span><br/> |
    | <span data-ttu-id="4ea41-558">**MF_E_TRANSFORM_STREAM_CHANGE**</span><span class="sxs-lookup"><span data-stu-id="4ea41-558">**MF_E_TRANSFORM_STREAM_CHANGE**</span></span>    | <span data-ttu-id="4ea41-559">Der Ausgabetyp des Mischers wurde ungültig, möglicherweise aufgrund einer upstreamänderung im Format.</span><span class="sxs-lookup"><span data-stu-id="4ea41-559">The mixer's output type has become invalid, possibly due to a format change upstream.</span></span><br/> <span data-ttu-id="4ea41-560">Wenn Sie diesen Fehlercode erhalten, legen Sie den Medientyp des Presenter auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="4ea41-560">If you get this error code, set the presenter's media type to **NULL**.</span></span> <span data-ttu-id="4ea41-561">Der EVR fordert ein neues Format an.</span><span class="sxs-lookup"><span data-stu-id="4ea41-561">The EVR will request a new format.</span></span><br/>                                                                                                                                                                         |
    | <span data-ttu-id="4ea41-562">**MF_E_TRANSFORM_TYPE_NOT_SET**</span><span class="sxs-lookup"><span data-stu-id="4ea41-562">**MF_E_TRANSFORM_TYPE_NOT_SET**</span></span>    | <span data-ttu-id="4ea41-563">Für den Mixer ist ein neuer Medientyp erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4ea41-563">The mixer requires a new media type.</span></span><br/> <span data-ttu-id="4ea41-564">Wenn Sie diesen Fehlercode erhalten, wiederholen Sie den Ausgabetyp des Mischers, wie in den [Aushandeln von Formaten](#negotiating-formats)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4ea41-564">If you get this error code, renegotiate the mixer's output type as described in [Negotiating Formats](#negotiating-formats).</span></span><br/>                                                                                                                                                                                                        |

    

     

    <span data-ttu-id="4ea41-565">Wenn [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) erfolgreich ist, fahren Sie fort.</span><span class="sxs-lookup"><span data-stu-id="4ea41-565">If [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) succeeds, continue.</span></span>

5.  <span data-ttu-id="4ea41-566">(Optional) Wenn die Uhr verfügbar ist, erhalten Sie die aktuelle Uhrzeit (*T2*).</span><span class="sxs-lookup"><span data-stu-id="4ea41-566">(Optional.) If the clock is available, get the current clock time (*T2*).</span></span> <span data-ttu-id="4ea41-567">Die vom Mixer eingeführte Latenzzeit ist (*T2*  -  *T1*).</span><span class="sxs-lookup"><span data-stu-id="4ea41-567">The amount of latency introduced by the mixer is (*T2* - *T1*).</span></span> <span data-ttu-id="4ea41-568">Senden Sie ein **EC_PROCESSING_LATENCY** Ereignis mit diesem Wert an den EVR.</span><span class="sxs-lookup"><span data-stu-id="4ea41-568">Send an **EC_PROCESSING_LATENCY** event with this value to the EVR.</span></span> <span data-ttu-id="4ea41-569">Der EVR verwendet diesen Wert für die Qualitätskontrolle.</span><span class="sxs-lookup"><span data-stu-id="4ea41-569">The EVR uses this value for quality control.</span></span> <span data-ttu-id="4ea41-570">Wenn keine Uhr verfügbar ist, gibt es keinen Grund, das **EC_PROCESSING_LATENCY** Ereignis zu senden.</span><span class="sxs-lookup"><span data-stu-id="4ea41-570">If no clock is available, there is no reason to send the **EC_PROCESSING_LATENCY** event.</span></span>
6.  <span data-ttu-id="4ea41-571">(Optional) Fragen Sie das Beispiel nach [**imftrackedsample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) ab, und nennen Sie [**imftrackedsample::**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) Set Sample, wie in nach [Verfolgungs Beispielen](#tracking-samples)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4ea41-571">(Optional.) Query the sample for [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) and call [**IMFTrackedSample::SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) as described in [Tracking Samples](#tracking-samples).</span></span>
7.  <span data-ttu-id="4ea41-572">Planen Sie das Beispiel für die Präsentation.</span><span class="sxs-lookup"><span data-stu-id="4ea41-572">Schedule the sample for presentation.</span></span>

<span data-ttu-id="4ea41-573">Diese Schritt Sequenz kann beendet werden, bevor der Presenter eine Ausgabe vom Mixer erhält.</span><span class="sxs-lookup"><span data-stu-id="4ea41-573">This sequence of steps can terminate before the presenter gets any output from the mixer.</span></span> <span data-ttu-id="4ea41-574">Um sicherzustellen, dass keine Anforderungen gelöscht werden, sollten Sie die gleichen Schritte wiederholen, wenn Folgendes geschieht:</span><span class="sxs-lookup"><span data-stu-id="4ea41-574">To ensure that no requests are dropped, you should repeat the same steps when the following occur:</span></span>

-   <span data-ttu-id="4ea41-575">Die [**imfclockstaatink:: onclockstart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) -Methode oder die **imfclockstaatink:: onclockstart** -Methode des Presenter wird aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-575">The presenter's [**IMFClockStateSink::OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) or **IMFClockStateSink::OnClockStart** method is called.</span></span> <span data-ttu-id="4ea41-576">Dies behandelt die Groß-/Kleinschreibung, in der der Mixer Eingaben ignoriert, da die Uhr angehalten wird (Schritt 1).</span><span class="sxs-lookup"><span data-stu-id="4ea41-576">This handles the case where the mixer ignores input because the clock is paused (step 1).</span></span>
-   <span data-ttu-id="4ea41-577">Der [**imftrackedsample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) -Rückruf wird aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-577">The [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) callback is invoked.</span></span> <span data-ttu-id="4ea41-578">Dies behandelt den Fall, in dem der Mixer Eingaben empfängt, aber alle Videobeispiele des Presenter verwendet werden (Schritt 2).</span><span class="sxs-lookup"><span data-stu-id="4ea41-578">This handles the case where the mixer receives input but all of the presenter's video samples are in use (step 2).</span></span>

<span data-ttu-id="4ea41-579">Die folgenden Codebeispiele zeigen diese Schritte ausführlicher.</span><span class="sxs-lookup"><span data-stu-id="4ea41-579">The next several code examples show these steps in more detail.</span></span> <span data-ttu-id="4ea41-580">Der Presenter Ruft die- `ProcessInputNotify` Methode auf (wie im folgenden Beispiel gezeigt), wenn die **MFVP_MESSAGE_PROCESSINPUTNOTIFY** Nachricht abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="4ea41-580">The presenter calls the `ProcessInputNotify` method (shown in the following example) when it gets the **MFVP_MESSAGE_PROCESSINPUTNOTIFY** message.</span></span>


```C++
//-----------------------------------------------------------------------------
// ProcessInputNotify
//
// Attempts to get a new output sample from the mixer.
//
// This method is called when the EVR sends an MFVP_MESSAGE_PROCESSINPUTNOTIFY
// message, which indicates that the mixer has a new input sample.
//
// Note: If there are multiple input streams, the mixer might not deliver an
// output sample for every input sample.
//-----------------------------------------------------------------------------

HRESULT EVRCustomPresenter::ProcessInputNotify()
{
    HRESULT hr = S_OK;

    // Set the flag that says the mixer has a new sample.
    m_bSampleNotify = TRUE;

    if (m_pMediaType == NULL)
    {
        // We don't have a valid media type yet.
        hr = MF_E_TRANSFORM_TYPE_NOT_SET;
    }
    else
    {
        // Try to process an output sample.
        ProcessOutputLoop();
    }
    return hr;
}
```



<span data-ttu-id="4ea41-581">Diese `ProcessInputNotify` Methode legt ein boolesches Flag fest, um die Tatsache aufzuzeichnen, dass der Mixer über neue Eingaben verfügt.</span><span class="sxs-lookup"><span data-stu-id="4ea41-581">This `ProcessInputNotify` method sets a Boolean flag to record the fact that the mixer has new input.</span></span> <span data-ttu-id="4ea41-582">Anschließend wird die- `ProcessOutputLoop` Methode aufgerufen, wie im nächsten Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="4ea41-582">Then it calls the `ProcessOutputLoop` method, shown in the next example.</span></span> <span data-ttu-id="4ea41-583">Diese Methode versucht, so viele Beispiele wie möglich vom Mixer abzurufen:</span><span class="sxs-lookup"><span data-stu-id="4ea41-583">This method attempts to pull as many samples as possible from the mixer:</span></span>


```C++
void EVRCustomPresenter::ProcessOutputLoop()
{
    HRESULT hr = S_OK;

    // Process as many samples as possible.
    while (hr == S_OK)
    {
        // If the mixer doesn't have a new input sample, break from the loop.
        if (!m_bSampleNotify)
        {
            hr = MF_E_TRANSFORM_NEED_MORE_INPUT;
            break;
        }

        // Try to process a sample.
        hr = ProcessOutput();

        // NOTE: ProcessOutput can return S_FALSE to indicate it did not
        // process a sample. If so, break out of the loop.
    }

    if (hr == MF_E_TRANSFORM_NEED_MORE_INPUT)
    {
        // The mixer has run out of input data. Check for end-of-stream.
        CheckEndOfStream();
    }
}
```



<span data-ttu-id="4ea41-584">Die `ProcessOutput` im nächsten Beispiel gezeigte-Methode versucht, einen einzelnen Videoframe aus dem Mixer zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4ea41-584">The `ProcessOutput` method, shown in the next example, attempts to get a single video frame from the mixer.</span></span> <span data-ttu-id="4ea41-585">Wenn kein Videoframe verfügbar ist, `ProcessSample` gibt S_FALSE oder einen Fehlercode zurück, von dem beide die Schleife unterbrechen `ProcessOutputLoop` .</span><span class="sxs-lookup"><span data-stu-id="4ea41-585">If no video frame is available, `ProcessSample` returns S_FALSE or an error code, either of which interrupts the loop in `ProcessOutputLoop`.</span></span> <span data-ttu-id="4ea41-586">Die meisten Aufgaben werden innerhalb der-Methode durchgeführt `ProcessOutput` :</span><span class="sxs-lookup"><span data-stu-id="4ea41-586">Most of the work is done inside the `ProcessOutput` method:</span></span>


```C++
//-----------------------------------------------------------------------------
// ProcessOutput
//
// Attempts to get a new output sample from the mixer.
//
// Called in two situations:
// (1) ProcessOutputLoop, if the mixer has a new input sample.
// (2) Repainting the last frame.
//-----------------------------------------------------------------------------

HRESULT EVRCustomPresenter::ProcessOutput()
{
    assert(m_bSampleNotify || m_bRepaint);  // See note above.

    HRESULT     hr = S_OK;
    DWORD       dwStatus = 0;
    LONGLONG    mixerStartTime = 0, mixerEndTime = 0;
    MFTIME      systemTime = 0;
    BOOL        bRepaint = m_bRepaint; // Temporarily store this state flag.

    MFT_OUTPUT_DATA_BUFFER dataBuffer;
    ZeroMemory(&dataBuffer, sizeof(dataBuffer));

    IMFSample *pSample = NULL;

    // If the clock is not running, we present the first sample,
    // and then don't present any more until the clock starts.

    if ((m_RenderState != RENDER_STATE_STARTED) &&  // Not running.
         !m_bRepaint &&             // Not a repaint request.
         m_bPrerolled               // At least one sample has been presented.
         )
    {
        return S_FALSE;
    }

    // Make sure we have a pointer to the mixer.
    if (m_pMixer == NULL)
    {
        return MF_E_INVALIDREQUEST;
    }

    // Try to get a free sample from the video sample pool.
    hr = m_SamplePool.GetSample(&pSample);
    if (hr == MF_E_SAMPLEALLOCATOR_EMPTY)
    {
        // No free samples. Try again when a sample is released.
        return S_FALSE;
    }
    else if (FAILED(hr))
    {
        return hr;
    }

    // From now on, we have a valid video sample pointer, where the mixer will
    // write the video data.
    assert(pSample != NULL);

    // (If the following assertion fires, it means we are not managing the sample pool correctly.)
    assert(MFGetAttributeUINT32(pSample, MFSamplePresenter_SampleCounter, (UINT32)-1) == m_TokenCounter);

    if (m_bRepaint)
    {
        // Repaint request. Ask the mixer for the most recent sample.
        SetDesiredSampleTime(
            pSample,
            m_scheduler.LastSampleTime(),
            m_scheduler.FrameDuration()
            );

        m_bRepaint = FALSE; // OK to clear this flag now.
    }
    else
    {
        // Not a repaint request. Clear the desired sample time; the mixer will
        // give us the next frame in the stream.
        ClearDesiredSampleTime(pSample);

        if (m_pClock)
        {
            // Latency: Record the starting time for ProcessOutput.
            (void)m_pClock->GetCorrelatedTime(0, &mixerStartTime, &systemTime);
        }
    }

    // Now we are ready to get an output sample from the mixer.
    dataBuffer.dwStreamID = 0;
    dataBuffer.pSample = pSample;
    dataBuffer.dwStatus = 0;

    hr = m_pMixer->ProcessOutput(0, 1, &dataBuffer, &dwStatus);

    if (FAILED(hr))
    {
        // Return the sample to the pool.
        HRESULT hr2 = m_SamplePool.ReturnSample(pSample);
        if (FAILED(hr2))
        {
            hr = hr2;
            goto done;
        }
        // Handle some known error codes from ProcessOutput.
        if (hr == MF_E_TRANSFORM_TYPE_NOT_SET)
        {
            // The mixer's format is not set. Negotiate a new format.
            hr = RenegotiateMediaType();
        }
        else if (hr == MF_E_TRANSFORM_STREAM_CHANGE)
        {
            // There was a dynamic media type change. Clear our media type.
            SetMediaType(NULL);
        }
        else if (hr == MF_E_TRANSFORM_NEED_MORE_INPUT)
        {
            // The mixer needs more input.
            // We have to wait for the mixer to get more input.
            m_bSampleNotify = FALSE;
        }
    }
    else
    {
        // We got an output sample from the mixer.

        if (m_pClock && !bRepaint)
        {
            // Latency: Record the ending time for the ProcessOutput operation,
            // and notify the EVR of the latency.

            (void)m_pClock->GetCorrelatedTime(0, &mixerEndTime, &systemTime);

            LONGLONG latencyTime = mixerEndTime - mixerStartTime;
            NotifyEvent(EC_PROCESSING_LATENCY, (LONG_PTR)&latencyTime, 0);
        }

        // Set up notification for when the sample is released.
        hr = TrackSample(pSample);
        if (FAILED(hr))
        {
            goto done;
        }

        // Schedule the sample.
        if ((m_FrameStep.state == FRAMESTEP_NONE) || bRepaint)
        {
            hr = DeliverSample(pSample, bRepaint);
            if (FAILED(hr))
            {
                goto done;
            }
        }
        else
        {
            // We are frame-stepping (and this is not a repaint request).
            hr = DeliverFrameStepSample(pSample);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        m_bPrerolled = TRUE; // We have presented at least one sample now.
    }

done:
    SafeRelease(&pSample);

    // Important: Release any events returned from the ProcessOutput method.
    SafeRelease(&dataBuffer.pEvents);
    return hr;
}
```



<span data-ttu-id="4ea41-587">Einige Hinweise zu diesem Beispiel:</span><span class="sxs-lookup"><span data-stu-id="4ea41-587">Some remarks about this example:</span></span>

-   <span data-ttu-id="4ea41-588">Bei der *m_SamplePool* Variablen handelt es sich um ein Auflistungs Objekt, das die Warteschlange von verfügbaren Videobeispielen enthält.</span><span class="sxs-lookup"><span data-stu-id="4ea41-588">The *m_SamplePool* variable is assumed to be a collection object that holds the queue of available video samples.</span></span> <span data-ttu-id="4ea41-589">Die-Methode des-Objekts `GetSample` gibt **MF_E_SAMPLEALLOCATOR_EMPTY** zurück, wenn die Warteschlange leer ist.</span><span class="sxs-lookup"><span data-stu-id="4ea41-589">The object's `GetSample` method returns **MF_E_SAMPLEALLOCATOR_EMPTY** if the queue is empty.</span></span>
-   <span data-ttu-id="4ea41-590">Wenn die [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) -Methode des Mischers MF_E_TRANSFORM_NEED_MORE_INPUT zurückgibt, bedeutet dies, dass der Mixer keine Ausgabe mehr ausgeben kann, sodass der Presenter das *m_fSampleNotify* -Flag löscht.</span><span class="sxs-lookup"><span data-stu-id="4ea41-590">If the mixer's [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) method returns MF_E_TRANSFORM_NEED_MORE_INPUT, it means the mixer cannot produce any more output, so the presenter clears the *m_fSampleNotify* flag.</span></span>
-   <span data-ttu-id="4ea41-591">Die- `TrackSample` Methode, mit der der [**IMF trackedsample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) -Rückruf festgelegt wird, wird im Abschnitt nach [Verfolgungs Beispielen](#tracking-samples)gezeigt.</span><span class="sxs-lookup"><span data-stu-id="4ea41-591">The `TrackSample` method, which sets the [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) callback, is shown in the section [Tracking Samples](#tracking-samples).</span></span>

### <a name="repainting-frames"></a><span data-ttu-id="4ea41-592">Neuzeichnen von Frames</span><span class="sxs-lookup"><span data-stu-id="4ea41-592">Repainting Frames</span></span>

<span data-ttu-id="4ea41-593">Gelegentlich muss der Presenter möglicherweise den neuesten Videoframe neu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-593">Occasionally the presenter might need to repaint the most recent video frame.</span></span> <span data-ttu-id="4ea41-594">Der Standard Presenter zeichnet den Frame z. b. in den folgenden Situationen:</span><span class="sxs-lookup"><span data-stu-id="4ea41-594">For example, the standard presenter repaints the frame in the following situations:</span></span>

-   <span data-ttu-id="4ea41-595">Im Fenstermodus als Reaktion auf **WM_PAINT** vom Anwendungsfenster empfangene Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="4ea41-595">In windowed mode, in response to **WM_PAINT** messages received by the application's window.</span></span> <span data-ttu-id="4ea41-596">Weitere Informationen finden Sie unter [**IMF videodisplaycontrol:: repaintvideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo).</span><span class="sxs-lookup"><span data-stu-id="4ea41-596">See [**IMFVideoDisplayControl::RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo).</span></span>
-   <span data-ttu-id="4ea41-597">, Wenn das Ziel Rechteck geändert wird, wenn die Anwendung [**IMF videodisplaycontrol:: setvideoposition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition)aufruft.</span><span class="sxs-lookup"><span data-stu-id="4ea41-597">If the destination rectangle changes when the application calls [**IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span></span>

<span data-ttu-id="4ea41-598">Führen Sie die folgenden Schritte aus, um den Mixer aufzufordern, den letzten Frame neu zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="4ea41-598">Use the following steps to request the mixer to re-create the most recent frame:</span></span>

1.  <span data-ttu-id="4ea41-599">Holen Sie sich ein Video Beispiel aus der Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="4ea41-599">Get a video sample from the queue.</span></span>
2.  <span data-ttu-id="4ea41-600">Fragen Sie das Beispiel nach der [**imbodesiredsample**](/windows/desktop/api/evr/nn-evr-imfdesiredsample) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="4ea41-600">Query the sample for the [**IMFDesiredSample**](/windows/desktop/api/evr/nn-evr-imfdesiredsample) interface.</span></span>
3.  <span data-ttu-id="4ea41-601">[**Imfdesiredsample:: setdesiredsampletimeandduration**](/windows/desktop/api/evr/nf-evr-imfdesiredsample-setdesiredsampletimeandduration)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-601">Call [**IMFDesiredSample::SetDesiredSampleTimeAndDuration**](/windows/desktop/api/evr/nf-evr-imfdesiredsample-setdesiredsampletimeandduration).</span></span> <span data-ttu-id="4ea41-602">Geben Sie den Zeitstempel des letzten Video Rahmens an.</span><span class="sxs-lookup"><span data-stu-id="4ea41-602">Specify the time stamp of the most recent video frame.</span></span> <span data-ttu-id="4ea41-603">(Sie müssen diesen Wert Zwischenspeichern und für jeden Frame aktualisieren.)</span><span class="sxs-lookup"><span data-stu-id="4ea41-603">(You will need to cache this value and update it for each frame.)</span></span>
4.  <span data-ttu-id="4ea41-604">Ruft [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) auf dem Mixer auf.</span><span class="sxs-lookup"><span data-stu-id="4ea41-604">Call [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) on the mixer.</span></span>

<span data-ttu-id="4ea41-605">Wenn Sie einen Frame neu zeichnen, können Sie die Präsentations Uhr ignorieren und den Frame sofort darstellen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-605">When repainting a frame, you can ignore the presentation clock and present the frame immediately.</span></span>

### <a name="scheduling-samples"></a><span data-ttu-id="4ea41-606">Beispiele für Zeitplanung</span><span class="sxs-lookup"><span data-stu-id="4ea41-606">Scheduling Samples</span></span>

<span data-ttu-id="4ea41-607">Video Frames können jederzeit den EVR erreichen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-607">Video frames can reach the EVR at any time.</span></span> <span data-ttu-id="4ea41-608">Der Presenter ist für die Darstellung der einzelnen Frames zur richtigen Zeit basierend auf dem Zeitstempel des Frames verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="4ea41-608">The presenter is responsible for presenting each frame at the correct time, based on the time stamp of the frame.</span></span> <span data-ttu-id="4ea41-609">Wenn der Presenter ein neues Beispiel aus dem Mixer erhält, wird das Beispiel in die geplante Warteschlange eingefügt.</span><span class="sxs-lookup"><span data-stu-id="4ea41-609">When the presenter gets a new sample from the mixer, it puts the sample on the scheduled queue.</span></span> <span data-ttu-id="4ea41-610">In einem separaten Thread ruft der Presenter das erste Beispiel kontinuierlich vom Anfang der Warteschlange ab und bestimmt, ob Folgendes möglich ist:</span><span class="sxs-lookup"><span data-stu-id="4ea41-610">On a separate thread, the presenter continually gets the first sample from the head of the queue and determines whether to:</span></span>

-   <span data-ttu-id="4ea41-611">Stellen Sie das Beispiel dar.</span><span class="sxs-lookup"><span data-stu-id="4ea41-611">Present the sample.</span></span>
-   <span data-ttu-id="4ea41-612">Behalten Sie das Beispiel in der Warteschlange, da es frühzeitig ist.</span><span class="sxs-lookup"><span data-stu-id="4ea41-612">Keep the sample on the queue because it is early.</span></span>
-   <span data-ttu-id="4ea41-613">Verwerfen Sie das Beispiel, weil es spät ist.</span><span class="sxs-lookup"><span data-stu-id="4ea41-613">Discard the sample because it is late.</span></span> <span data-ttu-id="4ea41-614">Obwohl Sie nach Möglichkeit das Löschen von Frames vermeiden sollten, ist es möglicherweise erforderlich, wenn der Presenter ständig dahinter stürzt.</span><span class="sxs-lookup"><span data-stu-id="4ea41-614">Although you should avoid dropping frames if possible, you might need to if the presenter is continually falling behind.</span></span>

<span data-ttu-id="4ea41-615">Um den Zeitstempel für einen Videorahmen abzurufen, nennen Sie [**imfsample:: getsampletime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) im Video Beispiel.</span><span class="sxs-lookup"><span data-stu-id="4ea41-615">To get the time stamp for a video frame, call [**IMFSample::GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) on the video sample.</span></span> <span data-ttu-id="4ea41-616">Der Zeitstempel ist relativ zur Präsentations Uhr des EVR.</span><span class="sxs-lookup"><span data-stu-id="4ea41-616">The time stamp is relative to the EVR's presentation clock.</span></span> <span data-ttu-id="4ea41-617">Um die aktuelle Uhrzeit abzurufen, wenden Sie [**imfclock:: getcorrelatedtime**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime)an.</span><span class="sxs-lookup"><span data-stu-id="4ea41-617">To get the current clock time, call [**IMFClock::GetCorrelatedTime**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime).</span></span> <span data-ttu-id="4ea41-618">Wenn der EVR keine Präsentations Uhr hat oder wenn ein Beispiel keinen Zeitstempel hat, können Sie das Beispiel sofort nach dem Get-Vorgang darstellen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-618">If the EVR does not have a presentation clock, or if a sample does not have a time stamp, you can present the sample immediately after you get it.</span></span>

<span data-ttu-id="4ea41-619">Um die Dauer der einzelnen Stichproben abzurufen, müssen Sie [**imfsample:: getsampleduration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampleduration)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-619">To get the duration of each sample, call [**IMFSample::GetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampleduration).</span></span> <span data-ttu-id="4ea41-620">Wenn das Beispiel keine Dauer hat, können Sie die [**mfframerateesaveragetimeperframe**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) -Funktion verwenden, um die Dauer der Framerate zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-620">If the sample does not have a duration, you can use the [**MFFrameRateToAverageTimePerFrame**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) function to calculate the duration from the frame rate.</span></span>

<span data-ttu-id="4ea41-621">Beachten Sie beim Planen von Beispielen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="4ea41-621">When you schedule samples, keep in mind the following:</span></span>

-   <span data-ttu-id="4ea41-622">Wenn die Wiedergabe Rate schneller oder langsamer als die normale Geschwindigkeit ist, wird die Uhr schneller oder langsamer ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4ea41-622">If the playback rate is faster or slower than normal speed, the clock runs at a faster or slower rate.</span></span> <span data-ttu-id="4ea41-623">Dies bedeutet, dass der Zeitstempel in einem Beispiel immer die richtige Zielzeit in Relation zur Präsentationszeit ergibt.</span><span class="sxs-lookup"><span data-stu-id="4ea41-623">That means the time stamp on a sample always gives the correct target time relative to the presentation clock.</span></span> <span data-ttu-id="4ea41-624">Wenn Sie die Präsentations Zeiten jedoch in eine andere Uhrzeit übersetzen (z. b. den Leistungs-Leistungs-Leistungs-Leistungs-Leistungs-Leistungs-Leistungs Bewert), müssen Sie die Zeiten basierend auf der Taktfrequenz skalieren.</span><span class="sxs-lookup"><span data-stu-id="4ea41-624">However, if you translate presentation times into some other clock time (for example, the high-resolution performace counter), then you must scale the times based on the clock speed.</span></span> <span data-ttu-id="4ea41-625">Wenn sich die Taktfrequenz ändert, ruft der EVR die [**imfclockstaatink:: onclockertrate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) -Methode des Presenter auf.</span><span class="sxs-lookup"><span data-stu-id="4ea41-625">If the clock speed changes, the EVR calls the presenter's [**IMFClockStateSink::OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) method.</span></span>
-   <span data-ttu-id="4ea41-626">Die Wiedergabe Rate kann für die umgekehrte Wiedergabe negativ sein.</span><span class="sxs-lookup"><span data-stu-id="4ea41-626">The playback rate can be negative for reverse playback.</span></span> <span data-ttu-id="4ea41-627">Wenn die Wiedergabe Rate negativ ist, wird die Präsentations Uhr rückwärts ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4ea41-627">When the playback rate is negative, the presentation clock runs backward.</span></span> <span data-ttu-id="4ea41-628">Anders ausgedrückt: Zeit *n* + 1 tritt vor der Zeit *n* auf.</span><span class="sxs-lookup"><span data-stu-id="4ea41-628">In other words, time *N* + 1 occurs before time *N*.</span></span>

<span data-ttu-id="4ea41-629">Im folgenden Beispiel wird berechnet, wie früh oder spät ein Beispiel relativ zur Präsentations Uhr ist:</span><span class="sxs-lookup"><span data-stu-id="4ea41-629">The following example calculates how early or late a sample is, relative to the presentation clock:</span></span>


```C++
    LONGLONG hnsPresentationTime = 0;
    LONGLONG hnsTimeNow = 0;
    MFTIME   hnsSystemTime = 0;

    BOOL bPresentNow = TRUE;
    LONG lNextSleep = 0;

    if (m_pClock)
    {
        // Get the sample's time stamp. It is valid for a sample to
        // have no time stamp.
        hr = pSample->GetSampleTime(&hnsPresentationTime);

        // Get the clock time. (But if the sample does not have a time stamp,
        // we don't need the clock time.)
        if (SUCCEEDED(hr))
        {
            hr = m_pClock->GetCorrelatedTime(0, &hnsTimeNow, &hnsSystemTime);
        }

        // Calculate the time until the sample's presentation time.
        // A negative value means the sample is late.
        LONGLONG hnsDelta = hnsPresentationTime - hnsTimeNow;
        if (m_fRate < 0)
        {
            // For reverse playback, the clock runs backward. Therefore, the
            // delta is reversed.
            hnsDelta = - hnsDelta;
        }
```



<span data-ttu-id="4ea41-630">Die Präsentationszeit wird normalerweise durch die Systemuhr oder den audiorenderer gesteuert.</span><span class="sxs-lookup"><span data-stu-id="4ea41-630">The presentation clock is usually driven by the system clock or the audio renderer.</span></span> <span data-ttu-id="4ea41-631">(Der audiorenderer leitet die Uhrzeit von der Rate ab, mit der die Audiokarte Audiodaten verbraucht.) Im Allgemeinen wird die Präsentations Uhr nicht mit der Aktualisierungsrate des Monitors synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="4ea41-631">(The audio renderer derives the time from the rate at which the sound card consumes audio.) In general, the presentation clock is not synchronized with the refresh rate of the monitor.</span></span>

<span data-ttu-id="4ea41-632">Wenn Ihre Direct3D Presentation-Parameter für das Präsentations Intervall **D3DPRESENT_INTERVAL_DEFAULT** oder **D3DPRESENT_INTERVAL_ONE** angeben, wartet der **aktuelle** Vorgang auf die vertikale neuverfolgung des Monitors.</span><span class="sxs-lookup"><span data-stu-id="4ea41-632">If your Direct3D presentation parameters specify **D3DPRESENT_INTERVAL_DEFAULT** or **D3DPRESENT_INTERVAL_ONE** for the presentation interval, the **Present** operation waits for the monitor's vertical retrace.</span></span> <span data-ttu-id="4ea41-633">Dies ist eine einfache Möglichkeit, das Zerreißen zu verhindern, aber die Genauigkeit des Planungs Algorithmus zu verringern.</span><span class="sxs-lookup"><span data-stu-id="4ea41-633">This is an easy way to prevent tearing, but reduces the accuracy of your scheduling algorithm.</span></span> <span data-ttu-id="4ea41-634">Wenn das Präsentations Intervall **D3DPRESENT_INTERVAL_IMMEDIATE** ist, wird die **aktuelle** Methode sofort ausgeführt. Dies führt zu einem ausreißenden, es sei denn, der Zeit Planungs Algorithmus ist genau genug, den **Sie nur während** des vertikalen zurückverfolgen-Zeitraums aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-634">Conversely, if the presentation interval is **D3DPRESENT_INTERVAL_IMMEDIATE**, the **Present** method executes immediately, which causes tearing unless your scheduling algorithm is accurate enough that you call **Present** only during the vertical retrace period.</span></span>

<span data-ttu-id="4ea41-635">Die folgenden Funktionen können Ihnen helfen, genaue Zeit Steuerungsinformationen zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="4ea41-635">The following functions can help you get accurate timing information:</span></span>

-   <span data-ttu-id="4ea41-636">**IDirect3DDevice9:: getrasterstatus** gibt Informationen zum Raster zurück, einschließlich der aktuellen Überprüfungs Zeile und der Angabe, ob sich das Raster im vertikalen leeren Zeitraum befindet.</span><span class="sxs-lookup"><span data-stu-id="4ea41-636">**IDirect3DDevice9::GetRasterStatus** returns information about the raster, including the current scan line and whether the raster is in the vertical blank period.</span></span>
-   <span data-ttu-id="4ea41-637">**Dwmgetcompositiontiminginfo** gibt Zeit Steuerungsinformationen für den Desktop Fenster-Manager zurück.</span><span class="sxs-lookup"><span data-stu-id="4ea41-637">**DwmGetCompositionTimingInfo** returns timing information for the desktop window manager.</span></span> <span data-ttu-id="4ea41-638">Diese Informationen sind nützlich, wenn die Desktop Komposition aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="4ea41-638">This information is useful if desktop composition is enabled.</span></span>

### <a name="presenting-samples"></a><span data-ttu-id="4ea41-639">Präsentieren von Beispielen</span><span class="sxs-lookup"><span data-stu-id="4ea41-639">Presenting Samples</span></span>

<span data-ttu-id="4ea41-640">In diesem Abschnitt wird davon ausgegangen, dass Sie eine separate austauschkette für jede Oberfläche erstellt haben, wie unter [Zuordnen von Direct3D-Oberflächen](#allocating-direct3d-surfaces)</span><span class="sxs-lookup"><span data-stu-id="4ea41-640">This section assumes that you created a separate swap chain for each surface as described in [Allocating Direct3D Surfaces](#allocating-direct3d-surfaces).</span></span> <span data-ttu-id="4ea41-641">Um ein Beispiel zu präsentieren, können Sie die SwapChain aus dem Video Beispiel wie folgt erstellen:</span><span class="sxs-lookup"><span data-stu-id="4ea41-641">To present a sample, get the swap chain from the video sample as follows:</span></span>

1.  <span data-ttu-id="4ea41-642">Aufrufen von [**imfsample:: getbufferbyindex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) für das Video Beispiel zum Abrufen des Puffers.</span><span class="sxs-lookup"><span data-stu-id="4ea41-642">Call [**IMFSample::GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) on the video sample to get the buffer.</span></span>
2.  <span data-ttu-id="4ea41-643">Abfragen des Puffers für die [**IMF GetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="4ea41-643">Query the buffer for the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span>
3.  <span data-ttu-id="4ea41-644">Aufrufen von [**imfgetservice:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) zum Abrufen der **IDirect3DSurface9** -Schnittstelle der Direct3D-Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="4ea41-644">Call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) to get the **IDirect3DSurface9** interface of the Direct3D surface.</span></span> <span data-ttu-id="4ea41-645">(Sie können diesen Schritt und den vorherigen Schritt in einem Schritt kombinieren, indem Sie [**mfgetservice**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice)aufrufen.)</span><span class="sxs-lookup"><span data-stu-id="4ea41-645">(You can combine this step and the previous step into one by calling [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).)</span></span>
4.  <span data-ttu-id="4ea41-646">Aufrufen von **IDirect3DSurface9:: getContainer** auf der-Oberfläche, um einen Zeiger auf die Swapkette zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4ea41-646">Call **IDirect3DSurface9::GetContainer** on the surface to get a pointer to the swap chain.</span></span>
5.  <span data-ttu-id="4ea41-647">**IDirect3DSwapChain9::P erneut** an die Swapkette gesendet.</span><span class="sxs-lookup"><span data-stu-id="4ea41-647">Call **IDirect3DSwapChain9::Present** on the swap chain.</span></span>

<span data-ttu-id="4ea41-648">Diese Schritte sind im folgenden Code dargestellt:</span><span class="sxs-lookup"><span data-stu-id="4ea41-648">The following code shows these steps:</span></span>


```C++
HRESULT D3DPresentEngine::PresentSample(IMFSample* pSample, LONGLONG llTarget)
{
    HRESULT hr = S_OK;

    IMFMediaBuffer* pBuffer = NULL;
    IDirect3DSurface9* pSurface = NULL;
    IDirect3DSwapChain9* pSwapChain = NULL;

    if (pSample)
    {
        // Get the buffer from the sample.
        hr = pSample->GetBufferByIndex(0, &pBuffer);
        if (FAILED(hr))
        {
            goto done;
        }

        // Get the surface from the buffer.
        hr = MFGetService(pBuffer, MR_BUFFER_SERVICE, IID_PPV_ARGS(&pSurface));
        if (FAILED(hr))
        {
            goto done;
        }
    }
    else if (m_pSurfaceRepaint)
    {
        // Redraw from the last surface.
        pSurface = m_pSurfaceRepaint;
        pSurface->AddRef();
    }

    if (pSurface)
    {
        // Get the swap chain from the surface.
        hr = pSurface->GetContainer(IID_PPV_ARGS(&pSwapChain));
        if (FAILED(hr))
        {
            goto done;
        }

        // Present the swap chain.
        hr = PresentSwapChain(pSwapChain, pSurface);
        if (FAILED(hr))
        {
            goto done;
        }

        // Store this pointer in case we need to repaint the surface.
        CopyComPointer(m_pSurfaceRepaint, pSurface);
    }
    else
    {
        // No surface. All we can do is paint a black rectangle.
        PaintFrameWithGDI();
    }

done:
    SafeRelease(&pSwapChain);
    SafeRelease(&pSurface);
    SafeRelease(&pBuffer);

    if (FAILED(hr))
    {
        if (hr == D3DERR_DEVICELOST || hr == D3DERR_DEVICENOTRESET || hr == D3DERR_DEVICEHUNG)
        {
            // We failed because the device was lost. Fill the destination rectangle.
            PaintFrameWithGDI();

            // Ignore. We need to reset or re-create the device, but this method
            // is probably being called from the scheduler thread, which is not the
            // same thread that created the device. The Reset(Ex) method must be
            // called from the thread that created the device.

            // The presenter will detect the state when it calls CheckDeviceState()
            // on the next sample.
            hr = S_OK;
        }
    }
    return hr;
}
```



### <a name="source-and-destination-rectangles"></a><span data-ttu-id="4ea41-649">Quell-und Ziel Rechtecke</span><span class="sxs-lookup"><span data-stu-id="4ea41-649">Source and Destination Rectangles</span></span>

<span data-ttu-id="4ea41-650">Das *Quell Rechteck* ist der Teil des Video Frames, der angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4ea41-650">The *source rectangle* is the portion of the video frame to display.</span></span> <span data-ttu-id="4ea41-651">Sie wird relativ zu einem normalisierten Koordinatensystem definiert, in dem der gesamte Videorahmen ein Rechteck mit den Koordinaten {0, 0, 1, 1} einnimmt.</span><span class="sxs-lookup"><span data-stu-id="4ea41-651">It is defined relative to a normalized coordinate system, in which the entire video frame occupies a rectangle with coordinates {0, 0, 1, 1}.</span></span> <span data-ttu-id="4ea41-652">Das *Ziel Rechteck* ist der Bereich innerhalb der Ziel Oberfläche, in dem der Videorahmen gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="4ea41-652">The *destination rectangle* is the area within the destination surface where the video frame is drawn.</span></span> <span data-ttu-id="4ea41-653">Der Standard Presenter ermöglicht einer Anwendung, diese Rechtecke durch Aufrufen von [**imfvideodisplaycontrol:: setvideoposition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition)festzulegen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-653">The standard presenter enables an application to set these rectangles by calling [**IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span></span>

<span data-ttu-id="4ea41-654">Es gibt mehrere Optionen für das Anwenden von Quell-und Ziel Rechtecke.</span><span class="sxs-lookup"><span data-stu-id="4ea41-654">There are several options for applying source and destination rectangles.</span></span> <span data-ttu-id="4ea41-655">Die erste Option besteht darin, den Mixer darauf anzuwenden:</span><span class="sxs-lookup"><span data-stu-id="4ea41-655">The first option is to let the mixer apply them:</span></span>

-   <span data-ttu-id="4ea41-656">Legen Sie das Quell Rechteck mithilfe des [**VIDEO_ZOOM_RECT**](video-zoom-rect-attribute.md) -Attributs fest.</span><span class="sxs-lookup"><span data-stu-id="4ea41-656">Set the source rectangle using the [**VIDEO_ZOOM_RECT**](video-zoom-rect-attribute.md) attribute.</span></span> <span data-ttu-id="4ea41-657">Der Mixer wendet das Quell Rechteck an, wenn es das Video auf der Ziel Oberfläche Blicke.</span><span class="sxs-lookup"><span data-stu-id="4ea41-657">The mixer will apply the source rectangle when it blits the video to the destination surface.</span></span> <span data-ttu-id="4ea41-658">Das standardmäßige Quell Rechteck des Mischers ist der gesamte Frame.</span><span class="sxs-lookup"><span data-stu-id="4ea41-658">The mixer's default source rectangle is the entire frame.</span></span>
-   <span data-ttu-id="4ea41-659">Legen Sie das Ziel Rechteck als geometrische Öffnung im Ausgabetyp des Mischers fest.</span><span class="sxs-lookup"><span data-stu-id="4ea41-659">Set the destination rectangle as the geometric aperture in the mixer's output type.</span></span> <span data-ttu-id="4ea41-660">Weitere Informationen finden Sie unter [Aushandeln von Formaten](#negotiating-formats).</span><span class="sxs-lookup"><span data-stu-id="4ea41-660">For more information, see [Negotiating Formats](#negotiating-formats).</span></span>

<span data-ttu-id="4ea41-661">Die zweite Option ist das Anwenden der Rechtecke bei der **IDirect3DSwapChain9::P erneut gesendet** , indem die Parameter *psourcerect* und *pdestrect* in der **aktuellen** Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4ea41-661">The second option is to apply the rectangles when you **IDirect3DSwapChain9::Present** by specifying the *pSourceRect* and *pDestRect* parameters in the **Present** method.</span></span> <span data-ttu-id="4ea41-662">Diese Optionen können kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="4ea41-662">You can combine these options.</span></span> <span data-ttu-id="4ea41-663">Beispielsweise können Sie das Quell Rechteck auf dem Mixer festlegen, aber das Ziel Rechteck in der **aktuellen** Methode anwenden.</span><span class="sxs-lookup"><span data-stu-id="4ea41-663">For example, you could set the source rectangle on the mixer but apply the destination rectangle in the **Present** method.</span></span>

<span data-ttu-id="4ea41-664">Wenn die Anwendung das Ziel Rechteck ändert oder die Größe des Fensters ändert, müssen Sie möglicherweise neue Oberflächen zuordnen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-664">If the application changes the destination rectangle or resizes the window, you might need to allocate new surfaces.</span></span> <span data-ttu-id="4ea41-665">Wenn dies der Fall ist, müssen Sie darauf achten, diesen Vorgang mit Ihrem Zeit Planungs Thread zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="4ea41-665">If so, you must be careful to synchronize this operation with your scheduling thread.</span></span> <span data-ttu-id="4ea41-666">Leeren Sie die Planungs Warteschlange, und verwerfen Sie die alten Beispiele, bevor Sie neue Oberflächen</span><span class="sxs-lookup"><span data-stu-id="4ea41-666">Flush the scheduling queue and discard the old samples before allocating new surfaces.</span></span>

### <a name="end-of-stream"></a><span data-ttu-id="4ea41-667">Ende des Streams</span><span class="sxs-lookup"><span data-stu-id="4ea41-667">End of Stream</span></span>

<span data-ttu-id="4ea41-668">Wenn jeder Eingabedaten Strom im EVR beendet wurde, sendet der EVR eine **MFVP_MESSAGE_ENDOFSTREAM** Meldung an den Presenter.</span><span class="sxs-lookup"><span data-stu-id="4ea41-668">When every input stream on the EVR has ended, the EVR sends an **MFVP_MESSAGE_ENDOFSTREAM** message to the presenter.</span></span> <span data-ttu-id="4ea41-669">An dem Punkt, an dem Sie die Nachricht erhalten, kann es jedoch noch einige Video Frames geben, die verarbeitet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-669">At the point when you receive the message, however, there might be a few video frames remaining to be processed.</span></span> <span data-ttu-id="4ea41-670">Bevor Sie auf das Ende der Stream-Nachricht reagieren, müssen Sie die gesamte Ausgabe des Mischers ableiten und alle verbleibenden Frames darstellen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-670">Before you respond to the end-of-stream message, you must drain all of the output from the mixer and present all of the remaining frames.</span></span> <span data-ttu-id="4ea41-671">Nachdem der letzte Frame angezeigt wurde, senden Sie ein **EC_COMPLETE** Ereignis an den EVR.</span><span class="sxs-lookup"><span data-stu-id="4ea41-671">After the last frame is presented, send an **EC_COMPLETE** event to the EVR.</span></span>

<span data-ttu-id="4ea41-672">Das nächste Beispiel zeigt eine Methode, die das **EC_COMPLETE** Ereignis sendet, wenn verschiedene Bedingungen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="4ea41-672">The next example shows a method that sends the **EC_COMPLETE** event if various conditions are met.</span></span> <span data-ttu-id="4ea41-673">Andernfalls wird S_OK zurückgegeben, ohne das Ereignis zu senden:</span><span class="sxs-lookup"><span data-stu-id="4ea41-673">Otherwise, it returns S_OK without sending the event:</span></span>


```C++
HRESULT EVRCustomPresenter::CheckEndOfStream()
{
    if (!m_bEndStreaming)
    {
        // The EVR did not send the MFVP_MESSAGE_ENDOFSTREAM message.
        return S_OK;
    }

    if (m_bSampleNotify)
    {
        // The mixer still has input.
        return S_OK;
    }

    if (m_SamplePool.AreSamplesPending())
    {
        // Samples are still scheduled for rendering.
        return S_OK;
    }

    // Everything is complete. Now we can tell the EVR that we are done.
    NotifyEvent(EC_COMPLETE, (LONG_PTR)S_OK, 0);
    m_bEndStreaming = FALSE;
    return S_OK;
}
```



<span data-ttu-id="4ea41-674">Diese Methode überprüft die folgenden Zustände:</span><span class="sxs-lookup"><span data-stu-id="4ea41-674">This method checks the following states:</span></span>

-   <span data-ttu-id="4ea41-675">Wenn die *m_fSampleNotify* Variable den Wert **true** aufweist, bedeutet dies, dass der Mixer über einen oder mehrere Frames verfügt, die noch nicht verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="4ea41-675">If the *m_fSampleNotify* variable is **TRUE**, it means the mixer has one or more frames that have not been processed yet.</span></span> <span data-ttu-id="4ea41-676">(Ausführliche Informationen finden Sie unter [Verarbeiten der Ausgabe](#processing-output).)</span><span class="sxs-lookup"><span data-stu-id="4ea41-676">(For details, see [Processing Output](#processing-output).)</span></span>
-   <span data-ttu-id="4ea41-677">Die *m_fEndStreaming* Variable ist ein boolesches Flag, dessen ursprünglicher Wert **false** ist.</span><span class="sxs-lookup"><span data-stu-id="4ea41-677">The *m_fEndStreaming* variable is a Boolean flag whose initial value **FALSE**.</span></span> <span data-ttu-id="4ea41-678">Der Presenter legt das-Flag auf **true** fest, wenn der EVR die **MFVP_MESSAGE_ENDOFSTREAM** Nachricht sendet.</span><span class="sxs-lookup"><span data-stu-id="4ea41-678">The presenter sets the flag to **TRUE** when the EVR sends the **MFVP_MESSAGE_ENDOFSTREAM** message.</span></span>
-   <span data-ttu-id="4ea41-679">`AreSamplesPending`Es wird davon ausgegangen, dass die Methode " **true** " zurückgibt, solange mindestens ein Rahmen in der geplanten Warteschlange wartet.</span><span class="sxs-lookup"><span data-stu-id="4ea41-679">The `AreSamplesPending` method is assumed to return **TRUE** as long as one or more frames are waiting in the scheduled queue.</span></span>

<span data-ttu-id="4ea41-680">Legen Sie in der [**imfvideopresenter::P rocess Message**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) -Methode *m_fEndStreaming* auf **true** fest, und geben Sie an, `CheckEndOfStream` Wenn der EVR die **MFVP_MESSAGE_ENDOFSTREAM** Nachricht sendet:</span><span class="sxs-lookup"><span data-stu-id="4ea41-680">In the [**IMFVideoPresenter::ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) method, set *m_fEndStreaming* to **TRUE** and call `CheckEndOfStream` when the EVR sends the **MFVP_MESSAGE_ENDOFSTREAM** message:</span></span>


```C++
HRESULT EVRCustomPresenter::ProcessMessage(
    MFVP_MESSAGE_TYPE eMessage,
    ULONG_PTR ulParam
    )
{
    HRESULT hr = S_OK;

    EnterCriticalSection(&m_ObjectLock);

    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    switch (eMessage)
    {
    // Flush all pending samples.
    case MFVP_MESSAGE_FLUSH:
        hr = Flush();
        break;

    // Renegotiate the media type with the mixer.
    case MFVP_MESSAGE_INVALIDATEMEDIATYPE:
        hr = RenegotiateMediaType();
        break;

    // The mixer received a new input sample.
    case MFVP_MESSAGE_PROCESSINPUTNOTIFY:
        hr = ProcessInputNotify();
        break;

    // Streaming is about to start.
    case MFVP_MESSAGE_BEGINSTREAMING:
        hr = BeginStreaming();
        break;

    // Streaming has ended. (The EVR has stopped.)
    case MFVP_MESSAGE_ENDSTREAMING:
        hr = EndStreaming();
        break;

    // All input streams have ended.
    case MFVP_MESSAGE_ENDOFSTREAM:
        // Set the EOS flag.
        m_bEndStreaming = TRUE;
        // Check if it's time to send the EC_COMPLETE event to the EVR.
        hr = CheckEndOfStream();
        break;

    // Frame-stepping is starting.
    case MFVP_MESSAGE_STEP:
        hr = PrepareFrameStep(LODWORD(ulParam));
        break;

    // Cancels frame-stepping.
    case MFVP_MESSAGE_CANCELSTEP:
        hr = CancelFrameStep();
        break;

    default:
        hr = E_INVALIDARG; // Unknown message. This case should never occur.
        break;
    }

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



<span data-ttu-id="4ea41-681">Außerdem wird aufgerufen, `CheckEndOfStream` Wenn die [**imftransform::P rocess Output**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) -Methode von Mixer **MF_E_TRANSFORM_NEED_MORE_INPUT** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="4ea41-681">In addition, call `CheckEndOfStream` if the mixer's [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) method returns **MF_E_TRANSFORM_NEED_MORE_INPUT**.</span></span> <span data-ttu-id="4ea41-682">Dieser Fehlercode gibt an, dass der Mixer keine weiteren Eingabe Beispiele hat (siehe [Verarbeitung der Ausgabe](#processing-output)).</span><span class="sxs-lookup"><span data-stu-id="4ea41-682">This error code indicates that the mixer has no more input samples (see [Processing Output](#processing-output)).</span></span>

## <a name="frame-stepping"></a><span data-ttu-id="4ea41-683">Frame Schritt Schritt</span><span class="sxs-lookup"><span data-stu-id="4ea41-683">Frame Stepping</span></span>

<span data-ttu-id="4ea41-684">Der EVR ist so konzipiert, dass Frame Step in DirectShow und Bereinigungs in Media Foundation unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="4ea41-684">The EVR is designed to support frame stepping in DirectShow and scrubbing in Media Foundation.</span></span> <span data-ttu-id="4ea41-685">Frame-Step und Bereinigungs sind konzeptionell ähnlich.</span><span class="sxs-lookup"><span data-stu-id="4ea41-685">Frame stepping and scrubbing are conceptually similar.</span></span> <span data-ttu-id="4ea41-686">In beiden Fällen fordert die Anwendung einen Video Frame gleichzeitig an.</span><span class="sxs-lookup"><span data-stu-id="4ea41-686">In both cases, the application requests one video frame at a time.</span></span> <span data-ttu-id="4ea41-687">Intern verwendet der Presenter denselben Mechanismus zum Implementieren beider Features.</span><span class="sxs-lookup"><span data-stu-id="4ea41-687">Internally, the presenter uses the same mechanism to implement both features.</span></span>

<span data-ttu-id="4ea41-688">Das schrittweise Ausführen von Frame Works in DirectShow funktioniert wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4ea41-688">Frame stepping in DirectShow works as follows:</span></span>

-   <span data-ttu-id="4ea41-689">Die Anwendung ruft [**ivideoframestep:: Step**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-step)auf.</span><span class="sxs-lookup"><span data-stu-id="4ea41-689">The application calls [**IVideoFrameStep::Step**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-step).</span></span> <span data-ttu-id="4ea41-690">Die Anzahl der Schritte wird im Parameter " *dwsteps* " angegeben.</span><span class="sxs-lookup"><span data-stu-id="4ea41-690">The number of steps is given in the *dwSteps* parameter.</span></span> <span data-ttu-id="4ea41-691">Der EVR sendet eine **MFVP_MESSAGE_STEP** Meldung an den Presenter, wobei der Message-Parameter (*ulparam*) die Anzahl von Schritten ist.</span><span class="sxs-lookup"><span data-stu-id="4ea41-691">The EVR sends an **MFVP_MESSAGE_STEP** message to the presenter, where the message parameter (*ulParam*) is the number of steps.</span></span>
-   <span data-ttu-id="4ea41-692">Wenn die Anwendung [**ivideoframestep:: cancelstep**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-cancelstep) aufruft oder den Diagramm Zustand ändert (wird ausgeführt, angehalten oder beendet), sendet der EVR eine **MFVP_MESSAGE_CANCELSTEP** Nachricht.</span><span class="sxs-lookup"><span data-stu-id="4ea41-692">If the application calls [**IVideoFrameStep::CancelStep**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-cancelstep) or changes the graph state (running, paused, or stopped), the EVR sends an **MFVP_MESSAGE_CANCELSTEP** message.</span></span>

<span data-ttu-id="4ea41-693">Das Scrubbing in Media Foundation funktioniert wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4ea41-693">Scrubbing in Media Foundation works as follows:</span></span>

-   <span data-ttu-id="4ea41-694">Die Anwendung legt die Wiedergabe Rate auf NULL fest, indem [**imfratecontrol:: setRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="4ea41-694">The application sets the playback rate to zero by calling [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate).</span></span>
-   <span data-ttu-id="4ea41-695">Um einen neuen Frame zu erzeugen, ruft die Anwendung [**imfmediasession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) an der gewünschten Position auf.</span><span class="sxs-lookup"><span data-stu-id="4ea41-695">To render a new frame, the application calls [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) with the desired position.</span></span> <span data-ttu-id="4ea41-696">Der EVR sendet eine **MFVP_MESSAGE_STEP** Nachricht mit *ulparam* gleich 1.</span><span class="sxs-lookup"><span data-stu-id="4ea41-696">The EVR sends an **MFVP_MESSAGE_STEP** message with *ulParam* equal to 1.</span></span>
-   <span data-ttu-id="4ea41-697">Um das Scrubbing zu verhindern, legt die Anwendung die Wiedergabe Rate auf einen Wert ungleich 0 (null) fest.</span><span class="sxs-lookup"><span data-stu-id="4ea41-697">To stop scrubbing, the application sets the playback rate to a nonzero value.</span></span> <span data-ttu-id="4ea41-698">Der EVR sendet die **MFVP_MESSAGE_CANCELSTEP** Nachricht.</span><span class="sxs-lookup"><span data-stu-id="4ea41-698">The EVR sends the **MFVP_MESSAGE_CANCELSTEP** message.</span></span>

<span data-ttu-id="4ea41-699">Nach dem Empfang der **MFVP_MESSAGE_STEP** Nachricht wartet der Presenter, bis der Zielframe eintrifft.</span><span class="sxs-lookup"><span data-stu-id="4ea41-699">After receiving the **MFVP_MESSAGE_STEP** message, the presenter waits for the target frame to arrive.</span></span> <span data-ttu-id="4ea41-700">Wenn die Anzahl der Schritte *N* ist, verwirft der Presenter die nächsten (*n* -1) Beispiele und zeigt das *N* -te Beispiel an.</span><span class="sxs-lookup"><span data-stu-id="4ea41-700">If the number of steps is *N*, the presenter discards the next (*N* - 1) samples and presents the *N* th sample.</span></span> <span data-ttu-id="4ea41-701">Wenn der Presenter den Rahmen Schritt abgeschlossen hat, sendet er ein [**EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) Ereignis an den EVR, wobei *lParam1* auf **false** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4ea41-701">When the presenter completes the frame step, it sends an [**EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) event to the EVR with *lParam1* set to **FALSE**.</span></span> <span data-ttu-id="4ea41-702">Wenn die Wiedergabe Rate NULL ist, sendet der Presenter außerdem ein [**EC_SCRUB_TIME**](../directshow/ec-scrub-time.md) Ereignis.</span><span class="sxs-lookup"><span data-stu-id="4ea41-702">In addition, if the playback rate is zero, the presenter sends an [**EC_SCRUB_TIME**](../directshow/ec-scrub-time.md) event.</span></span> <span data-ttu-id="4ea41-703">Wenn der EVR die Frame Ausführung abbricht, während ein Rahmen Schritt noch aussteht, sendet der Presenter ein **EC_STEP_COMPLETE** Ereignis, wobei *lParam1* auf **true** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4ea41-703">If the EVR cancels frame stepping while a frame-step operation is still pending, the presenter sends an **EC_STEP_COMPLETE** event with *lParam1* set to **TRUE**.</span></span>

<span data-ttu-id="4ea41-704">Die Anwendung kann den Schritt oder das Bereinigen mehrmals durchlaufen, sodass der Presenter möglicherweise mehrere **MFVP_MESSAGE_STEP** Meldungen empfängt, bevor er eine **MFVP_MESSAGE_CANCELSTEP** Nachricht erhält.</span><span class="sxs-lookup"><span data-stu-id="4ea41-704">The application can frame step or scrub multiple times, so the presenter might receive multiple **MFVP_MESSAGE_STEP** messages before it gets an **MFVP_MESSAGE_CANCELSTEP** message.</span></span> <span data-ttu-id="4ea41-705">Außerdem kann der Presenter die **MFVP_MESSAGE_STEP** Nachricht empfangen, bevor die Uhr beginnt oder während die Uhr ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4ea41-705">Also, the presenter can receive the **MFVP_MESSAGE_STEP** message before the clock starts or while the clock is running.</span></span>

### <a name="implementing-frame-stepping"></a><span data-ttu-id="4ea41-706">Implementieren von Frame-Stepping</span><span class="sxs-lookup"><span data-stu-id="4ea41-706">Implementing Frame Stepping</span></span>

<span data-ttu-id="4ea41-707">In diesem Abschnitt wird ein Algorithmus zum Implementieren von Frame-Stepping beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4ea41-707">This section describes an algorithm to implement frame stepping.</span></span> <span data-ttu-id="4ea41-708">Der Frame Step-Algorithmus verwendet die folgenden Variablen:</span><span class="sxs-lookup"><span data-stu-id="4ea41-708">The frame stepping algorithm uses the following variables:</span></span>

-   <span data-ttu-id="4ea41-709">*step_count*.</span><span class="sxs-lookup"><span data-stu-id="4ea41-709">*step_count*.</span></span> <span data-ttu-id="4ea41-710">Eine ganze Zahl ohne Vorzeichen, die die Anzahl der Schritte im aktuellen Frame-Schritt Vorgang angibt.</span><span class="sxs-lookup"><span data-stu-id="4ea41-710">An unsigned integer that specifies the number of steps in the current frame stepping operation.</span></span>
-   <span data-ttu-id="4ea41-711">*step_queue*.</span><span class="sxs-lookup"><span data-stu-id="4ea41-711">*step_queue*.</span></span> <span data-ttu-id="4ea41-712">Eine Warteschlange von [**IMF Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) -Zeigern.</span><span class="sxs-lookup"><span data-stu-id="4ea41-712">A queue of [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) pointers.</span></span>
-   <span data-ttu-id="4ea41-713">*step_state*.</span><span class="sxs-lookup"><span data-stu-id="4ea41-713">*step_state*.</span></span> <span data-ttu-id="4ea41-714">Der Präsentator kann jederzeit einen der folgenden Zustände in Bezug auf die Frame-Schrittfolge aufweisen:</span><span class="sxs-lookup"><span data-stu-id="4ea41-714">At any time, the presenter can be in one of the following states with respect to frame stepping:</span></span> 

    | <span data-ttu-id="4ea41-715">State</span><span class="sxs-lookup"><span data-stu-id="4ea41-715">State</span></span>         | <span data-ttu-id="4ea41-716">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4ea41-716">Description</span></span>                                                                                                                                                                                                     |
    |---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="4ea41-717">NOT_STEPPING</span><span class="sxs-lookup"><span data-stu-id="4ea41-717">NOT_STEPPING</span></span> | <span data-ttu-id="4ea41-718">Kein Frame Schritt Schritt.</span><span class="sxs-lookup"><span data-stu-id="4ea41-718">Not frame stepping.</span></span>                                                                                                                                                                                             |
    | <span data-ttu-id="4ea41-719">WAITING</span><span class="sxs-lookup"><span data-stu-id="4ea41-719">WAITING</span></span>       | <span data-ttu-id="4ea41-720">Der Presenter hat die **MFVP_MESSAGE_STEP** Nachricht empfangen, aber die Uhr wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="4ea41-720">The presenter has received the **MFVP_MESSAGE_STEP** message, but the clock has not started.</span></span>                                                                                                                  |
    | <span data-ttu-id="4ea41-721">PENDING (AUSSTEHEND)</span><span class="sxs-lookup"><span data-stu-id="4ea41-721">PENDING</span></span>       | <span data-ttu-id="4ea41-722">Der Presenter hat die **MFVP_MESSAGE_STEP** Nachricht empfangen, und die Uhr wurde gestartet, aber der Presenter wartet darauf, den Zielframe zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-722">The presenter has received the **MFVP_MESSAGE_STEP** message and the clock has started, but the presenter is waiting to receive the target frame.</span></span>                                                             |
    | <span data-ttu-id="4ea41-723">Findet</span><span class="sxs-lookup"><span data-stu-id="4ea41-723">SCHEDULED</span></span>     | <span data-ttu-id="4ea41-724">Der Präsentator hat den Zielframe empfangen und ihn für die Präsentation eingeplant, aber der Frame wurde nicht präsentiert.</span><span class="sxs-lookup"><span data-stu-id="4ea41-724">The presenter has received the target frame and has scheduled it for presentation, but the frame has not been presented.</span></span>                                                                                        |
    | <span data-ttu-id="4ea41-725">Ganz</span><span class="sxs-lookup"><span data-stu-id="4ea41-725">COMPLETE</span></span>      | <span data-ttu-id="4ea41-726">Der Präsentator hat den Zielframe dargestellt und das [**EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) -Ereignis gesendet und wartet auf die nächste **MFVP_MESSAGE_STEP** oder **MFVP_MESSAGE_CANCELSTEP** Meldung.</span><span class="sxs-lookup"><span data-stu-id="4ea41-726">The presenter has presented the target frame and sent the [**EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) event, and is waiting for the next **MFVP_MESSAGE_STEP** or **MFVP_MESSAGE_CANCELSTEP** message.</span></span> |

    

     

    <span data-ttu-id="4ea41-727">Diese Zustände sind unabhängig von den präsentatorzuständen, die im Abschnitt [Presenter States](#presenter-states)aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="4ea41-727">These states are independent of the presenter states listed in the section [Presenter States](#presenter-states).</span></span>

<span data-ttu-id="4ea41-728">Die folgenden Prozeduren sind für den Frame Step-Algorithmus definiert:</span><span class="sxs-lookup"><span data-stu-id="4ea41-728">The following procedures are defined for the frame-stepping algorithm:</span></span>

<span data-ttu-id="4ea41-729">Prepareframestep-Prozedur</span><span class="sxs-lookup"><span data-stu-id="4ea41-729">PrepareFrameStep Procedure</span></span>

1.  <span data-ttu-id="4ea41-730">*Step_count* Inkrement.</span><span class="sxs-lookup"><span data-stu-id="4ea41-730">Increment *step_count*.</span></span>
2.  <span data-ttu-id="4ea41-731">Legen Sie *step_state* auf warten fest.</span><span class="sxs-lookup"><span data-stu-id="4ea41-731">Set *step_state* to WAITING.</span></span>
3.  <span data-ttu-id="4ea41-732">Wenn die Uhr ausgeführt wird, müssen Sie startframestep aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-732">If the clock is running, call StartFrameStep.</span></span>

<span data-ttu-id="4ea41-733">Startframestep-Prozedur</span><span class="sxs-lookup"><span data-stu-id="4ea41-733">StartFrameStep Procedure</span></span>

1.  <span data-ttu-id="4ea41-734">Wenn *step_state* auf "warten" festgelegt ist, legen Sie *step_state* auf Pending</span><span class="sxs-lookup"><span data-stu-id="4ea41-734">If *step_state* equals WAITING, set *step_state* to PENDING.</span></span> <span data-ttu-id="4ea41-735">Nennen Sie für jedes Beispiel in *step_queue* deliverframestepsample.</span><span class="sxs-lookup"><span data-stu-id="4ea41-735">For each sample in *step_queue*, call DeliverFrameStepSample.</span></span>
2.  <span data-ttu-id="4ea41-736">Wenn *step_state* NOT_STEPPING ist, entfernen Sie alle Beispiele aus *step_queue* , und planen Sie Sie für die Präsentation.</span><span class="sxs-lookup"><span data-stu-id="4ea41-736">If *step_state* equals NOT_STEPPING, remove any samples from *step_queue* and schedule them for presentation.</span></span>

<span data-ttu-id="4ea41-737">Completeframestep-Prozedur</span><span class="sxs-lookup"><span data-stu-id="4ea41-737">CompleteFrameStep Procedure</span></span>

1.  <span data-ttu-id="4ea41-738">Legen Sie *step_state* auf Complete fest.</span><span class="sxs-lookup"><span data-stu-id="4ea41-738">Set *step_state* to COMPLETE.</span></span>
2.  <span data-ttu-id="4ea41-739">Senden Sie das EC_STEP_COMPLETE-Ereignis mit *lParam1*  =  **false**.</span><span class="sxs-lookup"><span data-stu-id="4ea41-739">Send the EC_STEP_COMPLETE event with *lParam1* = **FALSE**.</span></span>
3.  <span data-ttu-id="4ea41-740">Wenn die Taktrate NULL ist, senden Sie das **EC_SCRUB_TIME** -Ereignis mit der Beispiel Zeit.</span><span class="sxs-lookup"><span data-stu-id="4ea41-740">If the clock rate is zero, send the **EC_SCRUB_TIME** event with the sample time.</span></span>

<span data-ttu-id="4ea41-741">Deliverframestepsample-Prozedur</span><span class="sxs-lookup"><span data-stu-id="4ea41-741">DeliverFrameStepSample Procedure</span></span>

1.  <span data-ttu-id="4ea41-742">Wenn die Taktfrequenz 0 (null) und *Beispiel Zeit für Zeit*  +  *Stichprobe* ist  <  , verwerfen Sie das Beispiel.</span><span class="sxs-lookup"><span data-stu-id="4ea41-742">If the clock rate is zero and *sample time* + *sample duration* < *clock time*, discard the sample.</span></span> <span data-ttu-id="4ea41-743">Beenden</span><span class="sxs-lookup"><span data-stu-id="4ea41-743">Exit.</span></span>
2.  <span data-ttu-id="4ea41-744">Wenn *step_state* auf geplant oder fertiggestellt ist, fügen Sie das Beispiel *step_queue* hinzu.</span><span class="sxs-lookup"><span data-stu-id="4ea41-744">If *step_state* equals SCHEDULED or COMPLETE, add the sample to *step_queue*.</span></span> <span data-ttu-id="4ea41-745">Beenden</span><span class="sxs-lookup"><span data-stu-id="4ea41-745">Exit.</span></span>
3.  <span data-ttu-id="4ea41-746">Dekrement *step_count*.</span><span class="sxs-lookup"><span data-stu-id="4ea41-746">Decrement *step_count*.</span></span>
4.  <span data-ttu-id="4ea41-747">Wenn *step_count* > 0, verwerfen Sie das Beispiel.</span><span class="sxs-lookup"><span data-stu-id="4ea41-747">If *step_count* > 0, discard the sample.</span></span> <span data-ttu-id="4ea41-748">Beenden</span><span class="sxs-lookup"><span data-stu-id="4ea41-748">Exit.</span></span>
5.  <span data-ttu-id="4ea41-749">Wenn *step_state* den Zustand "warten" entspricht, fügen Sie das Beispiel *step_queue* hinzu.</span><span class="sxs-lookup"><span data-stu-id="4ea41-749">If *step_state* equals WAITING, add the sample to *step_queue*.</span></span> <span data-ttu-id="4ea41-750">Beenden</span><span class="sxs-lookup"><span data-stu-id="4ea41-750">Exit.</span></span>
6.  <span data-ttu-id="4ea41-751">Planen Sie das Beispiel für die Präsentation.</span><span class="sxs-lookup"><span data-stu-id="4ea41-751">Schedule the sample for presentation.</span></span>
7.  <span data-ttu-id="4ea41-752">Legen Sie *step_state* auf geplant fest.</span><span class="sxs-lookup"><span data-stu-id="4ea41-752">Set *step_state* to SCHEDULED.</span></span>

<span data-ttu-id="4ea41-753">Cancelframestep-Prozedur</span><span class="sxs-lookup"><span data-stu-id="4ea41-753">CancelFrameStep Procedure</span></span>

1.  <span data-ttu-id="4ea41-754">Legen Sie *step_state* auf NOT_STEPPING</span><span class="sxs-lookup"><span data-stu-id="4ea41-754">Set *step_state* to NOT_STEPPING</span></span>
2.  <span data-ttu-id="4ea41-755">*Step_count* auf Null zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-755">Reset *step_count* to zero.</span></span>
3.  <span data-ttu-id="4ea41-756">Wenn der vorherige Wert von *step_state* gewartet, Ausstehend oder geplant ist, senden Sie EC_STEP_COMPLETE mit *lParam1*  =  **true**.</span><span class="sxs-lookup"><span data-stu-id="4ea41-756">If the previous value of *step_state* was WAITING, PENDING, or SCHEDULED, send EC_STEP_COMPLETE with *lParam1* = **TRUE**.</span></span>

<span data-ttu-id="4ea41-757">Diese Prozeduren werden wie folgt aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="4ea41-757">Call these procedures as follows:</span></span>



| <span data-ttu-id="4ea41-758">Presenter-Nachricht oder-Methode</span><span class="sxs-lookup"><span data-stu-id="4ea41-758">Presenter message or method</span></span>                                                   | <span data-ttu-id="4ea41-759">Prozedur</span><span class="sxs-lookup"><span data-stu-id="4ea41-759">Procedure</span></span>           |
|-------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="4ea41-760">**MFVP_MESSAGE_STEP** Meldung</span><span class="sxs-lookup"><span data-stu-id="4ea41-760">**MFVP_MESSAGE_STEP** message</span></span>                                               | `PrepareFrameStep`  |
| <span data-ttu-id="4ea41-761">**MFVP_MESSAGE_STEP** Meldung</span><span class="sxs-lookup"><span data-stu-id="4ea41-761">**MFVP_MESSAGE_STEP** message</span></span>                                               | `CancelStep`        |
| [<span data-ttu-id="4ea41-762">**IMF clockstaatink:: onclockstart**</span><span class="sxs-lookup"><span data-stu-id="4ea41-762">**IMFClockStateSink::OnClockStart**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart)     | `StartFrameStep`    |
| [<span data-ttu-id="4ea41-763">**IMF clockstaatink:: onclockrestart**</span><span class="sxs-lookup"><span data-stu-id="4ea41-763">**IMFClockStateSink::OnClockRestart**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart) | `StartFrameStep`    |
| <span data-ttu-id="4ea41-764">[**IMF trackedsample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) -Rückruf</span><span class="sxs-lookup"><span data-stu-id="4ea41-764">[**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) callback</span></span>                         | `CompleteFrameStep` |
| [<span data-ttu-id="4ea41-765">**IMF clockstaatink:: onclockstopp**</span><span class="sxs-lookup"><span data-stu-id="4ea41-765">**IMFClockStateSink::OnClockStop**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop)       | `CancelFrameStep`   |
| [<span data-ttu-id="4ea41-766">**IMF clockstaatink:: onclock-trate**</span><span class="sxs-lookup"><span data-stu-id="4ea41-766">**IMFClockStateSink::OnClockSetRate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) | `CancelFrameStep`   |



 

<span data-ttu-id="4ea41-767">Im folgenden Flussdiagramm werden die Frame-Step-Prozeduren angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4ea41-767">The following flow chart shows the frame-stepping procedures.</span></span>

![Flussdiagramm mit den Pfaden, die mit dem MF \- -Nachrichten Schritt beginnen, \- und der MF \- \- -Nachricht processinputnotify und am Ende "State = Complete"](images/d9baaa67-a9b1-4e27-9a32-08a45b0677d3.gif)

## <a name="setting-the-presenter-on-the-evr"></a><span data-ttu-id="4ea41-769">Festlegen des Präsentators für den EVR</span><span class="sxs-lookup"><span data-stu-id="4ea41-769">Setting the Presenter on the EVR</span></span>

<span data-ttu-id="4ea41-770">Nachdem Sie den Presenter implementiert haben, besteht der nächste Schritt darin, den EVR für seine Verwendung zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="4ea41-770">After implementing the presenter, the next step is to configure the EVR to use it.</span></span>

### <a name="setting-the-presenter-in-directshow"></a><span data-ttu-id="4ea41-771">Festlegen des Präsentators in DirectShow</span><span class="sxs-lookup"><span data-stu-id="4ea41-771">Setting the Presenter in DirectShow</span></span>

<span data-ttu-id="4ea41-772">Legen Sie in einer DirectShow-Anwendung den Presenter wie folgt auf den EVR fest:</span><span class="sxs-lookup"><span data-stu-id="4ea41-772">In a DirectShow application, set the presenter on the EVR as follows:</span></span>

1.  <span data-ttu-id="4ea41-773">Erstellen Sie den EVR-Filter durch Aufrufen von **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="4ea41-773">Create the EVR filter by calling **CoCreateInstance**.</span></span> <span data-ttu-id="4ea41-774">Die CLSID ist **CLSID_EnhancedVideoRenderer**.</span><span class="sxs-lookup"><span data-stu-id="4ea41-774">The CLSID is **CLSID_EnhancedVideoRenderer**.</span></span>
2.  <span data-ttu-id="4ea41-775">Fügen Sie den EVR dem Filter Diagramm hinzu.</span><span class="sxs-lookup"><span data-stu-id="4ea41-775">Add the EVR to the filter graph.</span></span>
3.  <span data-ttu-id="4ea41-776">Erstellen Sie eine Instanz Ihres Präsentators.</span><span class="sxs-lookup"><span data-stu-id="4ea41-776">Create an instance of your presenter.</span></span> <span data-ttu-id="4ea41-777">Ihr Presenter kann die Standard-COM-Objekt Erstellung über **IClassFactory** unterstützen, dies ist jedoch nicht zwingend erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4ea41-777">Your presenter can support standard COM object creation through **IClassFactory**, but this is not mandatory.</span></span>
4.  <span data-ttu-id="4ea41-778">Fragen Sie den EVR-Filter nach der [**imsvideorenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="4ea41-778">Query the EVR filter for the [**IMFVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer) interface.</span></span>
5.  <span data-ttu-id="4ea41-779">[**Imfvideorenderer:: initializererderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-779">Call [**IMFVideoRenderer::InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).</span></span>

### <a name="setting-the-presenter-in-media-foundation"></a><span data-ttu-id="4ea41-780">Festlegen des Präsentators in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4ea41-780">Setting the Presenter in Media Foundation</span></span>

<span data-ttu-id="4ea41-781">In Media Foundation haben Sie mehrere Optionen, je nachdem, ob Sie die "EVR Media Sink" oder das "EVR Activation"-Objekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-781">In Media Foundation, you have several options, depending on whether you create the EVR media sink or the EVR activation object.</span></span> <span data-ttu-id="4ea41-782">Weitere Informationen zu Aktivierungs Objekten finden Sie unter [Activation Objects](activation-objects.md).</span><span class="sxs-lookup"><span data-stu-id="4ea41-782">For more information about activation objects, see [Activation Objects](activation-objects.md).</span></span>

<span data-ttu-id="4ea41-783">Führen Sie für die EVR-Medien Senke die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="4ea41-783">For the EVR media sink, do the following:</span></span>

1.  <span data-ttu-id="4ea41-784">Rufen Sie [**mfkreatevideorenderer**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) auf, um die Medien Senke zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-784">Call [**MFCreateVideoRenderer**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) to create the media sink.</span></span>
2.  <span data-ttu-id="4ea41-785">Erstellen Sie eine Instanz Ihres Präsentators.</span><span class="sxs-lookup"><span data-stu-id="4ea41-785">Create an instance of your presenter.</span></span>
3.  <span data-ttu-id="4ea41-786">Fragen Sie die EVR-Medien Senke für die [**imlvideorenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="4ea41-786">Query the EVR media sink for the [**IMFVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer) interface.</span></span>
4.  <span data-ttu-id="4ea41-787">[**Imfvideorenderer:: initializererderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-787">Call [**IMFVideoRenderer::InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).</span></span>

<span data-ttu-id="4ea41-788">Führen Sie für das EVR-Aktivierungs Objekt die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="4ea41-788">For the EVR activation object, do the following:</span></span>

1.  <span data-ttu-id="4ea41-789">Rufen Sie [**mfkreatevideorendereractivation**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) auf, um das Aktivierungs Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-789">Call [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) to create the activation object.</span></span>
2.  <span data-ttu-id="4ea41-790">Legen Sie eines der folgenden Attribute für das Aktivierungs Objekt fest:</span><span class="sxs-lookup"><span data-stu-id="4ea41-790">Set one of the following attributes on the activation object:</span></span> 

    | <span data-ttu-id="4ea41-791">Attribut</span><span class="sxs-lookup"><span data-stu-id="4ea41-791">Attribute</span></span>                                                                                                         | <span data-ttu-id="4ea41-792">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4ea41-792">Description</span></span>                                                                                                                                                                                                                               |
    |-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [<span data-ttu-id="4ea41-793">**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_ACTIVATE**</span><span class="sxs-lookup"><span data-stu-id="4ea41-793">**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_ACTIVATE**</span></span>](mf-activate-custom-video-presenter-activate-attribute.md) | <span data-ttu-id="4ea41-794">Zeiger auf ein Aktivierungs Objekt für den Presenter.</span><span class="sxs-lookup"><span data-stu-id="4ea41-794">Pointer to an activation object for the presenter.</span></span><br/> <span data-ttu-id="4ea41-795">Mit diesem Flag müssen Sie ein Aktivierungs Objekt für den Presenter bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-795">With this flag, you must provide an activation object for your presenter.</span></span> <span data-ttu-id="4ea41-796">Das Aktivierungs Objekt muss die [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="4ea41-796">The activation object must implement the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span><br/> |
    | [<span data-ttu-id="4ea41-797">**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_CLSID**</span><span class="sxs-lookup"><span data-stu-id="4ea41-797">**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_CLSID**</span></span>](mf-activate-custom-video-presenter-clsid-attribute.md)       | <span data-ttu-id="4ea41-798">CLSID des Präsentators.</span><span class="sxs-lookup"><span data-stu-id="4ea41-798">CLSID of the presenter.</span></span><br/> <span data-ttu-id="4ea41-799">Mit diesem Flag muss der Presenter eine Standard-COM-Objekt Erstellung über **IClassFactory** unterstützen.</span><span class="sxs-lookup"><span data-stu-id="4ea41-799">With this flag, your presenter must support standard COM object creation through **IClassFactory**.</span></span><br/>                                                                                         |

    

     

3.  <span data-ttu-id="4ea41-800">Legen Sie optional das [**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_FLAGS**](mf-activate-custom-video-presenter-flags-attribute.md) -Attribut für das Aktivierungs Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="4ea41-800">Optionally, set the [**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_FLAGS**](mf-activate-custom-video-presenter-flags-attribute.md) attribute on the activation object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4ea41-801">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4ea41-801">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ea41-802">Erweiterter Videorenderer</span><span class="sxs-lookup"><span data-stu-id="4ea41-802">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> <dt>

[<span data-ttu-id="4ea41-803">Evrpresenter-Beispiel</span><span class="sxs-lookup"><span data-stu-id="4ea41-803">EVRPresenter Sample</span></span>](evrpresenter-sample.md)
</dt> </dl>

 

 
