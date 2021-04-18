---
description: In diesem Thema wird veranschaulicht, wie die Pixel einer Bitmap-Quelle mithilfe der IWICBitmap-und der iwicbitmaplock-Komponente geändert werden.
ms.assetid: a08af015-bc42-4a31-af03-106714b08d08
title: Ändern der Pixel einer Bitmap-Quelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8be623d540fcd313476ea5c7ec5e724231d33aec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358974"
---
# <a name="how-to-modify-the-pixels-of-a-bitmap-source"></a>Ändern der Pixel einer Bitmap-Quelle

In diesem Thema wird veranschaulicht, wie die Pixel einer Bitmap-Quelle mithilfe der [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) -und der [**iwicbitmaplock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) -Komponente geändert werden.

So ändern Sie die Pixel einer Bitmap-Quelle

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

4.  Erstellen Sie eine [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) aus dem zuvor Abbild Frame.

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

    

5.  Rufen Sie eine [**iwicbitmaplock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) für ein angegebenes Rechteck der [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)ab.

    ```C++
    if (SUCCEEDED(hr))
    {
       // Obtain a bitmap lock for exclusive write.
       // The lock is for a 10x10 rectangle starting at the top left of the
       // bitmap.
       hr = pIBitmap->Lock(&rcLock, WICBitmapLockWrite, &pILock);
    ```

    

6.  Verarbeiten Sie die Pixeldaten, die jetzt vom [**iwicbitmaplock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) -Objekt gesperrt sind.

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

    

    Um die [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)zu entsperren, nennen Sie [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) für alle [**iwicbitmaplock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) -Objekte, die der **IWICBitmap** zugeordnet sind.

7.  Bereinigen Sie erstellte Objekte.

    ```C++
    SafeRelease(&pIBitmap);
    SafeRelease(&pIDecoder);
    SafeRelease(&pIDecoderFrame);
    ```

    

## <a name="see-also"></a>Weitere Informationen

[Programmierhandbuch](-wic-programming-guide.md)


[Verweis](-wic-codec-reference.md)


[Beispiele](-wic-samples.md)


 

 
