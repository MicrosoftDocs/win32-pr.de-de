---
description: VideoMischungsrenderer Filter 9
ms.assetid: 3885cca2-74b1-4066-8ecb-84c9841f9e66
title: VideoMischungsrenderer Filter 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46e20418aad6b9648835665fff98f894eeed1386
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986243"
---
# <a name="video-mixing-renderer-filter-9"></a>VideoMischungsrenderer Filter 9

In DirectX 9 bietet der Filter Video Mixing Renderer 9 (VMR-9) erweiterte Videorenderingfunktionen auf allen plattformen, die von DirectX unterstützt werden. Es ist vollständig in DirectX 9 3D-Funktionen integriert. Beispielsweise können Sie Mithilfe der Direct3D-Pixel-Shader und anderer Effekte problemlos Videos zu Spielen und anderen 3D-Umgebungen hinzufügen oder Videobilder transformieren.

Dieser Filter unterstützt keine Videoports.

Aus Gründen der Abwärtskompatibilität ist VMR-9 nicht der Standardrenderer auf jedem System. Um diesen Filter zu verwenden, fügen Sie ihn explizit dem Filterdiagramm hinzu, und konfigurieren Sie ihn, bevor Sie einen seiner Eingabepins verbinden. VMR-9 verwendet einen eigenen Satz von Schnittstellen, Strukturen und Enumerationen, die nicht immer mit den entsprechenden Datentypen identisch sind, die mit VMR-7 verwendet werden.

VMR-9 unterstützt bis zu 16 Monitore.




| Bezeichnung | Wert |
|--------|-------|
| Filterschnittstellen | VMR-9 unterstützt mehrere verschiedene Renderingmodi. Je nach Renderingmodus werden unterschiedliche Schnittstellen unterstützt:<br /><ul><li>Alle Modi: <a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeinterlaceControl9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></li><li>Renderloser Modus: <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"> <strong>IVMRSurfaceAllocatorNotify9</strong></a></li><li>Fenstermodus: <a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>IBasicVideo</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></li><li>Fensterloser Modus: <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9,</strong></a> <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></li></ul>Rufen Sie zum Festlegen des Renderingmodus <a href="/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode"><strong>IVMRFilterConfig9::SetRenderingMode auf.</strong></a> Weitere Informationen finden Sie unter <a href="vmr-modes-of-operation.md">VMR-Betriebsmodi.</a><br /> | 
| Eingabepin-Medientypen | Die Eingabepins stellen eine Verbindung mit einem beliebigen Typ auf, der von der zugrunde liegenden Videohardware unterstützt wird. | 
| Eingabepinschnittstellen | <a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrvideostreamcontrol9"><strong>IVMRVideoStreamControl9</strong></a> | 
| Ausgabepin-Medientypen | Nicht zutreffend | 
| Ausgabe-PIN-Schnittstellen | Nicht zutreffend | 
| Filtern der CLSID | CLSID_VideoMixingRenderer9 | 
| Eigenschaftenseite CLSID | Nicht zutreffend | 
| Ausführbare Datei | Quartz.dll | 
| <a href="merit.md">Verdienst</a> | MERIT_DO_NOT_USE | 
| <a href="filter-categories.md">Filterkategorie</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Bemerkungen

Eine Anwendung kann ein benutzerdefiniertes Allocator-Presenter-Objekt bereitstellen, das die folgenden Schnittstellen verfügbar macht:

-   [**IVMRImagePresenter9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9)
-   [**IVMRImagePresenterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenterconfig9) (optional)
-   [**IVMRSurfaceAllocator9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9)
-   [**IVMRSurfaceAllocatorEx9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9) (optional)
-   [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) (optional)

Weitere Informationen zu benutzerdefinierten Allocator-Presentern finden Sie unter [Supplying a Custom Allocator-Presenter for VMR-9](supplying-a-custom-allocator-presenter-for-vmr-9.md).

Eine Anwendung kann auch einen benutzerdefinierten Plug-In-Compositor bereitstellen, der die folgende Schnittstelle verfügbar macht:

-   [**IVMRImageCompositor9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagecompositor9)

Rufen Sie ZUM Konfigurieren der VMR mit einem benutzerdefinierten Compositor [**IVMRFilterConfig9::SetImageCompositor auf.**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setimagecompositor)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[Verwenden des Renderers für das Mischen von Videos](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 




