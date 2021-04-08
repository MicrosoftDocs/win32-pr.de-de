---
description: VideoPort-Manager
ms.assetid: d70558a5-9820-432a-b4f3-ccf7bb2a34d5
title: VideoPort-Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7ca884ff009584ef2904387d872733ddf8d53dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866436"
---
# <a name="video-port-manager"></a>VideoPort-Manager

Mit dem Video Port Manager-Filter (VPM) kann der Video Mischungs-Renderer Filter 7 (VMR-7) mit Video Erfassungs Geräten oder Hardware Decodern arbeiten, die einen Videoport verwenden. Ein Videoport ist eine direkte Hardware Verbindung mit dem Grafikchip. Es ermöglicht, dass Videos direkt auf den Grafikchip übertragen werden, ohne den Systembus zu überspringen.

> [!Note]  
> Der Videoport-Manager ist nicht kompatibel mit VMR-9, da VMR-9 keine videports unterstützt.

 



|                                          |                                                                                                                                                                                                                      |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filter Schnittstellen                        | [**Iamvideodecimationproperties**](/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties), [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**ikspropertyset**](ikspropertyset.md), [**iqualprop**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop), [**ivpmanager**](/windows/desktop/api/Strmif/nn-strmif-ivpmanager) |
| Eingabe-PIN-Medientypen                    | MediaType \_ Video, mediasubtype \_ vpvideo oder mediasubtype \_ vpvbi, Format \_ None                                                                                                                                         |
| PIN-Eingabeschnittstellen                     | [**Ikspin**](ikspin.md), [**ikspropertyset**](ikspropertyset.md), [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**ipinconnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Ausgabe-PIN-Medientypen                   | MediaType- \_ Video, Format \_ VideoInfo2                                                                                                                                                                                 |
| PIN-Schnittstellen                    | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                                     |
| CLSID Filtern                             | CLSID \_ videoportmanager                                                                                                                                                                                              |
| [Verdienst](merit.md)                       | Verdienst \_ Normal                                                                                                                                                                                                        |
| [Filter Kategorie](filter-categories.md) | CLSID \_ legacyamfiltercategory                                                                                                                                                                                        |



 

## <a name="remarks"></a>Bemerkungen

Der Video Port-Manager kombiniert die Video Port Funktionen des [Überlagerungs-Mischungs Filters](overlay-mixer-filter.md) und die Funktionalität der [VBI-Oberflächen Zuweisung](vbi-surface-allocator.md). Das VPM ordnet videports und Oberflächen zu und synchronisiert die Datenerfassung über den Videoport. Sie ermöglicht eine Video Port basierte Erfassung, die unabhängig vom Rendering ist. Wenn die Vorschau gewünscht ist, koordiniert VPM die VMR-7, um erfasste videoportdaten anzuzeigen. Wenn ein Videoport auf dem System vorhanden ist, erfordert der Erfassungs Filter zusätzliche Puffer zum Extrahieren von VBI-Daten aus dem Videostream. Diese Puffer werden von VPM bereitgestellt. Nachdem der Erfassungs Filter die VBI-Daten extrahiert hat, übergibt er Sie an eine separate PIN an Filter wie den CC-Decoder. Die folgende Abbildung zeigt das VPM und seine Verbindungen in einem Filter Diagramm.

![Video Port-Manager-Filter Diagramm Segment](images/vpm.png)

Der DVD Graph-Generator fügt das VPM automatisch dem Filter Diagramm hinzu, wenn ein Videoport auf dem System erkannt wird. Nach dem Hinzufügen zum Diagramm verwendet das VPM ein vom Video Mischungs-Renderer bereitgestelltes DirectDraw-Objekt, um zwei oder drei Oberflächen zuzuordnen. Diese Oberflächen empfangen die digitalisierten Frames aus dem upstreamerfassungs-Filter. Als Reaktion auf Benutzermodus-Ereignis Benachrichtigungen, die gesendet werden, wenn Daten auf der-Oberfläche vorhanden sind, führt das VPM einen automatischen Blit auf eine von VMR bereitgestellte Offscreen-Oberfläche aus.

Die Tatsache, dass das VPM mehrere Oberflächen für die Eingabepuffer verwendet, bedeutet, dass mehr VRAM als bei der vorherigen Implementierung des DirectShow-Video Ports erforderlich ist. Der zusätzliche Blit von VPM zu VMR-7 erfordert zusätzliche Grafikspeicher Bandbreite. Da das automatische Kippen von Hardware nicht mehr verwendet wird, gibt es ein theoretisches Potenzial für verworfene Frames, aber der empirische Beweis deutet darauf hin, dass dies nicht geschieht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[**Ivpmanager-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ivpmanager)
</dt> </dl>

 

 



