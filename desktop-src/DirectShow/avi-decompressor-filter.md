---
description: AVI-Debug-Filter
ms.assetid: 6a9914db-483a-429c-9b26-9451578951c9
title: AVI-Debug-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9b6fcff61dd867c598e793fb5aa8fbff67dc6cd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746921"
---
# <a name="avi-decompressor-filter"></a>AVI-Debug-Filter

Der AVI-Debug-Filter ermöglicht VCM-Codecs (Video Compression Manager) zum Verknüpfen eines Filter Diagramms. Die Anwendung muss den Filter nicht zum Filter Diagramm hinzufügen. Sie wird automatisch vom Filter Graph-Manager abgerufen, wenn dies erforderlich ist.

Wenn der Filter Graph-Manager ein Diagramm zum Rendering einer AVI-Datei aufbaut, überprüft er den FourCC im AVI-Header der Datei, um zu bestimmen, ob der Videostream komprimiert ist. Wenn dies der Fall ist, fügt der Filter Graph-Manager den AVI Dekompressor hinzu, der dann in der Registrierung nach einem installierten Dekompressor sucht, der die Datei verarbeiten kann.

> [!Note]  
> MPEG-Debug werden nie als VCM-Codecs implementiert, sondern nur als Native DirectShow-Filter.

 

In der upstreampin stellt der AVI-Debug in der Regel eine Verbindung mit dem [avi-Splitter](avi-splitter-filter.md)her. Bei der Ausgabe-PIN stellt Sie in der Regel eine Verbindung mit dem [Videorenderer](video-renderer-filter.md) oder dem [AVI MUX-Filter](avi-mux-filter.md)her.



|                                          |                                                                                                                                                                                                                    |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filter Schnittstellen                        | [**Ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                                                                                 |
| Eingabe-PIN-Medientypen                    | Haupttyp: MediaType \_ videosubtype: muss dem FourCC-Code für den Komprimierungstyp entsprechen. Weitere Informationen finden Sie unter [FOURCC Codes](fourcc-codes.md).<br/> Formattyp: \_ Video Info formatieren<br/> |
| PIN-Eingabeschnittstellen                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                             |
| Ausgabe-PIN-Medientypen                   | MediaType- \_ Video, mediasubtype \_ NULL, \_ Video Info formatieren                                                                                                                                                            |
| PIN-Schnittstellen                    | [**Imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition), [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                 |
| CLSID Filtern                             | CLSID- \_ avidec                                                                                                                                                                                                      |
| CLSID der Eigenschaften Seite                      | Keine Eigenschaften Seite.                                                                                                                                                                                                  |
| Ausführbare Datei                               | quartz.dll                                                                                                                                                                                                         |
| [Verdienst](merit.md)                       | Verdienst \_ Normal                                                                                                                                                                                                      |
| [Filter Kategorie](filter-categories.md) | CLSID \_ legacyamfiltercategory                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 




