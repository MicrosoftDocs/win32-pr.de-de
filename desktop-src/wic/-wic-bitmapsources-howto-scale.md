---
description: In diesem Thema wird veranschaulicht, wie eine IWICBitmapSource mithilfe der IWICBitmapScaler-Komponente skaliert wird.
ms.assetid: d2c65c9b-6f52-46f7-935d-0c582ca83867
title: Skalieren einer Bitmap-Quelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 737f72014929065bc63ec9c6021b05e38799d06e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128976"
---
# <a name="how-to-scale-a-bitmap-source"></a><span data-ttu-id="1df50-103">Skalieren einer Bitmap-Quelle</span><span class="sxs-lookup"><span data-stu-id="1df50-103">How to Scale a Bitmap Source</span></span>

<span data-ttu-id="1df50-104">In diesem Thema wird veranschaulicht, wie eine [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) mithilfe der [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) -Komponente skaliert wird.</span><span class="sxs-lookup"><span data-stu-id="1df50-104">This topic demonstrates how to scale an [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) using the [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) component.</span></span>

<span data-ttu-id="1df50-105">So skalieren Sie eine Bitmap-Quelle</span><span class="sxs-lookup"><span data-stu-id="1df50-105">To scale a bitmap source</span></span>

1.  <span data-ttu-id="1df50-106">Erstellen Sie ein [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) -Objekt, um WIC-Objekte (Windows Imaging Component) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1df50-106">Create an [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) object to create Windows Imaging Component (WIC) objects.</span></span>

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  <span data-ttu-id="1df50-107">Verwenden Sie die Methode "Methode" von "| [**atedecoderfromfilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) ", um einen [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) aus einer Bilddatei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1df50-107">Use the [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method to create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from an image file.</span></span>

    ```C++
    HRESULT hr = S_OK;

    IWICBitmapDecoder *pIDecoder = NULL;
    IWICBitmapFrameDecode *pIDecoderFrame  = NULL;
    IWICBitmapScaler *pIScaler = NULL;


    hr = m_pIWICFactory->CreateDecoderFromFilename(
       L"turtle.jpg",                  // Image to be decoded
       NULL,                           // Do not prefer a particular vendor
       GENERIC_READ,                   // Desired read access to the file
       WICDecodeMetadataCacheOnDemand, // Cache metadata when needed
       &pIDecoder                      // Pointer to the decoder
       );
    ```

    

3.  <span data-ttu-id="1df50-108">Holen Sie sich den ersten [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) des Bilds.</span><span class="sxs-lookup"><span data-stu-id="1df50-108">Get the first [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) of the image.</span></span>

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    <span data-ttu-id="1df50-109">Das JPEG-Dateiformat unterstützt nur einen einzelnen Frame.</span><span class="sxs-lookup"><span data-stu-id="1df50-109">The JPEG file format only supports a single frame.</span></span> <span data-ttu-id="1df50-110">Da es sich bei der Datei in diesem Beispiel um eine JPEG-Datei handelt, wird der erste Frame ( `0` ) verwendet.</span><span class="sxs-lookup"><span data-stu-id="1df50-110">Because the file in this example is a JPEG file, the first frame (`0`) is used.</span></span> <span data-ttu-id="1df50-111">Informationen zu Bildformaten mit mehreren Frames finden [Sie unter Abrufen der Frames eines Bilds](-wic-bitmapsources-howto-retrieveimageframes.md) für den Zugriff auf die einzelnen Frames des Bilds.</span><span class="sxs-lookup"><span data-stu-id="1df50-111">For image formats that have multiple frames, see [How to Retrieve the Frames of an Image](-wic-bitmapsources-howto-retrieveimageframes.md) for accessing each frame of the image.</span></span>

4.  <span data-ttu-id="1df50-112">Erstellen Sie das [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) -Element, das für die Bildskalierung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1df50-112">Create the [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) to use for the image scaling.</span></span>

    ```C++
    // Create the scaler.
    if (SUCCEEDED(hr))
    {
       hr = m_pIWICFactory->CreateBitmapScaler(&pIScaler);
    }
    ```

    

5.  <span data-ttu-id="1df50-113">Initialisieren Sie das Scaler-Objekt mit den Bilddaten des bitmapframes in der Hälfte der Größe.</span><span class="sxs-lookup"><span data-stu-id="1df50-113">Initialize the scaler object with the image data of the bitmap frame at half the size.</span></span>

    ```C++
    // Initialize the scaler to half the size of the original source.
    if (SUCCEEDED(hr))
    {
       hr = pIScaler->Initialize(
          pIDecoderFrame,                    // Bitmap source to scale.
          uiWidth/2,                         // Scale width to half of original.
          uiHeight/2,                        // Scale height to half of original.
          WICBitmapInterpolationModeFant);   // Use Fant mode interpolation.
    }
    ```

    

6.  <span data-ttu-id="1df50-114">Zeichnen Sie die skalierte Bitmapquelle, oder verarbeiten Sie Sie.</span><span class="sxs-lookup"><span data-stu-id="1df50-114">Draw or process the scaled bitmap source.</span></span>

    <span data-ttu-id="1df50-115">Die folgende Abbildung veranschaulicht die Skalierung von Skalierungen.</span><span class="sxs-lookup"><span data-stu-id="1df50-115">The following illustration demonstrates imaging scaling.</span></span> <span data-ttu-id="1df50-116">Das ursprüngliche Bild auf der linken Seite ist 200 x 130 Pixel.</span><span class="sxs-lookup"><span data-stu-id="1df50-116">The original image on the left is 200 x 130 pixels.</span></span> <span data-ttu-id="1df50-117">Das Bild auf der rechten Seite ist das ursprüngliche Bild, das auf die Hälfte der Größe skaliert wird.</span><span class="sxs-lookup"><span data-stu-id="1df50-117">The image on the right is the original image scaled to half the size.</span></span>

    ![Abbildung der Skalierung eines Bilds auf eine geringere Größe](graphics/scaledregion.png)

## <a name="see-also"></a><span data-ttu-id="1df50-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1df50-119">See Also</span></span>

[<span data-ttu-id="1df50-120">Programmierhandbuch</span><span class="sxs-lookup"><span data-stu-id="1df50-120">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="1df50-121">Verweis</span><span class="sxs-lookup"><span data-stu-id="1df50-121">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="1df50-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1df50-122">Samples</span></span>](-wic-samples.md)


 

 



