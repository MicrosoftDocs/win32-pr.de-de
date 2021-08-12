---
description: Legen Sie Zuweisungseigenschaften als Teil des Schreibens eines Transformationsfilters fest. Der Ausgabepin des Transformationsfilters wählt die Downstreamzuweisung aus.
ms.assetid: c2fd6d8b-b239-45e4-9c02-41edafa58762
title: Schritt 4. Festlegen von Zuweisungseigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33376cff0e6c0674edfadcffed59d16d8d7dccb9f48384a22ec4c69fc48d8eb7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118652130"
---
# <a name="step-4-set-allocator-properties"></a>Schritt 4. Festlegen von Zuweisungseigenschaften

Dies ist Schritt 4 des Tutorials [Schreiben von Transformationsfiltern](writing-transform-filters.md).

> [!Note]  
> Dieser Schritt ist für Filter, die von **CTransInPlaceFilter** ableiten, nicht erforderlich.

 

Nachdem sich zwei Pins auf einen Medientyp einigen, wählen sie eine Zuweisung für die Verbindungs- und Aushandlungszuweisungseigenschaften aus, z. B. die Puffergröße und die Anzahl der Puffer.

In der **CTransformFilter-Klasse** gibt es zwei Zuweisungen: einen für die Upstream-PIN-Verbindung und einen für die Downstream-Pinverbindung. Der Upstreamfilter wählt die Upstreamzuweisung und auch die Zuweisungseigenschaften aus. Der Eingabepin akzeptiert alles, was der Upstreamfilter entscheidet. Wenn Sie dieses Verhalten ändern müssen, überschreiben Sie die [**CBaseInputPin::NotifyAllocator-Methode.**](cbaseinputpin-notifyallocator.md)

Der Ausgabepin des Transformationsfilters wählt die Downstreamzuweisung aus. Sie führt die folgenden Schritte aus:

1.  Wenn der Downstreamfilter eine Zuweisung bereitstellen kann, verwendet der Ausgabepin diesen. Andernfalls erstellt der Ausgabepin eine neue Zuweisung.
2.  Der Ausgabepin ruft die Zuweisungsanforderungen des Downstreamfilters ab (sofern dies der Fall ist), indem [**er IMemInputPin::GetAllocatorRequirements aufruft.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements)
3.  Der Ausgabepin ruft die [**CTransformFilter::D ecideBufferSize-Methode**](ctransformfilter-decidebuffersize.md) des Transformationsfilters auf, die rein virtuell ist. Die Parameter für diese Methode sind ein Zeiger auf die Zuweisung und eine [**ALLOCATOR \_ PROPERTIES-Struktur**](/windows/win32/api/strmif/ns-strmif-allocator_properties) mit den Anforderungen des Downstreamfilters. Wenn der Downstreamfilter keine Zuweisungsanforderungen hat, wird die Struktur auf Null gesetzt.
4.  In der **DecideBufferSize-Methode** legt die abgeleitete Klasse die Zuweisungseigenschaften fest, indem [**sie IMemAllocator::SetProperties aufruft.**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties)

Im Allgemeinen wählt die abgeleitete Klasse Zuweisungseigenschaften basierend auf dem Ausgabeformat, den Anforderungen des Downstreamfilters und den eigenen Anforderungen des Filters aus. Versuchen Sie, Eigenschaften auszuwählen, die mit der Anforderung des Downstreamfilters kompatibel sind. Andernfalls kann der Downstreamfilter die Verbindung ablehnen.

Im folgenden Beispiel legt der RLE-Encoder Mindestwerte für Die Puffergröße, Pufferausrichtung und Pufferanzahl fest. Für das Präfix wird der vom Downstreamfilter angeforderte Wert verwendet. Das Präfix ist in der Regel 0 (null) Bytes, aber einige Filter erfordern es. Der AVI [Mux-Filter](avi-mux-filter.md) verwendet z. B. das Präfix zum Schreiben von SUFFIX-Headern.


```C++
HRESULT CRleFilter::DecideBufferSize(
    IMemAllocator *pAlloc, ALLOCATOR_PROPERTIES *pProp)
{
    AM_MEDIA_TYPE mt;
    HRESULT hr = m_pOutput->ConnectionMediaType(&mt);
    if (FAILED(hr))
    {
        return hr;
    }

    ASSERT(mt.formattype == FORMAT_VideoInfo);
    BITMAPINFOHEADER *pbmi = HEADER(mt.pbFormat);
    pProp->cbBuffer = DIBSIZE(*pbmi) * 2; 
    if (pProp->cbAlign == 0)
    {
        pProp->cbAlign = 1;
    }
    if (pProp->cBuffers == 0)
    {
        pProp->cBuffers = 1;
    }
    // Release the format block.
    FreeMediaType(mt);

    // Set allocator properties.
    ALLOCATOR_PROPERTIES Actual;
    hr = pAlloc->SetProperties(pProp, &Actual);
    if (FAILED(hr)) 
    {
        return hr;
    }
    // Even when it succeeds, check the actual result.
    if (pProp->cbBuffer > Actual.cbBuffer) 
    {
        return E_FAIL;
    }
    return S_OK;
}
```



Die Zuweisung kann Möglicherweise nicht genau mit Ihrer Anforderung übereinstimmen. Daher gibt die **SetProperties-Methode** das tatsächliche Ergebnis in einer separaten **ALLOCATOR \_ PROPERTIES-Struktur** zurück (im vorherigen Beispiel der *Actual-Parameter).* Auch wenn **SetProperties erfolgreich** ist, sollten Sie das Ergebnis überprüfen, um sicherzustellen, dass es die Mindestanforderungen Ihres Filters erfüllt.

**Benutzerdefinierte Zuweisungen**

Standardmäßig verwenden alle Filterklassen die [**CMemAllocator-Klasse**](cmemallocator.md) für ihre Zuweisungen. Diese Klasse weist Arbeitsspeicher aus dem virtuellen Adressraum des Clientprozesses zu **(mithilfe von VirtualAlloc**). Wenn Ihr Filter eine andere Art von Arbeitsspeicher verwenden muss, z. B. DirectDraw-Oberflächen, können Sie eine benutzerdefinierte Zuweisung implementieren. Sie können die [**CBaseAllocator-Klasse**](cbaseallocator.md) verwenden oder eine völlig neue Zuweisungsklasse schreiben. Wenn Ihr Filter über eine benutzerdefinierte Zuweisung verfügt, überschreiben Sie die folgenden Methoden, je nachdem, welcher Pin die Zuweisung verwendet:

-   Eingabepin: [**CBaseInputPin::GetAllocator**](cbaseinputpin-getallocator.md) und [**CBaseInputPin::NotifyAllocator**](cbaseinputpin-notifyallocator.md).
-   Ausgabepin: [**CBaseOutputPin::D ecideAllocator**](cbaseoutputpin-decideallocator.md).

Wenn der andere Filter die Verbindung mithilfe Ihrer benutzerdefinierten Zuweisung verweigert, kann ihr Filter entweder die Verbindung fehlschlagen oder eine Verbindung mit der Zuweisung des anderen Filters herstellen. Im letzteren Fall müssen Sie möglicherweise ein internes Flag festlegen, das den Typ der Zuweisung angibt. Ein Beispiel für diesen Ansatz finden Sie unter [**CDrawImage-Klasse**](cdrawimage.md).

Weiter: [Schritt 5. Transformieren Sie das Image](step-5--transform-the-image.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben von DirectShow-Filtern](writing-directshow-filters.md)
</dt> </dl>

 

 



