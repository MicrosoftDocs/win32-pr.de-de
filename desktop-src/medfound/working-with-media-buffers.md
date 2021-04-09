---
description: Arbeiten mit Medien Puffern
ms.assetid: c7e079e0-99f3-4bff-9163-1c5a022c14ae
title: Arbeiten mit Medien Puffern (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db63843ded32be6b1baa9c62e21a33f6563a43d5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103869544"
---
# <a name="working-with-media-buffers-microsoft-media-foundation"></a>Arbeiten mit Medien Puffern (Microsoft Media Foundation)

In diesem Thema wird beschrieben, wie die [**imfmediabuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) -Schnittstelle für den Zugriff auf die Daten in einem Medien Puffer verwendet wird. Alle Medien Puffer machen **imfmediabuffer** verfügbar, das für beliebige Datentypen konzipiert ist. Nicht komprimierte Video Frames sind ein Sonderfall, der im Thema [unkomprimierte Video Puffer](uncompressed-video-buffers.md)beschrieben wird.

## <a name="buffer-size"></a>Puffergröße

Einem Medien Puffer sind zwei Größen zugeordnet:

-   Die *Maximale Länge* ist die physische Größe des Arbeitsspeichers, der dem Puffer zugeordnet ist. Dieser Wert wird festgelegt, wenn der Puffer erstellt wird, und wird während der Lebensdauer des Puffers nicht geändert. Die maximale Länge gibt an, wie viele Daten im Puffer gespeichert werden können. Um die maximale Größe zu ermitteln, nennen Sie [**imfmediabuffer:: getmaxlength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getmaxlength).

-   Die *aktuelle Länge* ist die Menge gültiger Daten, die sich derzeit im Puffer befinden. Beim ersten zuordnen des Puffers ist die aktuelle Länge 0 (null), da keine gültigen Daten im Puffer vorhanden sind. Wenn Sie Daten in den Puffer schreiben, müssen Sie die aktuelle Länge durch Aufrufen von [**imfmediabuffer:: setcurrentlength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength)aktualisieren. Wenn Sie z. b. 100 Bytes an Daten in den Puffer schreiben, nennen Sie **setcurrentlength** mit dem Wert 100. Wenn Sie Daten aus einem Medien Puffer lesen, können Sie [**imfmediabuffer:: getcurrentlength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength) aufrufen, um herauszufinden, wie viele Daten aktuell im Puffer sind. Liest die aktuelle Länge nicht. Die aktuelle Länge kann die maximale Länge des Puffers nie überschreiten.

## <a name="accessing-the-buffer-memory"></a>Zugreifen auf den Pufferspeicher

Um auf den Speicher im Puffer zuzugreifen, nennen Sie [**imfmediabuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock). Diese Methode gibt einen Zeiger auf den Anfang des Speicherblocks zurück. Außerdem werden die maximale Länge und die aktuelle Länge zurückgegeben. Wenn Sie die Verwendung des Zeigers abgeschlossen haben, nennen Sie [**imfmediabuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock).

So schreiben Sie Daten in einen Medien Puffer:

1.  Zum Abrufen eines Zeigers auf den Speicher muss [**imfmediabuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) aufgerufen werden. Die-Methode gibt auch die maximale Länge des Puffers zurück.
2.  Schreiben Sie die Daten in den Arbeitsspeicher, bis die maximale Länge des Puffers angezeigt wird.
3.  Aufrufen von [**imfmediabuffer:: setcurrentlength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength) zum Aktualisieren der aktuellen Länge. Legen Sie die aktuelle Länge auf die Menge der Daten fest, die Sie in Schritt 2 geschrieben haben.
4.  Zum Entsperren des Puffers muss [**imfmediabuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) aufgerufen werden.

So lesen Sie Daten aus einem Medien Puffer:

1.  Zum Abrufen eines Zeigers auf den Speicher muss [**imfmediabuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) aufgerufen werden. Die-Methode gibt auch die aktuelle Länge des Puffers (die Menge der gültigen Daten im Puffer) zurück.
2.  Lesen Sie den Inhalt des Arbeitsspeichers bis zur aktuellen Länge.
3.  Zum Entsperren des Puffers muss [**imfmediabuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) aufgerufen werden.

## <a name="creating-system-memory-buffers"></a>Erstellen von System Speicher Puffern

Der Systemspeicher Puffer ist ein Medien Puffer, der einen Block des System Speichers verwaltet. Um eine Instanz dieses Objekts zu erstellen, rufen Sie [**mfkreatememorybuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) oder [**mfkreatealignedmemorybuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatealignedmemorybuffer) auf, und geben Sie eine Puffergröße an. Beide Funktionen weisen einen Speicherblock zu und geben einen [**imfmediabuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) -Zeiger zurück. Der Arbeitsspeicher wird automatisch freigegeben, wenn der Verweis Zähler des Medien Puffers Null erreicht und das Objekt zerstört wird.

Im folgenden Beispiel wird gezeigt, wie ein Systemspeicher Puffer erstellt und in den Puffer geschrieben wird.


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

[Medien Puffer](media-buffers.md)
</dt> <dt>

[Media Foundation Plattform-APIs](media-foundation-platform-apis.md)
</dt> </dl>

 

 



