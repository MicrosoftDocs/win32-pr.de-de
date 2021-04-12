---
description: Windows Media-Quell Filter
ms.assetid: e59b3086-4f62-4541-8bef-b0581f01906f
title: Windows Media-Quell Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe60a038cfd5109a5c55ca6c40640d39b2426d3a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104218975"
---
# <a name="windows-media-source-filter"></a>Windows Media-Quell Filter

Dieser Filter ist der Legacy-Quell Filter für Windows Media®-Inhalt. Sie wird von Windows Media Player 6,4 verwendet. Im Allgemeinen ist die einfachste und zuverlässigste Methode zur Verwendung dieses Filters die Verwendung des ActiveX-Steuer Elements Windows Media Player 6,4. Viele der Methoden, die von diesem Filter verfügbar gemacht werden, werden auch über das ActiveX-Steuerelement verfügbar gemacht. Weitere Informationen finden Sie unter Windows Media Player SDK.

Wenn diesem Filter der Name einer lokalen ASF-Datei oder eine URL für eine Remote Datei zugewiesen wird, liest er die Datei, analysiert die komprimierten Streams und erstellt eine Ausgabe-PIN für jede einzelne Datei. Dieser Filter verwendet nicht das Windows Media-Format-SDK. Es verwendet die installierbaren Codec-Versionen der Windows Media-Decoders, nicht die DMO-Versionen. Die audioausgabepin stellt immer eine Verbindung mit dem ASF-ACM-HandlerFilter her, und die Videopin stellt immer eine Verbindung mit dem ASF-ICM (ICM bezieht sich in diesem Fall auf den ursprünglichen Namen des Video Komprimierungs-Managers.) Der Filter unterstützt keine Suchvorgänge.

Das folgende Diagramm zeigt ein Filter Diagramm mit diesem Filter.

![Diagramm für Windows Media-Quell Filter](images/wms-wmv-graph.png)

Um die Abwärtskompatibilität mit Windows Media Player 6,4 zu gewährleisten, ist dieser Filter der Standard Quell Filter für Dateien mit den Dateierweiterungen. WMA,. WMV und. ASF. Bei der Wiedergabe von Dateien sollten neuere Anwendungen den [WM-ASF-Reader](wm-asf-reader-filter.md) -Filter verwenden. Der WM-ASF-Reader unterstützt die Wiedergabe von gestreuten Inhalten jedoch nicht.

Die einfachste Möglichkeit für eine Anwendung, auf Windows Media basierende Inhalte zu übertragen, ist die Verwendung des Windows Media Player SDK. Eine andere Möglichkeit ist die Verwendung des Windows Media SDK-SDKs. Es wird nicht empfohlen, einen benutzerdefinierten Player auf der Grundlage des Windows-Quell Filters für Medien zu erstellen.



|                                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filter Schnittstellen                        | [**Ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**iamchannelinfo**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamchannelinfo), [**iamextendedseeking**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamextendedseeking), [**iammediacontent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**iamopenprogress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress), [**iamnetshowconfig**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowconfig), [**iamnetshowex-**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowexprops)Eigenschaften, [**iamnetshowpreroll**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowpreroll), [**iamnetworkstatus**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetworkstatus), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) |
| Eingabe-PIN-Medientypen                    | Nicht zutreffend                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| PIN-Eingabeschnittstellen                     | Nicht zutreffend                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Ausgabe-PIN-Medientypen                   | Variiert je nach den Datenströmen innerhalb der ASF-Datei.                                                                                                                                                                                                                                                                                                                                                                                                               |
| PIN-Schnittstellen                    | [**Imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)                                                                                                                                                                                                                                                                                                                                                                                                                             |
| CLSID Filtern                             | Siehe Hinweise                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Ausführbare Datei                               | dxmasf.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [Verdienst](merit.md)                       | Verdienst \_ Normal                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [Filter Kategorie](filter-categories.md) | CLSID \_ legacyamfiltercategory                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="remarks"></a>Bemerkungen

Die CLSID des Filters ist nicht in "qnetwork. h" definiert. Verwenden Sie dieses Makro in ihrer eigenen Header Datei:


```C++
//  {6B6D0800-9ADA-11d0-A520-00A0D10129C0}
DEFINE_GUID(CLSID_NetShowSource, 
0x6b6d0800, 0x9ada, 0x11d0, 0xa5, 0x20, 0x0, 0xa0, 0xd1, 0x1, 0x29, 0xc0);
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[Lesen von ASF-Dateien in DirectShow](reading-asf-files-in-directshow.md)
</dt> <dt>

[WM-ASF-Lesefilter](wm-asf-reader-filter.md)
</dt> </dl>

 

 



