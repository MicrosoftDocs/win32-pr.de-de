---
description: In diesem Thema wird der Prozess zum Zeichnen einer IWICBitmapSource mithilfe von Direct2D veranschaulicht.
ms.assetid: 11d38c9a-775d-41f7-a193-37b702b29a96
title: Zeichnen einer BitmapSource mithilfe von Direct2D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6dfdddb7cd6f7ab7341eb3c13a9fe40b797f09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106367954"
---
# <a name="how-to-draw-a-bitmapsource-using-direct2d"></a>Zeichnen einer BitmapSource mithilfe von Direct2D

In diesem Thema wird der Prozess zum Zeichnen einer [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) mithilfe von Direct2D veranschaulicht.

So zeichnen Sie eine Bitmap-Quelle mithilfe von Direct2D

1.  Decodieren eines Quell Bilds und Abrufen einer Bitmap-Quelle. In diesem Beispiel wird ein [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) verwendet, um das Bild zu decodieren, und der erste Bild Rahmen wird abgerufen.

    ```C++
       // Create a decoder
       IWICBitmapDecoder *pDecoder = NULL;

       hr = m_pIWICFactory->CreateDecoderFromFilename(
           szFileName,                      // Image to be decoded
           NULL,                            // Do not prefer a particular vendor
           GENERIC_READ,                    // Desired read access to the file
           WICDecodeMetadataCacheOnDemand,  // Cache metadata when needed
           &pDecoder                        // Pointer to the decoder
           );

       // Retrieve the first frame of the image from the decoder
       IWICBitmapFrameDecode *pFrame = NULL;

       if (SUCCEEDED(hr))
       {
           hr = pDecoder->GetFrame(0, &pFrame);
       }
    ```

    

    Weitere Typen von bitmapquellen, die gezeichnet werden sollen, finden Sie in der [Übersicht über Bitmap-Quellen](-wic-bitmapsources.md).

2.  Konvertieren Sie die Bitmapquelle in ein 32 bpppbgra-Pixel Format.

    Bevor Direct2D ein Bild verwenden kann, muss es in das 32bpppbgra-Pixel Format konvertiert werden. Um das Bildformat zu konvertieren, verwenden Sie die Methode " [**kreateformatconverter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) ", um ein [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) -Objekt zu erstellen. Verwenden Sie nach der Erstellung die [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicformatconverter-initialize) -Methode, um die Konvertierung auszuführen.

    ```C++
       // Format convert the frame to 32bppPBGRA
       if (SUCCEEDED(hr))
       {
           SafeRelease(&m_pConvertedSourceBitmap);
           hr = m_pIWICFactory->CreateFormatConverter(&m_pConvertedSourceBitmap);
       }

       if (SUCCEEDED(hr))
       {
           hr = m_pConvertedSourceBitmap->Initialize(
               pFrame,                          // Input bitmap to convert
               GUID_WICPixelFormat32bppPBGRA,   // Destination pixel format
               WICBitmapDitherTypeNone,         // Specified dither pattern
               NULL,                            // Specify a particular palette 
               0.f,                             // Alpha threshold
               WICBitmapPaletteTypeCustom       // Palette translation type
               );
       }
    ```

    

3.  Erstellen Sie ein [ID2D1RenderTarget](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) -Objekt für das Rendering in einem Fenster handle.

    ```C++
       // Create a D2D render target properties
       D2D1_RENDER_TARGET_PROPERTIES renderTargetProperties = D2D1::RenderTargetProperties();

       // Set the DPI to be the default system DPI to allow direct mapping
       // between image pixels and desktop pixels in different system DPI settings
       renderTargetProperties.dpiX = DEFAULT_DPI;
       renderTargetProperties.dpiY = DEFAULT_DPI;

       // Create a D2D render target
       D2D1_SIZE_U size = D2D1::SizeU(rc.right - rc.left, rc.bottom - rc.top);

       hr = m_pD2DFactory->CreateHwndRenderTarget(
           renderTargetProperties,
           D2D1::HwndRenderTargetProperties(hWnd, size),
           &m_pRT
           );
    ```

    

    Weitere Informationen zu renderzielen finden Sie in der Übersicht über die Direct2D- [Renderziele](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget).

4.  Erstellen Sie ein [ID2D1Bitmap](../direct2d/render-targets-overview.md) -Objekt mithilfe der [ID2D1RenderTarget::](../direct2d/id2d1rendertarget-createbitmapfromwicbitmap.md) -Methode.

    ```C++
        // D2DBitmap may have been released due to device loss. 
        // If so, re-create it from the source bitmap
        if (m_pConvertedSourceBitmap && !m_pD2DBitmap)
        {
            m_pRT->CreateBitmapFromWicBitmap(m_pConvertedSourceBitmap, NULL, &m_pD2DBitmap);
        }
    ```

    

5.  Zeichnen Sie die [ID2D1Bitmap](../direct2d/render-targets-overview.md) mit D2D [ID2D1RenderTarget::D rawbitmap](../direct2d/id2d1rendertarget-drawbitmap.md) -Methode.

    ```C++
        // Draws an image and scales it to the current window size
        if (m_pD2DBitmap)
        {
            m_pRT->DrawBitmap(m_pD2DBitmap, rectangle);
        }
    ```

    

Code wurde in diesem Beispiel ausgelassen. Den gesamten Code finden [Sie unter WIC Image Viewer using Direct2D Sample](-wic-sample-d2d-viewer.md).

## <a name="see-also"></a>Weitere Informationen

[Programmierhandbuch](-wic-programming-guide.md)


[Verweis](-wic-codec-reference.md)


[Beispiele](-wic-samples.md)


[Direct2D](../direct2d/direct2d-portal.md)


 

 
