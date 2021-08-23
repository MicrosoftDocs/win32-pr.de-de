---
description: In diesem Thema wird veranschaulicht, wie die Pixel einer Bitmapquelle mithilfe der Komponenten IWICBitmap und IWICBitmapLock geändert werden.
ms.assetid: a08af015-bc42-4a31-af03-106714b08d08
title: Ändern der Pixel einer Bitmapquelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbfa25a5f09742066c4e67af1fb1735aa038f086d6a107e88ae34e7b7c597770
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965389"
---
# <a name="how-to-modify-the-pixels-of-a-bitmap-source"></a>Ändern der Pixel einer Bitmapquelle

In diesem Thema wird veranschaulicht, wie die Pixel einer Bitmapquelle mithilfe der Komponenten [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) und [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) geändert werden.

So ändern Sie die Pixel einer Bitmapquelle

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

4.  Erstellen Sie eine [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) aus dem zuvor abgerufenen Bildrahmen.

    ```C++
    IWICBitmap *pIBitmap = NULL;
    IWICBitmapLock *pILock = NULL;

    UINT uiWidth = 10;
    UINT uiHeight = 10;

    WICRect rcLock = { 0, 0, uiWidth, uiHeight };

    // Create the bitmap from the image frame.
    if (SUCCEEDED(hr))
    {
       hr = m_pIWICFactory->CreateBitmapFromSource(
          pIDecoderFrame,          // Create a bitmap from the image frame
          WICBitmapCacheOnDemand,  // Cache metadata when needed
          &pIBitmap);              // Pointer to the bitmap
    }
    ```

    

5.  Rufen Sie ein [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) für ein angegebenes Rechteck der [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)ab.

    ```C++
    if (SUCCEEDED(hr))
    {
       // Obtain a bitmap lock for exclusive write.
       // The lock is for a 10x10 rectangle starting at the top left of the
       // bitmap.
       hr = pIBitmap->Lock(&rcLock, WICBitmapLockWrite, &pILock);
    ```

    

6.  Verarbeiten Sie die Pixeldaten, die jetzt durch das [**IWICBitmapLock-Objekt**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) gesperrt sind.

    ```C++
       if (SUCCEEDED(hr))
       {
          UINT cbBufferSize = 0;
          BYTE *pv = NULL;

          // Retrieve a pointer to the pixel data.
          if (SUCCEEDED(hr))
          {
             hr = pILock->GetDataPointer(&cbBufferSize, &pv);
          }
          
          // Pixel manipulation using the image data pointer pv.
          // ...

          // Release the bitmap lock.
          SafeRelease(&pILock);
       }
    }
    ```

    

    Um die [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)zu entsperren, rufen [Sie IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) für alle [**IWICBitmapLock-Objekte**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) auf, die **IWICBitmap** zugeordnet sind.

7.  Bereinigen sie erstellte Objekte.

    ```C++
    SafeRelease(&pIBitmap);
    SafeRelease(&pIDecoder);
    SafeRelease(&pIDecoderFrame);
    ```

    

## <a name="see-also"></a>Weitere Informationen

[Programmierhandbuch](-wic-programming-guide.md)


[Referenz](-wic-codec-reference.md)


[Beispiele](-wic-samples.md)


 

 
