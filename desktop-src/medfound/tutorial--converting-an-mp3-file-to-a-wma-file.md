---
description: In diesem Tutorial wird gezeigt, wie Sie die transcode-API verwenden, um eine Windows Media Audio-Datei (WMA) zu codieren.
ms.assetid: 2397ca78-edb5-4756-bd07-00529db28f76
title: 'Tutorial: Codieren einer WMA-Datei'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f491a9d460771dae91a49ab42982fbe97b24c42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358813"
---
# <a name="tutorial-encoding-a-wma-file"></a><span data-ttu-id="3cebc-103">Tutorial: Codieren einer WMA-Datei</span><span class="sxs-lookup"><span data-stu-id="3cebc-103">Tutorial: Encoding a WMA File</span></span>

<span data-ttu-id="3cebc-104">In diesem Tutorial wird gezeigt, wie Sie die [transcode-API](transcode-api.md) verwenden, um eine Windows Media Audio-Datei (WMA) zu codieren.</span><span class="sxs-lookup"><span data-stu-id="3cebc-104">This tutorial shows how to use the [Transcode API](transcode-api.md) to encode a Windows Media Audio (WMA) file.</span></span>

<span data-ttu-id="3cebc-105">In diesem Tutorial wird der größte Teil des Codes aus dem Tutorial zum [Codieren einer MP4-Datei](tutorial--encoding-an-mp4-file-.md)wieder verwendet. Daher sollten Sie dieses Tutorial zuerst lesen.</span><span class="sxs-lookup"><span data-stu-id="3cebc-105">This tutorial reuses most of the code from the tutorial [Encoding an MP4 File](tutorial--encoding-an-mp4-file-.md), so you should read that tutorial first.</span></span> <span data-ttu-id="3cebc-106">Der einzige Code, der sich unterscheidet, ist die-Funktion `CreateTranscodeProfile` , die das transcodieren-Profil erstellt.</span><span class="sxs-lookup"><span data-stu-id="3cebc-106">The only code that differs is the function `CreateTranscodeProfile`, which creates the transcode profile.</span></span>

## <a name="create-the-transcode-profile"></a><span data-ttu-id="3cebc-107">Erstellen des transcode-Profils</span><span class="sxs-lookup"><span data-stu-id="3cebc-107">Create the Transcode Profile</span></span>

<span data-ttu-id="3cebc-108">Ein *transcodieren-Profil* beschreibt die Codierungs Parameter und den Datei Container.</span><span class="sxs-lookup"><span data-stu-id="3cebc-108">A *transcode profile* describes the encoding parameters and the file container.</span></span> <span data-ttu-id="3cebc-109">Bei WMA handelt es sich bei dem Datei Container um eine ASF-Datei (Advanced Streaming Format).</span><span class="sxs-lookup"><span data-stu-id="3cebc-109">For WMA, the file container is an Advanced Streaming Format (ASF) file.</span></span> <span data-ttu-id="3cebc-110">Die ASF-Datei enthält einen Audiostream, der mit dem [**Windows Media Audio Encoder**](windowsmediaaudioencoder.md)codiert wird.</span><span class="sxs-lookup"><span data-stu-id="3cebc-110">The ASF file contains an audio stream, which is encoded using the [**Windows Media Audio Encoder**](windowsmediaaudioencoder.md).</span></span>

<span data-ttu-id="3cebc-111">Um die transcodieren-Topologie zu erstellen, erstellen Sie das transcodieren-Profil, und geben Sie die Parameter für den Audiodatenstrom und den Container an.</span><span class="sxs-lookup"><span data-stu-id="3cebc-111">To build the transcode topology, create the transcode profile and specify the parameters for the audio stream and the container.</span></span> <span data-ttu-id="3cebc-112">Erstellen Sie dann die Topologie, indem Sie die Eingabe Quelle, die Ausgabe-URL und das transcodieren-Profil angeben.</span><span class="sxs-lookup"><span data-stu-id="3cebc-112">Then create the topology by specifying the input source, the output URL, and the transcode profile.</span></span>

<span data-ttu-id="3cebc-113">Führen Sie die folgenden Schritte aus, um das Profil zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3cebc-113">To create the profile, perform the following steps.</span></span>

1.  <span data-ttu-id="3cebc-114">Rufen Sie die Funktion [**mfkreatetranscodeprofile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) auf, um ein leeres transcodieren-Profil zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3cebc-114">Call the [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) function to create an empty transcode profile.</span></span>
2.  <span data-ttu-id="3cebc-115">Aufrufen von [**mftranscodegetaudiooutputavailabletypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) zum Abrufen einer Liste von audiomedientyp aus dem Encoder.</span><span class="sxs-lookup"><span data-stu-id="3cebc-115">Call [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) to get a list of audio media types from the encoder.</span></span> <span data-ttu-id="3cebc-116">Diese Funktion gibt einen [**IMF Collection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) -Zeiger zurück, der eine Auflistung von [**IMF MediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) -Zeigern darstellt.</span><span class="sxs-lookup"><span data-stu-id="3cebc-116">This function returns an [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) pointer that represents a collection of [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) pointers.</span></span>
3.  <span data-ttu-id="3cebc-117">Wählen Sie den audiomedientyp aus, der Ihren Transcodierungs Anforderungen entspricht, und kopieren Sie die Attribute in einen Attribut Speicher.</span><span class="sxs-lookup"><span data-stu-id="3cebc-117">Choose the audio media type that matches your transcoding requirements and copy the attributes to an attribute store.</span></span> <span data-ttu-id="3cebc-118">In diesem Tutorial wird der erste Medientyp in der Liste verwendet.</span><span class="sxs-lookup"><span data-stu-id="3cebc-118">For this tutorial, the first media type in the list is used.</span></span>
    -   <span data-ttu-id="3cebc-119">Wenn Sie [**imfcollection:: getElements**](/windows/desktop/api/mfobjects/nf-mfobjects-imfcollection-getelement) aufrufen, wählen Sie einen audiomedientyp aus der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="3cebc-119">Call [**IMFCollection::GetElement**](/windows/desktop/api/mfobjects/nf-mfobjects-imfcollection-getelement) to select an audio media type from the list.</span></span>
    -   <span data-ttu-id="3cebc-120">Fragen Sie den Medientyp ab, um einen Zeiger auf die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle des Attribut Speicher des Medientyps zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3cebc-120">Query the media type to get a pointer to the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface of the media type's attribute store.</span></span>
    -   <span data-ttu-id="3cebc-121">Aufrufen von [**imfattributes:: GetCount**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getcount) , um die Anzahl der Attribute zu erhalten, die im Medientyp enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="3cebc-121">Call [**IMFAttributes::GetCount**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getcount) to get the number of attributes contained in the media type.</span></span>
    -   <span data-ttu-id="3cebc-122">Rufen Sie [**mfkreateattributs**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) auf, um einen neuen Attribut Speicher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3cebc-122">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create a new attribute store.</span></span>
    -   <span data-ttu-id="3cebc-123">Nennen Sie [**imfattributes:: copyallitems**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-copyallitems) , um die Attribute aus dem Medientyp in den neuen Attribut Speicher zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="3cebc-123">Call [**IMFAttributes::CopyAllItems**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-copyallitems) to copy the attributes from the media type to the new attribute store.</span></span>
4.  <span data-ttu-id="3cebc-124">Wenn Sie [**imftranscodeprofile:: setaudioattribute**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes) aufrufen, legen Sie die Attribute für den Audiodatenstrom fest.</span><span class="sxs-lookup"><span data-stu-id="3cebc-124">Call [**IMFTranscodeProfile::SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes) to set the attributes for the audio stream.</span></span>
5.  <span data-ttu-id="3cebc-125">Rufen Sie [**mfkreateattributs**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) auf, um einen Attribut Speicher für die Attribute auf Container Ebene zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3cebc-125">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create an attribute store for the container-level attributes.</span></span>
6.  <span data-ttu-id="3cebc-126">Legen Sie das Attribut [MF \_ transcode \_ ContainerType](mf-transcode-containertype.md) auf **mftranscodecontainertype \_ ASF** fest, das einen ASF-Datei Container angibt.</span><span class="sxs-lookup"><span data-stu-id="3cebc-126">Set the [MF\_TRANSCODE\_CONTAINERTYPE](mf-transcode-containertype.md) attribute to **MFTranscodeContainerType\_ASF**, which specifies an ASF file container.</span></span>
7.  <span data-ttu-id="3cebc-127">Wenn Sie [**imftranscodeprofile:: setcontainerattribute**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes) aufrufen, legen Sie die Attribute auf Container Ebene für das Profil fest.</span><span class="sxs-lookup"><span data-stu-id="3cebc-127">Call [**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes) to set the container-level attributes on the profile.</span></span>


```C++
template <class Q>
HRESULT GetCollectionObject(IMFCollection *pCollection, DWORD index, Q **ppObj)
{
    IUnknown *pUnk;
    HRESULT hr = pCollection->GetElement(index, &pUnk);
    if (SUCCEEDED(hr))
    {
        hr = pUnk->QueryInterface(IID_PPV_ARGS(ppObj));
        pUnk->Release();
    }
    return hr;
}

HRESULT CreateTranscodeProfile(IMFTranscodeProfile **ppProfile)
{
    IMFTranscodeProfile *pProfile = NULL;     // Transcode profile.
    IMFCollection   *pAvailableTypes = NULL;  // List of audio media types.
    IMFMediaType    *pAudioType = NULL;       // Audio media type.
    IMFAttributes   *pAudioAttrs = NULL;      // Copy of the audio media type.
    IMFAttributes   *pContainer = NULL;       // Container attributes.

    DWORD dwMTCount = 0;
    
    // Create an empty transcode profile.
    HRESULT hr = MFCreateTranscodeProfile(&pProfile);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get output media types for the Windows Media audio encoder.

    // Enumerate all codecs except for codecs with field-of-use restrictions.
    // Sort the results.

    DWORD dwFlags = 
        (MFT_ENUM_FLAG_ALL & (~MFT_ENUM_FLAG_FIELDOFUSE)) | 
        MFT_ENUM_FLAG_SORTANDFILTER;

    hr = MFTranscodeGetAudioOutputAvailableTypes(MFAudioFormat_WMAudioV9, 
        dwFlags, NULL, &pAvailableTypes);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAvailableTypes->GetElementCount(&dwMTCount);
    if (FAILED(hr))
    {
        goto done;
    }
    if (dwMTCount == 0)
    {
        hr = E_FAIL;
        goto done;
    }

    // Get the first audio type in the collection and make a copy.
    hr = GetCollectionObject(pAvailableTypes, 0, &pAudioType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFCreateAttributes(&pAudioAttrs, 0);       
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAudioType->CopyAllItems(pAudioAttrs);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the audio attributes on the profile.
    hr = pProfile->SetAudioAttributes(pAudioAttrs);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the container attributes.
    hr = MFCreateAttributes(&pContainer, 1);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pContainer->SetGUID(MF_TRANSCODE_CONTAINERTYPE, MFTranscodeContainerType_ASF);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pProfile->SetContainerAttributes(pContainer);
    if (FAILED(hr))
    {
        goto done;
    }

    *ppProfile = pProfile;
    (*ppProfile)->AddRef();

done:
    SafeRelease(&pProfile);
    SafeRelease(&pAvailableTypes);
    SafeRelease(&pAudioType);
    SafeRelease(&pAudioAttrs);
    SafeRelease(&pContainer);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="3cebc-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3cebc-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3cebc-129">Transcode-API</span><span class="sxs-lookup"><span data-stu-id="3cebc-129">Transcode API</span></span>](transcode-api.md)
</dt> </dl>

 

 



