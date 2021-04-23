---
description: Dateiquellenfilter (asynchron)
ms.assetid: 0cf6e7ab-b1fe-42f9-b682-c5484ef48c71
title: Dateiquellenfilter (asynchron)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ddeea7398ce332a8b1db444b6b74fe3841f9053
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909698"
---
# <a name="file-source-async-filter"></a>Dateiquellenfilter (asynchron)

Der Filter Asynchrone Dateiquelle wird geöffnet und liest lokale Dateien mit vielen verschiedenen Datenformaten und übergibt die Daten an einen Parserfilter.

Verwenden Sie zum Herunterladen von Mediendateien aus dem Web über HTTP den Filter Dateiquelle [(URL).](file-source--url--filter.md) Verwenden Sie zum Lesen von ASF-Dateien den [WM ASF-Readerfilter.](wm-asf-reader-filter.md)



| Bezeichnung | Wert |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| Filterschnittstellen                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)                                                   |
| Eingabepin-Medientypen                    | Nicht zutreffend                                                                                                                       |
| Eingabepinschnittstellen                     | Nicht zutreffend                                                                                                                       |
| Ausgabepin-Medientypen                   | **MEDIATYPE \_ Streamen Sie**. Der Untertyp hängt vom Medienformat ab. (**MEDIASUBTYPE \_ NULL,** wenn der Filter das Format nicht erkennt.) |
| Ausgabe-PIN-Schnittstellen                    | [**IAMAsyncReaderTimestampScaling,**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling) [**IAsyncReader,**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) |
| Filtern der CLSID                             | **CLSID \_ AsyncReader**                                                                                                               |
| Eigenschaftenseite CLSID                      | Keine Eigenschaftenseite                                                                                                                     |
| Ausführbare Datei                               | quartz.dll                                                                                                                           |
| [Verdienst](merit.md)                       | **\_UNWAHRSCHEINLICHE WAHRSCHEINLICHKEIT**                                                                                                                  |
| [Filterkategorie](filter-categories.md) | **CLSID \_ LegacyAmFilterCategory**                                                                                                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



