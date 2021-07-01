---
description: In diesem Artikel wird beschrieben, wie Sie eine benutzerdefinierte Präsentation für den erweiterten Videorenderer (EVR) schreiben.
ms.assetid: 1135b309-b158-4b70-9f76-5c93d0ad3250
title: Schreiben eines EVR-Presenters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 505ba7ec225ac5f1316ad4343a4e1058ff0b6cb8
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118775"
---
# <a name="how-to-write-an-evr-presenter"></a><span data-ttu-id="73809-103">Schreiben eines EVR-Presenters</span><span class="sxs-lookup"><span data-stu-id="73809-103">How to Write an EVR Presenter</span></span>

<span data-ttu-id="73809-104">In diesem Artikel wird beschrieben, wie Sie eine benutzerdefinierte Präsentation für den erweiterten Videorenderer (EVR) schreiben.</span><span class="sxs-lookup"><span data-stu-id="73809-104">This article describes how to write a custom presenter for the enhanced video renderer (EVR).</span></span> <span data-ttu-id="73809-105">Eine benutzerdefinierte Präsentation kann sowohl mit DirectShow als auch mit Media Foundation verwendet werden. Die Schnittstellen und das Objektmodell sind für beide Technologien identisch, obwohl die genaue Reihenfolge der Vorgänge variieren kann.</span><span class="sxs-lookup"><span data-stu-id="73809-105">A custom presenter can be used with both DirectShow and Media Foundation; the interfaces and object model are the same for both technologies, although the exact sequence of operations might vary.</span></span>

<span data-ttu-id="73809-106">Der Beispielcode in diesem Thema wird aus dem [EVRPresenter-Beispiel](evrpresenter-sample.md)angepasst, das im Windows SDK bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="73809-106">The example code in this topic is adapted from the [EVRPresenter Sample](evrpresenter-sample.md), which is provided in the Windows SDK.</span></span>

<span data-ttu-id="73809-107">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="73809-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="73809-108">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="73809-108">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="73809-109">Presenter-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="73809-109">Presenter Object Model</span></span>](#presenter-object-model)
    -   [<span data-ttu-id="73809-110">Datenfluss innerhalb der EVR</span><span class="sxs-lookup"><span data-stu-id="73809-110">Data Flow Inside the EVR</span></span>](#data-flow-inside-the-evr)
    -   [<span data-ttu-id="73809-111">Presenter States</span><span class="sxs-lookup"><span data-stu-id="73809-111">Presenter States</span></span>](#presenter-states)
    -   [<span data-ttu-id="73809-112">Presenter-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="73809-112">Presenter Interfaces</span></span>](#presenter-interfaces)
    -   [<span data-ttu-id="73809-113">Implementieren von IMPLEMENTVIDEODeviceID</span><span class="sxs-lookup"><span data-stu-id="73809-113">Implementing IMFVideoDeviceID</span></span>](#implementing-imfvideodeviceid)
    -   [<span data-ttu-id="73809-114">Implementieren vonTOPTOPOLOGYServiceLookupClient</span><span class="sxs-lookup"><span data-stu-id="73809-114">Implementing IMFTopologyServiceLookupClient</span></span>](#implementing-imftopologyservicelookupclient)
    -   [<span data-ttu-id="73809-115">Implementieren von IMPLEMENTVIDEOPresenter</span><span class="sxs-lookup"><span data-stu-id="73809-115">Implementing IMFVideoPresenter</span></span>](#implementing-imfvideopresenter)
    -   [<span data-ttu-id="73809-116">Implementieren von IMPLEMENTClockStateSink</span><span class="sxs-lookup"><span data-stu-id="73809-116">Implementing IMFClockStateSink</span></span>](#implementing-imfclockstatesink)
    -   [<span data-ttu-id="73809-117">Implementieren von IMPLEMENTRATESupport</span><span class="sxs-lookup"><span data-stu-id="73809-117">Implementing IMFRateSupport</span></span>](#implementing-imfratesupport)
    -   [<span data-ttu-id="73809-118">Senden von Ereignissen an die EVR</span><span class="sxs-lookup"><span data-stu-id="73809-118">Sending Events to the EVR</span></span>](#sending-events-to-the-evr)
-   [<span data-ttu-id="73809-119">Aushandeln von Formaten</span><span class="sxs-lookup"><span data-stu-id="73809-119">Negotiating Formats</span></span>](#negotiating-formats)
-   [<span data-ttu-id="73809-120">Verwalten des Direct3D-Geräts</span><span class="sxs-lookup"><span data-stu-id="73809-120">Managing the Direct3D Device</span></span>](#managing-the-direct3d-device)
    -   [<span data-ttu-id="73809-121">Zuordnen von Direct3D-Oberflächen</span><span class="sxs-lookup"><span data-stu-id="73809-121">Allocating Direct3D Surfaces</span></span>](#allocating-direct3d-surfaces)
    -   [<span data-ttu-id="73809-122">Überwachungsbeispiele</span><span class="sxs-lookup"><span data-stu-id="73809-122">Tracking Samples</span></span>](#tracking-samples)
-   [<span data-ttu-id="73809-123">Verarbeiten der Ausgabe</span><span class="sxs-lookup"><span data-stu-id="73809-123">Processing Output</span></span>](#processing-output)
    -   [<span data-ttu-id="73809-124">Neumalen von Frames</span><span class="sxs-lookup"><span data-stu-id="73809-124">Repainting Frames</span></span>](#repainting-frames)
    -   [<span data-ttu-id="73809-125">Zeitplanungsbeispiele</span><span class="sxs-lookup"><span data-stu-id="73809-125">Scheduling Samples</span></span>](#scheduling-samples)
    -   [<span data-ttu-id="73809-126">Präsentieren von Beispielen</span><span class="sxs-lookup"><span data-stu-id="73809-126">Presenting Samples</span></span>](#presenting-samples)
    -   [<span data-ttu-id="73809-127">Quell- und Zielrechtecke</span><span class="sxs-lookup"><span data-stu-id="73809-127">Source and Destination Rectangles</span></span>](#source-and-destination-rectangles)
    -   [<span data-ttu-id="73809-128">Ende des Streams</span><span class="sxs-lookup"><span data-stu-id="73809-128">End of Stream</span></span>](#end-of-stream)
-   [<span data-ttu-id="73809-129">Einzelschritt im Rahmen</span><span class="sxs-lookup"><span data-stu-id="73809-129">Frame Stepping</span></span>](#frame-stepping)
    -   [<span data-ttu-id="73809-130">Implementieren von Frameschritten</span><span class="sxs-lookup"><span data-stu-id="73809-130">Implementing Frame Stepping</span></span>](#implementing-frame-stepping)
-   [<span data-ttu-id="73809-131">Festlegen des Presenters auf der EVR</span><span class="sxs-lookup"><span data-stu-id="73809-131">Setting the Presenter on the EVR</span></span>](#setting-the-presenter-on-the-evr)
    -   [<span data-ttu-id="73809-132">Festlegen der Präsentation in DirectShow</span><span class="sxs-lookup"><span data-stu-id="73809-132">Setting the Presenter in DirectShow</span></span>](#setting-the-presenter-in-directshow)
    -   [<span data-ttu-id="73809-133">Festlegen des Presenters in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="73809-133">Setting the Presenter in Media Foundation</span></span>](#setting-the-presenter-in-media-foundation)
-   [<span data-ttu-id="73809-134">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="73809-134">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="73809-135">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="73809-135">Prerequisites</span></span>

<span data-ttu-id="73809-136">Bevor Sie eine benutzerdefinierte Präsentation schreiben, sollten Sie mit den folgenden Technologien vertraut sein:</span><span class="sxs-lookup"><span data-stu-id="73809-136">Before writing a custom presenter, you should be familiar with the following technologies:</span></span>

-   <span data-ttu-id="73809-137">Der erweiterte Videorenderer.</span><span class="sxs-lookup"><span data-stu-id="73809-137">The enhanced video renderer.</span></span> <span data-ttu-id="73809-138">Weitere Informationen finden Sie unter [Erweiterter Videorenderer.](enhanced-video-renderer.md)</span><span class="sxs-lookup"><span data-stu-id="73809-138">See [Enhanced Video Renderer](enhanced-video-renderer.md).</span></span>
-   <span data-ttu-id="73809-139">Direct3D-Grafiken.</span><span class="sxs-lookup"><span data-stu-id="73809-139">Direct3D graphics.</span></span> <span data-ttu-id="73809-140">Sie müssen keine 3D-Grafiken verstehen, um eine Präsentation zu schreiben, aber Sie müssen wissen, wie Sie ein Direct3D-Gerät erstellen und Direct3D-Oberflächen verwalten.</span><span class="sxs-lookup"><span data-stu-id="73809-140">You don't need to understand 3-D graphics to write a presenter, but you must know how to create a Direct3D device and manage Direct3D surfaces.</span></span> <span data-ttu-id="73809-141">Wenn Sie nicht mit Direct3D vertraut sind, lesen Sie die Abschnitte "Direct3D-Geräte" und "Direct3D-Ressourcen" in der DirectX Graphics SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="73809-141">If you aren't familiar with Direct3D, read the sections "Direct3D Devices" and "Direct3D Resources" in the DirectX Graphics SDK documentation.</span></span>
-   <span data-ttu-id="73809-142">DirectShow-Filterdiagramme oder die Media Foundation Pipeline, je nachdem, welche Technologie Ihre Anwendung zum Rendern von Videos verwendet.</span><span class="sxs-lookup"><span data-stu-id="73809-142">DirectShow filter graphs or the Media Foundation pipeline, depending on which technology your application will use to render video.</span></span>
-   <span data-ttu-id="73809-143">[Media Foundation Transformiert](media-foundation-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="73809-143">[Media Foundation Transforms](media-foundation-transforms.md).</span></span> <span data-ttu-id="73809-144">Der EVR-Mixer ist eine Media Foundation-Transformation, und der Moderator ruft Methoden direkt auf dem Mixer auf.</span><span class="sxs-lookup"><span data-stu-id="73809-144">The EVR mixer is a Media Foundation transform, and the presenter calls methods directly on the mixer.</span></span>
-   <span data-ttu-id="73809-145">Implementieren von COM-Objekten.</span><span class="sxs-lookup"><span data-stu-id="73809-145">Implementing COM objects.</span></span> <span data-ttu-id="73809-146">Der Presenter ist ein Prozess-COM-Objekt mit Freethreading.</span><span class="sxs-lookup"><span data-stu-id="73809-146">The presenter is an in-process, free-threaded COM object.</span></span>

## <a name="presenter-object-model"></a><span data-ttu-id="73809-147">Presenter-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="73809-147">Presenter Object Model</span></span>

<span data-ttu-id="73809-148">Dieser Abschnitt enthält eine Übersicht über das Presenter-Objektmodell und die Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="73809-148">This section contains an overview the presenter object model and interfaces.</span></span>

### <a name="data-flow-inside-the-evr"></a><span data-ttu-id="73809-149">Datenfluss innerhalb der EVR</span><span class="sxs-lookup"><span data-stu-id="73809-149">Data Flow Inside the EVR</span></span>

<span data-ttu-id="73809-150">Die EVR verwendet zwei Plug-In-Komponenten zum Rendern von Videos: den *Mixer* und den *Presenter*.</span><span class="sxs-lookup"><span data-stu-id="73809-150">The EVR uses two plug-in components to render video: the *mixer* and the *presenter*.</span></span> <span data-ttu-id="73809-151">Der Mixer kombiniert die Videostreams und deinterlaciert das Video bei Bedarf.</span><span class="sxs-lookup"><span data-stu-id="73809-151">The mixer blends the video streams and deinterlaces the video if needed.</span></span> <span data-ttu-id="73809-152">Die Moderatorin zeichnet (oder *präsentiert*) das Video auf der Anzeige und plant, wann jeder Frame gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="73809-152">The presenter draws (or *presents*) the video onto the display and schedules when each frame is drawn.</span></span> <span data-ttu-id="73809-153">Anwendungen können eines dieser Objekte durch eine benutzerdefinierte Implementierung ersetzen.</span><span class="sxs-lookup"><span data-stu-id="73809-153">Applications can replace either of these objects with a custom implementation.</span></span>

<span data-ttu-id="73809-154">Die EVR verfügt über einen oder mehrere Eingabestreams, und der Mixer verfügt über eine entsprechende Anzahl von Eingabestreams.</span><span class="sxs-lookup"><span data-stu-id="73809-154">The EVR has one or more input streams, and the mixer has a corresponding number of input streams.</span></span> <span data-ttu-id="73809-155">Stream 0 ist immer der *Verweisstream.*</span><span class="sxs-lookup"><span data-stu-id="73809-155">Stream 0 is always the *reference stream*.</span></span> <span data-ttu-id="73809-156">Die anderen Streams sind *Unterstreams,* die der Mixer alpha-blendet in den Verweisstream einblendet.</span><span class="sxs-lookup"><span data-stu-id="73809-156">The other streams are *substreams*, which the mixer alpha-blends onto the reference stream.</span></span> <span data-ttu-id="73809-157">Der Verweisstream bestimmt die Masterbildrate für das zusammengesetzte Video.</span><span class="sxs-lookup"><span data-stu-id="73809-157">The reference stream determines the master frame-rate for the composited video.</span></span> <span data-ttu-id="73809-158">Für jeden Verweisrahmen nimmt der Mixer den neuesten Frame aus jedem Unterstream, blendet sie alpha-blendend in den Referenzrahmen ein und gibt einen einzelnen zusammengesetzten Frame aus.</span><span class="sxs-lookup"><span data-stu-id="73809-158">For each reference frame, the mixer takes the most recent frame from each substream, alpha-blends them onto the reference frame, and outputs a single composited frame.</span></span> <span data-ttu-id="73809-159">Der Mixer führt bei Bedarf auch Deinterlacing und Farbkonvertierung von YUV in RGB durch.</span><span class="sxs-lookup"><span data-stu-id="73809-159">The mixer also performs deinterlacing and color conversion from YUV to RGB if needed.</span></span> <span data-ttu-id="73809-160">Die EVR fügt den Mixer immer in die Videopipeline ein, unabhängig von der Anzahl der Eingabestreams oder dem Videoformat.</span><span class="sxs-lookup"><span data-stu-id="73809-160">The EVR always inserts the mixer into the video pipeline, regardless of the number of input streams or the video format.</span></span> <span data-ttu-id="73809-161">Die folgende Abbildung veranschaulicht diesen Prozess.</span><span class="sxs-lookup"><span data-stu-id="73809-161">The following image illustrates this process.</span></span>

![Diagramm, das den Verweisstream und den Unterstream zeigt, der auf den Mixer zeigt, der auf die Darstellung zeigt, die auf die Anzeige zeigt](images/459338c4-cff8-4d20-bffd-ff1cbbe6f332.gif)

<span data-ttu-id="73809-163">Die Moderatorin führt die folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="73809-163">The presenter performs the following tasks:</span></span>

-   <span data-ttu-id="73809-164">Legt das Ausgabeformat für den Mixer fest.</span><span class="sxs-lookup"><span data-stu-id="73809-164">Sets the output format on the mixer.</span></span> <span data-ttu-id="73809-165">Bevor das Streaming beginnt, legt die Moderatorin einen Medientyp für den Ausgabestream des Mixers fest.</span><span class="sxs-lookup"><span data-stu-id="73809-165">Before streaming begins, the presenter sets a media type on the mixer's output stream.</span></span> <span data-ttu-id="73809-166">Dieser Medientyp definiert das Format des zusammengesetzten Bilds.</span><span class="sxs-lookup"><span data-stu-id="73809-166">This media type defines the format of the composited image.</span></span>
-   <span data-ttu-id="73809-167">Erstellt das Direct3D-Gerät.</span><span class="sxs-lookup"><span data-stu-id="73809-167">Creates the Direct3D device.</span></span>
-   <span data-ttu-id="73809-168">Ordnet Direct3D-Oberflächen zu.</span><span class="sxs-lookup"><span data-stu-id="73809-168">Allocates Direct3D surfaces.</span></span> <span data-ttu-id="73809-169">Der Mixer blitt die zusammengesetzten Frames auf diese Oberflächen.</span><span class="sxs-lookup"><span data-stu-id="73809-169">The mixer blits the composited frames onto these surfaces.</span></span>
-   <span data-ttu-id="73809-170">Ruft die Ausgabe des Mixers ab.</span><span class="sxs-lookup"><span data-stu-id="73809-170">Gets the output from the mixer.</span></span>
-   <span data-ttu-id="73809-171">Zeitpläne, wenn die Frames angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="73809-171">Schedules when the frames are presented.</span></span> <span data-ttu-id="73809-172">Die EVR stellt die Präsentationsuhr bereit, und der Moderator plant Frames entsprechend dieser Uhr.</span><span class="sxs-lookup"><span data-stu-id="73809-172">The EVR provides the presentation clock, and the presenter schedules frames according to this clock.</span></span>
-   <span data-ttu-id="73809-173">Stellt jeden Frame mit Direct3D dar.</span><span class="sxs-lookup"><span data-stu-id="73809-173">Presents each frame using Direct3D.</span></span>
-   <span data-ttu-id="73809-174">Führt die Einzelschritt- und Bereinigungsschritte des Frames aus.</span><span class="sxs-lookup"><span data-stu-id="73809-174">Performs frame stepping and scrubbing.</span></span>

### <a name="presenter-states"></a><span data-ttu-id="73809-175">Presenter States</span><span class="sxs-lookup"><span data-stu-id="73809-175">Presenter States</span></span>

<span data-ttu-id="73809-176">Der Presenter befindet sich jederzeit in einem der folgenden Zustände:</span><span class="sxs-lookup"><span data-stu-id="73809-176">At any time, the presenter is in one of following states:</span></span>

-   <span data-ttu-id="73809-177">*Gestartet.*</span><span class="sxs-lookup"><span data-stu-id="73809-177">*Started*.</span></span> <span data-ttu-id="73809-178">Die Präsentationsuhr der EVR wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="73809-178">The EVR's presentation clock is running.</span></span> <span data-ttu-id="73809-179">Die Moderatorin plant Videoframes für die Präsentation, sobald sie eintreffen.</span><span class="sxs-lookup"><span data-stu-id="73809-179">The presenter schedules video frames for presentation as they arrive.</span></span>
-   <span data-ttu-id="73809-180">*Angehalten.*</span><span class="sxs-lookup"><span data-stu-id="73809-180">*Paused*.</span></span> <span data-ttu-id="73809-181">Die Präsentationsuhr wird angehalten.</span><span class="sxs-lookup"><span data-stu-id="73809-181">The presentation clock is suspended.</span></span> <span data-ttu-id="73809-182">Der Presenter stellt keine neuen Beispiele vor, behält aber seine Warteschlange mit geplanten Stichproben bei.</span><span class="sxs-lookup"><span data-stu-id="73809-182">The presenter does not present any new samples but maintains its queue of scheduled samples.</span></span> <span data-ttu-id="73809-183">Wenn neue Beispiele empfangen werden, fügt die Moderatorin sie der Warteschlange hinzu.</span><span class="sxs-lookup"><span data-stu-id="73809-183">If new samples are received, the presenter adds them to the queue.</span></span>
-   <span data-ttu-id="73809-184">*Stopped*(Beendet): Dies ist der anfängliche Status des Kanals nach seiner Erstellung (es sei denn, im Portal wurde das automatische Starten gewählt).</span><span class="sxs-lookup"><span data-stu-id="73809-184">*Stopped*.</span></span> <span data-ttu-id="73809-185">Die Präsentationsuhr wird beendet.</span><span class="sxs-lookup"><span data-stu-id="73809-185">The presentation clock is stopped.</span></span> <span data-ttu-id="73809-186">Die Präsentation verwirft alle geplanten Beispiele.</span><span class="sxs-lookup"><span data-stu-id="73809-186">The presenter discards any samples that were scheduled.</span></span>
-   <span data-ttu-id="73809-187">*Fahren Sie herunter.*</span><span class="sxs-lookup"><span data-stu-id="73809-187">*Shut down*.</span></span> <span data-ttu-id="73809-188">Die Präsentation gibt alle Ressourcen frei, die sich auf das Streaming beziehen, z. B. Direct3D-Oberflächen.</span><span class="sxs-lookup"><span data-stu-id="73809-188">The presenter releases any resources related to streaming, such as Direct3D surfaces.</span></span> <span data-ttu-id="73809-189">Dies ist der Anfangszustand des Moderators und der endgültige Zustand, bevor der Presenter zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="73809-189">This is the presenter's initial state, and the final state before the presenter is destroyed.</span></span>

<span data-ttu-id="73809-190">Im Beispielcode in diesem Thema wird der Darstellungszustand durch eine -Enumeration dargestellt:</span><span class="sxs-lookup"><span data-stu-id="73809-190">In the example code in this topic, the presenter state is represented by an enumeration:</span></span>


```C++
enum RENDER_STATE
{
    RENDER_STATE_STARTED = 1,
    RENDER_STATE_STOPPED,
    RENDER_STATE_PAUSED,
    RENDER_STATE_SHUTDOWN,  // Initial state.
};
```



<span data-ttu-id="73809-191">Einige Vorgänge sind ungültig, während sich die Darstellung im Zustand "Herunterfahren" befindet.</span><span class="sxs-lookup"><span data-stu-id="73809-191">Some operations are not valid while the presenter is in the shutdown state.</span></span> <span data-ttu-id="73809-192">Der Beispielcode überprüft diesen Zustand, indem eine Hilfsmethode aufgerufen wird:</span><span class="sxs-lookup"><span data-stu-id="73809-192">The example code checks for this state by calling a helper method:</span></span>


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



### <a name="presenter-interfaces"></a><span data-ttu-id="73809-193">Presenter-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="73809-193">Presenter Interfaces</span></span>

<span data-ttu-id="73809-194">Ein Presenter ist erforderlich, um die folgenden Schnittstellen zu implementieren:</span><span class="sxs-lookup"><span data-stu-id="73809-194">A presenter is required to implement the following interfaces:</span></span>



| <span data-ttu-id="73809-195">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="73809-195">Interface</span></span>                                                                | <span data-ttu-id="73809-196">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="73809-196">Description</span></span>                                                                                                                                                         |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="73809-197">**ÜBER DIE UHRClockStateSink**</span><span class="sxs-lookup"><span data-stu-id="73809-197">**IMFClockStateSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)                           | <span data-ttu-id="73809-198">Benachrichtigt den Moderator, wenn sich der Zustand der EVR-Uhr ändert.</span><span class="sxs-lookup"><span data-stu-id="73809-198">Notifies the presenter when the EVR's clock changes state.</span></span> <span data-ttu-id="73809-199">Weitere Informationen finden Sie unter [Implementieren von IMPLEMENTClockStateSink.](#implementing-imfclockstatesink)</span><span class="sxs-lookup"><span data-stu-id="73809-199">See [Implementing IMFClockStateSink](#implementing-imfclockstatesink).</span></span>                                   |
| [<span data-ttu-id="73809-200">**ÜBER DIE NSDGET-DIENST**</span><span class="sxs-lookup"><span data-stu-id="73809-200">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                                   | <span data-ttu-id="73809-201">Bietet der Anwendung und anderen Komponenten in der Pipeline eine Möglichkeit, Schnittstellen vom Präsentieren zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="73809-201">Provides a way for the application and other components in the pipeline to get interfaces from the presenter.</span></span>                                                       |
| [<span data-ttu-id="73809-202">**TOPOLOGYServiceLookupClient**</span><span class="sxs-lookup"><span data-stu-id="73809-202">**IMFTopologyServiceLookupClient**</span></span>](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) | <span data-ttu-id="73809-203">Ermöglicht es der Moderatorin, Schnittstellen aus der EVR oder dem Mixer zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="73809-203">Enables the presenter to get interfaces from the EVR or the mixer.</span></span> <span data-ttu-id="73809-204">Weitere Informationen [finden Sie unter ImplementingTOPOLOGYTopologyServiceLookupClient (Implementieren vonTOPOLOGYTopologyServiceLookupClient).](#implementing-imftopologyservicelookupclient)</span><span class="sxs-lookup"><span data-stu-id="73809-204">See [Implementing IMFTopologyServiceLookupClient](#implementing-imftopologyservicelookupclient).</span></span> |
| [<span data-ttu-id="73809-205">**BESENVIDEODeviceID**</span><span class="sxs-lookup"><span data-stu-id="73809-205">**IMFVideoDeviceID**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)                             | <span data-ttu-id="73809-206">Stellt sicher, dass der Presenter und der Mixer kompatible Technologien verwenden.</span><span class="sxs-lookup"><span data-stu-id="73809-206">Ensures that the presenter and the mixer use compatible technologies.</span></span> <span data-ttu-id="73809-207">Weitere Informationen [finden Sie unter ImplementingUNGVIDEODeviceID](#implementing-imfvideodeviceid).</span><span class="sxs-lookup"><span data-stu-id="73809-207">See [Implementing IMFVideoDeviceID](#implementing-imfvideodeviceid).</span></span>                          |
| [<span data-ttu-id="73809-208">**VERERBUNGVideoPresenter**</span><span class="sxs-lookup"><span data-stu-id="73809-208">**IMFVideoPresenter**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopresenter)                           | <span data-ttu-id="73809-209">Verarbeitet Nachrichten vom EVR.</span><span class="sxs-lookup"><span data-stu-id="73809-209">Processes messages from the EVR.</span></span> <span data-ttu-id="73809-210">Weitere Informationen [finden Sie unter Implementieren vonPRESENTVideoPresenter](#implementing-imfvideopresenter).</span><span class="sxs-lookup"><span data-stu-id="73809-210">See [Implementing IMFVideoPresenter](#implementing-imfvideopresenter).</span></span>                                                             |



 

<span data-ttu-id="73809-211">Die folgenden Schnittstellen sind optional:</span><span class="sxs-lookup"><span data-stu-id="73809-211">The following interfaces are optional:</span></span>



| <span data-ttu-id="73809-212">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="73809-212">Interface</span></span>                                                | <span data-ttu-id="73809-213">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="73809-213">Description</span></span>                                                                                                                                                               |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="73809-214">**IEVRTrustedVideoPlugin**</span><span class="sxs-lookup"><span data-stu-id="73809-214">**IEVRTrustedVideoPlugin**</span></span>](/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin) | <span data-ttu-id="73809-215">Ermöglicht es dem Moderator, mit geschützten Medien zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="73809-215">Enables the presenter to work with protected media.</span></span> <span data-ttu-id="73809-216">Implementieren Sie diese Schnittstelle, wenn ihr Presenter eine vertrauenswürdige Komponente ist, die für die Arbeit im geschützten Medienpfad (PMP) konzipiert ist.</span><span class="sxs-lookup"><span data-stu-id="73809-216">Implement this interface if your presenter is a trusted component designed to work in the protected media path (PMP).</span></span> |
| [<span data-ttu-id="73809-217">**VERRATRateSupport**</span><span class="sxs-lookup"><span data-stu-id="73809-217">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)                 | <span data-ttu-id="73809-218">Gibt den Bereich der Wiedergaberaten an, die der Presenter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="73809-218">Reports the range of playback rates that the presenter supports.</span></span> <span data-ttu-id="73809-219">Weitere Informationen [finden Sie unter Implementieren von DURCHSTRateSupport.](#implementing-imfratesupport)</span><span class="sxs-lookup"><span data-stu-id="73809-219">See [Implementing IMFRateSupport](#implementing-imfratesupport).</span></span>                                         |
| [<span data-ttu-id="73809-220">**CITRIXVideoPositionMapper**</span><span class="sxs-lookup"><span data-stu-id="73809-220">**IMFVideoPositionMapper**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper) | <span data-ttu-id="73809-221">Ordnet Koordinaten auf dem Ausgabevideoframe Koordinaten auf dem Eingabevideoframe zu.</span><span class="sxs-lookup"><span data-stu-id="73809-221">Maps coordinates on the output video frame to coordinates on the input video frame.</span></span>                                                                                       |
| [<span data-ttu-id="73809-222">**IQualProp**</span><span class="sxs-lookup"><span data-stu-id="73809-222">**IQualProp**</span></span>](/previous-versions/windows/desktop/api/amvideo/nn-amvideo-iqualprop)                         | <span data-ttu-id="73809-223">Meldet Leistungsinformationen.</span><span class="sxs-lookup"><span data-stu-id="73809-223">Reports performance information.</span></span> <span data-ttu-id="73809-224">Der EVR verwendet diese Informationen für die Verwaltung der Qualitätskontrolle.</span><span class="sxs-lookup"><span data-stu-id="73809-224">The EVR uses this information for quality-control management.</span></span> <span data-ttu-id="73809-225">Diese Schnittstelle ist im DirectShow SDK dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="73809-225">This interface is documented in the DirectShow SDK.</span></span>                        |



 

<span data-ttu-id="73809-226">Sie können auch Schnittstellen für die Anwendung bereitstellen, um mit dem Moderator zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="73809-226">You can also provide interfaces for the application to communicate with the presenter.</span></span> <span data-ttu-id="73809-227">Die Standard-Moderatorin implementiert zu diesem Zweck [**die BENUTZEROBERFLÄCHEVideoDisplayControl-Schnittstelle.**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol)</span><span class="sxs-lookup"><span data-stu-id="73809-227">The standard presenter implements the [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface for this purpose.</span></span> <span data-ttu-id="73809-228">Sie können diese Schnittstelle implementieren oder eine eigene definieren.</span><span class="sxs-lookup"><span data-stu-id="73809-228">You can implement this interface or define your own.</span></span> <span data-ttu-id="73809-229">Die Anwendung ruft Schnittstellen aus dem Presenter ab, indem [**sie AUFTGETService::GetService in**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) der EVR aufruft.</span><span class="sxs-lookup"><span data-stu-id="73809-229">The application obtains interfaces from the presenter by calling [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the EVR.</span></span> <span data-ttu-id="73809-230">Wenn die Dienst-GUID **MR_VIDEO_RENDER_SERVICE** ist, übergibt der EVR die **GetService-Anforderung** an den Moderator.</span><span class="sxs-lookup"><span data-stu-id="73809-230">When the service GUID is **MR_VIDEO_RENDER_SERVICE**, the EVR passes the **GetService** request to the presenter.</span></span>

### <a name="implementing-imfvideodeviceid"></a><span data-ttu-id="73809-231">Implementieren von NNTVideoDeviceID</span><span class="sxs-lookup"><span data-stu-id="73809-231">Implementing IMFVideoDeviceID</span></span>

<span data-ttu-id="73809-232">Die [**BENUTZEROBERFLÄCHEVideoDeviceID-Schnittstelle**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) enthält eine Methode, [**GetDeviceID,**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid)die eine Geräte-GUID zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="73809-232">The [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) interface contains one method, [**GetDeviceID**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid), which returns a device GUID.</span></span> <span data-ttu-id="73809-233">Die Geräte-GUID stellt sicher, dass der Moderator und der Mixer kompatible Technologien verwenden.</span><span class="sxs-lookup"><span data-stu-id="73809-233">The device GUID ensures that the presenter and the mixer use compatible technologies.</span></span> <span data-ttu-id="73809-234">Wenn die Geräte-GUIDs nicht übereinstimmen, kann die EVR nicht initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="73809-234">If the device GUIDs do not match, the EVR fails to initialize.</span></span>

<span data-ttu-id="73809-235">Sowohl der Standardmixer als auch der Presenter verwenden Direct3D 9, und die Geräte-GUID entspricht **IID_IDirect3DDevice9.**</span><span class="sxs-lookup"><span data-stu-id="73809-235">The standard mixer and presenter both use Direct3D 9, with the device GUID equal to **IID_IDirect3DDevice9**.</span></span> <span data-ttu-id="73809-236">Wenn Sie Ihre benutzerdefinierte Präsentation mit dem Standardmixer verwenden möchten, muss die Geräte-GUID des Moderators **IID_IDirect3DDevice9.**</span><span class="sxs-lookup"><span data-stu-id="73809-236">If you intend to use your custom presenter with the standard mixer, the presenter's device GUID must be **IID_IDirect3DDevice9**.</span></span> <span data-ttu-id="73809-237">Wenn Sie beide Komponenten ersetzen, können Sie eine neue Geräte-GUID definieren.</span><span class="sxs-lookup"><span data-stu-id="73809-237">If you replace both components, you could define a new device GUID.</span></span> <span data-ttu-id="73809-238">Im weiteren Verlauf dieses Artikels wird davon ausgegangen, dass der Moderator Direct3D 9 verwendet.</span><span class="sxs-lookup"><span data-stu-id="73809-238">For the remainder of this article, it is assumed that the presenter uses Direct3D 9.</span></span> <span data-ttu-id="73809-239">Hier ist die Standardimplementierung [**von GetDeviceID:**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid)</span><span class="sxs-lookup"><span data-stu-id="73809-239">Here is the standard implementation of [**GetDeviceID**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid):</span></span>


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



<span data-ttu-id="73809-240">Die Methode sollte auch dann erfolgreich sein, wenn der Presenter heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="73809-240">The method should succeed even when the presenter is shut down.</span></span>

### <a name="implementing-imftopologyservicelookupclient"></a><span data-ttu-id="73809-241">Implementieren vonTOPOLOGYTopologyServiceLookupClient</span><span class="sxs-lookup"><span data-stu-id="73809-241">Implementing IMFTopologyServiceLookupClient</span></span>

<span data-ttu-id="73809-242">Die [**SCHNITTSTELLETOPOLOGYTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) ermöglicht es dem Moderator, Schnittstellenzeiger wie folgt vom EVR und vom Mixer zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="73809-242">The [**IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) interface enables the presenter to get interface pointers from the EVR and from the mixer as follows:</span></span>

1.  <span data-ttu-id="73809-243">Wenn der EVR den Presenter initialisiert, ruft er [**dieTOPOLOGYTopologyServiceLookupClient::InitServicePointers-Methode**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) des Presenters auf.</span><span class="sxs-lookup"><span data-stu-id="73809-243">When the EVR initializes the presenter, it calls the presenter's [**IMFTopologyServiceLookupClient::InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) method.</span></span> <span data-ttu-id="73809-244">Das -Argument ist ein Zeiger auf [**dieTOPOLOGYServiceLookup-Schnittstelle**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookup) des EVR.</span><span class="sxs-lookup"><span data-stu-id="73809-244">The argument is a pointer to the EVR's [**IMFTopologyServiceLookup**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookup) interface.</span></span>
2.  <span data-ttu-id="73809-245">Die Moderatorin ruft [**DENTOPOLOGYServiceLookup::LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) auf, um Schnittstellenzeiger entweder vom EVR oder vom Mixer zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="73809-245">The presenter calls [**IMFTopologyServiceLookup::LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) to get interface pointers from either the EVR or the mixer.</span></span>

<span data-ttu-id="73809-246">Die [**LookupService-Methode**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) ähnelt der [**METHODE "GEGETService::GetService".**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice)</span><span class="sxs-lookup"><span data-stu-id="73809-246">The [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) method is similar to the [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) method.</span></span> <span data-ttu-id="73809-247">Beide Methoden nehmen eine Dienst-GUID und eine Schnittstellen-ID (IID) als Eingabe an, **lookupService** gibt jedoch ein Array von Schnittstellenzeigern zurück, während **GetService** einen einzelnen Zeiger zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="73809-247">Both methods take a service GUID and an interface identifier (IID) as input, but **LookupService** returns an array of interface pointers, while **GetService** returns a single pointer.</span></span> <span data-ttu-id="73809-248">In der Praxis können Sie die Arraygröße jedoch immer auf 1 festlegen.</span><span class="sxs-lookup"><span data-stu-id="73809-248">In practice, however, you can always set the array size to 1.</span></span> <span data-ttu-id="73809-249">Das abgefragte Objekt hängt von der Dienst-GUID ab:</span><span class="sxs-lookup"><span data-stu-id="73809-249">The object queried depends on the service GUID:</span></span>

-   <span data-ttu-id="73809-250">Wenn die Dienst-GUID **MR_VIDEO_RENDER_SERVICE** ist, wird die EVR abgefragt.</span><span class="sxs-lookup"><span data-stu-id="73809-250">If the service GUID is **MR_VIDEO_RENDER_SERVICE**, the EVR is queried.</span></span>
-   <span data-ttu-id="73809-251">Wenn die Dienst-GUID **MR_VIDEO_MIXER_SERVICE** ist, wird der Mixer abgefragt.</span><span class="sxs-lookup"><span data-stu-id="73809-251">If the service GUID is **MR_VIDEO_MIXER_SERVICE**, the mixer is queried.</span></span>

<span data-ttu-id="73809-252">Verwenden Sie in Ihrer [**Implementierung von InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers)die folgenden Schnittstellen aus der EVR:</span><span class="sxs-lookup"><span data-stu-id="73809-252">In your implementation of [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers), get the following interfaces from the EVR:</span></span>



| <span data-ttu-id="73809-253">EVR-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="73809-253">EVR Interface</span></span>                                | <span data-ttu-id="73809-254">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="73809-254">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="73809-255">**IMediaEventSink**</span><span class="sxs-lookup"><span data-stu-id="73809-255">**IMediaEventSink**</span></span>](/windows/win32/api/strmif/nn-strmif-imediaeventsink) | <span data-ttu-id="73809-256">Bietet dem Moderator eine Möglichkeit, Nachrichten an die EVR zu senden.</span><span class="sxs-lookup"><span data-stu-id="73809-256">Provides a way for the presenter to send messages to the EVR.</span></span> <span data-ttu-id="73809-257">Diese Schnittstelle wird im DirectShow SDK definiert, sodass die Nachrichten dem Muster für DirectShow-Ereignisse folgen, nicht Media Foundation Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="73809-257">This interface is defined in the DirectShow SDK, so the messages follow the pattern for DirectShow events, not Media Foundation events.</span></span><br/>                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="73809-258">**DEADClock**</span><span class="sxs-lookup"><span data-stu-id="73809-258">**IMFClock**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfclock)                 | <span data-ttu-id="73809-259">Stellt die Uhr des EVR dar.</span><span class="sxs-lookup"><span data-stu-id="73809-259">Represents the EVR's clock.</span></span> <span data-ttu-id="73809-260">Die Präsentation verwendet diese Schnittstelle, um Beispiele für die Präsentation zu planen.</span><span class="sxs-lookup"><span data-stu-id="73809-260">The presenter uses this interface to schedule samples for presentation.</span></span> <span data-ttu-id="73809-261">Die EVR kann ohne Uhr ausgeführt werden, sodass diese Schnittstelle möglicherweise nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="73809-261">The EVR can run without a clock, so this interface might not be available.</span></span> <span data-ttu-id="73809-262">Wenn nicht, ignorieren Sie den Fehlercode aus [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice).</span><span class="sxs-lookup"><span data-stu-id="73809-262">If not, ignore the error code from [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice).</span></span><br/> <span data-ttu-id="73809-263">Die Uhr implementiert auch die [**BENUTZEROBERFLÄCHETimer-Schnittstelle.**](/windows/desktop/api/mfidl/nn-mfidl-imftimer)</span><span class="sxs-lookup"><span data-stu-id="73809-263">The clock also implements the [**IMFTimer**](/windows/desktop/api/mfidl/nn-mfidl-imftimer) interface.</span></span> <span data-ttu-id="73809-264">In der Media Foundation implementiert die Uhr die [**BERPresentationClock-Schnittstelle.**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock)</span><span class="sxs-lookup"><span data-stu-id="73809-264">In the Media Foundation pipeline, the clock implements the [**IMFPresentationClock**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) interface.</span></span> <span data-ttu-id="73809-265">Diese Schnittstelle wird in DirectShow nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="73809-265">It does not implement this interface in DirectShow.</span></span><br/> |



 

<span data-ttu-id="73809-266">Erhalten Sie die folgenden Schnittstellen aus dem Mixer:</span><span class="sxs-lookup"><span data-stu-id="73809-266">Get the following interfaces from the mixer:</span></span>



| <span data-ttu-id="73809-267">Mixerschnittstelle</span><span class="sxs-lookup"><span data-stu-id="73809-267">Mixer Interface</span></span>                              | <span data-ttu-id="73809-268">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="73809-268">Description</span></span>                                                |
|----------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="73809-269">**VORRÜBERSETZUNGTransform**</span><span class="sxs-lookup"><span data-stu-id="73809-269">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)         | <span data-ttu-id="73809-270">Ermöglicht dem Moderator die Kommunikation mit dem Mixer.</span><span class="sxs-lookup"><span data-stu-id="73809-270">Enables the presenter to communicate with the mixer.</span></span>       |
| [<span data-ttu-id="73809-271">**BESENVIDEODeviceID**</span><span class="sxs-lookup"><span data-stu-id="73809-271">**IMFVideoDeviceID**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) | <span data-ttu-id="73809-272">Ermöglicht es dem Moderator, die Geräte-GUID des Mixers zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="73809-272">Enables the presenter to validate the mixer's device GUID.</span></span> |



 

<span data-ttu-id="73809-273">Der folgende Code implementiert die [**InitServicePointers-Methode:**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers)</span><span class="sxs-lookup"><span data-stu-id="73809-273">The following code implements the [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) method :</span></span>


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



<span data-ttu-id="73809-274">Wenn die von [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) erhaltenen Schnittstellenzeigen nicht mehr gültig sind, ruft der EVR [**DEN TOPOLOGIEdienstLookupClient::ReleaseServicePointers auf.**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers)</span><span class="sxs-lookup"><span data-stu-id="73809-274">When the interface pointers obtained from [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) are no longer valid, the EVR calls [**IMFTopologyServiceLookupClient::ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers).</span></span> <span data-ttu-id="73809-275">Geben Sie in dieser Methode alle Schnittstellenzeiger frei, und legen Sie den Presenter-Zustand auf "Herunterfahren" fest:</span><span class="sxs-lookup"><span data-stu-id="73809-275">Inside this method, release all interface pointers and set the presenter state to shut down:</span></span>


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



<span data-ttu-id="73809-276">Der EVR ruft [**ReleaseServicePointers aus**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) verschiedenen Gründen auf, z. B.:</span><span class="sxs-lookup"><span data-stu-id="73809-276">The EVR calls [**ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) for various reasons, including:</span></span>

-   <span data-ttu-id="73809-277">Trennen oder Erneutes Verbinden von Pins (DirectShow) oder Hinzufügen oder Entfernen von Streamsenken (Media Foundation).</span><span class="sxs-lookup"><span data-stu-id="73809-277">Disconnecting or reconnecting pins (DirectShow), or adding or removing stream sinks (Media Foundation).</span></span>
-   <span data-ttu-id="73809-278">Ändern des Formats.</span><span class="sxs-lookup"><span data-stu-id="73809-278">Changing format.</span></span>
-   <span data-ttu-id="73809-279">Festlegen einer neuen Uhr.</span><span class="sxs-lookup"><span data-stu-id="73809-279">Setting a new clock.</span></span>
-   <span data-ttu-id="73809-280">Endgültiges Herunterfahren der EVR.</span><span class="sxs-lookup"><span data-stu-id="73809-280">Final shutdown of the EVR.</span></span>

<span data-ttu-id="73809-281">Während der Lebensdauer des Moderators kann der EVR [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) und [**ReleaseServicePointers mehrmals**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="73809-281">During the lifetime of the presenter, the EVR might call [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) and [**ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) several times.</span></span>

### <a name="implementing-imfvideopresenter"></a><span data-ttu-id="73809-282">Implementieren vonPRESENTVideoPresenter</span><span class="sxs-lookup"><span data-stu-id="73809-282">Implementing IMFVideoPresenter</span></span>

<span data-ttu-id="73809-283">Die [**BERDVideoPresenter-Schnittstelle**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) erbt [**DENTLOCKStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) und fügt zwei Methoden hinzu:</span><span class="sxs-lookup"><span data-stu-id="73809-283">The [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) interface inherits [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) and adds two methods:</span></span>



| <span data-ttu-id="73809-284">Methode</span><span class="sxs-lookup"><span data-stu-id="73809-284">Method</span></span>                                                               | <span data-ttu-id="73809-285">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="73809-285">Description</span></span>                                            |
|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="73809-286">**GetCurrentMediaType**</span><span class="sxs-lookup"><span data-stu-id="73809-286">**GetCurrentMediaType**</span></span>](/windows/desktop/api/evr/nf-evr-imfvideopresenter-getcurrentmediatype) | <span data-ttu-id="73809-287">Gibt den Medientyp der zusammengesetzten Videoframes zurück.</span><span class="sxs-lookup"><span data-stu-id="73809-287">Returns the media type of the composited video frames.</span></span> |
| [<span data-ttu-id="73809-288">**ProcessMessage**</span><span class="sxs-lookup"><span data-stu-id="73809-288">**ProcessMessage**</span></span>](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage)           | <span data-ttu-id="73809-289">Signalisiert dem Moderator, verschiedene Aktionen durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="73809-289">Signals the presenter to perform various actions.</span></span>      |



 

<span data-ttu-id="73809-290">Die [**GetCurrentMediaType-Methode**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-getcurrentmediatype) gibt den Medientyp des Presenters zurück.</span><span class="sxs-lookup"><span data-stu-id="73809-290">The [**GetCurrentMediaType**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-getcurrentmediatype) method returns the presenter's media type.</span></span> <span data-ttu-id="73809-291">(Weitere Informationen zum Festlegen des Medientyps finden Sie unter [Aushandeln von Formaten.)](#negotiating-formats) Der Medientyp wird als [**INTERFACEMediaType-Schnittstellenzeiger VOM TYP 1**](/windows/desktop/api/mfobjects/nn-mfobjects-imfvideomediatype) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="73809-291">(For details about setting the media type, see [Negotiating Formats](#negotiating-formats).) The media type is returned as an [**IMFVideoMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfvideomediatype) interface pointer.</span></span> <span data-ttu-id="73809-292">Im folgenden Beispiel wird davon ausgegangen, dass der Presenter den Medientyp als [**EINFMediaType-Zeiger**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) speichert.</span><span class="sxs-lookup"><span data-stu-id="73809-292">The following example assumes that the presenter stores the media type as an [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) pointer.</span></span> <span data-ttu-id="73809-293">Rufen Sie QueryInterface auf, um die **BENUTZEROBERFLÄCHEVideoMediaType-Schnittstelle** vom **Medientyp zu erhalten:**</span><span class="sxs-lookup"><span data-stu-id="73809-293">To get the **IMFVideoMediaType** interface from the media type, call **QueryInterface**:</span></span>


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



<span data-ttu-id="73809-294">Die [**ProcessMessage-Methode**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) ist der primäre Mechanismus, mit dem die EVR mit dem Moderator kommunizieren kann.</span><span class="sxs-lookup"><span data-stu-id="73809-294">The [**ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) method is the primary mechanism for the EVR to communicate with the presenter.</span></span> <span data-ttu-id="73809-295">Die folgenden Meldungen werden definiert.</span><span class="sxs-lookup"><span data-stu-id="73809-295">The following messages are defined.</span></span> <span data-ttu-id="73809-296">Die Details zur Implementierung der einzelnen Nachrichten finden Sie im weiteren Verlauf dieses Themas.</span><span class="sxs-lookup"><span data-stu-id="73809-296">The details of implementing each message are given in the remainder of this topic.</span></span>



| <span data-ttu-id="73809-297">`Message`</span><span class="sxs-lookup"><span data-stu-id="73809-297">Message</span></span>                                | <span data-ttu-id="73809-298">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="73809-298">Description</span></span>                                                                                                                                                                                                                                        |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73809-299">**MFVP_MESSAGE_INVALIDATEMEDIATYPE**</span><span class="sxs-lookup"><span data-stu-id="73809-299">**MFVP_MESSAGE_INVALIDATEMEDIATYPE**</span></span> | <span data-ttu-id="73809-300">Der Ausgabemedientyp des Mixers ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="73809-300">The mixer's output media type is invalid.</span></span> <span data-ttu-id="73809-301">Der Moderator sollte einen neuen Medientyp mit dem Mixer aushandeln.</span><span class="sxs-lookup"><span data-stu-id="73809-301">The presenter should negotiate a new media type with the mixer.</span></span> <span data-ttu-id="73809-302">Weitere Informationen [finden Sie unter Aushandeln von Formaten.](#negotiating-formats)</span><span class="sxs-lookup"><span data-stu-id="73809-302">See [Negotiating Formats](#negotiating-formats).</span></span>                                                                                         |
| <span data-ttu-id="73809-303">**MFVP_MESSAGE_BEGINSTREAMING**</span><span class="sxs-lookup"><span data-stu-id="73809-303">**MFVP_MESSAGE_BEGINSTREAMING**</span></span>      | <span data-ttu-id="73809-304">Das Streaming wurde gestartet.</span><span class="sxs-lookup"><span data-stu-id="73809-304">Streaming has started.</span></span> <span data-ttu-id="73809-305">Für diese Nachricht ist keine bestimmte Aktion erforderlich, aber Sie können sie zum Zuordnen von Ressourcen verwenden.</span><span class="sxs-lookup"><span data-stu-id="73809-305">No particular action is required by this message, but you can use it to allocate resources.</span></span>                                                                                                                                 |
| <span data-ttu-id="73809-306">**MFVP_MESSAGE_ENDSTREAMING**</span><span class="sxs-lookup"><span data-stu-id="73809-306">**MFVP_MESSAGE_ENDSTREAMING**</span></span>        | <span data-ttu-id="73809-307">Das Streaming wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="73809-307">Streaming has ended.</span></span> <span data-ttu-id="73809-308">Geben Sie alle Ressourcen frei, die Sie als Reaktion auf die **MFVP_MESSAGE_BEGINSTREAMING** zugeordnet haben.</span><span class="sxs-lookup"><span data-stu-id="73809-308">Release any resources that you allocated in response to the **MFVP_MESSAGE_BEGINSTREAMING** message.</span></span>                                                                                                                        |
| <span data-ttu-id="73809-309">**MFVP_MESSAGE_PROCESSINPUTNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="73809-309">**MFVP_MESSAGE_PROCESSINPUTNOTIFY**</span></span>  | <span data-ttu-id="73809-310">Der Mixer hat ein neues Eingabebeispiel erhalten und kann möglicherweise einen neuen Ausgaberahmen generieren.</span><span class="sxs-lookup"><span data-stu-id="73809-310">The mixer has received a new input sample and might be able to generate a new output frame.</span></span> <span data-ttu-id="73809-311">Der Presenter sollte [**IMTRANSFORM::P rocessOutput für**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) den Mixer aufrufen.</span><span class="sxs-lookup"><span data-stu-id="73809-311">The presenter should call [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) on the mixer.</span></span> <span data-ttu-id="73809-312">Weitere Informationen finden [Sie unter Verarbeiten der Ausgabe](#processing-output).</span><span class="sxs-lookup"><span data-stu-id="73809-312">See [Processing Output](#processing-output).</span></span> |
| <span data-ttu-id="73809-313">**MFVP_MESSAGE_ENDOFSTREAM**</span><span class="sxs-lookup"><span data-stu-id="73809-313">**MFVP_MESSAGE_ENDOFSTREAM**</span></span>         | <span data-ttu-id="73809-314">Die Präsentation wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="73809-314">The presentation has ended.</span></span> <span data-ttu-id="73809-315">Weitere Informationen [finden Sie unter Ende des Datenstroms.](#end-of-stream)</span><span class="sxs-lookup"><span data-stu-id="73809-315">See [End of Stream](#end-of-stream).</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="73809-316">**MFVP_MESSAGE_FLUSH**</span><span class="sxs-lookup"><span data-stu-id="73809-316">**MFVP_MESSAGE_FLUSH**</span></span>               | <span data-ttu-id="73809-317">Der EVR leert die Daten in seiner Renderingpipeline.</span><span class="sxs-lookup"><span data-stu-id="73809-317">The EVR is flushing the data in its rendering pipeline.</span></span> <span data-ttu-id="73809-318">Der Moderator sollte alle Videoframes verwerfen, die für die Präsentation geplant sind.</span><span class="sxs-lookup"><span data-stu-id="73809-318">The presenter should discard any video frames that are scheduled for presentation.</span></span>                                                                                                         |
| <span data-ttu-id="73809-319">**MFVP_MESSAGE_STEP**</span><span class="sxs-lookup"><span data-stu-id="73809-319">**MFVP_MESSAGE_STEP**</span></span>                | <span data-ttu-id="73809-320">Fordert den Moderator an, N Frames schrittweise vorwärts zu bringen.</span><span class="sxs-lookup"><span data-stu-id="73809-320">Requests the presenter to step forward N frames.</span></span> <span data-ttu-id="73809-321">Der Moderator sollte die nächsten N-1 Frames verwerfen und den N. Frame anzeigen.</span><span class="sxs-lookup"><span data-stu-id="73809-321">The presenter should discard the next N-1 frames and display the Nth frame.</span></span> <span data-ttu-id="73809-322">Weitere Informationen finden [Sie unter Frame Stepping (Frameschritt).](#frame-stepping)</span><span class="sxs-lookup"><span data-stu-id="73809-322">See [Frame Stepping](#frame-stepping).</span></span>                                                                                |
| <span data-ttu-id="73809-323">**MFVP_MESSAGE_CANCELSTEP**</span><span class="sxs-lookup"><span data-stu-id="73809-323">**MFVP_MESSAGE_CANCELSTEP**</span></span>          | <span data-ttu-id="73809-324">Bricht frame stepping ab.</span><span class="sxs-lookup"><span data-stu-id="73809-324">Cancels frame stepping.</span></span>                                                                                                                                                                                                                            |



 

### <a name="implementing-imfclockstatesink"></a><span data-ttu-id="73809-325">Implementieren von DEADClockStateSink</span><span class="sxs-lookup"><span data-stu-id="73809-325">Implementing IMFClockStateSink</span></span>

<span data-ttu-id="73809-326">Der Präsentationser muss im Rahmen seiner Implementierung von [**VORZEIGERVideoPresenter,**](/windows/desktop/api/evr/nn-evr-imfvideopresenter)der **DEN NAMEN ZUNEClockStateSink erbt, die INTERFACEClockStateSink-Schnittstelle implementieren.** [](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)</span><span class="sxs-lookup"><span data-stu-id="73809-326">The presenter must implement the [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) interface as part of its implementation of [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter), which inherits **IMFClockStateSink**.</span></span> <span data-ttu-id="73809-327">Die EVR verwendet diese Schnittstelle, um den Moderator zu benachrichtigen, wenn sich der Status der EVR-Uhr ändert.</span><span class="sxs-lookup"><span data-stu-id="73809-327">The EVR uses this interface to notify the presenter whenever the EVR's clock changes state.</span></span> <span data-ttu-id="73809-328">Weitere Informationen zu den Uhrzuständen finden Sie unter [Presentation Clock](presentation-clock.md).</span><span class="sxs-lookup"><span data-stu-id="73809-328">For more information about the clock states, see [Presentation Clock](presentation-clock.md).</span></span>

<span data-ttu-id="73809-329">Hier sind einige Richtlinien für die Implementierung der Methoden in dieser Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="73809-329">Here are some guidelines for implementing the methods in this interface.</span></span> <span data-ttu-id="73809-330">Alle Methoden sollten fehlschlagen, wenn der Presenter heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="73809-330">All of the methods should fail if the presenter is shut down.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="73809-331"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>OnClockStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="73809-331"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>OnClockStart</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="73809-332">Legen Sie den Presenterzustand auf Gestartet fest.</span><span class="sxs-lookup"><span data-stu-id="73809-332">Set the presenter state to started.</span></span></li>
<li><span data-ttu-id="73809-333">Wenn <em>llClockStartOffset</em> nicht <strong>PRESENTATION_CURRENT_POSITION</strong>ist, leeren Sie die Warteschlange der Beispiele des Moderators.</span><span class="sxs-lookup"><span data-stu-id="73809-333">If the <em>llClockStartOffset</em> is not <strong>PRESENTATION_CURRENT_POSITION</strong>, flush the presenter's queue of samples.</span></span> <span data-ttu-id="73809-334">(Dies entspricht dem Empfangen <strong>einer</strong> MFVP_MESSAGE_FLUSH Nachricht.)</span><span class="sxs-lookup"><span data-stu-id="73809-334">(This is equivalent to receiving an <strong>MFVP_MESSAGE_FLUSH</strong> message.)</span></span></li>
<li><span data-ttu-id="73809-335">Wenn eine vorherige Frameschrittanforderung noch aussteht, verarbeiten Sie die Anforderung (siehe <a href="#frame-stepping">Frame Stepping</a>).</span><span class="sxs-lookup"><span data-stu-id="73809-335">If a previous frame-step request is still pending, process the request (see <a href="#frame-stepping">Frame Stepping</a>).</span></span> <span data-ttu-id="73809-336">Versuchen Sie andernfalls, die Ausgabe des Mixers zu verarbeiten (siehe <a href="#processing-output">Verarbeiten der Ausgabe</a>.</span><span class="sxs-lookup"><span data-stu-id="73809-336">Otherwise, try to process output from the mixer (see <a href="#processing-output">Processing Output</a>.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73809-337"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop"><strong>OnClockStop</strong></a></span><span class="sxs-lookup"><span data-stu-id="73809-337"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop"><strong>OnClockStop</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="73809-338">Legen Sie den Presenterzustand auf Beendet fest.</span><span class="sxs-lookup"><span data-stu-id="73809-338">Set the presenter state to stopped.</span></span></li>
<li><span data-ttu-id="73809-339">Leeren Sie die Warteschlange der Warteschlange der Beispiele des Moderators.</span><span class="sxs-lookup"><span data-stu-id="73809-339">Flush the presenter's queue of samples.</span></span></li>
<li><span data-ttu-id="73809-340">Brechen Sie alle ausstehenden Frameschritt-Operation ab.</span><span class="sxs-lookup"><span data-stu-id="73809-340">Cancel any pending frame-step operation.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73809-341"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockpause"><strong>OnClockPause</strong></a></span><span class="sxs-lookup"><span data-stu-id="73809-341"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockpause"><strong>OnClockPause</strong></a></span></span></td>
<td><span data-ttu-id="73809-342">Legen Sie den Presenterzustand auf angehalten fest.</span><span class="sxs-lookup"><span data-stu-id="73809-342">Set the presenter state to paused.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73809-343"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart"><strong>OnClockRestart</strong></a></span><span class="sxs-lookup"><span data-stu-id="73809-343"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart"><strong>OnClockRestart</strong></a></span></span></td>
<td><span data-ttu-id="73809-344">Behandeln Sie dasselbe wie <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>OnClockStart,</strong></a> aber leeren Sie die Warteschlange der Beispiele nicht.</span><span class="sxs-lookup"><span data-stu-id="73809-344">Treat the same as <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>OnClockStart</strong></a> but do not flush the queue of samples.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73809-345"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate"><strong>OnClockSetRate</strong></a></span><span class="sxs-lookup"><span data-stu-id="73809-345"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate"><strong>OnClockSetRate</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="73809-346">Wenn die Rate von null in ungleich 0 (null) geändert wird, brechen Sie frame stepping ab.</span><span class="sxs-lookup"><span data-stu-id="73809-346">If the rate is changing from zero to nonzero, cancel frame stepping.</span></span></li>
<li><span data-ttu-id="73809-347">Speichern Sie die neue Taktrate.</span><span class="sxs-lookup"><span data-stu-id="73809-347">Store the new clock rate.</span></span> <span data-ttu-id="73809-348">Die Taktrate wirkt sich darauf aus, wenn Stichproben dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="73809-348">The clock rate affects when samples are presented.</span></span> <span data-ttu-id="73809-349">Weitere Informationen finden Sie unter <a href="#scheduling-samples">Zeitplanungsbeispiele.</a></span><span class="sxs-lookup"><span data-stu-id="73809-349">For more information, see <a href="#scheduling-samples">Scheduling Samples</a>.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="implementing-imfratesupport"></a><span data-ttu-id="73809-350">Implementieren vonTRATERateSupport</span><span class="sxs-lookup"><span data-stu-id="73809-350">Implementing IMFRateSupport</span></span>

<span data-ttu-id="73809-351">Um andere Wiedergaberaten als 1× zu unterstützen, muss die Moderatorin die [**BERATERateSupport-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) implementieren.</span><span class="sxs-lookup"><span data-stu-id="73809-351">To support playback rates other than 1× speed, the presenter must implement the [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) interface.</span></span> <span data-ttu-id="73809-352">Hier sind einige Richtlinien für die Implementierung der Methoden in dieser Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="73809-352">Here are some guidelines for implementing the methods in this interface.</span></span> <span data-ttu-id="73809-353">Alle Methoden sollten fehlschlagen, nachdem der Presenter heruntergefahren wurde.</span><span class="sxs-lookup"><span data-stu-id="73809-353">All of the methods should fail after the presenter is shut down.</span></span> <span data-ttu-id="73809-354">Weitere Informationen zu dieser Schnittstelle finden Sie unter [Rate Control](rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="73809-354">For more information about this interface, see [Rate Control](rate-control.md).</span></span>



| <span data-ttu-id="73809-355">Wert</span><span class="sxs-lookup"><span data-stu-id="73809-355">Value</span></span>                                                          | <span data-ttu-id="73809-356">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="73809-356">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="73809-357">**GetSlowestRate**</span><span class="sxs-lookup"><span data-stu-id="73809-357">**GetSlowestRate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate)   | <span data-ttu-id="73809-358">Gibt 0 (null) zurück, um keine minimale Wiedergaberate anzugeben.</span><span class="sxs-lookup"><span data-stu-id="73809-358">Return zero to indicate no minimum playback rate.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="73809-359">**GetFastestRate**</span><span class="sxs-lookup"><span data-stu-id="73809-359">**GetFastestRate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate)   | <span data-ttu-id="73809-360">Bei nicht schlanker Wiedergabe sollte die Wiedergaberate die Aktualisierungsrate des Monitors nicht *überschreiten:* maximale Aktualisierungsrate  =   (Hz) */Videobildrate* (FPS).</span><span class="sxs-lookup"><span data-stu-id="73809-360">For non-thinned playback, the playback rate should not exceed the refresh rate of the monitor: *maximum rate* = *refresh rate* (Hz) / *video frame rate* (fps).</span></span> <span data-ttu-id="73809-361">Die Videobildrate wird im Medientyp des Moderators angegeben.</span><span class="sxs-lookup"><span data-stu-id="73809-361">The video frame rate is specified in the presenter's media type.</span></span> <br/> <span data-ttu-id="73809-362">Bei der schlanken Wiedergabe ist die Wiedergaberate ungebunden. gibt den Wert **FLT_MAX.**</span><span class="sxs-lookup"><span data-stu-id="73809-362">For thinned playback, the playback rate is unbounded; return the value **FLT_MAX**.</span></span> <span data-ttu-id="73809-363">In der Praxis sind die Quelle und der Decoder die begrenzenden Faktoren bei der schlanken Wiedergabe.</span><span class="sxs-lookup"><span data-stu-id="73809-363">In practice, the source and the decoder will be the limiting factors during thinned playback.</span></span> <br/> <span data-ttu-id="73809-364">Geben Sie für die umgekehrte Wiedergabe den negativen Wert der maximalen Rate zurück.</span><span class="sxs-lookup"><span data-stu-id="73809-364">For reverse playback, return the negative of the maximum rate.</span></span><br/> |
| [<span data-ttu-id="73809-365">**IsRateSupported**</span><span class="sxs-lookup"><span data-stu-id="73809-365">**IsRateSupported**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) | <span data-ttu-id="73809-366">Gibt **MF_E_UNSUPPORTED_RATE** zurück, wenn der absolute Wert *von flRate* die maximale Wiedergaberate des Moderators überschreitet.</span><span class="sxs-lookup"><span data-stu-id="73809-366">Return **MF_E_UNSUPPORTED_RATE** if the absolute value of *flRate* exceeds the presenter's maximum playback rate.</span></span> <span data-ttu-id="73809-367">Berechnen Sie die maximale Wiedergaberate wie für [**GetFastestRate beschrieben.**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate)</span><span class="sxs-lookup"><span data-stu-id="73809-367">Calculate the maximum playback rate as described for [**GetFastestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate).</span></span>                                                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="73809-368">Das folgende Beispiel zeigt, wie die [**GetFastestRate-Methode implementiert**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate) wird:</span><span class="sxs-lookup"><span data-stu-id="73809-368">The following example shows how to implement the [**GetFastestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate) method:</span></span>


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



<span data-ttu-id="73809-369">Im vorherigen Beispiel wird die Hilfsmethode GetMaxRate zum Berechnen der maximalen Vorwärtswiedergaberate aufruft:</span><span class="sxs-lookup"><span data-stu-id="73809-369">The previous example calls a helper method, GetMaxRate, to calculate the maximum forward playback rate:</span></span>

<span data-ttu-id="73809-370">Das folgende Beispiel zeigt, wie die [**IsRateSupported-Methode implementiert**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) wird:</span><span class="sxs-lookup"><span data-stu-id="73809-370">The following example shows how to implement the [**IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) method:</span></span>


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



### <a name="sending-events-to-the-evr"></a><span data-ttu-id="73809-371">Senden von Ereignissen an die EVR</span><span class="sxs-lookup"><span data-stu-id="73809-371">Sending Events to the EVR</span></span>

<span data-ttu-id="73809-372">Der Moderator muss den EVR über verschiedene Ereignisse benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="73809-372">The presenter must notify the EVR of various events.</span></span> <span data-ttu-id="73809-373">Zu diesem Zwecke wird die [**IMediaEventSink-Schnittstelle**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) des EVR verwendet, die beim Aufrufen der [**METHODETOPOLOGYServiceLookupClient::InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) des Moderators durch den EVR ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="73809-373">To do so, it uses the EVR's [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) interface, obtained when the EVR calls the presenter's [**IMFTopologyServiceLookupClient::InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) method.</span></span> <span data-ttu-id="73809-374">(Die **IMediaEventSink-Schnittstelle** ist ursprünglich eine DirectShow-Schnittstelle, wird jedoch sowohl im DirectShow EVR als auch im Media Foundation.) Der folgende Code zeigt, wie sie ein Ereignis an die EVR senden:</span><span class="sxs-lookup"><span data-stu-id="73809-374">(The **IMediaEventSink** interface is originally a DirectShow interface, but is used in both the DirectShow EVR and the Media Foundation.) The following code shows how to send an event to the EVR:</span></span>


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



<span data-ttu-id="73809-375">In der folgenden Tabelle sind die ereignisse aufgeführt, die der Moderator zusammen mit den Ereignisparametern sendet.</span><span class="sxs-lookup"><span data-stu-id="73809-375">The following table lists the events that the presenter sends, along with the event parameters.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="73809-376">Ereignis</span><span class="sxs-lookup"><span data-stu-id="73809-376">Event</span></span></th>
<th><span data-ttu-id="73809-377">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="73809-377">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="73809-378"><a href="/windows/desktop/DirectShow/ec-complete"><strong>EC_COMPLETE</strong></a></span><span class="sxs-lookup"><span data-stu-id="73809-378"><a href="/windows/desktop/DirectShow/ec-complete"><strong>EC_COMPLETE</strong></a></span></span></td>
<td><span data-ttu-id="73809-379">Der Moderator hat das Rendern aller Frames nach der MFVP_MESSAGE_ENDOFSTREAM abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="73809-379">The presenter has finished rendering all frames after the MFVP_MESSAGE_ENDOFSTREAM message.</span></span><br/>
<ul>
<li><span data-ttu-id="73809-380"><em>Param1:</em>HRESULT, das den Status des Vorgangs angibt.</span><span class="sxs-lookup"><span data-stu-id="73809-380"><em>Param1</em>: HRESULT indicating the status of the operation.</span></span></li>
<li><span data-ttu-id="73809-381"><em>Param2:</em>Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="73809-381"><em>Param2</em>: Not used.</span></span></li>
</ul>
<span data-ttu-id="73809-382">Weitere Informationen finden Sie unter <a href="#end-of-stream">Ende des Streams.</a></span><span class="sxs-lookup"><span data-stu-id="73809-382">For more information, see <a href="#end-of-stream">End of Stream</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73809-383"><a href="/windows/desktop/DirectShow/ec-display-changed"><strong>EC_DISPLAY_CHANGED</strong></a></span><span class="sxs-lookup"><span data-stu-id="73809-383"><a href="/windows/desktop/DirectShow/ec-display-changed"><strong>EC_DISPLAY_CHANGED</strong></a></span></span></td>
<td><span data-ttu-id="73809-384">Das Direct3D-Gerät wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="73809-384">The Direct3D device has changed.</span></span><br/>
<ul>
<li><span data-ttu-id="73809-385"><em>Param1:</em>Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="73809-385"><em>Param1</em>: Not used.</span></span></li>
<li><span data-ttu-id="73809-386"><em>Param2:</em>Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="73809-386"><em>Param2</em>: Not used.</span></span></li>
</ul>
<span data-ttu-id="73809-387">Weitere Informationen finden Sie unter <a href="#managing-the-direct3d-device">Verwalten des Direct3D-Geräts.</a></span><span class="sxs-lookup"><span data-stu-id="73809-387">For more information, see <a href="#managing-the-direct3d-device">Managing the Direct3D Device</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73809-388"><a href="/windows/desktop/DirectShow/ec-errorabort"><strong>EC_ERRORABORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="73809-388"><a href="/windows/desktop/DirectShow/ec-errorabort"><strong>EC_ERRORABORT</strong></a></span></span></td>
<td><span data-ttu-id="73809-389">Es ist ein Fehler aufgetreten, der das Beenden des Streamings erfordert.</span><span class="sxs-lookup"><span data-stu-id="73809-389">An error has occurred that requires streaming to stop.</span></span><br/>
<ul>
<li><span data-ttu-id="73809-390"><em>Param1</em>: <strong>HRESULT gibt</strong> den aufgetretenen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="73809-390"><em>Param1</em>: <strong>HRESULT</strong> indicating the error that occurred.</span></span></li>
<li><span data-ttu-id="73809-391"><em>Param2:</em>Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="73809-391"><em>Param2</em>: Not used.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73809-392"><a href="/windows/desktop/DirectShow/ec-processing-latency"><strong>EC_PROCESSING_LATENCY</strong></a></span><span class="sxs-lookup"><span data-stu-id="73809-392"><a href="/windows/desktop/DirectShow/ec-processing-latency"><strong>EC_PROCESSING_LATENCY</strong></a></span></span></td>
<td><span data-ttu-id="73809-393">Gibt die Zeit an, die der Presenter zum Rendern der einzelnen Frames in Zeit nimmt.</span><span class="sxs-lookup"><span data-stu-id="73809-393">Specifies the amount of time that the presenter is taking to render each frame.</span></span> <span data-ttu-id="73809-394">(Optional.)</span><span class="sxs-lookup"><span data-stu-id="73809-394">(Optional.)</span></span><br/>
<ul>
<li><span data-ttu-id="73809-395"><em>Param1:</em>Zeiger auf einen konstanten <strong>LONGLONG-Wert,</strong> der die Zeit zum Verarbeiten des Frames in Einheiten von 100 Nanosekunden enthält.</span><span class="sxs-lookup"><span data-stu-id="73809-395"><em>Param1</em>: Pointer to a constant <strong>LONGLONG</strong> value that contains the amount of time to process the frame, in 100-nanosecond units.</span></span></li>
<li><span data-ttu-id="73809-396"><em>Param2:</em>Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="73809-396"><em>Param2</em>: Not used.</span></span></li>
</ul>
<span data-ttu-id="73809-397">Weitere Informationen finden Sie unter <a href="#processing-output">Verarbeiten der Ausgabe</a>.</span><span class="sxs-lookup"><span data-stu-id="73809-397">For more information, see <a href="#processing-output">Processing Output</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73809-398"><a href="/windows/desktop/DirectShow/ec-sample-latency"><strong>EC_SAMPLE_LATENCY</strong></a></span><span class="sxs-lookup"><span data-stu-id="73809-398"><a href="/windows/desktop/DirectShow/ec-sample-latency"><strong>EC_SAMPLE_LATENCY</strong></a></span></span></td>
<td><span data-ttu-id="73809-399">Gibt die aktuelle Verzögerungszeit in Renderingbeispielen an.</span><span class="sxs-lookup"><span data-stu-id="73809-399">Specifies the current lag time in rendering samples.</span></span> <span data-ttu-id="73809-400">Wenn der Wert positiv ist, liegen die Stichproben hinter dem Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="73809-400">If the value is positive, samples are behind schedule.</span></span> <span data-ttu-id="73809-401">Wenn der Wert negativ ist, liegen die Stichproben dem Zeitplan voraus.</span><span class="sxs-lookup"><span data-stu-id="73809-401">If the value is negative, samples are ahead of schedule.</span></span> <span data-ttu-id="73809-402">(Optional.)</span><span class="sxs-lookup"><span data-stu-id="73809-402">(Optional.)</span></span><br/>
<ul>
<li><span data-ttu-id="73809-403"><em>Param1:</em>Zeiger auf einen konstanten <strong>LONGLONG-Wert,</strong> der die Verzögerungszeit in Einheiten von 100 Nanosekunden enthält.</span><span class="sxs-lookup"><span data-stu-id="73809-403"><em>Param1</em>: Pointer to a constant <strong>LONGLONG</strong> value that contains the lag time, in 100-nanosecond units.</span></span></li>
<li><span data-ttu-id="73809-404"><em>Param2:</em>Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="73809-404"><em>Param2</em>: Not used.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73809-405"><a href="/windows/desktop/DirectShow/ec-scrub-time"><strong>EC_SCRUB_TIME</strong></a></span><span class="sxs-lookup"><span data-stu-id="73809-405"><a href="/windows/desktop/DirectShow/ec-scrub-time"><strong>EC_SCRUB_TIME</strong></a></span></span></td>
<td><span data-ttu-id="73809-406">Wird unmittelbar <strong>nach</strong> EC_STEP_COMPLETE gesendet, wenn die Wiedergaberate 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="73809-406">Sent immediately after <strong>EC_STEP_COMPLETE</strong> if the playback rate is zero.</span></span> <span data-ttu-id="73809-407">Dieses Ereignis enthält den Zeitstempel des angezeigten Frames.</span><span class="sxs-lookup"><span data-stu-id="73809-407">This event contains the time stamp of the frame that was displayed.</span></span><br/>
<ul>
<li><span data-ttu-id="73809-408"><em>Param1:</em>Niedrigere 32 Bits des Zeitstempels.</span><span class="sxs-lookup"><span data-stu-id="73809-408"><em>Param1</em>: Lower 32 bits of the time stamp.</span></span></li>
<li><span data-ttu-id="73809-409"><em>Param2:</em>Obere 32 Bits des Zeitstempels.</span><span class="sxs-lookup"><span data-stu-id="73809-409"><em>Param2</em>: Upper 32 bits of the time stamp.</span></span></li>
</ul>
<span data-ttu-id="73809-410">Weitere Informationen finden Sie unter <a href="#frame-stepping">Frame Stepping</a>.</span><span class="sxs-lookup"><span data-stu-id="73809-410">For more information, see <a href="#frame-stepping">Frame Stepping</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73809-411"><a href="/windows/desktop/DirectShow/ec-step-complete"><strong>EC_STEP_COMPLETE</strong></a></span><span class="sxs-lookup"><span data-stu-id="73809-411"><a href="/windows/desktop/DirectShow/ec-step-complete"><strong>EC_STEP_COMPLETE</strong></a></span></span></td>
<td><span data-ttu-id="73809-412">Der Presenter hat einen Frameschritt abgeschlossen oder abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="73809-412">The presenter has completed or canceled a frame step.</span></span><br/>
<ul>
<li><span data-ttu-id="73809-413"><em>Param1:</em>Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="73809-413"><em>Param1</em>: Not used.</span></span></li>
<li><span data-ttu-id="73809-414"><em>Param2:</em>Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="73809-414"><em>Param2</em>: Not used.</span></span></li>
</ul>
<span data-ttu-id="73809-415">Weitere Informationen finden Sie unter <a href="#frame-stepping">Frame Stepping</a>.</span><span class="sxs-lookup"><span data-stu-id="73809-415">For more information, see <a href="#frame-stepping">Frame Stepping</a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="73809-416">In einer früheren Version der Dokumentation wurde <em>Param1 falsch</em> beschrieben.</span><span class="sxs-lookup"><span data-stu-id="73809-416">A previous version of the documentation described <em>Param1</em> incorrectly.</span></span> <span data-ttu-id="73809-417">Dieser Parameter wird für dieses Ereignis nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="73809-417">This parameter is not used for this event.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="negotiating-formats"></a><span data-ttu-id="73809-418">Aushandeln von Formaten</span><span class="sxs-lookup"><span data-stu-id="73809-418">Negotiating Formats</span></span>

<span data-ttu-id="73809-419">Wenn der Moderator eine **MFVP_MESSAGE_INVALIDATEMEDIATYPE** evr empfängt, muss er das Ausgabeformat für den Mixer wie folgt festlegen:</span><span class="sxs-lookup"><span data-stu-id="73809-419">Whenever the presenter receives an **MFVP_MESSAGE_INVALIDATEMEDIATYPE** message from the EVR, it must set the output format on the mixer, as follows:</span></span>

1.  <span data-ttu-id="73809-420">Rufen [**Sie IMTRANSFORM::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) für den Mixer auf, um einen möglichen Ausgabetyp zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="73809-420">Call [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) on the mixer to get a possible output type.</span></span> <span data-ttu-id="73809-421">Dieser Typ beschreibt ein Format, das der Mixer mit den Eingabestreams und den Videoverarbeitungsfunktionen des Grafikgeräts erzeugen kann.</span><span class="sxs-lookup"><span data-stu-id="73809-421">This type describes a format that the mixer can produce given the input streams and the video processing capabilities of the graphics device.</span></span>
2.  <span data-ttu-id="73809-422">Überprüfen Sie, ob der Presenter diesen Medientyp als Renderingformat verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="73809-422">Check whether the presenter can use this media type as its rendering format.</span></span> <span data-ttu-id="73809-423">Hier sind einige Dinge zu überprüfen, obwohl Ihre Implementierung möglicherweise eigene Anforderungen hat:</span><span class="sxs-lookup"><span data-stu-id="73809-423">Here are some things to check, although your implementation might have its own requirements:</span></span>

    -   <span data-ttu-id="73809-424">Das Video muss unkomprimiert sein.</span><span class="sxs-lookup"><span data-stu-id="73809-424">The video must be uncompressed.</span></span>
    -   <span data-ttu-id="73809-425">Das Video darf nur progressive Frames haben.</span><span class="sxs-lookup"><span data-stu-id="73809-425">The video must have progressive frames only.</span></span> <span data-ttu-id="73809-426">Überprüfen Sie, [**ob MF_MT_INTERLACE_MODE**](mf-mt-interlace-mode-attribute.md) Attribut gleich **MFVideoInterlace_Progressive.**</span><span class="sxs-lookup"><span data-stu-id="73809-426">Check that the [**MF_MT_INTERLACE_MODE**](mf-mt-interlace-mode-attribute.md) attribute equals **MFVideoInterlace_Progressive**.</span></span>
    -   <span data-ttu-id="73809-427">Das Format muss mit dem Direct3D-Gerät kompatibel sein.</span><span class="sxs-lookup"><span data-stu-id="73809-427">The format must be compatible with the Direct3D device.</span></span>

    <span data-ttu-id="73809-428">Wenn der Typ nicht akzeptabel ist, kehren Sie zu Schritt 1 zurück, und erhalten Sie den nächsten vorgeschlagenen Typ des Mixers.</span><span class="sxs-lookup"><span data-stu-id="73809-428">If the type is not acceptable, return to step 1 and get the mixer's next proposed type.</span></span>

3.  <span data-ttu-id="73809-429">Erstellen Sie einen neuen Medientyp, der ein Klon des ursprünglichen Typs ist, und ändern Sie dann die folgenden Attribute:</span><span class="sxs-lookup"><span data-stu-id="73809-429">Create a new media type that is a clone of the original type and then change the following attributes:</span></span>

    -   <span data-ttu-id="73809-430">Legen Sie [**MF_MT_FRAME_SIZE-Attribut**](mf-mt-frame-size-attribute.md) auf die Breite und Höhe fest, die Sie für die Direct3D-Oberflächen verwenden möchten, die Sie zuordnen möchten.</span><span class="sxs-lookup"><span data-stu-id="73809-430">Set the [**MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) attribute equal to the width and height that you want for the Direct3D surfaces you will allocate.</span></span>
    -   <span data-ttu-id="73809-431">Legen Sie das [**MF_MT_PAN_SCAN_ENABLED-Attribut**](mf-mt-pan-scan-enabled-attribute.md) auf **FALSE fest.**</span><span class="sxs-lookup"><span data-stu-id="73809-431">Set the [**MF_MT_PAN_SCAN_ENABLED**](mf-mt-pan-scan-enabled-attribute.md) attribute to **FALSE**.</span></span>
    -   <span data-ttu-id="73809-432">Legen Sie [**MF_MT_PIXEL_ASPECT_RATIO-Attribut**](mf-mt-pixel-aspect-ratio-attribute.md) auf den PAR-Wert der Anzeige fest (in der Regel 1:1).</span><span class="sxs-lookup"><span data-stu-id="73809-432">Set the [**MF_MT_PIXEL_ASPECT_RATIO**](mf-mt-pixel-aspect-ratio-attribute.md) attribute equal to the PAR of the display (typically 1:1).</span></span>
    -   <span data-ttu-id="73809-433">Legen Sie die[](mf-mt-geometric-aperture-attribute.md) geometrische Öffnung ( MF_MT_GEOMETRIC_APERTURE-Attribut) auf ein Rechteck innerhalb der Direct3D-Oberfläche fest.</span><span class="sxs-lookup"><span data-stu-id="73809-433">Set the geometric aperture ([**MF_MT_GEOMETRIC_APERTURE**](mf-mt-geometric-aperture-attribute.md) attribute) equal to a rectangle within the Direct3D surface.</span></span> <span data-ttu-id="73809-434">Wenn der Mixer einen Ausgaberahmen generiert, schneide er das Quellbild auf dieses Rechteck.</span><span class="sxs-lookup"><span data-stu-id="73809-434">When the mixer generates an output frame, it blits the source image onto this rectangle.</span></span> <span data-ttu-id="73809-435">Die geometrische Öffnung kann so groß wie die Oberfläche sein, oder es kann sich um ein Unterrektgle innerhalb der Oberfläche befinden.</span><span class="sxs-lookup"><span data-stu-id="73809-435">The geometric aperture can be as large as the surface, or it can be a subrectangle within the surface.</span></span> <span data-ttu-id="73809-436">Weitere Informationen finden Sie unter [Quell- und Zielrechtecke.](#source-and-destination-rectangles)</span><span class="sxs-lookup"><span data-stu-id="73809-436">For more information, see [Source and Destination Rectangles](#source-and-destination-rectangles).</span></span>

4.  <span data-ttu-id="73809-437">Um zu testen, ob der Mixer den geänderten Ausgabetyp akzeptiert, rufen Sie [**DIETRANSFORM::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) mit dem MFT_SET_TYPE_TEST_ONLY **auf.**</span><span class="sxs-lookup"><span data-stu-id="73809-437">To test whether the mixer will accept the modified output type, call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) with the **MFT_SET_TYPE_TEST_ONLY** flag.</span></span> <span data-ttu-id="73809-438">Wenn der Mixer den Typ ablehnt, wechseln Sie zurück zu Schritt 1, und erhalten Sie den nächsten Typ.</span><span class="sxs-lookup"><span data-stu-id="73809-438">If the mixer rejects the type, go back to step 1 and get the next type.</span></span>
5.  <span data-ttu-id="73809-439">Ordnen Sie einen Pool von Direct3D-Oberflächen zu, wie unter [Zuordnen von Direct3D-Oberflächen beschrieben.](#allocating-direct3d-surfaces)</span><span class="sxs-lookup"><span data-stu-id="73809-439">Allocate a pool of Direct3D surfaces, as described in [Allocating Direct3D Surfaces](#allocating-direct3d-surfaces).</span></span> <span data-ttu-id="73809-440">Der Mixer verwendet diese Oberflächen, wenn er die zusammengesetzten Videoframes zeichnet.</span><span class="sxs-lookup"><span data-stu-id="73809-440">The mixer will use these surfaces when it draws the composited video frames.</span></span>
6.  <span data-ttu-id="73809-441">Legen Sie den Ausgabetyp für den Mixer fest, indem [**Sie SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) ohne Flags aufrufen.</span><span class="sxs-lookup"><span data-stu-id="73809-441">Set the output type on the mixer by calling [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) with no flags.</span></span> <span data-ttu-id="73809-442">Wenn der erste Aufruf von **SetOutputType** in Schritt 4 erfolgreich war, sollte die Methode erneut erfolgreich sein.</span><span class="sxs-lookup"><span data-stu-id="73809-442">If the first call to **SetOutputType** succeeded in step 4, the method should succeed again.</span></span>

<span data-ttu-id="73809-443">Wenn die Typen des Mixers nicht mehr vorhanden sind, gibt die [**GetOutputAvailableType-Methode**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) MF_E_NO_MORE_TYPES.</span><span class="sxs-lookup"><span data-stu-id="73809-443">If the mixer runs out of types, the [**GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) method returns **MF_E_NO_MORE_TYPES**.</span></span> <span data-ttu-id="73809-444">Wenn der Moderator keinen geeigneten Ausgabetyp für den Mixer finden kann, kann der Stream nicht gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="73809-444">If the presenter cannot find a suitable output type for the mixer, the stream cannot be rendered.</span></span> <span data-ttu-id="73809-445">In diesem Fall können DirectShow oder Media Foundation ein anderes Streamformat ausprobieren.</span><span class="sxs-lookup"><span data-stu-id="73809-445">In that case, DirectShow or Media Foundation might try another stream format.</span></span> <span data-ttu-id="73809-446">Daher kann der Moderator mehrere Nachrichten MFVP_MESSAGE_INVALIDATEMEDIATYPE **in** einer Zeile empfangen, bis ein gültiger Typ gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="73809-446">Therefore, the presenter might receive several **MFVP_MESSAGE_INVALIDATEMEDIATYPE** messages in a row until a valid type is found.</span></span>

<span data-ttu-id="73809-447">Der Mixer postiert das Video automatisch und berücksichtigt dabei das Pixel-Seitenverhältnis (PAR) der Quelle und des Ziels.</span><span class="sxs-lookup"><span data-stu-id="73809-447">The mixer automatically letterboxes the video, taking into account the pixel aspect ratio (PAR) of the source and destination.</span></span> <span data-ttu-id="73809-448">Um optimale Ergebnisse zu erzielen, sollten die Breite und Höhe der Oberfläche und die geometrische Öffnung der tatsächlichen Größe des Videos auf der Anzeige entspricht.</span><span class="sxs-lookup"><span data-stu-id="73809-448">For best results, the surface width and height and the geometric aperture should be equal to the actual size that you want the video to appear on the display.</span></span> <span data-ttu-id="73809-449">Die folgende Abbildung veranschaulicht diesen Prozess.</span><span class="sxs-lookup"><span data-stu-id="73809-449">The following image illustrates this process.</span></span>

![Diagramm, das einen zusammengesetzten Fram zeigt, der zu einer direct3d-Oberfläche führt, die zu einem Fenster führt](images/b746edca-8830-4c88-aa59-0067b020d4af.gif)

<span data-ttu-id="73809-451">Der folgende Code zeigt die Gliederung des Prozesses.</span><span class="sxs-lookup"><span data-stu-id="73809-451">The following code shows the outline of the process.</span></span> <span data-ttu-id="73809-452">Einige der Schritte werden in Hilfsfunktionen platziert, deren genaue Details von den Anforderungen Ihrer Moderatorin abhängen.</span><span class="sxs-lookup"><span data-stu-id="73809-452">Some of the steps are placed in helper functions, the exact details of which will depend on the requirements of your presenter.</span></span>


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



<span data-ttu-id="73809-453">Weitere Informationen zu Videomedientypen finden Sie unter [Videomedientypen.](video-media-types.md)</span><span class="sxs-lookup"><span data-stu-id="73809-453">For more information about video media types, see [Video Media Types](video-media-types.md).</span></span>

## <a name="managing-the-direct3d-device"></a><span data-ttu-id="73809-454">Verwalten des Direct3D-Geräts</span><span class="sxs-lookup"><span data-stu-id="73809-454">Managing the Direct3D Device</span></span>

<span data-ttu-id="73809-455">Der Moderator erstellt das Direct3D-Gerät und behandelt jeglichen Geräteverlust während des Streamings.</span><span class="sxs-lookup"><span data-stu-id="73809-455">The presenter creates the Direct3D device and handles any device loss during streaming.</span></span> <span data-ttu-id="73809-456">Der Presenter hostet auch den Direct3D-Geräte-Manager, der anderen Komponenten die Verwendung desselben Geräts ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="73809-456">The presenter also hosts the Direct3D device manager, which provides a way for other components to use the same device.</span></span> <span data-ttu-id="73809-457">Der Mixer verwendet z. B. das Direct3D-Gerät, um Unterstreams zu mischen, zu deinterketten und Farbanpassungen durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="73809-457">For example, the mixer uses the Direct3D device to mix substreams, deinterlace, and perform color adjustments.</span></span> <span data-ttu-id="73809-458">Decoder können das Direct3D-Gerät für die videobeschleunigte Decodierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="73809-458">Decoders can use the Direct3D device for video-accelerated decoding.</span></span> <span data-ttu-id="73809-459">(Weitere Informationen zur Videobeschleunigung finden Sie unter [DirectX Video Acceleration 2.0](directx-video-acceleration-2-0.md).)</span><span class="sxs-lookup"><span data-stu-id="73809-459">(For more information about video acceleration, see [DirectX Video Acceleration 2.0](directx-video-acceleration-2-0.md).)</span></span>

<span data-ttu-id="73809-460">Führen Sie zum Einrichten des Direct3D-Geräts die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="73809-460">To set up the Direct3D device, perform the following steps:</span></span>

1.  <span data-ttu-id="73809-461">Erstellen Sie das Direct3D-Objekt, indem Sie **Direct3DCreate9** oder **Direct3DCreate9Ex aufrufen.**</span><span class="sxs-lookup"><span data-stu-id="73809-461">Create the Direct3D object by calling **Direct3DCreate9** or **Direct3DCreate9Ex**.</span></span>
2.  <span data-ttu-id="73809-462">Erstellen Sie das Gerät, indem Sie **IDirect3D9::CreateDevice** oder **IDirect3D9Ex::CreateDevice aufrufen.**</span><span class="sxs-lookup"><span data-stu-id="73809-462">Create the device by calling **IDirect3D9::CreateDevice** or **IDirect3D9Ex::CreateDevice**.</span></span>
3.  <span data-ttu-id="73809-463">Erstellen Sie den Geräte-Manager, indem Sie [**DXVA2CreateDirect3DDeviceManager9 aufrufen.**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9)</span><span class="sxs-lookup"><span data-stu-id="73809-463">Create the device manager by calling [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9).</span></span>
4.  <span data-ttu-id="73809-464">Legen Sie das Gerät auf dem Geräte-Manager fest, indem [**Sie IDirect3DDeviceManager9::ResetDevice aufrufen.**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice)</span><span class="sxs-lookup"><span data-stu-id="73809-464">Set the device on the device manager by calling [**IDirect3DDeviceManager9::ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice).</span></span>

<span data-ttu-id="73809-465">Wenn eine andere Pipelinekomponente den Geräte-Manager benötigt, ruft sie AUF DER  EVR [**DEN DIENSTGETService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) auf und gibt MR_VIDEO_ACCELERATION_SERVICE für die Dienst-GUID an.</span><span class="sxs-lookup"><span data-stu-id="73809-465">If another pipeline component needs the device manager, it calls [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the EVR, specifying **MR_VIDEO_ACCELERATION_SERVICE** for the service GUID.</span></span> <span data-ttu-id="73809-466">Der EVR übergibt die Anforderung an den Moderator.</span><span class="sxs-lookup"><span data-stu-id="73809-466">The EVR passes the request to the presenter.</span></span> <span data-ttu-id="73809-467">Nachdem das Objekt den [**IDirect3DDeviceManager9-Zeiger**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) erhalten hat, kann es ein Handle für das Gerät erhalten, indem [**es IDirect3DDeviceManager9::OpenDeviceHandle aufruft.**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle)</span><span class="sxs-lookup"><span data-stu-id="73809-467">After the object gets the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) pointer, it can get a handle to the device by calling [**IDirect3DDeviceManager9::OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle).</span></span> <span data-ttu-id="73809-468">Wenn das Objekt das Gerät verwenden muss, übergibt es das Gerätehandchen an die [**IDirect3DDeviceManager9::LockDevice-Methode,**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) die einen **IDirect3DDevice9-Zeiger** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="73809-468">When the object needs to use the device, it passes the device handle to the [**IDirect3DDeviceManager9::LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) method, which returns an **IDirect3DDevice9** pointer.</span></span>

<span data-ttu-id="73809-469">Wenn der Moderator nach der Geräteeinrichtung das Gerät zerstört und ein neues erstellt, muss er [**ResetDevice erneut**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="73809-469">After the device is created, if the presenter destroys the device and creates a new one, the presenter must call [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) again.</span></span> <span data-ttu-id="73809-470">Die **ResetDevice-Methode** macht alle vorhandenen Gerätehandles ungültig, wodurch [**LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) **DXVA2_E_NEW_VIDEO_DEVICE.**</span><span class="sxs-lookup"><span data-stu-id="73809-470">The **ResetDevice** method invalidates any existing device handles, which causes [**LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) to return **DXVA2_E_NEW_VIDEO_DEVICE**.</span></span> <span data-ttu-id="73809-471">Dieser Fehlercode signalisiert anderen Objekten, die das Gerät verwenden, dass sie ein neues Gerätehand handle öffnen sollten.</span><span class="sxs-lookup"><span data-stu-id="73809-471">This error code signals to other objects using the device that they should open a new device handle.</span></span> <span data-ttu-id="73809-472">Weitere Informationen zur Verwendung des Geräte-Managers finden Sie unter [Direct3D Geräte-Manager](direct3d-device-manager.md).</span><span class="sxs-lookup"><span data-stu-id="73809-472">For more information about using the device manager, see [Direct3D Device Manager](direct3d-device-manager.md).</span></span>

<span data-ttu-id="73809-473">Der Moderator kann das Gerät im Fenstermodus oder im exklusiven Vollbildmodus erstellen.</span><span class="sxs-lookup"><span data-stu-id="73809-473">The presenter can create the device in windowed mode or full-screen exclusive mode.</span></span> <span data-ttu-id="73809-474">Für den Fenstermodus sollten Sie der Anwendung eine Möglichkeit bieten, das Videofenster anzugeben.</span><span class="sxs-lookup"><span data-stu-id="73809-474">For windowed mode, you should provide a way for the application to specify the video window.</span></span> <span data-ttu-id="73809-475">Die Standard-Moderatorin implementiert zu diesem Zweck [**die METHODE DURCHEVIDEODisplayControl::SetVideoWindow.**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow)</span><span class="sxs-lookup"><span data-stu-id="73809-475">The standard presenter implements the [**IMFVideoDisplayControl::SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) method for this purpose.</span></span> <span data-ttu-id="73809-476">Sie müssen das Gerät erstellen, wenn die Präsentation zum ersten Mal erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="73809-476">You must create the device when the presenter is first created.</span></span> <span data-ttu-id="73809-477">In der Regel kennen Sie derzeit nicht alle Geräteparameter, z. B. das Fenster oder das Format des Hintergrundpuffers.</span><span class="sxs-lookup"><span data-stu-id="73809-477">Typically, you won't know all of the device parameters at this time, such as the window or the back buffer format.</span></span> <span data-ttu-id="73809-478">Sie können ein temporäres Gerät erstellen und später durch&ersetzen. Denken Sie daran, \# [**ResetDevice im**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) Geräte-Manager aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="73809-478">You can create a temporary device and replace it later&\#;just remember to call [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) on the device manager.</span></span>

<span data-ttu-id="73809-479">Wenn Sie ein neues Gerät erstellen oder **IDirect3DDevice9::Reset** oder **IDirect3DDevice9Ex::ResetEx** auf einem vorhandenen Gerät aufrufen, senden Sie ein [**EC_DISPLAY_CHANGED-Ereignis an**](../directshow/ec-display-changed.md) die EVR.</span><span class="sxs-lookup"><span data-stu-id="73809-479">If you create a new device, or if you call **IDirect3DDevice9::Reset** or **IDirect3DDevice9Ex::ResetEx** on an existing device, send an [**EC_DISPLAY_CHANGED**](../directshow/ec-display-changed.md) event to the EVR.</span></span> <span data-ttu-id="73809-480">Dieses Ereignis benachrichtigt den EVR, den Medientyp erneut zu ausgehandelt.</span><span class="sxs-lookup"><span data-stu-id="73809-480">This event notifies the EVR to renegotiate the media type.</span></span> <span data-ttu-id="73809-481">Der EVR ignoriert die Ereignisparameter für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="73809-481">The EVR ignores the event parameters for this event.</span></span>

### <a name="allocating-direct3d-surfaces"></a><span data-ttu-id="73809-482">Zuordnen von Direct3D-Oberflächen</span><span class="sxs-lookup"><span data-stu-id="73809-482">Allocating Direct3D Surfaces</span></span>

<span data-ttu-id="73809-483">Nachdem der Moderator den Medientyp definiert hat, kann er die Direct3D-Oberflächen zuordnen, die der Mixer zum Schreiben der Videoframes verwendet.</span><span class="sxs-lookup"><span data-stu-id="73809-483">After the presenter sets the media type, it can allocate the Direct3D surfaces, which the mixer will use to write the video frames.</span></span> <span data-ttu-id="73809-484">Die Oberfläche muss mit dem Medientyp des Moderators übereinstimmen:</span><span class="sxs-lookup"><span data-stu-id="73809-484">The surface must match the presenter's media type:</span></span>

-   <span data-ttu-id="73809-485">Das Oberflächenformat muss mit dem Medienuntertyp übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="73809-485">The surface format must match the media subtype.</span></span> <span data-ttu-id="73809-486">Wenn der Untertyp beispielsweise MFVideoFormat_RGB24 **ist,** muss das Oberflächenformat **D3DFMT_X8R8G8B8.**</span><span class="sxs-lookup"><span data-stu-id="73809-486">For example, if the subtype is **MFVideoFormat_RGB24**, the surface format must be **D3DFMT_X8R8G8B8**.</span></span> <span data-ttu-id="73809-487">Weitere Informationen zu Untertypen und Direct3D-Formaten finden Sie unter [Video Subtype GUIDs](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="73809-487">For more information about subtypes and Direct3D formats, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>
-   <span data-ttu-id="73809-488">Die Breite und Höhe der Oberfläche muss mit den Dimensionen übereinstimmen, die im [**MF_MT_FRAME_SIZE-Attribut**](mf-mt-frame-size-attribute.md) des Medientyps angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="73809-488">The surface width and height must match the dimensions given in the [**MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) attribute of the media type.</span></span>

<span data-ttu-id="73809-489">Die empfohlene Methode zum Zuordnen von Oberflächen hängt davon ab, ob die Präsentation im Fenstermodus oder im Vollbildmodus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="73809-489">The recommended way to allocate surfaces depends on whether the presenter runs windowed or full-screen.</span></span>

<span data-ttu-id="73809-490">Wenn für das Direct3D-Gerät ein Fenster angezeigt wird, können Sie mehrere Swapketten mit jeweils einem einzelnen Hintergrundpuffer erstellen.</span><span class="sxs-lookup"><span data-stu-id="73809-490">If the Direct3D device is windowed, you can create several swap chains, each with a single back buffer.</span></span> <span data-ttu-id="73809-491">Bei diesem Ansatz können Sie jede Oberfläche unabhängig voneinander präsentieren, da die Präsentation einer Auslagerungskette die anderen Austauschketten nicht beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="73809-491">Using this approach, you can present each surface independently, because presenting one swap chain will not interfere with the other swap chains.</span></span> <span data-ttu-id="73809-492">Der Mixer kann Daten auf eine Oberfläche schreiben, während eine andere Oberfläche für die Präsentation geplant ist.</span><span class="sxs-lookup"><span data-stu-id="73809-492">The mixer can write data to a surface while another surface is scheduled for presentation.</span></span>

<span data-ttu-id="73809-493">Entscheiden Sie zunächst, wie viele Swapketten erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="73809-493">First, decide how many swap chains to create.</span></span> <span data-ttu-id="73809-494">Es werden mindestens drei empfohlen.</span><span class="sxs-lookup"><span data-stu-id="73809-494">A minimum of three is recommended.</span></span> <span data-ttu-id="73809-495">Führen Sie für jede Auslagerungskette folgende Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="73809-495">For each swap chain, do the following:</span></span>

1.  <span data-ttu-id="73809-496">Rufen **Sie IDirect3DDevice9::CreateAdditionalSwapChain** auf, um die Swapkette zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="73809-496">Call **IDirect3DDevice9::CreateAdditionalSwapChain** to create the swap chain.</span></span>
2.  <span data-ttu-id="73809-497">Rufen **Sie IDirect3DSwapChain9::GetBackBuffer** auf, um einen Zeiger auf die Hintergrundpufferoberfläche der Austauschkette zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="73809-497">Call **IDirect3DSwapChain9::GetBackBuffer** to get a pointer to the swap chain's back buffer surface.</span></span>
3.  <span data-ttu-id="73809-498">Rufen [**Sie MFCreateVideoSampleFromSurface auf,**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) und übergeben Sie einen Zeiger auf die Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="73809-498">Call [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) and pass in a pointer to the surface.</span></span> <span data-ttu-id="73809-499">Diese Funktion gibt einen Zeiger auf ein Videobeispielobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="73809-499">This function returns a pointer to a video sample object.</span></span> <span data-ttu-id="73809-500">Das Videobeispielobjekt implementiert die [**METHODESAMPLE-Schnittstelle,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) und der Moderator verwendet diese Schnittstelle, um die Oberfläche an den Mixer zu übertragen, wenn der Moderator die [**METHODE "VORZEIGETransform::P rocessOutput"**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) des Mixers aufruft.</span><span class="sxs-lookup"><span data-stu-id="73809-500">The video sample object implements the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, and the presenter uses this interface to deliver the surface to the mixer when the presenter calls the mixer's [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) method.</span></span> <span data-ttu-id="73809-501">Weitere Informationen zum Videobeispielobjekt finden Sie unter [Videobeispiele.](video-samples.md)</span><span class="sxs-lookup"><span data-stu-id="73809-501">For more information about the video sample object, see [Video Samples](video-samples.md).</span></span>
4.  <span data-ttu-id="73809-502">Speichern Sie [**den WARTESCHLANGENsample-Zeiger**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) in einer Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="73809-502">Store the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) pointer in a queue.</span></span> <span data-ttu-id="73809-503">Der Presenter pullt Während der Verarbeitung Stichproben aus dieser Warteschlange, wie unter [Processing Output (Verarbeiten der Ausgabe) beschrieben.](#processing-output)</span><span class="sxs-lookup"><span data-stu-id="73809-503">The presenter will pull samples from this queue during processing as described in [Processing Output](#processing-output).</span></span>
5.  <span data-ttu-id="73809-504">Behalten Sie einen Verweis auf den **IDirect3DSwapChain9-Zeiger** bei, damit die Swapkette nicht freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="73809-504">Keep a reference to the **IDirect3DSwapChain9** pointer so the swap chain is not released.</span></span>

<span data-ttu-id="73809-505">Im exklusiven Vollbildmodus kann das Gerät nicht mehr als eine Auslagerungskette haben.</span><span class="sxs-lookup"><span data-stu-id="73809-505">In full-screen exclusive mode, the device cannot have more than one swap chain.</span></span> <span data-ttu-id="73809-506">Diese Swapkette wird implizit erstellt, wenn Sie das Vollbildgerät erstellen.</span><span class="sxs-lookup"><span data-stu-id="73809-506">This swap chain is created implicitly when you create the full-screen device.</span></span> <span data-ttu-id="73809-507">Die Auslagerungskette kann mehr als einen Hintergrundpuffer haben.</span><span class="sxs-lookup"><span data-stu-id="73809-507">The swap chain can have more than one back buffer.</span></span> <span data-ttu-id="73809-508">Wenn Sie jedoch einen Hintergrundpuffer präsentieren, während Sie in einen anderen Hintergrundpuffer in derselben Swapkette schreiben, gibt es keine einfache Möglichkeit, die beiden Vorgänge zu koordinieren.</span><span class="sxs-lookup"><span data-stu-id="73809-508">Unfortunately, however, if you present one back buffer while you write to another back buffer in the same swap chain, there is no easy way to coordinate the two operations.</span></span> <span data-ttu-id="73809-509">Dies liegt an der Art und Weise, wie Direct3D Das Spiegeln von Oberflächen implementiert.</span><span class="sxs-lookup"><span data-stu-id="73809-509">This is because of the way Direct3D implements surface flipping.</span></span> <span data-ttu-id="73809-510">Wenn Sie Present aufrufen, aktualisiert der Grafiktreiber die Surface-Zeiger im Grafikspeicher.</span><span class="sxs-lookup"><span data-stu-id="73809-510">When you call Present, the graphics driver updates the surface pointers in graphics memory.</span></span> <span data-ttu-id="73809-511">Wenn Sie beim Aufrufen von **Present** **IDirect3DSurface9-Zeiger** halten, zeigen diese auf verschiedene Puffer, nachdem der **Present-Aufruf** zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="73809-511">If you are holding any **IDirect3DSurface9** pointers when you call **Present**, they will point to different buffers after the **Present** call returns.</span></span>

<span data-ttu-id="73809-512">Die einfachste Möglichkeit besteht in der Erstellung eines Videobeispiels für die Austauschkette.</span><span class="sxs-lookup"><span data-stu-id="73809-512">The simplest option is to create one video sample for the swap chain.</span></span> <span data-ttu-id="73809-513">Wenn Sie diese Option auswählen, führen Sie die gleichen Schritte wie für den Fenstermodus aus.</span><span class="sxs-lookup"><span data-stu-id="73809-513">If you choose this option, follow the same steps given for windowed mode.</span></span> <span data-ttu-id="73809-514">Der einzige Unterschied ist, dass die Beispielwarteschlange ein einzelnes Videobeispiel enthält.</span><span class="sxs-lookup"><span data-stu-id="73809-514">The only difference is that the sample queue contains a single video sample.</span></span> <span data-ttu-id="73809-515">Eine weitere Möglichkeit ist das Erstellen von Offscreenoberflächen und das anschließende Aufschneiden in den Hintergrundpuffer.</span><span class="sxs-lookup"><span data-stu-id="73809-515">Another option is to create offscreen surfaces and then blit them to the back buffer.</span></span> <span data-ttu-id="73809-516">Die von Ihnen erstellten Oberflächen müssen die [**IDirectXVideoProcessor::VideoProcessBlt-Methode**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) unterstützen, die der Mixer zum Zusammenstellen der Ausgabeframes verwendet.</span><span class="sxs-lookup"><span data-stu-id="73809-516">The surfaces that you create must support the [**IDirectXVideoProcessor::VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) method, which the mixer uses to composite the output frames.</span></span>

### <a name="tracking-samples"></a><span data-ttu-id="73809-517">Überwachungsbeispiele</span><span class="sxs-lookup"><span data-stu-id="73809-517">Tracking Samples</span></span>

<span data-ttu-id="73809-518">Wenn die Moderatorin die Videobeispiele zum ersten Mal zuteilen, werden sie in eine Warteschlange gestellt.</span><span class="sxs-lookup"><span data-stu-id="73809-518">When the presenter first allocates the video samples, it places them in a queue.</span></span> <span data-ttu-id="73809-519">Der Presenter zeichnet immer dann aus dieser Warteschlange, wenn er einen neuen Frame aus dem Mixer erhalten muss.</span><span class="sxs-lookup"><span data-stu-id="73809-519">The presenter draws from this queue whenever it needs to get a new frame from the mixer.</span></span> <span data-ttu-id="73809-520">Nachdem der Mixer den Frame ausgegeben hat, verschiebt der Moderator das Beispiel in eine zweite Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="73809-520">After the mixer outputs the frame, the presenter moves the sample into a second queue.</span></span> <span data-ttu-id="73809-521">Die zweite Warteschlange ist für Beispiele vorgesehen, die auf ihre geplanten Präsentationszeiten warten.</span><span class="sxs-lookup"><span data-stu-id="73809-521">The second queue is for samples that are waiting for their scheduled presentation times.</span></span>

<span data-ttu-id="73809-522">Um das Nachverfolgen des Status der einzelnen Stichproben zu vereinfachen, implementiert das Videobeispielobjekt die [**BENUTZEROBERFLÄCHETRACKedSample-Schnittstelle.**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)</span><span class="sxs-lookup"><span data-stu-id="73809-522">To make it easier to track the status of each sample, the video sample object implements the [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) interface.</span></span> <span data-ttu-id="73809-523">Sie können diese Schnittstelle wie folgt verwenden:</span><span class="sxs-lookup"><span data-stu-id="73809-523">You can use this interface as follows:</span></span>

1.  <span data-ttu-id="73809-524">Implementieren Sie [**dieASYNCCallback-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) in Ihrer Präsentation.</span><span class="sxs-lookup"><span data-stu-id="73809-524">Implement the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface in your presenter.</span></span>
2.  <span data-ttu-id="73809-525">Bevor Sie ein Beispiel in der geplanten Warteschlange platzieren, fragen Sie das Videobeispielobjekt für die [**BENUTZEROBERFLÄCHENTtrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) ab.</span><span class="sxs-lookup"><span data-stu-id="73809-525">Before you place a sample in the scheduled queue, query the video sample object for the [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) interface.</span></span>

3.  <span data-ttu-id="73809-526">Rufen Sie MIT EINEM Zeiger auf Ihre Rückrufschnittstelle [**DEN CALLTrackedSample::SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) auf.</span><span class="sxs-lookup"><span data-stu-id="73809-526">Call [**IMFTrackedSample::SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) with a pointer to your callback interface.</span></span>
4.  <span data-ttu-id="73809-527">Wenn das Beispiel zur Präsentation bereit ist, entfernen Sie es aus der geplanten Warteschlange, stellen Sie es vor, und geben Sie alle Verweise auf das Beispiel frei.</span><span class="sxs-lookup"><span data-stu-id="73809-527">When the sample is ready for presentation, remove it from the scheduled queue, present it, and release all references to the sample.</span></span>
5.  <span data-ttu-id="73809-528">Im Beispiel wird der Rückruf aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="73809-528">The sample invokes the callback.</span></span> <span data-ttu-id="73809-529">(Das Beispielobjekt wird in diesem Fall nicht gelöscht, da es einen Verweiszähler für sich selbst enthält, bis der Rückruf aufgerufen wird.)</span><span class="sxs-lookup"><span data-stu-id="73809-529">(The sample object is not deleted in this case because it holds a reference count on itself until the callback is invoked.)</span></span>
6.  <span data-ttu-id="73809-530">Geben Sie innerhalb des Rückrufs das Beispiel an die verfügbare Warteschlange zurück.</span><span class="sxs-lookup"><span data-stu-id="73809-530">Inside the callback, return the sample to the available queue.</span></span>

<span data-ttu-id="73809-531">Eine Moderatorin ist nicht erforderlich, um [**MITTTTrackedSample Beispiele**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) nachverfolgungen zu können. Sie können jede Technik implementieren, die für Ihren Entwurf am besten funktioniert.</span><span class="sxs-lookup"><span data-stu-id="73809-531">A presenter is not required to use [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) to track samples; you can implement any technique that works best for your design.</span></span> <span data-ttu-id="73809-532">Ein Vorteil von **RENDERTrackedSample** ist, dass Sie die Planungs- und Renderingfunktionen des Moderators in Hilfsobjekte verschieben können, und diese Objekte benötigen keinen speziellen Mechanismus zum Aufrufen zurück an den Moderator, wenn sie Videobeispiele veröffentlichen, da das Beispielobjekt diesen Mechanismus bietet.</span><span class="sxs-lookup"><span data-stu-id="73809-532">One advantage of **IMFTrackedSample** is that you can move the presenter's scheduling and rendering functions into helper objects, and these objects do not need any special mechanism for calling back to the presenter when they release video samples because the sample object provides that mechanism.</span></span>

<span data-ttu-id="73809-533">Der folgende Code zeigt, wie der Rückruf festgelegt wird:</span><span class="sxs-lookup"><span data-stu-id="73809-533">The following code shows how to set the callback:</span></span>


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



<span data-ttu-id="73809-534">Rufen Sie im Rückruf [**DIEASYNCResult::GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject) für das asynchrone Ergebnisobjekt auf, um einen Zeiger auf das Beispiel abzurufen:</span><span class="sxs-lookup"><span data-stu-id="73809-534">In the callback, call [**IMFAsyncResult::GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject) on the asynchronous result object to retrieve a pointer to the sample:</span></span>


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

    /*** Begin lock ***/

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

    /*** End lock ***/

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



## <a name="processing-output"></a><span data-ttu-id="73809-535">Verarbeiten der Ausgabe</span><span class="sxs-lookup"><span data-stu-id="73809-535">Processing Output</span></span>

<span data-ttu-id="73809-536">Wenn der Mixer ein neues Eingabebeispiel empfängt, sendet der EVR eine MFVP_MESSAGE_PROCESSINPUTNOTIFY **nachricht** an den Moderator.</span><span class="sxs-lookup"><span data-stu-id="73809-536">Whenever the mixer receives a new input sample, the EVR sends an **MFVP_MESSAGE_PROCESSINPUTNOTIFY** message to the presenter.</span></span> <span data-ttu-id="73809-537">Diese Meldung gibt an, dass der Mixer möglicherweise über einen neuen Videoframe für die Bereitstellung verfügen kann.</span><span class="sxs-lookup"><span data-stu-id="73809-537">This message indicates that the mixer might have a new video frame to deliver.</span></span> <span data-ttu-id="73809-538">Als Antwort ruft die Moderatorin [**IM MIXERTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) auf.</span><span class="sxs-lookup"><span data-stu-id="73809-538">In response, the presenter calls [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) on the mixer.</span></span> <span data-ttu-id="73809-539">Wenn die Methode erfolgreich ist, wird das Beispiel von der Präsentation geplant.</span><span class="sxs-lookup"><span data-stu-id="73809-539">If the method succeeds, the presenter schedules the sample for presentation.</span></span>

<span data-ttu-id="73809-540">Führen Sie die folgenden Schritte aus, um die Ausgabe des Mixers zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="73809-540">To get output from the mixer, perform the following steps:</span></span>

1.  <span data-ttu-id="73809-541">Überprüfen Sie den Uhrzustand.</span><span class="sxs-lookup"><span data-stu-id="73809-541">Check the clock state.</span></span> <span data-ttu-id="73809-542">Wenn die Uhr angehalten ist, ignorieren Sie die **MFVP_MESSAGE_PROCESSINPUTNOTIFY,** es sei denn, dies ist der erste Videoframe.</span><span class="sxs-lookup"><span data-stu-id="73809-542">If the clock is paused, ignore the **MFVP_MESSAGE_PROCESSINPUTNOTIFY** message unless this is the first video frame.</span></span> <span data-ttu-id="73809-543">Wenn die Uhr ausgeführt wird oder dies der erste Videoframe ist, fahren Sie fort.</span><span class="sxs-lookup"><span data-stu-id="73809-543">If the clock is running, or if this is the first video frame, continue.</span></span>
2.  <span data-ttu-id="73809-544">Hier finden Sie ein Beispiel aus der Warteschlange der verfügbaren Beispiele.</span><span class="sxs-lookup"><span data-stu-id="73809-544">Get a sample from the queue of available samples.</span></span> <span data-ttu-id="73809-545">Wenn die Warteschlange leer ist, bedeutet dies, dass derzeit alle zugeordneten Stichproben für die Präsentation geplant sind.</span><span class="sxs-lookup"><span data-stu-id="73809-545">If the queue is empty, it means that all allocated samples are currently scheduled for presenting.</span></span> <span data-ttu-id="73809-546">Ignorieren Sie in diesem Fall **die MFVP_MESSAGE_PROCESSINPUTNOTIFY** Nachricht.</span><span class="sxs-lookup"><span data-stu-id="73809-546">In that case, ignore the **MFVP_MESSAGE_PROCESSINPUTNOTIFY** message at this time.</span></span> <span data-ttu-id="73809-547">Wenn das nächste Beispiel verfügbar ist, wiederholen Sie die hier aufgeführten Schritte.</span><span class="sxs-lookup"><span data-stu-id="73809-547">When the next sample becomes available, repeat the steps listed here.</span></span>
3.  <span data-ttu-id="73809-548">(Optional.) Wenn die Uhr verfügbar ist, rufen Sie die aktuelle Uhrzeit (*T1*) ab, indem [**Sie DENKlock::GetCorrelatedTime aufrufen.**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime)</span><span class="sxs-lookup"><span data-stu-id="73809-548">(Optional.) If the clock is available, get the current clock time (*T1*) by calling [**IMFClock::GetCorrelatedTime**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime).</span></span>
4.  <span data-ttu-id="73809-549">Rufen [**Sie IM MIXERTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) auf.</span><span class="sxs-lookup"><span data-stu-id="73809-549">Call [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) on the mixer.</span></span> <span data-ttu-id="73809-550">Wenn **ProcessOutput erfolgreich** ist, enthält das Beispiel einen Videoframe.</span><span class="sxs-lookup"><span data-stu-id="73809-550">If **ProcessOutput** succeeds, the sample contains a video frame.</span></span> <span data-ttu-id="73809-551">Wenn bei der Methode ein Fehler auftritt, überprüfen Sie den Rückgabecode.</span><span class="sxs-lookup"><span data-stu-id="73809-551">If the method fails, check the return code.</span></span> <span data-ttu-id="73809-552">Die folgenden Fehlercodes aus **ProcessOutput** sind keine kritischen Fehler:</span><span class="sxs-lookup"><span data-stu-id="73809-552">The following error codes from **ProcessOutput** are not critical failures:</span></span>

    

    | <span data-ttu-id="73809-553">Fehlercode</span><span class="sxs-lookup"><span data-stu-id="73809-553">Error code</span></span>                              | <span data-ttu-id="73809-554">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="73809-554">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                    |
    |-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="73809-555">**MF_E_TRANSFORM_NEED_MORE_INPUT**</span><span class="sxs-lookup"><span data-stu-id="73809-555">**MF_E_TRANSFORM_NEED_MORE_INPUT**</span></span> | <span data-ttu-id="73809-556">Der Mixer benötigt mehr Eingaben, bevor er einen neuen Ausgaberahmen erzeugen kann.</span><span class="sxs-lookup"><span data-stu-id="73809-556">The mixer needs more input before it can produce a new output frame.</span></span><br/> <span data-ttu-id="73809-557">Wenn Sie diesen Fehlercode erhalten, überprüfen Sie, ob die EVR das Ende des Streams erreicht hat, und antworten Sie entsprechend, wie unter [Ende des Streams beschrieben.](#end-of-stream)</span><span class="sxs-lookup"><span data-stu-id="73809-557">If you get this error code, check whether the EVR has reached the end of the stream and respond accordingly, as described in [End of Stream](#end-of-stream).</span></span> <span data-ttu-id="73809-558">Ignorieren Sie andernfalls **MF_E_TRANSFORM_NEED_MORE_INPUT** Meldung.</span><span class="sxs-lookup"><span data-stu-id="73809-558">Otherwise, ignore this **MF_E_TRANSFORM_NEED_MORE_INPUT** message.</span></span> <span data-ttu-id="73809-559">Der EVR sendet eine weitere, wenn der Mixer mehr Eingaben erhält.</span><span class="sxs-lookup"><span data-stu-id="73809-559">The EVR will send another one when the mixer gets more input.</span></span><br/> |
    | <span data-ttu-id="73809-560">**MF_E_TRANSFORM_STREAM_CHANGE**</span><span class="sxs-lookup"><span data-stu-id="73809-560">**MF_E_TRANSFORM_STREAM_CHANGE**</span></span>    | <span data-ttu-id="73809-561">Der Ausgabetyp des Mixers ist ungültig geworden, möglicherweise aufgrund einer Formatänderung im Upstream.</span><span class="sxs-lookup"><span data-stu-id="73809-561">The mixer's output type has become invalid, possibly due to a format change upstream.</span></span><br/> <span data-ttu-id="73809-562">Wenn Sie diesen Fehlercode erhalten, legen Sie den Medientyp des Presenters auf **NULL fest.**</span><span class="sxs-lookup"><span data-stu-id="73809-562">If you get this error code, set the presenter's media type to **NULL**.</span></span> <span data-ttu-id="73809-563">Der EVR fordert ein neues Format an.</span><span class="sxs-lookup"><span data-stu-id="73809-563">The EVR will request a new format.</span></span><br/>                                                                                                                                                                         |
    | <span data-ttu-id="73809-564">**MF_E_TRANSFORM_TYPE_NOT_SET**</span><span class="sxs-lookup"><span data-stu-id="73809-564">**MF_E_TRANSFORM_TYPE_NOT_SET**</span></span>    | <span data-ttu-id="73809-565">Der Mixer erfordert einen neuen Medientyp.</span><span class="sxs-lookup"><span data-stu-id="73809-565">The mixer requires a new media type.</span></span><br/> <span data-ttu-id="73809-566">Wenn Sie diesen Fehlercode erhalten, können Sie den Ausgabetyp des Mixers erneut aushandeln, wie unter [Aushandeln von Formaten beschrieben.](#negotiating-formats)</span><span class="sxs-lookup"><span data-stu-id="73809-566">If you get this error code, renegotiate the mixer's output type as described in [Negotiating Formats](#negotiating-formats).</span></span><br/>                                                                                                                                                                                                        |

    

     

    <span data-ttu-id="73809-567">Wenn [**ProcessOutput erfolgreich**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) ist, fahren Sie fort.</span><span class="sxs-lookup"><span data-stu-id="73809-567">If [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) succeeds, continue.</span></span>

5.  <span data-ttu-id="73809-568">(Optional.) Wenn die Uhr verfügbar ist, erhalten Sie die aktuelle Uhrzeit (*T2*).</span><span class="sxs-lookup"><span data-stu-id="73809-568">(Optional.) If the clock is available, get the current clock time (*T2*).</span></span> <span data-ttu-id="73809-569">Die vom Mixer eingeführte Latenzzeit beträgt (*T2*  -  *T1*).</span><span class="sxs-lookup"><span data-stu-id="73809-569">The amount of latency introduced by the mixer is (*T2* - *T1*).</span></span> <span data-ttu-id="73809-570">Senden Sie **EC_PROCESSING_LATENCY** Ereignis mit diesem Wert an die EVR.</span><span class="sxs-lookup"><span data-stu-id="73809-570">Send an **EC_PROCESSING_LATENCY** event with this value to the EVR.</span></span> <span data-ttu-id="73809-571">Der EVR verwendet diesen Wert für die Qualitätskontrolle.</span><span class="sxs-lookup"><span data-stu-id="73809-571">The EVR uses this value for quality control.</span></span> <span data-ttu-id="73809-572">Wenn keine Uhr verfügbar ist, gibt es keinen Grund, das Ereignis **EC_PROCESSING_LATENCY** senden.</span><span class="sxs-lookup"><span data-stu-id="73809-572">If no clock is available, there is no reason to send the **EC_PROCESSING_LATENCY** event.</span></span>
6.  <span data-ttu-id="73809-573">(Optional.) Fragen Sie das Beispiel [**für DIETTTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) ab, und rufen Sie [**DANNTrackedSample::SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) auf, wie unter [Tracking Samples (Nachverfolgungsbeispiele) beschrieben.](#tracking-samples)</span><span class="sxs-lookup"><span data-stu-id="73809-573">(Optional.) Query the sample for [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) and call [**IMFTrackedSample::SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) as described in [Tracking Samples](#tracking-samples).</span></span>
7.  <span data-ttu-id="73809-574">Planen Sie das Beispiel für die Präsentation.</span><span class="sxs-lookup"><span data-stu-id="73809-574">Schedule the sample for presentation.</span></span>

<span data-ttu-id="73809-575">Diese Sequenz von Schritten kann beendet werden, bevor der Moderator eine Ausgabe vom Mixer erhält.</span><span class="sxs-lookup"><span data-stu-id="73809-575">This sequence of steps can terminate before the presenter gets any output from the mixer.</span></span> <span data-ttu-id="73809-576">Um sicherzustellen, dass keine Anforderungen gelöscht werden, sollten Sie dieselben Schritte wiederholen, wenn Folgendes auftritt:</span><span class="sxs-lookup"><span data-stu-id="73809-576">To ensure that no requests are dropped, you should repeat the same steps when the following occur:</span></span>

-   <span data-ttu-id="73809-577">Die METHODE [**DER PRÄSENTATIONClockStateSink::OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) oder **DERENTLOCKSTATESink::OnClockStart** wird aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="73809-577">The presenter's [**IMFClockStateSink::OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) or **IMFClockStateSink::OnClockStart** method is called.</span></span> <span data-ttu-id="73809-578">Dies behandelt den Fall, in dem der Mixer Eingaben ignoriert, da die Uhr angehalten wird (Schritt 1).</span><span class="sxs-lookup"><span data-stu-id="73809-578">This handles the case where the mixer ignores input because the clock is paused (step 1).</span></span>
-   <span data-ttu-id="73809-579">Der [**RÜCKRUFTrackedSample-Rückruf**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) wird aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="73809-579">The [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) callback is invoked.</span></span> <span data-ttu-id="73809-580">Dies behandelt den Fall, in dem der Mixer Eingaben empfängt, aber alle Videobeispiele des Moderators verwendet werden (Schritt 2).</span><span class="sxs-lookup"><span data-stu-id="73809-580">This handles the case where the mixer receives input but all of the presenter's video samples are in use (step 2).</span></span>

<span data-ttu-id="73809-581">Die nächsten Codebeispiele zeigen diese Schritte ausführlicher.</span><span class="sxs-lookup"><span data-stu-id="73809-581">The next several code examples show these steps in more detail.</span></span> <span data-ttu-id="73809-582">Der Presenter ruft die -Methode auf (wie im folgenden Beispiel gezeigt), wenn sie die MFVP_MESSAGE_PROCESSINPUTNOTIFY `ProcessInputNotify` erhält. </span><span class="sxs-lookup"><span data-stu-id="73809-582">The presenter calls the `ProcessInputNotify` method (shown in the following example) when it gets the **MFVP_MESSAGE_PROCESSINPUTNOTIFY** message.</span></span>


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



<span data-ttu-id="73809-583">Diese `ProcessInputNotify` Methode legt ein boolesches Flag fest, um die Tatsache zu erfassen, dass der Mixer über eine neue Eingabe verfügt.</span><span class="sxs-lookup"><span data-stu-id="73809-583">This `ProcessInputNotify` method sets a Boolean flag to record the fact that the mixer has new input.</span></span> <span data-ttu-id="73809-584">Anschließend ruft sie die `ProcessOutputLoop` -Methode auf, die im nächsten Beispiel gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="73809-584">Then it calls the `ProcessOutputLoop` method, shown in the next example.</span></span> <span data-ttu-id="73809-585">Diese Methode versucht, so viele Beispiele wie möglich aus dem Mixer zu pullen:</span><span class="sxs-lookup"><span data-stu-id="73809-585">This method attempts to pull as many samples as possible from the mixer:</span></span>


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



<span data-ttu-id="73809-586">Die `ProcessOutput` -Methode, die im nächsten Beispiel gezeigt wird, versucht, einen einzelnen Videoframe aus dem Mixer zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="73809-586">The `ProcessOutput` method, shown in the next example, attempts to get a single video frame from the mixer.</span></span> <span data-ttu-id="73809-587">Wenn kein Videoframe verfügbar ist, gibt S_FALSE oder einen Fehlercode zurück, der die `ProcessSample` Schleife in `ProcessOutputLoop` unterbricht.</span><span class="sxs-lookup"><span data-stu-id="73809-587">If no video frame is available, `ProcessSample` returns S_FALSE or an error code, either of which interrupts the loop in `ProcessOutputLoop`.</span></span> <span data-ttu-id="73809-588">Der Großteil der Arbeit erfolgt innerhalb der `ProcessOutput` -Methode:</span><span class="sxs-lookup"><span data-stu-id="73809-588">Most of the work is done inside the `ProcessOutput` method:</span></span>


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



<span data-ttu-id="73809-589">Einige Hinweise zu diesem Beispiel:</span><span class="sxs-lookup"><span data-stu-id="73809-589">Some remarks about this example:</span></span>

-   <span data-ttu-id="73809-590">Die *m_SamplePool* Variable wird als Sammlungsobjekt angenommen, das die Warteschlange der verfügbaren Videobeispiele enthält.</span><span class="sxs-lookup"><span data-stu-id="73809-590">The *m_SamplePool* variable is assumed to be a collection object that holds the queue of available video samples.</span></span> <span data-ttu-id="73809-591">Die -Methode des `GetSample` -Objekts gibt MF_E_SAMPLEALLOCATOR_EMPTY zurück, wenn  die Warteschlange leer ist.</span><span class="sxs-lookup"><span data-stu-id="73809-591">The object's `GetSample` method returns **MF_E_SAMPLEALLOCATOR_EMPTY** if the queue is empty.</span></span>
-   <span data-ttu-id="73809-592">Wenn die [**ProcessOutput-Methode**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) des Mixers MF_E_TRANSFORM_NEED_MORE_INPUT zurückgibt, bedeutet dies, dass der Mixer keine weitere Ausgabe erzeugen kann, sodass der Moderator das m_fSampleNotify *wird.*</span><span class="sxs-lookup"><span data-stu-id="73809-592">If the mixer's [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) method returns MF_E_TRANSFORM_NEED_MORE_INPUT, it means the mixer cannot produce any more output, so the presenter clears the *m_fSampleNotify* flag.</span></span>
-   <span data-ttu-id="73809-593">Die `TrackSample` -Methode, mit der der [**RÜCKRUF VON DURCHTTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) bestimmt wird, wird im Abschnitt Tracking Samples [(Nachverfolgungsbeispiele) gezeigt.](#tracking-samples)</span><span class="sxs-lookup"><span data-stu-id="73809-593">The `TrackSample` method, which sets the [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) callback, is shown in the section [Tracking Samples](#tracking-samples).</span></span>

### <a name="repainting-frames"></a><span data-ttu-id="73809-594">Neupaintieren von Frames</span><span class="sxs-lookup"><span data-stu-id="73809-594">Repainting Frames</span></span>

<span data-ttu-id="73809-595">Gelegentlich muss der Moderator möglicherweise den neuesten Videoframe neu anpainten.</span><span class="sxs-lookup"><span data-stu-id="73809-595">Occasionally the presenter might need to repaint the most recent video frame.</span></span> <span data-ttu-id="73809-596">Beispielsweise wird der Rahmen von der Standard-Moderatorin in den folgenden Situationen neu gepaint:</span><span class="sxs-lookup"><span data-stu-id="73809-596">For example, the standard presenter repaints the frame in the following situations:</span></span>

-   <span data-ttu-id="73809-597">Im Fenstermodus als Reaktion auf **WM_PAINT,** die vom Fenster der Anwendung empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="73809-597">In windowed mode, in response to **WM_PAINT** messages received by the application's window.</span></span> <span data-ttu-id="73809-598">Weitere [**Informationen finden Sie unter ATTRIBUTEVideoDisplayControl::RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo).</span><span class="sxs-lookup"><span data-stu-id="73809-598">See [**IMFVideoDisplayControl::RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo).</span></span>
-   <span data-ttu-id="73809-599">Wenn sich das Zielrechteck ändert, wenn die Anwendung [**DIEVIDEODisplayControl::SetVideoPosition aufruft.**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition)</span><span class="sxs-lookup"><span data-stu-id="73809-599">If the destination rectangle changes when the application calls [**IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span></span>

<span data-ttu-id="73809-600">Führen Sie die folgenden Schritte aus, um den Mixer an fordern, den neuesten Frame neu zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="73809-600">Use the following steps to request the mixer to re-create the most recent frame:</span></span>

1.  <span data-ttu-id="73809-601">Hier erhalten Sie ein Videobeispiel aus der Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="73809-601">Get a video sample from the queue.</span></span>
2.  <span data-ttu-id="73809-602">Fragen Sie das Beispiel für die [**BENUTZEROBERFLÄCHEDesiredSample-Schnittstelle**](/windows/desktop/api/evr/nn-evr-imfdesiredsample) ab.</span><span class="sxs-lookup"><span data-stu-id="73809-602">Query the sample for the [**IMFDesiredSample**](/windows/desktop/api/evr/nn-evr-imfdesiredsample) interface.</span></span>
3.  <span data-ttu-id="73809-603">Rufen [**Sie DANNDESiredSample::SetDesiredSampleTimeAndDuration auf.**](/windows/desktop/api/evr/nf-evr-imfdesiredsample-setdesiredsampletimeandduration)</span><span class="sxs-lookup"><span data-stu-id="73809-603">Call [**IMFDesiredSample::SetDesiredSampleTimeAndDuration**](/windows/desktop/api/evr/nf-evr-imfdesiredsample-setdesiredsampletimeandduration).</span></span> <span data-ttu-id="73809-604">Geben Sie den Zeitstempel des letzten Videoframes an.</span><span class="sxs-lookup"><span data-stu-id="73809-604">Specify the time stamp of the most recent video frame.</span></span> <span data-ttu-id="73809-605">(Sie müssen diesen Wert zwischenspeichern und für jeden Frame aktualisieren.)</span><span class="sxs-lookup"><span data-stu-id="73809-605">(You will need to cache this value and update it for each frame.)</span></span>
4.  <span data-ttu-id="73809-606">Rufen [**Sie ProcessOutput für**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) den Mixer auf.</span><span class="sxs-lookup"><span data-stu-id="73809-606">Call [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) on the mixer.</span></span>

<span data-ttu-id="73809-607">Beim Neupaintieren eines Frames können Sie die Präsentationsuhr ignorieren und den Rahmen sofort präsentieren.</span><span class="sxs-lookup"><span data-stu-id="73809-607">When repainting a frame, you can ignore the presentation clock and present the frame immediately.</span></span>

### <a name="scheduling-samples"></a><span data-ttu-id="73809-608">Zeitplanungsbeispiele</span><span class="sxs-lookup"><span data-stu-id="73809-608">Scheduling Samples</span></span>

<span data-ttu-id="73809-609">Videoframes können den EVR jederzeit erreichen.</span><span class="sxs-lookup"><span data-stu-id="73809-609">Video frames can reach the EVR at any time.</span></span> <span data-ttu-id="73809-610">Der Presenter ist dafür verantwortlich, jeden Frame zum richtigen Zeitpunkt basierend auf dem Zeitstempel des Frames zu präsentieren.</span><span class="sxs-lookup"><span data-stu-id="73809-610">The presenter is responsible for presenting each frame at the correct time, based on the time stamp of the frame.</span></span> <span data-ttu-id="73809-611">Wenn der Moderator ein neues Beispiel aus dem Mixer erhält, wird das Beispiel in die geplante Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="73809-611">When the presenter gets a new sample from the mixer, it puts the sample on the scheduled queue.</span></span> <span data-ttu-id="73809-612">In einem separaten Thread ruft der Moderator kontinuierlich das erste Beispiel vom Anfang der Warteschlange ab und bestimmt, ob Dies der Fall ist:</span><span class="sxs-lookup"><span data-stu-id="73809-612">On a separate thread, the presenter continually gets the first sample from the head of the queue and determines whether to:</span></span>

-   <span data-ttu-id="73809-613">Stellen Sie das Beispiel vor.</span><span class="sxs-lookup"><span data-stu-id="73809-613">Present the sample.</span></span>
-   <span data-ttu-id="73809-614">Behalten Sie das Beispiel in der Warteschlange bei, da es früh ist.</span><span class="sxs-lookup"><span data-stu-id="73809-614">Keep the sample on the queue because it is early.</span></span>
-   <span data-ttu-id="73809-615">Verwerfen Sie das Beispiel, da es zu spät ist.</span><span class="sxs-lookup"><span data-stu-id="73809-615">Discard the sample because it is late.</span></span> <span data-ttu-id="73809-616">Obwohl Sie möglichst vermeiden sollten, Frames zu löschen, müssen Sie dies möglicherweise machen, wenn der Moderator ständig ins Rückstand geraten soll.</span><span class="sxs-lookup"><span data-stu-id="73809-616">Although you should avoid dropping frames if possible, you might need to if the presenter is continually falling behind.</span></span>

<span data-ttu-id="73809-617">Um den Zeitstempel für einen Videoframe zu erhalten, rufen Sie [**IMTSample::GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) im Videobeispiel auf.</span><span class="sxs-lookup"><span data-stu-id="73809-617">To get the time stamp for a video frame, call [**IMFSample::GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) on the video sample.</span></span> <span data-ttu-id="73809-618">Der Zeitstempel ist relativ zur Präsentationsuhr des EVR.</span><span class="sxs-lookup"><span data-stu-id="73809-618">The time stamp is relative to the EVR's presentation clock.</span></span> <span data-ttu-id="73809-619">Um die aktuelle Uhrzeit zu erhalten, rufen [**Sie DIEClock::GetCorrelatedTime auf.**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime)</span><span class="sxs-lookup"><span data-stu-id="73809-619">To get the current clock time, call [**IMFClock::GetCorrelatedTime**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime).</span></span> <span data-ttu-id="73809-620">Wenn der EVR keine Präsentationsuhr hat oder ein Beispiel keinen Zeitstempel hat, können Sie das Beispiel sofort nach dem Erhalten präsentieren.</span><span class="sxs-lookup"><span data-stu-id="73809-620">If the EVR does not have a presentation clock, or if a sample does not have a time stamp, you can present the sample immediately after you get it.</span></span>

<span data-ttu-id="73809-621">Um die Dauer jedes Beispiels zu erhalten, rufen [**Sie DIESAMPLE::GetSampleDuration auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampleduration)</span><span class="sxs-lookup"><span data-stu-id="73809-621">To get the duration of each sample, call [**IMFSample::GetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampleduration).</span></span> <span data-ttu-id="73809-622">Wenn das Beispiel über keine Dauer verfügt, können Sie die [**Funktion MFFrameRateToAverageTimePerFrame**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) verwenden, um die Dauer aus der Framerate zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="73809-622">If the sample does not have a duration, you can use the [**MFFrameRateToAverageTimePerFrame**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) function to calculate the duration from the frame rate.</span></span>

<span data-ttu-id="73809-623">Beachten Sie beim Planen von Beispielen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="73809-623">When you schedule samples, keep in mind the following:</span></span>

-   <span data-ttu-id="73809-624">Wenn die Wiedergaberate schneller oder langsamer als die normale Geschwindigkeit ist, wird die Uhr mit einer schnelleren oder langsameren Geschwindigkeit ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="73809-624">If the playback rate is faster or slower than normal speed, the clock runs at a faster or slower rate.</span></span> <span data-ttu-id="73809-625">Das bedeutet, dass der Zeitstempel für ein Beispiel immer die richtige Zielzeit relativ zur Präsentationsuhr liefert.</span><span class="sxs-lookup"><span data-stu-id="73809-625">That means the time stamp on a sample always gives the correct target time relative to the presentation clock.</span></span> <span data-ttu-id="73809-626">Wenn Sie die Präsentationszeiten jedoch in eine andere Uhrzeit (z. B. den Leistungsindikator für hohe Auflösung) übersetzen, müssen Sie die Zeiten basierend auf der Taktgeschwindigkeit skalieren.</span><span class="sxs-lookup"><span data-stu-id="73809-626">However, if you translate presentation times into some other clock time (for example, the high-resolution performace counter), then you must scale the times based on the clock speed.</span></span> <span data-ttu-id="73809-627">Wenn sich die Taktgeschwindigkeit ändert, ruft der EVR die [**METHODE DER MODERATORClockStateSink::OnClockSetRate auf.**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate)</span><span class="sxs-lookup"><span data-stu-id="73809-627">If the clock speed changes, the EVR calls the presenter's [**IMFClockStateSink::OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) method.</span></span>
-   <span data-ttu-id="73809-628">Die Wiedergaberate kann bei umgekehrter Wiedergabe negativ sein.</span><span class="sxs-lookup"><span data-stu-id="73809-628">The playback rate can be negative for reverse playback.</span></span> <span data-ttu-id="73809-629">Wenn die Wiedergaberate negativ ist, wird die Präsentationsuhr rückwärts ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="73809-629">When the playback rate is negative, the presentation clock runs backward.</span></span> <span data-ttu-id="73809-630">Anders ausgedrückt: Die *Zeit N* + 1 tritt vor der Zeit *N auf.*</span><span class="sxs-lookup"><span data-stu-id="73809-630">In other words, time *N* + 1 occurs before time *N*.</span></span>

<span data-ttu-id="73809-631">Im folgenden Beispiel wird berechnet, wie früh oder spät ein Beispiel relativ zur Präsentationsuhr ist:</span><span class="sxs-lookup"><span data-stu-id="73809-631">The following example calculates how early or late a sample is, relative to the presentation clock:</span></span>


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



<span data-ttu-id="73809-632">Die Präsentationsuhr wird in der Regel von der Systemuhr oder dem Audiorenderer gesteuert.</span><span class="sxs-lookup"><span data-stu-id="73809-632">The presentation clock is usually driven by the system clock or the audio renderer.</span></span> <span data-ttu-id="73809-633">(Der Audiorenderer leitet die Zeit von der Rate ab, mit der die Soundkarte Audiodaten verwendet.) Im Allgemeinen wird die Präsentationsuhr nicht mit der Aktualisierungsrate des Monitors synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="73809-633">(The audio renderer derives the time from the rate at which the sound card consumes audio.) In general, the presentation clock is not synchronized with the refresh rate of the monitor.</span></span>

<span data-ttu-id="73809-634">Wenn Ihre Direct3D-Präsentationsparameter D3DPRESENT_INTERVAL_DEFAULT oder **D3DPRESENT_INTERVAL_ONE** für das Präsentationsintervall angeben, wartet der Present-Vorgang auf die vertikale Rückverziehung des Monitors.  </span><span class="sxs-lookup"><span data-stu-id="73809-634">If your Direct3D presentation parameters specify **D3DPRESENT_INTERVAL_DEFAULT** or **D3DPRESENT_INTERVAL_ONE** for the presentation interval, the **Present** operation waits for the monitor's vertical retrace.</span></span> <span data-ttu-id="73809-635">Dies ist eine einfache Möglichkeit, um Dasins zu verhindern, verringert jedoch die Genauigkeit Ihres Planungsalgorithmus.</span><span class="sxs-lookup"><span data-stu-id="73809-635">This is an easy way to prevent tearing, but reduces the accuracy of your scheduling algorithm.</span></span> <span data-ttu-id="73809-636">Wenn das Präsentationsintervall hingegen D3DPRESENT_INTERVAL_IMMEDIATE **ist,** wird die **Present-Methode** sofort ausgeführt. Dies führt zu einer Tränkung, es sei denn, Ihr Planungsalgorithmus ist genau genug, dass Sie **Present** nur während des vertikalen Rücklaufzeitraums aufrufen.</span><span class="sxs-lookup"><span data-stu-id="73809-636">Conversely, if the presentation interval is **D3DPRESENT_INTERVAL_IMMEDIATE**, the **Present** method executes immediately, which causes tearing unless your scheduling algorithm is accurate enough that you call **Present** only during the vertical retrace period.</span></span>

<span data-ttu-id="73809-637">Mit den folgenden Funktionen können Sie genaue Zeitsteuerungsinformationen erhalten:</span><span class="sxs-lookup"><span data-stu-id="73809-637">The following functions can help you get accurate timing information:</span></span>

-   <span data-ttu-id="73809-638">**IDirect3DDevice9::GetRasterStatus** gibt Informationen zum Raster zurück, einschließlich der aktuellen Scanzeile und ob sich das Raster im vertikalen leeren Bereich befindet.</span><span class="sxs-lookup"><span data-stu-id="73809-638">**IDirect3DDevice9::GetRasterStatus** returns information about the raster, including the current scan line and whether the raster is in the vertical blank period.</span></span>
-   <span data-ttu-id="73809-639">**DwmGetCompositionTimingInfo gibt** Zeitsteuerungsinformationen für den Desktopfenster-Manager zurück.</span><span class="sxs-lookup"><span data-stu-id="73809-639">**DwmGetCompositionTimingInfo** returns timing information for the desktop window manager.</span></span> <span data-ttu-id="73809-640">Diese Informationen sind nützlich, wenn die Desktopkomposition aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="73809-640">This information is useful if desktop composition is enabled.</span></span>

### <a name="presenting-samples"></a><span data-ttu-id="73809-641">Präsentieren von Beispielen</span><span class="sxs-lookup"><span data-stu-id="73809-641">Presenting Samples</span></span>

<span data-ttu-id="73809-642">In diesem Abschnitt wird davon ausgegangen, dass Sie eine separate Austauschkette für jede Oberfläche erstellt haben, wie unter [Allocating Direct3D Surfaces (Zuordnen von Direct3D-Oberflächen) beschrieben.](#allocating-direct3d-surfaces)</span><span class="sxs-lookup"><span data-stu-id="73809-642">This section assumes that you created a separate swap chain for each surface as described in [Allocating Direct3D Surfaces](#allocating-direct3d-surfaces).</span></span> <span data-ttu-id="73809-643">Um ein Beispiel zu präsentieren, erhalten Sie die Swap-Kette wie folgt aus dem Videobeispiel:</span><span class="sxs-lookup"><span data-stu-id="73809-643">To present a sample, get the swap chain from the video sample as follows:</span></span>

1.  <span data-ttu-id="73809-644">Rufen [**Sie IMBSAMPLE::GetBufferByIndex im**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) Videobeispiel auf, um den Puffer zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="73809-644">Call [**IMFSample::GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) on the video sample to get the buffer.</span></span>
2.  <span data-ttu-id="73809-645">Fragen Sie den Puffer für die [**BENUTZEROBERFLÄCHEGetService-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) ab.</span><span class="sxs-lookup"><span data-stu-id="73809-645">Query the buffer for the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span>
3.  <span data-ttu-id="73809-646">Rufen [**SieGEGETService::GetService auf,**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) um die **IDirect3DSurface9-Schnittstelle** der Direct3D-Oberfläche zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="73809-646">Call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) to get the **IDirect3DSurface9** interface of the Direct3D surface.</span></span> <span data-ttu-id="73809-647">(Sie können diesen Schritt und den vorherigen Schritt zu einem Schritt kombinieren, indem Sie [**MFGetService aufrufen.)**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice)</span><span class="sxs-lookup"><span data-stu-id="73809-647">(You can combine this step and the previous step into one by calling [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).)</span></span>
4.  <span data-ttu-id="73809-648">Rufen **Sie IDirect3DSurface9::GetContainer** auf der Oberfläche auf, um einen Zeiger auf die Austauschkette zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="73809-648">Call **IDirect3DSurface9::GetContainer** on the surface to get a pointer to the swap chain.</span></span>
5.  <span data-ttu-id="73809-649">Rufen **Sie IDirect3DSwapChain9::P für die** Swapkette zurück.</span><span class="sxs-lookup"><span data-stu-id="73809-649">Call **IDirect3DSwapChain9::Present** on the swap chain.</span></span>

<span data-ttu-id="73809-650">Diese Schritte sind im folgenden Code dargestellt:</span><span class="sxs-lookup"><span data-stu-id="73809-650">The following code shows these steps:</span></span>


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



### <a name="source-and-destination-rectangles"></a><span data-ttu-id="73809-651">Quell- und Zielrechtecke</span><span class="sxs-lookup"><span data-stu-id="73809-651">Source and Destination Rectangles</span></span>

<span data-ttu-id="73809-652">Das *Quellrechteck* ist der Anzuzeigende Teil des Videoframes.</span><span class="sxs-lookup"><span data-stu-id="73809-652">The *source rectangle* is the portion of the video frame to display.</span></span> <span data-ttu-id="73809-653">Sie wird relativ zu einem normalisierten Koordinatensystem definiert, bei dem der gesamte Videoframe ein Rechteck mit den Koordinaten {0, 0, 1, 1} einnimmt.</span><span class="sxs-lookup"><span data-stu-id="73809-653">It is defined relative to a normalized coordinate system, in which the entire video frame occupies a rectangle with coordinates {0, 0, 1, 1}.</span></span> <span data-ttu-id="73809-654">Das *Zielrechteck* ist der Bereich innerhalb der Zieloberfläche, in dem der Videoframe gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="73809-654">The *destination rectangle* is the area within the destination surface where the video frame is drawn.</span></span> <span data-ttu-id="73809-655">Mit dem Standardvorzeiger kann eine Anwendung diese Rechtecke festlegen, indem [**SIE DENKVideoDisplayControl::SetVideoPosition aufruft.**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition)</span><span class="sxs-lookup"><span data-stu-id="73809-655">The standard presenter enables an application to set these rectangles by calling [**IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span></span>

<span data-ttu-id="73809-656">Es gibt mehrere Optionen zum Anwenden von Quell- und Zielrechtecke.</span><span class="sxs-lookup"><span data-stu-id="73809-656">There are several options for applying source and destination rectangles.</span></span> <span data-ttu-id="73809-657">Die erste Option besteht in der Anwendung durch den Mixer:</span><span class="sxs-lookup"><span data-stu-id="73809-657">The first option is to let the mixer apply them:</span></span>

-   <span data-ttu-id="73809-658">Legen Sie das Quellrechteck [**mithilfe**](video-zoom-rect-attribute.md) des VIDEO_ZOOM_RECT fest.</span><span class="sxs-lookup"><span data-stu-id="73809-658">Set the source rectangle using the [**VIDEO_ZOOM_RECT**](video-zoom-rect-attribute.md) attribute.</span></span> <span data-ttu-id="73809-659">Der Mixer wird das Quellrechteck anwenden, wenn er das Video auf die Zieloberfläche blitt.</span><span class="sxs-lookup"><span data-stu-id="73809-659">The mixer will apply the source rectangle when it blits the video to the destination surface.</span></span> <span data-ttu-id="73809-660">Das Standardquellenrechteck des Mixers ist der gesamte Frame.</span><span class="sxs-lookup"><span data-stu-id="73809-660">The mixer's default source rectangle is the entire frame.</span></span>
-   <span data-ttu-id="73809-661">Legen Sie das Zielrechteck als geometrische Öffnung im Ausgabetyp des Mixers fest.</span><span class="sxs-lookup"><span data-stu-id="73809-661">Set the destination rectangle as the geometric aperture in the mixer's output type.</span></span> <span data-ttu-id="73809-662">Weitere Informationen finden Sie unter [Aushandeln von Formaten.](#negotiating-formats)</span><span class="sxs-lookup"><span data-stu-id="73809-662">For more information, see [Negotiating Formats](#negotiating-formats).</span></span>

<span data-ttu-id="73809-663">Die zweite Option besteht in der Anwendung der Rechtecke, wenn Sie **IDirect3DSwapChain9::P resent** verwenden, indem Sie die *Parameter pSourceRect* und *pDestRect* in der **Present-Methode** angeben.</span><span class="sxs-lookup"><span data-stu-id="73809-663">The second option is to apply the rectangles when you **IDirect3DSwapChain9::Present** by specifying the *pSourceRect* and *pDestRect* parameters in the **Present** method.</span></span> <span data-ttu-id="73809-664">Sie können diese Optionen kombinieren.</span><span class="sxs-lookup"><span data-stu-id="73809-664">You can combine these options.</span></span> <span data-ttu-id="73809-665">Beispielsweise können Sie das Quellrechteck für den Mixer festlegen, aber das Zielrechteck in der **Present-Methode** anwenden.</span><span class="sxs-lookup"><span data-stu-id="73809-665">For example, you could set the source rectangle on the mixer but apply the destination rectangle in the **Present** method.</span></span>

<span data-ttu-id="73809-666">Wenn die Anwendung das Zielrechteck ändert oder die Größe des Fensters ändert, müssen Sie möglicherweise neue Oberflächen zuordnen.</span><span class="sxs-lookup"><span data-stu-id="73809-666">If the application changes the destination rectangle or resizes the window, you might need to allocate new surfaces.</span></span> <span data-ttu-id="73809-667">Wenn dies der Fall ist, müssen Sie darauf achten, diesen Vorgang mit Ihrem Planungsthread zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="73809-667">If so, you must be careful to synchronize this operation with your scheduling thread.</span></span> <span data-ttu-id="73809-668">Leeren Sie die Planungswarteschlange, und verwerfen Sie die alten Stichproben, bevor Sie neue Oberflächen zuordnen.</span><span class="sxs-lookup"><span data-stu-id="73809-668">Flush the scheduling queue and discard the old samples before allocating new surfaces.</span></span>

### <a name="end-of-stream"></a><span data-ttu-id="73809-669">Ende des Streams</span><span class="sxs-lookup"><span data-stu-id="73809-669">End of Stream</span></span>

<span data-ttu-id="73809-670">Wenn jeder Eingabedatenstrom auf der EVR beendet wurde, sendet der EVR eine MFVP_MESSAGE_ENDOFSTREAM **nachricht** an den Moderator.</span><span class="sxs-lookup"><span data-stu-id="73809-670">When every input stream on the EVR has ended, the EVR sends an **MFVP_MESSAGE_ENDOFSTREAM** message to the presenter.</span></span> <span data-ttu-id="73809-671">An dem Punkt, an dem Sie die Nachricht empfangen, müssen jedoch möglicherweise noch einige Videoframes verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="73809-671">At the point when you receive the message, however, there might be a few video frames remaining to be processed.</span></span> <span data-ttu-id="73809-672">Bevor Sie auf die Nachricht zum Ende des Streams antworten, müssen Sie die ganze Ausgabe des Mixers leeren und alle verbleibenden Frames anzeigen.</span><span class="sxs-lookup"><span data-stu-id="73809-672">Before you respond to the end-of-stream message, you must drain all of the output from the mixer and present all of the remaining frames.</span></span> <span data-ttu-id="73809-673">Nachdem der letzte Frame angezeigt wurde, senden Sie **ein** EC_COMPLETE an die EVR.</span><span class="sxs-lookup"><span data-stu-id="73809-673">After the last frame is presented, send an **EC_COMPLETE** event to the EVR.</span></span>

<span data-ttu-id="73809-674">Das nächste Beispiel zeigt eine Methode, die das **EC_COMPLETE** sendet, wenn verschiedene Bedingungen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="73809-674">The next example shows a method that sends the **EC_COMPLETE** event if various conditions are met.</span></span> <span data-ttu-id="73809-675">Andernfalls wird S_OK zurückgegeben, ohne das Ereignis zu senden:</span><span class="sxs-lookup"><span data-stu-id="73809-675">Otherwise, it returns S_OK without sending the event:</span></span>


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



<span data-ttu-id="73809-676">Diese Methode überprüft die folgenden Zustände:</span><span class="sxs-lookup"><span data-stu-id="73809-676">This method checks the following states:</span></span>

-   <span data-ttu-id="73809-677">Wenn die *m_fSampleNotify* true **ist,** bedeutet dies, dass der Mixer über einen oder mehrere Frames verfügt, die noch nicht verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="73809-677">If the *m_fSampleNotify* variable is **TRUE**, it means the mixer has one or more frames that have not been processed yet.</span></span> <span data-ttu-id="73809-678">(Weitere Informationen finden Sie unter [Processing Output](#processing-output).)</span><span class="sxs-lookup"><span data-stu-id="73809-678">(For details, see [Processing Output](#processing-output).)</span></span>
-   <span data-ttu-id="73809-679">Die *m_fEndStreaming* variable ist ein boolesches Flag, dessen Anfangswert **FALSE ist.**</span><span class="sxs-lookup"><span data-stu-id="73809-679">The *m_fEndStreaming* variable is a Boolean flag whose initial value **FALSE**.</span></span> <span data-ttu-id="73809-680">Der Moderator legt das Flag auf **TRUE fest,** wenn der EVR **die** MFVP_MESSAGE_ENDOFSTREAM sendet.</span><span class="sxs-lookup"><span data-stu-id="73809-680">The presenter sets the flag to **TRUE** when the EVR sends the **MFVP_MESSAGE_ENDOFSTREAM** message.</span></span>
-   <span data-ttu-id="73809-681">Es wird davon ausgegangen, dass die Methode TRUE zurück gibt, solange ein oder mehrere Frames `AreSamplesPending` in der geplanten Warteschlange warten. </span><span class="sxs-lookup"><span data-stu-id="73809-681">The `AreSamplesPending` method is assumed to return **TRUE** as long as one or more frames are waiting in the scheduled queue.</span></span>

<span data-ttu-id="73809-682">Legen Sie [**in der METHODE VORVIDEOPresenter::P rocessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) m_fEndStreaming **TRUE** fest, und rufen Sie auf, wenn die EVR die MFVP_MESSAGE_ENDOFSTREAM  `CheckEndOfStream` sendet: </span><span class="sxs-lookup"><span data-stu-id="73809-682">In the [**IMFVideoPresenter::ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) method, set *m_fEndStreaming* to **TRUE** and call `CheckEndOfStream` when the EVR sends the **MFVP_MESSAGE_ENDOFSTREAM** message:</span></span>


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



<span data-ttu-id="73809-683">Rufen Sie darüber hinaus auf, wenn `CheckEndOfStream` die [**METHODE VERFORMTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) des Mixers MF_E_TRANSFORM_NEED_MORE_INPUT. </span><span class="sxs-lookup"><span data-stu-id="73809-683">In addition, call `CheckEndOfStream` if the mixer's [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) method returns **MF_E_TRANSFORM_NEED_MORE_INPUT**.</span></span> <span data-ttu-id="73809-684">Dieser Fehlercode gibt an, dass der Mixer keine Eingabebeispiele mehr enthält (siehe [Verarbeiten der Ausgabe](#processing-output)).</span><span class="sxs-lookup"><span data-stu-id="73809-684">This error code indicates that the mixer has no more input samples (see [Processing Output](#processing-output)).</span></span>

## <a name="frame-stepping"></a><span data-ttu-id="73809-685">Rahmenschritt</span><span class="sxs-lookup"><span data-stu-id="73809-685">Frame Stepping</span></span>

<span data-ttu-id="73809-686">Der EVR ist für die Unterstützung von Rahmenschritten in DirectShow und bereinigung in Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="73809-686">The EVR is designed to support frame stepping in DirectShow and scrubbing in Media Foundation.</span></span> <span data-ttu-id="73809-687">Frameschritt- und Bereinigungsschritte sind konzeptionell ähnlich.</span><span class="sxs-lookup"><span data-stu-id="73809-687">Frame stepping and scrubbing are conceptually similar.</span></span> <span data-ttu-id="73809-688">In beiden Fällen fordert die Anwendung einen Videoframe nach dem anderen an.</span><span class="sxs-lookup"><span data-stu-id="73809-688">In both cases, the application requests one video frame at a time.</span></span> <span data-ttu-id="73809-689">Intern verwendet der Presenter denselben Mechanismus, um beide Features zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="73809-689">Internally, the presenter uses the same mechanism to implement both features.</span></span>

<span data-ttu-id="73809-690">Frameschritte in DirectShow funktionieren wie folgt:</span><span class="sxs-lookup"><span data-stu-id="73809-690">Frame stepping in DirectShow works as follows:</span></span>

-   <span data-ttu-id="73809-691">Die Anwendung ruft [**IVideoFrameStep::Step auf.**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-step)</span><span class="sxs-lookup"><span data-stu-id="73809-691">The application calls [**IVideoFrameStep::Step**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-step).</span></span> <span data-ttu-id="73809-692">Die Anzahl der Schritte wird im *dwSteps-Parameter* angegeben.</span><span class="sxs-lookup"><span data-stu-id="73809-692">The number of steps is given in the *dwSteps* parameter.</span></span> <span data-ttu-id="73809-693">Der EVR sendet eine **MFVP_MESSAGE_STEP** nachricht an den Moderator, wobei der Message-Parameter (*ulParam*) die Anzahl der Schritte ist.</span><span class="sxs-lookup"><span data-stu-id="73809-693">The EVR sends an **MFVP_MESSAGE_STEP** message to the presenter, where the message parameter (*ulParam*) is the number of steps.</span></span>
-   <span data-ttu-id="73809-694">Wenn die Anwendung [**IVideoFrameStep::CancelStep**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-cancelstep) aufruft oder den Graphzustand ändert (wird ausgeführt, angehalten oder **beendet),** sendet die EVR eine MFVP_MESSAGE_CANCELSTEP Nachricht.</span><span class="sxs-lookup"><span data-stu-id="73809-694">If the application calls [**IVideoFrameStep::CancelStep**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-cancelstep) or changes the graph state (running, paused, or stopped), the EVR sends an **MFVP_MESSAGE_CANCELSTEP** message.</span></span>

<span data-ttu-id="73809-695">Die Bereinigung in Media Foundation funktioniert wie folgt:</span><span class="sxs-lookup"><span data-stu-id="73809-695">Scrubbing in Media Foundation works as follows:</span></span>

-   <span data-ttu-id="73809-696">Die Anwendung legt die Wiedergaberate auf 0 (null) fest, indem [**sie DURCH AUFRUFEN VONTRATEControl::SetRate aufruft.**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate)</span><span class="sxs-lookup"><span data-stu-id="73809-696">The application sets the playback rate to zero by calling [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate).</span></span>
-   <span data-ttu-id="73809-697">Um einen neuen Frame zu rendern, ruft die Anwendung [**DIETMEDIASession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) mit der gewünschten Position auf.</span><span class="sxs-lookup"><span data-stu-id="73809-697">To render a new frame, the application calls [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) with the desired position.</span></span> <span data-ttu-id="73809-698">Der EVR sendet **eine** MFVP_MESSAGE_STEP nachricht mit *ulParam* gleich 1.</span><span class="sxs-lookup"><span data-stu-id="73809-698">The EVR sends an **MFVP_MESSAGE_STEP** message with *ulParam* equal to 1.</span></span>
-   <span data-ttu-id="73809-699">Um die Bereinigung zu beenden, legt die Anwendung die Wiedergaberate auf einen Wert ungleich 0 (null) fest.</span><span class="sxs-lookup"><span data-stu-id="73809-699">To stop scrubbing, the application sets the playback rate to a nonzero value.</span></span> <span data-ttu-id="73809-700">Der EVR sendet die **MFVP_MESSAGE_CANCELSTEP** Nachricht.</span><span class="sxs-lookup"><span data-stu-id="73809-700">The EVR sends the **MFVP_MESSAGE_CANCELSTEP** message.</span></span>

<span data-ttu-id="73809-701">Nachdem die **MFVP_MESSAGE_STEP** empfangen wurde, wartet die Moderatorin, bis der Zielframe eintrifft.</span><span class="sxs-lookup"><span data-stu-id="73809-701">After receiving the **MFVP_MESSAGE_STEP** message, the presenter waits for the target frame to arrive.</span></span> <span data-ttu-id="73809-702">Wenn die Anzahl der Schritte *N beträgt,* verwirft der Moderator die nächsten (*N* - 1) Beispiele und stellt das *N-te* Beispiel vor.</span><span class="sxs-lookup"><span data-stu-id="73809-702">If the number of steps is *N*, the presenter discards the next (*N* - 1) samples and presents the *N* th sample.</span></span> <span data-ttu-id="73809-703">Wenn die Moderatorin den Rahmenschritt abgeschlossen [](../directshow/ec-step-complete.md) hat, sendet sie ein EC_STEP_COMPLETE-Ereignis an die EVR, bei dem *lParam1* auf **FALSE festgelegt ist.**</span><span class="sxs-lookup"><span data-stu-id="73809-703">When the presenter completes the frame step, it sends an [**EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) event to the EVR with *lParam1* set to **FALSE**.</span></span> <span data-ttu-id="73809-704">Wenn die Wiedergaberate 0 (null) ist, sendet die Moderatorin außerdem [**ein**](../directshow/ec-scrub-time.md) EC_SCRUB_TIME Ereignis.</span><span class="sxs-lookup"><span data-stu-id="73809-704">In addition, if the playback rate is zero, the presenter sends an [**EC_SCRUB_TIME**](../directshow/ec-scrub-time.md) event.</span></span> <span data-ttu-id="73809-705">Wenn die EVR frame stepping abbricht, während ein Frameschrittvorgang  noch aussteht, sendet die Moderatorin ein EC_STEP_COMPLETE-Ereignis, wobei *lParam1* auf **TRUE festgelegt ist.**</span><span class="sxs-lookup"><span data-stu-id="73809-705">If the EVR cancels frame stepping while a frame-step operation is still pending, the presenter sends an **EC_STEP_COMPLETE** event with *lParam1* set to **TRUE**.</span></span>

<span data-ttu-id="73809-706">Die Anwendung kann schritt- oder bereinigungsschritte  mehrmals umrahmen, sodass der Moderator möglicherweise mehrere MFVP_MESSAGE_STEP empfangen kann, bevor er eine MFVP_MESSAGE_CANCELSTEP **erhält.**</span><span class="sxs-lookup"><span data-stu-id="73809-706">The application can frame step or scrub multiple times, so the presenter might receive multiple **MFVP_MESSAGE_STEP** messages before it gets an **MFVP_MESSAGE_CANCELSTEP** message.</span></span> <span data-ttu-id="73809-707">Außerdem kann der Moderator  die MFVP_MESSAGE_STEP empfangen, bevor die Uhr gestartet wird oder während die Uhr ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="73809-707">Also, the presenter can receive the **MFVP_MESSAGE_STEP** message before the clock starts or while the clock is running.</span></span>

### <a name="implementing-frame-stepping"></a><span data-ttu-id="73809-708">Implementieren von Rahmenschritten</span><span class="sxs-lookup"><span data-stu-id="73809-708">Implementing Frame Stepping</span></span>

<span data-ttu-id="73809-709">In diesem Abschnitt wird ein Algorithmus zum Implementieren von Rahmenschritten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="73809-709">This section describes an algorithm to implement frame stepping.</span></span> <span data-ttu-id="73809-710">Der Frameschrittalgorithmus verwendet die folgenden Variablen:</span><span class="sxs-lookup"><span data-stu-id="73809-710">The frame stepping algorithm uses the following variables:</span></span>

-   <span data-ttu-id="73809-711">*step_count*.</span><span class="sxs-lookup"><span data-stu-id="73809-711">*step_count*.</span></span> <span data-ttu-id="73809-712">Eine ganze Zahl ohne Vorzeichen, die die Anzahl der Schritte im aktuellen Rahmenschrittvorgang angibt.</span><span class="sxs-lookup"><span data-stu-id="73809-712">An unsigned integer that specifies the number of steps in the current frame stepping operation.</span></span>
-   <span data-ttu-id="73809-713">*step_queue*.</span><span class="sxs-lookup"><span data-stu-id="73809-713">*step_queue*.</span></span> <span data-ttu-id="73809-714">Eine Warteschlange [**von WARTESCHLANGENsample-Zeigern.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)</span><span class="sxs-lookup"><span data-stu-id="73809-714">A queue of [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) pointers.</span></span>
-   <span data-ttu-id="73809-715">*step_state*.</span><span class="sxs-lookup"><span data-stu-id="73809-715">*step_state*.</span></span> <span data-ttu-id="73809-716">Der Moderator kann sich in Bezug auf die Rahmenschritte jederzeit in einem der folgenden Zustände befingen:</span><span class="sxs-lookup"><span data-stu-id="73809-716">At any time, the presenter can be in one of the following states with respect to frame stepping:</span></span> 

    | <span data-ttu-id="73809-717">State</span><span class="sxs-lookup"><span data-stu-id="73809-717">State</span></span>         | <span data-ttu-id="73809-718">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="73809-718">Description</span></span>                                                                                                                                                                                                     |
    |---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="73809-719">NOT_STEPPING</span><span class="sxs-lookup"><span data-stu-id="73809-719">NOT_STEPPING</span></span> | <span data-ttu-id="73809-720">Keine Rahmenschritte.</span><span class="sxs-lookup"><span data-stu-id="73809-720">Not frame stepping.</span></span>                                                                                                                                                                                             |
    | <span data-ttu-id="73809-721">WAITING</span><span class="sxs-lookup"><span data-stu-id="73809-721">WAITING</span></span>       | <span data-ttu-id="73809-722">Der Moderator hat die **MFVP_MESSAGE_STEP** empfangen, aber die Uhr wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="73809-722">The presenter has received the **MFVP_MESSAGE_STEP** message, but the clock has not started.</span></span>                                                                                                                  |
    | <span data-ttu-id="73809-723">PENDING (AUSSTEHEND)</span><span class="sxs-lookup"><span data-stu-id="73809-723">PENDING</span></span>       | <span data-ttu-id="73809-724">Der Moderator hat die **MFVP_MESSAGE_STEP** empfangen, und die Uhr wurde gestartet, aber der Moderator wartet auf den Empfang des Zielframes.</span><span class="sxs-lookup"><span data-stu-id="73809-724">The presenter has received the **MFVP_MESSAGE_STEP** message and the clock has started, but the presenter is waiting to receive the target frame.</span></span>                                                             |
    | <span data-ttu-id="73809-725">Geplant</span><span class="sxs-lookup"><span data-stu-id="73809-725">SCHEDULED</span></span>     | <span data-ttu-id="73809-726">Der Präsentationser hat den Zielframe empfangen und für die Präsentation geplant, aber der Frame wurde nicht dargestellt.</span><span class="sxs-lookup"><span data-stu-id="73809-726">The presenter has received the target frame and has scheduled it for presentation, but the frame has not been presented.</span></span>                                                                                        |
    | <span data-ttu-id="73809-727">vollständig</span><span class="sxs-lookup"><span data-stu-id="73809-727">COMPLETE</span></span>      | <span data-ttu-id="73809-728">Der Moderator hat den Zielframe dargestellt und das EC_STEP_COMPLETE [**gesendet**](../directshow/ec-step-complete.md) und wartet auf die nächste MFVP_MESSAGE_STEP **oder** **MFVP_MESSAGE_CANCELSTEP** Nachricht.</span><span class="sxs-lookup"><span data-stu-id="73809-728">The presenter has presented the target frame and sent the [**EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) event, and is waiting for the next **MFVP_MESSAGE_STEP** or **MFVP_MESSAGE_CANCELSTEP** message.</span></span> |

    

     

    <span data-ttu-id="73809-729">Diese Zustände sind unabhängig von den Presenterzuständen, die im Abschnitt [Presenter States aufgeführt sind.](#presenter-states)</span><span class="sxs-lookup"><span data-stu-id="73809-729">These states are independent of the presenter states listed in the section [Presenter States](#presenter-states).</span></span>

<span data-ttu-id="73809-730">Die folgenden Verfahren sind für den Algorithmus für die Frameschritt-Prozedur definiert:</span><span class="sxs-lookup"><span data-stu-id="73809-730">The following procedures are defined for the frame-stepping algorithm:</span></span>

<span data-ttu-id="73809-731">PrepareFrameStep-Prozedur</span><span class="sxs-lookup"><span data-stu-id="73809-731">PrepareFrameStep Procedure</span></span>

1.  <span data-ttu-id="73809-732">*Inkrement step_count*.</span><span class="sxs-lookup"><span data-stu-id="73809-732">Increment *step_count*.</span></span>
2.  <span data-ttu-id="73809-733">Legen *step_state* auf WAITING fest.</span><span class="sxs-lookup"><span data-stu-id="73809-733">Set *step_state* to WAITING.</span></span>
3.  <span data-ttu-id="73809-734">Wenn die Uhr ausgeführt wird, rufen Sie StartFrameStep auf.</span><span class="sxs-lookup"><span data-stu-id="73809-734">If the clock is running, call StartFrameStep.</span></span>

<span data-ttu-id="73809-735">StartFrameStep-Prozedur</span><span class="sxs-lookup"><span data-stu-id="73809-735">StartFrameStep Procedure</span></span>

1.  <span data-ttu-id="73809-736">Wenn *step_state* warte, legen *Sie* step_state ausstehend fest.</span><span class="sxs-lookup"><span data-stu-id="73809-736">If *step_state* equals WAITING, set *step_state* to PENDING.</span></span> <span data-ttu-id="73809-737">Rufen Sie für jedes Beispiel in *step_queue* DeliverFrameStepSample auf.</span><span class="sxs-lookup"><span data-stu-id="73809-737">For each sample in *step_queue*, call DeliverFrameStepSample.</span></span>
2.  <span data-ttu-id="73809-738">Wenn *step_state* gleich NOT_STEPPING, entfernen Sie alle Beispiele aus *step_queue,* und planen Sie sie für die Präsentation.</span><span class="sxs-lookup"><span data-stu-id="73809-738">If *step_state* equals NOT_STEPPING, remove any samples from *step_queue* and schedule them for presentation.</span></span>

<span data-ttu-id="73809-739">CompleteFrameStep-Prozedur</span><span class="sxs-lookup"><span data-stu-id="73809-739">CompleteFrameStep Procedure</span></span>

1.  <span data-ttu-id="73809-740">Legen *step_state* auf COMPLETE fest.</span><span class="sxs-lookup"><span data-stu-id="73809-740">Set *step_state* to COMPLETE.</span></span>
2.  <span data-ttu-id="73809-741">Senden Sie das EC_STEP_COMPLETE mit *lParam1*  =  **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="73809-741">Send the EC_STEP_COMPLETE event with *lParam1* = **FALSE**.</span></span>
3.  <span data-ttu-id="73809-742">Wenn die Taktrate null ist, senden Sie **das** EC_SCRUB_TIME mit der Beispielzeit.</span><span class="sxs-lookup"><span data-stu-id="73809-742">If the clock rate is zero, send the **EC_SCRUB_TIME** event with the sample time.</span></span>

<span data-ttu-id="73809-743">DeliverFrameStepSample-Prozedur</span><span class="sxs-lookup"><span data-stu-id="73809-743">DeliverFrameStepSample Procedure</span></span>

1.  <span data-ttu-id="73809-744">Wenn die Taktrate 0 (null) und *die* Stichprobendauer  +  *der Stichprobendauer*  <  ist, verwerfen Sie die Stichprobe.</span><span class="sxs-lookup"><span data-stu-id="73809-744">If the clock rate is zero and *sample time* + *sample duration* < *clock time*, discard the sample.</span></span> <span data-ttu-id="73809-745">Beenden</span><span class="sxs-lookup"><span data-stu-id="73809-745">Exit.</span></span>
2.  <span data-ttu-id="73809-746">Wenn *step_state* SCHEDULED oder COMPLETE ist, fügen Sie das Beispiel zu *step_queue.*</span><span class="sxs-lookup"><span data-stu-id="73809-746">If *step_state* equals SCHEDULED or COMPLETE, add the sample to *step_queue*.</span></span> <span data-ttu-id="73809-747">Beenden</span><span class="sxs-lookup"><span data-stu-id="73809-747">Exit.</span></span>
3.  <span data-ttu-id="73809-748">Dekrementierung *step_count*.</span><span class="sxs-lookup"><span data-stu-id="73809-748">Decrement *step_count*.</span></span>
4.  <span data-ttu-id="73809-749">Wenn *step_count* > 0 ist, verwerfen Sie das Beispiel.</span><span class="sxs-lookup"><span data-stu-id="73809-749">If *step_count* > 0, discard the sample.</span></span> <span data-ttu-id="73809-750">Beenden</span><span class="sxs-lookup"><span data-stu-id="73809-750">Exit.</span></span>
5.  <span data-ttu-id="73809-751">Wenn *step_state* warte, fügen Sie das Beispiel zu *step_queue.*</span><span class="sxs-lookup"><span data-stu-id="73809-751">If *step_state* equals WAITING, add the sample to *step_queue*.</span></span> <span data-ttu-id="73809-752">Beenden</span><span class="sxs-lookup"><span data-stu-id="73809-752">Exit.</span></span>
6.  <span data-ttu-id="73809-753">Planen Sie das Beispiel für die Präsentation.</span><span class="sxs-lookup"><span data-stu-id="73809-753">Schedule the sample for presentation.</span></span>
7.  <span data-ttu-id="73809-754">Legen *step_state* auf SCHEDULED fest.</span><span class="sxs-lookup"><span data-stu-id="73809-754">Set *step_state* to SCHEDULED.</span></span>

<span data-ttu-id="73809-755">CancelFrameStep-Prozedur</span><span class="sxs-lookup"><span data-stu-id="73809-755">CancelFrameStep Procedure</span></span>

1.  <span data-ttu-id="73809-756">Legen *step_state* auf NOT_STEPPING</span><span class="sxs-lookup"><span data-stu-id="73809-756">Set *step_state* to NOT_STEPPING</span></span>
2.  <span data-ttu-id="73809-757">Setzen *step_count* auf 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="73809-757">Reset *step_count* to zero.</span></span>
3.  <span data-ttu-id="73809-758">Wenn der vorherige Wert von *step_state* WAITING, PENDING oder SCHEDULED war, senden Sie EC_STEP_COMPLETE *lParam1*  =  **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="73809-758">If the previous value of *step_state* was WAITING, PENDING, or SCHEDULED, send EC_STEP_COMPLETE with *lParam1* = **TRUE**.</span></span>

<span data-ttu-id="73809-759">Rufen Sie diese Verfahren wie folgt auf:</span><span class="sxs-lookup"><span data-stu-id="73809-759">Call these procedures as follows:</span></span>



| <span data-ttu-id="73809-760">Presenter-Nachricht oder -Methode</span><span class="sxs-lookup"><span data-stu-id="73809-760">Presenter message or method</span></span>                                                   | <span data-ttu-id="73809-761">Prozedur</span><span class="sxs-lookup"><span data-stu-id="73809-761">Procedure</span></span>           |
|-------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="73809-762">**MFVP_MESSAGE_STEP-Nachricht**</span><span class="sxs-lookup"><span data-stu-id="73809-762">**MFVP_MESSAGE_STEP** message</span></span>                                               | `PrepareFrameStep`  |
| <span data-ttu-id="73809-763">**MFVP_MESSAGE_STEP-Nachricht**</span><span class="sxs-lookup"><span data-stu-id="73809-763">**MFVP_MESSAGE_STEP** message</span></span>                                               | `CancelStep`        |
| [<span data-ttu-id="73809-764">**DEADClockStateSink::OnClockStart**</span><span class="sxs-lookup"><span data-stu-id="73809-764">**IMFClockStateSink::OnClockStart**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart)     | `StartFrameStep`    |
| [<span data-ttu-id="73809-765">**DEADClockStateSink::OnClockRestart**</span><span class="sxs-lookup"><span data-stu-id="73809-765">**IMFClockStateSink::OnClockRestart**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart) | `StartFrameStep`    |
| <span data-ttu-id="73809-766">[**RÜCKRUFTrackedSample-Rückruf**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)</span><span class="sxs-lookup"><span data-stu-id="73809-766">[**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) callback</span></span>                         | `CompleteFrameStep` |
| [<span data-ttu-id="73809-767">**DEADClockStateSink::OnClockStop**</span><span class="sxs-lookup"><span data-stu-id="73809-767">**IMFClockStateSink::OnClockStop**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop)       | `CancelFrameStep`   |
| [<span data-ttu-id="73809-768">**DEADClockStateSink::OnClockSetRate**</span><span class="sxs-lookup"><span data-stu-id="73809-768">**IMFClockStateSink::OnClockSetRate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) | `CancelFrameStep`   |



 

<span data-ttu-id="73809-769">Das folgende Flussdiagramm zeigt die Prozeduren für die Frameschritte.</span><span class="sxs-lookup"><span data-stu-id="73809-769">The following flow chart shows the frame-stepping procedures.</span></span>

![Flussdiagramm mit Pfaden, die mit mfvp message step und \- \- mfvp message processinputnotify beginnen und mit \- \- "state = complete" enden](images/d9baaa67-a9b1-4e27-9a32-08a45b0677d3.gif)

## <a name="setting-the-presenter-on-the-evr"></a><span data-ttu-id="73809-771">Festlegen des Presenters auf der EVR</span><span class="sxs-lookup"><span data-stu-id="73809-771">Setting the Presenter on the EVR</span></span>

<span data-ttu-id="73809-772">Nach der Implementierung des Presenters besteht der nächste Schritt im Konfigurieren der EVR für die Verwendung.</span><span class="sxs-lookup"><span data-stu-id="73809-772">After implementing the presenter, the next step is to configure the EVR to use it.</span></span>

### <a name="setting-the-presenter-in-directshow"></a><span data-ttu-id="73809-773">Festlegen des Presenters in DirectShow</span><span class="sxs-lookup"><span data-stu-id="73809-773">Setting the Presenter in DirectShow</span></span>

<span data-ttu-id="73809-774">Legen Sie in einer DirectShow-Anwendung den Presenter auf der EVR wie folgt fest:</span><span class="sxs-lookup"><span data-stu-id="73809-774">In a DirectShow application, set the presenter on the EVR as follows:</span></span>

1.  <span data-ttu-id="73809-775">Erstellen Sie den EVR-Filter, indem **Sie CoCreateInstance aufrufen.**</span><span class="sxs-lookup"><span data-stu-id="73809-775">Create the EVR filter by calling **CoCreateInstance**.</span></span> <span data-ttu-id="73809-776">Die CLSID ist **CLSID_EnhancedVideoRenderer**.</span><span class="sxs-lookup"><span data-stu-id="73809-776">The CLSID is **CLSID_EnhancedVideoRenderer**.</span></span>
2.  <span data-ttu-id="73809-777">Fügen Sie die EVR dem Filterdiagramm hinzu.</span><span class="sxs-lookup"><span data-stu-id="73809-777">Add the EVR to the filter graph.</span></span>
3.  <span data-ttu-id="73809-778">Erstellen Sie eine Instanz Ihrer Präsentation.</span><span class="sxs-lookup"><span data-stu-id="73809-778">Create an instance of your presenter.</span></span> <span data-ttu-id="73809-779">Ihre Moderatorin kann die Com-Standardobjekterstellung über **IClassFactory** unterstützen, dies ist jedoch nicht zwingend erforderlich.</span><span class="sxs-lookup"><span data-stu-id="73809-779">Your presenter can support standard COM object creation through **IClassFactory**, but this is not mandatory.</span></span>
4.  <span data-ttu-id="73809-780">Fragen Sie den EVR-Filter für die [**BENUTZEROBERFLÄCHEVideoRenderer-Schnittstelle**](/windows/desktop/api/evr/nn-evr-imfvideorenderer) ab.</span><span class="sxs-lookup"><span data-stu-id="73809-780">Query the EVR filter for the [**IMFVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer) interface.</span></span>
5.  <span data-ttu-id="73809-781">Rufen [**Sie DIE NSDVideoRenderer::InitializeRenderer auf.**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer)</span><span class="sxs-lookup"><span data-stu-id="73809-781">Call [**IMFVideoRenderer::InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).</span></span>

### <a name="setting-the-presenter-in-media-foundation"></a><span data-ttu-id="73809-782">Festlegen des Presenters in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="73809-782">Setting the Presenter in Media Foundation</span></span>

<span data-ttu-id="73809-783">In Media Foundation stehen Ihnen mehrere Optionen zur Verfügung, je nachdem, ob Sie die EVR-Mediensenke oder das EVR-Aktivierungsobjekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="73809-783">In Media Foundation, you have several options, depending on whether you create the EVR media sink or the EVR activation object.</span></span> <span data-ttu-id="73809-784">Weitere Informationen zu Aktivierungsobjekten finden Sie unter [Activation Objects](activation-objects.md).</span><span class="sxs-lookup"><span data-stu-id="73809-784">For more information about activation objects, see [Activation Objects](activation-objects.md).</span></span>

<span data-ttu-id="73809-785">Gehen Sie für die EVR-Mediensenke wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="73809-785">For the EVR media sink, do the following:</span></span>

1.  <span data-ttu-id="73809-786">Rufen [**Sie MFCreateVideoRenderer auf,**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) um die Mediensenke zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="73809-786">Call [**MFCreateVideoRenderer**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) to create the media sink.</span></span>
2.  <span data-ttu-id="73809-787">Erstellen Sie eine Instanz Ihrer Präsentation.</span><span class="sxs-lookup"><span data-stu-id="73809-787">Create an instance of your presenter.</span></span>
3.  <span data-ttu-id="73809-788">Fragen Sie die EVR-Mediensenke für die [**BENUTZEROBERFLÄCHEVideoRenderer-Schnittstelle**](/windows/desktop/api/evr/nn-evr-imfvideorenderer) ab.</span><span class="sxs-lookup"><span data-stu-id="73809-788">Query the EVR media sink for the [**IMFVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer) interface.</span></span>
4.  <span data-ttu-id="73809-789">Rufen [**Sie DIE NSDVideoRenderer::InitializeRenderer auf.**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer)</span><span class="sxs-lookup"><span data-stu-id="73809-789">Call [**IMFVideoRenderer::InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).</span></span>

<span data-ttu-id="73809-790">Gehen Sie für das EVR-Aktivierungsobjekt wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="73809-790">For the EVR activation object, do the following:</span></span>

1.  <span data-ttu-id="73809-791">Rufen [**Sie MFCreateVideoRendererActivate auf,**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) um das Aktivierungsobjekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="73809-791">Call [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) to create the activation object.</span></span>
2.  <span data-ttu-id="73809-792">Legen Sie eines der folgenden Attribute für das Aktivierungsobjekt fest:</span><span class="sxs-lookup"><span data-stu-id="73809-792">Set one of the following attributes on the activation object:</span></span> 

    | <span data-ttu-id="73809-793">attribute</span><span class="sxs-lookup"><span data-stu-id="73809-793">Attribute</span></span>                                                                                                         | <span data-ttu-id="73809-794">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="73809-794">Description</span></span>                                                                                                                                                                                                                               |
    |-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [<span data-ttu-id="73809-795">**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_ACTIVATE**</span><span class="sxs-lookup"><span data-stu-id="73809-795">**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_ACTIVATE**</span></span>](mf-activate-custom-video-presenter-activate-attribute.md) | <span data-ttu-id="73809-796">Zeiger auf ein Aktivierungsobjekt für den Presenter.</span><span class="sxs-lookup"><span data-stu-id="73809-796">Pointer to an activation object for the presenter.</span></span><br/> <span data-ttu-id="73809-797">Mit diesem Flag müssen Sie ein Aktivierungsobjekt für Ihre Präsentation bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="73809-797">With this flag, you must provide an activation object for your presenter.</span></span> <span data-ttu-id="73809-798">Das Aktivierungsobjekt muss die [**-SCHNITTSTELLE FÜR DIE-Aktivierung**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) implementieren.</span><span class="sxs-lookup"><span data-stu-id="73809-798">The activation object must implement the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span><br/> |
    | [<span data-ttu-id="73809-799">**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_CLSID**</span><span class="sxs-lookup"><span data-stu-id="73809-799">**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_CLSID**</span></span>](mf-activate-custom-video-presenter-clsid-attribute.md)       | <span data-ttu-id="73809-800">CLSID des Presenters.</span><span class="sxs-lookup"><span data-stu-id="73809-800">CLSID of the presenter.</span></span><br/> <span data-ttu-id="73809-801">Mit diesem Flag muss Ihr Presenter die Standardmäßigerstellung von COM-Objekten über **IClassFactory** unterstützen.</span><span class="sxs-lookup"><span data-stu-id="73809-801">With this flag, your presenter must support standard COM object creation through **IClassFactory**.</span></span><br/>                                                                                         |

    

     

3.  <span data-ttu-id="73809-802">Legen Sie optional das [**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_FLAGS-Attribut**](mf-activate-custom-video-presenter-flags-attribute.md) für das Aktivierungsobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="73809-802">Optionally, set the [**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_FLAGS**](mf-activate-custom-video-presenter-flags-attribute.md) attribute on the activation object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="73809-803">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="73809-803">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73809-804">Erweiterter Videorenderer</span><span class="sxs-lookup"><span data-stu-id="73809-804">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> <dt>

[<span data-ttu-id="73809-805">EVRPresenter-Beispiel</span><span class="sxs-lookup"><span data-stu-id="73809-805">EVRPresenter Sample</span></span>](evrpresenter-sample.md)
</dt> </dl>

 

 
