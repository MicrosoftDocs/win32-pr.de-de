---
description: DirectX-Oberflächenpuffer
ms.assetid: 2c82c023-4436-4f8a-b896-7f4765f989b3
title: DirectX-Oberflächenpuffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 746cff1489a644fd5c4144c8c0d923f11e5ca4555886e8defbce3b9b26a16a35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828270"
---
# <a name="directx-surface-buffer"></a>DirectX-Oberflächenpuffer

Das DirectX-Oberflächenpufferobjekt ist ein Medienpuffer, der eine Direct3D-Oberfläche verwaltet. Um eine Instanz dieses Objekts zu erstellen, rufen [**Sie MFCreateDXSurfaceBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer) auf, und übergeben Sie einen Zeiger auf die DirectX-Oberfläche. Der DirectX-Oberflächenpuffer macht die folgenden Schnittstellen verfügbar:

-   [**BUFFERMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer)
-   [**2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer)
-   [**VERZRGETService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)

Es gibt mehrere Möglichkeiten, über das Pufferobjekt auf den Oberflächenspeicher zuzugreifen:

-   Empfohlen: Rufen Sie IM Puffer DIE DATEI [**"CSVGetService::GetService"**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) auf. Verwenden Sie den Dienstbezeichner **MR \_ BUFFER \_ SERVICE**. Die -Methode gibt einen Zeiger auf die zugrunde liegende Direct3D-Oberfläche zurück.
-   Rufen Sie [**DIE DATEI 2DBuffer::Lock2D auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) Diese Methode ruft **IDirect3DSurface9::LockRect** direkt auf der Oberfläche auf. Die [**UNLOCK2DBuffer::Unlock2D-Methode**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-unlock2d) ruft **UnlockRect** auf der Oberfläche auf.
-   Rufen Sie [**DEN AUFRUF VONMEDIABUFFER::Lock auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) Im Allgemeinen wird dies nicht empfohlen, da das Objekt gezwungen wird, Speicher von der Direct3D-Oberfläche zu kopieren und dann wieder zurückzukehren. Die [**Lock2D-Methode**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) ist effizienter.

Sowohl [**Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) als auch [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) können fehlschlagen, wenn die zugrunde liegende Oberfläche nicht gesperrt werden kann. Der DirectX-Oberflächenpuffer implementiert diese beiden Methoden hauptsächlich für Komponenten, die nicht für die Arbeit mit Direct3D-Oberflächen konzipiert sind.

Der erweiterte Videorenderer (Enhanced Video Renderer, EVR) erstellt DirectX-Oberflächenpuffer, wenn der Decoder nicht für DirectX Video Acceleration (DXVA) konfiguriert ist. Weitere Informationen finden Sie unter [**DEM THEMAVIDEOSampleAllocator.**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator)

### <a name="obtaining-the-direct3d-surface"></a>Abrufen der Direct3D-Oberfläche

Gehen Sie wie folgt vor, um eine Direct3D-Oberfläche aus einem Videobeispiel abzurufen:

1.  Rufen Sie [**DEN NOTSAMPLE::GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) mit dem Indexwert 0 (null) auf.
2.  Rufen Sie [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) auf, und geben Sie den DIENSTbezeichner **MR BUFFER \_ \_ SERVICE** an.

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

[Medienpuffer](media-buffers.md)
</dt> <dt>

[Videobeispiele](video-samples.md)
</dt> </dl>

 

 



