---
description: In diesem Thema wird beschrieben, wie ein Bitmap-Decoder mit einem Stream erstellt wird.
ms.assetid: 982d2110-ff2f-43e0-a931-cb2b8146ad0a
title: Erstellen eines Decoders mithilfe eines Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b0a76badec0e2587f9136cfa6bc3ff041b76592
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362743"
---
# <a name="how-to-create-a-decoder-using-a-stream"></a><span data-ttu-id="6938f-103">Erstellen eines Decoders mithilfe eines Streams</span><span class="sxs-lookup"><span data-stu-id="6938f-103">How to Create a Decoder Using a Stream</span></span>

<span data-ttu-id="6938f-104">In diesem Thema wird beschrieben, wie ein Bitmap-Decoder mit einem Stream erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="6938f-104">This topic describes how to create a bitmap decoder by using a stream.</span></span>

<span data-ttu-id="6938f-105">So erstellen Sie einen Bitmap-Decoder mithilfe eines Streams</span><span class="sxs-lookup"><span data-stu-id="6938f-105">To create a bitmap decoder by using a stream</span></span>

1.  <span data-ttu-id="6938f-106">Laden Sie eine Bilddatei in einen Stream.</span><span class="sxs-lookup"><span data-stu-id="6938f-106">Load an image file into a stream.</span></span> <span data-ttu-id="6938f-107">In diesem Beispiel wird ein Stream für eine Anwendungs Ressource erstellt.</span><span class="sxs-lookup"><span data-stu-id="6938f-107">In this example, a stream is created for an application resource.</span></span>

    <span data-ttu-id="6938f-108">Definieren Sie in der Anwendungs Ressourcen-Definitionsdatei (RC-Datei) die Ressource.</span><span class="sxs-lookup"><span data-stu-id="6938f-108">In the application resource definition (.rc) file, define the resource.</span></span> <span data-ttu-id="6938f-109">Im folgenden Beispiel wird eine `Image` Ressource mit dem Namen definiert `IDR_SAMPLE_IMAGE` .</span><span class="sxs-lookup"><span data-stu-id="6938f-109">The following example defines an `Image` resource named `IDR_SAMPLE_IMAGE`.</span></span>

    ```C++
    IDR_SAMPLE_IMAGE IMAGE "turtle.jpg"
    ```

    

    <span data-ttu-id="6938f-110">Die Ressource wird den Ressourcen der Anwendung hinzugefügt, wenn die Anwendung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="6938f-110">The resource will be added to the application's resources when the application is built.</span></span>

2.  <span data-ttu-id="6938f-111">Laden Sie die Ressource aus der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="6938f-111">Load the resource from the application.</span></span>

    ```C++
    HRESULT hr = S_OK;

    // WIC interface pointers.
    IWICStream *pIWICStream = NULL;
    IWICBitmapDecoder *pIDecoder = NULL;
    IWICBitmapFrameDecode *pIDecoderFrame = NULL;

    // Resource management.
    HRSRC imageResHandle = NULL;
    HGLOBAL imageResDataHandle = NULL;
    void *pImageFile = NULL;
    DWORD imageFileSize = 0;

    // Locate the resource in the application's executable.
    imageResHandle = FindResource(
       NULL,             // This component.
       L"SampleImage",   // Resource name.
       L"Image");        // Resource type.

    hr = (imageResHandle ? S_OK : E_FAIL);

    // Load the resource to the HGLOBAL.
    if (SUCCEEDED(hr)){
       imageResDataHandle = LoadResource(NULL, imageResHandle);
       hr = (imageResDataHandle ? S_OK : E_FAIL);
    }
    
    ```

    

3.  <span data-ttu-id="6938f-112">Sperren Sie die Ressource, und erhalten Sie die Größe.</span><span class="sxs-lookup"><span data-stu-id="6938f-112">Lock the resource and get the size.</span></span>

    ```C++
    // Lock the resource to retrieve memory pointer.
    if (SUCCEEDED(hr)){
       pImageFile = LockResource(imageResDataHandle);
       hr = (pImageFile ? S_OK : E_FAIL);
    }

    // Calculate the size.
    if (SUCCEEDED(hr)){
       imageFileSize = SizeofResource(NULL, imageResHandle);
       hr = (imageFileSize ? S_OK : E_FAIL);
    }
    
    ```

    

4.  <span data-ttu-id="6938f-113">Erstellen Sie eine [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) , um WIC-Objekte (Windows Imaging Component) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6938f-113">Create an [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) to create Windows Imaging Component (WIC) objects.</span></span>

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

5.  <span data-ttu-id="6938f-114">Verwenden Sie die Methode " [**kreatestream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) ", um ein [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) -Objekt zu erstellen, und initialisieren Sie es mit dem Bildspeicher Zeiger.</span><span class="sxs-lookup"><span data-stu-id="6938f-114">Use the [**CreateStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) method to create an [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) object and initialize it by using the image memory pointer.</span></span>

    ```C++
    // Create a WIC stream to map onto the memory.
    if (SUCCEEDED(hr)){
       hr = m_pIWICFactory->CreateStream(&pIWICStream);
    }

    // Initialize the stream with the memory pointer and size.
    if (SUCCEEDED(hr)){
       hr = pIWICStream->InitializeFromMemory(
             reinterpret_cast<BYTE*>(pImageFile),
             imageFileSize);
    }
    ```

    

6.  <span data-ttu-id="6938f-115">Erstellen Sie einen [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) aus dem neuen Stream-Objekt mithilfe der Methode " [**kreatedecoderfromstream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) ".</span><span class="sxs-lookup"><span data-stu-id="6938f-115">Create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from the new stream object using the [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) method.</span></span>

    ```C++
    // Create a decoder for the stream.
    if (SUCCEEDED(hr)){
       hr = m_pIWICFactory->CreateDecoderFromStream(
          pIWICStream,                   // The stream to use to create the decoder
          NULL,                          // Do not prefer a particular vendor
          WICDecodeMetadataCacheOnLoad,  // Cache metadata when needed
          &pIDecoder);                   // Pointer to the decoder
    }
    ```

    

7.  <span data-ttu-id="6938f-116">Holen Sie sich den ersten [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) des Bilds.</span><span class="sxs-lookup"><span data-stu-id="6938f-116">Get the first [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) of the image.</span></span>

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    <span data-ttu-id="6938f-117">Das JPEG-Dateiformat unterstützt nur einen einzelnen Frame.</span><span class="sxs-lookup"><span data-stu-id="6938f-117">The JPEG file format only supports a single frame.</span></span> <span data-ttu-id="6938f-118">Da es sich bei der Datei in diesem Beispiel um eine JPEG-Datei handelt, wird der erste Frame ( `0` ) verwendet.</span><span class="sxs-lookup"><span data-stu-id="6938f-118">Because the file in this example is a JPEG file, the first frame (`0`) is used.</span></span> <span data-ttu-id="6938f-119">Informationen zu Bildformaten mit mehreren Frames finden [Sie unter Abrufen der Frames eines Bilds](-wic-bitmapsources-howto-retrieveimageframes.md) für den Zugriff auf die einzelnen Frames des Bilds.</span><span class="sxs-lookup"><span data-stu-id="6938f-119">For image formats that have multiple frames, see [How to Retrieve the Frames of an Image](-wic-bitmapsources-howto-retrieveimageframes.md) for accessing each frame of the image.</span></span>

8.  <span data-ttu-id="6938f-120">Verarbeiten Sie den Bildframe.</span><span class="sxs-lookup"><span data-stu-id="6938f-120">Process the image frame.</span></span> <span data-ttu-id="6938f-121">Weitere Informationen zu [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) -Objekten finden Sie in der [Übersicht über Bitmap-Quellen](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="6938f-121">For additional information about [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) objects, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="6938f-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6938f-122">See Also</span></span>

[<span data-ttu-id="6938f-123">Programmierhandbuch</span><span class="sxs-lookup"><span data-stu-id="6938f-123">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="6938f-124">Verweis</span><span class="sxs-lookup"><span data-stu-id="6938f-124">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="6938f-125">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6938f-125">Samples</span></span>](-wic-samples.md)


 

 



