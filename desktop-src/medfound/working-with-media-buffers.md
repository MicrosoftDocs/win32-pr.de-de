---
description: Arbeiten mit Medienpuffern
ms.assetid: c7e079e0-99f3-4bff-9163-1c5a022c14ae
title: Arbeiten mit Medienpuffern (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c559e54d38c5a601a51bf3d6a879cbfe5b8403e1df48117e15d23f6264554437
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118736611"
---
# <a name="working-with-media-buffers-microsoft-media-foundation"></a>Arbeiten mit Medienpuffern (Microsoft Media Foundation)

In diesem Thema wird beschrieben, wie sie mithilfe der [**INTERFACESMediaBuffer-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) auf die Daten in einem Medienpuffer zugreifen. Alle Medienpuffer machen **DENMEDIABuffer** verfügbar, der für jeden Datentyp konzipiert ist. Unkomprimierte Videoframes sind ein Sonderfall, der im Thema [Unkomprimierte Videopuffer](uncompressed-video-buffers.md)beschrieben wird.

## <a name="buffer-size"></a>Puffergröße

Einem Medienpuffer sind zwei Größen zugeordnet:

-   Die *maximale Länge* ist die physische Größe des Arbeitsspeichers, der dem Puffer zugeordnet ist. Dieser Wert wird beim Erstellen des Puffers festgelegt und ändert sich während der Lebensdauer des Puffers nicht. Die maximale Länge gibt an, wie viele Daten im Puffer gespeichert werden können. Rufen Sie ZUM Ermitteln der maximalen Größe [**DEN AUFRUF VONMEDIABUFFER::GetMaxLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getmaxlength)auf.

-   Die *aktuelle Länge* ist die Menge gültiger Daten, die sich derzeit im Puffer befinden. Wenn der Puffer zum ersten Mal zugeordnet wird, ist die aktuelle Länge 0 (null), da im Puffer keine gültigen Daten vorhanden sind. Wenn Sie Daten in den Puffer schreiben, müssen Sie die aktuelle Länge aktualisieren, indem Sie [**DENMEDIABUFFER::SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength)aufrufen. Wenn Sie beispielsweise 100 Bytes Daten in den Puffer schreiben, rufen **Sie SetCurrentLength** mit dem Wert 100 auf. Wenn Sie Daten aus einem Medienpuffer lesen, rufen [**Sie ÜBERMEDIAMediaBuffer::GetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength) auf, um herauszufinden, wie viele Daten sich derzeit im Puffer befinden. Lesen Sie nicht über die aktuelle Länge. Die aktuelle Länge darf nie die maximale Länge des Puffers überschreiten.

## <a name="accessing-the-buffer-memory"></a>Zugreifen auf den Pufferspeicher

Rufen Sie ZUM Zugreifen auf den Arbeitsspeicher im Puffer [**DEN AUFRUF VONMEDIABUFFER::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock)auf. Diese Methode gibt einen Zeiger auf den Anfang des Speicherblocks zurück. Außerdem wird die maximale Länge und die aktuelle Länge zurückgegeben. Wenn Sie die Verwendung des Zeigers abgeschlossen haben, rufen Sie [**DENMEDIABUFFER::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock)auf.

So schreiben Sie Daten in einen Medienpuffer:

1.  Rufen Sie [**ÜBERMEDIAMEDIABUFFER::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) auf, um einen Zeiger auf den Arbeitsspeicher abzurufen. Die -Methode gibt auch die maximale Länge des Puffers zurück.
2.  Schreiben Sie Ihre Daten bis zur maximalen Länge des Puffers in den Arbeitsspeicher.
3.  Rufen Sie [**ÜBERMEDIABUFFER::SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength) auf, um die aktuelle Länge zu aktualisieren. Legen Sie die aktuelle Länge auf die Datenmenge fest, die Sie in Schritt 2 geschrieben haben.
4.  Rufen Sie [**DIE SPERREMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) auf, um den Puffer zu entsperren.

So lesen Sie Daten aus einem Medienpuffer:

1.  Rufen Sie [**ÜBERMEDIAMEDIABUFFER::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) auf, um einen Zeiger auf den Arbeitsspeicher abzurufen. Die -Methode gibt auch die aktuelle Länge des Puffers (die Menge der gültigen Daten im Puffer) zurück.
2.  Lesen Sie den Inhalt des Arbeitsspeichers bis zur aktuellen Länge.
3.  Rufen Sie [**DIE SPERREMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) auf, um den Puffer zu entsperren.

## <a name="creating-system-memory-buffers"></a>Erstellen von Systemspeicherpuffern

Der Systemspeicherpuffer ist ein Medienpuffer, der einen Block des Systemspeichers verwaltet. Um eine Instanz dieses Objekts zu erstellen, rufen Sie [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) oder [**MFCreateAlignedMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatealignedmemorybuffer) auf, und geben Sie eine Puffergröße an. Beide Funktionen weisen einen Speicherblock zu und geben einen [**POINTERMediaBuffer-Zeiger**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) zurück. Der Arbeitsspeicher wird automatisch freigegeben, wenn der Verweiszähler des Medienpuffers 0 (null) erreicht und das Objekt zerstört wird.

Das folgende Beispiel zeigt, wie Sie einen Systemspeicherpuffer erstellen und in den Puffer schreiben.


```C++
HRESULT CreateSystemMemoryBuffer(
    BYTE *pSrc, 
    DWORD cbData, 
    IMFMediaBuffer **ppBuffer
    )
{
    HRESULT hr = S_OK;
    BYTE *pData = NULL;

    IMFMediaBuffer *pBuffer = NULL;

    // Create the media buffer.
    hr = MFCreateMemoryBuffer(
        cbData,   // Amount of memory to allocate, in bytes.
        &pBuffer        
        );

    // Lock the buffer to get a pointer to the memory.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->Lock(&pData, NULL, NULL);
    }

    if (SUCCEEDED(hr))
    {
        memcpy_s(pData, cbData, pSrc, cbData);
    }

    // Update the current length.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbData);
    }

    // Unlock the buffer.
    if (pData)
    {
        hr = pBuffer->Unlock();
    }

    if (SUCCEEDED(hr))
    {
        *ppBuffer = pBuffer;
        (*ppBuffer)->AddRef();
    }

    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medienpuffer](media-buffers.md)
</dt> <dt>

[Media Foundation-Plattform-APIs](media-foundation-platform-apis.md)
</dt> </dl>

 

 



