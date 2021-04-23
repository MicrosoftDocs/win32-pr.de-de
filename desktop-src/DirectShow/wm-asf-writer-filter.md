---
description: WM ASF Writer-Filter
ms.assetid: 1b12f65f-8d77-4d38-aad9-92bb15cc0426
title: WM ASF Writer Filter (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bf09a99673b07e88198fd57b95a766ce821eb02
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909278"
---
# <a name="wm-asf-writer-filter-directshow"></a>WM ASF Writer Filter (DirectShow)

Der WM ASF Writer ist ein Wrapperfilter für das Writer-Objekt, das mit dem Windows Media™ Format SDK bereitgestellt wird. Der Filter akzeptiert eine variable Anzahl von Eingabestreams und erstellt eine ASF-Datei (Advanced Systems Format). Der Filter verarbeitet alle Komprimierungen und Multiplexings (obwohl der Komprimierungsmechanismus umgangen werden kann). Sie können den WM ASF Writer in verschiedenen Szenarien verwenden, einschließlich der Erfassung digitaler Videos (DV), der Audiorekomprimierung und der Konvertierung von Audio-Video Interleaved (AVI) oder MPEG-Multimediadateien für das Netzwerkstreaming. Dieser Filter bietet die einzige Möglichkeit zum Erstellen von Microsoft® Windows Media™ Audio- und Windows Media Video-Dateien in Microsoft DirectShow.

Weitere Informationen finden Sie unter [Erstellen von ASF-Dateien in DirectShow.](creating-asf-files-in-directshow.md)



| Bezeichnung | Wert |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filtern von Schnittstellen                        | [**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter), [**IConfigAsfWriter2**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iconfigasfwriter2), [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), **IPersistStream**, **IServiceProvider**, **ISpecifyPropertyPages** Darüber hinaus macht der Filter die folgenden Windows Media Format SDK-Schnittstellen verfügbar: **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2**<br/> |
| Eingabepin-Medientypen                    | Hängt vom ASF-Profil ab. In der Regel unkomprimierte Audio- und Videotypen, obwohl der Filter komprimierte Typen akzeptiert, wenn sie mit dem ASF-Profil übereinstimmen.                                                                                                                                                                                                                                                                                                                                             |
| Eingabepinschnittstellen                     | [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass), [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), **IServiceProvider** Zusätzlich macht der Pin die folgende Windows Media Format SDK-Schnittstelle verfügbar: **IWMStreamConfig2** (über **IServiceProvider**)<br/>                                                                                                                                                                                 |
| Ausgabepin-Medientypen                   | Nicht zutreffend                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Schnittstellen für Ausgabepins                    | Nicht zutreffend                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Filtern der CLSID                             | CLSID \_ WMAsfWriter                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| CLSID der Eigenschaftenseite                      | CLSID \_ AsfWriterProperties                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Ausführbare Datei                               | Qasf.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [Verdienst](merit.md)                       | NOT USE (NICHT \_ \_ \_ VERWENDEN)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [Filterkategorie](filter-categories.md) | Nicht angegeben                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="remarks"></a>Bemerkungen

Der Filter erfordert das Windows Media Format Software Development Kit (SDK) und die zugrunde liegenden Abhängigkeiten.

Die Anzahl der Eingabepins für den Filter, abhängig vom Profil- oder Profilbezeichner des ASF-Streams.

Die Eingabepins unterstützen eine Methode der **IAMStreamConfig-Schnittstelle:** [**IAMStreamConfig::GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat). Alle anderen Methoden geben E \_ NOTIMPL zurück. Rufen Sie die **GetFormat-Methode** auf, um das Zielkomprimierungsformat des Pins abzufragen, das durch das aktuelle ASF-Profil definiert wird. Verwenden Sie die [**IConfigAsfWriter-Schnittstelle,**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) um das Profil festzulegen.

Sie können die **IServiceProvider-Schnittstelle** des Filters verwenden, um einen Zeiger auf die **IWMWriterAdvanced2-Schnittstelle** abzurufen, die im Windows Media Format SDK definiert ist. Sie können die **IWMWriterAdvanced2-Schnittstelle** verwenden, um das Videodeinterlacing zu steuern, wenn das Quellvideo per Interlacing übertragen wird. Um den Deinterlacingmodus festzulegen, rufen **Sie IWMWriterAdvanced2::SetInputSetting auf.** Verwenden Sie für den *dwInputNum-Parameter* den nullbasierten Index des Videoeingabepins, wie von der [**IEnumPins-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) aufgeführt.

Das folgende Beispiel zeigt, wie diese Schnittstelle abgefragt wird:


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



Anwendungen sollten keine der **IWMWriterAdvanced-Methoden** verwenden, die die **IWMWriterAdvanced2-Schnittstelle** erbt. Wenn Sie diese Methoden aufrufen, kann dies mit dem Vorgang des Filters zusammenpassen.

Der einzige Dateischreibmodus, der von diesem Filter unterstützt wird, ist AM \_ FILE \_ OVERWRITE. Siehe [**IFileSinkFilter2::GetMode**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter2-getmode).

Wenn die Windows Media Format SDK-Runtime WMT STATUS-Nachrichten an den WM ASF Writer-Filter sendet, leitet der Filter sie als \_ [**EC \_ WMT \_ EVENT-Ereignisse**](ec-wmt-event.md) weiter.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 




