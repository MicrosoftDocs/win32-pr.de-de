---
description: In diesem Thema wird veranschaulicht, wie ein rechteckiger Teil einer IWICBitmapSource mithilfe einer iwicbitmapclipperkomponente abgerufen wird.
ms.assetid: c9834827-8e1d-436d-be82-c1a2a2f7ca5c
title: Vorgehensweise beim Abschneiden einer Bitmap-Quelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43919e03d5d866d37ad4af203e741d2b10e60889
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104567618"
---
# <a name="how-to-clip-a-bitmap-source"></a><span data-ttu-id="97b2f-103">Vorgehensweise beim Abschneiden einer Bitmap-Quelle</span><span class="sxs-lookup"><span data-stu-id="97b2f-103">How to Clip a Bitmap Source</span></span>

<span data-ttu-id="97b2f-104">In diesem Thema wird veranschaulicht, wie ein rechteckiger Teil einer [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) mithilfe einer [**iwicbitmapclipperkomponente**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="97b2f-104">This topic demonstrates how to obtain a rectangular portion of an [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) using an [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) component.</span></span>

<span data-ttu-id="97b2f-105">So schneiden Sie eine Bitmap-Quelle ab</span><span class="sxs-lookup"><span data-stu-id="97b2f-105">To clip a bitmap source</span></span>

1.  <span data-ttu-id="97b2f-106">Erstellen Sie ein [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) -Objekt, um WIC-Objekte (Windows Imaging Component) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="97b2f-106">Create an [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) object to create Windows Imaging Component (WIC) objects.</span></span>

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  <span data-ttu-id="97b2f-107">Verwenden Sie die Methode "Methode" von "| [**atedecoderfromfilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) ", um einen [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) aus einer Bilddatei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="97b2f-107">Use the [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method to create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from an image file.</span></span>

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

    

3.  <span data-ttu-id="97b2f-108">Holen Sie sich den ersten [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) des Bilds.</span><span class="sxs-lookup"><span data-stu-id="97b2f-108">Get the first [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) of the image.</span></span>

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    <span data-ttu-id="97b2f-109">Das JPEG-Dateiformat unterstützt nur einen einzelnen Frame.</span><span class="sxs-lookup"><span data-stu-id="97b2f-109">The JPEG file format only supports a single frame.</span></span> <span data-ttu-id="97b2f-110">Da es sich bei der Datei in diesem Beispiel um eine JPEG-Datei handelt, wird der erste Frame ( `0` ) verwendet.</span><span class="sxs-lookup"><span data-stu-id="97b2f-110">Because the file in this example is a JPEG file, the first frame (`0`) is used.</span></span> <span data-ttu-id="97b2f-111">Informationen zu Bildformaten mit mehreren Frames finden [Sie unter Abrufen der Frames eines Bilds](-wic-bitmapsources-howto-retrieveimageframes.md) für den Zugriff auf die einzelnen Frames des Bilds.</span><span class="sxs-lookup"><span data-stu-id="97b2f-111">For image formats that have multiple frames, see [How to Retrieve the Frames of an Image](-wic-bitmapsources-howto-retrieveimageframes.md) for accessing each frame of the image.</span></span>

4.  <span data-ttu-id="97b2f-112">Erstellen Sie den [**iwicbitmapclippertyp**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) , der für das Abbild Clipping verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="97b2f-112">Create the [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) to use for the image clipping.</span></span>

    ```C++
    IWICBitmapClipper *pIClipper = NULL;

    if (SUCCEEDED(hr))
    {
       hr = m_pIWICFactory->CreateBitmapClipper(&pIClipper);
    }
    ```

    

5.  <span data-ttu-id="97b2f-113">Initialisieren Sie das Clipper-Objekt mit den Bilddaten innerhalb des angegebenen Rechtecks des bitmapframes.</span><span class="sxs-lookup"><span data-stu-id="97b2f-113">Initialize the clipper object with the image data within the given rectangle of the bitmap frame.</span></span>

    ```C++
    // Create the clipping rectangle.
    WICRect rcClip = { 0, 0, uiWidth/2, uiHeight/2 };

    // Initialize the clipper with the given rectangle of the frame's image data.
    if (SUCCEEDED(hr))
    {
       hr = pIClipper->Initialize(pIDecoderFrame, &rcClip);
    }
    ```

    

6.  <span data-ttu-id="97b2f-114">Zeichnen oder verarbeiten Sie das abgeschnittene Bild.</span><span class="sxs-lookup"><span data-stu-id="97b2f-114">Draw or process the clipped image.</span></span>

    <span data-ttu-id="97b2f-115">In der folgenden Abbildung wird die Abbild Erstellung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="97b2f-115">The following illustration demonstrates imaging clipping.</span></span> <span data-ttu-id="97b2f-116">Das ursprüngliche Bild auf der linken Seite ist 200 x 130 Pixel.</span><span class="sxs-lookup"><span data-stu-id="97b2f-116">The original image on the left is 200 x 130 pixels.</span></span> <span data-ttu-id="97b2f-117">Das Bild auf der rechten Seite ist das ursprüngliche Bild, das auf ein als definiertes Rechteck zugeschnitten ist `{20,20,100,100}` .</span><span class="sxs-lookup"><span data-stu-id="97b2f-117">The image on the right is the original image clipped to a rectangle defined as `{20,20,100,100}`.</span></span>

    ![Abbildung der Abbild Erstellung](graphics/cliparegion_axisalignedclip.png)

## <a name="see-also"></a><span data-ttu-id="97b2f-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="97b2f-119">See Also</span></span>

[<span data-ttu-id="97b2f-120">Programmierhandbuch</span><span class="sxs-lookup"><span data-stu-id="97b2f-120">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="97b2f-121">Verweis</span><span class="sxs-lookup"><span data-stu-id="97b2f-121">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="97b2f-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="97b2f-122">Samples</span></span>](-wic-samples.md)


 

 



