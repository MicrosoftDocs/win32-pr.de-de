---
description: Windows Medienquellfilter
ms.assetid: e59b3086-4f62-4541-8bef-b0581f01906f
title: Windows Medienquellfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb1e617a51095aec7cb409e46ba8f19f14f76fcd6f8d8a9bffeaa13843b1728b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982205"
---
# <a name="windows-media-source-filter"></a>Windows Medienquellfilter

Dieser Filter ist der Legacyquellfilter für Windows Medieninhalt®. Sie wird von Windows Media Player 6.4 verwendet. Im Allgemeinen ist die einfachste und zuverlässigste Möglichkeit zur Verwendung dieses Filters die Verwendung des Windows Media Player 6.4 ActiveX-Steuerelements. Viele der von diesem Filter verfügbar gemachten Methoden werden auch über das ActiveX-Steuerelement verfügbar gemacht. Weitere Informationen finden Sie im Windows Media Player SDK.

Wenn dieser Filter den Namen einer lokalen ASF-Datei oder einer URL für eine Remotedatei erhält, liest er die Datei, analysiert die komprimierten Datenströme und erstellt einen Ausgabepin für jeden. Dieser Filter verwendet nicht das Windows Media Format SDK. Es werden die installierbaren Codecversionen der Windows Mediendecoder verwendet, nicht die DMO Versionen. Der Audioausgabepin stellt immer eine Verbindung mit dem ASF-ACM-Handlerfilter her, und der Videopin stellt immer eine Verbindung mit dem ASF ICM Handler her. (ICM bezieht sich in diesem Fall auf den ursprünglichen Namen des Videokomprimierungs-Managers.) Der Filter unterstützt keine Suchabfragen.

Das folgende Diagramm zeigt ein Filterdiagramm mit diesem Filter.

![Windows-Medienquellfilterdiagramm](images/wms-wmv-graph.png)

Um die Abwärtskompatibilität mit Windows Media Player 6.4 aufrechtzuerhalten, ist dieser Filter der Standardquellfilter für Dateien mit WMA-, WMV- und ASF-Dateierweiterungen. Für die Dateiwiedergabe sollten neuere Anwendungen den [WM ASF-Readerfilter](wm-asf-reader-filter.md) verwenden. Der WM ASF-Reader unterstützt jedoch keine Wiedergabe von gestreamten Inhalten.

Die einfachste Möglichkeit für eine Anwendung, gestreamte Windows medienbasierten Inhalt wiederzuspielen, ist die Verwendung des Windows Media Player SDK. Eine weitere Option ist die Verwendung des Windows Media Format SDK. Es wird nicht empfohlen, einen benutzerdefinierten Player basierend auf dem Windows Medienquellenfilter zu erstellen.



| Bezeichnung | Wert |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filterschnittstellen                        | [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IAMChannelInfo,**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamchannelinfo) [**IAMExtendedSeeking,**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamextendedseeking) [**IAMMediaContent,**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent) [**IAMOpenProgress,**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress) [**IAMNetShowConfig,**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowconfig) [**IAMNetShowExProps,**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowexprops) [**IAMNetShowPreroll,**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowpreroll) [**IAMNetworkStatus,**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetworkstatus) [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) |
| Eingabepinmedientypen                    | Nicht zutreffend                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Eingabepinschnittstellen                     | Nicht zutreffend                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Medientypen des Ausgabepins                   | Variiert abhängig von den Streams in der ASF-Datei.                                                                                                                                                                                                                                                                                                                                                                                                               |
| Ausgabepinschnittstellen                    | [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Filtern von CLSID                             | Siehe Hinweise                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Ausführbare Datei                               | dxmasf.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [Verdienst](merit.md)                       | NORMALER WERT \_                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [Filterkategorie](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="remarks"></a>Hinweise

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

 

 



