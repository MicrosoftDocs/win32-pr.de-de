---
title: So zählen Sie Eingabeformate auf
description: So zählen Sie Eingabeformate auf
ms.assetid: 482adfc4-d9ed-403d-912b-1a5a70baf04c
keywords:
- Advanced Systems Format (ASF), Aufzählen von Eingabe Formaten
- ASF (Advanced Systems Format), Aufzählen von Eingabe Formaten
- Profile, Auflisten von Eingabe Formaten
- Codecs, Aufzählen von Eingabe Formaten
- Advanced Systems Format (ASF), Eingabe Format-Enumerationen
- ASF (Advanced Systems Format), Eingabe formatenumerationen
- Profile, Eingabe formatenumerationen
- Codecs, Eingabe formatenumerationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18360d3172af785fd1c00648ba0c9e869fb7fbc6
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104038685"
---
# <a name="to-enumerate-input-formats"></a>So zählen Sie Eingabeformate auf

Alle Windows Media-Codecs akzeptieren mindestens einen Eingabe Datentyp für die Komprimierung. Mit dem Windows Media-Format-SDK können Sie eine größere Vielfalt von Formaten als die von den Codecs unterstützten Formate eingeben. Das SDK führt dies durch, indem bei Bedarf Vorverarbeitungs Transformationen für die Eingaben durchgeführt werden, z. b. das Ändern der Größe von Video Frames oder das erneute Sampling von Audio In jedem Fall müssen Sie sicherstellen, dass die Eingabeformate für die Dateien, die Sie schreiben, den Daten entsprechen, die Sie an den Writer senden. Jeder Codec verfügt über ein Standardformat für Eingabemedien, das beim Laden des Profils im Writer festgelegt wird. Sie können das Standardeingabe Format überprüfen, indem Sie [**iwmwriter:: GetInput-**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops)Eigenschaften aufrufen.

Die Video Codecs unterstützen die folgenden Formate: IYUV, I420, YV12, im YUY2, UYVY, yvyu, YVU9, RGB 32, RGB 24, RGB 565, RGB 555 und RGB 8. Die Audiocodecs unterstützen PCM-Audiodaten.

Führen Sie die folgenden Schritte aus, um die von einem Codec unterstützten Eingabeformate aufzulisten:

1.  Erstellen Sie ein Writer-Objekt, und legen Sie ein Profil zur Verwendung fest. Weitere Informationen zum Festlegen von Profilen im Writer finden [Sie unter So verwenden Sie Profile mit dem Writer](to-use-profiles-with-the-writer.md).
2.  Identifizieren Sie die Eingabe Nummer, für die Sie die Formate überprüfen möchten. Weitere Informationen zum Identifizieren von Eingabe Nummern finden [Sie unter So identifizieren Sie Eingaben nach Nummer](to-identify-inputs-by-number.md).
3.  Rufen Sie die Gesamtanzahl von Eingabe Formaten ab, die von der gewünschten Eingabe unterstützt werden, indem Sie [**iwmwriter:: getinputformatcount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount)aufrufen.
4.  Durchlaufen Sie alle unterstützten Eingabeformate, und führen Sie jeweils die folgenden Schritte aus.
    -   Rufen Sie die [**iwminputmediarequicenschnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) für das Eingabeformat durch Aufrufen von [**iwmwriter:: getinputformat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat)ab.
    -   Rufen Sie die [**WM- \_ \_ Medientyp**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) Struktur für das Eingabeformat ab. Nennen Sie [**iwmmedia-Eigenschaften:: getmediatype**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype), und übergeben Sie **null** für den *pType* -Parameter, um die Größe der Struktur abzurufen. Weisen Sie dann den Speicher zu, um die Struktur aufzunehmen, und wiederholen Sie dann **getmediatype** , um die Struktur abzurufen. [**Iwminputmedia-**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) Eigenschaften erbt von [**iwmmedia-**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)Eigenschaften, sodass Sie die Aufrufe von **getmediatype** aus der im vorherigen Schritt abgerufenen Instanz von **iwminputmedia-** Eigenschaften durchführen können.
    -   Das in der WM- [**\_ \_ Medientyp**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) Struktur beschriebene Format enthält alle relevanten Informationen zum Eingabeformat. Das Grundformat des Mediums wird durch den **WM- \_ \_ Medientyp. Untertyp** identifiziert. Für Videostreams verweist das **pbformat** -Element auf eine dynamisch zugeordnete [**wmvideoinfoheader**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) -Struktur, die weitere Details zum Stream einschließlich der Rechteck Größe enthält. Die Größe der Eingabe Rahmen ist nicht erforderlich, um genau eine Größe abzugleichen, die vom Codec unterstützt wird. Wenn keine Entsprechung gefunden wird, ändern die SDK-Laufzeitkomponenten in vielen Fällen automatisch die Größe der Eingabe Video Frames an den Codec, den der Codec annehmen kann.

Der folgende Beispielcode sucht das Eingabeformat des unter Typs, der als Parameter übergeben wird. Weitere Informationen zur Verwendung dieses Codes finden Sie unter [Verwenden der Codebeispiele](using-the-code-examples.md).


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

[**Iwmwriter-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Schreiben von ASF-Dateien**](writing-asf-files.md)
</dt> </dl>

 

 




