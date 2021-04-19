---
description: In diesem Thema wird beschrieben, wie ein Bitmap-Decoder mithilfe eines Bild Datei namens erstellt wird.
ms.assetid: b384861d-4e71-4e07-8b44-5c1cbcb3a70f
title: Erstellen eines Decoders mit einem Bilddateinamen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 113ea82b741f2a8dab6c92d6391d65eb7d7e99c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353944"
---
# <a name="how-to-create-a-decoder-using-an-image-filename"></a><span data-ttu-id="f7f8e-103">Erstellen eines Decoders mit einem Bilddateinamen</span><span class="sxs-lookup"><span data-stu-id="f7f8e-103">How to Create a Decoder Using an Image Filename</span></span>

<span data-ttu-id="f7f8e-104">In diesem Thema wird beschrieben, wie ein Bitmap-Decoder mithilfe eines Bild Datei namens erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="f7f8e-104">This topic describes how to create a bitmap decoder by using an image filename.</span></span>

<span data-ttu-id="f7f8e-105">So erstellen Sie einen Bitmap-Decoder mit einem Bilddateinamen</span><span class="sxs-lookup"><span data-stu-id="f7f8e-105">To create a bitmap decoder by using an image filename</span></span>

1.  <span data-ttu-id="f7f8e-106">Erstellen Sie ein [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) -Objekt, um WIC-Objekte (Windows Imaging Component) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f7f8e-106">Create an [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) object to create Windows Imaging Component (WIC) objects.</span></span>

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  <span data-ttu-id="f7f8e-107">Verwenden Sie die Methode "Methode" von "| [**atedecoderfromfilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) ", um einen [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) aus einer Bilddatei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f7f8e-107">Use the [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method to create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from an image file.</span></span>

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

    

3.  <span data-ttu-id="f7f8e-108">Holen Sie sich den ersten [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) des Bilds.</span><span class="sxs-lookup"><span data-stu-id="f7f8e-108">Get the first [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) of the image.</span></span>

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    <span data-ttu-id="f7f8e-109">Das JPEG-Dateiformat unterstützt nur einen einzelnen Frame.</span><span class="sxs-lookup"><span data-stu-id="f7f8e-109">The JPEG file format only supports a single frame.</span></span> <span data-ttu-id="f7f8e-110">Da es sich bei der Datei in diesem Beispiel um eine JPEG-Datei handelt, wird der erste Frame ( `0` ) verwendet.</span><span class="sxs-lookup"><span data-stu-id="f7f8e-110">Because the file in this example is a JPEG file, the first frame (`0`) is used.</span></span> <span data-ttu-id="f7f8e-111">Informationen zu Bildformaten mit mehreren Frames finden [Sie unter Abrufen der Frames eines Bilds](-wic-bitmapsources-howto-retrieveimageframes.md) für den Zugriff auf die einzelnen Frames des Bilds.</span><span class="sxs-lookup"><span data-stu-id="f7f8e-111">For image formats that have multiple frames, see [How to Retrieve the Frames of an Image](-wic-bitmapsources-howto-retrieveimageframes.md) for accessing each frame of the image.</span></span>

4.  <span data-ttu-id="f7f8e-112">Verarbeiten Sie den Bildframe.</span><span class="sxs-lookup"><span data-stu-id="f7f8e-112">Process the image frame.</span></span> <span data-ttu-id="f7f8e-113">Weitere Informationen zu [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) -Objekten finden Sie in der [Übersicht über Bitmap-Quellen](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="f7f8e-113">For additional information about [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) objects, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="f7f8e-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f7f8e-114">See Also</span></span>

[<span data-ttu-id="f7f8e-115">Programmierhandbuch</span><span class="sxs-lookup"><span data-stu-id="f7f8e-115">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="f7f8e-116">Verweis</span><span class="sxs-lookup"><span data-stu-id="f7f8e-116">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="f7f8e-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f7f8e-117">Samples</span></span>](-wic-samples.md)


 

 



