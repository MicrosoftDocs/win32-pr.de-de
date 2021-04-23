---
description: AVI-Dekomprimierungsfilter
ms.assetid: 6a9914db-483a-429c-9b26-9451578951c9
title: AVI-Dekomprimierungsfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 214ccfeee18a01fa9c8d52ffbf4593b9de5664bb
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910098"
---
# <a name="avi-decompressor-filter"></a>AVI-Dekomprimierungsfilter

Der FILTER FÜR DEN AVI-Dekomprimierungsfilter ermöglicht videokomprimierungs-Manager-Codecs (VCM), um einen Filtergraphen zu verbinden. Die Anwendung muss den Filter nicht dem Filterdiagramm hinzufügen. Sie wird bei Bedarf automatisch vom Filtergraph-Manager eingezogen.

Wenn der Filter graph Manager ein Diagramm zum Rendern einer AVI-Datei aufbaut, überprüft er fourcc im AVI-Header der Datei, um zu bestimmen, ob der Videostream komprimiert ist. In diesem Beispiel fügt der Filter graph-Manager den AVI-Dekomprimor hinzu, der dann in der Registrierung nach einem installierten Dekomprimator sucht, der die Datei verarbeiten kann.

> [!Note]  
> MPEG-Dekomprimierungen werden nie als VCM-Codecs implementiert, sondern nur als native DirectShow-Filter.

 

An seinem Upstreampin stellt der AVI-Dekomprimator in der Regel eine Verbindung mit dem [AVI-Splitter () auf.](avi-splitter-filter.md) Auf dem Ausgabepin wird in der Regel eine Verbindung mit dem [Videorenderer](video-renderer-filter.md) oder [dem AVI Mux Filter -Filter herstellt.](avi-mux-filter.md)



| Bezeichnung | Wert |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filterschnittstellen                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                                                                                 |
| Eingabepin-Medientypen                    | Haupttyp: MEDIATYPE \_ VideoSubtype: Muss dem FOURCC-Code für den Komprimierungstyp entsprechen. Weitere Informationen finden Sie unter [FOURCC Codes](fourcc-codes.md).<br/> Formattyp: FORMAT \_ VideoInfo<br/> |
| Eingabepinschnittstellen                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                             |
| Ausgabepin-Medientypen                   | MEDIATYPE \_ Video, MEDIASUBTYPE \_ NULL, FORMAT \_ VideoInfo                                                                                                                                                            |
| Ausgabe-Pin-Schnittstellen                    | [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                 |
| Filtern von CLSID                             | CLSID \_ AVIDec                                                                                                                                                                                                      |
| CLSID der Eigenschaftenseite                      | Keine Eigenschaftenseite.                                                                                                                                                                                                  |
| Ausführbare Datei                               | quartz.dll                                                                                                                                                                                                         |
| [Verdienst](merit.md)                       | NORMALER WERT \_                                                                                                                                                                                                      |
| [Filterkategorie](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 




