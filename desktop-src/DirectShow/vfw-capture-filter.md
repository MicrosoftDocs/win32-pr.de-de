---
description: VFW-Erfassungsfilter
ms.assetid: 663b6b3b-2a50-4586-9506-600a59869abe
title: VFW-Erfassungsfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eadc2c8a22ed6e00ff76d79a0b7ce2db012abb4
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908398"
---
# <a name="vfw-capture-filter"></a>VFW-Erfassungsfilter

Dieser Filter funktioniert mit älterer Videoaufnahmehardware, die Video für Windows verwendet.

Dieser Filter verfügt über zwei Ausgabepins. Eine wird als Capture und die andere als Vorschau oder Overlay bezeichnet.



| Bezeichnung | Wert |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filterschnittstellen                        | **IPersistPropertyBag**, [**IAMVfwCaptureDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs), [**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), **ISpecifyPropertyPages**, [**IOverlayNotify**](/windows/desktop/api/Strmif/nn-strmif-ioverlaynotify)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Eingabepin-Medientypen                    | Nicht zutreffend                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Eingabepinschnittstellen                     | Nicht zutreffend                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Ausgabepin-Medientypen                   | Capture: MEDIATYPE \_ Video, MEDIASUBTYPE \_ NULL, FORMAT \_ VideoInfoOverlay: MEDIATYPE \_ Video, MEDIASUBTYPE \_ Overlay, FORMAT \_ VideoInfo<br/> Vorschau: MEDIATYPE \_ Video, MEDIASUBTYPE \_ NULL, FORMAT \_ VideoInfo<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Ausgabe-PIN-Schnittstellen                    | Erfassungspin: [**IAMBufferNegotiation**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation), [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes), [**IAMPushSource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource), [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IKsPropertySet**](ikspropertyset.md), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)Overlay Pin: [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**IKsPropertySet**](ikspropertyset.md), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/> Vorschaupin: [**IAMPushSource,**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) [**IAMStreamControl,**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) [**IKsPropertySet,**](ikspropertyset.md) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/> |
| Filtern der CLSID                             | CLSID \_ VfwCapture                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Eigenschaftenseite CLSID                      | CLSID \_ CaptureProperties                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Ausführbare Datei                               | qcap.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [Verdienst](merit.md)                       | NOT USE (NICHT \_ \_ \_ VERWENDEN)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [Filterkategorie](filter-categories.md) | CLSID \_ VideoInputDeviceCategory                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

## <a name="remarks"></a>Bemerkungen

Obwohl der Erfassungspin die [**IAMStreamConfig-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) verfügbar macht, werden nur die **Methoden SetFormat** und **GetFormat** für diese Schnittstelle implementiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[Videoaufnahme](video-capture.md)
</dt> </dl>

 

 




