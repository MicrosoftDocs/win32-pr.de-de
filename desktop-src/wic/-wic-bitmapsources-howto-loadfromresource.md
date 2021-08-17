---
description: In diesem Thema wird veranschaulicht, wie sie einen IWICBitmapFrameDecode aus einer Anwendungsressource laden.
ms.assetid: 2260ad3a-44d4-4fe2-aa8c-608ffc11fbfb
title: Laden einer Bitmap aus einer Ressource (Windows Imaging-Komponente)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88bc10766ed6720e60dd85a9600107c883da80d7b326ddd810b6261e509915da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118034742"
---
# <a name="how-to-load-a-bitmap-from-a-resource-windows-imaging-component"></a>Laden einer Bitmap aus einer Ressource (Windows Imaging-Komponente)

In diesem Thema wird veranschaulicht, wie sie [**einen IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) aus einer Anwendungsressource laden.

1.  Definieren Sie in der Anwendungsressourcendefinitionsdatei (RC) die Ressource. Im folgenden Beispiel wird eine Ressource `Image` mit dem Namen `IDR_SAMPLE_IMAGE` definiert.

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

    

4.  Verwenden Sie die [**CreateStream-Methode,**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) um ein [**IWICStream-Objekt zu**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) erstellen und es mithilfe des Bildspeicherzeigers zu initialisieren.

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

    

5.  Erstellen Sie mithilfe der [**CreateDecoderFromStream-Methode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) einen [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) aus dem neuen Streamobjekt.

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

    

6.  Rufen Sie [**einen IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) aus dem decodierten Bild ab.

    ```C++
    // Retrieve the initial frame.
    if (SUCCEEDED(hr)){
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    Dieser Code ruft nur den ersten Frame `0` () des Bilds ab. Verwenden Sie für Bilder mit mehreren Frames [**GetFrameCount,**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) um die Anzahl der Frames im Bild zu bestimmen.

## <a name="see-also"></a>Weitere Informationen

[Programmierhandbuch](-wic-programming-guide.md)


[Referenz](-wic-codec-reference.md)


[Beispiele](-wic-samples.md)


 

 



