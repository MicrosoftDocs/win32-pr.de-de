---
description: DirectX-Oberflächen Puffer
ms.assetid: 2c82c023-4436-4f8a-b896-7f4765f989b3
title: DirectX-Oberflächen Puffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02211d268e23bd7185cd480bee4e4dff297293b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127904"
---
# <a name="directx-surface-buffer"></a>DirectX-Oberflächen Puffer

Das DirectX-Oberflächen Puffer Objekt ist ein Medien Puffer, der eine Direct3D-Oberfläche verwaltet. Um eine Instanz dieses Objekts zu erstellen, rufen Sie [**mfkreatedxsurfacebuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer) auf und übergeben einen Zeiger auf die DirectX-Oberfläche. Der DirectX-Oberflächen Puffer macht die folgenden Schnittstellen verfügbar:

-   [**Imfmediabuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer)
-   [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer)
-   [**IMF-Dienst**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)

Es gibt mehrere Möglichkeiten, auf den Surface-Speicher aus dem Puffer Objekt zuzugreifen:

-   Empfohlen: [**imfgetservice:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) wird für den Puffer aufgerufen. Verwenden Sie den Dienst Bezeichner **Mr- \_ Puffer \_ Dienst**. Die-Methode gibt einen Zeiger auf die zugrunde liegende Direct3D-Oberfläche zurück.
-   [**IMF2DBuffer:: Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d)aufgerufen wird. Diese Methode ruft **IDirect3DSurface9:: lockrect** direkt auf der-Oberfläche auf. Die [**IMF2DBuffer:: Unlock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-unlock2d) -Methode ruft **unlockrect** auf der-Oberfläche auf.
-   Rückrufe [**imfmediabuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock). Dies wird im Allgemeinen nicht empfohlen, da das-Objekt zwingt, Arbeitsspeicher von der Direct3D-Oberfläche und dann wieder zurück zu kopieren. Die [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) -Methode ist effizienter.

Sowohl [**Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) als auch [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) können fehlschlagen, wenn die zugrunde liegende Oberfläche nicht Sperr fähig ist. Der DirectX-Oberflächen Puffer implementiert diese beiden Methoden primär für Komponenten, die nicht für die Verwendung mit Direct3D-Oberflächen entwickelt wurden.

Der Enhanced Video Renderer (EVR) erstellt DirectX-Oberflächen Puffer, wenn der Decoder nicht für die DirectX-Videobeschleunigung (DXVA) konfiguriert ist. Weitere Informationen finden Sie unter [**IMF videosamplezuordcator**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator).

### <a name="obtaining-the-direct3d-surface"></a>Abrufen der Direct3D-Oberfläche

Gehen Sie folgendermaßen vor, um eine Direct3D-Oberfläche aus einem Video Beispiel zu erhalten:

1.  Aufrufen von [**imfsample:: getbufferbyindex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) mit einem Indexwert von 0 (null).
2.  Aufrufen von [**mfgetservice**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) und angeben des Dienst Bezeichners für den **Mr- \_ Puffer \_ Dienst** .

Diese Schritte sind im folgenden Code dargestellt:


```C++
HRESULT GetD3DSurfaceFromSample(IMFSample *pSample, IDirect3DSurface9 **ppSurface)
{
    *ppSurface = NULL;

    IMFMediaBuffer *pBuffer = NULL;

    HRESULT hr = pSample->GetBufferByIndex(0, &pBuffer);
    if (SUCCEEDED(hr))
    {
        hr = MFGetService(pBuffer, MR_BUFFER_SERVICE, IID_PPV_ARGS(ppSurface));
        pBuffer->Release();
    }

    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medien Puffer](media-buffers.md)
</dt> <dt>

[Video Beispiele](video-samples.md)
</dt> </dl>

 

 



