---
description: In diesem Thema wird veranschaulicht, wie eine IWICBitmapSource mithilfe einer IWICBitmapFlipRotator-Komponente gedreht wird.
ms.assetid: 371c7759-0165-4a2a-b2ff-f9c8a31053a4
title: Vorgehensweise beim Kippen und Drehen einer Bitmap-Quelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87f6a805144025f185a4f4793fc4fafb27d7695a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128980"
---
# <a name="how-to-flip-and-rotate-a-bitmap-source"></a><span data-ttu-id="a7b51-103">Vorgehensweise beim Kippen und Drehen einer Bitmap-Quelle</span><span class="sxs-lookup"><span data-stu-id="a7b51-103">How to Flip and Rotate a Bitmap Source</span></span>

<span data-ttu-id="a7b51-104">In diesem Thema wird veranschaulicht, wie eine [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) mithilfe einer [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) -Komponente gedreht wird.</span><span class="sxs-lookup"><span data-stu-id="a7b51-104">This topic demonstrates how to rotate an [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) by using an [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) component.</span></span>

<span data-ttu-id="a7b51-105">So kippen und drehen Sie eine Bitmap-Quelle</span><span class="sxs-lookup"><span data-stu-id="a7b51-105">To flip and rotate a bitmap source</span></span>

1.  <span data-ttu-id="a7b51-106">Erstellen Sie ein [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) -Objekt, um WIC-Objekte (Windows Imaging Component) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a7b51-106">Create an [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) object to create Windows Imaging Component (WIC) objects.</span></span>

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  <span data-ttu-id="a7b51-107">Verwenden Sie die Methode "Methode" von "| [**atedecoderfromfilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) ", um einen [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) aus einer Bilddatei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a7b51-107">Use the [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method to create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from an image file.</span></span>

    ```C++
    HRESULT hr = S_OK;

    IWICBitmapDecoder *pIDecoder = NULL;
    IWICBitmapFrameDecode *pIDecoderFrame  = NULL;
    IWICBitmapFlipRotator *pIFlipRotator = NULL;

    hr = m_pIWICFactory->CreateDecoderFromFilename(
       L"turtle.jpg",                  // Image to be decoded
       NULL,                           // Do not prefer a particular vendor
       GENERIC_READ,                   // Desired read access to the file
       WICDecodeMetadataCacheOnDemand, // Cache metadata when needed
       &pIDecoder                      // Pointer to the decoder
       );
    ```

    

3.  <span data-ttu-id="a7b51-108">Holen Sie sich den ersten [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) des Bilds.</span><span class="sxs-lookup"><span data-stu-id="a7b51-108">Get the first [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) of the image.</span></span>

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    <span data-ttu-id="a7b51-109">Das JPEG-Dateiformat unterstützt nur einen einzelnen Frame.</span><span class="sxs-lookup"><span data-stu-id="a7b51-109">The JPEG file format only supports a single frame.</span></span> <span data-ttu-id="a7b51-110">Da es sich bei der Datei in diesem Beispiel um eine JPEG-Datei handelt, wird der erste Frame ( `0` ) verwendet.</span><span class="sxs-lookup"><span data-stu-id="a7b51-110">Because the file in this example is a JPEG file, the first frame (`0`) is used.</span></span> <span data-ttu-id="a7b51-111">Informationen zu Bildformaten mit mehreren Frames finden [Sie unter Abrufen der Frames eines Bilds](-wic-bitmapsources-howto-retrieveimageframes.md) für den Zugriff auf die einzelnen Frames des Bilds.</span><span class="sxs-lookup"><span data-stu-id="a7b51-111">For image formats that have multiple frames, see [How to Retrieve the Frames of an Image](-wic-bitmapsources-howto-retrieveimageframes.md) for accessing each frame of the image.</span></span>

4.  <span data-ttu-id="a7b51-112">Erstellen Sie den [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) , der zum Kippen des Bilds verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a7b51-112">Create the [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) to use for flipping the image.</span></span>

    ```C++
    // Create the flip/rotator.
    if (SUCCEEDED(hr))
    {
       hr = m_pIWICFactory->CreateBitmapFlipRotator(&pIFlipRotator);
    }
    ```

    

5.  <span data-ttu-id="a7b51-113">Initialisieren Sie das Flip/Rotator-Objekt mit den Bilddaten des horizontal gekippten bitmapframes (entlang der vertikalen y-Achse).</span><span class="sxs-lookup"><span data-stu-id="a7b51-113">Initialize the flip/rotator object with the image data of the bitmap frame flipped horizontally (along the vertical y-axis).</span></span>

    ```C++
    // Initialize the flip/rotator to flip the original source horizontally.
    if (SUCCEEDED(hr))
    {
       hr = pIFlipRotator->Initialize(
          pIDecoderFrame,                     // Bitmap source to flip.
          WICBitmapTransformFlipHorizontal);  // Flip the pixels along the 
                                              //  vertical y-axis.
    }
    ```

    

    <span data-ttu-id="a7b51-114">Weitere Rotations-und flippingoptionen finden Sie unter [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) .</span><span class="sxs-lookup"><span data-stu-id="a7b51-114">See [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) for additional rotations and flipping options.</span></span>

6.  <span data-ttu-id="a7b51-115">Zeichnen Sie die geflippte Bitmapquelle, oder verarbeiten Sie Sie.</span><span class="sxs-lookup"><span data-stu-id="a7b51-115">Draw or process the flipped bitmap source.</span></span>

    > [!Note]  
    > <span data-ttu-id="a7b51-116">Die [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) -Schnittstelle erbt von der [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) -Schnittstelle, sodass Sie das initialisierte Flip/Rotator-Objekt überall verwenden können, was eine **IWICBitmapSource** akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="a7b51-116">The [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) interface inherits from the [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) interface, so you can use the initialized flip/rotator object anywhere that accepts a **IWICBitmapSource**.</span></span>

     

    <span data-ttu-id="a7b51-117">In der folgenden Abbildung wird veranschaulicht, wie eine Bildverarbeitung horizontal (entlang der vertikalen x-Achse) gekippt wird.</span><span class="sxs-lookup"><span data-stu-id="a7b51-117">The following illustration demonstrates flipping an imaging horizontally (along the vertical x-axis).</span></span>

    ![Abbildung: ein horizontales kippen (entlang der veritalen x-Achse) eines Bilds](graphics/fliphorizontal.png)

## <a name="see-also"></a><span data-ttu-id="a7b51-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a7b51-119">See Also</span></span>

[<span data-ttu-id="a7b51-120">Programmierhandbuch</span><span class="sxs-lookup"><span data-stu-id="a7b51-120">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="a7b51-121">Verweis</span><span class="sxs-lookup"><span data-stu-id="a7b51-121">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="a7b51-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a7b51-122">Samples</span></span>](-wic-samples.md)


 

 



