---
title: Vorgehensweise beim Laden einer Bitmap aus einer Ressource (Direct2D)
description: Zeigt, wie eine Direct2D-Bitmap, die als Anwendungs Ressource gespeichert wird, geladen wird.
ms.assetid: 7285e6ea-ebc7-4693-8a77-99bff0b5d0d1
ms.topic: article
ms.date: 03/09/2019
ms.openlocfilehash: fe96ba4e0674392333173df7daeb5a354a379343
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106339921"
---
# <a name="how-to-load-a-bitmap-from-a-resource-direct2d"></a>Vorgehensweise beim Laden einer Bitmap aus einer Ressource (Direct2D)

Wie unter Gewusst [wie: Laden einer Bitmap aus einer Datei](how-to-load-a-direct2d-bitmap-from-a-file.md)beschrieben, verwendet Direct2D die Windows Imaging Component (WIC) zum Laden von Bitmaps. Zum Laden einer Bitmap aus einer Ressource verwenden Sie WIC-Objekte, um das Bild zu laden und in ein Direct2D-kompatibles Format zu konvertieren. Verwenden Sie dann die [**Methode "**](id2d1rendertarget-createbitmapfromwicbitmap.md) Methode erstellen" mit der Methode " [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)".

1.  Definieren Sie in der [Anwendungs Ressourcen-Definitionsdatei](/windows/desktop/menurc/about-resource-files)die Ressource. Im folgenden Beispiel wird eine Ressource mit dem Namen "sampleImage" definiert.

    ```C++
    // THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
    // ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
    // THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
    // PARTICULAR PURPOSE.
    //
    // Copyright (c) Microsoft Corporation. All rights reserved
    #include "windows.h"

    SampleImage Image "sampleImage.jpg"
    ```

Diese Ressource wird der Ressourcen Datei der Anwendung hinzugefügt, wenn die Anwendung erstellt wird.

2.  Laden Sie das Bild aus der Anwendungs Ressourcen Datei.

    ```C++
    HRESULT DemoApp::LoadResourceBitmap(
        ID2D1RenderTarget *pRenderTarget,
        IWICImagingFactory *pIWICFactory,
        PCWSTR resourceName,
        PCWSTR resourceType,
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

        HRSRC imageResHandle = NULL;
        HGLOBAL imageResDataHandle = NULL;
        void *pImageFile = NULL;
        DWORD imageFileSize = 0;

        // Locate the resource.
        imageResHandle = FindResourceW(HINST_THISCOMPONENT, resourceName, resourceType);
        HRESULT hr = imageResHandle ? S_OK : E_FAIL;
        if (SUCCEEDED(hr))
        {
            // Load the resource.
            imageResDataHandle = LoadResource(HINST_THISCOMPONENT, imageResHandle);

            hr = imageResDataHandle ? S_OK : E_FAIL;
        }
    ```

    

3.  Sperren Sie die Ressource, und berechnen Sie die Größe des Images.
    ```C++
        if (SUCCEEDED(hr))
        {
            // Lock it to get a system memory pointer.
            pImageFile = LockResource(imageResDataHandle);

            hr = pImageFile ? S_OK : E_FAIL;
        }
        if (SUCCEEDED(hr))
        {
            // Calculate the size.
            imageFileSize = SizeofResource(HINST_THISCOMPONENT, imageResHandle);

            hr = imageFileSize ? S_OK : E_FAIL;
            
        }
    ```

    

4.  Verwenden Sie die [**IWICImagingFactory:: foratestream**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createstream) -Methode, um ein [**IWICStream**](/windows/win32/api/wincodec/nn-wincodec-iwicstream) -Objekt zu erstellen.
    ```C++
        if (SUCCEEDED(hr))
        {
              // Create a WIC stream to map onto the memory.
            hr = pIWICFactory->CreateStream(&pStream);
        }
        if (SUCCEEDED(hr))
        {
            // Initialize the stream with the memory pointer and size.
            hr = pStream->InitializeFromMemory(
                reinterpret_cast<BYTE*>(pImageFile),
                imageFileSize
                );
        }
    ```

    

5.  Verwenden Sie die [**IWICImagingFactory:: | atedecoderfromstream**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) -Methode zum Erstellen eines [**iwicbitmapdecoders**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapdecoder).

    ```C++
        if (SUCCEEDED(hr))
        {
            // Create a decoder for the stream.
            hr = pIWICFactory->CreateDecoderFromStream(
                pStream,
                NULL,
                WICDecodeMetadataCacheOnLoad,
                &pDecoder
                );
        }
    ```

    

6.  Rufen Sie einen Frame aus dem Bild ab, und speichern Sie ihn in einem [**IWICBitmapFrameDecode**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframedecode) -Objekt.

    ```C++
        if (SUCCEEDED(hr))
        {
            // Create the initial frame.
            hr = pDecoder->GetFrame(0, &pSource);
        }
    ```

    

7.  Bevor Direct2D das Image verwenden kann, muss es in das Pixel Format 32bpppbgra konvertiert werden. Um das Bildformat zu konvertieren, verwenden Sie die [**IWICImagingFactory:: kreateformatconverter**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) -Methode, um ein [**IWICFormatConverter**](/windows/win32/api/wincodec/nn-wincodec-iwicformatconverter) -Objekt zu erstellen, und verwenden Sie dann die [**Initialize**](/windows/win32/api/wincodec/nf-wincodec-iwicformatconverter-initialize) -Methode des **IWICFormatConverter** -Objekts, um die Konvertierung auszuführen.
 
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

    

8.  Verwenden Sie abschließend die Methode " [**kreatebitmapfromwicbitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) ", um ein [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) -Objekt zu erstellen, das von einem Renderziel gezeichnet und mit anderen Direct2D-Objekten verwendet werden kann.
    ```C++
        if (SUCCEEDED(hr))
        {
            //create a Direct2D bitmap from the WIC bitmap.
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

    

In diesem Beispiel wurde Code weggelassen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Laden einer Bitmap aus einer Datei](how-to-load-a-direct2d-bitmap-from-a-file.md)
</dt> </dl>

 

 
