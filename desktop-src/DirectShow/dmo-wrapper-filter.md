---
description: DMO-Wrapper Filter
ms.assetid: ffa6234d-9040-4838-8f51-0cf87df40a5c
title: DMO-Wrapper Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8b01ee006203e2e1fd328bacc13c01de4a3b25f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482435"
---
# <a name="dmo-wrapper-filter"></a>DMO-Wrapper Filter

Der DMO-Wrapper Filter ermöglicht einer DirectShow-Anwendung die Verwendung eines [DirectX-Medien Objekts](directx-media-objects.md) (DMO) innerhalb eines Filter Diagramms. Der Filter umschließt den DMO und behandelt alle Details der Verwendung des DMO, z. b. das Übergeben von Daten an und aus dem DMO. Außerdem aggregiert der Filter den DMO, sodass die Anwendung den Filter nach allen COM-Schnittstellen Abfragen kann, die der DMO verfügbar macht.



|                                          |                                                                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filter Schnittstellen                        | [**Ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**idmuwrapperfilter**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter), [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream)                                                                                                                       |
| Eingabe-PIN-Medientypen                    | Siehe Hinweise                                                                                                                                                                                                                                        |
| PIN-Eingabeschnittstellen                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| Ausgabe-PIN-Medientypen                   | Siehe Hinweise                                                                                                                                                                                                                                        |
| PIN-Schnittstellen                    | [**Iamstreamconfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition), [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID Filtern                             | CLSID \_ dmurapperfilter                                                                                                                                                                                                                            |
| CLSID der Eigenschaften Seite                      | Keine Eigenschaften Seite                                                                                                                                                                                                                                   |
| Ausführbare Datei                               | Qasf.dll                                                                                                                                                                                                                                           |
| [Verdienst](merit.md)                       | Siehe Hinweise                                                                                                                                                                                                                                        |
| [Filter Kategorie](filter-categories.md) | Siehe Hinweise                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a>Bemerkungen

### <a name="limitations"></a>Einschränkungen

Der DMO-Wrapper weist die folgenden Einschränkungen auf:

-   DMOS mit NULL Eingaben, mehreren Eingaben oder null Ausgaben werden nicht unterstützt. (Es werden DMOS mit einer Eingabe und mehreren Ausgaben unterstützt.)
-   Benutzerdefinierte Transporte werden nicht unterstützt. Der gesamte Datentransport erfolgt über die [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) -Schnittstelle.
-   Die **imediaobjectinplace** -Schnittstelle wird nicht verwendet. die gesamte Verarbeitung erfolgt mithilfe von [**imediaobject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) -Methoden.

### <a name="pins"></a>Pins

Für jeden Eingabedaten Strom im DMO erstellt der Filter eine entsprechende Eingabe-PIN. Für jeden Ausgabestream wird eine entsprechende Ausgabepin erstellt. Die von den einzelnen Pins unterstützten Medientypen hängen vom DMO ab.

### <a name="encoder-interfaces"></a>Encoder-Schnittstellen

Wenn es sich bei dem DMO um einen Video Encoder oder einen Audioencoder handelt, macht die Ausgabe-PIN die [**iamstreamconfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) -Schnittstelle verfügbar. Wenn es sich bei dem DMO um einen Video Encoder handelt, macht die Ausgabe-PIN auch die [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) -Schnittstelle verfügbar. In beiden Fällen, wenn der DMO die-Schnittstelle unterstützt, delegiert die PIN an den DMO. Andernfalls stellt die PIN eine eigene Implementierung bereit.

### <a name="streaming"></a>Streaming

Der Filter verwendet die [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) -Schnittstelle, um das gesamte Streaming zu verarbeiten. [**Iasynkreader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) -Verbindungen werden nicht unterstützt. Der Filter ruft [**imediaobject::P rocess Output**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processoutput) nur dann für das DMO auf, wenn Daten vom Upstream empfangen werden (einschließlich Benachrichtigungen zum Ende des Datenstroms). Daher wird DMOS mit NULL-Eingabedaten strömen nicht unterstützt.

### <a name="seeking"></a>Diejenigen

Alle Suchanforderungen werden über die erste Eingabe-PIN für den DMO-Wrapper an den upstreamfilter übergeben. Bei DMOS mit mehreren Ausgaben bedeutet dies, dass der upstreamfilter möglicherweise mehrere Suchanforderungen empfängt, wenn die Anwendung das Diagramm durchsucht.

### <a name="merit"></a>Verdienst

DirectShow weist allen DMOS einen Standardwert für den Wert "Value **\_ Normal** + 0x800" zu. Dieser Wert liegt zwischen dem Wert " **\_ Normal** " und dem **\_ bevorzugten Verdienst**. Decoderfilter weisen in der Regel den Wert Wert "Value **" auf. \_** Daher wählt der Filter Graph-Manager normalerweise einen DMO-Decoder über einen Decoderfilter aus. Fügen Sie zum Überschreiben des Standardwert Werts einen Registrierungs Eintrag zum Registrierungsschlüssel des DMO in HKEY \_ Classes \_ root \\ CLSID hinzu. Fügen Sie einen **DWORD** -Wert mit dem Namen "Value" ein, dessen Wert den Verdienst angibt.

### <a name="category"></a>Category

Der DMO-Wrapper Filter wird in keiner Kategorie allein angezeigt. Wenn ein DMO umschlossen wird, wird es in der DirectShow-Kategorie angezeigt, die der Kategorie des DMO unter dem Namen des DMO entspricht.

### <a name="buffers"></a>Puffer

Der DMO-Wrapper Filter übergibt Medien Puffer an den DMO, der die [**imediabuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) -Schnittstelle verfügbar macht.

In Windows Vista oder höher machen die Medien Puffer auch die IServiceProvider-Schnittstelle verfügbar. Der DMO kann diese Schnittstelle verwenden, um einen Zeiger auf das dem Puffer zugeordnete Medien Beispiel zu erhalten. Verwenden Sie die **IID \_ imediasample** des Dienst Bezeichners. Ein Video-DMO kann die [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) -Schnittstelle des Medien Beispiels verwenden, um damit-Flags für das Beispiel festzulegen. Der folgende Code zeigt, wie Sie den Zeiger auf das Medien Beispiel erhalten:


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



Weitere Informationen zu damit-Flags pro Stichprobe finden Sie unter [**am \_ SAMPLE2 Properties- \_ Struktur**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties).

### <a name="quality-control"></a>Qualitätslenkung

Wenn der DMO die [**idmoqualitycontrol**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-idmoqualitycontrol) -Schnittstelle verfügbar macht, übersetzt der Filter [**iqualitycontrol:: notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) -Aufrufe für die Ausgabepin in den [**idmoqualitycontrol:: setnow**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-idmoqualitycontrol-setnow) -Aufruf für den DMO. Der *rtnow* -Parameter von **setnow** wird als Summe aus dem **Zeitstempel** und den **späten** Membern der [**Qualitäts**](/windows/win32/api/strmif/ns-strmif-quality) Struktur berechnet.

### <a name="using-the-fiter-in-graphedit"></a>Verwenden des Arbeitsblatts in GraphEdit

In GraphEdit wird der DMO-Wrapper Filter nicht unter dem eigenen Namen angezeigt. Stattdessen wird jedes registrierte DMO unter der entsprechenden Filterkategorie aufgeführt. Wenn Sie im Dialogfeld " **Filter einfügen** " eine DMO-Datei hinzufügen, erstellt GraphEdit den DMO-Wrapper Filter und konfiguriert ihn für die Verwendung dieses DMO.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[DirectX-Medienobjekte](directx-media-objects.md)
</dt> </dl>

 

 
