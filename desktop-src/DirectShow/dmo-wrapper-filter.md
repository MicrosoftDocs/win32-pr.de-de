---
description: DMO Wrapperfilter
ms.assetid: ffa6234d-9040-4838-8f51-0cf87df40a5c
title: DMO Wrapperfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a13383e7539f478327f1a904d60fcd069692180239e76bcfd48bcc090a068e9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118653040"
---
# <a name="dmo-wrapper-filter"></a>DMO Wrapperfilter

Der DMO Wrapperfilter ermöglicht einer DirectShow-Anwendung [](directx-media-objects.md) die Verwendung eines DirectX-Medienobjekts (DMO) in einem Filterdiagramm. Der Filter umschließt die DMO und verarbeitet alle Details der Verwendung der DMO, z. B. das Übergeben von Daten an und DMO. Außerdem aggregiert der Filter die DMO, sodass die Anwendung den Filter für alle COM-Schnittstellen abfragen kann, die DMO verfügbar macht.



| Bezeichnung | Wert |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filterschnittstellen                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter), [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream)                                                                                                                       |
| Eingabepin-Medientypen                    | Siehe Hinweise                                                                                                                                                                                                                                        |
| Eingabepinschnittstellen                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| Ausgabepin-Medientypen                   | Siehe Hinweise                                                                                                                                                                                                                                        |
| Ausgabe-PIN-Schnittstellen                    | [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Filtern der CLSID                             | CLSID \_ DMOWrapperFilter                                                                                                                                                                                                                            |
| Eigenschaftenseite CLSID                      | Keine Eigenschaftenseite                                                                                                                                                                                                                                   |
| Ausführbare Datei                               | Qasf.dll                                                                                                                                                                                                                                           |
| [Verdienst](merit.md)                       | Siehe Hinweise                                                                                                                                                                                                                                        |
| [Filterkategorie](filter-categories.md) | Siehe Hinweise                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a>Hinweise

### <a name="limitations"></a>Einschränkungen

Der DMO Wrapper hat die folgenden Einschränkungen:

-   DMOs mit null Eingaben, mehreren Eingaben oder 0 Ausgaben werden nicht unterstützt. (DmOs werden mit einer Eingabe und mehreren Ausgaben unterstützt.)
-   Benutzerdefinierte Transporte werden nicht unterstützt. Der sämtliche Datentransport erfolgt über die [**IMemInputPin-Schnittstelle.**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)
-   Die **IMediaObjectInPlace-Schnittstelle wird nicht** verwendet. die Verarbeitung erfolgt mithilfe von [**IMediaObject-Methoden.**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject)

### <a name="pins"></a>Pins

Für jeden Eingabestream auf dem DMO erstellt der Filter einen entsprechenden Eingabepin. Für jeden Ausgabestream wird ein entsprechender Ausgabepin erstellt. Welche Medientypen von den einzelnen Pins unterstützt werden, hängt von der DMO

### <a name="encoder-interfaces"></a>Encoderschnittstellen

Wenn der DMO ein Videoencoder oder ein Audioencoder ist, macht der Ausgabepin die [**IAMStreamConfig-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) verfügbar. Wenn der DMO ein Videoencoder ist, macht der Ausgabepin auch die [**IAMVideoCompression-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) verfügbar. Wenn die Schnittstelle von der DMO unterstützt wird, wird die Pin in beiden Fällen an die DMO. Andernfalls stellt die Stecknadel eine eigene Implementierung zur Anwendung.

### <a name="streaming"></a>Streaming

Der Filter verwendet die [**IMemInputPin-Schnittstelle,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) um alle Streamings zu verarbeiten. [**IAsyncReader-Verbindungen werden nicht**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) unterstützt. Der Filter ruft [**IMediaObject::P rocessOut DMO put**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processoutput) nur dann auf, wenn daten vom Upstream empfangen werden (einschließlich Benachrichtigungen vom Streamende). Aus diesem Grund werden DMOs mit null Eingabestreams nicht unterstützt.

### <a name="seeking"></a>Suchen

Alle Suchanforderungen werden über den ersten Eingabepin auf dem DMO an den Upstreamfilter übergeben. Bei DMOs mit mehreren Ausgaben bedeutet dies, dass der Upstreamfilter möglicherweise mehrere Suchanforderungen erhält, wenn die Anwendung das Diagramm sucht.

### <a name="merit"></a>Verdienst

DirectShow weist allen DMOs den Standardwert **NORMAL \_** + 0x800. Dieser Wert liegt zwischen **DEM NORMALWERT \_ UND** **DEM BEVORZUGTEN \_ WERT.** Decoderfilter haben in der Regel den Wert **FÜR NORMAL NORMAL \_**. Daher wählt der Filterdiagramm-Manager in der Regel einen DMO decoder-Filter aus. Fügen Sie zum Überschreiben des Standardwerts einen Registrierungseintrag zum Registrierungsschlüssel DMO in HKEY \_ CLASSES \_ ROOT \\ CLSID hinzu. Schließen Sie einen **DWORD-Wert** mit dem Namen "Zeichner" ein, dessen Wert den Zeichner angibt.

### <a name="category"></a>Category

Der DMO Wrapperfilter wird nicht allein in einer Kategorie angezeigt. Wenn eine DMO umschließt, wird sie in der Kategorie DirectShow angezeigt, die der Kategorie DMO unter dem Namen des DMO.

### <a name="buffers"></a>Puffer

Der DMO Wrapperfilter übergibt Medienpuffer an die DMO die die [**IMediaBuffer-Schnittstelle verfügbar**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) machen.

In Windows Vista oder höher machen die Medienpuffer auch die IServiceProvider-Schnittstelle verfügbar. Der DMO kann diese Schnittstelle verwenden, um einen Zeiger auf das Medienbeispiel zu erhalten, das dem Puffer zugeordnet ist. Verwenden Sie den **IiD-Dienstbezeichner \_ IMediaSample**. Ein Video DMO die [**IMediaSample2-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) des Medienbeispiels verwenden, um Interlace-Flags für das Beispiel zu setzen. Der folgende Code zeigt, wie sie den Zeiger auf das Medienbeispiel erhalten:


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



Weitere Informationen zu Interlace-Flags pro Beispiel finden Sie unter [**AM \_ SAMPLE2 \_ PROPERTIES Structure**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties).

### <a name="quality-control"></a>Qualitätslenkung

Wenn der DMO die [**IDMOQualityControl-Schnittstelle**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-idmoqualitycontrol) verfügbar macht, übersetzt der Filter [**IQualityControl::Notify-Aufrufe**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) für seinen Ausgabepin in [**IDMOQualityControl::SetNow-Aufrufe**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-idmoqualitycontrol-setnow) auf dem DMO. Der *rtNow-Parameter* **von SetNow** wird als Summe der **TimeStamp-** und **Late-Elemente** der [**Quality-Struktur**](/windows/win32/api/strmif/ns-strmif-quality) berechnet.

### <a name="using-the-fiter-in-graphedit"></a>Verwenden von Fiter in GraphEdit

In GraphEdit wird der DMO Wrapperfilter nicht unter seinem eigenen Namen angezeigt. Stattdessen wird jeder registrierte DMO unter der entsprechenden Filterkategorie aufgeführt. Wenn Sie eine DMO Dialogfeld  Filter einfügen hinzufügen, erstellt GraphEdit den DMO Wrapper-Filter und konfiguriert ihn für die Verwendung DMO.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[DirectX-Medienobjekte](directx-media-objects.md)
</dt> </dl>

 

 
