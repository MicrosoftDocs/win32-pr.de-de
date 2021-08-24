---
description: Schnittstellen für Videorendering und Überlagerung
ms.assetid: e4d4e456-61fb-492b-b817-30629681e270
title: Schnittstellen für Videorendering und Überlagerung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d40a8fcfa2d5e848c0e33fda14828c868cead28b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482576"
---
# <a name="interfaces-for-video-rendering-and-overlay"></a>Schnittstellen für Videorendering und Überlagerung

Diese Schnittstellen unterstützen die Anwendungssteuerung über das Videorendering. Beachten Sie, dass einige dieser Schnittstellen jetzt veraltet sind, da der Filter Video Mixing Renderer ein besseres Rendering- und Überlagerungssteuerelement bietet.




| Schnittstelle | BESCHREIBUNG | 
|-----------|-------------|
| <a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder</strong></a> | Ermöglicht den Zugriff auf Untertitelinformationen und -einstellungen. | 
| <a href="/windows/desktop/api/Strmif/nn-strmif-iamoverlayfx"><strong>IAMOverlayFX</strong></a> | Anwenden von Überlagerungseffekten auf die Videooberfläche. (Veraltet.) | 
| <a href="/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties"><strong>IAMVideoDecimationProperties</strong></a> | Steuern Sie, wie DirectShow ein Videobild skaliert, wenn das Videofenster kleiner als die native Größe des Videos ist. (Veraltet.) | 
| <a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a> | Festlegen von Videoeigenschaften. | 
| <a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>IDDrawExclModeVideo</strong></a> | Rendern von Videos im exklusiven Vollbildmodus Microsoft DirectDraw (Veraltet.) | 
| <a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideocallback"><strong>IDDrawExclModeVideoCallback</strong></a> | Rückrufschnittstelle, um Benachrichtigungen zu Änderungen an der Überlagerungsposition, -größe und -sichtbarkeit zu erhalten. (Veraltet.) | 
| <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-idirectdrawvideo"><strong>IDirectDrawVideo</strong></a> | Deaktivieren Sie die angegebenen DirectDraw-Funktionen. (Veraltet.) | 
| <a href="/previous-versions/windows/desktop/api/Amstream/nn-amstream-idirectdrawmediasample"><strong>IDirectDrawMediaSample</strong></a> | Greifen Sie auf eine DirectDraw-Oberfläche zu, die vom <a href="overlay-mixer-filter.md">Filter Overlay Mixer</a> zugeordnet wird. (Veraltet.) | 
| <a href="/previous-versions/windows/desktop/api/Mixerocx/nn-mixerocx-imixerocx"><strong>IMixerOCX</strong></a> | Wird auf dem Overlay-Mixer implementiert. Ermöglicht fensterlosen Clients wie ActiveX® Steuerelementen, Eigenschaften des Videorechtecks abzurufen und festzulegen und den Filter von Ereignissen zu empfehlen. | 
| <a href="/previous-versions/windows/desktop/api/mixerocx/nn-mixerocx-imixerocxnotify"><strong>IMixerOCXNotify</strong></a> | Wird von fensterlosen Clients implementiert und vom Overlay-Mixer aufgerufen, um Benachrichtigungen über Ereignisse zu senden, die sich auf das Videoanzeigerechteck auswirken. | 
| <a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2"><strong>IMixerPinConfig2</strong></a> | Legen Sie Videofarbsteuerelemente auf dem Overlay-Mixer Filter fest, wenn Sie mehrere Videostreams kombinieren. (Veraltet.) | 
| <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a> | Fragen Sie einen Videorenderer nach Leistungsinformationen ab. | 
| <a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a> | Festlegen der Eigenschaften des Videofensters. | 
| <ul><li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeinterlaceControl9</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagecompositor9"><strong>IVMRImageCompositor9</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9"><strong>IVMRImagePresenter9</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenterconfig9"><strong>IVMRImagePresenterConfig9</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurface9"><strong>IVMRSurface9</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9"><strong>IVMRSurfaceAllocator9</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9"><strong>IVMRSurfaceAllocatorEx9</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"><strong>IVMRSurfaceAllocatorNotify9</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></li></ul> | Video Mixing Renderer 9-Schnittstellen. | 
| <ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmraspectratiocontrol"><strong>IVMRAspectRatioControl</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol"><strong>IVMRDeinterlaceControl</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig"><strong>IVMRFilterConfig</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagecompositor"><strong>IVMRImageCompositor</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter"><strong>IVMRImagePresenter</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterconfig"><strong>IVMRImagePresenterConfig</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap"><strong>IVMRMixerBitmap</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol"><strong>IVMRMixerControl</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator"><strong>IVMRSurfaceAllocator</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify"><strong>IVMRSurfaceAllocatorNotify</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol"><strong>IVMRWindowlessControl</strong></a></li></ul> | Video Mixing Renderer 7-Schnittstellen. | 




 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des Videomischungsrenderers](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 



