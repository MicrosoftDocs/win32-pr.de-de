---
description: Windows-Medienquellenfilter
ms.assetid: e59b3086-4f62-4541-8bef-b0581f01906f
title: Windows-Medienquellenfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa8e2c2f2e575a70d85fdce3d9b8d643e270f721
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908998"
---
# <a name="windows-media-source-filter"></a>Windows-Medienquellenfilter

Dieser Filter ist der Legacyquellfilter für Windows Media®Inhalt. Sie wird von Windows Media Player 6.4 verwendet. Im Allgemeinen ist die einfachste und zuverlässigste Möglichkeit, diesen Filter zu verwenden, die Verwendung des activeX-Steuerelements Windows Media Player 6.4. Viele der von diesem Filter verfügbar gemachten Methoden werden auch über das ActiveX-Steuerelement verfügbar gemacht. Weitere Informationen finden Sie im Windows Media Player SDK.

Wenn dieser Filter den Namen einer lokalen ASF-Datei oder einer URL für eine Remotedatei erhält, liest er die Datei, analysiert die komprimierten Datenströme und erstellt einen Ausgabepin für jeden. Dieser Filter verwendet nicht das Windows Media Format SDK. Es werden die installierbaren Codecversionen der Windows Media-Decoder verwendet, nicht die DMO-Versionen. Der Audioausgabepin stellt immer eine Verbindung mit dem ASF-ACM-Handlerfilter her, und der Videopin stellt immer eine Verbindung mit dem ASF-ICM-Handler her. (ICM bezieht sich in diesem Fall auf den ursprünglichen Namen des Videokomprimierungs-Managers.) Der Filter unterstützt keine Suchabfragen.

Das folgende Diagramm zeigt ein Filterdiagramm mit diesem Filter.

![Windows-Medienquellfilterdiagramm](images/wms-wmv-graph.png)

Um die Abwärtskompatibilität mit Windows Media Player 6.4 aufrechtzuerhalten, ist dieser Filter der Standardquellfilter für Dateien mit WMA-, WMV- und ASF-Dateierweiterungen. Für die Dateiwiedergabe sollten neuere Anwendungen den [WM ASF-Readerfilter](wm-asf-reader-filter.md) verwenden. Der WM ASF-Reader unterstützt jedoch keine Wiedergabe von gestreamten Inhalten.

Die einfachste Möglichkeit für eine Anwendung, gestreamte Windows Media-basierte Inhalte wiederzuspielen, ist die Verwendung des Windows Media Player SDK. Eine weitere Option ist die Verwendung des Windows Media Format SDK. Es wird nicht empfohlen, einen benutzerdefinierten Player basierend auf dem Windows Media Source-Filter zu erstellen.



| Bezeichnung | Wert |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filtern von Schnittstellen                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IAMChannelInfo**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamchannelinfo), [**IAMExtendedSeeking**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamextendedseeking), [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IAMOpenProgress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress), [**IAMNetShowConfig**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowconfig), [**IAMNetShowExProps**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowexprops), [**IAMNetShowPreroll**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowpreroll), [**IAMNetworkStatus**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetworkstatus), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) |
| Eingabepin-Medientypen                    | Nicht zutreffend                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Eingabepinschnittstellen                     | Nicht zutreffend                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Ausgabepin-Medientypen                   | Variiert abhängig von den Streams in der ASF-Datei.                                                                                                                                                                                                                                                                                                                                                                                                               |
| Schnittstellen für Ausgabepins                    | [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Filtern der CLSID                             | Weitere Informationen finden Sie unter Hinweise.                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Ausführbare Datei                               | dxmasf.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [Verdienst](merit.md)                       | MERIT \_ NORMAL                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [Filterkategorie](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="remarks"></a>Bemerkungen

Die CLSID des Filters ist in qnetwork.h nicht definiert. Verwenden Sie dieses Makro in Ihrer eigenen Headerdatei:


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

[WM ASF-Leserfilter](wm-asf-reader-filter.md)
</dt> </dl>

 

 



