---
description: Verwenden Sie dieses Beispiel, um zu verstehen, wie der RLE-Encoder die -Methode beim Schreiben eines Transformationsfilters implementieren kann.
ms.assetid: b7d878ab-523f-4b52-b98d-c9d4fa18ce8a
title: 'Schritt 5: Transformieren des Bilds'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecbb2290b35347ccbc9b9821d423f7b3b26c9878187d09387dec914001df1a67
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650810"
---
# <a name="step-5-transform-the-image"></a>Schritt 5: Transformieren des Bilds

Dies ist Schritt 5 des Tutorials Schreiben von [Transformationsfiltern.](writing-transform-filters.md)

Der Upstreamfilter übermittelt Medienbeispiele an den Transformationsfilter, indem er die [**IMemInputPin::Receive-Methode**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) auf dem Eingabepin des Transformationsfilters aufruft. Um die Daten zu verarbeiten, ruft der Transformationsfilter die **Transformationsmethode** auf, die rein virtuell ist. Die Klassen **CTransformFilter** und **CTransInPlaceFilter** verwenden zwei verschiedene Versionen dieser Methode:

-   [**CTransformFilter::Transform**](ctransformfilter-transform.md) verwendet einen Zeiger auf das Eingabebeispiel und einen Zeiger auf das Ausgabebeispiel. Bevor der Filter die -Methode aufruft, kopiert er die Beispieleigenschaften aus dem Eingabebeispiel in das Ausgabebeispiel, einschließlich der Zeitstempel.
-   [**CTransInPlaceFilter::Transform**](ctransinplacefilter-transform.md) verwendet einen Zeiger auf das Eingabebeispiel. Der Filter ändert die daten vor Ort.

Wenn die **Transform-Methode** S \_ OK zurückgibt, übermittelt der Filter das Beispiel downstream. Um einen Frame zu überspringen, geben Sie S \_ FALSE zurück. Wenn ein Streamingfehler auftritt, geben Sie einen Fehlercode zurück.

Das folgende Beispiel zeigt, wie der RLE-Encoder diese Methode implementieren kann. Ihre eigene Implementierung kann sich je nach Filter erheblich unterscheiden.


```C++
HRESULT CRleFilter::Transform(IMediaSample *pSource, IMediaSample *pDest)
{
    // Get pointers to the underlying buffers.
    BYTE *pBufferIn, *pBufferOut;
    hr = pSource->GetPointer(&pBufferIn);
    if (FAILED(hr))
    {
        return hr;
    }
    hr = pDest->GetPointer(&pBufferOut);
    if (FAILED(hr))
    {
        return hr;
    }
    // Process the data.
    DWORD cbDest = EncodeFrame(pBufferIn, pBufferOut);
    KASSERT((long)cbDest <= pDest->GetSize());

    pDest->SetActualDataLength(cbDest);
    pDest->SetSyncPoint(TRUE);
    return S_OK;
}
```



In diesem Beispiel wird davon ausgegangen, dass EncodeFrame eine private Methode ist, die die RLE-Codierung implementiert. Der Codierungsalgorithmus selbst wird hier nicht beschrieben. Weitere Informationen finden Sie im Thema "Bitmapkomprimierung" in der Plattform-SDK-Dokumentation.

Zunächst ruft das Beispiel [**IMediaSample::GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) auf, um die Adressen der zugrunde liegenden Puffer abzurufen. Diese werden an die private EncoderFrame-Methode übergeben. Anschließend ruft sie [**IMediaSample::SetActualDataLength**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) auf, um die Länge der codierten Daten anzugeben. Der Downstreamfilter benötigt diese Informationen, damit er den Puffer ordnungsgemäß verwalten kann. Schließlich ruft die -Methode [**IMediaSample::SetSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint) auf, um das Keyframeflag auf **TRUE** festzulegen. Bei der Codierung der Ausführungslänge werden keine Deltaframes verwendet, sodass jeder Frame ein Keyframe ist. Legen Sie für Deltaframes den Wert auf **FALSE** fest.

Weitere Probleme, die Sie berücksichtigen müssen, sind:

-   Zeitstempel. Die **CTransformFilter-Klasse** zeitstempelt das Ausgabebeispiel, bevor die **Transform-Methode** aufgerufen wird. Die Zeitstempelwerte werden aus dem Eingabebeispiel kopiert, ohne sie zu ändern. Wenn Ihr Filter die Zeitstempel ändern muss, rufen [**Sie IMediaSample::SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) im Ausgabebeispiel auf.
-   Formatänderungen. Der Upstreamfilter kann Formate während des Streams ändern, indem er einen Medientyp an das Beispiel anfügt. Zuvor wird [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) auf dem Eingabepin Ihres Filters angezeigt. In der **CTransformFilter-Klasse** führt dies zu einem Aufruf von **CheckInputType** gefolgt von **CheckTransform.** Der Downstreamfilter kann auch Medientypen mit demselben Mechanismus ändern. In Ihrem eigenen Filter gibt es zwei Dinge zu beobachten:

    -   Stellen Sie sicher, dass **QueryAccept** keine falschen Zustimmungen zurückgibt.
    -   Wenn Ihr Filter Formatänderungen akzeptiert, überprüfen Sie diese in der **Transform-Methode,** indem [**Sie IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype)aufrufen. Wenn diese Methode S \_ OK zurückgibt, muss Ihr Filter auf die Formatänderung reagieren.

    Weitere Informationen finden Sie unter [Dynamische Formatänderungen.](dynamic-format-changes.md)

-   Threads. Sowohl in **CTransformFilter** als **auch in CTransInPlaceFilter** liefert der Transformationsfilter Ausgabebeispiele synchron innerhalb der **Receive-Methode.** Der Filter erstellt keine Arbeitsthreads zum Verarbeiten der Daten. In der Regel gibt es keinen Grund für einen Transformationsfilter, Arbeitsthreads zu erstellen.

Weiter: [Schritt 6. Unterstützung für COM hinzugefügt.](step-6--add-support-for-com.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben von DirectShow-Filtern](writing-directshow-filters.md)
</dt> </dl>

 

 



