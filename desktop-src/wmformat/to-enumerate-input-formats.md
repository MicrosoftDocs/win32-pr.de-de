---
title: So enumerieren Sie Eingabeformate
description: So enumerieren Sie Eingabeformate
ms.assetid: 482adfc4-d9ed-403d-912b-1a5a70baf04c
keywords:
- Advanced Systems Format (ASF), Aufzählen von Eingabeformaten
- ASF (Advanced Systems Format), Aufzählen von Eingabeformaten
- Profile,Aufzählen von Eingabeformaten
- Codecs,Aufzählen von Eingabeformaten
- Advanced Systems Format (ASF), Eingabeformatenumeration
- ASF (Advanced Systems Format), Eingabeformatenumeration
- Profile,Eingabeformatenumeration
- Codecs,Eingabeformatenumeration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09e1583c9331e9cfab26e7ac64064224111ea58858d32b876ece843b83df0d2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929250"
---
# <a name="to-enumerate-input-formats"></a>So enumerieren Sie Eingabeformate

Jeder der Windows Mediencodecs akzeptiert einen oder mehrere Arten von Eingabemedien für die Komprimierung. Mit Windows Media Format SDK können Sie eine größere Bandbreite von Formaten eingeben, als von den Codecs unterstützt werden. Das SDK führt dazu bei Bedarf Vorverarbeitungstransformationen für die Eingaben durch, z. B. das Ändern der Größe von Videoframes oder das Resampling von Audio. In jedem Fall müssen Sie sicherstellen, dass die Eingabeformate für die dateien, die Sie schreiben, mit den Daten übereinstimmen, die Sie an den Writer senden. Jeder Codec verfügt über ein Standardformat für Eingabemedien, das beim Laden des Profils im Writer festgelegt wird. Sie können das Standardeingabeformat untersuchen, indem Sie [**IWMWriter::GetInputProps aufrufen.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops)

Die Videocodecs unterstützen die folgenden Formate: IYUV, I420, YV12, YUY2, UYCLIP, YVCCA, YUV9, RGB 32, RGB 24, RGB 565, RGB 555 und RGB 8. Die Audiocodecs unterstützen PCM-Audio.

Um die von einem Codec unterstützten Eingabeformate aufzählen zu können, führen Sie die folgenden Schritte aus:

1.  Erstellen Sie ein Writerobjekt, und legen Sie ein zu verwendende Profil fest. Weitere Informationen zum Festlegen von Profilen im Writer finden Sie unter [So verwenden Sie Profile mit dem Writer](to-use-profiles-with-the-writer.md).
2.  Identifizieren Sie die Eingabenummer, für die Sie die Formate überprüfen möchten. Weitere Informationen zum Identifizieren von Eingabenummern finden Sie unter [So identifizieren Sie Eingaben nach Zahl.](to-identify-inputs-by-number.md)
3.  Rufen Sie die Gesamtzahl der Eingabeformate ab, die von der gewünschten Eingabe unterstützt werden, indem [**Sie IWMWriter::GetInputFormatCount aufrufen.**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount)
4.  Schleife durch alle unterstützten Eingabeformate, die jeweils die folgenden Schritte ausführen.
    -   Rufen Sie [**die IWMInputMediaProps-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) für das Eingabeformat ab, indem [**Sie IWMWriter::GetInputFormat aufrufen.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat)
    -   Rufen Sie die [**WM \_ MEDIA \_ TYPE-Struktur**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) für das Eingabeformat ab. Rufen [**Sie IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype)auf, und übergeben Sie **NULL** für den *pType-Parameter,* um die Größe der Struktur zu erhalten. Ordnen Sie dann Arbeitsspeicher zu, um die Struktur zu halten, und rufen **Sie Erneut GetMediaType** auf, um die Struktur zu erhalten. [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) erbt von [**IWMMediaProps,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)sodass Sie die Aufrufe von **GetMediaType** aus der Instanz **von IWMInputMediaProps,** die im vorherigen Schritt abgerufen wurde, tätigen können.
    -   Das in der [**WM \_ MEDIA \_ TYPE-Struktur**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) beschriebene Format enthält alle relevanten Informationen zum Eingabeformat. Das grundlegende Format des Mediums wird durch **WM \_ MEDIA \_ TYPE.subtype identifiziert.** Bei Videostreams verweist **das pbFormat-Element** auf eine dynamisch zugeordnete [**WMVIDEOINFOHEADER-Struktur,**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) die weitere Details zum Stream enthält, einschließlich der Rechteckgröße. Die Größe der Eingabeframes muss nicht genau mit einer vom Codec unterstützten Größe übereinstimmen. Wenn sie nicht übereinstimmen, ändern die SDK-Laufzeitkomponenten in vielen Fällen automatisch die Größe der Eingabevideoframes so, dass sie vom Codec akzeptiert werden können.

Der folgende Beispielcode sucht das Eingabeformat des Untertyps, der als Parameter übergeben wird. Weitere Informationen zur Verwendung dieses Codes finden Sie unter [Verwenden der Codebeispiele](using-the-code-examples.md).


```C++
HRESULT FindInputFormat(IWMWriter* pWriter, 
                       DWORD dwInput,
                       GUID guidSubType,
                       IWMInputMediaProps** ppProps)
{
    DWORD   cFormats = 0;
    DWORD   cbSize   = 0;

    WM_MEDIA_TYPE*      pType  = NULL;
    IWMInputMediaProps* pProps = NULL;

    // Set the ppProps parameter to point to NULL. This will
    //  be used to check the results of the function later.
    *ppProps = NULL;

    // Find the number of formats supported by this input.
    HRESULT hr = pWriter->GetInputFormatCount(dwInput, &cFormats);
    if (FAILED(hr))
    {
        goto Exit;
    }
    // Loop through all of the supported formats.
    for (DWORD formatIndex = 0; formatIndex < cFormats; formatIndex++)
    {
        // Get the input media properties for the input format.
        hr = pWriter->GetInputFormat(dwInput, formatIndex, &pProps);
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

        if(pType->subtype == guidSubType)
        {
            *ppProps = pProps;
            (*ppProps)->AddRef();
            goto Exit;
        }

        // Clean up for next iteration.
        delete [] pType;
        pType = NULL;
        SAFE_RELEASE(pProps);
    } // End for formatIndex.

    // If execution made it to this point, no matching format was found.
    hr = NS_E_INVALID_INPUT_FORMAT;

Exit:
    delete [] pType;
    SAFE_RELEASE(pProps);
    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWMWriter-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Schreiben von ASF-Dateien**](writing-asf-files.md)
</dt> </dl>

 

 




