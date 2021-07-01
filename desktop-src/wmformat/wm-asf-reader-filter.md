---
title: WM ASF-Readerfilter (Windows Media Format 11 SDK)
description: Erfahren Sie mehr über den WM ASF Reader-Filter für das Windows Media Format 11 SDK. Überprüfen Sie die Filterinformationen, und sehen Sie sich verwandte Themen an.
ms.assetid: 3d5ca88a-86bd-4d84-b4f4-782564ced58d
keywords:
- Windows Media Format SDK, WM ASF Reader
- DirectShow,WM ASF Reader
- QASF-Filter, WM ASF-Reader
- WM ASF Reader
- Advanced Systems Format (ASF), WM ASF Reader
- ASF (Advanced Systems Format), WM ASF Reader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26bde36b1b2cfa7644d6e75d8d1ff96260b2e457
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119645"
---
# <a name="wm-asf-reader-filter-windows-media-format-11-sdk"></a>WM ASF-Readerfilter (Windows Media Format 11 SDK)

Wenn der Name einer ASF-Datei oder einer URL angegeben wird, liest der WM ASF-Reader den komprimierten Inhalt, analysiert die Streams und macht einen Ausgabepin für jeden verfügbar. Dieser Filter stellt eine Downstreamverbindung mit den Windows Media Audio oder Windows Media Video DMOs her, die die Dekomprimierung durchführen. Suchen wird unterstützt, wenn die ASF-Datei gesucht werden kann. Der WM ASF-Reader wendet Zeitstempel auf die Medienbeispiele basierend auf dem Zeitstempel in der ASF-Datei an, ändert die Zeitstempel jedoch in keiner Weise. Intern verwendet der Filter das Windows Media Format-Readerobjekt, um den Windows Media-basierten Inhalt zu lesen.

> [!Note]  
> Im DirectX SDK ist dieser Filter nicht der Standardquellfilter für ASF-Dateien, sodass Sie mit diesem SDK diesen Filter nicht mit der **RenderFile-Methode** verwenden können. Sie müssen es dem Filterdiagramm explizit mithilfe seines Klassenbezeichners (CLSID) hinzufügen. Dieses Verhalten unterscheidet sich vom Windows Media Format SDK. Wenn Sie die Runtimebibliotheken des Windows Media Format SDK installieren, wird der WM ASF Reader als Standardfilter für ASF-Dateien registriert.

 

Die folgende Tabelle enthält Informationen zum WM ASF-Readerfilter, z. B. die unterstützten Schnittstellen und Medientypen.



|  Filterinformationen                      |  Typen                                                                                                                                                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filterschnittstellen      | **IBaseFilter**, **IFileSourceFilter**, **IServiceProvider**, **IWMHeaderInfo**, **IWMReaderAdvanced** (teilweise implementiert. Siehe Hinweise.), **IWMReaderAdvanced2** (teilweise implementiert), **IWMDRMReader** (über **IServiceProvider**) |
| Eingabepinmedientypen  | Nicht zutreffend                                                                                                                                                                                                                                |
| Eingabepinschnittstellen   | Nicht zutreffend                                                                                                                                                                                                                                |
| Medientypen des Ausgabepins | MEDIATYPE \_ Video, MEDIATYPE \_ Audio, MEDIATYPE \_ ScriptCommand, MEDIATYPE \_ FileTransfer                                                                                                                                                         |
| Formattyp            | **VIDEOINFOHEADER2,** wenn inhalt [*mit einem Zeilensprung verknüpft*](wmformat-glossary.md)ist, **andernfalls VIDEOINFOHEADER**                                                                                                                    |
| Ausgabepinschnittstellen  | **IMediaSeeking,** **IAMWMBufferPass,** **IServiceProvider,** **IWMStreamConfig2** (über **IServiceProvider**)                                                                                                                             |
| Filtern von CLSID           | CLSID \_ WMAsfReader                                                                                                                                                                                                                            |
| CLSID der Eigenschaftenseite    | Keine Eigenschaftenseite                                                                                                                                                                                                                              |
| Ausführbare Datei             | Qasf.dll                                                                                                                                                                                                                                      |
| Verdienst                  | \_UNWAHRSCHEINLICHE WAHRSCHEINLICHKEIT                                                                                                                                                                                                                               |
| Filterkategorie        | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Bemerkungen

Der WM ASF-Reader implementiert teilweise die Schnittstellen **IWMReaderAdvanced** und **IWMReaderAdvanced2,** um Anwendungen Zugriff auf die Informationsmethoden für das Readerobjekt zu gewähren. Die Implementierung des Filters übergibt einfach die Aufrufe an die Schnittstelle des Readerobjekts. Die Streamingmethoden werden nicht implementiert, da der Filter die vollständige Kontrolle über den Streamingprozess haben muss. Die folgenden **IWMReaderAdvanced-** und **IWMReaderAdvanced2-Methoden** werden implementiert:

-   [**IWMReaderAdvanced::GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics)
-   [**IWMReaderAdvanced::SetClientInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo)
-   [**IWMReaderAdvanced2::GetBufferProgress**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress)
-   [**IWMReaderAdvanced2::GetDownloadProgress**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress)
-   [**IWMReaderAdvanced2::GetPlayMode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode)
-   [**IWMReaderAdvanced2::GetProtocolName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname)
-   [**IWMReaderAdvanced2::SetLogClientID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid)
-   [**IWMReaderAdvanced2::SetPlayMode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setplaymode)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**DirectShow-QASF-Referenz**](directshow-qasf-reference.md)
</dt> <dt>

[**Lesen von ASF-Dateien in DirectShow**](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 




