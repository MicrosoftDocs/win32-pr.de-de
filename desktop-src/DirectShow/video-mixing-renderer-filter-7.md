---
description: Video Mischungs-Renderer Filter 7
ms.assetid: c83e6c50-76f2-4aeb-944b-5b244c6bf776
title: Video Mischungs-Renderer Filter 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14e396e15189e89dcebde69fb513419df340ab09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527812"
---
# <a name="video-mixing-renderer-filter-7"></a><span data-ttu-id="19af0-103">Video Mischungs-Renderer Filter 7</span><span class="sxs-lookup"><span data-stu-id="19af0-103">Video Mixing Renderer Filter 7</span></span>

<span data-ttu-id="19af0-104">Dieses Thema gilt für Windows XP oder höher.</span><span class="sxs-lookup"><span data-stu-id="19af0-104">This topic applies to Windows XP or later.</span></span>

<span data-ttu-id="19af0-105">In Windows XP und höher ist der Video Mischungs-Renderer 7 (VMR-7) der Standardvideorenderer.</span><span class="sxs-lookup"><span data-stu-id="19af0-105">In Windows XP and later, the Video Mixing Renderer 7 (VMR-7) is the default video renderer.</span></span> <span data-ttu-id="19af0-106">Sie wird als "VMR-7" bezeichnet, da intern DirectDraw 7 verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="19af0-106">It is called the VMR-7 because internally it uses DirectDraw 7.</span></span> <span data-ttu-id="19af0-107">In DirectX 9 ist ein ähnlicher, aber separater Filter (VMR-9) für die erneute Verteilung auf nicht-XP-Systemen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="19af0-107">In DirectX 9, a similar but separate filter, the VMR-9, is available for redistribution on non-XP systems.</span></span> <span data-ttu-id="19af0-108">VMR-9 verwendet Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="19af0-108">The VMR-9 uses Direct3D 9.</span></span>

> [!Note]  
> <span data-ttu-id="19af0-109">VMR ist unter Windows XP und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="19af0-109">The VMR is available on Windows XP and later.</span></span> <span data-ttu-id="19af0-110">Es ist nicht über die Redistributable von DirectX oder frühere Versionen von Windows verfügbar.</span><span class="sxs-lookup"><span data-stu-id="19af0-110">It is not available through the DirectX redistributable, or on previous versions of Windows.</span></span> <span data-ttu-id="19af0-111">In den meisten Szenarien sollten Anwendungen den [Video Mischungs-Renderer 9](video-mixing-renderer-filter-9.md)verwenden.</span><span class="sxs-lookup"><span data-stu-id="19af0-111">For most scenarios, applications should use the [Video Mixing Renderer 9](video-mixing-renderer-filter-9.md).</span></span>

 

<span data-ttu-id="19af0-112">Zu den Features der VMR gehören:</span><span class="sxs-lookup"><span data-stu-id="19af0-112">Features of the VMR include:</span></span>

-   <span data-ttu-id="19af0-113">Echte Alpha Mischung von bis zu 16 Eingabedaten strömen</span><span class="sxs-lookup"><span data-stu-id="19af0-113">True alpha blending of up to 16 input streams</span></span>
-   <span data-ttu-id="19af0-114">Zugriff auf das zusammengesetzte Image, bevor es gerendert wird</span><span class="sxs-lookup"><span data-stu-id="19af0-114">Access to the composited image before it is rendered</span></span>
-   <span data-ttu-id="19af0-115">Ein Plug-in-Modell, das Drittanbietern das Implementieren von benutzerdefinierten Video Effekten ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="19af0-115">A plug-in model that enables third-parties to implement custom video effects.</span></span>
-   <span data-ttu-id="19af0-116">Unterstützung für bis zu 15 Monitore.</span><span class="sxs-lookup"><span data-stu-id="19af0-116">Support for up to 15 monitors.</span></span>

<span data-ttu-id="19af0-117">Während der Diagramm Erstellung unter Windows XP und höher verwendet der Filter Graph-Manager nicht die älteren Videorenderer oder Überlagerungs Filter Filter, es sei denn, die Anwendung erstellt Sie explizit und fügt Sie dem Diagramm hinzu.</span><span class="sxs-lookup"><span data-stu-id="19af0-117">During graph building on Windows XP and later, the Filter Graph Manager will not use the older Video Renderer or Overlay Mixer filters, unless the application explicitly creates them and adds to the graph.</span></span>

<span data-ttu-id="19af0-118">Weitere Informationen finden Sie unter [using the Video mischungsrenderer](using-the-video-mixing-renderer.md).</span><span class="sxs-lookup"><span data-stu-id="19af0-118">For more information, see [Using the Video Mixing Renderer](using-the-video-mixing-renderer.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="19af0-119">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="19af0-119">Filter Interfaces</span></span></td>
<td><span data-ttu-id="19af0-120">Alle Modi:</span><span class="sxs-lookup"><span data-stu-id="19af0-120">All modes:</span></span>
<ul>
<li><span data-ttu-id="19af0-121"><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>Iamcertifiedoutputprotection</strong></a></span><span class="sxs-lookup"><span data-stu-id="19af0-121"><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a></span></span></li>
<li><span data-ttu-id="19af0-122"><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>Iamfilterfehlflags</strong></a></span><span class="sxs-lookup"><span data-stu-id="19af0-122"><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></span></span></li>
<li><span data-ttu-id="19af0-123"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ibasefilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="19af0-123"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></li>
<li><span data-ttu-id="19af0-124"><a href="ikspropertyset.md"><strong>"Ikspropertyset"</strong></a></span><span class="sxs-lookup"><span data-stu-id="19af0-124"><a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a></span></span></li>
<li><span data-ttu-id="19af0-125"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>Imediaposition</strong></a></span><span class="sxs-lookup"><span data-stu-id="19af0-125"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a></span></span></li>
<li><span data-ttu-id="19af0-126"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>Imediaseeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="19af0-126"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></li>
<li><span data-ttu-id="19af0-127"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>Iqualitycontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="19af0-127"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></li>
<li><span data-ttu-id="19af0-128"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>Iqualprop</strong></a></span><span class="sxs-lookup"><span data-stu-id="19af0-128"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></span></span></li>
<li><span data-ttu-id="19af0-129"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmraspectratiocontrol"><strong>Ivmraspectratiocontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="19af0-129"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmraspectratiocontrol"><strong>IVMRAspectRatioControl</strong></a></span></span></li>
<li><span data-ttu-id="19af0-130"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol"><strong>Ivmrdeinterlacecontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="19af0-130"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol"><strong>IVMRDeinterlaceControl</strong></a></span></span></li>
<li><span data-ttu-id="19af0-131"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig"><strong>Ivmrfilterconfig</strong></a></span><span class="sxs-lookup"><span data-stu-id="19af0-131"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig"><strong>IVMRFilterConfig</strong></a></span></span></li>
<li><span data-ttu-id="19af0-132"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap"><strong>Ivmrmixerbitmap</strong></a></span><span class="sxs-lookup"><span data-stu-id="19af0-132"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap"><strong>IVMRMixerBitmap</strong></a></span></span></li>
</ul>
<span data-ttu-id="19af0-133">Fenstermodus:</span><span class="sxs-lookup"><span data-stu-id="19af0-133">Windowed mode:</span></span><br/>
<ul>
<li><span data-ttu-id="19af0-134"><a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>Ibasicvideo</strong></a></span><span class="sxs-lookup"><span data-stu-id="19af0-134"><a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>IBasicVideo</strong></a></span></span></li>
<li><span data-ttu-id="19af0-135"><a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a></span><span class="sxs-lookup"><span data-stu-id="19af0-135"><a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a></span></span></li>
<li><span data-ttu-id="19af0-136"><a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a></span><span class="sxs-lookup"><span data-stu-id="19af0-136"><a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a></span></span></li>
<li><span data-ttu-id="19af0-137"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>Ivmrmonitorconfig</strong></a></span><span class="sxs-lookup"><span data-stu-id="19af0-137"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>IVMRMonitorConfig</strong></a></span></span></li>
</ul>
<span data-ttu-id="19af0-138">Fensterloser Modus:</span><span class="sxs-lookup"><span data-stu-id="19af0-138">Windowless mode:</span></span><br/>
<ul>
<li><span data-ttu-id="19af0-139"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol"><strong>Ivmrwindowlesscontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="19af0-139"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol"><strong>IVMRWindowlessControl</strong></a></span></span></li>
<li><span data-ttu-id="19af0-140"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>Ivmrmonitorconfig</strong></a></span><span class="sxs-lookup"><span data-stu-id="19af0-140"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>IVMRMonitorConfig</strong></a></span></span></li>
</ul>
<span data-ttu-id="19af0-141">Modus für renderlos:</span><span class="sxs-lookup"><span data-stu-id="19af0-141">Renderless mode:</span></span><br/>
<ul>
<li><span data-ttu-id="19af0-142"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify"><strong>Ivmrsurfacezuweisung</strong></a></span><span class="sxs-lookup"><span data-stu-id="19af0-142"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify"><strong>IVMRSurfaceAllocatorNotify</strong></a></span></span></li>
</ul>
<span data-ttu-id="19af0-143">Mischmodus:</span><span class="sxs-lookup"><span data-stu-id="19af0-143">Mixer mode:</span></span><br/>
<ul>
<li><span data-ttu-id="19af0-144"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol"><strong>Ivmrmixercontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="19af0-144"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol"><strong>IVMRMixerControl</strong></a></span></span></li>
</ul>
<span data-ttu-id="19af0-145">Informationen zu den verschiedenen VMR-7-Modi finden Sie unter <a href="vmr-modes-of-operation.md">VMR-Betriebsmodi</a>.</span><span class="sxs-lookup"><span data-stu-id="19af0-145">For information about the various VMR-7 modes, see <a href="vmr-modes-of-operation.md">VMR Modes of Operation</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19af0-146">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="19af0-146">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="19af0-147">Haupttyp: MEDIATYPE_VideoSubtype: hängt von der Grafikhardware ab.</span><span class="sxs-lookup"><span data-stu-id="19af0-147">Major type: MEDIATYPE_VideoSubtype: Depends on the graphics hardware.</span></span> <span data-ttu-id="19af0-148">Muss ein unkomprimiertes Video sein.</span><span class="sxs-lookup"><span data-stu-id="19af0-148">Must be uncompressed video.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19af0-149">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="19af0-149">Input Pin Interfaces</span></span></td>
<td><ul>
<li><span data-ttu-id="19af0-150"><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>Iamvideoaccelerator</strong></a></span><span class="sxs-lookup"><span data-stu-id="19af0-150"><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a></span></span></li>
<li><span data-ttu-id="19af0-151"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="19af0-151"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span></span></li>
<li><span data-ttu-id="19af0-152"><a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a> (siehe Hinweise)</span><span class="sxs-lookup"><span data-stu-id="19af0-152"><a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a> (see Remarks)</span></span></li>
<li><span data-ttu-id="19af0-153"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="19af0-153"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span></span></li>
<li><span data-ttu-id="19af0-154"><a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>Ipinconnection</strong></a></span><span class="sxs-lookup"><span data-stu-id="19af0-154"><a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a></span></span></li>
<li><span data-ttu-id="19af0-155"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>Iqualitycontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="19af0-155"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></li>
<li><span data-ttu-id="19af0-156"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrvideostreamcontrol"><strong>Ivmrvideostreamcontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="19af0-156"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrvideostreamcontrol"><strong>IVMRVideoStreamControl</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19af0-157">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="19af0-157">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="19af0-158">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="19af0-158">Not applicable.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19af0-159">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="19af0-159">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="19af0-160">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="19af0-160">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19af0-161">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="19af0-161">Filter CLSID</span></span></td>
<td><span data-ttu-id="19af0-162">Diesem Filter sind zwei CLSIDs zugeordnet:</span><span class="sxs-lookup"><span data-stu-id="19af0-162">There are two CLSIDs associated with this filter:</span></span>
<ul>
<li><span data-ttu-id="19af0-163">CLSID_VideoMixingRenderer: erstellt VMR-7.</span><span class="sxs-lookup"><span data-stu-id="19af0-163">CLSID_VideoMixingRenderer: Creates the VMR-7.</span></span> <span data-ttu-id="19af0-164">Wenn nicht genügend Systemressourcen vorhanden sind, um VMR-7 zu erstellen, tritt beim Aufrufen von <strong>CoCreateInstance</strong> ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="19af0-164">If there are not enough system resources to create the VMR-7, the call to <strong>CoCreateInstance</strong> fails.</span></span></li>
<li><span data-ttu-id="19af0-165">CLSID_VideoRendererDefault: erstellt VMR-7, wenn Systemressourcen verfügbar sind, oder erstellt andernfalls den alten <a href="video-renderer-filter.md">Videorendererfilter</a> .</span><span class="sxs-lookup"><span data-stu-id="19af0-165">CLSID_VideoRendererDefault: Creates the VMR-7 if system resources are available, or else creates the old <a href="video-renderer-filter.md">Video Renderer</a> filter.</span></span></li>
</ul>
<span data-ttu-id="19af0-166">Verwenden Sie CLSID_VideoMixingRenderer, wenn Sie die spezifischen Funktionen von VMR-7 benötigen.</span><span class="sxs-lookup"><span data-stu-id="19af0-166">Use CLSID_VideoMixingRenderer if you need the specific capabilities of the VMR-7.</span></span> <span data-ttu-id="19af0-167">Andernfalls verwenden Sie CLSID_VideoRendererDefault, was fast sicher ist, dass kein Fehler auftritt, da Sie auf den alten Videorendererfilter zurückgreift.</span><span class="sxs-lookup"><span data-stu-id="19af0-167">Otherwise, use CLSID_VideoRendererDefault, which is almost certain not to fail, because it falls back to the old Video Renderer filter.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19af0-168">CLSID der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="19af0-168">Property Page CLSID</span></span></td>
<td><span data-ttu-id="19af0-169">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="19af0-169">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19af0-170">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="19af0-170">Executable</span></span></td>
<td><span data-ttu-id="19af0-171">Quartz.dll</span><span class="sxs-lookup"><span data-stu-id="19af0-171">Quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19af0-172"><a href="merit.md">Verdienst</a></span><span class="sxs-lookup"><span data-stu-id="19af0-172"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="19af0-173">MERIT_PREFERRED + 1</span><span class="sxs-lookup"><span data-stu-id="19af0-173">MERIT_PREFERRED + 1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19af0-174"><a href="filter-categories.md">Filter Kategorie</a></span><span class="sxs-lookup"><span data-stu-id="19af0-174"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="19af0-175">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="19af0-175">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="19af0-176">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="19af0-176">Remarks</span></span>

<span data-ttu-id="19af0-177">Die Eingabe-PIN macht die **IOverlay** -Schnittstelle nur verfügbar, wenn sich der VMR-7-Filter im Fenstermodus befindet.</span><span class="sxs-lookup"><span data-stu-id="19af0-177">The input pin exposes the **IOverlay** interface only when the VMR-7 filter is in windowed mode.</span></span> <span data-ttu-id="19af0-178">Die einzige **IOverlay** -Methode, die die PIN implementiert, ist **getwindowhandle**, die einer Anwendung das Abrufen eines Handles für das Videofenster des Filters ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="19af0-178">The only **IOverlay** method that the pin implements is **GetWindowHandle**, which enables an application to obtain a handle to the filter's video window.</span></span> <span data-ttu-id="19af0-179">Alle anderen **IOverlay** -Methoden geben E \_ notimpl zurück.</span><span class="sxs-lookup"><span data-stu-id="19af0-179">All other **IOverlay** methods return E\_NOTIMPL.</span></span> <span data-ttu-id="19af0-180">Im fensterlosen Modus erstellt der Filter kein Videofenster, sodass die PIN die Schnittstelle nicht verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="19af0-180">In windowless mode, the filter does not create a video window, so the pin does not expose the interface.</span></span>

<span data-ttu-id="19af0-181">Eine Anwendung kann ein benutzerdefiniertes zuordnerpräsentatorobjekt bereitstellen, das die folgenden Schnittstellen verfügbar macht:</span><span class="sxs-lookup"><span data-stu-id="19af0-181">An application can provide a custom allocator-presenter object that exposes the following interfaces:</span></span>

-   [<span data-ttu-id="19af0-182">**Ivmrimagepresenter**</span><span class="sxs-lookup"><span data-stu-id="19af0-182">**IVMRImagePresenter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter)
-   <span data-ttu-id="19af0-183">[**Ivmrimagepresenterconfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterconfig) (optional)</span><span class="sxs-lookup"><span data-stu-id="19af0-183">[**IVMRImagePresenterConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterconfig) (optional)</span></span>
-   <span data-ttu-id="19af0-184">[**Ivmrmonitorconfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig) (optional)</span><span class="sxs-lookup"><span data-stu-id="19af0-184">[**IVMRMonitorConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig) (optional)</span></span>
-   [<span data-ttu-id="19af0-185">**Ivmrsurfacezucator**</span><span class="sxs-lookup"><span data-stu-id="19af0-185">**IVMRSurfaceAllocator**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator)
-   <span data-ttu-id="19af0-186">[**Ivmrwindowlesscontrol**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) (optional)</span><span class="sxs-lookup"><span data-stu-id="19af0-186">[**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) (optional)</span></span>

<span data-ttu-id="19af0-187">Weitere Informationen zu benutzerdefinierten Zuweiser finden Sie unter [Bereitstellen eines benutzerdefinierten Allocator-Presenter für VMR-7](supplying-a-custom-allocator-presenter-for-vmr-7.md).</span><span class="sxs-lookup"><span data-stu-id="19af0-187">For more information about custom allocator-presenters, see [Supplying a Custom Allocator-Presenter for VMR-7](supplying-a-custom-allocator-presenter-for-vmr-7.md).</span></span>

<span data-ttu-id="19af0-188">Eine Anwendung kann auch einen benutzerdefinierten Plug-in-Compositor bereitstellen, der die folgende Schnittstelle verfügbar macht:</span><span class="sxs-lookup"><span data-stu-id="19af0-188">An application can also provide a custom plug-in compositor that exposes the following interface:</span></span>

-   [<span data-ttu-id="19af0-189">**Ivmrimagecompositor**</span><span class="sxs-lookup"><span data-stu-id="19af0-189">**IVMRImageCompositor**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ivmrimagecompositor)

<span data-ttu-id="19af0-190">Um das VMR mit einem benutzerdefinierten Compositor zu konfigurieren, nennen Sie [**ivmrfilterconfig:: abtimagecompositor**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setimagecompositor).</span><span class="sxs-lookup"><span data-stu-id="19af0-190">To configure the VMR with a custom compositor, call [**IVMRFilterConfig::SetImageCompositor**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setimagecompositor).</span></span>

## <a name="related-topics"></a><span data-ttu-id="19af0-191">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="19af0-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19af0-192">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="19af0-192">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




