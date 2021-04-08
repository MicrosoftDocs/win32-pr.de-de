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
# <a name="how-to-load-a-bitmap-from-a-resource-windows-imaging-component"></a>Vorgehensweise beim Laden einer Bitmap aus einer Ressource (Windows Imaging Component)

In diesem Thema wird veranschaulicht, wie ein [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) aus einer Anwendungs Ressource geladen wird.

1.  Definieren Sie in der Anwendungs Ressourcen-Definitionsdatei (RC-Datei) die Ressource. Im folgenden Beispiel wird eine `Image` Ressource mit dem Namen definiert `IDR_SAMPLE_IMAGE` .

    ```C++
    IDR_SAMPLE_IMAGE IMAGE "turtle.jpg"
    ```

    

    Die Ressource wird den Ressourcen der Anwendung hinzugefügt, wenn die Anwendung erstellt wird.

2.  Laden Sie die Ressource aus der Anwendung.

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

    

3.  Sperren Sie die Ressource, und erhalten Sie die Größe.

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

    

4.  Verwenden Sie die Methode " [**kreatestream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) ", um ein [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) -Objekt zu erstellen, und initialisieren Sie es mit dem Bildspeicher Zeiger.

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

    

5.  Erstellen Sie einen [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) aus dem neuen Stream-Objekt mithilfe der Methode " [**kreatedecoderfromstream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) ".

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

    

6.  Rufen Sie einen [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) aus dem decodierten Bild ab.

    ```C++
    // Retrieve the initial frame.
    if (SUCCEEDED(hr)){
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    Mit diesem Code wird nur der erste `0` Frame () des Bilds abgerufen. Verwenden Sie für mehrstufige Bilder [**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) , um die Anzahl der Frames im Bild zu bestimmen.

## <a name="see-also"></a>Weitere Informationen

[Programmierhandbuch](-wic-programming-guide.md)


[Verweis](-wic-codec-reference.md)


[Beispiele](-wic-samples.md)


 

 



