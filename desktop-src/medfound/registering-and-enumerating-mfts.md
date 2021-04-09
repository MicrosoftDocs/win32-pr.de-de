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
# <a name="registering-and-enumerating-mfts"></a><span data-ttu-id="0525e-103">Registrieren und Auflisten von MFTs</span><span class="sxs-lookup"><span data-stu-id="0525e-103">Registering and Enumerating MFTs</span></span>

<span data-ttu-id="0525e-104">In diesem Abschnitt wird beschrieben, wie Sie Media Foundation Transformationen aufzählen und wie Sie eine benutzerdefinierte MFT registrieren, damit Anwendungen Sie ermitteln können.</span><span class="sxs-lookup"><span data-stu-id="0525e-104">This section describes how to enumerate Media Foundation transforms, and how to register a custom MFT so that applications can discover it.</span></span>

-   [<span data-ttu-id="0525e-105">Auflisten von MFTs</span><span class="sxs-lookup"><span data-stu-id="0525e-105">Enumerating MFTs</span></span>](#registering-and-enumerating-mfts)
-   [<span data-ttu-id="0525e-106">Registrieren von MFTs</span><span class="sxs-lookup"><span data-stu-id="0525e-106">Registering MFTs</span></span>](#registering-mfts)
-   [<span data-ttu-id="0525e-107">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0525e-107">Related topics</span></span>](#related-topics)

## <a name="enumerating-mfts"></a><span data-ttu-id="0525e-108">Auflisten von MFTs</span><span class="sxs-lookup"><span data-stu-id="0525e-108">Enumerating MFTs</span></span>

<span data-ttu-id="0525e-109">Um auf dem System registrierte MFTs zu ermitteln, kann eine Anwendung die [**mftenumex**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) -Funktion abrufen.</span><span class="sxs-lookup"><span data-stu-id="0525e-109">To discover MFTs that are registered on the system, an application can call the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

> [!Note]  
> <span data-ttu-id="0525e-110">Diese Funktion erfordert Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0525e-110">This function requires to Windows 7.</span></span> <span data-ttu-id="0525e-111">Vor Windows 7 sollten Anwendungen stattdessen die [**mftenum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="0525e-111">Prior to Windows 7, applications should use the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) function instead.</span></span>

 

<span data-ttu-id="0525e-112">Diese Funktion übernimmt die folgenden Informationen als Eingabe:</span><span class="sxs-lookup"><span data-stu-id="0525e-112">This function takes the following information as input:</span></span>

-   <span data-ttu-id="0525e-113">Die Kategorie der aufzuzählenden MFT, z. b. Video Decoder oder Audiodecoder.</span><span class="sxs-lookup"><span data-stu-id="0525e-113">The category of MFT to enumerate, such as video decoder or audio decoder.</span></span>
-   <span data-ttu-id="0525e-114">Ein Eingabe-oder Ausgabeformat, das gefunden werden soll.</span><span class="sxs-lookup"><span data-stu-id="0525e-114">An input or output format to match.</span></span>
-   <span data-ttu-id="0525e-115">Flags, die zusätzliche Suchbedingungen angeben.</span><span class="sxs-lookup"><span data-stu-id="0525e-115">Flags that specify additional search conditions.</span></span>

<span data-ttu-id="0525e-116">Die-Funktion gibt ein Array von [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeigern zurück, von denen jedes eine MFT darstellt, die den enumerationskriterien entspricht.</span><span class="sxs-lookup"><span data-stu-id="0525e-116">The function returns an array of [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers, each of which represents an MFT that matches the enumeration criteria.</span></span>

<span data-ttu-id="0525e-117">Der folgende Code listet z. b. Windows Media Video Decoders auf:</span><span class="sxs-lookup"><span data-stu-id="0525e-117">For example, the following code enumerates Windows Media Video decoders:</span></span>


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



<span data-ttu-id="0525e-118">Standardmäßig sind einige MFT-Typen aus der-Enumeration ausgeschlossen, einschließlich asynchroner MFTs, Hardware-MFTs und MFTs mit den Optionen für die Verwendung von Feldern.</span><span class="sxs-lookup"><span data-stu-id="0525e-118">By default, some types of MFT are excluded from the enumeration, including asynchronous MFTs, hardware MFTs, and MFTs with field-of-use restructions.</span></span> <span data-ttu-id="0525e-119">Diese werden ausgeschlossen, da Sie alle eine besondere Behandlung erfordern.</span><span class="sxs-lookup"><span data-stu-id="0525e-119">These are excluded because they all require special handling of some kind.</span></span> <span data-ttu-id="0525e-120">Verwenden Sie den *Flags* -Parameter von [**mftenumex**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) , um den Standardwert zu ändern.</span><span class="sxs-lookup"><span data-stu-id="0525e-120">Use the *Flags* parameter of [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) to change the default.</span></span> <span data-ttu-id="0525e-121">Um z. b. Hardware-MFTs in die enumerationsergebnisse einzubeziehen, legen Sie das hardwareflag für die **MFT \_ \_ \_** -Enumeration fest:</span><span class="sxs-lookup"><span data-stu-id="0525e-121">For example, to include hardware MFTs in the enumeration results, set the **MFT\_ENUM\_FLAG\_HARDWARE** flag:</span></span>


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



## <a name="registering-mfts"></a><span data-ttu-id="0525e-122">Registrieren von MFTs</span><span class="sxs-lookup"><span data-stu-id="0525e-122">Registering MFTs</span></span>

<span data-ttu-id="0525e-123">Beim Registrieren einer Media Foundation Transformation (MFT) werden zwei Arten von Informationen in die Registrierung geschrieben:</span><span class="sxs-lookup"><span data-stu-id="0525e-123">When you register a Media Foundation transform (MFT), two types of information are written to the registry:</span></span>

-   <span data-ttu-id="0525e-124">Die CLSID des MFT, sodass Clients **cokreateinstance** oder **CoGetClassObject** aufrufen können, um eine Instanz des MFT-Objekts zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0525e-124">The CLSID of the MFT, so that clients can call **CoCreateInstance** or **CoGetClassObject** to create an instance of the MFT.</span></span> <span data-ttu-id="0525e-125">Dieser Registrierungs Eintrag folgt dem Standardformat für com-Klassenfactorys.</span><span class="sxs-lookup"><span data-stu-id="0525e-125">This registry entry follows the standard format for COM class factories.</span></span> <span data-ttu-id="0525e-126">Weitere Informationen finden Sie in der Windows SDK-Dokumentation für die Component Object Model (com).</span><span class="sxs-lookup"><span data-stu-id="0525e-126">For more information, see the Windows SDK documentation for the Component Object Model (COM).</span></span>
-   <span data-ttu-id="0525e-127">Informationen, mit denen eine Anwendung MFTs nach funktionaler Kategorie aufzählen kann.</span><span class="sxs-lookup"><span data-stu-id="0525e-127">Information that enables an application to enumerate MFTs by functional category.</span></span>

<span data-ttu-id="0525e-128">Rufen Sie die [**mftregisterfunktion**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) auf, um die MFT-Enumerationseinträge in der Registrierung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0525e-128">To create the MFT enumeration entries in the registry, call the [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) function.</span></span> <span data-ttu-id="0525e-129">Sie können die folgenden Informationen über die MFT einschließen:</span><span class="sxs-lookup"><span data-stu-id="0525e-129">You can include the following information about the MFT:</span></span>

-   <span data-ttu-id="0525e-130">Die Kategorie des MFT, z. b. Video Decoder oder Video Encoder.</span><span class="sxs-lookup"><span data-stu-id="0525e-130">The category of the MFT, such as video decoder or video encoder.</span></span> <span data-ttu-id="0525e-131">Eine Liste der Kategorien finden Sie unter [**MFT \_ Category**](mft-category.md).</span><span class="sxs-lookup"><span data-stu-id="0525e-131">For a list of categories, see [**MFT\_CATEGORY**](mft-category.md).</span></span>
-   <span data-ttu-id="0525e-132">Eine Liste der vom MFT unterstützten Eingabe-und Ausgabeformate.</span><span class="sxs-lookup"><span data-stu-id="0525e-132">A list of input and output formats that the MFT supports.</span></span> <span data-ttu-id="0525e-133">Jedes Format wird durch einen Haupttyp und einen Untertyp definiert.</span><span class="sxs-lookup"><span data-stu-id="0525e-133">Each format is defined by a major type and a subtype.</span></span> <span data-ttu-id="0525e-134">(Um ausführlichere Formatierungsinformationen zu erhalten, muss der Client die MFT erstellen und [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Methoden aufzurufen.) Der topologielader verwendet diese Informationen, wenn er eine partielle Topologie auflöst.</span><span class="sxs-lookup"><span data-stu-id="0525e-134">(To get more detailed format information, the client must create the MFT and call [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) methods.) The topology loader uses this information when it resolves a partial topology.</span></span>

<span data-ttu-id="0525e-135">Um die Einträge aus der Registrierung zu entfernen, nennen Sie [**mftunregister**](/windows/desktop/api/mfapi/nf-mfapi-mftunregister).</span><span class="sxs-lookup"><span data-stu-id="0525e-135">To remove the entries from the registry, call [**MFTUnregister**](/windows/desktop/api/mfapi/nf-mfapi-mftunregister).</span></span>

<span data-ttu-id="0525e-136">Der folgende Code zeigt, wie ein MFT registriert wird.</span><span class="sxs-lookup"><span data-stu-id="0525e-136">The following code shows how to register an MFT.</span></span> <span data-ttu-id="0525e-137">In diesem Beispiel wird davon ausgegangen, dass es sich bei der MFT um einen Videoeffekt handelt, der für die Eingabe und die Ausgabe die gleichen Formate</span><span class="sxs-lookup"><span data-stu-id="0525e-137">This example assumes that the MFT is a video effect that supports the same formats for both input and output.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="0525e-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0525e-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0525e-139">Einschränkungen bei der Verwendung des Felds</span><span class="sxs-lookup"><span data-stu-id="0525e-139">Field of Use Restrictions</span></span>](field-of-use-restrictions.md)
</dt> <dt>

[<span data-ttu-id="0525e-140">Media Foundation Transformationen</span><span class="sxs-lookup"><span data-stu-id="0525e-140">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> </dl>

 

 



