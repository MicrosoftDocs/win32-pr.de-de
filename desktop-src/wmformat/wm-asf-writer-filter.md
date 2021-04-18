---
title: WM-ASF-Writer-Filter (Windows Media Format 11 SDK)
description: WM-ASF-Writer-Filter
ms.assetid: a902c92e-836d-492c-b2d2-89c216125774
keywords:
- Windows Media-Format-SDK, WM-ASF-Writer
- DirectShow, WM-ASF-Writer
- Qasf-Filter, WM-ASF-Writer
- WM-ASF-Writer, Informationen zu
- Advanced Systems Format (ASF), WM-ASF-Writer
- ASF (Advanced Systems Format), WM-ASF-Writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d0de34bcf4b4047673f832d78f40377f98e94d6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106340551"
---
# <a name="wm-asf-writer-filter-windows-media-format-11-sdk"></a>WM-ASF-Writer-Filter (Windows Media Format 11 SDK)

Der WM-ASF-Writer-Filter akzeptiert eine Variable Anzahl von Eingabedaten strömen und erstellt eine ASF-Datei. Der Filter verarbeitet alle Komprimierungen und Multiplexing (obwohl der Komprimierungs Mechanismus umgangen werden kann). Sie können den WM-ASF-Writer-Filter in verschiedenen Szenarien verwenden, einschließlich digitaler Video Erfassung (DV), audioneukomprimierung und Konvertierung von Audio-Video Interleaved (AVI) oder MPEG Digital Media Files for Network Streaming. Dieser Filter stellt die einzige Möglichkeit zum Erstellen von Microsoft-Windows Media Audio und Windows Media Video Dateien in DirectShow dar.

Weitere Informationen finden Sie unter [Erstellen von ASF-Dateien in DirectShow](creating-asf-files-in-directshow.md).

Die folgende Tabelle enthält Informationen zum WM-ASF-Writer-Filter, z. b. die Schnittstellen und die unterstützten Medientypen.



|                        |                                                                                                                                                                                                                         |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filter Schnittstellen      | **Iamfilterfehlflags**, **ibasefilter**, **iconfigasfwriter**, **IFileSinkFilter2**, imediaseeking, IPersistStream, IServiceProvider, ISpecifyPropertyPages, **IWMIndexer2**, **iwmheaderinfo**, **IWMWriterAdvanced2** |
| Eingabe-PIN-Medientypen  | Abhängig vom Profil. In der Regel unkomprimierte Typen wie MediaType \_ -Audiodaten oder MediaType- \_ Video, obwohl komprimierte Typen akzeptiert werden können, wenn Sie dem Profil entsprechen.                                                   |
| PIN-Eingabeschnittstellen   | **IPin**, **IMemInputPin**, **iamstreamconfig**, **IServiceProvider**, **iamwmbufferpass**, **IWMStreamConfig2** (über **IServiceProvider**)                                                                         |
| Ausgabe-PIN-Medientypen | Nicht verfügbar                                                                                                                                                                                                          |
| PIN-Schnittstellen  | Nicht verfügbar                                                                                                                                                                                                          |
| CLSID Filtern           | CLSID- \_ wmasberwriter                                                                                                                                                                                                      |
| CLSID der Eigenschaften Seite    | CLSID \_ wmasf-Eigenschaften                                                                                                                                                                                            |
| Ausführbare Datei             | Qasf.dll                                                                                                                                                                                                                |
| Verdienst                  | das Verdienst wird \_ \_ nicht \_ verwendet.                                                                                                                                                                                                     |
| Filter Kategorie        | Nicht angegeben                                                                                                                                                                                                           |



 

## <a name="remarks"></a>Bemerkungen

Die Anzahl der Eingabe Pins im Filter hängt von dem Profil ab, das an den Filter weitergeleitet wird. Für jeden Stream, der im Profil definiert ist, wird eine PIN des entsprechenden Medientyps erstellt.

Die Eingabe Pins unterstützen eine Methode aus der **iamstreamconfig** -Schnittstelle: **iamstreamconfig:: GetFormat**. Alle anderen Methoden geben E \_ notimpl zurück. Aufrufen der **GetFormat** -Methode, um das Ziel Komprimierungs Format der PIN abzufragen, das durch das aktuelle Profil definiert wird. Verwenden Sie die [**iconfigasfwriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) -Schnittstelle, um das Profil festzulegen.

Die **IServiceProvider** -Schnittstelle des Filters ermöglicht Anwendungen das Abrufen der [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) -Schnittstelle, die im Windows Media-Format-SDK definiert ist. Die **IWMWriterAdvanced2** -Schnittstelle steuert das Video Deinterlacing und ist nützlich, wenn die [*Eingabe eine Zeilen*](wmformat-glossary.md) Sprung Quelle ist, z. b. DV (digitales Video). Verwenden Sie die **getinputsetting** -Methode und die-Methode für die **Einstellungs** Methode, um Deinterlacing zu steuern. Es wird nicht empfohlen, dass Clients eine andere Methode für diese Schnittstelle verwenden. Diese Schnittstelle kann nur abgerufen werden, nachdem dem Filter Diagramm der Filter hinzugefügt wurde. Im folgenden Beispiel wird gezeigt, wie Sie diese Schnittstelle Abfragen:


```C++
// Assume that m_pGraph is a valid IGraphBuilder interface pointer,
// and that pAsfWriter points to the IBaseFilter interface
// on the WM ASF Writer filter.

IServiceProvider *pProvider = NULL;
IWMWriterAdvanced2 *pWMWA2 = NULL;

hr = m_pGraph->AddFilter(pAsfWriter, L"WM ASF Writer");
...
hr = pAsfWriter->QueryInterface(IID_IServiceProvider, (void**)&pProvider)
if (SUCCEEDED(hr))
{
    hr = pProvider->QueryService(IID_IWMWriterAdvanced2,
        IID_IWMWriterAdvanced2, (void**)&pWMWA2);
    pProvider->Release();
}

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**DirectShow-qasf-Referenz**](directshow-qasf-reference.md)
</dt> </dl>

 

 
