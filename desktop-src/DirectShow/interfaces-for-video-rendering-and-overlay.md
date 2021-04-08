---
description: Schnittstellen für Video Rendering und Overlay
ms.assetid: e4d4e456-61fb-492b-b817-30629681e270
title: Schnittstellen für Video Rendering und Overlay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cfa8a94765671e38c48418d37b929215e84b2fe
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747104"
---
# <a name="interfaces-for-video-rendering-and-overlay"></a><span data-ttu-id="0a27c-103">Schnittstellen für Video Rendering und Overlay</span><span class="sxs-lookup"><span data-stu-id="0a27c-103">Interfaces for Video Rendering and Overlay</span></span>

<span data-ttu-id="0a27c-104">Diese Schnittstellen unterstützen die Anwendungssteuerung des Video Rendering.</span><span class="sxs-lookup"><span data-stu-id="0a27c-104">These interfaces support application control over video rendering.</span></span> <span data-ttu-id="0a27c-105">Beachten Sie, dass einige dieser Schnittstellen nun veraltet sind, da der Filter für den Video Mischungs Renderer ein höheres Rendering und Überlagerungs Steuerelement bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="0a27c-105">Note that some of these interfaces are now deprecated, because the Video Mixing Renderer filter provides superior rendering and overlay control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0a27c-106">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="0a27c-106">Interface</span></span></th>
<th><span data-ttu-id="0a27c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0a27c-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0a27c-108"><a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a27c-108"><a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder</strong></a></span></span></td>
<td><span data-ttu-id="0a27c-109">Ermöglicht den Zugriff auf geschlossene Informationen und Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="0a27c-109">Provides access to closed-captioned information and settings.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a27c-110"><a href="/windows/desktop/api/Strmif/nn-strmif-iamoverlayfx"><strong>Iamoverlayfx</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a27c-110"><a href="/windows/desktop/api/Strmif/nn-strmif-iamoverlayfx"><strong>IAMOverlayFX</strong></a></span></span></td>
<td><span data-ttu-id="0a27c-111">Anwenden von Überlagerungs Effekten auf die Video Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="0a27c-111">Apply overlay effects to the video surface.</span></span> <span data-ttu-id="0a27c-112">(Veraltet.)</span><span class="sxs-lookup"><span data-stu-id="0a27c-112">(Deprecated.)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0a27c-113"><a href="/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties"><strong>Iamvideodecimationproperties</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a27c-113"><a href="/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties"><strong>IAMVideoDecimationProperties</strong></a></span></span></td>
<td><span data-ttu-id="0a27c-114">Steuern Sie, wie DirectShow ein Video Bild skaliert, wenn das Videofenster kleiner als die systemeigene Größe des Videos ist.</span><span class="sxs-lookup"><span data-stu-id="0a27c-114">Control how DirectShow scales a video image if the video window is smaller than the native size of the video.</span></span> <span data-ttu-id="0a27c-115">(Veraltet.)</span><span class="sxs-lookup"><span data-stu-id="0a27c-115">(Deprecated.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a27c-116"><a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a27c-116"><a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a></span></span></td>
<td><span data-ttu-id="0a27c-117">Legen Sie die Videoeigenschaften fest.</span><span class="sxs-lookup"><span data-stu-id="0a27c-117">Set video properties.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0a27c-118"><a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>Iddrawexclmodevideo</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a27c-118"><a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>IDDrawExclModeVideo</strong></a></span></span></td>
<td><span data-ttu-id="0a27c-119">Rendervideo in Microsoft DirectDraw exklusiv im Vollbildmodus.</span><span class="sxs-lookup"><span data-stu-id="0a27c-119">Render video in Microsoft DirectDraw exclusive full-screen mode.</span></span> <span data-ttu-id="0a27c-120">(Veraltet.)</span><span class="sxs-lookup"><span data-stu-id="0a27c-120">(Deprecated.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a27c-121"><a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideocallback"><strong>Iddrawexclmodevideocallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a27c-121"><a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideocallback"><strong>IDDrawExclModeVideoCallback</strong></a></span></span></td>
<td><span data-ttu-id="0a27c-122">Rückruf Schnittstelle zum Empfangen von Benachrichtigungen zu Änderungen an der Position, Größe und Sichtbarkeit der Überlagerung.</span><span class="sxs-lookup"><span data-stu-id="0a27c-122">Callback interface to receive notification about changes to the overlay position, size, and visibility.</span></span> <span data-ttu-id="0a27c-123">(Veraltet.)</span><span class="sxs-lookup"><span data-stu-id="0a27c-123">(Deprecated.)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0a27c-124"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-idirectdrawvideo"><strong>Idirectdrawvideo</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a27c-124"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-idirectdrawvideo"><strong>IDirectDrawVideo</strong></a></span></span></td>
<td><span data-ttu-id="0a27c-125">Deaktivieren Sie die angegebenen DirectDraw-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="0a27c-125">Disable specified DirectDraw capabilities.</span></span> <span data-ttu-id="0a27c-126">(Veraltet.)</span><span class="sxs-lookup"><span data-stu-id="0a27c-126">(Deprecated.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a27c-127"><a href="/previous-versions/windows/desktop/api/Amstream/nn-amstream-idirectdrawmediasample"><strong>Idirectdrawmediasample</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a27c-127"><a href="/previous-versions/windows/desktop/api/Amstream/nn-amstream-idirectdrawmediasample"><strong>IDirectDrawMediaSample</strong></a></span></span></td>
<td><span data-ttu-id="0a27c-128">Greifen Sie auf eine DirectDraw-Oberfläche zu, die durch den <a href="overlay-mixer-filter.md">Überlagerungs</a> Filter (Veraltet.)</span><span class="sxs-lookup"><span data-stu-id="0a27c-128">Access a DirectDraw surface allocated by the <a href="overlay-mixer-filter.md">Overlay Mixer</a> filter.(Deprecated.)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0a27c-129"><a href="/previous-versions/windows/desktop/api/Mixerocx/nn-mixerocx-imixerocx"><strong>Imixerocx</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a27c-129"><a href="/previous-versions/windows/desktop/api/Mixerocx/nn-mixerocx-imixerocx"><strong>IMixerOCX</strong></a></span></span></td>
<td><span data-ttu-id="0a27c-130">Wird auf dem Überlagerungs Mixer implementiert.</span><span class="sxs-lookup"><span data-stu-id="0a27c-130">Implemented on the Overlay Mixer.</span></span> <span data-ttu-id="0a27c-131">Ermöglicht fensterlosen Clients, wie z. b. ActiveX-® Steuerelemente, Eigenschaften des Video Rechtecks zu erhalten und festzulegen und den Ereignis Filter zu empfehlen.</span><span class="sxs-lookup"><span data-stu-id="0a27c-131">Enables windowless clients such as ActiveX® controls to get and set properties of the video rectangle and advise the filter of events.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a27c-132"><a href="/previous-versions/windows/desktop/api/mixerocx/nn-mixerocx-imixerocxnotify"><strong>Imixerocxnotify</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a27c-132"><a href="/previous-versions/windows/desktop/api/mixerocx/nn-mixerocx-imixerocxnotify"><strong>IMixerOCXNotify</strong></a></span></span></td>
<td><span data-ttu-id="0a27c-133">Wird von fensterlosen Clients implementiert und vom Overlay-Mixer aufgerufen, um Benachrichtigungen über Ereignisse zu senden, die das Videoanzeige Rechteck beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="0a27c-133">Implemented by windowless clients and called by the Overlay Mixer to send notifications of events affecting the video display rectangle.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0a27c-134"><a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2"><strong>IMixerPinConfig2</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a27c-134"><a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2"><strong>IMixerPinConfig2</strong></a></span></span></td>
<td><span data-ttu-id="0a27c-135">Legen Sie bei der Mischung mehrerer Videostreams auf dem Filter für den Überlagerungs Filter Farb Steuerelemente fest.</span><span class="sxs-lookup"><span data-stu-id="0a27c-135">Set video color controls on the Overlay Mixer filter when mixing multiple video streams.</span></span> <span data-ttu-id="0a27c-136">(Veraltet.)</span><span class="sxs-lookup"><span data-stu-id="0a27c-136">(Deprecated.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a27c-137"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>Iqualprop</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a27c-137"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></span></span></td>
<td><span data-ttu-id="0a27c-138">Fragt einen Videorenderer nach Leistungsinformationen ab.</span><span class="sxs-lookup"><span data-stu-id="0a27c-138">Query a video renderer for performance information.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0a27c-139"><a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a27c-139"><a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a></span></span></td>
<td><span data-ttu-id="0a27c-140">Festlegen von Videofenster Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0a27c-140">Set video window properties.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="0a27c-141"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a27c-141"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9</strong></a></span></span></li>
<li><span data-ttu-id="0a27c-142"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeinterlaceControl9</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a27c-142"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeinterlaceControl9</strong></a></span></span></li>
<li><span data-ttu-id="0a27c-143"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a27c-143"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9</strong></a></span></span></li>
<li><span data-ttu-id="0a27c-144"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagecompositor9"><strong>IVMRImageCompositor9</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a27c-144"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagecompositor9"><strong>IVMRImageCompositor9</strong></a></span></span></li>
<li><span data-ttu-id="0a27c-145"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9"><strong>IVMRImagePresenter9</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a27c-145"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9"><strong>IVMRImagePresenter9</strong></a></span></span></li>
<li><span data-ttu-id="0a27c-146"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenterconfig9"><strong>IVMRImagePresenterConfig9</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a27c-146"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenterconfig9"><strong>IVMRImagePresenterConfig9</strong></a></span></span></li>
<li><span data-ttu-id="0a27c-147"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a27c-147"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9</strong></a></span></span></li>
<li><span data-ttu-id="0a27c-148"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a27c-148"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></span></span></li>
<li><span data-ttu-id="0a27c-149"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a27c-149"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></span></span></li>
<li><span data-ttu-id="0a27c-150"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurface9"><strong>IVMRSurface9</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a27c-150"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurface9"><strong>IVMRSurface9</strong></a></span></span></li>
<li><span data-ttu-id="0a27c-151"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9"><strong>IVMRSurfaceAllocator9</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a27c-151"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9"><strong>IVMRSurfaceAllocator9</strong></a></span></span></li>
<li><span data-ttu-id="0a27c-152"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9"><strong>IVMRSurfaceAllocatorEx9</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a27c-152"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9"><strong>IVMRSurfaceAllocatorEx9</strong></a></span></span></li>
<li><span data-ttu-id="0a27c-153"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"><strong>IVMRSurfaceAllocatorNotify9</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a27c-153"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"><strong>IVMRSurfaceAllocatorNotify9</strong></a></span></span></li>
<li><span data-ttu-id="0a27c-154"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a27c-154"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="0a27c-155">Video Mischung Renderer 9-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="0a27c-155">Video Mixing Renderer 9 interfaces.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="0a27c-156"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmraspectratiocontrol"><strong>Ivmraspectratiocontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a27c-156"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmraspectratiocontrol"><strong>IVMRAspectRatioControl</strong></a></span></span></li>
<li><span data-ttu-id="0a27c-157"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol"><strong>Ivmrdeinterlacecontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a27c-157"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol"><strong>IVMRDeinterlaceControl</strong></a></span></span></li>
<li><span data-ttu-id="0a27c-158"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig"><strong>Ivmrfilterconfig</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a27c-158"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig"><strong>IVMRFilterConfig</strong></a></span></span></li>
<li><span data-ttu-id="0a27c-159"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagecompositor"><strong>Ivmrimagecompositor</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a27c-159"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagecompositor"><strong>IVMRImageCompositor</strong></a></span></span></li>
<li><span data-ttu-id="0a27c-160"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter"><strong>Ivmrimagepresenter</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a27c-160"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter"><strong>IVMRImagePresenter</strong></a></span></span></li>
<li><span data-ttu-id="0a27c-161"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterconfig"><strong>Ivmrimagepresenterconfig</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a27c-161"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterconfig"><strong>IVMRImagePresenterConfig</strong></a></span></span></li>
<li><span data-ttu-id="0a27c-162"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap"><strong>Ivmrmixerbitmap</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a27c-162"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap"><strong>IVMRMixerBitmap</strong></a></span></span></li>
<li><span data-ttu-id="0a27c-163"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol"><strong>Ivmrmixercontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a27c-163"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol"><strong>IVMRMixerControl</strong></a></span></span></li>
<li><span data-ttu-id="0a27c-164"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator"><strong>Ivmrsurfacezucator</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a27c-164"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator"><strong>IVMRSurfaceAllocator</strong></a></span></span></li>
<li><span data-ttu-id="0a27c-165"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify"><strong>Ivmrsurfacezuweisung</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a27c-165"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify"><strong>IVMRSurfaceAllocatorNotify</strong></a></span></span></li>
<li><span data-ttu-id="0a27c-166"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol"><strong>Ivmrwindowlesscontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a27c-166"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol"><strong>IVMRWindowlessControl</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="0a27c-167">Video Mischung Renderer 7-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="0a27c-167">Video Mixing Renderer 7 interfaces.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="0a27c-168">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0a27c-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a27c-169">Verwenden des Video Mischungs Renderers</span><span class="sxs-lookup"><span data-stu-id="0a27c-169">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 



