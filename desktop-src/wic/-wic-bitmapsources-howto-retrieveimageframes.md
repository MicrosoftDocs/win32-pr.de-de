---
description: In diesem Thema wird veranschaulicht, wie Sie ein Bild mit mehreren Frames decodieren und jeden Frame zur Verarbeitung abrufen.
ms.assetid: e4f69608-7bf1-4d54-b586-b749526700c9
title: Abrufen der Frames aus einem Bild
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc9fb9802071115f62da78a10798e5e76aa83052270d40108e7c590acb8b2f46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119841440"
---
# <a name="how-to-retrieve-the-frames-from-an-image"></a>Abrufen der Frames aus einem Bild

In diesem Thema wird veranschaulicht, wie Sie ein Bild mit mehreren Frames decodieren und jeden Frame zur Verarbeitung abrufen.

So rufen Sie die Frames eines Bilds ab

1.  Erstellen Sie eine [**IWICImagingFactory,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) um Windows WIC-Objekte (Imaging Component) zu erstellen.

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  Verwenden Sie die [**CreateDecoderFromFilename-Methode,**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) um einen [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) aus einer Bilddatei zu erstellen.

    ```C++
    HRESULT hr = S_OK;

    IWICBitmapDecoder *pIDecoder = NULL;
    IWICBitmapFrameDecode *pIDecoderFrame  = NULL;
    UINT nFrameCount = 0;
    UINT uiWidth, uiHeight;

    // Create decoder for an image.
    hr = m_pIWICFactory->CreateDecoderFromFilename(
       L"creek.tiff",                  // Image to be decoded
       NULL,                           // Do not prefer a particular vendor
       GENERIC_READ,                   // Desired read access to the file
       WICDecodeMetadataCacheOnDemand, // Cache metadata when needed
       &pIDecoder                      // Pointer to the decoder
       );
    ```

    

3.  Ruft die Anzahl der Frames in den Bildern ab.

    ```C++
    // Retrieve the frame count of the image.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrameCount(&nFrameCount);
    }
    ```

    

4.  Verarbeiten Sie jeden Frame, indem Sie einen [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) für jeden Frame im Bild abrufen.

    ```C++
    // Process each frame in the image.
    for (UINT i=0; i < nFrameCount; i++)
    {
       // Retrieve the next bitmap frame.
       if (SUCCEEDED(hr))
       {
          hr = pIDecoder->GetFrame(i, &pIDecoderFrame);
       }

       // Retrieve the size of the bitmap frame.
       if (SUCCEEDED(hr))
       {
          hr = pIDecoderFrame->GetSize(&uiWidth, &uiHeight);
       }

       // Additional frame processing.
       // ...

       SafeRelease(&pIDecoderFrame);
    }
    ```

    

## <a name="see-also"></a>Weitere Informationen

[Programmierhandbuch](-wic-programming-guide.md)


[Referenz](-wic-codec-reference.md)


[Beispiele](-wic-samples.md)


 

 



