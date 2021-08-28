---
description: Der Filter Enhanced Video Renderer (EVR) ist ein 16-Kanal-Videomixer und -renderer. Sie verfügt über die gleiche Kernfunktionalität und dasselbe Plug-In-Modell wie die Media Foundation EVR-Mediensenke.
ms.assetid: ead99cb3-2be2-42c6-ac22-be0c2ddf28d5
title: Erweiterter Videorendererfilter
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96075ab9149cdf219971c5d1c321474de784aaa8
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987893"
---
# <a name="enhanced-video-renderer-filter"></a>Erweiterter Videorendererfilter

> [!Note]  
> Dieses Thema gilt für Windows Vista und höher.

 

Der Filter Enhanced Video Renderer (EVR) ist ein 16-Kanal-Videomixer und -renderer. Sie verfügt über die gleiche Kernfunktionalität und dasselbe Plug-In-Modell wie die Media Foundation EVR-Mediensenke.

Der DirectShow EVR-Filter ist in der Media Foundation SDK-Dokumentation dokumentiert. Weitere Informationen finden Sie unter [Erweiterter Videorenderer.](../medfound/enhanced-video-renderer.md)




| Bezeichnung | Wert |
|--------|-------|
| Filterschnittstellen (über <strong>QueryInterface)</strong> | DirectShow-Schnittstellen:<ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></li><li><a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaeventsink"><strong>IMediaEventSink</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></li></ul>Media Foundation Schnittstellen:<br /><ul><li><a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfig"><strong>IEVRFilterConfig</strong></a></li><li><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>VERZRGETService</strong></a></li><li><a href="/windows/desktop/api/evr/nn-evr-imfvideopositionmapper"><strong>CITRIXVideoPositionMapper</strong></a></li><li><a href="/windows/desktop/api/evr/nn-evr-imfvideorenderer"><strong>DINNERVideoRenderer</strong></a></li></ul> | 
| Eingabepinmedientypen | Variable, abhängig vom Grafiktreiber. | 
| Eingabe-Stecknadelschnittstellen (über <strong>QueryInterface)</strong> | DirectShow-Schnittstellen:<ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li></ul>Media Foundation Schnittstellen:<br /><ul><li><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration"><strong>IDirectXVideoMemoryConfiguration</strong></a></li><li><a href="/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol"><strong>IEVRVideoStreamControl</strong></a></li><li><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>VERZRGETService</strong></a></li></ul> | 
| Medientypen des Ausgabepins | Nicht zutreffend | 
| Ausgabe-Pin-Schnittstellen | Nicht zutreffend | 
| Filtern von CLSID | CLSID_EnhancedVideoRenderer | 
| Ausführbare Datei | evr.dll | 
| <a href="merit.md">Verdienst</a> | MERIT_DO_NOT_USE | 
| <a href="filter-categories.md">Filterkategorie</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Bemerkungen

Zusätzlich zu den Schnittstellen, die über **QueryInterface** verfügbar gemacht werden, macht der EVR andere Schnittstellen über die [**METHODE "TARGETINGGetService::GetService"**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) verfügbar. Einige dieser Schnittstellen werden vom EVR-Presenter oder dem EVR-Mixer anstelle der EVR selbst implementiert. Wenn die Anwendung einen benutzerdefinierten Presenter oder Mixer auf der EVR festlegt, machen die benutzerdefinierten Versionen möglicherweise einen anderen Satz von Schnittstellen verfügbar.



| Object     | Dienstbezeichner                                              | Schnittstellen                                                                                                                                                                                                                                                                                                     |
|------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EVR-Filter | MR \_ VIDEO \_ RENDER \_ SERVICE(Queries EVR or presenter)<br/> | [**DINNERVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)<br/> [**THICKNESSVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol)<br/> [**CITRIXVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)<br/> [**DINNERVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter)<br/>                                                          |
| EVR-Filter | MR \_ VIDEO \_ ACCELERATION \_ SERVICE(Queries presenter)<br/>  | [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9)                                                                                                                                                                                                                                                      |
| EVR-Filter | MR \_ VIDEO \_ MIXER \_ SERVICE(Queries mixer)<br/>             | [**DINNERVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)<br/> [**ORBITVideoMixerBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap)<br/> [**DINNERVideoMixerControl**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol)<br/> [**CITRIXVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)<br/> [**DENKVideoProcessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor)<br/> |
| Eingabepins | \_ \_ MR-VIDEOBESCHLEUNIGUNGSDIENST \_                                | [**IDirectXVideoMemoryConfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)                                                                                                                                                                                                                                    |



 

Die EVR kann bis zu 16 Videostreams kombinieren. Der erste Eingabestream (Pin 0) wird als *Verweisstream* bezeichnet. Der Verweisstream wird immer zuerst in der Z-Reihenfolge angezeigt. Alle zusätzlichen Streams werden als Substreams bezeichnet und über dem Verweisstream gemischt. Die Anwendung kann die Z-Reihenfolge der Unterstreams ändern, aber kein Unterstream kann zuerst in der Z-Reihenfolge stehen.

Der Grafiktreiber bestimmt, welche Videoformate unterstützt werden, aber in der Regel sind sie auf Folgendes beschränkt:

-   Verweisdatenstrom: Progressive oder verschachtelte YUV ohne Pro-Pixel-Alpha (z. B. NV12 oder YUY2); oder progressive RGB.
-   Substreams: Progressive YUV mit pro Pixel-Alpha, z. B. AYUV oder AI44.

Die verfügbaren Unterstreamformate hängen möglicherweise vom Format des Verweisstreams ab.

Die EVR leitet Suchbefehle upstream über Pin 0 weiter. Die Substream-Pins leiten suchbefehle nicht weiter. Es liegt in der Verantwortung des Quell- oder Splitterfilters, die Substreams mit dem Verweisstream synchronisiert zu halten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

