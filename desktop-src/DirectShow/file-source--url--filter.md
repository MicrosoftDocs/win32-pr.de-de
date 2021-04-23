---
description: Filter für Dateiquelle (URL)
ms.assetid: 405fd6ea-aa17-4d11-8f07-067468cb090b
title: Filter für Dateiquelle (URL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0ddfa7282adbf5117bd2c52465c6eb30efbd69e
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909238"
---
# <a name="file-source-url-filter"></a>Filter für Dateiquelle (URL)

Der Filter URL-Dateiquelle ist ein generischer asynchroner Quellfilter, der mit jeder Quelldatei funktioniert, die durch eine Uniform Resource Locator (URL) identifiziert werden kann und deren Haupttyp des Mediums stream ist. Dies schließt AVI-, MOV-, MPEG- und WAV-Dateien ein. Der Downstreamfilter muss ein Parser sein, z. B. der [MPEG-1-Stream Splitter,](mpeg-1-stream-splitter-filter.md)der [AVI-Splitter](avi-splitter-filter.md)oder der [QuickTime Movie Parser](quicktime-movie-parser-filter.md).



| Bezeichnung | Wert |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| Filterschnittstellen                        | [**IAMOpenProgress,**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress) [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)       |
| Eingabepin-Medientypen                    | Nicht zutreffend                                                                                                                       |
| Eingabepinschnittstellen                     | Nicht zutreffend                                                                                                                       |
| Ausgabepin-Medientypen                   | \_MEDIATYPE-Stream. Der Untertyp hängt vom Medienformat ab. (MEDIASUBTYPE \_ NULL, wenn der Filter das Format nicht erkennt.)         |
| Ausgabe-PIN-Schnittstellen                    | [**IAMAsyncReaderTimestampScaling,**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling) [**IAsyncReader,**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) |
| Filtern der CLSID                             | CLSID \_ URLReader                                                                                                                     |
| Eigenschaftenseite CLSID                      | Keine Eigenschaftenseite                                                                                                                     |
| Ausführbare Datei                               | quartz.dll                                                                                                                           |
| [Verdienst](merit.md)                       | \_UNWAHRSCHEINLICHE WAHRSCHEINLICHKEIT                                                                                                                      |
| [Filterkategorie](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                        |



 

## <a name="remarks"></a>Bemerkungen

Dieser Filter verwendet URLMon und unterstützt Codepages.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



