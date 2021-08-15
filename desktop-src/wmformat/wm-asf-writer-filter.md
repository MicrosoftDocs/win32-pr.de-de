---
title: WM ASF Writer Filter (Windows Media Format 11 SDK)
description: Erfahren Sie mehr über den WM ASF Writer-Filter für das Windows Media Format 11 SDK. Überprüfen Sie die Filterinformationen, und sehen Sie sich verwandte Themen an.
ms.assetid: a902c92e-836d-492c-b2d2-89c216125774
keywords:
- Windows Medienformat-SDK, WM ASF Writer
- DirectShow, WM ASF Writer
- QASF-Filter, WM ASF Writer
- WM ASF Writer,about
- Advanced Systems Format (ASF), WM ASF Writer
- ASF (Advanced Systems Format), WM ASF Writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5182de3bc171a6c70afa03aea32d18c86c174fde0bbc6a2594f31cf41d0f250a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963809"
---
# <a name="wm-asf-writer-filter-windows-media-format-11-sdk"></a>WM ASF Writer Filter (Windows Media Format 11 SDK)

Der WM ASF Writer-Filter akzeptiert eine variable Anzahl von Eingabestreams und erstellt eine ASF-Datei. Der Filter verarbeitet alle Komprimierungen und Multiplexings (obwohl der Komprimierungsmechanismus umgangen werden kann). Sie können den WM ASF Writer-Filter in verschiedenen Szenarien verwenden, einschließlich der Erfassung digitaler Videos (DV), der Audiorekomprimierung und der Konvertierung von Audio-Video Interleaved -Dateien (AVI) oder MPEG-Digitalmediendateien für das Netzwerkstreaming. Dieser Filter stellt die einzige Möglichkeit zum Erstellen von Microsoft Windows Media Audio- und Windows Media Video-Dateien in DirectShow zur Verfügung.

Weitere Informationen finden Sie unter [Erstellen von ASF-Dateien in DirectShow.](creating-asf-files-in-directshow.md)

Die folgende Tabelle enthält Informationen zum WM ASF Writer-Filter, z. B. die unterstützten Schnittstellen und Medientypen.



| Filterinformationen                       |  Typen                                                                                                                                                                                                                       |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filtern von Schnittstellen      | **IAMFilterMiscFlags**, **IBaseFilter**, **IConfigAsfWriter**, **IFileSinkFilter2**, IMediaSeeking, IPersistStream, IServiceProvider, ISpecifyPropertyPages, **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2** |
| Eingabepin-Medientypen  | Abhängig vom Profil. In der Regel unkomprimierte Typen wie MEDIATYPE Audio oder MEDIATYPE Video, obwohl komprimierte Typen akzeptiert werden können, wenn \_ sie mit dem Profil \_ übereinstimmen                                                   |
| Eingabepinschnittstellen   | **IPin**, **IMemInputPin**, **IAMStreamConfig**, **IServiceProvider**, **IAMWMBufferPass**, **IWMStreamConfig2** (über **IServiceProvider**)                                                                         |
| Ausgabepin-Medientypen | Nicht verfügbar                                                                                                                                                                                                          |
| Schnittstellen für Ausgabepins  | Nicht verfügbar                                                                                                                                                                                                          |
| Filtern der CLSID           | CLSID \_ WMAsfWriter                                                                                                                                                                                                      |
| Eigenschaftenseite CLSID    | CLSID \_ WMAsfWriterProperties                                                                                                                                                                                            |
| Ausführbare Datei             | Qasf.dll                                                                                                                                                                                                                |
| Verdienst                  | NICHT \_ \_ VERWENDEN \_                                                                                                                                                                                                     |
| Filterkategorie        | Nicht angegeben                                                                                                                                                                                                           |



 

## <a name="remarks"></a>Hinweise

Die Anzahl der Eingabepins für den Filter hängt vom Profil ab, das an den Filter übergeben wird. Für jeden im Profil definierten Stream wird ein Pin des entsprechenden Medientyps erstellt.

Die Eingabepins unterstützen eine Methode der **IAMStreamConfig-Schnittstelle:** **IAMStreamConfig::GetFormat**. Alle anderen Methoden geben E \_ NOTIMPL zurück. Rufen Sie die **GetFormat-Methode** auf, um das Zielkomprimierungsformat des Pins abfragt, das durch das aktuelle Profil definiert wird. Verwenden Sie die [**IConfigAsfWriter-Schnittstelle,**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) um das Profil festlegen.

Die **IServiceProvider-Schnittstelle** des Filters ermöglicht Anwendungen das Abrufen der [**IWMWriterAdvanced2-Schnittstelle,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) die im Windows Media Format SDK definiert ist. Die **IWMWriterAdvanced2-Schnittstelle** steuert das Videodeinterlacing und [](wmformat-glossary.md) ist nützlich, wenn es sich bei der Eingabe um eine Verschachtelungsquelle handelt, z. B. DV (digitales Video). Verwenden Sie **die Methoden GetInputSetting** und **SetInputSetting,** um das Deinterlacing zu steuern. Es wird nicht empfohlen, dass Clients eine der anderen Methoden auf dieser Schnittstelle verwenden. Diese Schnittstelle kann erst nach dem Hinzufügen des Filters zum Filterdiagramm ermittelt werden. Das folgende Beispiel zeigt, wie Sie diese Schnittstelle abfragen:


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

[**DirectShow QASF-Referenz**](directshow-qasf-reference.md)
</dt> </dl>

 

 
