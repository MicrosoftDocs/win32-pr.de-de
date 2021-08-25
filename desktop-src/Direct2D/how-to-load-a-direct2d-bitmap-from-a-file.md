---
title: Laden einer Bitmap aus einer Datei
description: Zeigt, wie sie eine Direct2D-Bitmap aus einer Bilddatei laden.
ms.assetid: 4abfbc2b-2730-4d96-897e-1e2232383a72
ms.topic: article
ms.date: 03/09/2019
ms.openlocfilehash: a330f0e32ee4abf62eb7df1c1d6a00b3f217e6f04502cebae6c489aa01eaaa9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824560"
---
# <a name="how-to-load-a-bitmap-from-a-file"></a>Laden einer Bitmap aus einer Datei

Direct2D verwendet die Windows Imaging Component (WIC) zum Laden von Bitmaps. Um eine Bitmap aus einer Datei zu laden, verwenden Sie zuerst WIC-Objekte, um das Bild zu laden und in ein Direct2D-kompatibles Format zu konvertieren, und verwenden Sie dann die [**CreateBitmapFromWicBitmap-Methode,**](id2d1rendertarget-createbitmapfromwicbitmap.md) um eine [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)zu erstellen.

1.  Erstellen Sie mithilfe der [**IWICImagingFactory::CreateDecoderFromFileName-Methode**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) einen [**IWICBitmapDecoder.**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapdecoder)

    ```C++
    HRESULT DemoApp::LoadBitmapFromFile(
        ID2D1RenderTarget *pRenderTarget,
        IWICImagingFactory *pIWICFactory,
        PCWSTR uri,
        UINT destinationWidth,
        UINT destinationHeight,
        ID2D1Bitmap **ppBitmap
        )
    {
        IWICBitmapDecoder *pDecoder = NULL;
        IWICBitmapFrameDecode *pSource = NULL;
        IWICStream *pStream = NULL;
        IWICFormatConverter *pConverter = NULL;
        IWICBitmapScaler *pScaler = NULL;

        HRESULT hr = pIWICFactory->CreateDecoderFromFilename(
            uri,
            NULL,
            GENERIC_READ,
            WICDecodeMetadataCacheOnLoad,
            &pDecoder
            );
            
    ```

    

2.  Rufen Sie einen Frame aus dem Bild ab, und speichern Sie den Frame in einem [**IWICBitmapFrameDecode-Objekt.**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframedecode)

    ```C++
        if (SUCCEEDED(hr))
        {
            // Create the initial frame.
            hr = pDecoder->GetFrame(0, &pSource);
        }
    ```

    

3.  Die Bitmap muss in ein Format konvertiert werden, das Direct2D verwenden kann. Konvertieren Sie daher das Pixelformat des Bilds in 32bppPBGRA. (Eine Liste der unterstützten Formate finden Sie unter [Pixelformate und Alphamodi](supported-pixel-formats-and-alpha-modes.md).). Rufen Sie [**die IWICImagingFactory::CreateFormatConverter-Methode**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) auf, um ein [**IWICFormatConverter-Objekt**](/windows/win32/api/wincodec/nn-wincodec-iwicformatconverter) zu erstellen, und rufen Sie dann die [**Initialize-Methode**](/windows/win32/api/wincodec/nf-wincodec-iwicformatconverter-initialize) des **IWICFormatConverter-Objekts** auf, um die Konvertierung durchzuführen.
    ```C++
        if (SUCCEEDED(hr))
        {

            // Convert the image format to 32bppPBGRA
            // (DXGI_FORMAT_B8G8R8A8_UNORM + D2D1_ALPHA_MODE_PREMULTIPLIED).
            hr = pIWICFactory->CreateFormatConverter(&pConverter);

        }
     
     
        if (SUCCEEDED(hr))
        {
            hr = pConverter->Initialize(
                pSource,
                GUID_WICPixelFormat32bppPBGRA,
                WICBitmapDitherTypeNone,
                NULL,
                0.f,
                WICBitmapPaletteTypeMedianCut
                );
    ```

    

4.  Rufen Sie [**die CreateBitmapFromWicBitmap-Methode**](id2d1rendertarget-createbitmapfromwicbitmap.md) auf, um ein [**ID2D1Bitmap-Objekt**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) zu erstellen, das von einem Renderziel gezeichnet und mit anderen Direct2D-Objekten verwendet werden kann.
    ```C++
        if (SUCCEEDED(hr))
        {
        
            // Create a Direct2D bitmap from the WIC bitmap.
            hr = pRenderTarget->CreateBitmapFromWicBitmap(
                pConverter,
                NULL,
                ppBitmap
                );
        }

        SafeRelease(&pDecoder);
        SafeRelease(&pSource);
        SafeRelease(&pStream);
        SafeRelease(&pConverter);
        SafeRelease(&pScaler);

        return hr;
    }
    ```

    

In diesem Beispiel wurde code weggelassen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)
</dt> <dt>

[**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md)
</dt> <dt>

[Laden einer Bitmap aus einer Ressource](how-to-load-a-bitmap-from-a-resource.md)
</dt> </dl>

 

 