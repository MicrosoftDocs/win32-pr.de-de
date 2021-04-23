---
description: DMO-Wrapperfilter
ms.assetid: ffa6234d-9040-4838-8f51-0cf87df40a5c
title: DMO-Wrapperfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d29c5b86bdff4a215ec2ef5854d09a1f842dbf0e
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908628"
---
# <a name="dmo-wrapper-filter"></a>DMO-Wrapperfilter

Der DMO-Wrapperfilter ermöglicht einer DirectShow-Anwendung die Verwendung eines [DirectX Media Object](directx-media-objects.md) (DMO) in einem Filterdiagramm. Der Filter umschließt den DMO und verarbeitet alle Details der Verwendung von DMO, z. B. das Übergeben von Daten an und von DMO. Außerdem aggregiert der Filter die DMO, sodass die Anwendung den Filter nach allen COM-Schnittstellen abfragen kann, die der DMO verfügbar macht.



| Bezeichnung | Wert |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filterschnittstellen                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter), [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream)                                                                                                                       |
| Eingabepin-Medientypen                    | Weitere Informationen finden Sie unter Hinweise.                                                                                                                                                                                                                                        |
| Eingabepinschnittstellen                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| Ausgabepin-Medientypen                   | Weitere Informationen finden Sie unter Hinweise.                                                                                                                                                                                                                                        |
| Ausgabe-PIN-Schnittstellen                    | [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Filtern der CLSID                             | CLSID \_ DMOWrapperFilter                                                                                                                                                                                                                            |
| Eigenschaftenseite CLSID                      | Keine Eigenschaftenseite                                                                                                                                                                                                                                   |
| Ausführbare Datei                               | Qasf.dll                                                                                                                                                                                                                                           |
| [Verdienst](merit.md)                       | Siehe Hinweise                                                                                                                                                                                                                                        |
| [Filterkategorie](filter-categories.md) | Siehe Hinweise                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a>Bemerkungen

### <a name="limitations"></a>Einschränkungen

Der DMO-Wrapper weist die folgenden Einschränkungen auf:

-   DMOs mit null Eingaben, mehreren Eingaben oder Nullausgaben werden nicht unterstützt. (DmOs mit einer Eingabe und mehreren Ausgaben werden unterstützt.)
-   Benutzerdefinierte Transporte werden nicht unterstützt. Der gesamte Datentransport erfolgt über die [**IMemInputPin-Schnittstelle.**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)
-   Die **IMediaObjectInPlace-Schnittstelle** wird nicht verwendet. die gesamte Verarbeitung erfolgt mithilfe von [**IMediaObject-Methoden.**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject)

### <a name="pins"></a>Pins

Für jeden Eingabestream im DMO erstellt der Filter einen entsprechenden Eingabepin. Für jeden Ausgabestream wird ein entsprechender Ausgabepin erstellt. Welche Medientypen von den einzelnen Pins unterstützt werden, hängt vom DMO ab.

### <a name="encoder-interfaces"></a>Encoderschnittstellen

Wenn der DMO ein Videoencoder oder Audioencoder ist, macht der Ausgabepin die [**IAMStreamConfig-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) verfügbar. Wenn der DMO ein Videoencoder ist, macht der Ausgabepin auch die [**IAMVideoCompression-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) verfügbar. Wenn DMO die -Schnittstelle unterstützt, delegiert der Pin in beiden Fällen an den DMO. Andernfalls stellt der Pin eine eigene Implementierung bereit.

### <a name="streaming"></a>Streaming

Der Filter verwendet die [**IMemInputPin-Schnittstelle,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) um das gesamte Streaming zu verarbeiten. [**IAsyncReader-Verbindungen werden nicht**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) unterstützt. Der Filter ruft [**IMediaObject::P rocessOutput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processoutput) nur dann auf, wenn Daten vom Upstream empfangen werden (einschließlich Benachrichtigungen zum Streamende). DmOs mit null Eingabestreams werden daher nicht unterstützt.

### <a name="seeking"></a>Suchen

Alle Suchanforderungen werden über den ersten Eingabepin im DMO-Wrapper an den Upstreamfilter übergeben. Bei DMOs mit mehreren Ausgaben bedeutet dies, dass der Upstreamfilter möglicherweise mehrere Suchanforderungen erhält, wenn die Anwendung das Diagramm sucht.

### <a name="merit"></a>Verdienst

DirectShow weist allen DMOs den Standardwert **NORMAL \_** + 0x800. Dieser Wert liegt zwischen **DEM NORMALWERT \_ UND** **DEM BEVORZUGTEN \_ WERT.** Decoderfilter haben in der Regel den Wert **FÜR NORMAL NORMAL \_**. Daher wählt der Filterdiagramm-Manager in der Regel einen DMO-Decoder über einem Decoderfilter aus. Fügen Sie dem Registrierungsschlüssel des DMO in HKEY CLASSES ROOT CLSID einen Registrierungseintrag hinzu, um den Standardwert des \_ \_ \\ Standardwerts zu überschreiben. Schließen Sie einen **DWORD-Wert** mit dem Namen "Zeichner" ein, dessen Wert den Zeichner angibt.

### <a name="category"></a>Category

Der DMO-Wrapperfilter wird nicht allein in einer Kategorie angezeigt. Wenn eine DMO umschließt wird, wird sie in der Kategorie DirectShow angezeigt, die der Kategorie des DMO unter dem Namen des DMO entspricht.

### <a name="buffers"></a>Puffer

Der DMO-Wrapperfilter übergibt Medienpuffer an DMO, die die [**IMediaBuffer-Schnittstelle**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) verfügbar machen.

In Windows Vista oder höher machen die Medienpuffer auch die IServiceProvider-Schnittstelle verfügbar. Der DMO kann diese Schnittstelle verwenden, um einen Zeiger auf das Medienbeispiel zu erhalten, das dem Puffer zugeordnet ist. Verwenden Sie den **IiD-Dienstbezeichner \_ IMediaSample**. Ein Video-DMO kann die [**IMediaSample2-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) des Medienbeispiels verwenden, um Interlace-Flags für das Beispiel zu setzen. Der folgende Code zeigt, wie Sie den Zeiger auf das Medienbeispiel abrufen:


```C++
IServiceProvider *pSp = NULL;
IMediaSample2 *pSample2 = NULL;
HRESULT hr = S_OK;

hr = pBuffer->QueryInterface(IID_IServiceProvider, (void**)&pSp);
if (SUCCEEDED(hr))
{
    hr = pSp->QueryService(
        IID_IMediaSample,  // Service identifier.
        IID_IMediaSample2, // Interface identifier.
        (void**)&pSample2
        );
    if (SUCCEEDED(hr))
    {
        // Set flags (not shown).
        pSample2->Release();
    }
    pSp->Release();
}
```



Weitere Informationen zu Pro-Sample-Interlace-Flags finden Sie unter [**AM \_ SAMPLE2 \_ PROPERTIES Structure**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties).

### <a name="quality-control"></a>Qualitätslenkung

Wenn der DMO die [**IDMOQualityControl-Schnittstelle**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-idmoqualitycontrol) verfügbar macht, übersetzt der Filter [**IQualityControl::Notify-Aufrufe**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) an seinem Ausgabepin in [**IDMOQualityControl::SetNow-Aufrufe**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-idmoqualitycontrol-setnow) für den DMO. Der *rtNow-Parameter* von **SetNow** wird als Summe der **Elemente TimeStamp** und **Late** der [**Quality-Struktur**](/windows/win32/api/strmif/ns-strmif-quality) berechnet.

### <a name="using-the-fiter-in-graphedit"></a>Verwenden von Fiter in GraphEdit

In GraphEdit wird der DMO-Wrapperfilter nicht unter seinem eigenen Namen angezeigt. Stattdessen wird jeder registrierte DMO unter der entsprechenden Filterkategorie aufgeführt. Wenn Sie einen DMO über das Dialogfeld **Filter einfügen** hinzufügen, erstellt GraphEdit den DMO-Wrapperfilter und konfiguriert ihn für die Verwendung dieses DMO.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[DirectX-Medienobjekte](directx-media-objects.md)
</dt> </dl>

 

 
