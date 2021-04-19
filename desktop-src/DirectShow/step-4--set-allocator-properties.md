---
description: Schritt 4.
ms.assetid: c2fd6d8b-b239-45e4-9c02-41edafa58762
title: Schritt 4. Festlegen von zuordnereigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a32d5e3affba32b96dc93cb97e1886322bc6f2c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350034"
---
# <a name="step-4-set-allocator-properties"></a>Schritt 4. Festlegen von zuordnereigenschaften

Dies ist Schritt 4 des Tutorials zum [Schreiben von Transformations Filtern](writing-transform-filters.md).

> [!Note]  
> Dieser Schritt ist für Filter, die von **ctransinplacefilter** abgeleitet werden, nicht erforderlich.

 

Nachdem zwei Pins einem Medientyp zugestimmt haben, wählen Sie eine Zuweisung für die Verbindungs-und Aushandlungs Eigenschaften aus, z. b. die Puffergröße und die Anzahl der Puffer.

In der **ctransformfilter** -Klasse gibt es zwei Zuweisungen, eine für die Upstream-Pin-Verbindung und eine für die downstreampin-Verbindung. Der upstreamfilter wählt die upstreamzuweisung aus und wählt außerdem die zuordnereigenschaften aus. Die Eingabe-PIN akzeptiert das, was der Upstream-Filter entscheidet. Wenn Sie dieses Verhalten ändern müssen, überschreiben Sie die [**cbasonputpin:: notifyzucator**](cbaseinputpin-notifyallocator.md) -Methode.

Mit dem Ausgabepin des Transformations Filters wird die Downstream-Zuweisung ausgewählt. Sie führt die folgenden Schritte aus:

1.  Wenn der Downstream-Filter eine Zuweisung bereitstellen kann, wird diese von der Ausgabepin verwendet. Andernfalls erstellt die Ausgabe-PIN eine neue Zuweisung.
2.  Durch den Aufruf von [**IMemInputPin:: getallocatorrequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements)erhält die Ausgabepin die zuordneranforderungen des nachgelagerten Filters (sofern vorhanden).
3.  Mit der Ausgabe-PIN wird die [**ctransformfilter::D ecidebuffersize**](ctransformfilter-decidebuffersize.md) -Methode des Transformations Filters aufgerufen, die rein virtuell ist. Die Parameter für diese Methode sind ein Zeiger auf die Zuweisung und eine [**\_ zuordnereigenschafts**](/windows/win32/api/strmif/ns-strmif-allocator_properties) Struktur mit den Anforderungen des downstreamfilters. Wenn der Downstream-Filter keine zuordneranforderungen aufweist, wird die-Struktur mit nulgerwert aufgefüllt.
4.  In der **decidebuffersize** -Methode legt die abgeleitete Klasse die zuordnereigenschaften fest, indem [**imemzuordcator:: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties)aufgerufen wird.

Im Allgemeinen wählt die abgeleitete Klasse zuordnereigenschaften basierend auf dem Ausgabeformat, den Anforderungen des downstreamfilters und den Anforderungen des Filters aus. Versuchen Sie, die Eigenschaften auszuwählen, die mit der Anforderung des downstreamfilters kompatibel sind. Andernfalls lehnt der Downstream-Filter die Verbindung möglicherweise ab.

Im folgenden Beispiel legt der RLE-Encoder die minimalen Werte für die Puffergröße, die Puffer Ausrichtung und die Puffer Anzahl fest. Für das Präfix wird ein beliebiger Wert verwendet, den der Downstream-Filter angefordert hat. Das Präfix ist in der Regel 0 (null) Bytes, einige Filter erfordern es jedoch. Der [AVI MUX](avi-mux-filter.md) -Filter verwendet beispielsweise das Präfix zum Schreiben von RIFF Headern.


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



Die Zuweisung ist möglicherweise nicht in der Lage, Ihre Anforderung genau abzugleichen. Daher gibt die **SetProperties** -Methode das tatsächliche Ergebnis in einer separaten **zuordnereigenschafts \_** -Struktur zurück (der *tatsächliche* Parameter im vorherigen Beispiel). Auch wenn **SetProperties** erfolgreich ist, sollten Sie das Ergebnis überprüfen, um sicherzustellen, dass Sie die Mindestanforderungen Ihres Filters erfüllen.

**Benutzerdefinierte Zuweisungen**

Standardmäßig verwenden alle Filterklassen die [**cmemzuordcator**](cmemallocator.md) -Klasse für ihre Zuweisungen. Diese Klasse ordnet Arbeitsspeicher aus dem virtuellen Adressraum des Client Prozesses zu (mit **virtualbelegc**). Wenn Ihr Filter eine andere Art von Arbeitsspeicher (z. b. DirectDraw-Oberflächen) verwenden muss, können Sie eine benutzerdefinierte Zuweisung implementieren. Sie können die Klasse [**cbasezucator**](cbaseallocator.md) verwenden oder eine vollständig neue zuordnerklasse schreiben. Wenn Ihr Filter über einen benutzerdefinierten Zuweiser verfügt, überschreiben Sie die folgenden Methoden, je nachdem, welche PIN die Zuweisung verwendet:

-   Eingabe-PIN: [**cbaseinputpin:: getallocator**](cbaseinputpin-getallocator.md) und [**cbaseinputpin:: notifyzuweisung**](cbaseinputpin-notifyallocator.md).
-   Ausgabe-PIN: [**cbaseoutputpin::D ecidezuordcator**](cbaseoutputpin-decideallocator.md).

Wenn der andere Filter die Verbindung mithilfe Ihrer benutzerdefinierten Zuweisung ablehnt, kann der Filter entweder die Verbindung nicht herstellen, oder es kann eine Verbindung mit der Zuweisung des anderen Filters hergestellt werden. Im letzteren Fall müssen Sie möglicherweise ein internes Flag festlegen, das den Typ der Zuweisung angibt. Ein Beispiel für diesen Ansatz finden Sie unter [**cdrawimage-Klasse**](cdrawimage.md).

Weiter: [Schritt 5. Transformieren Sie das Bild](step-5--transform-the-image.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben von DirectShow-Filtern](writing-directshow-filters.md)
</dt> </dl>

 

 



