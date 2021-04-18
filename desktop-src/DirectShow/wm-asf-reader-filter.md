---
description: WM-ASF-Lesefilter
ms.assetid: 82b9f849-b9dc-439b-8ca7-9dcd992338ab
title: WM-ASF-Lesefilter (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3df563667ed614a238e8fb31e08a2d71c721c2b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216390"
---
# <a name="wm-asf-reader-filter-directshow"></a>WM-ASF-Lesefilter (DirectShow)

Der WM-Decoder-Reader ist ein Wrapper Filter für das Reader-Objekt, das mit dem Windows Media SDK-SDK bereitgestellt wird. es ist der empfohlene Quell Filter für die Dateiwiedergabe von Windows Media-basierten Inhalten und Inhalten, die mit einem der Microsoft MPEG-4 Encoder-DMOS erstellt wurden.



|                                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filter Schnittstellen                        | [**Ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter), [**iamextendedseeking**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamextendedseeking), **IServiceProvider** Zusätzlich stellt der Filter die folgenden Windows Media-Format-SDK-Schnittstellen bereit: [**iwmheaderinfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo), [**iwmreaderadvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced), [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2), [**iwmdrmreader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) (über **IServiceProvider**)<br/> |
| Eingabe-PIN-Medientypen                    | Nicht zutreffend                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| PIN-Eingabeschnittstellen                     | Nicht zutreffend                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Ausgabe-PIN-Medientypen                   | MediaType \_ -Video, MediaType \_ -Audiodatei, MediaType \_ ScriptCommand, MediaType \_ Filetransfer                                                                                                                                                                                                                                                                                                                                                                                                     |
| PIN-Schnittstellen                    | [**Imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**iamwmbufferpass**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass), **IServiceProvider** zusätzlich machen die Pins die folgenden Windows Media-Format-SDK-Schnittstellen verfügbar: **IWMStreamConfig2** (über **IServiceProvider**)<br/>                                                                                                                                                                                                                                    |
| CLSID Filtern                             | CLSID- \_ wmasfreader                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| CLSID der Eigenschaften Seite                      | Keine Eigenschaften Seite.                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Ausführbare Datei                               | Qasf.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [Verdienst](merit.md)                       | nicht \_ wahrscheinlich                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [Filter Kategorie](filter-categories.md) | CLSID \_ legacyamfiltercategory                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="remarks"></a>Bemerkungen

Wenn der Name einer ASF-Datei oder einer URL angegeben wird, liest der WM-ASF-Reader den komprimierten Inhalt, analysiert die komprimierten Streams und macht für jeden eine Ausgabe-PIN verfügbar. Mit diesem Filter wird eine Downstream-Verbindung mit den Filtern von Audiodaten und/oder Video Codecs hergestellt, die die Komprimierung ausführen. Die Suche wird unterstützt, wenn die ASF-Datei suchbar ist. Der ASF-Reader fügt die Stichproben vor dem Senden nach dem downstreamvorgang ab, ändert jedoch nicht die Zeitstempel.

Die Wiedergabe mit einer anderen Geschwindigkeit als 1,0 (wie in [**imediaseeking::**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)* angegeben) wird nicht unterstützt.

Wenn die Windows Media-SDK-Laufzeit [**WMT- \_ Status**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_status) Meldungen an den WM-ASF-Writer-Filter sendet, leitet der Filter alle Nachrichten im Zusammenhang mit der DRM-Lizenz Übernahme als [**EC \_ WMT- \_ Ereignis**](ec-wmt-event.md) Ereignisse weiter Weitere Informationen finden Sie unter [Lesen von DRM-Protected-ASF-Dateien in DirectShow](reading-drm-protected-asf-files-in-directshow.md).

Der WM-ASF-Reader implementiert teilweise die [**iwmreaderadvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) -und [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) -Schnittstellen, um Anwendungen den Zugriff auf die Informationsmethoden für das Reader-Objekt zu erhalten. Die Implementierung des Filters übergibt die Aufrufe einfach an die-Schnittstelle des Reader-Objekts. Die Streamingmethoden werden nicht implementiert, da der Filter über eine umfassende Kontrolle über den streamingprozess verfügen muss. Die folgenden Methoden werden implementiert:

-   [**Iwmreaderadvanced:: getstatistics**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics)
-   [**Iwmreaderadvanced:: setClientInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo)
-   [**IWMReaderAdvanced2:: getbufferprogress**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress)
-   [**IWMReaderAdvanced2:: getdownloadprogress**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress)
-   [**IWMReaderAdvanced2:: getplaymode**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode)
-   [**IWMReaderAdvanced2:: getprotocolname**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname)
-   [**IWMReaderAdvanced2:: setlogclientid**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid)
-   [**IWMReaderAdvanced2:: setplaymode**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setplaymode)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[Lesen von ASF-Dateien in DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 
