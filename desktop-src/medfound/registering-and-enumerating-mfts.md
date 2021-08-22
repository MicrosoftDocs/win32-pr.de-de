---
description: In diesem Abschnitt wird beschrieben, wie sie Media Foundation Transformationen aufzählen und ein benutzerdefiniertes MFT registrieren, damit Anwendungen es ermitteln können.
ms.assetid: 76d2a703-4162-428e-a4ff-643e346eacfb
title: Registrieren und Aufzählen von MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a3110351479f2a906d68b6c054d9e23886cbcd4cdb031fc8a4951a1d4b8d1e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119101829"
---
# <a name="registering-and-enumerating-mfts"></a>Registrieren und Aufzählen von MFTs

In diesem Abschnitt wird beschrieben, wie sie Media Foundation Transformationen aufzählen und ein benutzerdefiniertes MFT registrieren, damit Anwendungen es ermitteln können.

-   [Aufzählen von MFTs](#registering-and-enumerating-mfts)
-   [Registrieren von MFTs](#registering-mfts)
-   [Zugehörige Themen](#related-topics)

## <a name="enumerating-mfts"></a>Aufzählen von MFTs

Um MFTs zu ermitteln, die auf dem System registriert sind, kann eine Anwendung die [**MFTEnumEx-Funktion**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) aufrufen.

> [!Note]  
> Diese Funktion erfordert Windows 7. Vor Windows 7 sollten Anwendungen stattdessen die [**MFTEnum-Funktion**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) verwenden.

 

Diese Funktion nimmt die folgenden Informationen als Eingabe an:

-   Die Kategorie des aufzuzählenden MFT, z. B. Videodecoder oder Audiodecoder.
-   Ein zu gleichendes Eingabe- oder Ausgabeformat.
-   Flags, die zusätzliche Suchbedingungen angeben.

Die Funktion gibt ein Array von [**POINTERActivate-Zeigern**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) zurück, von denen jeder einen MFT darstellt, der den Enumerationskriterien entspricht.

Der folgende Code listet z. B. Windows Medienvideodecoder auf:


```C++
HRESULT hr = S_OK;
UINT32 count = 0;

IMFActivate **ppActivate = NULL;    // Array of activation objects.
IMFTransform *pDecoder = NULL;      // Pointer to the decoder.

// Match WMV3 video.
MFT_REGISTER_TYPE_INFO info = { MFMediaType_Video, MFVideoFormat_WMV3 };

UINT32 unFlags = MFT_ENUM_FLAG_SYNCMFT  | 
                 MFT_ENUM_FLAG_LOCALMFT | 
                 MFT_ENUM_FLAG_SORTANDFILTER;

hr = MFTEnumEx(
    MFT_CATEGORY_VIDEO_DECODER,
    unFlags,
    &info,      // Input type
    NULL,       // Output type
    &ppActivate,
    &count
    );


if (SUCCEEDED(hr) && count == 0)
{
    hr = MF_E_TOPO_CODEC_NOT_FOUND;
}

// Create the first decoder in the list.

if (SUCCEEDED(hr))
{
    hr = ppActivate[0]->ActivateObject(IID_PPV_ARGS(&pDecoder));
}

for (UINT32 i = 0; i < count; i++)
{
    ppActivate[i]->Release();
}
CoTaskMemFree(ppActivate);
```



Standardmäßig werden einige MFT-Typen von der -Enumeration ausgeschlossen, einschließlich asynchroner MFTs, Hardware-MFTs und MFTs mit Feld-of-Use-Restructions. Diese werden ausgeschlossen, da sie alle eine spezielle Behandlung erfordern. Verwenden Sie den *Flags-Parameter* von [**MFTEnumEx,**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) um den Standardwert zu ändern. Um beispielsweise Hardware-MFTs in die Enumerationsergebnisse einzubetten, legen Sie das **Hardwareflag MFT \_ ENUM \_ FLAG \_** fest:


```C++
UINT32 unFlags = MFT_ENUM_FLAG_HARDWARE |
                 MFT_ENUM_FLAG_SYNCMFT  | 
                 MFT_ENUM_FLAG_LOCALMFT | 
                 MFT_ENUM_FLAG_SORTANDFILTER;
hr = MFTEnumEx(
    MFT_CATEGORY_VIDEO_DECODER,
    unFlags,
    &info,      // Input type
    NULL,       // Output type
    &ppActivate,
    &count
    );
```



## <a name="registering-mfts"></a>Registrieren von MFTs

Wenn Sie eine Media Foundation-Transformation (MFT) registrieren, werden zwei Arten von Informationen in die Registrierung geschrieben:

-   Die CLSID des MFT, sodass Clients **CoCreateInstance** oder **CoGetClassObject** aufrufen können, um eine Instanz des MFT zu erstellen. Dieser Registrierungseintrag folgt dem Standardformat für COM-Klassenfactorys. Weitere Informationen finden Sie in der Windows SDK-Dokumentation für die Component Object Model (COM).
-   Informationen, die es einer Anwendung ermöglichen, MFTs nach Funktionskategorie aufzuzählen.

Um die MFT-Enumerationseinträge in der Registrierung zu erstellen, rufen Sie die [**MFTRegister-Funktion auf.**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) Sie können die folgenden Informationen zum MFT einschließen:

-   Die Kategorie des MFT, z. B. Videodecoder oder Videoencoder. Eine Liste der Kategorien finden Sie unter [**MFT \_ CATEGORY**](mft-category.md).
-   Eine Liste der Vom MFT unterstützten Eingabe- und Ausgabeformate. Jedes Format wird durch einen Haupttyp und einen Untertyp definiert. (Um ausführlichere Formatinformationen zu erhalten, muss der Client den MFT erstellen und [**DIE METHODEN VONTRANSFORM**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) aufrufen.) Das Topologieladeprogramm verwendet diese Informationen, wenn eine Teiltopologie aufgelöst wird.

Um die Einträge aus der Registrierung zu entfernen, rufen Sie [**MFTUnregister**](/windows/desktop/api/mfapi/nf-mfapi-mftunregister)auf.

Der folgende Code zeigt, wie Sie einen MFT registrieren. In diesem Beispiel wird davon ausgegangen, dass der MFT-Effekt ein Videoeffekt ist, der die gleichen Formate für Eingabe und Ausgabe unterstützt.


```C++
// CLSID of the MFT.
extern const GUID CLSID_MyVideoEffectMFT;

// DllRegisterServer: Creates the registry entries.
STDAPI DllRegisterServer()
{
    HRESULT hr = S_OK;

    // Array of media types.
    MFT_REGISTER_TYPE_INFO aMediaTypes[] =
    {
        {   MFMediaType_Video, MFVideoFormat_NV12 },
        {   MFMediaType_Video, MFVideoFormat_YUY2 },
        {   MFMediaType_Video, MFVideoFormat_UYVY },
    };

    // Size of the array.
    const DWORD cNumMediaTypes = ARRAY_SIZE(aMediaTypes);

    hr = MFTRegister(
        CLSID_MyVideoEffectMFT,     // CLSID.
        MFT_CATEGORY_VIDEO_EFFECT,  // Category.
        L"My Video Effect",         // Friendly name.
        0,                          // Reserved, must be zero.
        cNumMediaTypes,             // Number of input types.
        aMediaTypes,                // Input types.
        cNumMediaTypes,             // Number of output types.
        aMediaTypes,                // Output types.
        NULL                        // Attributes (optional).
        );

    if (SUCCEEDED(hr))
    {
        // Register the CLSID for CoCreateInstance (not shown).
    }
    return hr;
}

// DllUnregisterServer: Removes the registry entries.
STDAPI DllUnregisterServer()
{
    HRESULT hr = MFTUnregister(CLSID_MyVideoEffectMFT);

    // Unregister the CLSID for CoCreateInstance (not shown).

    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einschränkungen des Verwendungsbereichs](field-of-use-restrictions.md)
</dt> <dt>

[Media Foundation Transformationen](media-foundation-transforms.md)
</dt> </dl>

 

 



