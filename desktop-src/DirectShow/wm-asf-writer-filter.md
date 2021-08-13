---
description: WM ASF Writer-Filter
ms.assetid: 1b12f65f-8d77-4d38-aad9-92bb15cc0426
title: WM ASF Writer Filter (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9281d09e609bd51bc0d0ab42291bd183e782df447e918d3c478e4e857063c21b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118650821"
---
# <a name="wm-asf-writer-filter-directshow"></a>WM ASF Writer Filter (DirectShow)

Der WM ASF Writer ist ein Wrapperfilter für das Writer-Objekt, das mit dem Windows Media™ Format SDK bereitgestellt wird. Der Filter akzeptiert eine variable Anzahl von Eingabestreams und erstellt eine ASF-Datei (Advanced Systems Format). Der Filter verarbeitet die Komprimierung und das Multiplexing (obwohl der Komprimierungsmechanismus umgangen werden kann). Sie können DEN WM ASF Writer in verschiedenen Szenarien verwenden, einschließlich der Aufnahme digitaler Videos (DV), der Audiorekomprimierung und der Konvertierung von Audio-Video Interleaved -Dateien (AVI) oder MPEG-Multimediadateien für das Netzwerkstreaming. Dieser Filter bietet die einzige Möglichkeit zum Erstellen von Microsoft® Windows Media™ Audio- und Windows Media Video-Dateien in Microsoft DirectShow.

Weitere Informationen finden Sie unter [Erstellen von ASF-Dateien in DirectShow.](creating-asf-files-in-directshow.md)



| Bezeichnung | Wert |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filtern von Schnittstellen                        | [**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter), [**IConfigAsfWriter2**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iconfigasfwriter2), [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), **IPersistStream**, **IServiceProvider**, **ISpecifyPropertyPages** Zusätzlich macht der Filter die folgenden Windows Media Format SDK-Schnittstellen verfügbar: **IWMIndexer2,** **IWMHeaderInfo,** **IWMWriterAdvanced2**<br/> |
| Eingabepin-Medientypen                    | Hängt vom ASF-Profil ab. In der Regel unkomprimierte Audio- und Videotypen, obwohl der Filter komprimierte Typen akzeptiert, wenn sie mit dem ASF-Profil übereinstimmen.                                                                                                                                                                                                                                                                                                                                             |
| Eingabepinschnittstellen                     | [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass), [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), **IServiceProvider** Zusätzlich macht der Pin die folgende Windows Media Format SDK-Schnittstelle verfügbar: **IWMStreamConfig2** (über **IServiceProvider**)<br/>                                                                                                                                                                                 |
| Ausgabepin-Medientypen                   | Nicht zutreffend                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Schnittstellen für Ausgabepins                    | Nicht zutreffend                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Filtern der CLSID                             | CLSID \_ WMAsfWriter                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Eigenschaftenseite CLSID                      | CLSID \_ AsfWriterProperties                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Ausführbare Datei                               | Qasf.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [Verdienst](merit.md)                       | NICHT \_ \_ VERWENDEN \_                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [Filterkategorie](filter-categories.md) | Nicht angegeben                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="remarks"></a>Hinweise

Der Filter erfordert das Windows Media Format Software Development Kit (SDK) und die zugrunde liegenden Abhängigkeiten.

Die Anzahl der Eingabepins für den Filter, abhängig vom Profil oder Profilbezeichner des ASF-Streams.

Die Eingabepins unterstützen eine Methode der **IAMStreamConfig-Schnittstelle:** [**IAMStreamConfig::GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat). Alle anderen Methoden geben E \_ NOTIMPL zurück. Rufen Sie die **GetFormat-Methode** auf, um das Zielkomprimierungsformat des Pins abfragt, das durch das aktuelle ASF-Profil definiert wird. Verwenden Sie die [**IConfigAsfWriter-Schnittstelle,**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) um das Profil festlegen.

Sie können die **IServiceProvider-Schnittstelle** des Filters verwenden, um einen Zeiger auf die **IWMWriterAdvanced2-Schnittstelle** zu erhalten, die im Windows Media Format SDK definiert ist. Sie können die **IWMWriterAdvanced2-Schnittstelle** verwenden, um das Videodeinterlacing zu steuern, wenn das Quellvideo verschachtelt wird. Rufen Sie zum Festlegen des Deinterlacingmodus **IWMWriterAdvanced2::SetInputSetting auf.** Verwenden Sie *für den dwInputNum-Parameter* den nullbasierten Index des Videoeingabepins, wie er von der [**IEnumPins-Schnittstelle aufzählt**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) wird.

Das folgende Beispiel zeigt, wie Sie diese Schnittstelle abfragen:


```C++
// Assume that pAsfWriter is a valid IBaseFilter pointer.
IServiceProvider *pProvider = NULL;
IWMWriterAdvanced2 *pWMWA2 = NULL;

hr = pAsfWriter->QueryInterface(
    IID_IServiceProvider, 
    (void**)&pProvider
    );
if (SUCCEEDED(hr))
{
    hr = pProvider->QueryService(
        IID_IWMWriterAdvanced2,
        IID_IWMWriterAdvanced2, 
        (void**)&pWMWA2
        );
    pProvider->Release();
    if (SUCCEEDED(hr))
    {
        // Use pWMWA2. (Not shown.)
        pWMWA2->Release();
    }
}
```



Anwendungen sollten keine der **IWMWriterAdvanced-Methoden** verwenden, die die **IWMWriterAdvanced2-Schnittstelle** erbt. Das Aufrufen dieser Methoden kann mit dem Vorgang des Filters interessieren.

Der einzige von diesem Filter unterstützte Dateischreibmodus ist AM \_ FILE \_ OVERWRITE. Siehe [**IFileSinkFilter2::GetMode**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter2-getmode).

Wenn die Windows Media Format SDK Runtime WMT STATUS-Nachrichten an den WM ASF Writer-Filter sendet, leitet der Filter sie als \_ [**EC \_ WMT \_ EVENT-Ereignisse**](ec-wmt-event.md) weiter.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 




