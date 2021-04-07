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
# <a name="to-enumerate-input-formats"></a><span data-ttu-id="cb7e5-111">So zählen Sie Eingabeformate auf</span><span class="sxs-lookup"><span data-stu-id="cb7e5-111">To Enumerate Input Formats</span></span>

<span data-ttu-id="cb7e5-112">Alle Windows Media-Codecs akzeptieren mindestens einen Eingabe Datentyp für die Komprimierung.</span><span class="sxs-lookup"><span data-stu-id="cb7e5-112">Each of the Windows Media codecs accepts one or more types of input media for compression.</span></span> <span data-ttu-id="cb7e5-113">Mit dem Windows Media-Format-SDK können Sie eine größere Vielfalt von Formaten als die von den Codecs unterstützten Formate eingeben.</span><span class="sxs-lookup"><span data-stu-id="cb7e5-113">The Windows Media Format SDK enables you to input a wider variety of formats than those supported by the codecs.</span></span> <span data-ttu-id="cb7e5-114">Das SDK führt dies durch, indem bei Bedarf Vorverarbeitungs Transformationen für die Eingaben durchgeführt werden, z. b. das Ändern der Größe von Video Frames oder das erneute Sampling von Audio</span><span class="sxs-lookup"><span data-stu-id="cb7e5-114">The SDK does this by performing pre-processing transformations on the inputs when necessary, such as resizing video frames or resampling audio.</span></span> <span data-ttu-id="cb7e5-115">In jedem Fall müssen Sie sicherstellen, dass die Eingabeformate für die Dateien, die Sie schreiben, den Daten entsprechen, die Sie an den Writer senden.</span><span class="sxs-lookup"><span data-stu-id="cb7e5-115">In any case, you must ensure that the input formats for the files you write match the data you send to the writer.</span></span> <span data-ttu-id="cb7e5-116">Jeder Codec verfügt über ein Standardformat für Eingabemedien, das beim Laden des Profils im Writer festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="cb7e5-116">Each codec has a default input media format that is set in the writer when the profile is loaded.</span></span> <span data-ttu-id="cb7e5-117">Sie können das Standardeingabe Format überprüfen, indem Sie [**iwmwriter:: GetInput-**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops)Eigenschaften aufrufen.</span><span class="sxs-lookup"><span data-stu-id="cb7e5-117">You can examine the default input format by calling [**IWMWriter::GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).</span></span>

<span data-ttu-id="cb7e5-118">Die Video Codecs unterstützen die folgenden Formate: IYUV, I420, YV12, im YUY2, UYVY, yvyu, YVU9, RGB 32, RGB 24, RGB 565, RGB 555 und RGB 8.</span><span class="sxs-lookup"><span data-stu-id="cb7e5-118">The video codecs support the following formats: IYUV, I420, YV12, YUY2, UYVY, YVYU, YVU9, RGB 32, RGB 24, RGB 565, RGB 555, and RGB 8.</span></span> <span data-ttu-id="cb7e5-119">Die Audiocodecs unterstützen PCM-Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="cb7e5-119">The audio codecs support PCM audio.</span></span>

<span data-ttu-id="cb7e5-120">Führen Sie die folgenden Schritte aus, um die von einem Codec unterstützten Eingabeformate aufzulisten:</span><span class="sxs-lookup"><span data-stu-id="cb7e5-120">To enumerate the input formats supported by a codec, perform the following steps:</span></span>

1.  <span data-ttu-id="cb7e5-121">Erstellen Sie ein Writer-Objekt, und legen Sie ein Profil zur Verwendung fest.</span><span class="sxs-lookup"><span data-stu-id="cb7e5-121">Create a writer object and set a profile to use.</span></span> <span data-ttu-id="cb7e5-122">Weitere Informationen zum Festlegen von Profilen im Writer finden [Sie unter So verwenden Sie Profile mit dem Writer](to-use-profiles-with-the-writer.md).</span><span class="sxs-lookup"><span data-stu-id="cb7e5-122">For more information about setting profiles in the writer, see [To Use Profiles with the Writer](to-use-profiles-with-the-writer.md).</span></span>
2.  <span data-ttu-id="cb7e5-123">Identifizieren Sie die Eingabe Nummer, für die Sie die Formate überprüfen möchten.</span><span class="sxs-lookup"><span data-stu-id="cb7e5-123">Identify the input number for which you want to check the formats.</span></span> <span data-ttu-id="cb7e5-124">Weitere Informationen zum Identifizieren von Eingabe Nummern finden [Sie unter So identifizieren Sie Eingaben nach Nummer](to-identify-inputs-by-number.md).</span><span class="sxs-lookup"><span data-stu-id="cb7e5-124">For more information about identifying input numbers, see [To Identify Inputs By Number](to-identify-inputs-by-number.md).</span></span>
3.  <span data-ttu-id="cb7e5-125">Rufen Sie die Gesamtanzahl von Eingabe Formaten ab, die von der gewünschten Eingabe unterstützt werden, indem Sie [**iwmwriter:: getinputformatcount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="cb7e5-125">Retrieve the total number of input formats supported by the desired input by calling [**IWMWriter::GetInputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount).</span></span>
4.  <span data-ttu-id="cb7e5-126">Durchlaufen Sie alle unterstützten Eingabeformate, und führen Sie jeweils die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="cb7e5-126">Loop through all of the supported input formats, performing the following steps for each.</span></span>
    -   <span data-ttu-id="cb7e5-127">Rufen Sie die [**iwminputmediarequicenschnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) für das Eingabeformat durch Aufrufen von [**iwmwriter:: getinputformat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat)ab.</span><span class="sxs-lookup"><span data-stu-id="cb7e5-127">Retrieve the [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) interface for the input format by calling [**IWMWriter::GetInputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat).</span></span>
    -   <span data-ttu-id="cb7e5-128">Rufen Sie die [**WM- \_ \_ Medientyp**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) Struktur für das Eingabeformat ab.</span><span class="sxs-lookup"><span data-stu-id="cb7e5-128">Retrieve the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure for the input format.</span></span> <span data-ttu-id="cb7e5-129">Nennen Sie [**iwmmedia-Eigenschaften:: getmediatype**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype), und übergeben Sie **null** für den *pType* -Parameter, um die Größe der Struktur abzurufen.</span><span class="sxs-lookup"><span data-stu-id="cb7e5-129">Call [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype), passing **NULL** for the *pType* parameter to get the size of the structure.</span></span> <span data-ttu-id="cb7e5-130">Weisen Sie dann den Speicher zu, um die Struktur aufzunehmen, und wiederholen Sie dann **getmediatype** , um die Struktur abzurufen.</span><span class="sxs-lookup"><span data-stu-id="cb7e5-130">Then allocate memory to hold the structure and call **GetMediaType** again to get the structure.</span></span> <span data-ttu-id="cb7e5-131">[**Iwminputmedia-**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) Eigenschaften erbt von [**iwmmedia-**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)Eigenschaften, sodass Sie die Aufrufe von **getmediatype** aus der im vorherigen Schritt abgerufenen Instanz von **iwminputmedia-** Eigenschaften durchführen können.</span><span class="sxs-lookup"><span data-stu-id="cb7e5-131">[**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) inherits from [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops), so you can make the calls to **GetMediaType** from the instance of **IWMInputMediaProps** retrieved in the previous step.</span></span>
    -   <span data-ttu-id="cb7e5-132">Das in der WM- [**\_ \_ Medientyp**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) Struktur beschriebene Format enthält alle relevanten Informationen zum Eingabeformat.</span><span class="sxs-lookup"><span data-stu-id="cb7e5-132">The format described in the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure contains all of the pertinent information about the input format.</span></span> <span data-ttu-id="cb7e5-133">Das Grundformat des Mediums wird durch den **WM- \_ \_ Medientyp. Untertyp** identifiziert.</span><span class="sxs-lookup"><span data-stu-id="cb7e5-133">The basic format of the media is identified by **WM\_MEDIA\_TYPE.subtype**.</span></span> <span data-ttu-id="cb7e5-134">Für Videostreams verweist das **pbformat** -Element auf eine dynamisch zugeordnete [**wmvideoinfoheader**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) -Struktur, die weitere Details zum Stream einschließlich der Rechteck Größe enthält.</span><span class="sxs-lookup"><span data-stu-id="cb7e5-134">For video streams, the **pbFormat** member points to a dynamically allocated [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) structure which contains further details about the stream, including rectangle size.</span></span> <span data-ttu-id="cb7e5-135">Die Größe der Eingabe Rahmen ist nicht erforderlich, um genau eine Größe abzugleichen, die vom Codec unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="cb7e5-135">The size of the input frames is not required to match exactly a size supported by the codec.</span></span> <span data-ttu-id="cb7e5-136">Wenn keine Entsprechung gefunden wird, ändern die SDK-Laufzeitkomponenten in vielen Fällen automatisch die Größe der Eingabe Video Frames an den Codec, den der Codec annehmen kann.</span><span class="sxs-lookup"><span data-stu-id="cb7e5-136">If they do not match, the SDK run-time components, in many cases, will automatically resize the input video frames to something the codec can accept.</span></span>

<span data-ttu-id="cb7e5-137">Der folgende Beispielcode sucht das Eingabeformat des unter Typs, der als Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="cb7e5-137">The following example code finds the input format of the subtype passed as a parameter.</span></span> <span data-ttu-id="cb7e5-138">Weitere Informationen zur Verwendung dieses Codes finden Sie unter [Verwenden der Codebeispiele](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="cb7e5-138">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="cb7e5-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cb7e5-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb7e5-140">**Iwmwriter-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="cb7e5-140">**IWMWriter Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[<span data-ttu-id="cb7e5-141">**Schreiben von ASF-Dateien**</span><span class="sxs-lookup"><span data-stu-id="cb7e5-141">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




