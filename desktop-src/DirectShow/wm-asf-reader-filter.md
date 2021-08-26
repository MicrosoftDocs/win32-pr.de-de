---
description: Erfahren Sie mehr über den WM ASF-Readerfilter für DirectShow. Dies ist ein Wrapperfilter für das Readerobjekt, das mit dem Windows Media Format SDK bereitgestellt wird.
ms.assetid: 82b9f849-b9dc-439b-8ca7-9dcd992338ab
title: WM ASF-Readerfilter (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e87642637e7a210707c049d9b3c6a1a431b0a277774ce432b1c5c962ff2f317
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049160"
---
# <a name="wm-asf-reader-filter-directshow"></a>WM ASF-Readerfilter (DirectShow)

Der WM ASF-Reader ist ein Wrapperfilter für das Readerobjekt, das mit dem Windows Media Format SDK bereitgestellt wird, und ist der empfohlene Quellfilter für die Dateiwiedergabe von Windows Medienbasierten Inhalten und Inhalten, die mit einem der Microsoft MPEG-4 Encoder-DMOs erstellt wurden.



| Bezeichnung | Wert |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filtern von Schnittstellen                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter), [**IAMExtendedSeeking**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamextendedseeking), **IServiceProvider** Zusätzlich macht der Filter die folgenden Windows Media Format SDK-Schnittstellen verfügbar: [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo), [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced), [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2), [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) (über **IServiceProvider**)<br/> |
| Eingabepin-Medientypen                    | Nicht zutreffend                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Eingabepinschnittstellen                     | Nicht zutreffend                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Ausgabepin-Medientypen                   | MEDIATYPE \_ Video, MEDIATYPE \_ Audio, MEDIATYPE \_ ScriptCommand, MEDIATYPE \_ FileTransfer                                                                                                                                                                                                                                                                                                                                                                                                     |
| Schnittstellen für Ausgabepins                    | [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass), **IServiceProvider** Zusätzlich machen die Pins die folgenden Windows Media Format SDK-Schnittstellen verfügbar: **IWMStreamConfig2** (über **IServiceProvider**)<br/>                                                                                                                                                                                                                                    |
| Filtern der CLSID                             | CLSID \_ WMAsfReader                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Eigenschaftenseite CLSID                      | Keine Eigenschaftenseite.                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Ausführbare Datei                               | Qasf.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [Verdienst](merit.md)                       | WAHRSCHEINLICHKEIT \_ UNWAHRSCHEINLICH                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [Filterkategorie](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="remarks"></a>Hinweise

Wenn der Name einer ASF-Datei oder einer URL angegeben wird, liest der WM ASF-Reader den komprimierten Inhalt, analysiert die komprimierten Datenströme und macht für jeden einen Ausgabepin verfügbar. Dieser Filter verbindet downstream mit Audio- und/oder Videocodecfiltern, die die Dekomprimierung anwenden. Die Suche wird unterstützt, wenn die ASF-Datei durchsuchbar ist. Der ASF-Reader stempelt die Stichproben, bevor er sie nachgelagert sendet, ändert die Zeitstempel jedoch in irgendeiner Weise.

Die Wiedergabe mit anderen Geschwindigkeiten als 1.0 (wie in [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)angegeben) wird nicht unterstützt.

Wenn die Windows Media Format SDK-Runtime [**WMT \_ STATUS-Nachrichten**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_status) an den WM ASF Writer-Filter sendet, leitet der Filter alle Nachrichten im Zusammenhang mit dem DRM-Lizenzerwerb als [**EC \_ WMT \_ EVENT-Ereignisse**](ec-wmt-event.md) weiter. Weitere Informationen finden Sie unter [Lesen DRM-Protected ASF-Dateien in DirectShow](reading-drm-protected-asf-files-in-directshow.md).

Der WM ASF-Reader implementiert teilweise die [**Schnittstellen IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) und [**IWMReaderAdvanced2,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) um Anwendungen Zugriff auf die Informationsmethoden auf dem Readerobjekt zu geben. Die Implementierung des Filters übergibt die Aufrufe einfach an die -Schnittstelle des Readerobjekts. Die Streamingmethoden werden nicht implementiert, da der Filter vollständige Kontrolle über den Streamingprozess haben muss. Die folgenden Methoden werden implementiert:

-   [**IWMReaderAdvanced::GetStatistics**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics)
-   [**IWMReaderAdvanced::SetClientInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo)
-   [**IWMReaderAdvanced2::GetBufferProgress**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress)
-   [**IWMReaderAdvanced2::GetDownloadProgress**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress)
-   [**IWMReaderAdvanced2::GetPlayMode**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode)
-   [**IWMReaderAdvanced2::GetProtocolName**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname)
-   [**IWMReaderAdvanced2::SetLogClientID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid)
-   [**IWMReaderAdvanced2::SetPlayMode**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setplaymode)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[Lesen von ASF-Dateien in DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 
