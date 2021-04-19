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
# <a name="how-to-load-a-bitmap-from-a-resource-direct2d"></a><span data-ttu-id="fb320-103">Vorgehensweise beim Laden einer Bitmap aus einer Ressource (Direct2D)</span><span class="sxs-lookup"><span data-stu-id="fb320-103">How to Load a Bitmap from a Resource (Direct2D)</span></span>

<span data-ttu-id="fb320-104">Wie unter Gewusst [wie: Laden einer Bitmap aus einer Datei](how-to-load-a-direct2d-bitmap-from-a-file.md)beschrieben, verwendet Direct2D die Windows Imaging Component (WIC) zum Laden von Bitmaps.</span><span class="sxs-lookup"><span data-stu-id="fb320-104">As described in [How to Load a Bitmap from a File](how-to-load-a-direct2d-bitmap-from-a-file.md), Direct2D uses the Windows Imaging Component (WIC) to load bitmaps.</span></span> <span data-ttu-id="fb320-105">Zum Laden einer Bitmap aus einer Ressource verwenden Sie WIC-Objekte, um das Bild zu laden und in ein Direct2D-kompatibles Format zu konvertieren. Verwenden Sie dann die [**Methode "**](id2d1rendertarget-createbitmapfromwicbitmap.md) Methode erstellen" mit der Methode " [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)".</span><span class="sxs-lookup"><span data-stu-id="fb320-105">To load a bitmap from a resource, use WIC objects to load the image and to convert it to a Direct2D-compatible format; then, use the [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) method to create an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span></span>

1.  <span data-ttu-id="fb320-106">Definieren Sie in der [Anwendungs Ressourcen-Definitionsdatei](/windows/desktop/menurc/about-resource-files)die Ressource.</span><span class="sxs-lookup"><span data-stu-id="fb320-106">In the [application resource definition file](/windows/desktop/menurc/about-resource-files), define the resource.</span></span> <span data-ttu-id="fb320-107">Im folgenden Beispiel wird eine Ressource mit dem Namen "sampleImage" definiert.</span><span class="sxs-lookup"><span data-stu-id="fb320-107">The following example defines a resource named "SampleImage".</span></span>

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

<span data-ttu-id="fb320-108">Diese Ressource wird der Ressourcen Datei der Anwendung hinzugefügt, wenn die Anwendung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="fb320-108">This resource will be added to the application's resource file when the application is built.</span></span>

2.  <span data-ttu-id="fb320-109">Laden Sie das Bild aus der Anwendungs Ressourcen Datei.</span><span class="sxs-lookup"><span data-stu-id="fb320-109">Load the image from the application resource file.</span></span>

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

    

3.  <span data-ttu-id="fb320-110">Sperren Sie die Ressource, und berechnen Sie die Größe des Images.</span><span class="sxs-lookup"><span data-stu-id="fb320-110">Lock the resource and calculate the image's size.</span></span>
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

    

4.  <span data-ttu-id="fb320-111">Verwenden Sie die [**IWICImagingFactory:: foratestream**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createstream) -Methode, um ein [**IWICStream**](/windows/win32/api/wincodec/nn-wincodec-iwicstream) -Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="fb320-111">Use the [**IWICImagingFactory::CreateStream**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createstream) method to create an [**IWICStream**](/windows/win32/api/wincodec/nn-wincodec-iwicstream) object.</span></span>
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

    

5.  <span data-ttu-id="fb320-112">Verwenden Sie die [**IWICImagingFactory:: | atedecoderfromstream**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) -Methode zum Erstellen eines [**iwicbitmapdecoders**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapdecoder).</span><span class="sxs-lookup"><span data-stu-id="fb320-112">Use the [**IWICImagingFactory::CreateDecoderFromStream**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) method to create an [**IWICBitmapDecoder**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapdecoder).</span></span>

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

    

6.  <span data-ttu-id="fb320-113">Rufen Sie einen Frame aus dem Bild ab, und speichern Sie ihn in einem [**IWICBitmapFrameDecode**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframedecode) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="fb320-113">Retrieve a frame from the image and store it in an [**IWICBitmapFrameDecode**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

    ```C++
        if (SUCCEEDED(hr))
        {
            // Create the initial frame.
            hr = pDecoder->GetFrame(0, &pSource);
        }
    ```

    

7.  <span data-ttu-id="fb320-114">Bevor Direct2D das Image verwenden kann, muss es in das Pixel Format 32bpppbgra konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="fb320-114">Before Direct2D can use the image, it must be converted to the 32bppPBGRA pixel format.</span></span> <span data-ttu-id="fb320-115">Um das Bildformat zu konvertieren, verwenden Sie die [**IWICImagingFactory:: kreateformatconverter**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) -Methode, um ein [**IWICFormatConverter**](/windows/win32/api/wincodec/nn-wincodec-iwicformatconverter) -Objekt zu erstellen, und verwenden Sie dann die [**Initialize**](/windows/win32/api/wincodec/nf-wincodec-iwicformatconverter-initialize) -Methode des **IWICFormatConverter** -Objekts, um die Konvertierung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="fb320-115">To convert the image format, use the [**IWICImagingFactory::CreateFormatConverter**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) method to create an [**IWICFormatConverter**](/windows/win32/api/wincodec/nn-wincodec-iwicformatconverter) object, then use the **IWICFormatConverter** object's [**Initialize**](/windows/win32/api/wincodec/nf-wincodec-iwicformatconverter-initialize) method to perform the conversion.</span></span>
 
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

    

8.  <span data-ttu-id="fb320-116">Verwenden Sie abschließend die Methode " [**kreatebitmapfromwicbitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) ", um ein [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) -Objekt zu erstellen, das von einem Renderziel gezeichnet und mit anderen Direct2D-Objekten verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="fb320-116">Finally, use the [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) method to create an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) object that can be drawn by a render target and used with other Direct2D objects.</span></span>
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

    

<span data-ttu-id="fb320-117">In diesem Beispiel wurde Code weggelassen.</span><span class="sxs-lookup"><span data-stu-id="fb320-117">Some code has been omitted from this example.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fb320-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fb320-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb320-119">Laden einer Bitmap aus einer Datei</span><span class="sxs-lookup"><span data-stu-id="fb320-119">How to Load a Bitmap from a File</span></span>](how-to-load-a-direct2d-bitmap-from-a-file.md)
</dt> </dl>

 

 
