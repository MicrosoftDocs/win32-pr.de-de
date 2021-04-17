---
description: In diesem Thema wird veranschaulicht, wie ein rechteckiger Teil einer IWICBitmapSource mithilfe einer iwicbitmapclipperkomponente abgerufen wird.
ms.assetid: c9834827-8e1d-436d-be82-c1a2a2f7ca5c
title: Vorgehensweise beim Abschneiden einer Bitmap-Quelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43919e03d5d866d37ad4af203e741d2b10e60889
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104567618"
---
# <a name="how-to-clip-a-bitmap-source"></a>Vorgehensweise beim Abschneiden einer Bitmap-Quelle

In diesem Thema wird veranschaulicht, wie ein rechteckiger Teil einer [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) mithilfe einer [**iwicbitmapclipperkomponente**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) abgerufen wird.

So schneiden Sie eine Bitmap-Quelle ab

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

4.  Erstellen Sie den [**iwicbitmapclippertyp**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) , der für das Abbild Clipping verwendet werden soll.

    ```C++
    IWICBitmapClipper *pIClipper = NULL;

    if (SUCCEEDED(hr))
    {
       hr = m_pIWICFactory->CreateBitmapClipper(&pIClipper);
    }
    ```

    

5.  Initialisieren Sie das Clipper-Objekt mit den Bilddaten innerhalb des angegebenen Rechtecks des bitmapframes.

    ```C++
    // Create the clipping rectangle.
    WICRect rcClip = { 0, 0, uiWidth/2, uiHeight/2 };

    // Initialize the clipper with the given rectangle of the frame's image data.
    if (SUCCEEDED(hr))
    {
       hr = pIClipper->Initialize(pIDecoderFrame, &rcClip);
    }
    ```

    

6.  Zeichnen oder verarbeiten Sie das abgeschnittene Bild.

    In der folgenden Abbildung wird die Abbild Erstellung veranschaulicht. Das ursprüngliche Bild auf der linken Seite ist 200 x 130 Pixel. Das Bild auf der rechten Seite ist das ursprüngliche Bild, das auf ein als definiertes Rechteck zugeschnitten ist `{20,20,100,100}` .

    ![Abbildung der Abbild Erstellung](graphics/cliparegion_axisalignedclip.png)

## <a name="see-also"></a>Weitere Informationen

[Programmierhandbuch](-wic-programming-guide.md)


[Verweis](-wic-codec-reference.md)


[Beispiele](-wic-samples.md)


 

 



