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
# <a name="interfaces-for-video-rendering-and-overlay"></a>Schnittstellen für Video Rendering und Overlay

Diese Schnittstellen unterstützen die Anwendungssteuerung des Video Rendering. Beachten Sie, dass einige dieser Schnittstellen nun veraltet sind, da der Filter für den Video Mischungs Renderer ein höheres Rendering und Überlagerungs Steuerelement bereitstellt.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Schnittstelle</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder</strong></a></td>
<td>Ermöglicht den Zugriff auf geschlossene Informationen und Einstellungen.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamoverlayfx"><strong>Iamoverlayfx</strong></a></td>
<td>Anwenden von Überlagerungs Effekten auf die Video Oberfläche. (Veraltet.)</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties"><strong>Iamvideodecimationproperties</strong></a></td>
<td>Steuern Sie, wie DirectShow ein Video Bild skaliert, wenn das Videofenster kleiner als die systemeigene Größe des Videos ist. (Veraltet.)</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a></td>
<td>Legen Sie die Videoeigenschaften fest.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>Iddrawexclmodevideo</strong></a></td>
<td>Rendervideo in Microsoft DirectDraw exklusiv im Vollbildmodus. (Veraltet.)</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideocallback"><strong>Iddrawexclmodevideocallback</strong></a></td>
<td>Rückruf Schnittstelle zum Empfangen von Benachrichtigungen zu Änderungen an der Position, Größe und Sichtbarkeit der Überlagerung. (Veraltet.)</td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-idirectdrawvideo"><strong>Idirectdrawvideo</strong></a></td>
<td>Deaktivieren Sie die angegebenen DirectDraw-Funktionen. (Veraltet.)</td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/api/Amstream/nn-amstream-idirectdrawmediasample"><strong>Idirectdrawmediasample</strong></a></td>
<td>Greifen Sie auf eine DirectDraw-Oberfläche zu, die durch den <a href="overlay-mixer-filter.md">Überlagerungs</a> Filter (Veraltet.)</td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/Mixerocx/nn-mixerocx-imixerocx"><strong>Imixerocx</strong></a></td>
<td>Wird auf dem Überlagerungs Mixer implementiert. Ermöglicht fensterlosen Clients, wie z. b. ActiveX-® Steuerelemente, Eigenschaften des Video Rechtecks zu erhalten und festzulegen und den Ereignis Filter zu empfehlen.</td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/api/mixerocx/nn-mixerocx-imixerocxnotify"><strong>Imixerocxnotify</strong></a></td>
<td>Wird von fensterlosen Clients implementiert und vom Overlay-Mixer aufgerufen, um Benachrichtigungen über Ereignisse zu senden, die das Videoanzeige Rechteck beeinflussen.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2"><strong>IMixerPinConfig2</strong></a></td>
<td>Legen Sie bei der Mischung mehrerer Videostreams auf dem Filter für den Überlagerungs Filter Farb Steuerelemente fest. (Veraltet.)</td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>Iqualprop</strong></a></td>
<td>Fragt einen Videorenderer nach Leistungsinformationen ab.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a></td>
<td>Festlegen von Videofenster Eigenschaften.</td>
</tr>
<tr class="even">
<td><ul>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeinterlaceControl9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagecompositor9"><strong>IVMRImageCompositor9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9"><strong>IVMRImagePresenter9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenterconfig9"><strong>IVMRImagePresenterConfig9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurface9"><strong>IVMRSurface9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9"><strong>IVMRSurfaceAllocator9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9"><strong>IVMRSurfaceAllocatorEx9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"><strong>IVMRSurfaceAllocatorNotify9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></li>
</ul></td>
<td>Video Mischung Renderer 9-Schnittstellen.</td>
</tr>
<tr class="odd">
<td><ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmraspectratiocontrol"><strong>Ivmraspectratiocontrol</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol"><strong>Ivmrdeinterlacecontrol</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig"><strong>Ivmrfilterconfig</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagecompositor"><strong>Ivmrimagecompositor</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter"><strong>Ivmrimagepresenter</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterconfig"><strong>Ivmrimagepresenterconfig</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap"><strong>Ivmrmixerbitmap</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol"><strong>Ivmrmixercontrol</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator"><strong>Ivmrsurfacezucator</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify"><strong>Ivmrsurfacezuweisung</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol"><strong>Ivmrwindowlesscontrol</strong></a></li>
</ul></td>
<td>Video Mischung Renderer 7-Schnittstellen.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des Video Mischungs Renderers](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 



