---
description: PARSE-Parserfilter
ms.assetid: a56576ad-f949-48fa-85e0-3e9898d2970d
title: PARSE-Parserfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60ce659559852497b8ec55709e77f9510a1deaf2
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908428"
---
# <a name="midi-parser-filter"></a>PARSE-Parserfilter

Der PARSER-Filter liest DIE IN-Daten, die in gefunden werden. MID und . RMI-Dateien. Der Filter akzeptiert einen Stream aus den Filtern [asynchrone Dateiquelle](file-source--async--filter.md) oder [URL-Dateiquelle](file-source--url--filter.md) und gibt FÜR-Beispiele für die Wiedergabe an den [**RENDERer VON RENDERER**](midi-renderer-filter.md) aus.



| Bezeichnung | Wert |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| Filterschnittstellen                        | [**IAMMediaContent,**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent) [ **IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                           |
| Eingabe-Stecknadelmedientypen                    | MEDIATYPE \_ Stream, MEDIASUBTYPE \_ Streams                                                                    |
| Eingabe-Pin-Schnittstellen                     | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                         |
| Medientypen des Ausgabepins                   | \_MEDIATYPE- Und MEDIASUBTYPE \_ NULL-Werte                                                                      |
| Ausgabe-Pin-Schnittstellen                    | [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IQualityControl,**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) |
| Filtern von CLSID                             | \_CLSID-DATEIPARSER                                                                                        |
| CLSID der Eigenschaftenseite                      | Keine Eigenschaftenseite                                                                                         |
| Ausführbare Datei                               | quartz.dll                                                                                               |
| [Verdienst](merit.md)                       | WAHRSCHEINLICHKEIT \_ UNWAHRSCHEINLICH                                                                                          |
| [Filterkategorie](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                            |



 

## <a name="remarks"></a>Bemerkungen

Weitere Informationen finden Sie unter [**RENDERING-Renderer**](midi-renderer-filter.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



