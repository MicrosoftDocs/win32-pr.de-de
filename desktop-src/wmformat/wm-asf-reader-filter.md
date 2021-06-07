---
title: WM ASF-Readerfilter (Windows Media Format 11 SDK)
description: Erfahren Sie mehr über den WM ASF-Readerfilter.
ms.assetid: 3d5ca88a-86bd-4d84-b4f4-782564ced58d
keywords:
- Windows Media Format SDK, WM ASF-Reader
- DirectShow, WM ASF Reader
- QASF-Filter, WM ASF-Reader
- WM ASF-Reader
- Advanced Systems Format (ASF), WM ASF Reader
- ASF (Advanced Systems Format), WM ASF Reader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 421ab634a0d68837b22961b37005c5670d73e5fa
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444281"
---
# <a name="wm-asf-reader-filter-windows-media-format-11-sdk"></a>WM ASF-Readerfilter (Windows Media Format 11 SDK)

Wenn der Name einer ASF-Datei oder einer URL angegeben wird, liest der WM ASF-Reader den komprimierten Inhalt, analysiert die Datenströme und macht für jeden einen Ausgabepin verfügbar. Dieser Filter stellt eine Downstream-Verbindung mit Windows Media Audio- oder Windows Media Video-DMOs, die die Dekomprimierung anwenden. Die Suche wird unterstützt, wenn die ASF-Datei durchsuchbar ist. Der WM ASF-Reader wendet Zeitstempel auf die Medienbeispiele basierend auf dem Zeitstempel in der ASF-Datei an, ändert die Zeitstempel jedoch in irgendeiner Weise. Intern verwendet der Filter das Windows Media Format-Readerobjekt, um den Windows Media-basierten Inhalt zu lesen.

> [!Note]  
> Im DirectX SDK ist dieser Filter nicht der Standardquellenfilter für ASF-Dateien, sodass Sie diesen Filter mit diesem SDK nicht mit der **RenderFile-Methode verwenden** können. Sie müssen es dem Filterdiagramm explizit mithilfe seines Klassenbezeichners (CLSID) hinzufügen. Dieses Verhalten ist beim Windows Media Format SDK anders. Wenn Sie die Runtimebibliotheken des Windows Media Format SDK installieren, wird der WM ASF-Reader als Standardfilter für ASF-Dateien registriert.

 

Die folgende Tabelle enthält Informationen zum WM ASF-Readerfilter, z. B. die unterstützten Schnittstellen und Medientypen.



|  Filterinformationen                      |  Typen                                                                                                                                                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filtern von Schnittstellen      | **IBaseFilter**, **IFileSourceFilter**, **IServiceProvider**, **IWMHeaderInfo**, **IWMReaderAdvanced** (teilweise implementiert. Siehe Hinweise.), **IWMReaderAdvanced2** (teilweise implementiert), **IWMDRMReader** (über **IServiceProvider**) |
| Eingabepin-Medientypen  | Nicht verfügbar                                                                                                                                                                                                                                |
| Eingabepinschnittstellen   | Nicht verfügbar                                                                                                                                                                                                                                |
| Ausgabepin-Medientypen | MEDIATYPE \_ Video, MEDIATYPE \_ Audio, MEDIATYPE \_ ScriptCommand, MEDIATYPE \_ FileTransfer                                                                                                                                                         |
| Formattyp            | **VIDEOINFOHEADER2,** wenn der Inhalt mit [*Einem Interlacing verkettet ist,*](wmformat-glossary.md) **andernfalls VIDEOINFOHEADER**                                                                                                                    |
| Schnittstellen für Ausgabepins  | **IMediaSeeking**, **IAMWMBufferPass**, **IServiceProvider**, **IWMStreamConfig2** (über **IServiceProvider**)                                                                                                                             |
| Filtern der CLSID           | CLSID \_ WMAsfReader                                                                                                                                                                                                                            |
| Eigenschaftenseite CLSID    | Keine Eigenschaftenseite                                                                                                                                                                                                                              |
| Ausführbare Datei             | Qasf.dll                                                                                                                                                                                                                                      |
| Verdienst                  | WAHRSCHEINLICHKEIT \_ UNWAHRSCHEINLICH                                                                                                                                                                                                                               |
| Filterkategorie        | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Hinweise

Der WM ASF-Reader implementiert teilweise die **Schnittstellen IWMReaderAdvanced** und **IWMReaderAdvanced2,** um Anwendungen Zugriff auf die Informationsmethoden auf dem Readerobjekt zu geben. Die Implementierung des Filters übergibt die Aufrufe einfach an die -Schnittstelle des Readerobjekts. Die Streamingmethoden werden nicht implementiert, da der Filter die vollständige Kontrolle über den Streamingprozess haben muss. Die folgenden **IWMReaderAdvanced-** und **IWMReaderAdvanced2-Methoden** werden implementiert:

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

[**DirectShow QASF-Referenz**](directshow-qasf-reference.md)
</dt> <dt>

[**Lesen von ASF-Dateien in DirectShow**](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 




