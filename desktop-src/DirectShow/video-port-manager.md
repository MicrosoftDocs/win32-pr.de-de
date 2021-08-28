---
description: Videoport-Manager
ms.assetid: d70558a5-9820-432a-b4f3-ccf7bb2a34d5
title: Videoport-Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fb7a31d21592bd94579ad608fb453e2a2ec0a264d674f807b404a43f2a0bc1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903514"
---
# <a name="video-port-manager"></a>Videoport-Manager

Der Videoport-Manager-Filter (VPM) ermöglicht dem Video Mixing Renderer Filter 7 (VMR-7) das Arbeiten mit Videoaufnahmegeräten oder Hardwaredecodern, die einen Videoport verwenden. Ein Videoport ist eine direkte Hardwareverbindung mit dem Grafikchip. Sie ermöglicht die direkte Übertragung von Videos auf den Grafikchip, ohne den Systembus zu durchlaufen.

> [!Note]  
> Der Videoport-Manager ist nicht mit VMR-9 kompatibel, da VMR-9 keine Videoports unterstützt.

 



| Bezeichnung | Wert |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filterschnittstellen                        | [**IAMVideoDecimationProperties,**](/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties) [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IKsPropertySet,**](ikspropertyset.md) [**IQualProp,**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop) [**IVPManager**](/windows/desktop/api/Strmif/nn-strmif-ivpmanager) |
| Eingabepinmedientypen                    | MEDIATYPE \_ Video, MEDIASUBTYPE \_ VPVideo oder MEDIASUBTYPE \_ VPVBI, FORMAT \_ None                                                                                                                                         |
| Eingabe-Pin-Schnittstellen                     | [**IKsPin,**](ikspin.md) [**IKsPropertySet,**](ikspropertyset.md) [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IPinConnection,**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Medientypen des Ausgabepins                   | MEDIATYPE \_ Video, FORMAT \_ VideoInfo2                                                                                                                                                                                 |
| Ausgabe-Pin-Schnittstellen                    | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                                     |
| Filtern von CLSID                             | CLSID \_ VideoPortManager                                                                                                                                                                                              |
| [Verdienst](merit.md)                       | NORMALER WERT \_                                                                                                                                                                                                        |
| [Filterkategorie](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                                        |



 

## <a name="remarks"></a>Hinweise

Der Videoport-Manager kombiniert die Videoportfunktionalität des [Overlay-Mixer-Filters](overlay-mixer-filter.md) und die Funktionalität der [VBI Surface Allocator-](vbi-surface-allocator.md). Der VPM ordnet Videoports und Oberflächen zu und synchronisiert die Datenerfassung über den Videoport. Sie ermöglicht die videoportbasierte Erfassung, die unabhängig vom Rendering ist. Wenn eine Vorschauversion gewünscht ist, koordiniert sich der VPM mit VMR-7, um aufgezeichnete Videoportdaten anzuzeigen. Wenn ein Videoport auf dem System vorhanden ist, benötigt der Erfassungsfilter zusätzliche Puffer, um VBI-Daten aus dem Videostream zu extrahieren. Diese Puffer werden vom VPM bereitgestellt. Nachdem der Erfassungsfilter die VBI-Daten extrahiert hat, übermittelt er sie an einen separaten Pin an Filter wie den CC-Decoder. Die folgende Abbildung zeigt den VPM und seine Verbindungen in einem Filterdiagramm.

![Filterdiagrammsegment des Videoport-Managers](images/vpm.png)

Der DVD Graph Builder fügt das VPM automatisch dem Filterdiagramm hinzu, wenn ein Videoport auf dem System erkannt wird. Nach dem Hinzufügen zum Diagramm verwendet das VPM ein DirectDraw-Objekt, das vom Videomischungsrenderer bereitgestellt wird, um zwei oder drei Oberflächen zuzuordnen. Diese Oberflächen empfangen die digitalisierten Frames vom Upstreamerfassungsfilter. Als Reaktion auf Benutzermodusereignisbenachrichtigungen, die gesendet werden, wenn Daten auf der Oberfläche vorhanden sind, führt das VPM einen automatischen Blit auf einer von der VMR bereitgestellten Offscreenoberfläche aus.

Die Tatsache, dass der VPM mehrere Oberflächen für seine Eingabepuffer verwendet, bedeutet, dass mehr VRAM erforderlich ist als bei der vorherigen DirectShow-Videoportimplementierungen. Die zusätzliche Blit-Auslastung zwischen VPM und VMR-7 erfordert zusätzliche Videospeicherbandbreite. Und da das automatische Hardware-Flipping nicht mehr verwendet wird, gibt es ein theoretisches Potenzial für gelöschte Frames, aber die empirischen Beweise deuten darauf hin, dass dies nicht geschieht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[**IVPManager-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ivpmanager)
</dt> </dl>

 

 



