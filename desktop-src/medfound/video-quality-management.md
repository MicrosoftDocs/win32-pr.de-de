---
description: Video Qualitäts Verwaltung
ms.assetid: 3617adf2-ed7b-4788-abce-58bc22a14511
title: Video Qualitäts Verwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 233ccd54cfcb98742abef9a91241e903c07ba549
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959225"
---
# <a name="video-quality-management"></a><span data-ttu-id="f2d3a-103">Video Qualitäts Verwaltung</span><span class="sxs-lookup"><span data-stu-id="f2d3a-103">Video Quality Management</span></span>

<span data-ttu-id="f2d3a-104">In diesem Thema werden einige Verbesserungen an der Video Pipeline in Windows 7 beschrieben, sowohl für Microsoft Media Foundation als auch für Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="f2d3a-104">This topic describes some improvements to the video pipeline in Windows 7, both for Microsoft Media Foundation and Microsoft DirectShow.</span></span>

<span data-ttu-id="f2d3a-105">In einer perfekten Welt würde das Video nie, unabhängig von der Videoauflösung oder der CPU-/GPU-Auslastung, nicht glatt verlaufen.</span><span class="sxs-lookup"><span data-stu-id="f2d3a-105">In a perfect world, video would never glitch, regardless of the video resolution or the CPU/GPU load.</span></span> <span data-ttu-id="f2d3a-106">Natürlich muss die Video Pipeline in der Lage sein, mit begrenzten Hardware Ressourcen umzugehen, und die Wiedergabe muss an die Systemumgebung angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="f2d3a-106">In reality, of course, the video pipeline must be able to cope with finite hardware resources, and it must adaptively tailor playback to the system environment.</span></span> <span data-ttu-id="f2d3a-107">Die Ziele für die Video Qualitäts Verwaltung sind folgende:</span><span class="sxs-lookup"><span data-stu-id="f2d3a-107">The goals for video quality management are to:</span></span>

-   <span data-ttu-id="f2d3a-108">Reduzieren Sie das Abgleiten (verworfene oder späte Rahmen).</span><span class="sxs-lookup"><span data-stu-id="f2d3a-108">Reduce glitching (dropped or late frames).</span></span>
-   <span data-ttu-id="f2d3a-109">Reduzieren Sie die Speicherauslastung, insbesondere in der GPU.</span><span class="sxs-lookup"><span data-stu-id="f2d3a-109">Reduce memory usage, especially in the GPU.</span></span>
-   <span data-ttu-id="f2d3a-110">Reduzieren Sie den Stromverbrauch, insbesondere bei Laptops, die auf Akkuleistung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f2d3a-110">Reduce power consumption, especially in laptops running on battery power.</span></span>
-   <span data-ttu-id="f2d3a-111">Erzielen Sie die bestmögliche Bildqualität, und zwar anhand von Ressourceneinschränkungen.</span><span class="sxs-lookup"><span data-stu-id="f2d3a-111">Get the best image quality possible, given resource constraints.</span></span>
-   <span data-ttu-id="f2d3a-112">Halten Sie das Video mit Audiodaten synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="f2d3a-112">Keep video synchronized with audio.</span></span>

<span data-ttu-id="f2d3a-113">Einige dieser Ziele sind gegenseitig, insbesondere bei Low-End-Systemen.</span><span class="sxs-lookup"><span data-stu-id="f2d3a-113">Some of these goals are contrary, particularly on low-end systems.</span></span> <span data-ttu-id="f2d3a-114">Im Allgemeinen gibt es einen Kompromiss zwischen Geschwindigkeit und Qualität.</span><span class="sxs-lookup"><span data-stu-id="f2d3a-114">Generally there is a trade-off between speed and quality.</span></span> <span data-ttu-id="f2d3a-115">Das Abrufen von Problemen ist eher verwerflich als bei moderater Reduzierung der visuellen Qualität.</span><span class="sxs-lookup"><span data-stu-id="f2d3a-115">Glitching is more objectionable than moderate reductions in visual quality.</span></span> <span data-ttu-id="f2d3a-116">Die relative Wichtigkeit des Stromverbrauchs variiert in Abhängigkeit von der Umgebung. auf einem Laptop, der mit Akkuleistung betrieben wird, ist es sehr wichtig.</span><span class="sxs-lookup"><span data-stu-id="f2d3a-116">The relative importance of power consumption varies with the environment; in a laptop running on battery power, it is very important.</span></span>

<span data-ttu-id="f2d3a-117">In Windows 7 bietet der Enhanced Video Renderer (EVR) eine bessere Unterstützung für die Video Qualitäts Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="f2d3a-117">In Windows 7, the enhanced video renderer (EVR) has better support for video quality management.</span></span> <span data-ttu-id="f2d3a-118">Sowohl die Media Foundation Pipeline als auch die DirectShow-Pipeline wurden aktualisiert, um diese Funktionen nutzen zu können.</span><span class="sxs-lookup"><span data-stu-id="f2d3a-118">Both the Media Foundation pipeline and the DirectShow pipeline have been updated to take advantage of these capabilities.</span></span> <span data-ttu-id="f2d3a-119">Eine zweistufige Vorgehensweise wird verwendet:</span><span class="sxs-lookup"><span data-stu-id="f2d3a-119">A two-pronged approach is used:</span></span>

-   <span data-ttu-id="f2d3a-120">Vor dem Start der Wiedergabe kann die Pipeline basierend auf den Energie Verwaltungs Einstellungen des Benutzers und den Hardwareinformationen statische Optimierungen durchführen.</span><span class="sxs-lookup"><span data-stu-id="f2d3a-120">Before playback starts, the pipeline can perform static optimizations, based on the user's power management settings and information about the hardware.</span></span>
-   <span data-ttu-id="f2d3a-121">Nach dem Start der Wiedergabe kann die Pipeline basierend auf der Laufzeitleistung dynamische Optimierungen anwenden.</span><span class="sxs-lookup"><span data-stu-id="f2d3a-121">After playback starts, the pipeline can apply dynamic optimizations, based on run-time performance.</span></span>

## <a name="quality-management-in-media-foundation"></a><span data-ttu-id="f2d3a-122">Qualitäts Verwaltung in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f2d3a-122">Quality Management in Media Foundation</span></span>

<span data-ttu-id="f2d3a-123">Um statische Optimierungen zu aktivieren, legen Sie das-Attribut für [ \_ \_ statische \_ Wiedergabe \_ Optimierungen der MF-Topologie](mf-topology-static-playback-optimizations.md) in der partiellen Topologie fest, bevor Sie die Topologie auflösen.</span><span class="sxs-lookup"><span data-stu-id="f2d3a-123">To enable static optimizations, set the [MF\_TOPOLOGY\_STATIC\_PLAYBACK\_OPTIMIZATIONS](mf-topology-static-playback-optimizations.md) attribute on the partial topology before resolving the topology.</span></span> <span data-ttu-id="f2d3a-124">Das topologielader fragt dieses Attribut in der [**imftopoloader:: Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) -Methode ab.</span><span class="sxs-lookup"><span data-stu-id="f2d3a-124">The topology loader queries this attribute in its [**IMFTopoLoader::Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) method.</span></span>

<span data-ttu-id="f2d3a-125">Wenn Sie statische Optimierungen aktivieren, sollten Sie zwei weitere Attribute in der Topologie festlegen:</span><span class="sxs-lookup"><span data-stu-id="f2d3a-125">If you enable static optimizations, you should set two other attributes on the topology:</span></span>



| <span data-ttu-id="f2d3a-126">Attribut</span><span class="sxs-lookup"><span data-stu-id="f2d3a-126">Attribute</span></span>                                                                                                                                      | <span data-ttu-id="f2d3a-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2d3a-127">Description</span></span>                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="f2d3a-128"><span id="MF_TOPOLOGY_PLAYBACK_MAX_DIMS"></span><span id="mf_topology_playback_max_dims"></span>maximal zulässige Anzahl von MF- \_ \_ topologiewiedergabe \_ \_</span><span class="sxs-lookup"><span data-stu-id="f2d3a-128"><span id="MF_TOPOLOGY_PLAYBACK_MAX_DIMS"></span><span id="mf_topology_playback_max_dims"></span>MF\_TOPOLOGY\_PLAYBACK\_MAX\_DIMS</span></span><br/>   | <span data-ttu-id="f2d3a-129">Gibt die maximale Größe des Videowiedergabe Fensters an.</span><span class="sxs-lookup"><span data-stu-id="f2d3a-129">Specifies the maximum size of the video playback window.</span></span><br/> |
| <span data-ttu-id="f2d3a-130"><span id="MF_TOPOLOGY_PLAYBACK_FRAMERATE"></span><span id="mf_topology_playback_framerate"></span>MF- \_ \_ topologiewiedergabe \_ Framerate</span><span class="sxs-lookup"><span data-stu-id="f2d3a-130"><span id="MF_TOPOLOGY_PLAYBACK_FRAMERATE"></span><span id="mf_topology_playback_framerate"></span>MF\_TOPOLOGY\_PLAYBACK\_FRAMERATE</span></span><br/> | <span data-ttu-id="f2d3a-131">Gibt die Aktualisierungsrate des Monitors an.</span><span class="sxs-lookup"><span data-stu-id="f2d3a-131">Specifies the monitor refresh rate.</span></span><br/>                      |



 

<span data-ttu-id="f2d3a-132">Diese beiden Attribute helfen der Pipeline, die effektivste Einstellung für die Qualitäts Verwaltung zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="f2d3a-132">These two attributes help the pipeline calculate the most effective setting for quality management.</span></span>

<span data-ttu-id="f2d3a-133">Dynamische Optimierungen werden vom Quality Manager ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f2d3a-133">Dynamic optimizations are performed by the quality manager.</span></span> <span data-ttu-id="f2d3a-134">Sie müssen nichts tun, um den Quality Manager zu aktivieren. Er ist automatisch aktiviert.</span><span class="sxs-lookup"><span data-stu-id="f2d3a-134">You do not need to do anything to enable the quality manager; it is automatically enabled.</span></span> <span data-ttu-id="f2d3a-135">Der Quality Manager war in Windows Vista vorhanden. in Windows 7 kann der EVR besser auf Nachrichten vom Quality Manager reagieren.</span><span class="sxs-lookup"><span data-stu-id="f2d3a-135">The quality manager existed in Windows Vista; in Windows 7, the EVR can respond better to messages from the quality manager.</span></span>

## <a name="quality-management-in-directshow"></a><span data-ttu-id="f2d3a-136">Qualitäts Verwaltung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="f2d3a-136">Quality Management in DirectShow</span></span>

<span data-ttu-id="f2d3a-137">DirectShow unterstützt statische und dynamische Optimierungen für die DVD-Wiedergabe.</span><span class="sxs-lookup"><span data-stu-id="f2d3a-137">DirectShow supports static and dynamic optimizations for DVD playback.</span></span> <span data-ttu-id="f2d3a-138">Um diese Optimierungen in einer DVD-Wiedergabe Anwendung zu aktivieren, legen Sie die folgenden Flags im *dwFlags* -Parameter der **idvdgraphbuilder:: renderdvdvideovolume** -Methode fest:</span><span class="sxs-lookup"><span data-stu-id="f2d3a-138">To enable these optimizations in a DVD playback application, set the following flags in the *dwFlags* parameter of the **IDvdGraphBuilder::RenderDvdVideoVolume** method:</span></span>



| <span data-ttu-id="f2d3a-139">Flag</span><span class="sxs-lookup"><span data-stu-id="f2d3a-139">Flag</span></span>                  | <span data-ttu-id="f2d3a-140">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f2d3a-140">Description</span></span>                    |
|-----------------------|--------------------------------|
| <span data-ttu-id="f2d3a-141">AM- \_ DVD- \_ Anpassungs \_ Diagramm</span><span class="sxs-lookup"><span data-stu-id="f2d3a-141">AM\_DVD\_ADAPT\_GRAPH</span></span> | <span data-ttu-id="f2d3a-142">Aktiviert statische Optimierungen.</span><span class="sxs-lookup"><span data-stu-id="f2d3a-142">Enables static optimizations.</span></span>  |
| <span data-ttu-id="f2d3a-143">AM \_ DVD- \_ EVR- \_ QoS</span><span class="sxs-lookup"><span data-stu-id="f2d3a-143">AM\_DVD\_EVR\_QOS</span></span>     | <span data-ttu-id="f2d3a-144">Aktiviert dynamische Optimierungen.</span><span class="sxs-lookup"><span data-stu-id="f2d3a-144">Enables dynamic optimizations.</span></span> |



 

<span data-ttu-id="f2d3a-145">Andere DirectShow-Anwendungen können dynamische Optimierungen aktivieren, indem Sie die [**ievrfilterconfigex:: setconfigprefs**](/windows/desktop/api/evr/nf-evr-ievrfilterconfigex-setconfigprefs) -Methode direkt für den EVR-Filter aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f2d3a-145">Other DirectShow applications can enable dynamic optimizations by calling the [**IEVRFilterConfigEx::SetConfigPrefs**](/windows/desktop/api/evr/nf-evr-ievrfilterconfigex-setconfigprefs) method directly on the EVR filter.</span></span> <span data-ttu-id="f2d3a-146">Geben Sie das Flag " **evrfilterconfigprefs \_ enableqos** " an.</span><span class="sxs-lookup"><span data-stu-id="f2d3a-146">Specify the **EVRFilterConfigPrefs\_EnableQoS** flag.</span></span>

> [!Note]  
> <span data-ttu-id="f2d3a-147">Statische Optimierungen in DirectShow sind auf die DVD-Wiedergabe beschränkt.</span><span class="sxs-lookup"><span data-stu-id="f2d3a-147">Static optimizations in DirectShow are limited to DVD playback.</span></span>

 

## <a name="quality-management-in-the-evr"></a><span data-ttu-id="f2d3a-148">Qualitäts Verwaltung im EVR</span><span class="sxs-lookup"><span data-stu-id="f2d3a-148">Quality Management in the EVR</span></span>

<span data-ttu-id="f2d3a-149">Der EVR unterstützt einige neue Konfigurationsflags für die Qualitäts Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="f2d3a-149">The EVR supports some new configuration flags for quality management.</span></span> <span data-ttu-id="f2d3a-150">Wenn Sie die zuvor beschriebenen Optimierungen der Qualitäts Verwaltung aktivieren, müssen diese Flags nicht direkt festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f2d3a-150">If you enable the quality management optimizations described previously, you do not have to set these flags directly.</span></span> <span data-ttu-id="f2d3a-151">Sie sind jedoch für Anwendungen dokumentiert, die eine präzisetere Kontrolle über den EVR wünschen.</span><span class="sxs-lookup"><span data-stu-id="f2d3a-151">However, they are documented for applications that want more granular control over the EVR.</span></span>

<span data-ttu-id="f2d3a-152">Legen Sie die folgenden Flags auf dem EVR-Mixer fest, indem Sie die [**IMFVideoMixerControl2:: setmixingprefs**](/windows/desktop/api/evr/nf-evr-imfvideomixercontrol2-setmixingprefs) -Methode aufrufen:</span><span class="sxs-lookup"><span data-stu-id="f2d3a-152">Set the following flags on the EVR mixer by calling the [**IMFVideoMixerControl2::SetMixingPrefs**](/windows/desktop/api/evr/nf-evr-imfvideomixercontrol2-setmixingprefs) method:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f2d3a-153">Flags</span><span class="sxs-lookup"><span data-stu-id="f2d3a-153">Flags</span></span></th>
<th><span data-ttu-id="f2d3a-154">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2d3a-154">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="f2d3a-155"><strong>MFVideoMixPrefs_ForceHalfInterlace</strong></span><span class="sxs-lookup"><span data-stu-id="f2d3a-155"><strong>MFVideoMixPrefs_ForceHalfInterlace</strong></span></span></li>
<li><span data-ttu-id="f2d3a-156"><strong>MFVideoMixPrefs_AllowDropToHalfInterlace</strong></span><span class="sxs-lookup"><span data-stu-id="f2d3a-156"><strong>MFVideoMixPrefs_AllowDropToHalfInterlace</strong></span></span></li>
</ul></td>
<td><span data-ttu-id="f2d3a-157">Überspringen Sie das zweite Feld jedes Zeilen Sprung Bilds.</span><span class="sxs-lookup"><span data-stu-id="f2d3a-157">Skip the second field of every interlaced frame.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="f2d3a-158"><strong>MFVideoMixPrefs_AllowDropToBob</strong></span><span class="sxs-lookup"><span data-stu-id="f2d3a-158"><strong>MFVideoMixPrefs_AllowDropToBob</strong></span></span></li>
<li><span data-ttu-id="f2d3a-159"><strong>MFVideoMixPrefs_ForceBob</strong></span><span class="sxs-lookup"><span data-stu-id="f2d3a-159"><strong>MFVideoMixPrefs_ForceBob</strong></span></span></li>
</ul></td>
<td><span data-ttu-id="f2d3a-160">Verwenden Sie Bob Deinterlacing, auch wenn der Treiber einen Modus mit höherer Qualität unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f2d3a-160">Use bob deinterlacing, even if the driver supports a higher-quality deinterlace mode.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="f2d3a-161">Legen Sie die folgenden Flags auf dem EVR Presenter fest, indem Sie die [**imfvideodisplaycontrol:: setrenderingprefs**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setrenderingprefs) -Methode aufrufen:</span><span class="sxs-lookup"><span data-stu-id="f2d3a-161">Set the following flags on the EVR presenter by calling the [**IMFVideoDisplayControl::SetRenderingPrefs**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setrenderingprefs) method:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f2d3a-162">Flags</span><span class="sxs-lookup"><span data-stu-id="f2d3a-162">Flags</span></span></th>
<th><span data-ttu-id="f2d3a-163">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2d3a-163">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="f2d3a-164"><strong>MFVideoRenderPrefs_ForceOutputThrottling</strong></span><span class="sxs-lookup"><span data-stu-id="f2d3a-164"><strong>MFVideoRenderPrefs_ForceOutputThrottling</strong></span></span></li>
<li><span data-ttu-id="f2d3a-165"><strong>MFVideoRenderPrefs_AllowOutputThrottling</strong></span><span class="sxs-lookup"><span data-stu-id="f2d3a-165"><strong>MFVideoRenderPrefs_AllowOutputThrottling</strong></span></span></li>
</ul></td>
<td><span data-ttu-id="f2d3a-166">Drosselung der Ausgabe, um die GPU-Bandbreite zu</span><span class="sxs-lookup"><span data-stu-id="f2d3a-166">Throttle output to match GPU bandwidth.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="f2d3a-167"><strong>MFVideoRenderPrefs_ForceBatching</strong></span><span class="sxs-lookup"><span data-stu-id="f2d3a-167"><strong>MFVideoRenderPrefs_ForceBatching</strong></span></span></li>
<li><span data-ttu-id="f2d3a-168"><strong>MFVideoRenderPrefs_AllowBatching</strong></span><span class="sxs-lookup"><span data-stu-id="f2d3a-168"><strong>MFVideoRenderPrefs_AllowBatching</strong></span></span></li>
</ul></td>
<td><span data-ttu-id="f2d3a-169">Batch Direct3D vorhandene Aufrufe.</span><span class="sxs-lookup"><span data-stu-id="f2d3a-169">Batch Direct3D Present calls.</span></span> <span data-ttu-id="f2d3a-170">Durch diese Optimierung kann das System häufiger in den Leerlauf Status eintreten, wodurch der Energieverbrauch reduziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="f2d3a-170">This optimization enables the system to enter into idle states more frequently, which can reduce power consumption.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="f2d3a-171">MFVideoRenderPrefs_ForceScaling</span><span class="sxs-lookup"><span data-stu-id="f2d3a-171">MFVideoRenderPrefs_ForceScaling</span></span></li>
<li><span data-ttu-id="f2d3a-172">MFVideoRenderPrefs_AllowScaling</span><span class="sxs-lookup"><span data-stu-id="f2d3a-172">MFVideoRenderPrefs_AllowScaling</span></span></li>
</ul></td>
<td><span data-ttu-id="f2d3a-173">Führen Sie eine Video Mischung mit einem Rechteck aus, das kleiner als das Ausgabe Rechteck ist.</span><span class="sxs-lookup"><span data-stu-id="f2d3a-173">Perform video mixing using a rectangle smaller than the output rectangle.</span></span> <span data-ttu-id="f2d3a-174">Skalieren Sie das Ergebnis auf die richtige Ausgabegröße.</span><span class="sxs-lookup"><span data-stu-id="f2d3a-174">Scale the result to the correct output size.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="f2d3a-175">Außerdem unterstützt die EVR-Medien Senke Konfigurations Attribute, die den einzelnen Flags entsprechen:</span><span class="sxs-lookup"><span data-stu-id="f2d3a-175">In addition, the EVR media sink supports configuration attributes that correspond to each of these flags:</span></span>

-   [<span data-ttu-id="f2d3a-176">Evrconfig \_ allowbatching</span><span class="sxs-lookup"><span data-stu-id="f2d3a-176">EVRConfig\_AllowBatching</span></span>](evrconfig-allowbatching.md)
-   [<span data-ttu-id="f2d3a-177">Evrconfig \_ allowdropto Bob</span><span class="sxs-lookup"><span data-stu-id="f2d3a-177">EVRConfig\_AllowDropToBob</span></span>](evrconfig-allowdroptobob.md)
-   [<span data-ttu-id="f2d3a-178">Evrconfig \_ allowdropabhalfinterlace</span><span class="sxs-lookup"><span data-stu-id="f2d3a-178">EVRConfig\_AllowDropToHalfInterlace</span></span>](evrconfig-allowdroptohalfinterlace.md)
-   [<span data-ttu-id="f2d3a-179">Evrconfig \_ allowscaling</span><span class="sxs-lookup"><span data-stu-id="f2d3a-179">EVRConfig\_AllowScaling</span></span>](evrconfig-allowscaling.md)
-   [<span data-ttu-id="f2d3a-180">"Evrconfig \_ allowdropto Throttle"</span><span class="sxs-lookup"><span data-stu-id="f2d3a-180">EVRConfig\_AllowDropToThrottle</span></span>](evrconfig-allowdroptothrottle.md)
-   [<span data-ttu-id="f2d3a-181">Evrconfig \_ forcebatching</span><span class="sxs-lookup"><span data-stu-id="f2d3a-181">EVRConfig\_ForceBatching</span></span>](evrconfig-forcebatching.md)
-   [<span data-ttu-id="f2d3a-182">Evrconfig \_ forcebob</span><span class="sxs-lookup"><span data-stu-id="f2d3a-182">EVRConfig\_ForceBob</span></span>](evrconfig-forcebob.md)
-   [<span data-ttu-id="f2d3a-183">Evrconfig \_ forcehalfinterlace</span><span class="sxs-lookup"><span data-stu-id="f2d3a-183">EVRConfig\_ForceHalfInterlace</span></span>](evrconfig-forcehalfinterlace.md)
-   [<span data-ttu-id="f2d3a-184">Evrconfig- \_ forcescaleing</span><span class="sxs-lookup"><span data-stu-id="f2d3a-184">EVRConfig\_ForceScaling</span></span>](evrconfig-forcescaling.md)
-   [<span data-ttu-id="f2d3a-185">Evrconfig- \_ forcethrottle</span><span class="sxs-lookup"><span data-stu-id="f2d3a-185">EVRConfig\_ForceThrottle</span></span>](evrconfig-forcethrottle.md)

<span data-ttu-id="f2d3a-186">Vor dem Start der Wiedergabe können Sie diese Attribute direkt auf der EVR-Medien Senke festlegen, als Alternative zum Aufrufen der [**IMFVideoMixerControl2**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol2) -Methode und der [**imfvideodisplaycontrol**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) -Methode.</span><span class="sxs-lookup"><span data-stu-id="f2d3a-186">Before playback starts, you can set these attributes directly on the EVR media sink, as an alternative to calling the [**IMFVideoMixerControl2**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol2) and [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) methods.</span></span> <span data-ttu-id="f2d3a-187">Um diese Attribute festzulegen, Fragen Sie die EVR-Medien Senke nach [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)ab.</span><span class="sxs-lookup"><span data-stu-id="f2d3a-187">To set these attributes, query the EVR media sink for [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2d3a-188">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f2d3a-188">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2d3a-189">Medien Sitzung</span><span class="sxs-lookup"><span data-stu-id="f2d3a-189">Media Session</span></span>](media-session.md)
</dt> </dl>

 

 




