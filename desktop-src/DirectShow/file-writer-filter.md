---
description: File Writer-Filter
ms.assetid: 2bfbea8a-679f-4656-9ff3-fdf34aa0eb26
title: File Writer-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e991536d505ee1bdfcaaaca5ce8660c4480decf6
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909688"
---
# <a name="file-writer-filter"></a>File Writer-Filter

Der File Writer-Filter kann verwendet werden, um Dateien unabhängig vom Format auf den Datenträger zu schreiben. Der Filter schreibt einfach auf den Datenträger, was er auf seinem Eingabepin empfängt, sodass er mit einem Multiplexer verbunden werden muss, der die Datei ordnungsgemäß formatieren kann. Sie können eine neue Ausgabedatei mit dem Dateiwriter erstellen oder eine vorhandene Datei angeben. Wenn die Datei bereits vorhanden ist, wird sie vollständig mit den neuen Daten überschrieben.

Der Dateiwriterfilter verwendet die Zeitstempel des Eingabestreams als Dateioffsets und bietet zufälligen Zugriff auf die Datei. IStream  wird unterstützt, um das Lesen und Schreiben des Dateiheaders zu ermöglichen, nachdem das Diagramm beendet wurde. Zur Verbesserung der Leistung werden auch nicht gepufferte überlappende Schreibvorgänge unterstützt und die entsprechende Pufferaushandlung verarbeitet.

> [!Note]  
> Verwenden Sie zum Schreiben von ASF-Dateien den [WM ASF](wm-asf-writer-filter.md) Writer-Filter.

 



| Bezeichnung | Wert |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filterschnittstellen                        | [**IAMFilterMiscFlags,**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags) [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IFileSinkFilter,**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) [**IFileSinkFilter2,**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2) **IPersistStream** |
| Eingabe-Stecknadelmedientypen                    | \_MEDIATYPE-Stream, MEDIASUBTYPE \_ NULL                                                                                                                                                              |
| Eingabe-Pin-Schnittstellen                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl,**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) **IStream**                                                                                |
| Medientypen des Ausgabepins                   | Nicht zutreffend                                                                                                                                                                                     |
| Ausgabe-Pin-Schnittstellen                    | Nicht zutreffend                                                                                                                                                                                     |
| Filtern von CLSID                             | CLSID \_ FileWriter                                                                                                                                                                                  |
| Eigenschaftenseite CLSID                      | Keine Eigenschaftenseite                                                                                                                                                                                   |
| Ausführbare Datei                               | qcap.dll                                                                                                                                                                                           |
| [Verdienst](merit.md)                       | NICHT \_ \_ VERWENDEN \_                                                                                                                                                                                |
| [Filterkategorie](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



