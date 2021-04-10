---
description: Datei Quellen Filter (URL)
ms.assetid: 405fd6ea-aa17-4d11-8f07-067468cb090b
title: Datei Quellen Filter (URL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caea04b74a6880452210f1a43d5dfb29f8753dd3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125107"
---
# <a name="file-source-url-filter"></a>Datei Quellen Filter (URL)

Der URL-Quell Filter ist ein generischer asynchroner Quell Filter, der mit einer beliebigen Quelldatei verwendet werden kann, die durch eine Uniform Resource Locator (URL) identifiziert werden kann und deren Haupt Datentyp Stream ist. Hierzu gehören AVI-, MOV-, MPEG-und WAV-Dateien. Der downstreamfilter muss ein Parser sein, z. b. der [MPEG-1-streamsplitter](mpeg-1-stream-splitter-filter.md), der [avi-Splitter](avi-splitter-filter.md)oder der QuickTime- [Film Parser](quicktime-movie-parser-filter.md).



|                                          |                                                                                                                                      |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| Filter Schnittstellen                        | [**Iamopenprogress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress), [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)       |
| Eingabe-PIN-Medientypen                    | Nicht verfügbar                                                                                                                       |
| PIN-Eingabeschnittstellen                     | Nicht verfügbar                                                                                                                       |
| Ausgabe-PIN-Medientypen                   | MediaType-Daten \_ Strom. Der Untertyp hängt vom Medienformat ab. (Mediasubtype \_ NULL, wenn der Filter das Format nicht erkennt.)         |
| PIN-Schnittstellen                    | [**Iamasynkreadertimestampscaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**iasynkreader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) |
| CLSID Filtern                             | CLSID- \_ urlreader                                                                                                                     |
| CLSID der Eigenschaften Seite                      | Keine Eigenschaften Seite                                                                                                                     |
| Ausführbare Datei                               | quartz.dll                                                                                                                           |
| [Verdienst](merit.md)                       | nicht \_ wahrscheinlich                                                                                                                      |
| [Filter Kategorie](filter-categories.md) | CLSID \_ legacyamfiltercategory                                                                                                        |



 

## <a name="remarks"></a>Bemerkungen

Dieser Filter verwendet Urlmon und unterstützt Codepages.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



