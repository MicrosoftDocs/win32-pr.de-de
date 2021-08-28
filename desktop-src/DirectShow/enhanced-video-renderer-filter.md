---
description: Der EVR-Filter (Enhanced Video Renderer) ist ein 16-Kanal-Videomixer und -renderer. Es verfügt über die gleiche Kernfunktionalität und das gleiche Plug-In-Modell wie Media Foundation EVR-Mediensenke.
ms.assetid: ead99cb3-2be2-42c6-ac22-be0c2ddf28d5
title: Erweiterter Videorendererfilter
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ed63ba80864f98012a178ed775e5812ee5abe88
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475526"
---
# <a name="enhanced-video-renderer-filter"></a>Erweiterter Videorendererfilter

> [!Note]  
> Dieses Thema gilt für Windows Vista und höher.

 

Der EVR-Filter (Enhanced Video Renderer) ist ein 16-Kanal-Videomixer und -renderer. Es verfügt über die gleiche Kernfunktionalität und das gleiche Plug-In-Modell wie Media Foundation EVR-Mediensenke.

Der DirectShow EVR-Filter ist in der Dokumentation zum Media Foundation SDK dokumentiert. Weitere Informationen finden Sie unter [Enhanced Video Renderer](../medfound/enhanced-video-renderer.md).




| | | Filterschnittstellen (über <strong>QueryInterface</strong>) | DirectShow-Schnittstellen:<ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></li><li><a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaeventsink"><strong>IMediaEventSink</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></li></ul>Media Foundation Schnittstellen:<br /><ul><li><a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfig"><strong>IEVRFilterConfig</strong></a></li><li><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>GEGETService</strong></a></li><li><a href="/windows/desktop/api/evr/nn-evr-imfvideopositionmapper"><strong>CITRIXVideoPositionMapper</strong></a></li><li><a href="/windows/desktop/api/evr/nn-evr-imfvideorenderer"><strong>BENTVideoRenderer</strong></a></li></ul> | | Eingabepin-Medientypen | Variable, abhängig vom Grafiktreiber. | | Eingabepinschnittstellen (über <strong>QueryInterface</strong>) | DirectShow-Schnittstellen:<ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li></ul>Media Foundation Schnittstellen:<br /><ul><li><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration"><strong>IDirectXVideoMemoryConfiguration</strong></a></li><li><a href="/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol"><strong>IEVRVideoStreamControl</strong></a></li><li><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>GEGETService</strong></a></li></ul> | | Ausgabepin-Medientypen | Nicht zutreffend. | | Ausgabepinschnittstellen | Nicht zutreffend. | | Filtern von CLSID-| CLSID_EnhancedVideoRenderer | | Ausführbare | evr.dll | | <a href="merit.md">Leistungs-|</a> MERIT_DO_NOT_USE | | <a href="filter-categories.md">Filterkategorie-|</a> CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Hinweise

Zusätzlich zu den Schnittstellen, die über **QueryInterface verfügbar** gemacht werden, macht der EVR andere Schnittstellen über die [**METHODE DURCHGETService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) verfügbar. Einige dieser Schnittstellen werden von der EVR-Moderatorin oder dem EVR-Mixer und nicht von der EVR selbst implementiert. Wenn die Anwendung eine benutzerdefinierte Präsentation oder einen benutzerdefinierten Mixer auf der EVR-Schnittstelle festgelegt, können die benutzerdefinierten Versionen einen anderen Satz von Schnittstellen verfügbar machen.



| Object     | Dienstbezeichner                                              | Schnittstellen                                                                                                                                                                                                                                                                                                     |
|------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EVR-Filter | MR \_ VIDEO \_ RENDER \_ SERVICE(Fragt EVR oder Presenter ab)<br/> | [**BENTVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)<br/> [**BILDSCHIRMEVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol)<br/> [**CITRIXVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)<br/> [**VERERBUNGVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter)<br/>                                                          |
| EVR-Filter | MR \_ VIDEO \_ ACCELERATION \_ SERVICE(Queries presenter)<br/>  | [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9)                                                                                                                                                                                                                                                      |
| EVR-Filter | MR \_ VIDEO MIXER SERVICE \_ \_ (Abfragemixer)<br/>             | [**BENTVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)<br/> [**VERSATZVideoMixerBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap)<br/> [**BEREINIGERVideoMixerControl**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol)<br/> [**CITRIXVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)<br/> [**VERWERTERVideoProzessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor)<br/> |
| Eingabepins | \_ \_ MR-VIDEOBESCHLEUNIGUNGSDIENST \_                                | [**IDirectXVideoMemoryConfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)                                                                                                                                                                                                                                    |



 

Der EVR kann bis zu 16 Videostreams mischen. Der erste Eingabestream (Pin 0) wird als *Verweisstream bezeichnet.* Der Verweisstream wird immer zuerst in der Z-Reihenfolge angezeigt. Alle zusätzlichen Streams werden als Unterstreams bezeichnet und über dem Verweisstream gemischt. Die Anwendung kann die Z-Reihenfolge der Unterstreams ändern, aber kein Unterstream darf in der Z-Reihenfolge an erster Stelle sein.

Der Grafiktreiber bestimmt, welche Videoformate unterstützt werden, in der Regel sind sie jedoch auf Folgendes beschränkt:

-   Verweisstream: Progressiver yuv ohne Pixel-Alpha (z. B. NV12 oder YUY2) oder progressives RGB.
-   Unterstreams: Progressive YUV mit Pro-Pixel-Alpha, z. B. AYUV oder AI44.

Die verfügbaren Unterstreamformate können vom Format des Verweisstreams abhängen.

Der EVR weitert Suchbefehle upstream über Pin 0. Die Unterstreampins geben keine Suchbefehle weiter. Es liegt in der Verantwortung des Quell- oder Splitterfilters, die Unterstreams mit dem Verweisstream synchron zu halten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

