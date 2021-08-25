---
description: In diesem Thema wird beschrieben, wie ein Bitmapdecoder mithilfe eines Bilddateinamens erstellt wird.
ms.assetid: b384861d-4e71-4e07-8b44-5c1cbcb3a70f
title: Erstellen eines Decoders mithilfe eines Bilddateinamens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 867581e06692188913e4bb1af4956956c462c46bc189a4983f3c5d24bc38c986
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811990"
---
# <a name="how-to-create-a-decoder-using-an-image-filename"></a>Erstellen eines Decoders mithilfe eines Bilddateinamens

In diesem Thema wird beschrieben, wie ein Bitmapdecoder mithilfe eines Bilddateinamens erstellt wird.

So erstellen Sie einen Bitmapdecoder mithilfe eines Bilddateinamens

1.  Erstellen Sie [**ein IWICImagingFactory-Objekt,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) um Windows Imaging Component (WIC)-Objekte zu erstellen.

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  Verwenden Sie [**die CreateDecoderFromFilename-Methode,**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) um [**einen IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) aus einer Bilddatei zu erstellen.

    ```C++
    HRESULT hr = S_OK;

    IWICBitmapDecoder *pIDecoder = NULL;
    IWICBitmapFrameDecode *pIDecoderFrame  = NULL;

    hr = m_pIWICFactory->CreateDecoderFromFilename(
       L"turtle.jpg",                  // Image to be decoded
       NULL,                           // Do not prefer a particular vendor
       GENERIC_READ,                   // Desired read access to the file
       WICDecodeMetadataCacheOnDemand, // Cache metadata when needed
       &pIDecoder                      // Pointer to the decoder
       );
    ```

    

3.  Sie erhalten den [**ersten IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) des Bilds.

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    Das JPEG-Dateiformat unterstützt nur einen einzelnen Frame. Da die Datei in diesem Beispiel eine JPEG-Datei ist, wird der erste Frame ( `0` ) verwendet. Informationen zu Bildformaten mit mehreren Frames finden Sie unter Abrufen der [Frames](-wic-bitmapsources-howto-retrieveimageframes.md) eines Bilds für den Zugriff auf die einzelnen Frames des Bilds.

4.  Verarbeiten Sie den Bildrahmen. Weitere Informationen zu [**IWICBitmapSource-Objekten finden**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) Sie in der Übersicht über [Bitmapquellen.](-wic-bitmapsources.md)

## <a name="see-also"></a>Weitere Informationen

[Programmierhandbuch](-wic-programming-guide.md)


[Referenz](-wic-codec-reference.md)


[Beispiele](-wic-samples.md)


 

 



