---
description: PARSER-Filter
ms.assetid: a56576ad-f949-48fa-85e0-3e9898d2970d
title: PARSER-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c5907c36e668a39494b46ec6bbc67e4d8cb4870357df9c1f0303c882bc86f0d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119256510"
---
# <a name="midi-parser-filter"></a>PARSER-Filter

Der PARSER-Filter liest DIE-Daten, die in gefunden werden. MID und . RMI-Dateien. Der Filter akzeptiert einen Stream aus den [Filtern Async File Source (Asynchrone](file-source--async--filter.md) Dateiquelle) oder [URL File Source (URL-Dateiquelle)](file-source--url--filter.md) und gibt DANN-Beispiele zur Wiedergabe an den [**RENDERING-Renderer**](midi-renderer-filter.md) aus.



| Bezeichnung | Wert |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| Filterschnittstellen                        | [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [ **IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                           |
| Eingabepin-Medientypen                    | MEDIATYPE \_ Stream, MEDIASUBTYPE \_ Format                                                                    |
| Eingabepinschnittstellen                     | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                         |
| Ausgabepin-Medientypen                   | MEDIATYPE \_ Format, MEDIASUBTYPE \_ NULL                                                                      |
| Ausgabe-PIN-Schnittstellen                    | [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IQualityControl,**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) |
| Filtern der CLSID                             | \_CLSID-FORMATPARSer                                                                                        |
| Eigenschaftenseite CLSID                      | Keine Eigenschaftenseite                                                                                         |
| Ausführbare Datei                               | quartz.dll                                                                                               |
| [Verdienst](merit.md)                       | WAHRSCHEINLICHKEIT \_ UNWAHRSCHEINLICH                                                                                          |
| [Filterkategorie](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                            |



 

## <a name="remarks"></a>Hinweise

Weitere Informationen finden Sie unter [**RENDERING-Renderer**](midi-renderer-filter.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



