---
description: Nicht komprimierte Video Puffer
ms.assetid: be5ec8a8-2d0b-401b-9d05-fdb87ad8c864
title: Nicht komprimierte Video Puffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24eda19136bf2dd7bc77f95d0efa6c48ca96e79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345863"
---
# <a name="uncompressed-video-buffers"></a>Nicht komprimierte Video Puffer

In diesem Artikel wird beschrieben, wie Sie mit Medien Puffern arbeiten, die nicht komprimierte Video Frames enthalten. In der bevorzugten Reihenfolge sind die folgenden Optionen verfügbar. Nicht jeder Medien Puffer unterstützt die einzelnen Optionen.

1.  Verwenden Sie die zugrunde liegende Direct3D-Oberfläche. (Gilt nur für Video Frames, die auf Direct3D-Oberflächen gespeichert sind.)
2.  Verwenden Sie die [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) -Schnittstelle.
3.  Verwenden Sie die [**imfmediabuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) -Schnittstelle.

## <a name="use-the-underlying-direct3d-surface"></a>Zugrunde liegende Direct3D-Oberfläche verwenden

Der Videoframe kann in einer Direct3D-Oberfläche gespeichert werden. Wenn dies der Fall ist, können Sie einen Zeiger auf die-Oberfläche abrufen, indem Sie [**imfgetservice:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) oder [**mfgetservice**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) für das Medien Puffer Objekt aufrufen. Verwenden Sie den Dienst Bezeichner Mr- \_ Puffer \_ Dienst. Diese Vorgehensweise wird empfohlen, wenn die Komponente, die auf den Videoframe zugreift, Direct3D verwendet. Beispielsweise sollte ein Video Decoder, der die DirectX-Videobeschleunigung unterstützt, diesen Ansatz verwenden.

Der folgende Code zeigt, wie Sie den **IDirect3DSurface9** -Zeiger aus einem Medien Puffer erhalten.


```C++
IDirect3DSurface9 *pSurface = NULL;

hr = MFGetService(
    pBuffer, 
    MR_BUFFER_SERVICE,
    __uuidof(IDirect3DSurface9), 
    (void**)&pSurface
    );

if (SUCCEEDED(hr))
{
    // Call IDirect3DSurface9 methods.
}
```



Die folgenden Objekte unterstützen den Dienst " **Mr- \_ Puffer \_ Dienst** ":

-   [DirectX-Oberflächen Puffer](directx-surface-buffer.md)
-   [Video Beispiele](video-samples.md)

## <a name="use-the-imf2dbuffer-interface"></a>Verwenden der IMF2DBuffer-Schnittstelle

Wenn der Videorahmen nicht in einer Direct3D-Oberfläche gespeichert ist oder die Komponente nicht für die Verwendung von Direct3D konzipiert ist, wird als nächstes empfohlen, auf den Videoframe zuzugreifen, um den Puffer für die [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) -Schnittstelle abzufragen. Diese Schnittstelle wurde speziell für Bilddaten entwickelt. Um einen Zeiger auf diese Schnittstelle abzurufen, nennen Sie **QueryInterface** für den Medien Puffer. Diese Schnittstelle wird nicht von allen Medien Puffer Objekten verfügbar gemacht. Wenn ein Medien Puffer jedoch die **IMF2DBuffer** -Schnittstelle verfügbar macht, sollten Sie diese Schnittstelle verwenden, um möglichst auf die Daten zuzugreifen, anstatt [**imfmediabuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer)zu verwenden. Sie können weiterhin die **imfmediabuffer** -Schnittstelle verwenden, Sie ist jedoch möglicherweise weniger effizient.

1.  Ruft **QueryInterface** für den Medien Puffer auf, um die [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) -Schnittstelle abzurufen.
2.  Aufrufen von [**IMF2DBuffer:: Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) , um auf den Arbeitsspeicher für den Puffer zuzugreifen. Diese Methode gibt einen Zeiger auf das erste Byte der obersten Zeile der Pixel zurück. Außerdem wird der Bild Sprung zurückgegeben, bei dem es sich um die Anzahl der Bytes vom Anfang einer Zeile bis zum Anfang der nächsten Zeile handelt. Der Puffer kann nach jeder Zeile von Pixeln Auffüll Bytes enthalten, sodass der Stride breiter als die Bildbreite in Bytes sein kann. Stride kann auch negativ sein, wenn das Bild im Arbeitsspeicher nach unten ausgerichtet wird. Weitere Informationen finden Sie unter [Image Stride](image-stride.md).
3.  Behalten Sie den Puffer nur dann bei, wenn Sie auf den Speicher zugreifen müssen. Entsperren Sie den Puffer durch Aufrufen von [**IMF2DBuffer:: Unlock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-unlock2d).

Nicht jeder Medien Puffer implementiert die [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) -Schnittstelle. Wenn der Medien Puffer diese Schnittstelle nicht implementiert (d. h., das Puffer Objekt gibt E \_ nointerface in Schritt 1 zurück), müssen Sie die [**imfmediabuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) -Schnittstellen Schnittstelle verwenden, die weiter unten beschrieben wird.

## <a name="use-the-imfmediabuffer-interface"></a>Verwenden der imfmediabuffer-Schnittstelle

Wenn ein Medien Puffer die [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) -Schnittstelle nicht verfügbar macht, verwenden Sie die [**imfmediabuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) -Schnittstelle. Die allgemeine Semantik dieser Schnittstelle wird im Thema [Arbeiten mit Medien Puffern](working-with-media-buffers.md)beschrieben.

1.  Ruft **QueryInterface** für den Medien Puffer auf, um die [**imfmediabuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) -Schnittstelle abzurufen.
2.  Aufrufen von [**imfmediabuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) , um auf den Pufferspeicher zuzugreifen. Diese Methode gibt einen Zeiger auf den Pufferspeicher zurück. Wenn die **Lock** -Methode verwendet wird, ist der Stride immer der minimale Schritt für das betreffende Videoformat und ohne zusätzliche Auffüll Zeichen.
3.  Behalten Sie den Puffer nur dann bei, wenn Sie auf den Speicher zugreifen müssen. Entsperren Sie den Puffer, indem Sie [**imfmediabuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock)aufrufen.

Sie sollten immer vermeiden, dass [**imfmediabuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) aufgerufen wird, wenn der Puffer [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer)verfügbar macht, da die **Lock** -Methode das Puffer Objekt für den Videoframe in einem zusammenhängenden Speicherblock erzwingen und dann wieder zurückgeben kann. Wenn der Puffer dagegen **IMF2DBuffer** nicht unterstützt, führt **imfmediabuffer:: Lock** wahrscheinlich nicht zu einer Kopie.

Berechnen Sie den minimalen Schritt vom Medientyp wie folgt:

-   Der minimale Schritt kann im [**MF \_ MT-Standard- \_ \_ Stride**](mf-mt-default-stride-attribute.md) -Attribut gespeichert werden.
-   Wenn das **MF \_ MT- \_ Standard- \_ Stride** -Attribut nicht festgelegt ist, müssen Sie die [**mfgetstrideforbitmapinfoheader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader) -Funktion aufrufen, um den Schritt für die meisten gängigen Videoformate zu berechnen.
-   Wenn die [**mfgetstrideforbitmapinfoheader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader) -Funktion das Format nicht erkennt, müssen Sie den Stride basierend auf der Definition des Formats berechnen. In diesem Fall gibt es keine allgemeine Regel. Sie müssen die Details der Format Definition kennen.

Der folgende Code zeigt, wie Sie den Standard Schritt für die gängigsten Videoformate erhalten.


```C++
HRESULT GetDefaultStride(IMFMediaType *pType, LONG *plStride)
{
    LONG lStride = 0;

    // Try to get the default stride from the media type.
    HRESULT hr = pType->GetUINT32(MF_MT_DEFAULT_STRIDE, (UINT32*)&lStride);
    if (FAILED(hr))
    {
        // Attribute not set. Try to calculate the default stride.

        GUID subtype = GUID_NULL;

        UINT32 width = 0;
        UINT32 height = 0;

        // Get the subtype and the image size.
        hr = pType->GetGUID(MF_MT_SUBTYPE, &subtype);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, &width, &height);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = MFGetStrideForBitmapInfoHeader(subtype.Data1, width, &lStride);
        if (FAILED(hr))
        {
            goto done;
        }

        // Set the attribute for later reference.
        (void)pType->SetUINT32(MF_MT_DEFAULT_STRIDE, UINT32(lStride));
    }

    if (SUCCEEDED(hr))
    {
        *plStride = lStride;
    }

done:
    return hr;
}
```



Abhängig von Ihrer Anwendung können Sie im Voraus wissen, ob ein bestimmter Medien Puffer [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) unterstützt (z. b. Wenn Sie den Puffer erstellt haben). Andernfalls müssen Sie darauf vorbereitet sein, eine der beiden Puffer Schnittstellen zu verwenden.

Das folgende Beispiel zeigt eine Hilfsklasse, die einige dieser Details verbirgt. Diese Klasse verfügt über eine LockBuffer-Methode, die entweder [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) oder [**Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) aufruft und einen Zeiger auf den Anfang der ersten Zeile der Pixel zurückgibt. (Dieses Verhalten stimmt mit der **Lock2D** -Methode überein.) Die LockBuffer-Methode nimmt den Standard Stride als Eingabeparameter an und gibt den eigentlichen Stride als Ausgabeparameter zurück.


```C++
class CBufferLock
{
public:
    CBufferLock(IMFMediaBuffer *pBuffer) : m_p2DBuffer(NULL), m_bLocked(FALSE)
    {
        m_pBuffer = pBuffer;
        m_pBuffer->AddRef();

        m_pBuffer->QueryInterface(IID_IMF2DBuffer, (void**)&m_p2DBuffer);
    }

    ~CBufferLock()
    {
        UnlockBuffer();
        SafeRelease(&m_pBuffer);
        SafeRelease(&m_p2DBuffer);
    }

    HRESULT LockBuffer(
        LONG  lDefaultStride,    // Minimum stride (with no padding).
        DWORD dwHeightInPixels,  // Height of the image, in pixels.
        BYTE  **ppbScanLine0,    // Receives a pointer to the start of scan line 0.
        LONG  *plStride          // Receives the actual stride.
        )
    {
        HRESULT hr = S_OK;

        // Use the 2-D version if available.
        if (m_p2DBuffer)
        {
            hr = m_p2DBuffer->Lock2D(ppbScanLine0, plStride);
        }
        else
        {
            // Use non-2D version.
            BYTE *pData = NULL;

            hr = m_pBuffer->Lock(&pData, NULL, NULL);
            if (SUCCEEDED(hr))
            {
                *plStride = lDefaultStride;
                if (lDefaultStride < 0)
                {
                    // Bottom-up orientation. Return a pointer to the start of the
                    // last row *in memory* which is the top row of the image.
                    *ppbScanLine0 = pData + abs(lDefaultStride) * (dwHeightInPixels - 1);
                }
                else
                {
                    // Top-down orientation. Return a pointer to the start of the
                    // buffer.
                    *ppbScanLine0 = pData;
                }
            }
        }

        m_bLocked = (SUCCEEDED(hr));

        return hr;
    }
    
    void UnlockBuffer()
    {
        if (m_bLocked)
        {
            if (m_p2DBuffer)
            {
                (void)m_p2DBuffer->Unlock2D();
            }
            else
            {
                (void)m_pBuffer->Unlock();
            }
            m_bLocked = FALSE;
        }
    }

private:
    IMFMediaBuffer  *m_pBuffer;
    IMF2DBuffer     *m_p2DBuffer;

    BOOL            m_bLocked;
};
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bild Schritt](image-stride.md)
</dt> <dt>

[Medien Puffer](media-buffers.md)
</dt> </dl>

 

 



