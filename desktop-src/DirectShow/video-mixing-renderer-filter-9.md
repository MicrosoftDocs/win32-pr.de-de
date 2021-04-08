---
description: Video Mischungs-Renderer Filter 9
ms.assetid: 3885cca2-74b1-4066-8ecb-84c9841f9e66
title: Video Mischungs-Renderer Filter 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8b2576f8c5f1b0f262b83141c14ce4836eecb4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757674"
---
# <a name="video-mixing-renderer-filter-9"></a><span data-ttu-id="3d970-103">Video Mischungs-Renderer Filter 9</span><span class="sxs-lookup"><span data-stu-id="3d970-103">Video Mixing Renderer Filter 9</span></span>

<span data-ttu-id="3d970-104">In DirectX 9 bietet der Filter Video Mischungs-Renderer 9 (VMR-9) erweiterte videorenderingfunktionen auf allen Plattformen, die von DirectX unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="3d970-104">In DirectX 9, the Video Mixing Renderer 9 (VMR-9) filter offers advanced video rendering capabilities on all platforms supported by DirectX.</span></span> <span data-ttu-id="3d970-105">Es ist vollständig in DirectX 9 3D-Funktionen integriert.</span><span class="sxs-lookup"><span data-stu-id="3d970-105">It is fully integrated with DirectX 9 3D capabilities.</span></span> <span data-ttu-id="3d970-106">Beispielsweise können Sie problemlos Videos zu spielen und anderen 3D-Umgebungen hinzufügen oder Videobilder mithilfe der Direct3D-Pixel-Shader und anderer Effekte transformieren.</span><span class="sxs-lookup"><span data-stu-id="3d970-106">For example, that you can easily add video to games and other 3D environments or transform video images using the Direct3D pixel shaders and other effects.</span></span>

<span data-ttu-id="3d970-107">Dieser Filter unterstützt keine Videoports.</span><span class="sxs-lookup"><span data-stu-id="3d970-107">This filter does not support video ports.</span></span>

<span data-ttu-id="3d970-108">Um die Abwärtskompatibilität zu gewährleisten, ist VMR-9 nicht der Standard-Renderer auf einem System.</span><span class="sxs-lookup"><span data-stu-id="3d970-108">To maintain backward compatibility, the VMR-9 is not the default renderer on any system.</span></span> <span data-ttu-id="3d970-109">Wenn Sie diesen Filter verwenden möchten, fügen Sie ihn explizit dem Filter Diagramm hinzu, und konfigurieren Sie ihn, bevor Sie seine Eingabe Pins verbinden.</span><span class="sxs-lookup"><span data-stu-id="3d970-109">To use this filter, add it to the filter graph explicitly and configure it before connecting any of its input pins.</span></span> <span data-ttu-id="3d970-110">VMR-9 verwendet einen eigenen Satz von Schnittstellen, Strukturen und Enumerationen, die nicht immer mit den entsprechenden Datentypen identisch sind, die mit VMR-7 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3d970-110">The VMR-9 uses its own set of interfaces, structures, and enumerations, which are not always identical to the corresponding data types used with the VMR-7.</span></span>

<span data-ttu-id="3d970-111">VMR-9 unterstützt bis zu 16 Monitore.</span><span class="sxs-lookup"><span data-stu-id="3d970-111">The VMR-9 supports up to 16 monitors.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3d970-112">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="3d970-112">Filter Interfaces</span></span></td>
<td><span data-ttu-id="3d970-113">VMR-9 unterstützt mehrere verschiedene Renderingmodi.</span><span class="sxs-lookup"><span data-stu-id="3d970-113">The VMR-9 supports several distinct rendering modes.</span></span> <span data-ttu-id="3d970-114">Sie unterstützt abhängig vom Renderingmodus einen anderen Satz von Schnittstellen:</span><span class="sxs-lookup"><span data-stu-id="3d970-114">It supports a different set of interfaces depending on the rendering mode:</span></span><br/>
<ul>
<li><span data-ttu-id="3d970-115">Alle Modi: <a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>iamcertifiedoutputprotection</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>iamfilterfehlflags</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>ibasefilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>imediaposition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>imediaseeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a>, <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>iqualprop</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeinterlaceControl9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d970-115">All modes: <a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeinterlaceControl9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></span></span></li>
<li><span data-ttu-id="3d970-116">Renderless-Modus: <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"> <strong>IVMRSurfaceAllocatorNotify9</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d970-116">Renderless mode: <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"><strong>IVMRSurfaceAllocatorNotify9</strong></a></span></span></li>
<li><span data-ttu-id="3d970-117">Fenstermodus: <a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>ibasicvideo</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d970-117">Windowed mode: <a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>IBasicVideo</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></span></span></li>
<li><span data-ttu-id="3d970-118">Fensterloser Modus: <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d970-118">Windowless mode: <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></span></span></li>
</ul>
<span data-ttu-id="3d970-119">Um den Renderingmodus festzulegen, nennen Sie <a href="/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode"><strong>IVMRFilterConfig9:: setrenderingmode</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="3d970-119">To set the rendering mode, call <a href="/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode"><strong>IVMRFilterConfig9::SetRenderingMode</strong></a>.</span></span> <span data-ttu-id="3d970-120">Weitere Informationen finden Sie unter <a href="vmr-modes-of-operation.md">VMR-Betriebsmodi</a>.</span><span class="sxs-lookup"><span data-stu-id="3d970-120">For more information, see <a href="vmr-modes-of-operation.md">VMR Modes of Operation</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d970-121">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="3d970-121">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="3d970-122">Die Eingabe Pins stellen eine Verbindung mit jedem Typ her, der von der zugrunde liegenden Video Hardware unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="3d970-122">The input pins will connect with any type supported by the underlying video hardware.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d970-123">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="3d970-123">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="3d970-124"><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>Iamvideoaccelerator</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>ipinconnection</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrvideostreamcontrol9"><strong>IVMRVideoStreamControl9</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d970-124"><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrvideostreamcontrol9"><strong>IVMRVideoStreamControl9</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d970-125">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="3d970-125">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="3d970-126">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="3d970-126">Not applicable.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d970-127">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="3d970-127">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="3d970-128">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="3d970-128">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d970-129">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="3d970-129">Filter CLSID</span></span></td>
<td><span data-ttu-id="3d970-130">CLSID_VideoMixingRenderer9</span><span class="sxs-lookup"><span data-stu-id="3d970-130">CLSID_VideoMixingRenderer9</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d970-131">CLSID der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="3d970-131">Property Page CLSID</span></span></td>
<td><span data-ttu-id="3d970-132">–</span><span class="sxs-lookup"><span data-stu-id="3d970-132">N/A</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d970-133">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="3d970-133">Executable</span></span></td>
<td><span data-ttu-id="3d970-134">Quartz.dll</span><span class="sxs-lookup"><span data-stu-id="3d970-134">Quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d970-135"><a href="merit.md">Verdienst</a></span><span class="sxs-lookup"><span data-stu-id="3d970-135"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="3d970-136">MERIT_DO_NOT_USE</span><span class="sxs-lookup"><span data-stu-id="3d970-136">MERIT_DO_NOT_USE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d970-137"><a href="filter-categories.md">Filter Kategorie</a></span><span class="sxs-lookup"><span data-stu-id="3d970-137"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="3d970-138">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="3d970-138">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="3d970-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3d970-139">Remarks</span></span>

<span data-ttu-id="3d970-140">Eine Anwendung kann ein benutzerdefiniertes zuordnerpräsentatorobjekt bereitstellen, das die folgenden Schnittstellen verfügbar macht:</span><span class="sxs-lookup"><span data-stu-id="3d970-140">An application can provide a custom allocator-presenter object that exposes the following interfaces:</span></span>

-   [<span data-ttu-id="3d970-141">**IVMRImagePresenter9**</span><span class="sxs-lookup"><span data-stu-id="3d970-141">**IVMRImagePresenter9**</span></span>](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9)
-   <span data-ttu-id="3d970-142">[**IVMRImagePresenterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenterconfig9) (optional)</span><span class="sxs-lookup"><span data-stu-id="3d970-142">[**IVMRImagePresenterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenterconfig9) (optional)</span></span>
-   [<span data-ttu-id="3d970-143">**IVMRSurfaceAllocator9**</span><span class="sxs-lookup"><span data-stu-id="3d970-143">**IVMRSurfaceAllocator9**</span></span>](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9)
-   <span data-ttu-id="3d970-144">[**IVMRSurfaceAllocatorEx9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9) (optional)</span><span class="sxs-lookup"><span data-stu-id="3d970-144">[**IVMRSurfaceAllocatorEx9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9) (optional)</span></span>
-   <span data-ttu-id="3d970-145">[**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) (optional)</span><span class="sxs-lookup"><span data-stu-id="3d970-145">[**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) (optional)</span></span>

<span data-ttu-id="3d970-146">Weitere Informationen zu benutzerdefinierten Zuweiser finden Sie unter [Bereitstellen eines benutzerdefinierten Allocator-Presenter für VMR-9](supplying-a-custom-allocator-presenter-for-vmr-9.md).</span><span class="sxs-lookup"><span data-stu-id="3d970-146">For more information about custom allocator-presenters, see [Supplying a Custom Allocator-Presenter for VMR-9](supplying-a-custom-allocator-presenter-for-vmr-9.md).</span></span>

<span data-ttu-id="3d970-147">Eine Anwendung kann auch einen benutzerdefinierten Plug-in-Compositor bereitstellen, der die folgende Schnittstelle verfügbar macht:</span><span class="sxs-lookup"><span data-stu-id="3d970-147">An application can also provide a custom plug-in compositor that exposes the following interface:</span></span>

-   [<span data-ttu-id="3d970-148">**IVMRImageCompositor9**</span><span class="sxs-lookup"><span data-stu-id="3d970-148">**IVMRImageCompositor9**</span></span>](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagecompositor9)

<span data-ttu-id="3d970-149">Um das VMR mit einem benutzerdefinierten Compositor zu konfigurieren, müssen Sie [**IVMRFilterConfig9:: abtimagecompositor**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setimagecompositor)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3d970-149">To configure the VMR with a custom compositor, call [**IVMRFilterConfig9::SetImageCompositor**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setimagecompositor).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3d970-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3d970-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d970-151">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="3d970-151">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="3d970-152">Verwenden des Video Mischungs Renderers</span><span class="sxs-lookup"><span data-stu-id="3d970-152">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 




