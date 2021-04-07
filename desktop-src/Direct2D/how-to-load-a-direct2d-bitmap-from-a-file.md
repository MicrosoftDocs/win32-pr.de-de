---
title: Laden einer Bitmap aus einer Datei
description: Zeigt, wie eine Direct2D-Bitmap aus einer Bilddatei geladen wird.
ms.assetid: 4abfbc2b-2730-4d96-897e-1e2232383a72
ms.topic: article
ms.date: 03/09/2019
ms.openlocfilehash: c9590e799e71e92056157b75573565cf79b9236b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728897"
---
# <a name="how-to-load-a-bitmap-from-a-file"></a><span data-ttu-id="2b966-103">Laden einer Bitmap aus einer Datei</span><span class="sxs-lookup"><span data-stu-id="2b966-103">How to Load a Bitmap from a File</span></span>

<span data-ttu-id="2b966-104">Direct2D verwendet die Windows Imaging Component (WIC) zum Laden von Bitmaps.</span><span class="sxs-lookup"><span data-stu-id="2b966-104">Direct2D uses the Windows Imaging Component (WIC) to load bitmaps.</span></span> <span data-ttu-id="2b966-105">Zum Laden einer Bitmap aus einer Datei verwenden Sie zunächst WIC-Objekte zum Laden des Bilds und zum Konvertieren in ein Direct2D-kompatibles Format. verwenden Sie dann die Methode " [**kreatebitmapfromwicbitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) ", um eine [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2b966-105">To load a bitmap from a file, first use WIC objects to load the image and to convert it to a Direct2D-compatible format, then use the [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) method to create an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span></span>

1.  <span data-ttu-id="2b966-106">Erstellen Sie einen [**IWICBitmapDecoder**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapdecoder) mithilfe der [**IWICImagingFactory:: dedeedecoderfromfilename**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) -Methode.</span><span class="sxs-lookup"><span data-stu-id="2b966-106">Create an [**IWICBitmapDecoder**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapdecoder) by using the [**IWICImagingFactory::CreateDecoderFromFileName**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method.</span></span>

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

    

2.  <span data-ttu-id="2b966-107">Rufen Sie einen Frame aus dem Bild ab, und speichern Sie den Frame in einem [**IWICBitmapFrameDecode**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframedecode) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="2b966-107">Retrieve a frame from the image and store the frame in an [**IWICBitmapFrameDecode**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

    ```C++
        if (SUCCEEDED(hr))
        {
            // Create the initial frame.
            hr = pDecoder->GetFrame(0, &pSource);
        }
    ```

    

3.  <span data-ttu-id="2b966-108">Die Bitmap muss in ein Format konvertiert werden, das von Direct2D verwendet werden kann, sodass das Pixel Format des Bilds in 32bpppbgra konvertiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="2b966-108">The bitmap must be converted to a format that Direct2D can use, so convert the image's pixel format to 32bppPBGRA.</span></span> <span data-ttu-id="2b966-109">(Eine Liste der unterstützten Formate finden Sie unter [Pixel Formate und Alpha Modi](supported-pixel-formats-and-alpha-modes.md).)</span><span class="sxs-lookup"><span data-stu-id="2b966-109">(For a list of supported formats, see [Pixel Formats and Alpha Modes](supported-pixel-formats-and-alpha-modes.md).).</span></span> <span data-ttu-id="2b966-110">Rufen Sie die [**IWICImagingFactory:: up-FormatConverter**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) -Methode auf, um ein [**IWICFormatConverter**](/windows/win32/api/wincodec/nn-wincodec-iwicformatconverter) -Objekt zu erstellen, und rufen Sie dann die [**Initialize**](/windows/win32/api/wincodec/nf-wincodec-iwicformatconverter-initialize) -Methode des **IWICFormatConverter** -Objekts auf, um die Konvertierung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="2b966-110">Call the [**IWICImagingFactory::CreateFormatConverter**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) method to create an [**IWICFormatConverter**](/windows/win32/api/wincodec/nn-wincodec-iwicformatconverter) object, then call the **IWICFormatConverter** object's [**Initialize**](/windows/win32/api/wincodec/nf-wincodec-iwicformatconverter-initialize) method to perform the conversion.</span></span>
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

    

4.  <span data-ttu-id="2b966-111">Rufen Sie die Methode "| [**atebitmapfromwicbitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) " auf, um ein [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) -Objekt zu erstellen, das von einem Renderziel gezeichnet und mit anderen Direct2D-Objekten verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="2b966-111">Call the [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) method to create an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) object that can be drawn by a render target and used with other Direct2D objects.</span></span>
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

    

<span data-ttu-id="2b966-112">In diesem Beispiel wurde Code weggelassen.</span><span class="sxs-lookup"><span data-stu-id="2b966-112">Some code has been omitted from this example.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b966-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2b966-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b966-114">**ID2D1Bitmap**</span><span class="sxs-lookup"><span data-stu-id="2b966-114">**ID2D1Bitmap**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)
</dt> <dt>

[<span data-ttu-id="2b966-115">**"Kreatebitmapfromwicbitmap"**</span><span class="sxs-lookup"><span data-stu-id="2b966-115">**CreateBitmapFromWicBitmap**</span></span>](id2d1rendertarget-createbitmapfromwicbitmap.md)
</dt> <dt>

[<span data-ttu-id="2b966-116">Laden einer Bitmap aus einer Ressource</span><span class="sxs-lookup"><span data-stu-id="2b966-116">How to Load a Bitmap from a Resource</span></span>](how-to-load-a-bitmap-from-a-resource.md)
</dt> </dl>

 

 