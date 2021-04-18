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
# <a name="how-to-modify-the-pixels-of-a-bitmap-source"></a><span data-ttu-id="64a95-103">Ändern der Pixel einer Bitmap-Quelle</span><span class="sxs-lookup"><span data-stu-id="64a95-103">How to Modify the Pixels of a Bitmap Source</span></span>

<span data-ttu-id="64a95-104">In diesem Thema wird veranschaulicht, wie die Pixel einer Bitmap-Quelle mithilfe der [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) -und der [**iwicbitmaplock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) -Komponente geändert werden.</span><span class="sxs-lookup"><span data-stu-id="64a95-104">This topic demonstrates how to modify the pixels of a bitmap source using the [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) and [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) components.</span></span>

<span data-ttu-id="64a95-105">So ändern Sie die Pixel einer Bitmap-Quelle</span><span class="sxs-lookup"><span data-stu-id="64a95-105">To modify the pixels of a bitmap source</span></span>

1.  <span data-ttu-id="64a95-106">Erstellen Sie ein [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) -Objekt, um WIC-Objekte (Windows Imaging Component) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="64a95-106">Create an [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) object to create Windows Imaging Component (WIC) objects.</span></span>

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  <span data-ttu-id="64a95-107">Verwenden Sie die Methode "Methode" von "| [**atedecoderfromfilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) ", um einen [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) aus einer Bilddatei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="64a95-107">Use the [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method to create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from an image file.</span></span>

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

    

3.  <span data-ttu-id="64a95-108">Holen Sie sich den ersten [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) des Bilds.</span><span class="sxs-lookup"><span data-stu-id="64a95-108">Get the first [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) of the image.</span></span>

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    <span data-ttu-id="64a95-109">Das JPEG-Dateiformat unterstützt nur einen einzelnen Frame.</span><span class="sxs-lookup"><span data-stu-id="64a95-109">The JPEG file format only supports a single frame.</span></span> <span data-ttu-id="64a95-110">Da es sich bei der Datei in diesem Beispiel um eine JPEG-Datei handelt, wird der erste Frame ( `0` ) verwendet.</span><span class="sxs-lookup"><span data-stu-id="64a95-110">Because the file in this example is a JPEG file, the first frame (`0`) is used.</span></span> <span data-ttu-id="64a95-111">Informationen zu Bildformaten mit mehreren Frames finden [Sie unter Abrufen der Frames eines Bilds](-wic-bitmapsources-howto-retrieveimageframes.md) für den Zugriff auf die einzelnen Frames des Bilds.</span><span class="sxs-lookup"><span data-stu-id="64a95-111">For image formats that have multiple frames, see [How to Retrieve the Frames of an Image](-wic-bitmapsources-howto-retrieveimageframes.md) for accessing each frame of the image.</span></span>

4.  <span data-ttu-id="64a95-112">Erstellen Sie eine [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) aus dem zuvor Abbild Frame.</span><span class="sxs-lookup"><span data-stu-id="64a95-112">Create an [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) from the previously obtained image frame.</span></span>

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

    

5.  <span data-ttu-id="64a95-113">Rufen Sie eine [**iwicbitmaplock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) für ein angegebenes Rechteck der [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)ab.</span><span class="sxs-lookup"><span data-stu-id="64a95-113">Obtain an [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) for a specified rectangle of the [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap).</span></span>

    ```C++
    if (SUCCEEDED(hr))
    {
       // Obtain a bitmap lock for exclusive write.
       // The lock is for a 10x10 rectangle starting at the top left of the
       // bitmap.
       hr = pIBitmap->Lock(&rcLock, WICBitmapLockWrite, &pILock);
    ```

    

6.  <span data-ttu-id="64a95-114">Verarbeiten Sie die Pixeldaten, die jetzt vom [**iwicbitmaplock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) -Objekt gesperrt sind.</span><span class="sxs-lookup"><span data-stu-id="64a95-114">Process the pixel data that is now locked by the [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) object.</span></span>

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

    

    <span data-ttu-id="64a95-115">Um die [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)zu entsperren, nennen Sie [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) für alle [**iwicbitmaplock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) -Objekte, die der **IWICBitmap** zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="64a95-115">To unlock the [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap), call [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on all [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) objects associated with the **IWICBitmap**.</span></span>

7.  <span data-ttu-id="64a95-116">Bereinigen Sie erstellte Objekte.</span><span class="sxs-lookup"><span data-stu-id="64a95-116">Clean up created objects.</span></span>

    ```C++
    SafeRelease(&pIBitmap);
    SafeRelease(&pIDecoder);
    SafeRelease(&pIDecoderFrame);
    ```

    

## <a name="see-also"></a><span data-ttu-id="64a95-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="64a95-117">See Also</span></span>

[<span data-ttu-id="64a95-118">Programmierhandbuch</span><span class="sxs-lookup"><span data-stu-id="64a95-118">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="64a95-119">Verweis</span><span class="sxs-lookup"><span data-stu-id="64a95-119">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="64a95-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="64a95-120">Samples</span></span>](-wic-samples.md)


 

 
