---
description: VideoMischungsrenderer Filter 7
ms.assetid: c83e6c50-76f2-4aeb-944b-5b244c6bf776
title: VideoMischungsrenderer Filter 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ac39dfeab90fe97085c97b3a767f06d348a0f02
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466037"
---
# <a name="video-mixing-renderer-filter-7"></a>VideoMischungsrenderer Filter 7

Dieses Thema gilt für Windows XP oder höher.

In Windows XP und höher ist der Video Mixing Renderer 7 (VMR-7) der Standardvideorenderer. Sie wird VMR-7 genannt, da intern DirectDraw 7 verwendet wird. In DirectX 9 ist ein ähnlicher, aber separater Filter, VMR-9, für die Weiterverteilung auf Nicht-XP-Systemen verfügbar. VMR-9 verwendet Direct3D 9.

> [!Note]  
> Die VMR ist auf Windows XP und höher verfügbar. Sie ist nicht über directX redistributable oder frühere Versionen von Windows. In den meisten Szenarien sollten Anwendungen den [Video Mixing Renderer 9 verwenden.](video-mixing-renderer-filter-9.md)

 

Zu den Features der VMR gehören:

-   Echte Alphamischung von bis zu 16 Eingabestreams
-   Zugriff auf das zusammengesetzte Bild, bevor es gerendert wird
-   Ein Plug-In-Modell, mit dem Drittanbieter benutzerdefinierte Videoeffekte implementieren können.
-   Unterstützung für bis zu 15 Monitore.

Beim Erstellen von Diagrammen auf Windows XP und höher verwendet der Filter-Graph-Manager nicht die älteren Filter Videorenderer oder Overlay Mixer, es sei denn, die Anwendung erstellt sie explizit und fügt sie dem Diagramm hinzu.

Weitere Informationen finden Sie unter [Using the Video Mixing Renderer](using-the-video-mixing-renderer.md).




| | | Filtern von Schnittstellen | Alle Modi:<ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></li><li><a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a></li><li><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmraspectratiocontrol"><strong>IVMRAspectRatioControl</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol"><strong>IVMRDeinterlaceControl</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig"><strong>IVMRFilterConfig</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap"><strong>IVMRMixerBitmap</strong></a></li></ul>Fenstermodus:<br /><ul><li><a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>IBasicVideo</strong></a></li><li><a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a></li><li><a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>IVMRMonitorConfig</strong></a></li></ul>Fensterloser Modus:<br /><ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol"><strong>IVMRWindowlessControl</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>IVMRMonitorConfig</strong></a></li></ul>Renderloser Modus:<br /><ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify"><strong>IVMRSurfaceAllocatorNotify</strong></a></li></ul>Mixer Modus:<br /><ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol"><strong>IVMRMixerControl</strong></a></li></ul>Informationen zu den verschiedenen VMR-7-Modi finden Sie unter <a href="vmr-modes-of-operation.md">VMR-Betriebsmodi.</a><br /> | | Eingabepin-Medientypen | Haupttyp: MEDIATYPE_VideoSubtype: Abhängig von der Grafikhardware. Muss ein unkomprimiertes Video sein.<br /> | | Eingabepinschnittstellen | <ul><li><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a> (siehe Hinweise)</li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrvideostreamcontrol"><strong>IVMRVideoStreamControl</strong></a></li></ul> | | Ausgabepin-Medientypen | Nicht zutreffend. | | Ausgabepinschnittstellen | Nicht zutreffend. | | Filtern von CLSID-| Diesem Filter sind zwei CLSIDs zugeordnet:<ul><li>CLSID_VideoMixingRenderer: Erstellt VMR-7. Wenn nicht genügend Systemressourcen zum Erstellen von VMR-7 vorhanden sind, schlägt der Aufruf von <strong>CoCreateInstance</strong> fehl.</li><li>CLSID_VideoRendererDefault: Erstellt VMR-7, wenn Systemressourcen verfügbar sind, oder erstellt den alten <a href="video-renderer-filter.md">Videorendererfilter.</a></li></ul>Verwenden CLSID_VideoMixingRenderer, wenn Sie die spezifischen Funktionen von VMR-7 benötigen. Verwenden Sie andernfalls CLSID_VideoRendererDefault, was fast sicher ist, dass kein Fehler vorfällt, da er auf den alten Videorendererfilter zurückfällt.<br /> | | CLSID-Eigenschaftsseite | Nicht zutreffend. | | Ausführbare | Quartz.dll | | <a href="merit.md">Leistungs-|</a> MERIT_PREFERRED + 1 | | <a href="filter-categories.md">Filterkategorie-|</a> CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Hinweise

Der Eingabepin macht die **IOverlay-Schnittstelle** nur verfügbar, wenn sich der VMR-7-Filter im Fenstermodus befindet. Die einzige **IOverlay-Methode,** die der Pin implementiert, ist **GetWindowHandle.** Dadurch kann eine Anwendung ein Handle für das Videofenster des Filters abrufen. Alle anderen **IOverlay-Methoden** geben E \_ NOTIMPL zurück. Im fensterlosen Modus erstellt der Filter kein Videofenster, sodass die Stecknadel die Schnittstelle nicht verfügbar macht.

Eine Anwendung kann ein benutzerdefiniertes Allocator-Presenter-Objekt bereitstellen, das die folgenden Schnittstellen verfügbar macht:

-   [**IVMRImagePresenter**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter)
-   [**IVMRImagePresenterConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterconfig) (optional)
-   [**IVMRMonitorConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig) (optional)
-   [**IVMRSurfaceAllocator**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator)
-   [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) (optional)

Weitere Informationen zu benutzerdefinierten Allocator-Presentern finden Sie unter [Supplying a Custom Allocator-Presenter for VMR-7](supplying-a-custom-allocator-presenter-for-vmr-7.md).

Eine Anwendung kann auch einen benutzerdefinierten Plug-In-Compositor bereitstellen, der die folgende Schnittstelle verfügbar macht:

-   [**IVMRImageCompositor**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagecompositor)

Rufen Sie ZUM Konfigurieren des virtuellen Computers mit einem benutzerdefinierten [**Compositor IVMRFilterConfig::SetImageCompositor auf.**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setimagecompositor)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 




