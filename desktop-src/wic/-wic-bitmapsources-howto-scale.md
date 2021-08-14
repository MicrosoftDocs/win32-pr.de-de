---
description: In diesem Thema wird veranschaulicht, wie eine IWICBitmapSource mithilfe der IWICBitmapScaler-Komponente skaliert wird.
ms.assetid: d2c65c9b-6f52-46f7-935d-0c582ca83867
title: Skalieren einer Bitmapquelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2771ed13c23fdb3d74cf9c24899bea7a355efefcb5e541ac21aff53f372ded0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118439690"
---
# <a name="how-to-scale-a-bitmap-source"></a>Skalieren einer Bitmapquelle

In diesem Thema wird veranschaulicht, wie eine [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) mithilfe der [**IWICBitmapScaler-Komponente skaliert**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) wird.

So skalieren Sie eine Bitmapquelle

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

    

2.  Verwenden Sie [**die CreateDecoderFromFilename-Methode,**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) um [**einen IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) aus einer Bilddatei zu erstellen.

    ```C++
    HRESULT hr = S_OK;

    IWICBitmapDecoder *pIDecoder = NULL;
    IWICBitmapFrameDecode *pIDecoderFrame  = NULL;
    IWICBitmapScaler *pIScaler = NULL;


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

4.  Erstellen Sie [**den IWICBitmapScaler,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) der für die Imageskalierung verwendet werden soll.

    ```C++
    // Create the scaler.
    if (SUCCEEDED(hr))
    {
       hr = m_pIWICFactory->CreateBitmapScaler(&pIScaler);
    }
    ```

    

5.  Initialisieren Sie das Scaler-Objekt mit den Bilddaten des Bitmapframes auf halber Größe.

    ```C++
    // Initialize the scaler to half the size of the original source.
    if (SUCCEEDED(hr))
    {
       hr = pIScaler->Initialize(
          pIDecoderFrame,                    // Bitmap source to scale.
          uiWidth/2,                         // Scale width to half of original.
          uiHeight/2,                        // Scale height to half of original.
          WICBitmapInterpolationModeFant);   // Use Fant mode interpolation.
    }
    ```

    

6.  Zeichnen oder verarbeiten Sie die skalierte Bitmapquelle.

    Die folgende Abbildung veranschaulicht die Bildverarbeitungsskalierung. Das ursprüngliche Bild auf der linken Seite ist 200 x 130 Pixel. Das Bild auf der rechten Seite ist das ursprüngliche Bild, das auf die Hälfte der Größe skaliert wird.

    ![Abbildung: Skalieren eines Bilds auf eine kleinere Größe](graphics/scaledregion.png)

## <a name="see-also"></a>Weitere Informationen

[Programmierhandbuch](-wic-programming-guide.md)


[Referenz](-wic-codec-reference.md)


[Beispiele](-wic-samples.md)


 

 



