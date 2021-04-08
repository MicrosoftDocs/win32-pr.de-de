---
description: In diesem Thema wird veranschaulicht, wie ein IWICBitmapFrameDecode aus einer Anwendungs Ressource geladen wird.
ms.assetid: 2260ad3a-44d4-4fe2-aa8c-608ffc11fbfb
title: Vorgehensweise beim Laden einer Bitmap aus einer Ressource (Windows Imaging Component)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deb33ad57b3b9dac1cb5d98719c681adb38c11de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865808"
---
# <a name="how-to-load-a-bitmap-from-a-resource-windows-imaging-component"></a><span data-ttu-id="8065b-103">Vorgehensweise beim Laden einer Bitmap aus einer Ressource (Windows Imaging Component)</span><span class="sxs-lookup"><span data-stu-id="8065b-103">How to Load a Bitmap from a Resource (Windows Imaging Component)</span></span>

<span data-ttu-id="8065b-104">In diesem Thema wird veranschaulicht, wie ein [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) aus einer Anwendungs Ressource geladen wird.</span><span class="sxs-lookup"><span data-stu-id="8065b-104">This topic demonstrates how to load an [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) from an application resource.</span></span>

1.  <span data-ttu-id="8065b-105">Definieren Sie in der Anwendungs Ressourcen-Definitionsdatei (RC-Datei) die Ressource.</span><span class="sxs-lookup"><span data-stu-id="8065b-105">In the application resource definition (.rc) file , define the resource.</span></span> <span data-ttu-id="8065b-106">Im folgenden Beispiel wird eine `Image` Ressource mit dem Namen definiert `IDR_SAMPLE_IMAGE` .</span><span class="sxs-lookup"><span data-stu-id="8065b-106">The following example defines an `Image` resource named `IDR_SAMPLE_IMAGE`.</span></span>

    ```C++
    IDR_SAMPLE_IMAGE IMAGE "turtle.jpg"
    ```

    

    <span data-ttu-id="8065b-107">Die Ressource wird den Ressourcen der Anwendung hinzugefügt, wenn die Anwendung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="8065b-107">The resource will be added to the application's resources when the application is built.</span></span>

2.  <span data-ttu-id="8065b-108">Laden Sie die Ressource aus der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="8065b-108">Load the resource from the application.</span></span>

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

    

3.  <span data-ttu-id="8065b-109">Sperren Sie die Ressource, und erhalten Sie die Größe.</span><span class="sxs-lookup"><span data-stu-id="8065b-109">Lock the resource and get the size.</span></span>

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

    

4.  <span data-ttu-id="8065b-110">Verwenden Sie die Methode " [**kreatestream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) ", um ein [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) -Objekt zu erstellen, und initialisieren Sie es mit dem Bildspeicher Zeiger.</span><span class="sxs-lookup"><span data-stu-id="8065b-110">Use the [**CreateStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) method to create an [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) object and initialize it by using the image memory pointer.</span></span>

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

    

5.  <span data-ttu-id="8065b-111">Erstellen Sie einen [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) aus dem neuen Stream-Objekt mithilfe der Methode " [**kreatedecoderfromstream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) ".</span><span class="sxs-lookup"><span data-stu-id="8065b-111">Create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from the new stream object by using the [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) method.</span></span>

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

    

6.  <span data-ttu-id="8065b-112">Rufen Sie einen [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) aus dem decodierten Bild ab.</span><span class="sxs-lookup"><span data-stu-id="8065b-112">Retrieve an [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) from the decoded image.</span></span>

    ```C++
    // Retrieve the initial frame.
    if (SUCCEEDED(hr)){
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    <span data-ttu-id="8065b-113">Mit diesem Code wird nur der erste `0` Frame () des Bilds abgerufen.</span><span class="sxs-lookup"><span data-stu-id="8065b-113">This code only retrieves the first (`0`) frame of the image.</span></span> <span data-ttu-id="8065b-114">Verwenden Sie für mehrstufige Bilder [**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) , um die Anzahl der Frames im Bild zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="8065b-114">For multi-framed images, use [**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) to determine the number of frames in the image.</span></span>

## <a name="see-also"></a><span data-ttu-id="8065b-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8065b-115">See Also</span></span>

[<span data-ttu-id="8065b-116">Programmierhandbuch</span><span class="sxs-lookup"><span data-stu-id="8065b-116">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="8065b-117">Verweis</span><span class="sxs-lookup"><span data-stu-id="8065b-117">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="8065b-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8065b-118">Samples</span></span>](-wic-samples.md)


 

 



