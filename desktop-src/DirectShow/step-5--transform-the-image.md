---
description: 'Schritt 5:'
ms.assetid: b7d878ab-523f-4b52-b98d-c9d4fa18ce8a
title: 'Schritt 5: Transformieren des Bilds'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 609acb626d00dbceea8b6f5bca6af012d8158b57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217480"
---
# <a name="step-5-transform-the-image"></a>Schritt 5: Transformieren des Bilds

Dies ist Schritt 5 des Tutorials zum [Schreiben von Transformations Filtern](writing-transform-filters.md).

Der upstreamfilter liefert Medien Beispiele für den Transformations Filter, indem die [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) -Methode für die Eingabe-PIN des Transformations Filters aufgerufen wird. Um die Daten zu verarbeiten, ruft der Transformations Filter die **transformier** Methode auf, die rein virtuell ist. Die **ctransformfilter** -Klasse und die **ctransinplacefilter** -Klasse verwenden zwei unterschiedliche Versionen dieser Methode:

-   [**Ctransformfilter:: Transform**](ctransformfilter-transform.md) übernimmt einen Zeiger auf das Eingabe Beispiel und einen Zeiger auf das Ausgabe Beispiel. Bevor der Filter die-Methode aufruft, werden die Beispiel Eigenschaften aus dem Eingabe Beispiel in das Ausgabe Beispiel kopiert, einschließlich der Zeitstempel.
-   [**Ctransinplacefilter:: Transform**](ctransinplacefilter-transform.md) nimmt einen Zeiger auf das Eingabe Beispiel an. Der Filter ändert die Daten an Ort und Stelle.

Wenn die **Transform** -Methode "S OK" zurückgibt, übermittelt \_ der Filter das Beispiel nach unten. Um einen Frame zu überspringen, geben Sie "false" zurück \_ . Wenn ein Streamingfehler vorliegt, wird ein Fehlercode zurückgegeben.

Das folgende Beispiel zeigt, wie der RLE-Encoder diese Methode implementieren kann. Abhängig von der Art Ihres Filters kann sich Ihre eigene Implementierung erheblich unterscheiden.


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



In diesem Beispiel wird davon ausgegangen, dass encodeframe eine private Methode ist, die die RLE-Codierung implementiert. Der Codierungs Algorithmus selbst wird hier nicht beschrieben. Weitere Informationen finden Sie im Thema "Bitmapkomprimierung" in der Platform SDK-Dokumentation.

Zunächst wird im Beispiel [**imediasample:: getpointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) aufgerufen, um die Adressen der zugrunde liegenden Puffer abzurufen. Sie übergibt diese an die private encoderframe-Methode. Anschließend wird [**imediasample:: setactualdatalength**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) aufgerufen, um die Länge der codierten Daten anzugeben. Der Downstream-Filter benötigt diese Informationen, damit der Puffer ordnungsgemäß verwaltet werden kann. Schließlich ruft die-Methode [**imediasample:: setsyncpoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint) auf, um das schlüsselframe-Flag auf " **true**" festzulegen. Bei der Codierung der Lauf Zeit Länge werden keine Delta Frames verwendet, sodass jeder Frame ein Keyframe ist. Legen Sie für Delta Frames den Wert auf **false** fest.

Weitere Aspekte, die Sie berücksichtigen müssen, sind:

-   Zeitstempel. Die **ctransformfilter** -Klasse Zeitstempel das Ausgabe Beispiel vor dem Aufruf der **Transform** -Methode. Die Zeitstempel Werte werden aus dem Eingabe Beispiel kopiert, ohne Sie zu ändern. Wenn der Filter die Zeitstempel ändern muss, nennen Sie [**imediasample:: setTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) im Ausgabe Beispiel.
-   Formatieren von Änderungen. Der upstreamfilter kann die Formate in der Mitte des Datenstroms ändern, indem er dem Beispiel einen Medientyp anfügt. Vor diesem Vorgang wird [**IPin:: queryaccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) in der Eingabe-PIN Ihres Filters aufgerufen. In der **ctransformfilter** -Klasse führt dies zu einem Rückruf von **checkinputtype** , gefolgt von **checktransform**. Der downstreamfilter kann auch die Medientypen mithilfe desselben Mechanismus ändern. In Ihrem eigenen Filter müssen Sie zwei Dinge beachten:

    -   Stellen Sie sicher, dass **queryaccept** keine falschen Annahmen zurückgibt.
    -   Wenn der Filter Formatänderungen annimmt, überprüfen Sie diese in der **Transformations** Methode, indem Sie [**imediasample:: getmediatype**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype)aufrufen. Wenn diese Methode S OK zurückgibt \_ , muss der Filter auf die Formatänderung reagieren.

    Weitere Informationen finden Sie unter [dynamische Format Änderungen](dynamic-format-changes.md).

-   Threads. In **ctransformfilter** und **ctransinplacefilter** liefert der Transformations Filter Ausgabe Beispiele synchron innerhalb der **Receive** -Methode. Der Filter erstellt keine Arbeitsthreads, um die Daten zu verarbeiten. In der Regel gibt es keinen Grund für einen Transformations Filter zum Erstellen von Arbeitsthreads.

Weiter: [Schritt 6. Unterstützung für com hinzufügen](step-6--add-support-for-com.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben von DirectShow-Filtern](writing-directshow-filters.md)
</dt> </dl>

 

 



