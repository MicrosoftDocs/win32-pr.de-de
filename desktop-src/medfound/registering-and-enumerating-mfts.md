---
description: In diesem Abschnitt wird beschrieben, wie Sie Media Foundation Transformationen aufzählen und wie Sie eine benutzerdefinierte MFT registrieren, damit Anwendungen Sie ermitteln können.
ms.assetid: 76d2a703-4162-428e-a4ff-643e346eacfb
title: Registrieren und Auflisten von MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 771a22b469d472dbc59d07c2754405276883bef4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959229"
---
# <a name="registering-and-enumerating-mfts"></a>Registrieren und Auflisten von MFTs

In diesem Abschnitt wird beschrieben, wie Sie Media Foundation Transformationen aufzählen und wie Sie eine benutzerdefinierte MFT registrieren, damit Anwendungen Sie ermitteln können.

-   [Auflisten von MFTs](#registering-and-enumerating-mfts)
-   [Registrieren von MFTs](#registering-mfts)
-   [Zugehörige Themen](#related-topics)

## <a name="enumerating-mfts"></a>Auflisten von MFTs

Um auf dem System registrierte MFTs zu ermitteln, kann eine Anwendung die [**mftenumex**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) -Funktion abrufen.

> [!Note]  
> Diese Funktion erfordert Windows 7. Vor Windows 7 sollten Anwendungen stattdessen die [**mftenum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) -Funktion verwenden.

 

Diese Funktion übernimmt die folgenden Informationen als Eingabe:

-   Die Kategorie der aufzuzählenden MFT, z. b. Video Decoder oder Audiodecoder.
-   Ein Eingabe-oder Ausgabeformat, das gefunden werden soll.
-   Flags, die zusätzliche Suchbedingungen angeben.

Die-Funktion gibt ein Array von [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeigern zurück, von denen jedes eine MFT darstellt, die den enumerationskriterien entspricht.

Der folgende Code listet z. b. Windows Media Video Decoders auf:


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



Standardmäßig sind einige MFT-Typen aus der-Enumeration ausgeschlossen, einschließlich asynchroner MFTs, Hardware-MFTs und MFTs mit den Optionen für die Verwendung von Feldern. Diese werden ausgeschlossen, da Sie alle eine besondere Behandlung erfordern. Verwenden Sie den *Flags* -Parameter von [**mftenumex**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) , um den Standardwert zu ändern. Um z. b. Hardware-MFTs in die enumerationsergebnisse einzubeziehen, legen Sie das hardwareflag für die **MFT \_ \_ \_** -Enumeration fest:


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

Beim Registrieren einer Media Foundation Transformation (MFT) werden zwei Arten von Informationen in die Registrierung geschrieben:

-   Die CLSID des MFT, sodass Clients **cokreateinstance** oder **CoGetClassObject** aufrufen können, um eine Instanz des MFT-Objekts zu erstellen. Dieser Registrierungs Eintrag folgt dem Standardformat für com-Klassenfactorys. Weitere Informationen finden Sie in der Windows SDK-Dokumentation für die Component Object Model (com).
-   Informationen, mit denen eine Anwendung MFTs nach funktionaler Kategorie aufzählen kann.

Rufen Sie die [**mftregisterfunktion**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) auf, um die MFT-Enumerationseinträge in der Registrierung zu erstellen. Sie können die folgenden Informationen über die MFT einschließen:

-   Die Kategorie des MFT, z. b. Video Decoder oder Video Encoder. Eine Liste der Kategorien finden Sie unter [**MFT \_ Category**](mft-category.md).
-   Eine Liste der vom MFT unterstützten Eingabe-und Ausgabeformate. Jedes Format wird durch einen Haupttyp und einen Untertyp definiert. (Um ausführlichere Formatierungsinformationen zu erhalten, muss der Client die MFT erstellen und [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Methoden aufzurufen.) Der topologielader verwendet diese Informationen, wenn er eine partielle Topologie auflöst.

Um die Einträge aus der Registrierung zu entfernen, nennen Sie [**mftunregister**](/windows/desktop/api/mfapi/nf-mfapi-mftunregister).

Der folgende Code zeigt, wie ein MFT registriert wird. In diesem Beispiel wird davon ausgegangen, dass es sich bei der MFT um einen Videoeffekt handelt, der für die Eingabe und die Ausgabe die gleichen Formate


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

[Einschränkungen bei der Verwendung des Felds](field-of-use-restrictions.md)
</dt> <dt>

[Media Foundation Transformationen](media-foundation-transforms.md)
</dt> </dl>

 

 



