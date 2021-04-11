---
description: In diesem Thema wird veranschaulicht, wie eine IWICBitmapSource mithilfe einer IWICBitmapFlipRotator-Komponente gedreht wird.
ms.assetid: 371c7759-0165-4a2a-b2ff-f9c8a31053a4
title: Vorgehensweise beim Kippen und Drehen einer Bitmap-Quelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87f6a805144025f185a4f4793fc4fafb27d7695a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128980"
---
# <a name="how-to-flip-and-rotate-a-bitmap-source"></a>Vorgehensweise beim Kippen und Drehen einer Bitmap-Quelle

In diesem Thema wird veranschaulicht, wie eine [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) mithilfe einer [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) -Komponente gedreht wird.

So kippen und drehen Sie eine Bitmap-Quelle

1.  Erstellen Sie ein [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) -Objekt, um WIC-Objekte (Windows Imaging Component) zu erstellen.

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  Verwenden Sie die Methode "Methode" von "| [**atedecoderfromfilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) ", um einen [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) aus einer Bilddatei zu erstellen.

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

    

3.  Holen Sie sich den ersten [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) des Bilds.

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    Das JPEG-Dateiformat unterstützt nur einen einzelnen Frame. Da es sich bei der Datei in diesem Beispiel um eine JPEG-Datei handelt, wird der erste Frame ( `0` ) verwendet. Informationen zu Bildformaten mit mehreren Frames finden [Sie unter Abrufen der Frames eines Bilds](-wic-bitmapsources-howto-retrieveimageframes.md) für den Zugriff auf die einzelnen Frames des Bilds.

4.  Erstellen Sie den [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) , der zum Kippen des Bilds verwendet werden soll.

    ```C++
    // Create the flip/rotator.
    if (SUCCEEDED(hr))
    {
       hr = m_pIWICFactory->CreateBitmapFlipRotator(&pIFlipRotator);
    }
    ```

    

5.  Initialisieren Sie das Flip/Rotator-Objekt mit den Bilddaten des horizontal gekippten bitmapframes (entlang der vertikalen y-Achse).

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

    

    Weitere Rotations-und flippingoptionen finden Sie unter [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) .

6.  Zeichnen Sie die geflippte Bitmapquelle, oder verarbeiten Sie Sie.

    > [!Note]  
    > Die [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) -Schnittstelle erbt von der [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) -Schnittstelle, sodass Sie das initialisierte Flip/Rotator-Objekt überall verwenden können, was eine **IWICBitmapSource** akzeptiert.

     

    In der folgenden Abbildung wird veranschaulicht, wie eine Bildverarbeitung horizontal (entlang der vertikalen x-Achse) gekippt wird.

    ![Abbildung: ein horizontales kippen (entlang der veritalen x-Achse) eines Bilds](graphics/fliphorizontal.png)

## <a name="see-also"></a>Weitere Informationen

[Programmierhandbuch](-wic-programming-guide.md)


[Verweis](-wic-codec-reference.md)


[Beispiele](-wic-samples.md)


 

 



