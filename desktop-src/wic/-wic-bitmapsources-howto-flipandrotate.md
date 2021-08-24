---
description: In diesem Thema wird veranschaulicht, wie eine IWICBitmapSource mithilfe einer IWICBitmapFlipRotator-Komponente gedreht wird.
ms.assetid: 371c7759-0165-4a2a-b2ff-f9c8a31053a4
title: Umkehren und Drehen einer Bitmapquelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a61a1546f5a0191d2e20cc3079af3e4d772e6d2c3c07a5dd1e1e4aa331dc3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119331545"
---
# <a name="how-to-flip-and-rotate-a-bitmap-source"></a>Umkehren und Drehen einer Bitmapquelle

In diesem Thema wird veranschaulicht, wie eine [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) mithilfe einer [**IWICBitmapFlipRotator-Komponente**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) gedreht wird.

So drehen Sie eine Bitmapquelle

1.  Erstellen Sie ein [**IWICImagingFactory-Objekt,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) um Windows WIC-Objekte (Imaging Component) zu erstellen.

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
    IWICBitmapFlipRotator *pIFlipRotator = NULL;

    hr = m_pIWICFactory->CreateDecoderFromFilename(
       L"turtle.jpg",                  // Image to be decoded
       NULL,                           // Do not prefer a particular vendor
       GENERIC_READ,                   // Desired read access to the file
       WICDecodeMetadataCacheOnDemand, // Cache metadata when needed
       &pIDecoder                      // Pointer to the decoder
       );
    ```

    

3.  Abrufen des ersten [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) des Bilds.

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    Das JPEG-Dateiformat unterstützt nur einen einzelnen Frame. Da die Datei in diesem Beispiel eine JPEG-Datei ist, wird der erste Frame ( `0` ) verwendet. Informationen zu Bildformaten mit mehreren Frames finden Sie unter [Abrufen der Frames eines Bilds](-wic-bitmapsources-howto-retrieveimageframes.md) für den Zugriff auf die einzelnen Frames des Bilds.

4.  Erstellen Sie den [**IWICBitmapFlipRotator, der**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) zum Spiegeln des Bilds verwendet werden soll.

    ```C++
    // Create the flip/rotator.
    if (SUCCEEDED(hr))
    {
       hr = m_pIWICFactory->CreateBitmapFlipRotator(&pIFlipRotator);
    }
    ```

    

5.  Initialisieren Sie das Flip/Rotator-Objekt mit horizontal gekippten Bilddaten des Bitmaprahmens (entlang der vertikalen y-Achse).

    ```C++
    // Initialize the flip/rotator to flip the original source horizontally.
    if (SUCCEEDED(hr))
    {
       hr = pIFlipRotator->Initialize(
          pIDecoderFrame,                     // Bitmap source to flip.
          WICBitmapTransformFlipHorizontal);  // Flip the pixels along the 
                                              //  vertical y-axis.
    }
    ```

    

    Weitere Drehungen und Flippingoptionen finden Sie unter [**WICBitmapTransformOptions.**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)

6.  Zeichnen oder verarbeiten Sie die gekippte Bitmapquelle.

    > [!Note]  
    > Die [**IWICBitmapFlipRotator-Schnittstelle**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) erbt von der [**IWICBitmapSource-Schnittstelle,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) sodass Sie das initialisierte Flip/Rotator-Objekt überall dort verwenden können, wo eine **IWICBitmapSource** akzeptiert wird.

     

    In der folgenden Abbildung wird das horizontale Drehen eines Bildbilds (entlang der vertikalen X-Achse) veranschaulicht.

    ![Abbildung, die einen horizontalen Flip (entlang der x-Achse) eines Bilds zeigt](graphics/fliphorizontal.png)

## <a name="see-also"></a>Weitere Informationen

[Programmierhandbuch](-wic-programming-guide.md)


[Referenz](-wic-codec-reference.md)


[Beispiele](-wic-samples.md)


 

 



