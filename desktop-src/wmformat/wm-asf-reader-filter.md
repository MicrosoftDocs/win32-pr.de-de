---
title: WM-ASF-Reader-Filter (Windows Media Format 11 SDK)
description: WM-ASF-Lesefilter
ms.assetid: 3d5ca88a-86bd-4d84-b4f4-782564ced58d
keywords:
- Windows Media-Format-SDK, WM-ASF-Reader
- DirectShow, WM-ASF-Reader
- Qasf-Filter, WM-ASF-Reader
- WM-ASF-Reader
- Advanced Systems Format (ASF), WM-ASF-Reader
- ASF (Advanced Systems Format), WM-ASF-Reader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e13b7944f45b850a158c9832e174ae5ec7dce4d6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739384"
---
# <a name="wm-asf-reader-filter-windows-media-format-11-sdk"></a>WM-ASF-Reader-Filter (Windows Media Format 11 SDK)

Wenn der Name einer ASF-Datei oder einer URL angegeben wird, liest der WM-ASF-Reader den komprimierten Inhalt, analysiert die Streams und macht für jeden eine Ausgabe-PIN verfügbar. Mit diesem Filter wird eine Downstream-Verbindung mit dem Windows Media Audio oder Windows Media Video DMOS hergestellt, die die Komprimierung durchführen. Die Suche wird unterstützt, wenn die ASF-Datei suchbar ist. Der WM-ASF-Reader wendet Zeitstempel auf die Medien Beispiele basierend auf dem Zeitstempel in der ASF-Datei an, ändert jedoch nicht die Zeitstempel. Intern verwendet der Filter das Windows Media-Format Reader-Objekt, um den Windows Media – basierten Inhalt zu lesen.

> [!Note]  
> Im DirectX SDK ist dieser Filter nicht der Standard Quell Filter für ASF-Dateien, sodass Sie mit diesem SDK diesen Filter nicht mit der **RenderFile** -Methode verwenden können. Sie müssen es explizit dem Filter Diagramm hinzufügen, indem Sie die zugehörige Klassen-ID (Class Identifier, CLSID) verwenden. Dieses Verhalten unterscheidet sich vom Windows Media-Format-SDK. Wenn Sie die Windows Media Format SDK-Laufzeitbibliotheken installieren, wird der WM-ASF-Reader als Standardfilter für ASF-Dateien registriert.

 

Die folgende Tabelle enthält Informationen zum WM-ASF-Reader-Filter, z. b. die Schnittstellen und die unterstützten Medientypen.



|                        |                                                                                                                                                                                                                                               |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filter Schnittstellen      | **Ibasefilter**, **IFileSourceFilter**, **IServiceProvider**, **iwmheaderinfo**, **iwmreaderadvanced** (teilweise implementiert. Weitere Informationen finden Sie unter "Hinweise".), **IWMReaderAdvanced2** (teilweise implementiert), **iwmdrmreader** (über **IServiceProvider**) |
| Eingabe-PIN-Medientypen  | Nicht verfügbar                                                                                                                                                                                                                                |
| PIN-Eingabeschnittstellen   | Nicht verfügbar                                                                                                                                                                                                                                |
| Ausgabe-PIN-Medientypen | MediaType \_ -Video, MediaType \_ -Audiodatei, MediaType \_ ScriptCommand, MediaType \_ Filetransfer                                                                                                                                                         |
| Formattyp            | **VIDEOINFOHEADER2** , wenn der Inhalt mit Zeilen Sprung [*verknüpft*](wmformat-glossary.md)ist, andernfalls **videoinfoheader** .                                                                                                                    |
| PIN-Schnittstellen  | **Imediaseeking**, **iamwmbufferpass**, **IServiceProvider**, **IWMStreamConfig2** (über **IServiceProvider**)                                                                                                                             |
| CLSID Filtern           | CLSID- \_ wmasfreader                                                                                                                                                                                                                            |
| CLSID der Eigenschaften Seite    | Keine Eigenschaften Seite                                                                                                                                                                                                                              |
| Ausführbare Datei             | Qasf.dll                                                                                                                                                                                                                                      |
| Verdienst                  | nicht \_ wahrscheinlich                                                                                                                                                                                                                               |
| Filter Kategorie        | CLSID \_ legacyamfiltercategory                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Bemerkungen

Der WM-ASF-Reader implementiert teilweise die **iwmreaderadvanced** -und **IWMReaderAdvanced2** -Schnittstellen, um Anwendungen den Zugriff auf die Informationsmethoden für das Reader-Objekt zu erhalten. Die Implementierung des Filters übergibt die Aufrufe einfach an die-Schnittstelle des Reader-Objekts. Die Streamingmethoden werden nicht implementiert, da der Filter über eine umfassende Kontrolle über den streamingprozess verfügen muss. Die folgenden **iwmreaderadvanced** -und **IWMReaderAdvanced2** -Methoden werden implementiert:

-   [**Iwmreaderadvanced:: getstatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics)
-   [**Iwmreaderadvanced:: setClientInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo)
-   [**IWMReaderAdvanced2:: getbufferprogress**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress)
-   [**IWMReaderAdvanced2:: getdownloadprogress**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress)
-   [**IWMReaderAdvanced2:: getplaymode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode)
-   [**IWMReaderAdvanced2:: getprotocolname**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname)
-   [**IWMReaderAdvanced2:: setlogclientid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid)
-   [**IWMReaderAdvanced2:: setplaymode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setplaymode)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**DirectShow-qasf-Referenz**](directshow-qasf-reference.md)
</dt> <dt>

[**Lesen von ASF-Dateien in DirectShow**](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 




