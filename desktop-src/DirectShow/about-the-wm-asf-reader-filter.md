---
description: Informationen zum WM-ASF-Reader-Filter
ms.assetid: e698c0da-88b2-497a-8a25-9d3b76c85a7d
title: Informationen zum WM-ASF-Reader-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b71d0b25070c446ebff88f18785df7b55ba7bbcc7b1bcaa1dcf21995185252ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873700"
---
# <a name="about-the-wm-asf-reader-filter"></a>Informationen zum WM-ASF-Reader-Filter

Die Wiedergabe von ASF-Dateien wird vom [WM-ASF-Readerfilter](wm-asf-reader-filter.md) verarbeitet. Wenn der WM ASF-Reader eine Datei liest, wird automatisch ein Ausgabepin für jeden Stream erstellt, einschließlich Webstreams, Skriptbefehlsstreams und beliebiger anderer Datenströme. Bei Dateien mit mehreren Bitraten werden Pins nur für die aktuell ausgewählten Streams erstellt. Um eine ASF-Datei mit dem WM ASF-Readerfilter wiederzugeben, rufen [**Sie IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) oder [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter)auf.

Der WM ASF Reader unterstützt die DirectShow [**IMediaSeeking-Schnittstelle,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) mit der Anwendungen temporale Suchaufgaben innerhalb der Datei ausführen können. Die Wiedergabe mit einer anderen Geschwindigkeit als 1.0 (wie in [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)angegeben) wird jedoch nicht unterstützt.

Der WM ASF Reader-Filter macht auch mehrere Windows Media Format SDK-Schnittstellen verfügbar, wie in der folgenden Tabelle beschrieben. Diese Schnittstellen sind in der Dokumentation Windows Media Format SDK dokumentiert.



| Schnittstelle                                             | Verfügbar gemacht                                 | Kommentare                                                                                                                       |
|-------------------------------------------------------|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)             | Über **IServiceProvider** für den Filter. | Wird für Anwendungen bereitgestellt, die Durch Digital Rights Management (DRM) geschützte Inhalte wiedergeben müssen.                             |
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | **QueryInterface** für den Filter.           | Wird bereitgestellt, damit Anwendungen Datei- und Inhaltsattribute sowie Marker- und Skriptinformationen und Metadaten lesen können.     |
| [**IWMReaderErweitert**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)   | **QueryInterface** für den Filter.           | Teilweise implementiert für den Filter, sodass Anwendungen auf die Informationsmethoden des WM-Readerobjekts zugreifen können.         |
| [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) | **QueryInterface** für den Filter.           | Teilweise implementiert für den Filter, sodass Anwendungen auf die Informationsmethoden im Format SDK Reader Object zugreifen können. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Lesen von ASF-Dateien in DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



