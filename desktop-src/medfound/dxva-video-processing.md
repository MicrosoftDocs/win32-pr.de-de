---
description: Die DXVA-Videoverarbeitung kapselt die Funktionen der Grafikhardware, die für die Verarbeitung von nicht komprimierten Videobildern verwendet werden. Die Video Verarbeitungsdienste umfassen Deinterlacing und Video Mischung.
ms.assetid: bd688f81-4b7c-4016-b0bd-e40782131f8e
title: DXVA-Video Verarbeitung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf5058d93ddd7c506a501eb6ca07c4661755fc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524544"
---
# <a name="dxva-video-processing"></a><span data-ttu-id="08243-104">DXVA-Video Verarbeitung</span><span class="sxs-lookup"><span data-stu-id="08243-104">DXVA Video Processing</span></span>

<span data-ttu-id="08243-105">Die DXVA-Videoverarbeitung kapselt die Funktionen der Grafikhardware, die für die Verarbeitung von nicht komprimierten Videobildern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="08243-105">DXVA video processing encapsulates the functions of the graphics hardware that are devoted to processing uncompressed video images.</span></span> <span data-ttu-id="08243-106">Die Video Verarbeitungsdienste umfassen Deinterlacing und Video Mischung.</span><span class="sxs-lookup"><span data-stu-id="08243-106">Video processing services include deinterlacing and video mixing.</span></span>

<span data-ttu-id="08243-107">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="08243-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="08243-108">Übersicht</span><span class="sxs-lookup"><span data-stu-id="08243-108">Overview</span></span>](#overview)
-   [<span data-ttu-id="08243-109">Erstellen eines Video Verarbeitungs Geräts</span><span class="sxs-lookup"><span data-stu-id="08243-109">Creating a Video Processing Device</span></span>](#creating-a-video-processing-device)
    -   [<span data-ttu-id="08243-110">Get the idirectxvideoprocess orservice-Zeiger</span><span class="sxs-lookup"><span data-stu-id="08243-110">Get the IDirectXVideoProcessorService Pointer</span></span>](#get-the-idirectxvideoprocessorservice-pointer)
    -   [<span data-ttu-id="08243-111">Auflisten der Video Verarbeitungsgeräte</span><span class="sxs-lookup"><span data-stu-id="08243-111">Enumerate the Video Processing Devices</span></span>](#enumerate-the-video-processing-devices)
    -   [<span data-ttu-id="08243-112">Render-Target Formate aufzählen</span><span class="sxs-lookup"><span data-stu-id="08243-112">Enumerate Render-Target Formats</span></span>](#enumerate-render-target-formats)
    -   [<span data-ttu-id="08243-113">Abfragen der Gerätefunktionen</span><span class="sxs-lookup"><span data-stu-id="08243-113">Query the Device Capabilities</span></span>](#query-the-device-capabilities)
    -   [<span data-ttu-id="08243-114">Erstellen des Geräts</span><span class="sxs-lookup"><span data-stu-id="08243-114">Create the Device</span></span>](#create-the-device)
-   [<span data-ttu-id="08243-115">Video Prozess Blit</span><span class="sxs-lookup"><span data-stu-id="08243-115">Video Process Blit</span></span>](#video-process-blit)
    -   [<span data-ttu-id="08243-116">Blit-Parameter</span><span class="sxs-lookup"><span data-stu-id="08243-116">Blit Parameters</span></span>](#blit-parameters)
    -   [<span data-ttu-id="08243-117">Eingabe Beispiele</span><span class="sxs-lookup"><span data-stu-id="08243-117">Input Samples</span></span>](#input-samples)
-   [<span data-ttu-id="08243-118">Bildkomposition</span><span class="sxs-lookup"><span data-stu-id="08243-118">Image Composition</span></span>](#image-composition)
    -   [<span data-ttu-id="08243-119">Beispiel 1: Briefkasten</span><span class="sxs-lookup"><span data-stu-id="08243-119">Example 1: Letterboxing</span></span>](#example-1-letterboxing)
    -   [<span data-ttu-id="08243-120">Beispiel 2: Stretching von substreamimages</span><span class="sxs-lookup"><span data-stu-id="08243-120">Example 2: Stretching Substream Images</span></span>](#example-2-stretching-substream-images)
    -   [<span data-ttu-id="08243-121">Beispiel 3: nicht übereinstimmende streamhöhen</span><span class="sxs-lookup"><span data-stu-id="08243-121">Example 3: Mismatched Stream Heights</span></span>](#example-3-mismatched-stream-heights)
    -   [<span data-ttu-id="08243-122">Beispiel 4: Ziel Rechteck kleiner als Ziel Oberfläche</span><span class="sxs-lookup"><span data-stu-id="08243-122">Example 4: Target Rectangle Smaller Than Destination Surface</span></span>](#example-4-target-rectangle-smaller-than-destination-surface)
    -   [<span data-ttu-id="08243-123">Beispiel 5: Quell Rechtecke</span><span class="sxs-lookup"><span data-stu-id="08243-123">Example 5: Source Rectangles</span></span>](#example-5-source-rectangles)
    -   [<span data-ttu-id="08243-124">Beispiel 6: überschneidende Ziel Rechtecke</span><span class="sxs-lookup"><span data-stu-id="08243-124">Example 6: Intersecting Destination Rectangles</span></span>](#example-6-intersecting-destination-rectangles)
    -   [<span data-ttu-id="08243-125">Beispiel 7: Stretching und Zuschneiden von Videos</span><span class="sxs-lookup"><span data-stu-id="08243-125">Example 7: Stretching and Cropping Video</span></span>](#example-7-stretching-and-cropping-video)
-   [<span data-ttu-id="08243-126">Eingabe Beispiel Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="08243-126">Input Sample Order</span></span>](#input-sample-order)
    -   [<span data-ttu-id="08243-127">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="08243-127">Example 1</span></span>](#example-1-letterboxing)
    -   [<span data-ttu-id="08243-128">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="08243-128">Example 2</span></span>](#example-2-stretching-substream-images)
    -   [<span data-ttu-id="08243-129">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="08243-129">Example 3</span></span>](#example-3-mismatched-stream-heights)
    -   [<span data-ttu-id="08243-130">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="08243-130">Example 4</span></span>](#example-4-target-rectangle-smaller-than-destination-surface)
-   [<span data-ttu-id="08243-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="08243-131">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="08243-132">Übersicht</span><span class="sxs-lookup"><span data-stu-id="08243-132">Overview</span></span>

<span data-ttu-id="08243-133">Grafikhardware kann die GPU (Graphics Processing Unit) zum Verarbeiten von nicht komprimierten Videobildern verwenden.</span><span class="sxs-lookup"><span data-stu-id="08243-133">Graphics hardware can use the graphics processing unit (GPU) to process uncompressed video images.</span></span> <span data-ttu-id="08243-134">Bei einem *Video Verarbeitungs* Gerät handelt es sich um eine Softwarekomponente, die diese Funktionen kapselt.</span><span class="sxs-lookup"><span data-stu-id="08243-134">A *video processing* device is a software component that encapsulates these functions.</span></span> <span data-ttu-id="08243-135">Anwendungen können ein Video Verarbeitungs Gerät zum Ausführen von Funktionen verwenden, wie z. b.:</span><span class="sxs-lookup"><span data-stu-id="08243-135">Applications can use a video processing device to perform functions such as:</span></span>

-   <span data-ttu-id="08243-136">Deinterlacing und Inverse Telecine</span><span class="sxs-lookup"><span data-stu-id="08243-136">Deinterlacing and inverse telecine</span></span>
-   <span data-ttu-id="08243-137">Mischen von videosubstreams auf das Hauptvideo Bild</span><span class="sxs-lookup"><span data-stu-id="08243-137">Mixing video substreams onto the main video image</span></span>
-   <span data-ttu-id="08243-138">Farbanpassung (ProcAmp) und Bildfilterung</span><span class="sxs-lookup"><span data-stu-id="08243-138">Color adjustment (ProcAmp) and image filtering</span></span>
-   <span data-ttu-id="08243-139">Bildskalierung</span><span class="sxs-lookup"><span data-stu-id="08243-139">Image scaling</span></span>
-   <span data-ttu-id="08243-140">Farb Raum Konvertierung</span><span class="sxs-lookup"><span data-stu-id="08243-140">Color-space conversion</span></span>
-   <span data-ttu-id="08243-141">Alpha Blending</span><span class="sxs-lookup"><span data-stu-id="08243-141">Alpha blending</span></span>

<span data-ttu-id="08243-142">Das folgende Diagramm zeigt die Phasen in der Video Verarbeitungs Pipeline.</span><span class="sxs-lookup"><span data-stu-id="08243-142">The following diagram shows the stages in the video processing pipeline.</span></span> <span data-ttu-id="08243-143">Das Diagramm soll keine tatsächliche Implementierung darstellen.</span><span class="sxs-lookup"><span data-stu-id="08243-143">The diagram is not meant to show an actual implementation.</span></span> <span data-ttu-id="08243-144">Beispielsweise kann der Grafiktreiber mehrere Stufen zu einem einzigen Vorgang zusammenfassen.</span><span class="sxs-lookup"><span data-stu-id="08243-144">For example, the graphics driver might combine several stages into a single operation.</span></span> <span data-ttu-id="08243-145">Alle diese Vorgänge können mit einem einzelnen-Befehl für das Video Verarbeitungs Gerät durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="08243-145">All of these operations can be performed in a single call to the video processing device.</span></span> <span data-ttu-id="08243-146">Einige der hier gezeigten Phasen, z. b. das Filtern von Filtern und Filtern, werden möglicherweise nicht vom Treiber unterstützt.</span><span class="sxs-lookup"><span data-stu-id="08243-146">Some stages shown here, such as noise and detail filtering, might not be supported by the driver.</span></span>

![das Diagramm zeigt die Phasen der DXVA-Videoverarbeitung an.](images/8581554e-a1bc-4cab-9ae1-99a6537e2a84.gif)

<span data-ttu-id="08243-148">Die Eingabe für die Video Verarbeitungs Pipeline enthält immer einen *primären* Videostream, der die Daten des Haupt Bilds enthält.</span><span class="sxs-lookup"><span data-stu-id="08243-148">The input to the video processing pipeline always includes a *primary* video stream, which contains the main image data.</span></span> <span data-ttu-id="08243-149">Der primäre Videostream bestimmt die Framerate für das Ausgabevideo.</span><span class="sxs-lookup"><span data-stu-id="08243-149">The primary video stream determines the frame rate for the output video.</span></span> <span data-ttu-id="08243-150">Jeder Frame des Ausgabevideos wird relativ zu den Eingabedaten aus dem primären Videostream berechnet.</span><span class="sxs-lookup"><span data-stu-id="08243-150">Each frame of the output video is calculated relative to the input data from the primary video stream.</span></span> <span data-ttu-id="08243-151">Pixel im primären Stream sind immer transparent, ohne Pixel-Alpha-Daten.</span><span class="sxs-lookup"><span data-stu-id="08243-151">Pixels in the primary stream are always opaque, with no per-pixel alpha data.</span></span> <span data-ttu-id="08243-152">Der primäre Videostream kann progressiv oder mit Zeilen Sprung sein.</span><span class="sxs-lookup"><span data-stu-id="08243-152">The primary video stream can be progressive or interlaced.</span></span>

<span data-ttu-id="08243-153">Optional kann die Video Verarbeitungs Pipeline bis zu 15 videosubstreams empfangen.</span><span class="sxs-lookup"><span data-stu-id="08243-153">Optionally, the video processing pipeline can receive up to 15 video substreams.</span></span> <span data-ttu-id="08243-154">Ein unter Datenstrom enthält zusätzliche Bilddaten, z. b. geschlossene Beschriftungen oder DVD-Teilbilder.</span><span class="sxs-lookup"><span data-stu-id="08243-154">A substream contains auxiliary image data, such as closed captions or DVD subpictures.</span></span> <span data-ttu-id="08243-155">Diese Bilder werden über den primären Videostream angezeigt und sind im Allgemeinen nicht für sich selbst zu sehen.</span><span class="sxs-lookup"><span data-stu-id="08243-155">These images are displayed over the primary video stream, and are generally not meant to be shown by themselves.</span></span> <span data-ttu-id="08243-156">Substreambilder können Alpha Daten pro Pixel enthalten und sind immer progressive Frames.</span><span class="sxs-lookup"><span data-stu-id="08243-156">Substream pictures can contain per-pixel alpha data, and are always progressive frames.</span></span> <span data-ttu-id="08243-157">Das Video für die Videoverarbeitung verbindet die substreambilder mit dem aktuellen deintercherungs-Frame aus dem primären Videostream.</span><span class="sxs-lookup"><span data-stu-id="08243-157">The video processing device alpha-blends the substream images with the current deinterlaced frame from the primary video stream.</span></span>

<span data-ttu-id="08243-158">Im restlichen Teil dieses Themas wird der Begriff *Bild* für die Eingabedaten für ein Video Verarbeitungs Gerät verwendet.</span><span class="sxs-lookup"><span data-stu-id="08243-158">In the remainder of this topic, the term *picture* is used for the input data to a video processing device.</span></span> <span data-ttu-id="08243-159">Ein Bild kann aus einem progressiven Frame, einem einzelnen Feld oder zwei verschachtelten Feldern bestehen.</span><span class="sxs-lookup"><span data-stu-id="08243-159">A picture might consist of a progressive frame, a single field, or two interleaved fields.</span></span> <span data-ttu-id="08243-160">Die Ausgabe ist immer ein Deinterlacing-Frame.</span><span class="sxs-lookup"><span data-stu-id="08243-160">The output is always a deinterlaced frame.</span></span>

<span data-ttu-id="08243-161">Ein Videotreiber kann mehr als ein Video Verarbeitungs Gerät implementieren, um unterschiedliche Sätze von Video Verarbeitungsfunktionen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="08243-161">A video driver can implement more than one video processing device, to provide different sets of video processing capabilities.</span></span> <span data-ttu-id="08243-162">Geräte werden anhand der GUID identifiziert.</span><span class="sxs-lookup"><span data-stu-id="08243-162">Devices are identified by GUID.</span></span> <span data-ttu-id="08243-163">Die folgenden GUIDs sind vordefiniert:</span><span class="sxs-lookup"><span data-stu-id="08243-163">The following GUIDs are predefined:</span></span>

-   <span data-ttu-id="08243-164">**DXVA2 \_ Videoprocbobdevice**.</span><span class="sxs-lookup"><span data-stu-id="08243-164">**DXVA2\_VideoProcBobDevice**.</span></span> <span data-ttu-id="08243-165">Dieses Gerät führt Bob Deinterlacing aus.</span><span class="sxs-lookup"><span data-stu-id="08243-165">This device performs bob deinterlacing.</span></span>
-   <span data-ttu-id="08243-166">**DXVA2 \_ Videoprocprogressivedevice**.</span><span class="sxs-lookup"><span data-stu-id="08243-166">**DXVA2\_VideoProcProgressiveDevice**.</span></span> <span data-ttu-id="08243-167">Dieses Gerät wird verwendet, wenn das Video nur progressive Frames ohne Zeilen Sprung enthält.</span><span class="sxs-lookup"><span data-stu-id="08243-167">This device is used if the video contains only progressive frames, with no interlaced frames.</span></span> <span data-ttu-id="08243-168">(Einige Videoinhalte enthalten eine Mischung aus progressiven und Zeilen Sprung enden Frames.</span><span class="sxs-lookup"><span data-stu-id="08243-168">(Some video content contains a mix of progressive and interlaced frames.</span></span> <span data-ttu-id="08243-169">Das progressive Gerät kann nicht für diese Art von "gemischtem" Videoinhalt verwendet werden, da für die Zeilen Sprung Rahmen ein Deinterlacing-Schritt erforderlich ist.)</span><span class="sxs-lookup"><span data-stu-id="08243-169">The progressive device cannot be used for this kind of "mixed" video content, because a deinterlacing step is required for the interlaced frames.)</span></span>

<span data-ttu-id="08243-170">Jeder Grafiktreiber, der die DXVA-Videoverarbeitung unterstützt, muss mindestens diese beiden Geräte implementieren.</span><span class="sxs-lookup"><span data-stu-id="08243-170">Every graphics driver that supports DXVA video processing must implement at least these two devices.</span></span> <span data-ttu-id="08243-171">Der Grafiktreiber kann auch andere Geräte bereitstellen, die durch Treiber spezifische GUIDs identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="08243-171">The graphics driver may also provide other devices, which are identified by driver-specific GUIDs.</span></span> <span data-ttu-id="08243-172">Ein Treiber könnte z. b. einen proprietären deinterlacingalgorithmus implementieren, der eine bessere Qualitäts Ausgabe als Bob Deinterlacing erzeugt.</span><span class="sxs-lookup"><span data-stu-id="08243-172">For example, a driver might implement a proprietary deinterlacing algorithm that produces better quality output than bob deinterlacing.</span></span> <span data-ttu-id="08243-173">Einige deinterlacingalgorithmen erfordern möglicherweise Forward-oder rückwärts Verweis Bilder aus dem primären Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="08243-173">Some deinterlacing algorithms may require forward or backward reference pictures from the primary stream.</span></span> <span data-ttu-id="08243-174">Wenn dies der Fall ist, muss der Aufrufer diese Bilder dem Treiber in der richtigen Reihenfolge bereitstellen, wie weiter unten in diesem Abschnitt beschrieben.</span><span class="sxs-lookup"><span data-stu-id="08243-174">If so, the caller must provide these pictures to the driver in the correct sequence, as described later in this section.</span></span>

<span data-ttu-id="08243-175">Außerdem wird ein Referenz Software-Gerät bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="08243-175">A reference software device is also provided.</span></span> <span data-ttu-id="08243-176">Das Software Gerät ist für die Qualität und nicht für die Geschwindigkeit optimiert und eignet sich möglicherweise nicht für die Echt Zeit Videoverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="08243-176">The software device is optimized for quality rather than speed, and may not be adequate for real-time video processing.</span></span> <span data-ttu-id="08243-177">Das Referenz Software Gerät verwendet den GUID-Wert DXVA2 \_ videoprocsoftwaredevice.</span><span class="sxs-lookup"><span data-stu-id="08243-177">The reference software device uses the GUID value DXVA2\_VideoProcSoftwareDevice.</span></span>

## <a name="creating-a-video-processing-device"></a><span data-ttu-id="08243-178">Erstellen eines Video Verarbeitungs Geräts</span><span class="sxs-lookup"><span data-stu-id="08243-178">Creating a Video Processing Device</span></span>

<span data-ttu-id="08243-179">Vor der Verwendung der DXVA-Videoverarbeitung muss von der Anwendung ein Video Verarbeitungs Gerät erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="08243-179">Before using DXVA video processing, the application must create a video processing device.</span></span> <span data-ttu-id="08243-180">Im folgenden finden Sie eine kurze Übersicht über die Schritte, die im restlichen Teil dieses Abschnitts ausführlicher erläutert werden:</span><span class="sxs-lookup"><span data-stu-id="08243-180">Here is a brief outline of the steps, which are explained in greater detail in the remainder of this section:</span></span>

1.  <span data-ttu-id="08243-181">Einen Zeiger auf die [**idirectxvideoprocess orservice**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) -Schnittstelle erhalten.</span><span class="sxs-lookup"><span data-stu-id="08243-181">Get a pointer to the [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) interface.</span></span>
2.  <span data-ttu-id="08243-182">Erstellen Sie eine Beschreibung des Video Formats für den primären Videostream.</span><span class="sxs-lookup"><span data-stu-id="08243-182">Create a description of the video format for the primary video stream.</span></span> <span data-ttu-id="08243-183">Verwenden Sie diese Beschreibung, um eine Liste der Video Verarbeitungsgeräte zu erhalten, die das Videoformat unterstützen.</span><span class="sxs-lookup"><span data-stu-id="08243-183">Use this description to get a list of the video processing devices that support the video format.</span></span> <span data-ttu-id="08243-184">Geräte werden anhand der GUID identifiziert.</span><span class="sxs-lookup"><span data-stu-id="08243-184">Devices are identified by GUID.</span></span>
3.  <span data-ttu-id="08243-185">Für ein bestimmtes Gerät wird eine Liste der vom Gerät unterstützten renderzielformate angezeigt.</span><span class="sxs-lookup"><span data-stu-id="08243-185">For a particular device, get a list of render-target formats supported by the device.</span></span> <span data-ttu-id="08243-186">Die Formate werden als Liste von **D3DFORMAT** -Werten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="08243-186">The formats are returned as a list of **D3DFORMAT** values.</span></span> <span data-ttu-id="08243-187">Wenn Sie das Mischen von Substreams planen, können Sie auch eine Liste der unterstützten substreamformate erhalten.</span><span class="sxs-lookup"><span data-stu-id="08243-187">If you plan to mix substreams, get a list of the supported substream formats as well.</span></span>
4.  <span data-ttu-id="08243-188">Fragen Sie die Funktionen der einzelnen Geräte ab.</span><span class="sxs-lookup"><span data-stu-id="08243-188">Query the capabilities of each device.</span></span>
5.  <span data-ttu-id="08243-189">Erstellen Sie das Video für die Verarbeitung von Geräten.</span><span class="sxs-lookup"><span data-stu-id="08243-189">Create the video processing device.</span></span>

<span data-ttu-id="08243-190">Manchmal können Sie einige dieser Schritte weglassen.</span><span class="sxs-lookup"><span data-stu-id="08243-190">Sometimes you can omit some of these steps.</span></span> <span data-ttu-id="08243-191">Anstatt z. b. die Liste der renderzielformate zu erhalten, können Sie einfach versuchen, das Video Verarbeitungs Gerät in Ihrem bevorzugten Format zu erstellen, und überprüfen, ob es erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="08243-191">For example, instead of getting the list of render-target formats, you could simply try creating the video processing device with your preferred format, and see if it succeeds.</span></span> <span data-ttu-id="08243-192">Ein gängiges Format, z \_ . b. D3DFMT X8R8G8B8, ist wahrscheinlich erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="08243-192">A common format such as D3DFMT\_X8R8G8B8 is likely to succeed.</span></span>

<span data-ttu-id="08243-193">Im restlichen Teil dieses Abschnitts werden diese Schritte ausführlich beschrieben.</span><span class="sxs-lookup"><span data-stu-id="08243-193">The remainder of this section describes these steps in detail.</span></span>

### <a name="get-the-idirectxvideoprocessorservice-pointer"></a><span data-ttu-id="08243-194">Get the idirectxvideoprocess orservice-Zeiger</span><span class="sxs-lookup"><span data-stu-id="08243-194">Get the IDirectXVideoProcessorService Pointer</span></span>

<span data-ttu-id="08243-195">Die [**idirectxvideoprocess orservice**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) -Schnittstelle wird vom Direct3D-Gerät abgerufen.</span><span class="sxs-lookup"><span data-stu-id="08243-195">The [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) interface is obtained from the Direct3D device.</span></span> <span data-ttu-id="08243-196">Es gibt zwei Möglichkeiten, einen Zeiger auf diese Schnittstelle zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="08243-196">There are two ways to get a pointer to this interface:</span></span>

-   <span data-ttu-id="08243-197">Von einem Direct3D-Gerät aus.</span><span class="sxs-lookup"><span data-stu-id="08243-197">From a Direct3D device.</span></span>
-   <span data-ttu-id="08243-198">Aus dem [Direct3D-Device Manager](direct3d-device-manager.md).</span><span class="sxs-lookup"><span data-stu-id="08243-198">From the [Direct3D Device Manager](direct3d-device-manager.md).</span></span>

<span data-ttu-id="08243-199">Wenn Sie einen Zeiger auf ein Direct3D-Gerät haben, können Sie einen [**idirectxvideoprocess orservice**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) -Zeiger abrufen, indem Sie die [**DXVA2CreateVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createvideoservice) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="08243-199">If you have a pointer to a Direct3D device, you can get an [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) pointer by calling the [**DXVA2CreateVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createvideoservice) function.</span></span> <span data-ttu-id="08243-200">Übergeben Sie einen Zeiger auf die **IDirect3DDevice9** -Schnittstelle des Geräts, und geben Sie **IID \_ idirectxvideoprocess orservice** für den *riid* -Parameter an, wie im folgenden Code gezeigt:</span><span class="sxs-lookup"><span data-stu-id="08243-200">Pass in a pointer to the device's **IDirect3DDevice9** interface, and specify **IID\_IDirectXVideoProcessorService** for the *riid* parameter, as shown in the following code:</span></span>


```C++
    // Create the DXVA-2 Video Processor service.
    hr = DXVA2CreateVideoService(g_pD3DD9, IID_PPV_ARGS(&g_pDXVAVPS));
```



<span data-ttu-id="08243-201">in einigen Fällen wird das Direct3D-Gerät von einem Objekt erstellt und dann über das [Direct3D-Device Manager](direct3d-device-manager.md)mit anderen Objekten geteilt.</span><span class="sxs-lookup"><span data-stu-id="08243-201">n some cases, one object creates the Direct3D device and then shares it with other objects through the [Direct3D Device Manager](direct3d-device-manager.md).</span></span> <span data-ttu-id="08243-202">In dieser Situation können Sie [**IDirect3DDeviceManager9:: getvideoservice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) auf dem Geräte-Manager aufrufen, um den [**idirectxvideoprocess orservice**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) -Zeiger abzurufen, wie im folgenden Code gezeigt:</span><span class="sxs-lookup"><span data-stu-id="08243-202">In this situation, you can call [**IDirect3DDeviceManager9::GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) on the device manager to get the [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) pointer, as shown in the following code:</span></span>


```C++
HRESULT GetVideoProcessorService(
    IDirect3DDeviceManager9 *pDeviceManager,
    IDirectXVideoProcessorService **ppVPService
    )
{
    *ppVPService = NULL;

    HANDLE hDevice;

    HRESULT hr = pDeviceManager->OpenDeviceHandle(&hDevice);
    if (SUCCEEDED(hr))
    {
        // Get the video processor service 
        HRESULT hr2 = pDeviceManager->GetVideoService(
            hDevice, 
            IID_PPV_ARGS(ppVPService)
            );

        // Close the device handle.
        hr = pDeviceManager->CloseDeviceHandle(hDevice);

        if (FAILED(hr2))
        {
            hr = hr2;
        }
    }

    if (FAILED(hr))
    {
        SafeRelease(ppVPService);
    }

    return hr;
}
```



### <a name="enumerate-the-video-processing-devices"></a><span data-ttu-id="08243-203">Auflisten der Video Verarbeitungsgeräte</span><span class="sxs-lookup"><span data-stu-id="08243-203">Enumerate the Video Processing Devices</span></span>

<span data-ttu-id="08243-204">Um eine Liste der Video Verarbeitungsgeräte zu erhalten, geben Sie eine [**DXVA2 \_ videodesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) -Struktur mit dem Format des primären Videostreams ein, und übergeben Sie diese Struktur an die [**idirectxvideoprocess orservice:: getvideoprocess ordeviceguids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) -Methode.</span><span class="sxs-lookup"><span data-stu-id="08243-204">To get a list of video processing devices, fill in a [**DXVA2\_VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) structure with the format of the primary video stream, and pass this structure to the [**IDirectXVideoProcessorService::GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) method.</span></span> <span data-ttu-id="08243-205">Die-Methode gibt ein Array von GUIDs zurück, eines für jedes Video Verarbeitungs Gerät, das in diesem Videoformat verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="08243-205">The method returns an array of GUIDs, one for each video processing device that can be used with this video format.</span></span>

<span data-ttu-id="08243-206">Stellen Sie sich eine Anwendung vor, die einen Videostream im im YUY2-Format rendert, indem Sie die BT. 709-Definition von YUV Color mit einer Frame Rate von 29,97 Frames pro Sekunde verwendet.</span><span class="sxs-lookup"><span data-stu-id="08243-206">Consider an application that renders a video stream in YUY2 format, using the BT.709 definition of YUV color, with a frame rate of 29.97 frames per second.</span></span> <span data-ttu-id="08243-207">Nehmen Sie an, dass der Videoinhalt vollständig aus progressiven Frames besteht.</span><span class="sxs-lookup"><span data-stu-id="08243-207">Assume that the video content consists entirely of progressive frames.</span></span> <span data-ttu-id="08243-208">Das folgende Code Fragment zeigt, wie Sie die Formatbeschreibung ausfüllen und die Geräte-GUIDs erhalten:</span><span class="sxs-lookup"><span data-stu-id="08243-208">The following code fragment shows how to fill in the format description and get the device GUIDs:</span></span>


```C++
    // Initialize the video descriptor.

    g_VideoDesc.SampleWidth                         = VIDEO_MAIN_WIDTH;
    g_VideoDesc.SampleHeight                        = VIDEO_MAIN_HEIGHT;
    g_VideoDesc.SampleFormat.VideoChromaSubsampling = DXVA2_VideoChromaSubsampling_MPEG2;
    g_VideoDesc.SampleFormat.NominalRange           = DXVA2_NominalRange_16_235;
    g_VideoDesc.SampleFormat.VideoTransferMatrix    = EX_COLOR_INFO[g_ExColorInfo][0];
    g_VideoDesc.SampleFormat.VideoLighting          = DXVA2_VideoLighting_dim;
    g_VideoDesc.SampleFormat.VideoPrimaries         = DXVA2_VideoPrimaries_BT709;
    g_VideoDesc.SampleFormat.VideoTransferFunction  = DXVA2_VideoTransFunc_709;
    g_VideoDesc.SampleFormat.SampleFormat           = DXVA2_SampleProgressiveFrame;
    g_VideoDesc.Format                              = VIDEO_MAIN_FORMAT;
    g_VideoDesc.InputSampleFreq.Numerator           = VIDEO_FPS;
    g_VideoDesc.InputSampleFreq.Denominator         = 1;
    g_VideoDesc.OutputFrameFreq.Numerator           = VIDEO_FPS;
    g_VideoDesc.OutputFrameFreq.Denominator         = 1;

    // Query the video processor GUID.

    UINT count;
    GUID* guids = NULL;

    hr = g_pDXVAVPS->GetVideoProcessorDeviceGuids(&g_VideoDesc, &count, &guids);
```



<span data-ttu-id="08243-209">Der Code für dieses Beispiel stammt aus dem [DXVA2 \_ videoproc](dxva2-videoproc-sample.md) SDK-Beispiel.</span><span class="sxs-lookup"><span data-stu-id="08243-209">The code for this example is taken from the [DXVA2\_VideoProc](dxva2-videoproc-sample.md) SDK sample.</span></span>

<span data-ttu-id="08243-210">Das *pguids* -Array in diesem Beispiel wird von der [**getvideoprocess ordeviceguids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) -Methode zugeordnet, sodass die Anwendung das Array durch Aufrufen von [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree)freigeben muss.</span><span class="sxs-lookup"><span data-stu-id="08243-210">The *pGuids* array in this example is allocated by the [**GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) method, so the application must free the array by calling [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span> <span data-ttu-id="08243-211">Die verbleibenden Schritte können mithilfe der von dieser Methode zurückgegebenen Geräte-GUIDs ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="08243-211">The remaining steps can be performed using any of the device GUIDs returned by this method.</span></span>

### <a name="enumerate-render-target-formats"></a><span data-ttu-id="08243-212">Render-Target Formate aufzählen</span><span class="sxs-lookup"><span data-stu-id="08243-212">Enumerate Render-Target Formats</span></span>

<span data-ttu-id="08243-213">Um die Liste der vom Gerät unterstützten renderzielformate zu erhalten, übergeben Sie die Geräte-GUID und die [**DXVA2 \_ videodesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) -Struktur an die [**idirectxvideoprocess orservice:: getvideoprocesorrendertargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorrendertargets) -Methode, wie im folgenden Code gezeigt:</span><span class="sxs-lookup"><span data-stu-id="08243-213">To get the list of render-target formats supported by the device, pass the device GUID and the [**DXVA2\_VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) structure to the [**IDirectXVideoProcessorService::GetVideoProcessorRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorrendertargets) method, as shown in the following code:</span></span>


```C++
    // Query the supported render-target formats.

    UINT i, count;
    D3DFORMAT* formats = NULL;

    HRESULT hr = g_pDXVAVPS->GetVideoProcessorRenderTargets(
        guid, &g_VideoDesc, &count, &formats);

    if (FAILED(hr))
    {
        DBGMSG((L"GetVideoProcessorRenderTargets failed: 0x%x.\n", hr));
        return FALSE;
    }

    for (i = 0; i < count; i++)
    {
        if (formats[i] == VIDEO_RENDER_TARGET_FORMAT)
        {
            break;
        }
    }

    CoTaskMemFree(formats);

    if (i >= count)
    {
        DBGMSG((L"The device does not support the render-target format.\n"));
        return FALSE;
    }
```



<span data-ttu-id="08243-214">Die-Methode gibt ein Array von **D3DFORMAT** -Werten zurück.</span><span class="sxs-lookup"><span data-stu-id="08243-214">The method returns an array of **D3DFORMAT** values.</span></span> <span data-ttu-id="08243-215">In diesem Beispiel, in dem der Eingabetyp "im YUY2" ist, kann eine typische Liste von Formaten D3DFMT \_ X8R8G8B8 (32 Bit RGB) und D3DMFT \_ im YUY2 (Eingabeformat) sein.</span><span class="sxs-lookup"><span data-stu-id="08243-215">In this example, where the input type is YUY2, a typical list of formats might be D3DFMT\_X8R8G8B8 (32-bit RGB) and D3DMFT\_YUY2 (the input format).</span></span> <span data-ttu-id="08243-216">Die genaue Liste hängt jedoch vom Treiber ab.</span><span class="sxs-lookup"><span data-stu-id="08243-216">However, the exact list will depend on the driver.</span></span>

<span data-ttu-id="08243-217">Die Liste der verfügbaren Formate für die untergeordneten Datenströme kann je nach Format des Renderziels und des Eingabe Formats variieren.</span><span class="sxs-lookup"><span data-stu-id="08243-217">The list of available formats for the substreams can vary depending on the render-target format and the input format.</span></span> <span data-ttu-id="08243-218">Um die Liste der substreamformate zu erhalten, übergeben Sie die Geräte-GUID, die Format Struktur und das renderzielformat an die [**idirectxvideoprocess orservice:: getvideoprocesorsubstreamformats**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorsubstreamformats) -Methode, wie im folgenden Code gezeigt:</span><span class="sxs-lookup"><span data-stu-id="08243-218">To get the list of substream formats, pass the device GUID, the format structure, and the render-target format to the [**IDirectXVideoProcessorService::GetVideoProcessorSubStreamFormats**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorsubstreamformats) method, as shown in the following code:</span></span>


```C++
    // Query the supported substream formats.

    formats = NULL;

    hr = g_pDXVAVPS->GetVideoProcessorSubStreamFormats(
        guid, &g_VideoDesc, VIDEO_RENDER_TARGET_FORMAT, &count, &formats);

    if (FAILED(hr))
    {
        DBGMSG((L"GetVideoProcessorSubStreamFormats failed: 0x%x.\n", hr));
        return FALSE;
    }

    for (i = 0; i < count; i++)
    {
        if (formats[i] == VIDEO_SUB_FORMAT)
        {
            break;
        }
    }

    CoTaskMemFree(formats);

    if (i >= count)
    {
        DBGMSG((L"The device does not support the substream format.\n"));
        return FALSE;
    }
```



<span data-ttu-id="08243-219">Diese Methode gibt ein weiteres Array von **D3DFORMAT** -Werten zurück.</span><span class="sxs-lookup"><span data-stu-id="08243-219">This method returns another array of **D3DFORMAT** values.</span></span> <span data-ttu-id="08243-220">Typische substreamformate sind ayuv und AI44.</span><span class="sxs-lookup"><span data-stu-id="08243-220">Typical substream formats are AYUV and AI44.</span></span>

### <a name="query-the-device-capabilities"></a><span data-ttu-id="08243-221">Abfragen der Gerätefunktionen</span><span class="sxs-lookup"><span data-stu-id="08243-221">Query the Device Capabilities</span></span>

<span data-ttu-id="08243-222">Wenn Sie die Funktionen eines bestimmten Geräts nutzen möchten, übergeben Sie die Geräte-GUID, die Format Struktur und ein renderzielformat an die [**idirectxvideoprocess orservice:: getvideoprocess orcaps**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorcaps) -Methode.</span><span class="sxs-lookup"><span data-stu-id="08243-222">To get the capabilities of a particular device, pass the device GUID, the format structure, and a render-target format to the [**IDirectXVideoProcessorService::GetVideoProcessorCaps**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorcaps) method.</span></span> <span data-ttu-id="08243-223">Die-Methode füllt eine [**DXVA2 \_ videoprocess orcaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) -Struktur Struktur mit den Gerätefunktionen auf.</span><span class="sxs-lookup"><span data-stu-id="08243-223">The method fills in a [**DXVA2\_VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) structure structure with the device capabilities.</span></span>


```C++
    // Query video processor capabilities.

    hr = g_pDXVAVPS->GetVideoProcessorCaps(
        guid, &g_VideoDesc, VIDEO_RENDER_TARGET_FORMAT, &g_VPCaps);

    if (FAILED(hr))
    {
        DBGMSG((L"GetVideoProcessorCaps failed: 0x%x.\n", hr));
        return FALSE;
    }
```



### <a name="create-the-device"></a><span data-ttu-id="08243-224">Erstellen des Geräts</span><span class="sxs-lookup"><span data-stu-id="08243-224">Create the Device</span></span>

<span data-ttu-id="08243-225">Um das Video Processing-Gerät zu erstellen, rufen Sie [**idirectxvideoprocessorservice:: "kreatevideoprocessor**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-createvideoprocessor)" auf.</span><span class="sxs-lookup"><span data-stu-id="08243-225">To create the video processing device, call [**IDirectXVideoProcessorService::CreateVideoProcessor**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-createvideoprocessor).</span></span> <span data-ttu-id="08243-226">Die Eingabe für diese Methode ist die Geräte-GUID, die Formatbeschreibung, das renderzielformat und die maximale Anzahl der zu mischenden Substreams.</span><span class="sxs-lookup"><span data-stu-id="08243-226">The input to this method is the device GUID, the format description, the render-target format, and the maximum number of substreams that you plan to mix.</span></span> <span data-ttu-id="08243-227">Die-Methode gibt einen Zeiger auf die [**idirectxvideoprocessor**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor) -Schnittstelle zurück, die das Video Verarbeitungs Gerät darstellt.</span><span class="sxs-lookup"><span data-stu-id="08243-227">The method returns a pointer to the [**IDirectXVideoProcessor**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor) interface, which represents the video processing device.</span></span>


```C++
    // Finally create a video processor device.

    hr = g_pDXVAVPS->CreateVideoProcessor(
        guid,
        &g_VideoDesc,
        VIDEO_RENDER_TARGET_FORMAT,
        SUB_STREAM_COUNT,
        &g_pDXVAVPD
        );
```



## <a name="video-process-blit"></a><span data-ttu-id="08243-228">Video Prozess Blit</span><span class="sxs-lookup"><span data-stu-id="08243-228">Video Process Blit</span></span>

<span data-ttu-id="08243-229">Der Hauptvideo Verarbeitungsvorgang ist das *Video Processing Blit*.</span><span class="sxs-lookup"><span data-stu-id="08243-229">The main video processing operation is the *video processing blit*.</span></span> <span data-ttu-id="08243-230">(Ein *Blit* ist jeder Vorgang, bei dem zwei oder mehr Bitmaps zu einer einzelnen Bitmap kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="08243-230">(A *blit* is any operation that combines two or more bitmaps into a single bitmap.</span></span> <span data-ttu-id="08243-231">Ein Video Processing Blit kombiniert Eingabe Bilder, um einen Ausgabe Frame zu erstellen.) Um ein Blit für die Videoverarbeitung auszuführen, nennen Sie [**idirectxvideoprocessor:: videoprocessblt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt).</span><span class="sxs-lookup"><span data-stu-id="08243-231">A video processing blit combines input pictures to create an output frame.) To perform a video processing blit, call [**IDirectXVideoProcessor::VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt).</span></span> <span data-ttu-id="08243-232">Diese Methode übergibt eine Reihe von Videobeispielen an das Video Verarbeitungs Gerät.</span><span class="sxs-lookup"><span data-stu-id="08243-232">This method passes a set of video samples to the video processing device.</span></span> <span data-ttu-id="08243-233">Als Antwort verarbeitet das Video Verarbeitungs Gerät die Eingabe Bilder und generiert einen Ausgabe Frame.</span><span class="sxs-lookup"><span data-stu-id="08243-233">In response, the video processing device processes the input pictures and generates one output frame.</span></span> <span data-ttu-id="08243-234">Die Verarbeitung kann Deinterlacing, Farb Raum Konvertierung und unter Datenstrom-Vermischung einschließen.</span><span class="sxs-lookup"><span data-stu-id="08243-234">Processing can include deinterlacing, color-space conversion, and substream mixing.</span></span> <span data-ttu-id="08243-235">Die Ausgabe wird auf eine vom Aufrufer bereitgestellte Ziel Oberfläche geschrieben.</span><span class="sxs-lookup"><span data-stu-id="08243-235">The output is written to a destination surface provided by the caller.</span></span>

<span data-ttu-id="08243-236">Die [**videoprocess BLT**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) -Methode übernimmt die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="08243-236">The [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) method takes the following parameters:</span></span>

-   <span data-ttu-id="08243-237">*PRT* verweist auf eine **IDirect3DSurface9** -Renderziel-Oberfläche, die den verarbeiteten Videorahmen empfängt.</span><span class="sxs-lookup"><span data-stu-id="08243-237">*pRT* points to an **IDirect3DSurface9** render target surface that will receive the processed video frame.</span></span>
-   <span data-ttu-id="08243-238">*pbltparameams* verweist auf eine [**DXVA2 \_ videoprocess bltparameams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) -Struktur, die die Parameter für den Blit angibt.</span><span class="sxs-lookup"><span data-stu-id="08243-238">*pBltParams* points to a [**DXVA2\_VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) structure that specifies the parameters for the blit.</span></span>
-   <span data-ttu-id="08243-239">*psamples* ist die Adresse eines Arrays von [**DXVA2 \_ Videosample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="08243-239">*pSamples* is the address of an array of [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structures.</span></span> <span data-ttu-id="08243-240">Diese Strukturen enthalten die Eingabe Beispiele für den Blit.</span><span class="sxs-lookup"><span data-stu-id="08243-240">These structures contain the input samples for the blit.</span></span>
-   <span data-ttu-id="08243-241">*NumSamples* gibt die Größe des *psamples* -Arrays an.</span><span class="sxs-lookup"><span data-stu-id="08243-241">*NumSamples* gives the size of the *pSamples* array.</span></span>
-   <span data-ttu-id="08243-242">Der *reservierte* Parameter ist reserviert und sollte auf **null** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="08243-242">The *Reserved* parameter is reserved and should be set to **NULL**.</span></span>

<span data-ttu-id="08243-243">Im *psamples* -Array muss der Aufrufer die folgenden Eingabe Beispiele bereitstellen:</span><span class="sxs-lookup"><span data-stu-id="08243-243">In the *pSamples* array, the caller must provide the following input samples:</span></span>

-   <span data-ttu-id="08243-244">Das aktuelle Bild aus dem primären Videostream.</span><span class="sxs-lookup"><span data-stu-id="08243-244">The current picture from the primary video stream.</span></span>
-   <span data-ttu-id="08243-245">Vorwärts-und rückwärts Verweis Bilder, wenn dies für den Deinterlacing-Algorithmus erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="08243-245">Forward and backward reference pictures, if required by the deinterlacing algorithm.</span></span>
-   <span data-ttu-id="08243-246">0 (null) oder mehr substreambilder, maximal 15 unter Ströme.</span><span class="sxs-lookup"><span data-stu-id="08243-246">Zero or more substream pictures, up to a maximum of 15 substreams.</span></span>

<span data-ttu-id="08243-247">Der Treiber erwartet, dass dieses Array in einer bestimmten Reihenfolge angezeigt wird, wie in der [Eingabe Stichprobe-Reihenfolge](#input-sample-order)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="08243-247">The driver expects this array to be in a particular order, as described in [Input Sample Order](#input-sample-order).</span></span>

### <a name="blit-parameters"></a><span data-ttu-id="08243-248">Blit-Parameter</span><span class="sxs-lookup"><span data-stu-id="08243-248">Blit Parameters</span></span>

<span data-ttu-id="08243-249">Die [**DXVA2 \_ videoprocess bltparameams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) -Struktur enthält allgemeine Parameter für den Blit.</span><span class="sxs-lookup"><span data-stu-id="08243-249">The [**DXVA2\_VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) structure contains general parameters for the blit.</span></span> <span data-ttu-id="08243-250">Die wichtigsten Parameter werden in den folgenden Membern der-Struktur gespeichert:</span><span class="sxs-lookup"><span data-stu-id="08243-250">The most important parameters are stored in the following members of the structure:</span></span>

-   <span data-ttu-id="08243-251">**TargetFrame** ist die Präsentationszeit des Ausgabe Frames.</span><span class="sxs-lookup"><span data-stu-id="08243-251">**TargetFrame** is the presentation time of the output frame.</span></span> <span data-ttu-id="08243-252">Bei progressivem Inhalt muss dieser Zeitrahmen der Startzeit für den aktuellen Frame aus dem primären Videostream entsprechen.</span><span class="sxs-lookup"><span data-stu-id="08243-252">For progressive content, this time must equal the start time for the current frame from the primary video stream.</span></span> <span data-ttu-id="08243-253">Diese Zeit wird im **StartMember** der [**DXVA2 \_ Videosample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) -Struktur für dieses Eingabe Beispiel angegeben.</span><span class="sxs-lookup"><span data-stu-id="08243-253">This time is specified in the **Start** member of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure for that input sample.</span></span>

    <span data-ttu-id="08243-254">Beim Zeilen Sprung Inhalt erzeugt ein Frame mit zwei verschachtelten Feldern zwei Deinterlacing-Ausgabe Frames.</span><span class="sxs-lookup"><span data-stu-id="08243-254">For interlaced content, a frame with two interleaved fields produces two deinterlaced output frames.</span></span> <span data-ttu-id="08243-255">Beim ersten Ausgabe Frame muss die Präsentationszeit mit der Startzeit des aktuellen Bilds im primären Videostream identisch sein, ebenso wie progressiver Inhalt.</span><span class="sxs-lookup"><span data-stu-id="08243-255">On the first output frame, the presentation time must equal the start time of the current picture in the primary video stream, just like progressive content.</span></span> <span data-ttu-id="08243-256">Im zweiten Ausgabe Frame muss die Startzeit der Mitte zwischen der Startzeit des aktuellen Bilds im primären Videostream und der Startzeit des nächsten Bilds im Stream entsprechen.</span><span class="sxs-lookup"><span data-stu-id="08243-256">On the second output frame, the start time must equal the midpoint between the start time of the current picture in the primary video stream and the start time of the next picture in the stream.</span></span> <span data-ttu-id="08243-257">Wenn das Eingabe Video z. b. 25 Frames pro Sekunde (50 Felder pro Sekunde) ist, haben die Ausgabe Rahmen die in der folgenden Tabelle angezeigten Zeitstempel.</span><span class="sxs-lookup"><span data-stu-id="08243-257">For example, if the input video is 25 frames per second (50 fields per second), the output frames will have the time stamps shown in the following table.</span></span> <span data-ttu-id="08243-258">Zeitstempel werden in Einheiten von 100 Nanosekunden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="08243-258">Time stamps are shown in units of 100 nanoseconds.</span></span>

    

    | <span data-ttu-id="08243-259">Eingabebild</span><span class="sxs-lookup"><span data-stu-id="08243-259">Input picture</span></span> | <span data-ttu-id="08243-260">**TargetFrame** (1)</span><span class="sxs-lookup"><span data-stu-id="08243-260">**TargetFrame** (1)</span></span> | <span data-ttu-id="08243-261">**TargetFrame** (2)</span><span class="sxs-lookup"><span data-stu-id="08243-261">**TargetFrame** (2)</span></span> |
    |---------------|---------------------|---------------------|
    | <span data-ttu-id="08243-262">0</span><span class="sxs-lookup"><span data-stu-id="08243-262">0</span></span>             | <span data-ttu-id="08243-263">0</span><span class="sxs-lookup"><span data-stu-id="08243-263">0</span></span>                   | <span data-ttu-id="08243-264">200.000</span><span class="sxs-lookup"><span data-stu-id="08243-264">200000</span></span>              |
    | <span data-ttu-id="08243-265">400000</span><span class="sxs-lookup"><span data-stu-id="08243-265">400000</span></span>        | <span data-ttu-id="08243-266">0</span><span class="sxs-lookup"><span data-stu-id="08243-266">0</span></span>                   | <span data-ttu-id="08243-267">600000</span><span class="sxs-lookup"><span data-stu-id="08243-267">600000</span></span>              |
    | <span data-ttu-id="08243-268">800000</span><span class="sxs-lookup"><span data-stu-id="08243-268">800000</span></span>        | <span data-ttu-id="08243-269">800000</span><span class="sxs-lookup"><span data-stu-id="08243-269">800000</span></span>              | <span data-ttu-id="08243-270">1000000</span><span class="sxs-lookup"><span data-stu-id="08243-270">1000000</span></span>             |
    | <span data-ttu-id="08243-271">1,2 Millionen</span><span class="sxs-lookup"><span data-stu-id="08243-271">1200000</span></span>       | <span data-ttu-id="08243-272">1,2 Millionen</span><span class="sxs-lookup"><span data-stu-id="08243-272">1200000</span></span>             | <span data-ttu-id="08243-273">1,4 Millionen</span><span class="sxs-lookup"><span data-stu-id="08243-273">1400000</span></span>             |

    

     

    <span data-ttu-id="08243-274">Wenn der Zeilen Sprung Inhalt aus einzelnen Feldern anstelle von verschachtelten Feldern besteht, entsprechen die Ausgabe Zeiten immer den Eingabe Zeiten, wie bei progressivem Inhalt.</span><span class="sxs-lookup"><span data-stu-id="08243-274">If interlaced content consists of single fields rather than interleaved fields, the output times always match the input times, as with progressive content.</span></span>

-   <span data-ttu-id="08243-275">**Targetrect** definiert einen rechteckigen Bereich innerhalb der Ziel Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="08243-275">**TargetRect** defines a rectangular region within the destination surface.</span></span> <span data-ttu-id="08243-276">Die Ausgabe wird von Blit in diese Region geschrieben.</span><span class="sxs-lookup"><span data-stu-id="08243-276">The blit will write the output to this region.</span></span> <span data-ttu-id="08243-277">Insbesondere wird jedes Pixel innerhalb von **targetrect** geändert, und es werden keine Pixel außerhalb von **targetrect** geändert.</span><span class="sxs-lookup"><span data-stu-id="08243-277">Specifically, every pixel inside **TargetRect** will be modified, and no pixels outside of **TargetRect** will be modified.</span></span> <span data-ttu-id="08243-278">Das Ziel Rechteck definiert das Begrenzungs Rechteck für alle eingabevideostreams.</span><span class="sxs-lookup"><span data-stu-id="08243-278">The target rectangle defines the bounding rectangle for all of the input video streams.</span></span> <span data-ttu-id="08243-279">Die Platzierung einzelner Streams innerhalb dieses Rechtecks wird über den *psamples* -Parameter von [**idirectxvideoprocessor:: videoprocessblt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt)gesteuert.</span><span class="sxs-lookup"><span data-stu-id="08243-279">Placement of individual streams within that rectangle is controlled through the *pSamples* parameter of [**IDirectXVideoProcessor::VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt).</span></span>
-   <span data-ttu-id="08243-280">**BackgroundColor** gibt die Hintergrundfarbe an, wo kein Video Bild angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="08243-280">**BackgroundColor** gives the color of the background wherever no video image appears.</span></span> <span data-ttu-id="08243-281">Wenn z. b. ein Video mit einer Größe von 16 x 9 in einem 4 x 3-Bereich (Letterboxing) angezeigt wird, werden die in einem Briefkasten enthaltenen Bereiche mit der Hintergrundfarbe angezeigt.</span><span class="sxs-lookup"><span data-stu-id="08243-281">For example, when a 16 x 9 video image is displayed within a 4 x 3 area (letterboxing), the letterboxed regions are displayed with the background color.</span></span> <span data-ttu-id="08243-282">Die Hintergrundfarbe ist nur innerhalb des Ziel Rechtecks (**targetrect**) anwendbar.</span><span class="sxs-lookup"><span data-stu-id="08243-282">The background color applies only within the target rectangle (**TargetRect**).</span></span> <span data-ttu-id="08243-283">Alle Pixel außerhalb von **targetrect** werden nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="08243-283">Any pixels outside of **TargetRect** are not modified.</span></span>
-   <span data-ttu-id="08243-284">**Destformat** beschreibt den Farbraum für das Ausgabevideo – beispielsweise, ob die Farbe "ITU-R BT. 709" oder "BT. 601" verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="08243-284">**DestFormat** describes the color space for the output video—for example, whether ITU-R BT.709 or BT.601 color is used.</span></span> <span data-ttu-id="08243-285">Diese Informationen können sich darauf auswirken, wie das Bild angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="08243-285">This information can affect how the image is displayed.</span></span> <span data-ttu-id="08243-286">Weitere Informationen finden Sie unter [Erweiterte Farbinformationen](extended-color-information.md).</span><span class="sxs-lookup"><span data-stu-id="08243-286">For more information, see [Extended Color Information](extended-color-information.md).</span></span>

<span data-ttu-id="08243-287">Andere Parameter werden auf der Referenzseite für die [**DXVA2 \_ videoprocess bltparameams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) -Struktur beschrieben.</span><span class="sxs-lookup"><span data-stu-id="08243-287">Other parameters are described on the reference page for the [**DXVA2\_VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) structure.</span></span>

### <a name="input-samples"></a><span data-ttu-id="08243-288">Eingabe Beispiele</span><span class="sxs-lookup"><span data-stu-id="08243-288">Input Samples</span></span>

<span data-ttu-id="08243-289">Der *psamples* -Parameter von [**idirectxvideoprocessor:: videoprocessblt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) verweist auf ein Array von [**DXVA2 \_ Videosample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="08243-289">The *pSamples* parameter of [**IDirectXVideoProcessor::VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) points to an array of [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structures.</span></span> <span data-ttu-id="08243-290">Jede dieser Strukturen enthält Informationen zu einem Eingabe Beispiel und einen Zeiger auf die Direct3D-Oberfläche, die das Beispiel enthält.</span><span class="sxs-lookup"><span data-stu-id="08243-290">Each of these structures contains information about one input sample and a pointer to the Direct3D surface that contains the sample.</span></span> <span data-ttu-id="08243-291">Jedes Beispiel ist einer der folgenden:</span><span class="sxs-lookup"><span data-stu-id="08243-291">Each sample is one of the following:</span></span>

-   <span data-ttu-id="08243-292">Das aktuelle Bild aus dem primären Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="08243-292">The current picture from the primary stream.</span></span>
-   <span data-ttu-id="08243-293">Ein vorwärts-oder rückwärts Verweis Bild aus dem primären Stream, das für Deinterlacing verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="08243-293">A forward or backward reference picture from the primary stream, used for deinterlacing.</span></span>
-   <span data-ttu-id="08243-294">Ein substreambild.</span><span class="sxs-lookup"><span data-stu-id="08243-294">A substream picture.</span></span>

<span data-ttu-id="08243-295">Die genaue Reihenfolge, in der die Stichproben im Array angezeigt werden müssen, wird später im Abschnitt [Eingabe Stichprobe-Reihenfolge](#input-sample-order)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="08243-295">The exact order in which the samples must appear in the array is described later, in the section [Input Sample Order](#input-sample-order).</span></span>

<span data-ttu-id="08243-296">Es können bis zu 15 substreambilder bereitgestellt werden, obwohl die meisten Videoanwendungen höchstens einen teilstream benötigen.</span><span class="sxs-lookup"><span data-stu-id="08243-296">Up to 15 substream pictures can be provided, although most video applications need only one substream, at the most.</span></span> <span data-ttu-id="08243-297">Die Anzahl der untergeordneten Datenströme kann bei jedem Aufrufen von [**videoprocess BLT**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt)geändert werden.</span><span class="sxs-lookup"><span data-stu-id="08243-297">The number of substreams can change with each call to [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt).</span></span> <span data-ttu-id="08243-298">Substreambilder werden angezeigt, indem das **Sampleformat. Sampleformat** -Member der [**DXVA2 \_ Videosample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) -Struktur auf DXVA2 \_ samplesubstream festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="08243-298">Substream pictures are indicated by setting the **SampleFormat.SampleFormat** member of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure equal to DXVA2\_SampleSubStream.</span></span> <span data-ttu-id="08243-299">Für den primären Videostream beschreibt dieser Member das Zeilen Sprung des Eingabe Videos.</span><span class="sxs-lookup"><span data-stu-id="08243-299">For the primary video stream, this member describes the interlacing of the input video.</span></span> <span data-ttu-id="08243-300">Weitere Informationen finden Sie unter [**DXVA2 \_ Sampleformat**](/windows/desktop/api/dxva2api/ne-dxva2api-dxva2_sampleformat) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="08243-300">For more information, see [**DXVA2\_SampleFormat**](/windows/desktop/api/dxva2api/ne-dxva2api-dxva2_sampleformat) enumeration.</span></span>

<span data-ttu-id="08243-301">Für den primären Videostream geben die **Start** -und **Endelemente** der [**DXVA2 \_ Videosample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) -Struktur die Start-und Endzeiten der Eingabe Stichprobe an.</span><span class="sxs-lookup"><span data-stu-id="08243-301">For the primary video stream, the **Start** and **End** members of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure give the start and end times of the input sample.</span></span> <span data-ttu-id="08243-302">Legen Sie für substreambilder diese Werte auf 0 (null) fest, da die Präsentationszeit immer aus dem primären Stream berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="08243-302">For substream pictures, set these values to zero, because the presentation time is always calculated from the primary stream.</span></span> <span data-ttu-id="08243-303">Die Anwendung ist für die Nachverfolgung zuständig, wenn jedes subnetzbild präsentiert und zum richtigen Zeitpunkt an [**videoprocstinblt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) übermittelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="08243-303">The application is responsible for tracking when each substream picture should be presented and submitting it to [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) at the proper time.</span></span>

<span data-ttu-id="08243-304">Zwei Rechtecke definieren, wie das Quellvideo für jeden Stream positioniert wird:</span><span class="sxs-lookup"><span data-stu-id="08243-304">Two rectangles define how the source video is positioned for each stream:</span></span>

-   <span data-ttu-id="08243-305">Der **srcRect** -Member der [**DXVA2 \_ Videosample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) -Struktur gibt das *Quell Rechteck* an, einem rechteckigen Bereich des Quell Bilds, der im zusammengesetzten Ausgabe Rahmen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="08243-305">The **SrcRect** member of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure specifies the *source rectangle*, a rectangular region of the source picture that will appear in the composited output frame.</span></span> <span data-ttu-id="08243-306">Legen Sie diese Einstellung auf einen Wert fest, der kleiner als die Frame Größe ist, um das Bild zu zuschneiden</span><span class="sxs-lookup"><span data-stu-id="08243-306">To crop the picture, set this to a value smaller than the frame size.</span></span> <span data-ttu-id="08243-307">Legen Sie andernfalls die Größe der Frame Größe fest.</span><span class="sxs-lookup"><span data-stu-id="08243-307">Otherwise, set it equal to the frame size.</span></span>
-   <span data-ttu-id="08243-308">Der **dstrect** -Member der gleichen Struktur gibt das *Ziel Rechteck* an, einen rechteckigen Bereich der Ziel Oberfläche, auf dem der Videoframe angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="08243-308">The **DstRect** member of the same structure specifies the *destination rectangle*, a rectangular region of the destination surface where the video frame will appear.</span></span>

<span data-ttu-id="08243-309">Der Treiber blitet Pixel aus dem Quell Rechteck in das Ziel Rechteck.</span><span class="sxs-lookup"><span data-stu-id="08243-309">The driver blits pixels from the source rectangle into the destination rectangle.</span></span> <span data-ttu-id="08243-310">Die zwei Rechtecke können unterschiedliche Größen oder Seitenverhältnisse aufweisen. der Treiber skaliert das Image nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="08243-310">The two rectangles can have different sizes or aspect ratios; the driver will scale the image as needed.</span></span> <span data-ttu-id="08243-311">Außerdem kann jeder Eingabedaten Strom einen anderen Skalierungsfaktor verwenden.</span><span class="sxs-lookup"><span data-stu-id="08243-311">Moreover, each input stream can use a different scaling factor.</span></span> <span data-ttu-id="08243-312">Tatsächlich kann eine Skalierung erforderlich sein, um das richtige Seitenverhältnis im Ausgabe Rahmen zu schaffen.</span><span class="sxs-lookup"><span data-stu-id="08243-312">In fact, scaling might be necessary to produce the correct aspect ratio in the output frame.</span></span> <span data-ttu-id="08243-313">Der Treiber übernimmt nicht das Pixel Seitenverhältnis der Quelle. wenn das Quell Image also nicht quadratische Pixel verwendet, liegt es an der Anwendung, das richtige Ziel Rechteck zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="08243-313">The driver does not take the source's pixel aspect ratio into account, so if the source image uses non-square pixels, it is up to the application to calculate the correct destination rectangle.</span></span>

<span data-ttu-id="08243-314">Die bevorzugten substreamformate sind ayuv und AI44.</span><span class="sxs-lookup"><span data-stu-id="08243-314">The preferred substream formats are AYUV and AI44.</span></span> <span data-ttu-id="08243-315">Letzteres ist ein Palettenformat mit 16 Farben.</span><span class="sxs-lookup"><span data-stu-id="08243-315">The latter is a palletized format with 16 colors.</span></span> <span data-ttu-id="08243-316">Paletteneinträge werden im **PAL** -Member der [**DXVA2 \_ Videosample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) -Struktur angegeben.</span><span class="sxs-lookup"><span data-stu-id="08243-316">Palette entries are specified in the **Pal** member of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure.</span></span> <span data-ttu-id="08243-317">(Wenn das Quellvideo Format ursprünglich als Media Foundation Medientyp ausgedrückt wird, werden die Paletteneinträge im [**MF \_ MT- \_ palettenattribut**](mf-mt-palette-attribute.md) gespeichert.) Deaktivieren Sie dieses Array bei nicht-palettenformaten auf 0 (null).</span><span class="sxs-lookup"><span data-stu-id="08243-317">(If your source video format is originally expressed as a Media Foundation media type, the palette entries are stored in the [**MF\_MT\_PALETTE**](mf-mt-palette-attribute.md) attribute.) For non-palletized formats, clear this array to zero.</span></span>

## <a name="image-composition"></a><span data-ttu-id="08243-318">Bildkomposition</span><span class="sxs-lookup"><span data-stu-id="08243-318">Image Composition</span></span>

<span data-ttu-id="08243-319">Jeder Blit-Vorgang wird durch die folgenden drei Rechtecke definiert:</span><span class="sxs-lookup"><span data-stu-id="08243-319">Every blit operation is defined by the following three rectangles:</span></span>

-   <span data-ttu-id="08243-320">Das *Ziel* Rechteck (**targetrect**) definiert den Bereich innerhalb der Ziel Oberfläche, in dem die Ausgabe angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="08243-320">The *target* rectangle (**TargetRect**) defines the region within the destination surface where the output will appear.</span></span> <span data-ttu-id="08243-321">Das Ausgabe Bild wird auf dieses Rechteck zugeschnitten.</span><span class="sxs-lookup"><span data-stu-id="08243-321">The output image is clipped to this rectangle.</span></span>
-   <span data-ttu-id="08243-322">Das *Ziel* Rechteck für jeden Datenstrom (**dstrect**) definiert, wo der Eingabestream im zusammengesetzten Image angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="08243-322">The *destination* rectangle for each stream (**DstRect**) defines where the input stream appears in the composited image.</span></span>
-   <span data-ttu-id="08243-323">Das *Quell* Rechteck für jeden Stream (**srcRect**) definiert, welcher Teil des Quell Bilds angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="08243-323">The *source* rectangle for each stream (**SrcRect**) defines which part of the source image appears.</span></span>

<span data-ttu-id="08243-324">Die Ziel-und Ziel Rechtecke werden relativ zur Ziel Oberfläche angegeben.</span><span class="sxs-lookup"><span data-stu-id="08243-324">The target and destination rectangles are specified relative to the destination surface.</span></span> <span data-ttu-id="08243-325">Das Quell Rechteck wird relativ zum Quell Abbild angegeben.</span><span class="sxs-lookup"><span data-stu-id="08243-325">The source rectangle is specified relative to the source image.</span></span> <span data-ttu-id="08243-326">Alle Rechtecke werden in Pixel angegeben.</span><span class="sxs-lookup"><span data-stu-id="08243-326">All rectangles are specified in pixels.</span></span>

![Diagramm, das Quell-, Ziel-und Ziel Rechtecke anzeigt](images/dxva-vp-rects.gif)

<span data-ttu-id="08243-328">Der Video Verarbeitungs Gerät Alpha kombiniert die Eingabe Bilder und verwendet dabei eine der folgenden Quellen für Alpha Daten:</span><span class="sxs-lookup"><span data-stu-id="08243-328">The video processing device alpha blends the input pictures, using any of the following sources of alpha data:</span></span>

-   <span data-ttu-id="08243-329">Pro-Pixel-Alpha Daten aus untergeordneten Datenströmen.</span><span class="sxs-lookup"><span data-stu-id="08243-329">Per-pixel alpha data from substreams.</span></span>
-   <span data-ttu-id="08243-330">Ein planarer Alpha Wert für jeden Videostream, der im **planaralpha** -Member der [**DXVA2 \_ Videosample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) -Struktur angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="08243-330">A planar alpha value for each video stream, specified in the **PlanarAlpha** member of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure.</span></span>
-   <span data-ttu-id="08243-331">Der planare Alpha Wert des zusammengesetzten Bilds, das im **Alpha** -Member der [**DXVA2 \_ videoprocess bltparameams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) -Struktur angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="08243-331">The planar alpha value of the composited image, specified in the **Alpha** member of the [**DXVA2\_VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) structure.</span></span> <span data-ttu-id="08243-332">Dieser Wert wird verwendet, um das gesamte zusammengesetzte Bild mit der Hintergrundfarbe zu kombinieren.</span><span class="sxs-lookup"><span data-stu-id="08243-332">This value is used to blend the entire composited image with the background color.</span></span>

<span data-ttu-id="08243-333">Dieser Abschnitt enthält eine Reihe von Beispielen, die zeigen, wie das Video Verarbeitungs Gerät das Ausgabe Image erstellt.</span><span class="sxs-lookup"><span data-stu-id="08243-333">This section gives a series of examples that show how the video processing device creates the output image.</span></span>

### <a name="example-1-letterboxing"></a><span data-ttu-id="08243-334">Beispiel 1: Briefkasten</span><span class="sxs-lookup"><span data-stu-id="08243-334">Example 1: Letterboxing</span></span>

<span data-ttu-id="08243-335">In diesem Beispiel wird gezeigt, wie das Quell Abbild durch das Ziel Rechteck als kleiner als das Ziel Rechteck festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="08243-335">This example shows how to letterbox the source image, by setting the destination rectangle to be smaller than the target rectangle.</span></span> <span data-ttu-id="08243-336">Der primäre Videostream in diesem Beispiel ist ein 720 × 480-Bild, das mit einem 16:9-Seitenverhältnis angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="08243-336">The primary video stream in this example is a 720 × 480 image, and is meant to be displayed at a 16:9 aspect ratio.</span></span> <span data-ttu-id="08243-337">Die Ziel Oberfläche ist 640 × 480 Pixel (4:3 Seitenverhältnis).</span><span class="sxs-lookup"><span data-stu-id="08243-337">The destination surface is 640 × 480 pixels (4:3 aspect ratio).</span></span> <span data-ttu-id="08243-338">Um das richtige Seitenverhältnis zu erreichen, muss das Ziel Rechteck 640 × 360 sein.</span><span class="sxs-lookup"><span data-stu-id="08243-338">To achieve the correct aspect ratio, the destination rectangle must be 640 × 360.</span></span> <span data-ttu-id="08243-339">Der Einfachheit halber enthält dieses Beispiel keinen substream.</span><span class="sxs-lookup"><span data-stu-id="08243-339">For simplicity, this example does not include a substream.</span></span> <span data-ttu-id="08243-340">Das folgende Diagramm zeigt die Quell-und Ziel Rechtecke.</span><span class="sxs-lookup"><span data-stu-id="08243-340">The following diagram shows the source and destination rectangles.</span></span>

![Diagramm, das Letterboxing anzeigt.](images/428105fa-a26b-48a6-991d-44d24ab786b1.gif)

<span data-ttu-id="08243-342">Das vorangehende Diagramm zeigt die folgenden Rechtecke:</span><span class="sxs-lookup"><span data-stu-id="08243-342">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="08243-343">Ziel Rechteck: {0, 0, 640, 480}</span><span class="sxs-lookup"><span data-stu-id="08243-343">Target rectangle: { 0, 0, 640, 480 }</span></span>
-   <span data-ttu-id="08243-344">Primäres Video:</span><span class="sxs-lookup"><span data-stu-id="08243-344">Primary video:</span></span>

    -   <span data-ttu-id="08243-345">Quell Rechteck: {0, 0, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="08243-345">Source rectangle: { 0, 0, 720, 480 }</span></span>
    -   <span data-ttu-id="08243-346">Ziel Rechteck: {0, 60, 640, 420}</span><span class="sxs-lookup"><span data-stu-id="08243-346">Destination rectangle: { 0, 60, 640, 420 }</span></span>

<span data-ttu-id="08243-347">Der Treiber deinstalhnt das Video, verkleinert den deinterllingframe auf 640 × 360 und Blit den Frame in das Ziel Rechteck.</span><span class="sxs-lookup"><span data-stu-id="08243-347">The driver will deinterlace the video, shrink the deinterlaced frame to 640 × 360, and blit the frame into the destination rectangle.</span></span> <span data-ttu-id="08243-348">Das Ziel Rechteck ist größer als das Ziel Rechteck, daher verwendet der Treiber die Hintergrundfarbe, um die horizontalen Balken oberhalb und unterhalb des Rahmens zu füllen.</span><span class="sxs-lookup"><span data-stu-id="08243-348">The target rectangle is larger than the destination rectangle, so the driver will use the background color to fill the horizontal bars above and below the frame.</span></span> <span data-ttu-id="08243-349">Die Hintergrundfarbe wird in der [**DXVA2 \_ videoprocess bltparameams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) -Struktur angegeben.</span><span class="sxs-lookup"><span data-stu-id="08243-349">The background color is specified in the [**DXVA2\_VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) structure.</span></span>

### <a name="example-2-stretching-substream-images"></a><span data-ttu-id="08243-350">Beispiel 2: Stretching von substreamimages</span><span class="sxs-lookup"><span data-stu-id="08243-350">Example 2: Stretching Substream Images</span></span>

<span data-ttu-id="08243-351">Substreambilder können über das primäre Video Bild hinaus erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="08243-351">Substream pictures can extend beyond the primary video picture.</span></span> <span data-ttu-id="08243-352">In DVD-Videos kann der primäre Videostream z. b. ein 4:3-Seitenverhältnis aufweisen, während der unter Datenstrom 16:9 ist.</span><span class="sxs-lookup"><span data-stu-id="08243-352">In DVD video, for example, the primary video stream can have a 4:3 aspect ratio while the substream is 16:9.</span></span> <span data-ttu-id="08243-353">In diesem Beispiel verfügen beide Videostreams über die gleichen Quell Dimensionen (720 × 480), der unter Datenstrom sollte jedoch mit einem 16:9-Seitenverhältnis angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="08243-353">In this example, both video streams have the same source dimensions (720 × 480), but the substream is intended to be shown at a 16:9 aspect ratio.</span></span> <span data-ttu-id="08243-354">Um dieses Seitenverhältnis zu erreichen, wird das substreambild horizontal gestreckt.</span><span class="sxs-lookup"><span data-stu-id="08243-354">To achieve this aspect ratio, the substream image is stretched horizontally.</span></span> <span data-ttu-id="08243-355">Die Quell-und Ziel Rechtecke werden im folgenden Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="08243-355">The source and destination rectangles are shown in the following diagram.</span></span>

![Diagramm, das die Bild Streckung des Substreams anzeigt.](images/7ab31c65-06b9-4843-90b8-2f9fb6f6b20e.gif)

<span data-ttu-id="08243-357">Das vorangehende Diagramm zeigt die folgenden Rechtecke:</span><span class="sxs-lookup"><span data-stu-id="08243-357">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="08243-358">Ziel Rechteck: {0, 0, 854, 480}</span><span class="sxs-lookup"><span data-stu-id="08243-358">Target rectangle: { 0, 0, 854, 480 }</span></span>
-   <span data-ttu-id="08243-359">Primäres Video:</span><span class="sxs-lookup"><span data-stu-id="08243-359">Primary video:</span></span>

    -   <span data-ttu-id="08243-360">Quell Rechteck: {0, 0, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="08243-360">Source rectangle: { 0, 0, 720, 480 }</span></span>
    -   <span data-ttu-id="08243-361">Ziel Rechteck: {0, 107, 474, 480}</span><span class="sxs-lookup"><span data-stu-id="08243-361">Destination rectangle: { 0, 107, 474, 480 }</span></span>

-   <span data-ttu-id="08243-362">Unter Datenstrom</span><span class="sxs-lookup"><span data-stu-id="08243-362">Substream:</span></span>
    -   <span data-ttu-id="08243-363">Quell Rechteck: {0, 0, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="08243-363">Source rectangle: { 0, 0, 720, 480 }</span></span>
    -   <span data-ttu-id="08243-364">Ziel Rechteck: {0, 0, 854, 480}</span><span class="sxs-lookup"><span data-stu-id="08243-364">Destination rectangle: { 0, 0, 854, 480 }</span></span>

<span data-ttu-id="08243-365">Diese Werte behalten die Bildhöhe bei und Skalieren beide Bilder horizontal.</span><span class="sxs-lookup"><span data-stu-id="08243-365">These values preserve the image height and scale both images horizontally.</span></span> <span data-ttu-id="08243-366">In den Regionen, in denen beide Bilder angezeigt werden, sind Sie Alpha gemischt.</span><span class="sxs-lookup"><span data-stu-id="08243-366">In the regions where both images appear, they are alpha blended.</span></span> <span data-ttu-id="08243-367">Wenn das substreambild über das primay-Video hinausgeht, wird der unter Datenstrom mit der Hintergrundfarbe mit Alpha gemischt.</span><span class="sxs-lookup"><span data-stu-id="08243-367">Where the substream picture exends beyond the primay video, the substream is alpha blended with the background color.</span></span> <span data-ttu-id="08243-368">Mit diesem Alpha werden die Konten für die geänderten Farben auf der rechten Seite des Diagramms gemischt.</span><span class="sxs-lookup"><span data-stu-id="08243-368">This alpha blending accounts for the altered colors in the right-hand side of the diagram.</span></span>

### <a name="example-3-mismatched-stream-heights"></a><span data-ttu-id="08243-369">Beispiel 3: nicht übereinstimmende streamhöhen</span><span class="sxs-lookup"><span data-stu-id="08243-369">Example 3: Mismatched Stream Heights</span></span>

<span data-ttu-id="08243-370">Im vorherigen Beispiel weisen der unter Datenstrom und der primäre Stream dieselbe Höhe auf.</span><span class="sxs-lookup"><span data-stu-id="08243-370">In the previous example, the substream and the primary stream are the same height.</span></span> <span data-ttu-id="08243-371">Streams können auch eine nicht übereinstimmende Höhe aufweisen, wie in diesem Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="08243-371">Streams can also have mismatched heights, as shown in this example.</span></span> <span data-ttu-id="08243-372">Bereiche innerhalb des Ziel Rechtecks, in denen kein Video angezeigt wird, werden mit der Hintergrundfarbe gezeichnet – schwarz in diesem Beispiel.</span><span class="sxs-lookup"><span data-stu-id="08243-372">Areas within the target rectangle where no video appears are drawn using the background color—black in this example.</span></span> <span data-ttu-id="08243-373">Die Quell-und Ziel Rechtecke werden im folgenden Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="08243-373">The source and destination rectangles are shown in the following diagram.</span></span>

![Diagramm mit nicht übereinstimmenden streamhöhen,](images/0190a15a-d971-450f-90ed-ce5633e1069c.gif)

<span data-ttu-id="08243-375">Das vorangehende Diagramm zeigt die folgenden Rechtecke:</span><span class="sxs-lookup"><span data-stu-id="08243-375">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="08243-376">Ziel Rechteck: {0, 0, 150, 85}</span><span class="sxs-lookup"><span data-stu-id="08243-376">Target rectangle: { 0, 0, 150, 85 }</span></span>
-   <span data-ttu-id="08243-377">Primäres Video:</span><span class="sxs-lookup"><span data-stu-id="08243-377">Primary video:</span></span>
    -   <span data-ttu-id="08243-378">Quell Rechteck: {0, 0, 150, 50}</span><span class="sxs-lookup"><span data-stu-id="08243-378">Source rectangle: { 0, 0, 150, 50 }</span></span>
    -   <span data-ttu-id="08243-379">Ziel Rechteck: {0,0, 150, 67}</span><span class="sxs-lookup"><span data-stu-id="08243-379">Destination rectangle: { 0, 17, 150, 67 }</span></span>
-   <span data-ttu-id="08243-380">Unter Datenstrom</span><span class="sxs-lookup"><span data-stu-id="08243-380">Substream:</span></span>
    -   <span data-ttu-id="08243-381">Quell Rechteck: {0, 0, 100, 85}</span><span class="sxs-lookup"><span data-stu-id="08243-381">Source rectangle: { 0, 0, 100, 85 }</span></span>
    -   <span data-ttu-id="08243-382">Ziel Rechteck: {25, 0, 125, 85}</span><span class="sxs-lookup"><span data-stu-id="08243-382">Destination rectangle: { 25, 0, 125, 85 }</span></span>

### <a name="example-4-target-rectangle-smaller-than-destination-surface"></a><span data-ttu-id="08243-383">Beispiel 4: Ziel Rechteck kleiner als Ziel Oberfläche</span><span class="sxs-lookup"><span data-stu-id="08243-383">Example 4: Target Rectangle Smaller Than Destination Surface</span></span>

<span data-ttu-id="08243-384">Dieses Beispiel zeigt einen Fall, bei dem das Ziel Rechteck kleiner als die Ziel Oberfläche ist.</span><span class="sxs-lookup"><span data-stu-id="08243-384">This example shows a case where the target rectangle is smaller than the destination surface.</span></span>

![Diagramm, das einen Blit zu einem Ziel Rechteck anzeigt.](images/360a85a3-333c-4b32-b8f7-1beb1e805921.gif)

<span data-ttu-id="08243-386">Das vorangehende Diagramm zeigt die folgenden Rechtecke:</span><span class="sxs-lookup"><span data-stu-id="08243-386">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="08243-387">Ziel Oberfläche: {0, 0, 300, 200}</span><span class="sxs-lookup"><span data-stu-id="08243-387">Destination surface: { 0, 0, 300, 200 }</span></span>
-   <span data-ttu-id="08243-388">Ziel Rechteck: {0, 0, 150, 85}</span><span class="sxs-lookup"><span data-stu-id="08243-388">Target rectangle: { 0, 0, 150, 85 }</span></span>
-   <span data-ttu-id="08243-389">Primäres Video:</span><span class="sxs-lookup"><span data-stu-id="08243-389">Primary video:</span></span>
    -   <span data-ttu-id="08243-390">Quell Rechteck: {0, 0, 150, 50}</span><span class="sxs-lookup"><span data-stu-id="08243-390">Source rectangle: { 0, 0, 150, 50 }</span></span>
    -   <span data-ttu-id="08243-391">Ziel Rechteck: {0,0, 150, 67}</span><span class="sxs-lookup"><span data-stu-id="08243-391">Destination rectangle: { 0, 17, 150, 67 }</span></span>
-   <span data-ttu-id="08243-392">Unter Datenstrom</span><span class="sxs-lookup"><span data-stu-id="08243-392">Substream:</span></span>
    -   <span data-ttu-id="08243-393">Quell Rechteck: {0, 0, 100, 85}</span><span class="sxs-lookup"><span data-stu-id="08243-393">Source rectangle: { 0, 0, 100, 85 }</span></span>
    -   <span data-ttu-id="08243-394">Ziel Rechteck: {25, 0, 125, 85}</span><span class="sxs-lookup"><span data-stu-id="08243-394">Destination rectangle: { 25, 0, 125, 85 }</span></span>

<span data-ttu-id="08243-395">Pixel außerhalb des Ziel Rechtecks werden nicht geändert, sodass die Hintergrundfarbe nur innerhalb des Ziel Rechtecks angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="08243-395">Pixels outside of the target rectangle are not modified, so the background color appears only within the target rectangle.</span></span> <span data-ttu-id="08243-396">Der gepunktete Bereich gibt Teile der Ziel Oberfläche an, die vom Blit nicht betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="08243-396">The dotted area indicates portions of the destination surface that are not affected by the blit.</span></span>

### <a name="example-5-source-rectangles"></a><span data-ttu-id="08243-397">Beispiel 5: Quell Rechtecke</span><span class="sxs-lookup"><span data-stu-id="08243-397">Example 5: Source Rectangles</span></span>

<span data-ttu-id="08243-398">Wenn Sie ein Quell Rechteck angeben, das kleiner als das Quellbild ist, wird der Treiber nur diesen Teil des Bilds blitten.</span><span class="sxs-lookup"><span data-stu-id="08243-398">If you specify a source rectangle that is smaller than the source picture, the driver will blit just that portion of the picture.</span></span> <span data-ttu-id="08243-399">In diesem Beispiel geben die Quell Rechtecke den unteren rechten Quadranten des primären Videodaten Stroms und den unteren linken Quadranten des Substreams an (angegeben durch Hash Zeichen im Diagramm).</span><span class="sxs-lookup"><span data-stu-id="08243-399">In this example, the source rectangles specify the lower-right quadrant of the primary video stream and the lower-left quadrant of the substream (indicated by hash marks in the diagram).</span></span> <span data-ttu-id="08243-400">Die Ziel Rechtecke sind identisch mit den Quell Rechtecke, sodass das Video nicht gestreckt wird.</span><span class="sxs-lookup"><span data-stu-id="08243-400">The destination rectangles are the same sizes as the source rectangles, so the video is not stretched.</span></span> <span data-ttu-id="08243-401">Die Quell-und Ziel Rechtecke werden im folgenden Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="08243-401">The source and destination rectangles are shown in the following diagram.</span></span>

![Diagramm, das einen Blit aus zwei Quell Rechtecke anzeigt.](images/b1de4cc3-0155-40be-acac-b486e2af8c0d.gif)

<span data-ttu-id="08243-403">Das vorangehende Diagramm zeigt die folgenden Rechtecke:</span><span class="sxs-lookup"><span data-stu-id="08243-403">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="08243-404">Ziel Rechteck: {0, 0, 720, 576}</span><span class="sxs-lookup"><span data-stu-id="08243-404">Target rectangle: { 0, 0, 720, 576 }</span></span>
-   <span data-ttu-id="08243-405">Primäres Video:</span><span class="sxs-lookup"><span data-stu-id="08243-405">Primary video:</span></span>
    -   <span data-ttu-id="08243-406">Quell Oberflächen Größe: {0, 0, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="08243-406">Source surface size: { 0, 0, 720, 480 }</span></span>
    -   <span data-ttu-id="08243-407">Quell Rechteck: {360, 240, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="08243-407">Source rectangle: { 360, 240, 720, 480 }</span></span>
    -   <span data-ttu-id="08243-408">Ziel Rechteck: {0, 0, 360, 240}</span><span class="sxs-lookup"><span data-stu-id="08243-408">Destination rectangle: { 0, 0, 360, 240 }</span></span>
-   <span data-ttu-id="08243-409">Unter Datenstrom</span><span class="sxs-lookup"><span data-stu-id="08243-409">Substream:</span></span>
    -   <span data-ttu-id="08243-410">Quell Oberflächen Größe: {0, 0, 640, 576}</span><span class="sxs-lookup"><span data-stu-id="08243-410">Source surface size: { 0, 0, 640, 576 }</span></span>
    -   <span data-ttu-id="08243-411">Quell Rechteck: {0, 288, 320, 576}</span><span class="sxs-lookup"><span data-stu-id="08243-411">Source rectangle: { 0, 288, 320, 576 }</span></span>
    -   <span data-ttu-id="08243-412">Ziel Rechteck: {400, 0, 720, 288}</span><span class="sxs-lookup"><span data-stu-id="08243-412">Destination rectangle: { 400, 0, 720, 288 }</span></span>

### <a name="example-6-intersecting-destination-rectangles"></a><span data-ttu-id="08243-413">Beispiel 6: überschneidende Ziel Rechtecke</span><span class="sxs-lookup"><span data-stu-id="08243-413">Example 6: Intersecting Destination Rectangles</span></span>

<span data-ttu-id="08243-414">Dieses Beispiel ähnelt dem vorherigen, aber die Ziel Rechtecke überschneiden sich.</span><span class="sxs-lookup"><span data-stu-id="08243-414">This example is similar to previous one, but the destination rectangles intersect.</span></span> <span data-ttu-id="08243-415">Die Oberflächen Dimensionen sind identisch mit denen im vorherigen Beispiel, die Quell-und Ziel Rechtecke hingegen nicht.</span><span class="sxs-lookup"><span data-stu-id="08243-415">The surface dimensions are the same as in the previous example, but the source and destination rectangles are not.</span></span> <span data-ttu-id="08243-416">Auch hier wird das Video beschnitten, aber nicht gestreckt.</span><span class="sxs-lookup"><span data-stu-id="08243-416">Again, the video is cropped but not stretched.</span></span> <span data-ttu-id="08243-417">Die Quell-und Ziel Rechtecke werden im folgenden Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="08243-417">The source and destination rectangles are shown in the following diagram.</span></span>

![Diagramm, das sich überschneidende Ziel Rechtecke zeigt.](images/fbe450cb-c84d-4110-9515-00f27601528e.gif)

<span data-ttu-id="08243-419">Das vorangehende Diagramm zeigt die folgenden Rechtecke:</span><span class="sxs-lookup"><span data-stu-id="08243-419">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="08243-420">Ziel Rechteck: {0, 0, 720, 576}</span><span class="sxs-lookup"><span data-stu-id="08243-420">Target rectangle: { 0, 0, 720, 576 }</span></span>
-   <span data-ttu-id="08243-421">Primäres Video:</span><span class="sxs-lookup"><span data-stu-id="08243-421">Primary video:</span></span>
    -   <span data-ttu-id="08243-422">Quell Oberflächen Größe: {0, 0, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="08243-422">Source surface size: { 0, 0, 720, 480 }</span></span>
    -   <span data-ttu-id="08243-423">Quell Rechteck: {260, 92, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="08243-423">Source rectangle: { 260, 92, 720, 480 }</span></span>
    -   <span data-ttu-id="08243-424">Ziel Rechteck: {0, 0, 460, 388}</span><span class="sxs-lookup"><span data-stu-id="08243-424">Destination rectangle: { 0, 0, 460, 388 }</span></span>
-   <span data-ttu-id="08243-425">Unter Datenstrom</span><span class="sxs-lookup"><span data-stu-id="08243-425">Substream:</span></span>
    -   <span data-ttu-id="08243-426">Quell Oberflächen Größe: {0, 0, 640, 576}</span><span class="sxs-lookup"><span data-stu-id="08243-426">Source surface size: { 0, 0, 640, 576 }</span></span>
    -   <span data-ttu-id="08243-427">Quell Rechteck: {0, 0, 460, 388}</span><span class="sxs-lookup"><span data-stu-id="08243-427">Source rectangle: { 0, 0, 460, 388 }</span></span>
    -   <span data-ttu-id="08243-428">Ziel Rechteck: {260, 188, 720, 576}</span><span class="sxs-lookup"><span data-stu-id="08243-428">Destination rectangle: { 260, 188, 720, 576 }</span></span>

### <a name="example-7-stretching-and-cropping-video"></a><span data-ttu-id="08243-429">Beispiel 7: Stretching und Zuschneiden von Videos</span><span class="sxs-lookup"><span data-stu-id="08243-429">Example 7: Stretching and Cropping Video</span></span>

<span data-ttu-id="08243-430">In diesem Beispiel wird das Video gestreckt und abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="08243-430">In this example, the video is stretched as well as cropped.</span></span> <span data-ttu-id="08243-431">Eine 180 × 120-Region aus jedem Stream wird gestreckt, um einen 360 × 240-Bereich im Ziel Rechteck abzudecken.</span><span class="sxs-lookup"><span data-stu-id="08243-431">A 180 × 120 region from each stream is stretched to cover a 360 × 240 area in the destination rectangle.</span></span>

![Diagramm, das Stretching und Zuschneiden anzeigt.](images/ce83529c-8545-492c-9d3e-ef221c30e326.gif)

<span data-ttu-id="08243-433">Das vorangehende Diagramm zeigt die folgenden Rechtecke:</span><span class="sxs-lookup"><span data-stu-id="08243-433">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="08243-434">Ziel Rechteck: {0, 0, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="08243-434">Target rectangle: { 0, 0, 720, 480 }</span></span>
-   <span data-ttu-id="08243-435">Primäres Video:</span><span class="sxs-lookup"><span data-stu-id="08243-435">Primary video:</span></span>
    -   <span data-ttu-id="08243-436">Quell Oberflächen Größe: {0, 0, 360, 240}</span><span class="sxs-lookup"><span data-stu-id="08243-436">Source surface size: { 0, 0, 360, 240 }</span></span>
    -   <span data-ttu-id="08243-437">Quell Rechteck: {180, 120, 360, 240}</span><span class="sxs-lookup"><span data-stu-id="08243-437">Source rectangle: { 180, 120, 360, 240 }</span></span>
    -   <span data-ttu-id="08243-438">Ziel Rechteck: {0, 0, 360, 240}</span><span class="sxs-lookup"><span data-stu-id="08243-438">Destination rectangle: { 0, 0, 360, 240 }</span></span>
-   <span data-ttu-id="08243-439">Unter Datenstrom</span><span class="sxs-lookup"><span data-stu-id="08243-439">Substream:</span></span>
    -   <span data-ttu-id="08243-440">Quell Oberflächen Größe: {0, 0, 360, 240}</span><span class="sxs-lookup"><span data-stu-id="08243-440">Source surface size: { 0, 0, 360, 240 }</span></span>
    -   <span data-ttu-id="08243-441">Quell Rechteck: {0, 0, 180, 120}</span><span class="sxs-lookup"><span data-stu-id="08243-441">Source rectangle: { 0, 0, 180, 120 }</span></span>
    -   <span data-ttu-id="08243-442">Ziel Rechteck: {360, 240, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="08243-442">Destination rectangle: { 360, 240, 720, 480 }</span></span>

## <a name="input-sample-order"></a><span data-ttu-id="08243-443">Eingabe Beispiel Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="08243-443">Input Sample Order</span></span>

<span data-ttu-id="08243-444">Der *psamples* -Parameter der [**videoprocess BLT**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) -Methode ist ein Zeiger auf ein Array von Eingabe Beispielen.</span><span class="sxs-lookup"><span data-stu-id="08243-444">The *pSamples* parameter of the [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) method is a pointer to an array of input samples.</span></span> <span data-ttu-id="08243-445">Beispiele aus dem primären Videostream werden zuerst angezeigt, gefolgt von unter Datenstrom-Bildern in Z-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="08243-445">Samples from the primary video stream appear first, followed by substream pictures in Z-order.</span></span> <span data-ttu-id="08243-446">Beispiele müssen in der folgenden Reihenfolge in das Array eingefügt werden:</span><span class="sxs-lookup"><span data-stu-id="08243-446">Samples must be placed into the array in the following order:</span></span>

-   <span data-ttu-id="08243-447">Die Beispiele für den primären Videostream werden zuerst in der zeitlichen Reihenfolge im Array angezeigt.</span><span class="sxs-lookup"><span data-stu-id="08243-447">Samples for the primary video stream appear first in the array, in temporal order.</span></span> <span data-ttu-id="08243-448">Abhängig vom Deinterlacing-Modus benötigt der Treiber möglicherweise ein oder mehrere Verweis Beispiele aus dem primären Videostream.</span><span class="sxs-lookup"><span data-stu-id="08243-448">Depending on the deinterlace mode, the driver may require one or more reference samples from the primary video stream.</span></span> <span data-ttu-id="08243-449">Die Member **numforwardrefsamples** und **numbackwardrefsamples** der [**DXVA2 \_ videoprocess orcaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) -Struktur geben an, wie viele vorwärts-und rückwärts Verweis Beispiele benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="08243-449">The **NumForwardRefSamples** and **NumBackwardRefSamples** members of the [**DXVA2\_VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) structure specify how many forward and backward reference samples are needed.</span></span> <span data-ttu-id="08243-450">Der Aufrufer muss diese Verweis Beispiele auch dann bereitstellen, wenn der Videoinhalt progressiv ist und Deinterlacing nicht erfordert.</span><span class="sxs-lookup"><span data-stu-id="08243-450">The caller must provide these reference samples even if the video content is progressive and does not require deinterlacing.</span></span> <span data-ttu-id="08243-451">(Dies kann vorkommen, wenn progressive Frames an ein Deinterlacing-Gerät übergeben werden, z. b. wenn die Quelle eine Mischung aus Zeilen Sprung-und progressivem Rahmen enthält.)</span><span class="sxs-lookup"><span data-stu-id="08243-451">(This can occur when progressive frames are given to a deinterlacing device, for example when the source contains a mix of both interlaced and progressive frames.)</span></span>
-   <span data-ttu-id="08243-452">Nach den Beispielen für den primären Videostream kann das Array bis zu 15 substreambeispiele enthalten, die in der Z-Reihenfolge von unten nach oben angeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="08243-452">After the samples for the primary video stream, the array can contain up to 15 substream samples, arranged in Z-order, from bottom to top.</span></span> <span data-ttu-id="08243-453">Unter Ströme sind immer progressiv und erfordern keine Referenzbilder.</span><span class="sxs-lookup"><span data-stu-id="08243-453">Substreams are always progressive and do not require reference pictures.</span></span>

<span data-ttu-id="08243-454">Der primäre Videostream kann jederzeit zwischen Zeilen Sprung-und progressivem Inhalt wechseln, und die Anzahl der untergeordneten Datenströme kann sich ändern.</span><span class="sxs-lookup"><span data-stu-id="08243-454">At any time, the primary video stream can switch between interlaced and progressive content, and the number of substreams can change.</span></span>

<span data-ttu-id="08243-455">Der **Sampleformat. Sampleformat** -Member der [**DXVA2 \_ Videosample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) -Struktur gibt den Bildtyp an.</span><span class="sxs-lookup"><span data-stu-id="08243-455">The **SampleFormat.SampleFormat** member of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure indicates the type of picture.</span></span> <span data-ttu-id="08243-456">Legen Sie für substreambilder diesen Wert auf DXVA2 \_ samplesubstream fest.</span><span class="sxs-lookup"><span data-stu-id="08243-456">For substream pictures, set this value to DXVA2\_SampleSubStream.</span></span> <span data-ttu-id="08243-457">Für Progressive Bilder lautet der Wert DXVA2 \_ sampleprogressiveframe.</span><span class="sxs-lookup"><span data-stu-id="08243-457">For progressive pictures, the value is DXVA2\_SampleProgressiveFrame.</span></span> <span data-ttu-id="08243-458">Für Zeilen Sprung Bilder hängt der Wert vom Feld Layout ab.</span><span class="sxs-lookup"><span data-stu-id="08243-458">For interlaced pictures, the value depends on the field layout.</span></span>

<span data-ttu-id="08243-459">Wenn der Treiber Forward-und rückwärts Verweis Beispiele erfordert, ist die vollständige Anzahl von Samplings möglicherweise zu Beginn der Videosequenz nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="08243-459">If the driver requires forward and backward reference samples, the full number of samples might not be available at the start of the video sequence.</span></span> <span data-ttu-id="08243-460">Fügen Sie in diesem Fall Einträge für Sie in das *psamples* -Array ein, aber markieren Sie die fehlenden Beispiele als Typ DXVA2 \_ sampleunknown.</span><span class="sxs-lookup"><span data-stu-id="08243-460">In that case, include entries for them in the *pSamples* array, but mark the missing samples as having type DXVA2\_SampleUnknown.</span></span>

<span data-ttu-id="08243-461">Das **Start** -und das **Endelement** der [**DXVA2 \_ Videosample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) -Struktur gibt den temporalen Speicherort jeder Stichprobe an.</span><span class="sxs-lookup"><span data-stu-id="08243-461">The **Start** and **End** members of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure give the temporal location of each sample.</span></span> <span data-ttu-id="08243-462">Diese Werte werden nur für Beispiele aus dem primären Videostream verwendet.</span><span class="sxs-lookup"><span data-stu-id="08243-462">These values are used only for samples from the primary video stream.</span></span> <span data-ttu-id="08243-463">Legen Sie für substreambilder beide Elemente auf 0 (null) fest.</span><span class="sxs-lookup"><span data-stu-id="08243-463">For substream pictures, set both members to zero.</span></span>

<span data-ttu-id="08243-464">Die folgenden Beispiele helfen Ihnen möglicherweise dabei, diese Anforderungen zu verdeutlichen.</span><span class="sxs-lookup"><span data-stu-id="08243-464">The following examples may help to clarify these requirements.</span></span>

### <a name="example-1"></a><span data-ttu-id="08243-465">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="08243-465">Example 1</span></span>

<span data-ttu-id="08243-466">Der einfachste Fall tritt auf, wenn keine untergeordneten Datenströme vorhanden sind und der Deinterlacing-Algorithmus keine Verweis Beispiele erfordert (**numforwardrefsamples** und **numbackwardrefsamples** sind gleich null).</span><span class="sxs-lookup"><span data-stu-id="08243-466">The simplest case occurs when there are no substreams and the deinterlacing algorithm does not require reference samples (**NumForwardRefSamples** and **NumBackwardRefSamples** are both zero).</span></span> <span data-ttu-id="08243-467">Bob Deinterlacing ist ein Beispiel für einen solchen Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="08243-467">Bob deinterlacing is an example of such an algorithm.</span></span> <span data-ttu-id="08243-468">In diesem Fall sollte das *psamples* -Array eine einzelne Eingabe Oberfläche enthalten, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="08243-468">In this case, the *pSamples* array should contain a single input surface, as shown in the following table.</span></span>



| <span data-ttu-id="08243-469">Index</span><span class="sxs-lookup"><span data-stu-id="08243-469">Index</span></span>           | <span data-ttu-id="08243-470">Surface-Typ</span><span class="sxs-lookup"><span data-stu-id="08243-470">Surface type</span></span>        | <span data-ttu-id="08243-471">Temporaler Speicherort</span><span class="sxs-lookup"><span data-stu-id="08243-471">Temporal location</span></span> |
|-----------------|---------------------|-------------------|
| <span data-ttu-id="08243-472">*psamples* \[ 1,0\]</span><span class="sxs-lookup"><span data-stu-id="08243-472">*pSamples*\[0\]</span></span> | <span data-ttu-id="08243-473">Zeilen Sprung Bild.</span><span class="sxs-lookup"><span data-stu-id="08243-473">Interlaced picture.</span></span> | <span data-ttu-id="08243-474">*T*</span><span class="sxs-lookup"><span data-stu-id="08243-474">*T*</span></span>               |



 

<span data-ttu-id="08243-475">Der Zeitwert *T* wird als Startzeit des aktuellen Video Rahmens angenommen.</span><span class="sxs-lookup"><span data-stu-id="08243-475">The time value *T* is assumed to be the start time of the current video frame.</span></span>

### <a name="example-2"></a><span data-ttu-id="08243-476">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="08243-476">Example 2</span></span>

<span data-ttu-id="08243-477">In diesem Beispiel werden von der Anwendung zwei untergeordnete Datenströme mit dem primären Stream gemischt.</span><span class="sxs-lookup"><span data-stu-id="08243-477">In this example, the application mixes two substreams with the primary stream.</span></span> <span data-ttu-id="08243-478">Der Deinterlacing-Algorithmus benötigt keine Verweis Beispiele.</span><span class="sxs-lookup"><span data-stu-id="08243-478">The deinterlacing algorithm does not require reference samples.</span></span> <span data-ttu-id="08243-479">In der folgenden Tabelle wird gezeigt, wie diese Beispiele im *psamples* -Array angeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="08243-479">The following table shows how these samples are arranged in the *pSamples* array.</span></span>



| <span data-ttu-id="08243-480">Index</span><span class="sxs-lookup"><span data-stu-id="08243-480">Index</span></span>           | <span data-ttu-id="08243-481">Surface-Typ</span><span class="sxs-lookup"><span data-stu-id="08243-481">Surface type</span></span>       | <span data-ttu-id="08243-482">Temporaler Speicherort</span><span class="sxs-lookup"><span data-stu-id="08243-482">Temporal location</span></span> | <span data-ttu-id="08243-483">Z-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="08243-483">Z-order</span></span> |
|-----------------|--------------------|-------------------|---------|
| <span data-ttu-id="08243-484">*psamples* \[ 1,0\]</span><span class="sxs-lookup"><span data-stu-id="08243-484">*pSamples*\[0\]</span></span> | <span data-ttu-id="08243-485">Zeilen Sprung Bild</span><span class="sxs-lookup"><span data-stu-id="08243-485">Interlaced picture</span></span> | <span data-ttu-id="08243-486">*T*</span><span class="sxs-lookup"><span data-stu-id="08243-486">*T*</span></span>               | <span data-ttu-id="08243-487">0</span><span class="sxs-lookup"><span data-stu-id="08243-487">0</span></span>       |
| <span data-ttu-id="08243-488">*psamples* \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="08243-488">*pSamples*\[1\]</span></span> | <span data-ttu-id="08243-489">Unter Datenstrom</span><span class="sxs-lookup"><span data-stu-id="08243-489">Substream</span></span>          | <span data-ttu-id="08243-490">0</span><span class="sxs-lookup"><span data-stu-id="08243-490">0</span></span>                 | <span data-ttu-id="08243-491">1</span><span class="sxs-lookup"><span data-stu-id="08243-491">1</span></span>       |
| <span data-ttu-id="08243-492">*psamples* \[ 2,2\]</span><span class="sxs-lookup"><span data-stu-id="08243-492">*pSamples*\[2\]</span></span> | <span data-ttu-id="08243-493">Unter Datenstrom</span><span class="sxs-lookup"><span data-stu-id="08243-493">Substream</span></span>          | <span data-ttu-id="08243-494">0</span><span class="sxs-lookup"><span data-stu-id="08243-494">0</span></span>                 | <span data-ttu-id="08243-495">2</span><span class="sxs-lookup"><span data-stu-id="08243-495">2</span></span>       |



 

### <a name="example-3"></a><span data-ttu-id="08243-496">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="08243-496">Example 3</span></span>

<span data-ttu-id="08243-497">Nehmen Sie nun an, dass für den Deinterlacing-Algorithmus ein abwärts Verweis Beispiel und ein vorwärts Verweis Beispiel erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="08243-497">Now suppose that the deinterlacing algorithm requires one backward reference sample and one forward reference sample.</span></span> <span data-ttu-id="08243-498">Außerdem werden zwei substreambilder bereitgestellt, die insgesamt fünf Oberflächen enthalten.</span><span class="sxs-lookup"><span data-stu-id="08243-498">In addition, two substream pictures are provided, for a total of five surfaces.</span></span> <span data-ttu-id="08243-499">Die richtige Reihenfolge wird in der folgenden Tabelle gezeigt.</span><span class="sxs-lookup"><span data-stu-id="08243-499">The correct ordering is shown in the following table.</span></span>



| <span data-ttu-id="08243-500">Index</span><span class="sxs-lookup"><span data-stu-id="08243-500">Index</span></span>           | <span data-ttu-id="08243-501">Surface-Typ</span><span class="sxs-lookup"><span data-stu-id="08243-501">Surface type</span></span>                   | <span data-ttu-id="08243-502">Temporaler Speicherort</span><span class="sxs-lookup"><span data-stu-id="08243-502">Temporal location</span></span> | <span data-ttu-id="08243-503">Z-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="08243-503">Z-order</span></span>        |
|-----------------|--------------------------------|-------------------|----------------|
| <span data-ttu-id="08243-504">*psamples* \[ 1,0\]</span><span class="sxs-lookup"><span data-stu-id="08243-504">*pSamples*\[0\]</span></span> | <span data-ttu-id="08243-505">Zeilen Sprung Bild (Referenz)</span><span class="sxs-lookup"><span data-stu-id="08243-505">Interlaced picture (reference)</span></span> | <span data-ttu-id="08243-506">*T* -1</span><span class="sxs-lookup"><span data-stu-id="08243-506">*T* −1</span></span>            | <span data-ttu-id="08243-507">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="08243-507">Not applicable</span></span> |
| <span data-ttu-id="08243-508">*psamples* \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="08243-508">*pSamples*\[1\]</span></span> | <span data-ttu-id="08243-509">Zeilen Sprung Bild</span><span class="sxs-lookup"><span data-stu-id="08243-509">Interlaced picture</span></span>             | <span data-ttu-id="08243-510">*T*</span><span class="sxs-lookup"><span data-stu-id="08243-510">*T*</span></span>               | <span data-ttu-id="08243-511">0</span><span class="sxs-lookup"><span data-stu-id="08243-511">0</span></span>              |
| <span data-ttu-id="08243-512">*psamples* \[ 2,2\]</span><span class="sxs-lookup"><span data-stu-id="08243-512">*pSamples*\[2\]</span></span> | <span data-ttu-id="08243-513">Zeilen Sprung Bild (Referenz)</span><span class="sxs-lookup"><span data-stu-id="08243-513">Interlaced picture (reference)</span></span> | <span data-ttu-id="08243-514">*T* + 1</span><span class="sxs-lookup"><span data-stu-id="08243-514">*T* +1</span></span>            | <span data-ttu-id="08243-515">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="08243-515">Not applicable</span></span> |
| <span data-ttu-id="08243-516">*psamples* \[ €\]</span><span class="sxs-lookup"><span data-stu-id="08243-516">*pSamples*\[3\]</span></span> | <span data-ttu-id="08243-517">Unter Datenstrom</span><span class="sxs-lookup"><span data-stu-id="08243-517">Substream</span></span>                      | <span data-ttu-id="08243-518">0</span><span class="sxs-lookup"><span data-stu-id="08243-518">0</span></span>                 | <span data-ttu-id="08243-519">1</span><span class="sxs-lookup"><span data-stu-id="08243-519">1</span></span>              |
| <span data-ttu-id="08243-520">*psamples* \[ 0:\]</span><span class="sxs-lookup"><span data-stu-id="08243-520">*pSamples*\[4\]</span></span> | <span data-ttu-id="08243-521">Unter Datenstrom</span><span class="sxs-lookup"><span data-stu-id="08243-521">Substream</span></span>                      | <span data-ttu-id="08243-522">0</span><span class="sxs-lookup"><span data-stu-id="08243-522">0</span></span>                 | <span data-ttu-id="08243-523">2</span><span class="sxs-lookup"><span data-stu-id="08243-523">2</span></span>              |



 

<span data-ttu-id="08243-524">Die Zeit *t* − 1 ist die Startzeit des Frames vor dem aktuellen Frame, und *T* + 1 ist die Startzeit des folgenden Frames.</span><span class="sxs-lookup"><span data-stu-id="08243-524">The time *T* −1 is the start time of the frame before the current frame, and *T* +1 is the start time of the following frame.</span></span>

<span data-ttu-id="08243-525">Wenn der Videostream in den progressiven Inhalt wechselt, muss die Anwendung dieselbe Anzahl von Stichproben bereitstellen, wie in der folgenden Tabelle gezeigt.</span><span class="sxs-lookup"><span data-stu-id="08243-525">If the video stream switches to progressive content, using the same deinterlacing mode, the application must provide the same number of samples, as shown in the following table.</span></span>



| <span data-ttu-id="08243-526">Index</span><span class="sxs-lookup"><span data-stu-id="08243-526">Index</span></span>           | <span data-ttu-id="08243-527">Surface-Typ</span><span class="sxs-lookup"><span data-stu-id="08243-527">Surface type</span></span>                    | <span data-ttu-id="08243-528">Temporaler Speicherort</span><span class="sxs-lookup"><span data-stu-id="08243-528">Temporal location</span></span> | <span data-ttu-id="08243-529">Z-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="08243-529">Z-order</span></span>        |
|-----------------|---------------------------------|-------------------|----------------|
| <span data-ttu-id="08243-530">*psamples* \[ 1,0\]</span><span class="sxs-lookup"><span data-stu-id="08243-530">*pSamples*\[0\]</span></span> | <span data-ttu-id="08243-531">Progressives Bild (Referenz)</span><span class="sxs-lookup"><span data-stu-id="08243-531">Progressive picture (reference)</span></span> | <span data-ttu-id="08243-532">*T* -1</span><span class="sxs-lookup"><span data-stu-id="08243-532">*T* −1</span></span>            | <span data-ttu-id="08243-533">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="08243-533">Not applicable</span></span> |
| <span data-ttu-id="08243-534">*psamples* \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="08243-534">*pSamples*\[1\]</span></span> | <span data-ttu-id="08243-535">Progressives Bild</span><span class="sxs-lookup"><span data-stu-id="08243-535">Progressive picture</span></span>             | <span data-ttu-id="08243-536">*T*</span><span class="sxs-lookup"><span data-stu-id="08243-536">*T*</span></span>               | <span data-ttu-id="08243-537">0</span><span class="sxs-lookup"><span data-stu-id="08243-537">0</span></span>              |
| <span data-ttu-id="08243-538">*psamples* \[ 2,2\]</span><span class="sxs-lookup"><span data-stu-id="08243-538">*pSamples*\[2\]</span></span> | <span data-ttu-id="08243-539">Progressives Bild (Referenz)</span><span class="sxs-lookup"><span data-stu-id="08243-539">Progressive picture (reference)</span></span> | <span data-ttu-id="08243-540">*T* + 1</span><span class="sxs-lookup"><span data-stu-id="08243-540">*T* +1</span></span>            | <span data-ttu-id="08243-541">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="08243-541">Not applicable</span></span> |
| <span data-ttu-id="08243-542">*psamples* \[ €\]</span><span class="sxs-lookup"><span data-stu-id="08243-542">*pSamples*\[3\]</span></span> | <span data-ttu-id="08243-543">Unter Datenstrom</span><span class="sxs-lookup"><span data-stu-id="08243-543">Substream</span></span>                       | <span data-ttu-id="08243-544">0</span><span class="sxs-lookup"><span data-stu-id="08243-544">0</span></span>                 | <span data-ttu-id="08243-545">1</span><span class="sxs-lookup"><span data-stu-id="08243-545">1</span></span>              |
| <span data-ttu-id="08243-546">*psamples* \[ 0:\]</span><span class="sxs-lookup"><span data-stu-id="08243-546">*pSamples*\[4\]</span></span> | <span data-ttu-id="08243-547">Unter Datenstrom</span><span class="sxs-lookup"><span data-stu-id="08243-547">Substream</span></span>                       | <span data-ttu-id="08243-548">0</span><span class="sxs-lookup"><span data-stu-id="08243-548">0</span></span>                 | <span data-ttu-id="08243-549">2</span><span class="sxs-lookup"><span data-stu-id="08243-549">2</span></span>              |



 

### <a name="example-4"></a><span data-ttu-id="08243-550">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="08243-550">Example 4</span></span>

<span data-ttu-id="08243-551">Zu Beginn einer Videosequenz sind möglicherweise vorwärts-und rückwärts Verweis Beispiele nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="08243-551">At the start of a video sequence, forward and backward reference samples might not be available.</span></span> <span data-ttu-id="08243-552">In diesem Fall sind Einträge für die fehlenden Stichproben im *psamples* -Array mit dem Beispieltyp DXVA2 \_ sampleunknown enthalten.</span><span class="sxs-lookup"><span data-stu-id="08243-552">When this happens, entries for the missing samples are included in the *pSamples* array, with sample type DXVA2\_SampleUnknown.</span></span>

<span data-ttu-id="08243-553">Vorausgesetzt, dass der Deinterlacing-Modus ein vorwärts-und ein abwärts Verweis Beispiel benötigt, verfügen die ersten drei Aufrufe an [**videoprocesblt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) über die Sequenzen von Eingaben, die in den folgenden drei Tabellen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="08243-553">Assuming that the deinterlacing mode needs one forward and one backward reference sample, the first three calls to [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) would have the sequences of inputs shown in the following three tables.</span></span>



| <span data-ttu-id="08243-554">Index</span><span class="sxs-lookup"><span data-stu-id="08243-554">Index</span></span>           | <span data-ttu-id="08243-555">Surface-Typ</span><span class="sxs-lookup"><span data-stu-id="08243-555">Surface type</span></span>                   | <span data-ttu-id="08243-556">Temporaler Speicherort</span><span class="sxs-lookup"><span data-stu-id="08243-556">Temporal location</span></span> |
|-----------------|--------------------------------|-------------------|
| <span data-ttu-id="08243-557">*psamples* \[ 1,0\]</span><span class="sxs-lookup"><span data-stu-id="08243-557">*pSamples*\[0\]</span></span> | <span data-ttu-id="08243-558">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="08243-558">Unknown</span></span>                        | <span data-ttu-id="08243-559">0</span><span class="sxs-lookup"><span data-stu-id="08243-559">0</span></span>                 |
| <span data-ttu-id="08243-560">*psamples* \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="08243-560">*pSamples*\[1\]</span></span> | <span data-ttu-id="08243-561">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="08243-561">Unknown</span></span>                        | <span data-ttu-id="08243-562">0</span><span class="sxs-lookup"><span data-stu-id="08243-562">0</span></span>                 |
| <span data-ttu-id="08243-563">*psamples* \[ 2,2\]</span><span class="sxs-lookup"><span data-stu-id="08243-563">*pSamples*\[2\]</span></span> | <span data-ttu-id="08243-564">Zeilen Sprung Bild (Referenz)</span><span class="sxs-lookup"><span data-stu-id="08243-564">Interlaced picture (reference)</span></span> | <span data-ttu-id="08243-565">*T* + 1</span><span class="sxs-lookup"><span data-stu-id="08243-565">*T* +1</span></span>            |



 



| <span data-ttu-id="08243-566">Index</span><span class="sxs-lookup"><span data-stu-id="08243-566">Index</span></span>           | <span data-ttu-id="08243-567">Surface-Typ</span><span class="sxs-lookup"><span data-stu-id="08243-567">Surface type</span></span>                   | <span data-ttu-id="08243-568">Temporaler Speicherort</span><span class="sxs-lookup"><span data-stu-id="08243-568">Temporal location</span></span> |
|-----------------|--------------------------------|-------------------|
| <span data-ttu-id="08243-569">*psamples* \[ 1,0\]</span><span class="sxs-lookup"><span data-stu-id="08243-569">*pSamples*\[0\]</span></span> | <span data-ttu-id="08243-570">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="08243-570">Unknown</span></span>                        | <span data-ttu-id="08243-571">0</span><span class="sxs-lookup"><span data-stu-id="08243-571">0</span></span>                 |
| <span data-ttu-id="08243-572">*psamples* \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="08243-572">*pSamples*\[1\]</span></span> | <span data-ttu-id="08243-573">Zeilen Sprung Bild</span><span class="sxs-lookup"><span data-stu-id="08243-573">Interlaced picture</span></span>             | <span data-ttu-id="08243-574">*T*</span><span class="sxs-lookup"><span data-stu-id="08243-574">*T*</span></span>               |
| <span data-ttu-id="08243-575">*psamples* \[ 2,2\]</span><span class="sxs-lookup"><span data-stu-id="08243-575">*pSamples*\[2\]</span></span> | <span data-ttu-id="08243-576">Zeilen Sprung Bild (Referenz)</span><span class="sxs-lookup"><span data-stu-id="08243-576">Interlaced picture (reference)</span></span> | <span data-ttu-id="08243-577">*T* + 1</span><span class="sxs-lookup"><span data-stu-id="08243-577">*T* +1</span></span>            |



 



| <span data-ttu-id="08243-578">Index</span><span class="sxs-lookup"><span data-stu-id="08243-578">Index</span></span>           | <span data-ttu-id="08243-579">Surface-Typ</span><span class="sxs-lookup"><span data-stu-id="08243-579">Surface type</span></span>                   | <span data-ttu-id="08243-580">Temporaler Speicherort</span><span class="sxs-lookup"><span data-stu-id="08243-580">Temporal location</span></span> |
|-----------------|--------------------------------|-------------------|
| <span data-ttu-id="08243-581">*psamples* \[ 1,0\]</span><span class="sxs-lookup"><span data-stu-id="08243-581">*pSamples*\[0\]</span></span> | <span data-ttu-id="08243-582">Zeilen Sprung Bild</span><span class="sxs-lookup"><span data-stu-id="08243-582">Interlaced picture</span></span>             | <span data-ttu-id="08243-583">*T* -1</span><span class="sxs-lookup"><span data-stu-id="08243-583">*T* −1</span></span>            |
| <span data-ttu-id="08243-584">*psamples* \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="08243-584">*pSamples*\[1\]</span></span> | <span data-ttu-id="08243-585">Zeilen Sprung Bild</span><span class="sxs-lookup"><span data-stu-id="08243-585">Interlaced picture</span></span>             | <span data-ttu-id="08243-586">*T*</span><span class="sxs-lookup"><span data-stu-id="08243-586">*T*</span></span>               |
| <span data-ttu-id="08243-587">*psamples* \[ 2,2\]</span><span class="sxs-lookup"><span data-stu-id="08243-587">*pSamples*\[2\]</span></span> | <span data-ttu-id="08243-588">Zeilen Sprung Bild (Referenz)</span><span class="sxs-lookup"><span data-stu-id="08243-588">Interlaced picture (reference)</span></span> | <span data-ttu-id="08243-589">*T* + 1</span><span class="sxs-lookup"><span data-stu-id="08243-589">*T* +1</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="08243-590">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="08243-590">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08243-591">DirectX-Video Beschleunigung 2,0</span><span class="sxs-lookup"><span data-stu-id="08243-591">DirectX Video Acceleration 2.0</span></span>](directx-video-acceleration-2-0.md)
</dt> <dt>

[<span data-ttu-id="08243-592">DXVA2 \_ videoproc-Beispiel</span><span class="sxs-lookup"><span data-stu-id="08243-592">DXVA2\_VideoProc Sample</span></span>](dxva2-videoproc-sample.md)
</dt> </dl>

 

 
