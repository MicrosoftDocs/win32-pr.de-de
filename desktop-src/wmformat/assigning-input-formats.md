---
title: Zuweisen von Eingabeformaten
description: Zuweisen von Eingabeformaten
ms.assetid: 44c4ed7e-b35e-4ab5-9975-021f343dab6a
keywords:
- Advanced Systems Format (ASF), Zuweisen von Eingabeformaten
- ASF (Advanced Systems Format), Zuweisen von Eingabeformaten
- Profile, Zuweisen von Eingabeformaten
- Codecs, Zuweisen von Eingabeformaten
- Advanced Systems Format (ASF), Eingabeformatzuweisungen
- ASF (Advanced Systems Format), Eingabeformatzuweisungen
- Profile, Eingabeformatzuweisungen
- Codecs, Eingabeformatzuweisungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6f87ec74bc5d3750d65ecc91e2df4640a6ed02c9e9a9425b27897e70f825983
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119840330"
---
# <a name="assigning-input-formats"></a>Zuweisen von Eingabeformaten

Wenn Sie das Eingabeformat identifiziert haben, das Ihren Daten entspricht, können Sie es für die Verwendung durch den Writer festlegen, indem Sie [**IWMWriter::SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops)aufrufen.

Für Videostreams müssen Sie die Größe der Frames in den Eingabebeispielen festlegen. Der folgende Beispielcode veranschaulicht das Konfigurieren und Festlegen einer Videoeingabe. Sie verwendet die **FindInputFormat-Funktion,** die im Abschnitt [To Enumerate Input Formats (Zum Aufzählen von Eingabeformaten)](to-enumerate-input-formats.md) definiert ist, um das Eingabeformat für 24-Bit-RGB-Videos abzurufen. Weitere Informationen zur Verwendung dieses Codes finden Sie unter [Verwenden der Codebeispiele.](using-the-code-examples.md)


```C++
HRESULT ConfigureVideoInput(IWMWriter* pWriter,
                            DWORD dwInput,
                            GUID guidSubType,
                            LONG lFrameWidth,
                            LONG lFrameHeight)
{
    DWORD   cbSize = 0;
    LONG    lStride = 0;

    IWMInputMediaProps* pProps  = NULL;
    WM_MEDIA_TYPE*      pType   = NULL;
    WMVIDEOINFOHEADER*  pVidHdr = NULL;
    BITMAPINFOHEADER*   pbmi    = NULL;

    // Get the base input format for the required subtype.
    HRESULT hr = FindInputFormat(pWriter, dwInput, guidSubType, &pProps);
    if (FAILED(hr))
    {
        goto Exit;
    }

    // Get the size of the media type structure.
    hr = pProps->GetMediaType(NULL, &cbSize);
    if (FAILED(hr))
    {
        goto Exit;
    }

    // Allocate memory for the media type structure.
    pType = (WM_MEDIA_TYPE*) new (std::nothrow) BYTE[cbSize];
    if (pType == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto Exit;
    }
    
    // Get the media type structure.
    hr = pProps->GetMediaType(pType, &cbSize);
    if (FAILED(hr))
    {
        goto Exit;
    }

    // Adjust the format to match your source images.

    // First set pointers to the video structures.
    pVidHdr = (WMVIDEOINFOHEADER*) pType->pbFormat;
    pbmi  = &(pVidHdr->bmiHeader);
        
    pbmi->biWidth  = lFrameWidth;  
    pbmi->biHeight = lFrameHeight;
    
    // Stride = (width * bytes/pixel), rounded to the next DWORD boundary.
    lStride = (lFrameWidth * (pbmi->biBitCount / 8) + 3) & ~3;


    // Image size = stride * height. 
    pbmi->biSizeImage = lFrameHeight * lStride;

    // Apply the adjusted type to the video input. 
    hr = pProps->SetMediaType(pType);
    if (FAILED(hr))
    {
        goto Exit;
    }

    hr = pWriter->SetInputProps(dwInput, pProps);

Exit:
    delete [] pType;
    SAFE_RELEASE(pProps);
    return hr;
}
```





## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Arbeiten mit Eingaben**](working-with-inputs.md)
</dt> </dl>

 

 




