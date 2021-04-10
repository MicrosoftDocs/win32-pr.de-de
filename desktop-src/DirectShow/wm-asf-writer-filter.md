---
description: WM-ASF-Writer-Filter
ms.assetid: 1b12f65f-8d77-4d38-aad9-92bb15cc0426
title: WM-ASF-Writer-Filter (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 672996124c88632228fff3a84525c9d47f2276b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130457"
---
# <a name="wm-asf-writer-filter-directshow"></a>WM-ASF-Writer-Filter (DirectShow)

Der WM-ASF-Writer ist ein Wrapper Filter für das Writer-Objekt, das mit dem Windows Media™ Format SDK bereitgestellt wird. Der Filter akzeptiert eine Variable Anzahl von Eingabedaten strömen und erstellt eine ASF-Datei (Advanced Systems Format). Der Filter verarbeitet alle Komprimierungen und Multiplexing (obwohl der Komprimierungs Mechanismus umgangen werden kann). Sie können den WM-ASF-Writer in verschiedenen Szenarien verwenden, einschließlich Digital Video (DV) Capture, audiorekomprimierung und Konvertierung von Audio-Video Interleaved (AVI) oder MPEG Multimedia-Dateien für das Netzwerk Streaming. Dieser Filter bietet die einzige Möglichkeit zum Erstellen von Microsoft® Windows Media™ Audiodateien und Windows Media Video Dateien in Microsoft DirectShow.

Weitere Informationen finden Sie unter [Erstellen von ASF-Dateien in DirectShow](creating-asf-files-in-directshow.md).



|                                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filter Schnittstellen                        | [**Iamfilterfehlflags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags), [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**iconfigasfwriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter), [**IConfigAsfWriter2**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iconfigasfwriter2), [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2), [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), **IPersistStream**, **IServiceProvider**, **ISpecifyPropertyPages** Zusätzlich stellt der Filter die folgenden Windows Media-Format-SDK-Schnittstellen bereit: **IWMIndexer2**, **iwmheaderinfo**, **IWMWriterAdvanced2**<br/> |
| Eingabe-PIN-Medientypen                    | Hängt vom ASF-Profil ab. In der Regel unkomprimierte Audiodaten und Video Typen, obwohl der Filter komprimierte Typen akzeptiert, wenn Sie dem ASF-Profil entsprechen.                                                                                                                                                                                                                                                                                                                                             |
| PIN-Eingabeschnittstellen                     | [**Iamstreamconfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**iamwmbufferpass**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass), [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), **IServiceProvider** Zusätzlich stellt die PIN die folgende Windows Media-Format-SDK-Schnittstelle bereit: **IWMStreamConfig2** (über **IServiceProvider**)<br/>                                                                                                                                                                                 |
| Ausgabe-PIN-Medientypen                   | Nicht zutreffend                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| PIN-Schnittstellen                    | Nicht zutreffend                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| CLSID Filtern                             | CLSID- \_ wmasberwriter                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| CLSID der Eigenschaften Seite                      | CLSID- \_ asfscripterproperties                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Ausführbare Datei                               | Qasf.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [Verdienst](merit.md)                       | das Verdienst wird \_ \_ nicht \_ verwendet.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [Filter Kategorie](filter-categories.md) | Nicht angegeben                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="remarks"></a>Bemerkungen

Der Filter erfordert das Windows Media-Format Software Development Kit (SDK) und die zugrunde liegenden Abhängigkeiten.

Die Anzahl der Eingabe Pins in den Filter Abhängigkeiten für das Profil oder den Profil Bezeichner des ASF-Streams.

Die Eingabe Pins unterstützen eine Methode aus der **iamstreamconfig** -Schnittstelle: [**iamstreamconfig:: GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat). Alle anderen Methoden geben E \_ notimpl zurück. Aufrufen der **GetFormat** -Methode, um das Ziel Komprimierungs Format der PIN abzufragen, das durch das aktuelle ASF-Profil definiert wird. Verwenden Sie die [**iconfigasfwriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) -Schnittstelle, um das Profil festzulegen.

Sie können die **IServiceProvider** -Schnittstelle des Filters verwenden, um einen Zeiger auf die **IWMWriterAdvanced2** -Schnittstelle zu erhalten, die im SDK für den Windows Media-Format definiert ist. Sie können die **IWMWriterAdvanced2** -Schnittstelle verwenden, um das Video Deinterlacing zu steuern, wenn das Quellvideo mit Zeilen Sprung verknüpft ist. Um den Deinterlacing-Modus festzulegen, nennen Sie **IWMWriterAdvanced2:: setinputsetting**. Verwenden Sie für den *dwinputnum* -Parameter den NULL basierten Index der Videoeingabe-PIN, wie von der [**ienumpins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) -Schnittstelle aufgelistet.

Im folgenden Beispiel wird gezeigt, wie Sie diese Schnittstelle Abfragen:


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



Anwendungen sollten keine der **iwmbeschreiteradvanced** -Methoden verwenden, die von der **IWMWriterAdvanced2** -Schnittstelle geerbt werden. Der Aufruf dieser Methoden kann mit der Operation des Filters interagieren.

Der einzige von diesem Filter unterstützte Datei Schreibmodus ist das \_ über \_ Schreiben von Dateien. Weitere Informationen finden Sie unter [**IFileSinkFilter2:: getMode**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter2-getmode).

Wenn die Windows Media-Format-SDK-Laufzeit WMT- \_ Status Meldungen an den WM-ASF-Writer-Filter sendet, leitet der Filter Sie als [**EC \_ WMT- \_ Ereignis**](ec-wmt-event.md) Ereignisse weiter.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 




