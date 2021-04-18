---
description: In diesem Thema wird beschrieben, wie Sie in Microsoft Media Foundation als ASF-Profil erstellen.
ms.assetid: 9633bc88-12bd-404a-b779-878eb1ee5699
title: Erstellen eines ASF-Profils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08ed9553811645b8589de7fb1805f1a307c4bdef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344018"
---
# <a name="creating-an-asf-profile"></a><span data-ttu-id="34555-103">Erstellen eines ASF-Profils</span><span class="sxs-lookup"><span data-stu-id="34555-103">Creating an ASF Profile</span></span>

<span data-ttu-id="34555-104">In diesem Thema wird beschrieben, wie Sie in Microsoft Media Foundation als ASF-Profil erstellen.</span><span class="sxs-lookup"><span data-stu-id="34555-104">This topic describes how to create as ASF profile in Microsoft Media Foundation.</span></span>

-   [<span data-ttu-id="34555-105">Erstellen eines neuen Profils</span><span class="sxs-lookup"><span data-stu-id="34555-105">Create a New Profile</span></span>](#create-a-new-profile)
-   [<span data-ttu-id="34555-106">Profil aus dem Objekt "ASF ContentInfo" erhalten</span><span class="sxs-lookup"><span data-stu-id="34555-106">Get the Profile from the ASF ContentInfo Object</span></span>](#get-the-profile-from-the-asf-contentinfo-object)
-   [<span data-ttu-id="34555-107">Profil aus einem Präsentations Deskriptor abgerufen</span><span class="sxs-lookup"><span data-stu-id="34555-107">Get the Profile from a Presentation Descriptor</span></span>](#get-the-profile-from-a-presentation-descriptor)
-   [<span data-ttu-id="34555-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="34555-108">Related topics</span></span>](#related-topics)

## <a name="create-a-new-profile"></a><span data-ttu-id="34555-109">Erstellen eines neuen Profils</span><span class="sxs-lookup"><span data-stu-id="34555-109">Create a New Profile</span></span>

<span data-ttu-id="34555-110">Um ein leeres ASF-Profil zu erstellen, rufen Sie die Funktion [**mfkreateasfprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) auf.</span><span class="sxs-lookup"><span data-stu-id="34555-110">To create an empty ASF profile, call the [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) function.</span></span> <span data-ttu-id="34555-111">Diese Funktion gibt einen Zeiger auf die [**imfasfprofile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) -Schnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="34555-111">This function returns a pointer to the [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) interface.</span></span> <span data-ttu-id="34555-112">Die Anwendung kann diese Schnittstelle verwenden, um Datenströme zum Profil hinzuzufügen und die einzelnen Streams zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="34555-112">The application can use this interface to add streams to the profile, and to configure each of the streams.</span></span> <span data-ttu-id="34555-113">Weitere Informationen finden Sie unter [Erstellen und Konfigurieren von ASF-Streams](creating-and-configuring-asf-streams.md).</span><span class="sxs-lookup"><span data-stu-id="34555-113">For more information, see [Creating and Configuring ASF Streams](creating-and-configuring-asf-streams.md).</span></span>

<span data-ttu-id="34555-114">Optional kann die Anwendung zwei oder mehr Streams Objekte mit gegenseitigem Ausschluss hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="34555-114">Optionally, the application can add mutual-exclusion objects to two or more streams.</span></span> <span data-ttu-id="34555-115">Siehe [Verwenden des gegenseitigen Ausschlusses für ASF-Streams](using-mutual-exclusion-for-asf-streams.md).</span><span class="sxs-lookup"><span data-stu-id="34555-115">See [Using Mutual Exclusion for ASF Streams](using-mutual-exclusion-for-asf-streams.md).</span></span>

## <a name="get-the-profile-from-the-asf-contentinfo-object"></a><span data-ttu-id="34555-116">Profil aus dem Objekt "ASF ContentInfo" erhalten</span><span class="sxs-lookup"><span data-stu-id="34555-116">Get the Profile from the ASF ContentInfo Object</span></span>

<span data-ttu-id="34555-117">Eine Anwendung kann das ASF-Profil einer vorhandenen ASF-Datei aus dem [Objekt "ASF ContentInfo](asf-contentinfo-object.md)" erhalten.</span><span class="sxs-lookup"><span data-stu-id="34555-117">An application can get the ASF profile of an existing ASF file from the [ASF ContentInfo Object](asf-contentinfo-object.md).</span></span> <span data-ttu-id="34555-118">Das Profil ist bereits konfiguriert und enthält Einstellungen für alle Streams in der Datei.</span><span class="sxs-lookup"><span data-stu-id="34555-118">The profile is already configured and contains settings for the all of the streams in the file.</span></span>

<span data-ttu-id="34555-119">Initialisieren Sie das ContentInfo-Objekt, indem Sie das ASF-Header Objekt der Datei übernehmen.</span><span class="sxs-lookup"><span data-stu-id="34555-119">Initialize the ContentInfo object by parsing the ASF Header Object of the file.</span></span> <span data-ttu-id="34555-120">Dies erfolgt über die [**imfasf ContentInfo::P arsheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) -Methode.</span><span class="sxs-lookup"><span data-stu-id="34555-120">This is done through the [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) method.</span></span> <span data-ttu-id="34555-121">Nachdem alle Header Objekte gelesen und die ASF-Bibliothek aufgefüllt wurde, wird das Profil für diese Datei generiert.</span><span class="sxs-lookup"><span data-stu-id="34555-121">After all the Header Objects are read and the ASF library is populated, the profile for this file is generated.</span></span> <span data-ttu-id="34555-122">Die Anwendung kann einen Zeiger auf dieses initialisierte Profil abrufen, indem [**imfasfcontentinfo:: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="34555-122">The application can get a pointer to this initialized profile by calling [**IMFASFContentInfo::GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span></span>

## <a name="get-the-profile-from-a-presentation-descriptor"></a><span data-ttu-id="34555-123">Profil aus einem Präsentations Deskriptor abgerufen</span><span class="sxs-lookup"><span data-stu-id="34555-123">Get the Profile from a Presentation Descriptor</span></span>

<span data-ttu-id="34555-124">Sie können das Profil Objekt einer vorhandenen ASF-Datei aus dem [Präsentations Deskriptor](presentation-descriptors.md) für die Datei oder aus dem Objekt " [ASF ContentInfo](asf-contentinfo-object.md) " erhalten.</span><span class="sxs-lookup"><span data-stu-id="34555-124">You can get the profile object of an existing ASF file from the [presentation descriptor](presentation-descriptors.md) for the file, or from the [ASF ContentInfo](asf-contentinfo-object.md) object.</span></span> <span data-ttu-id="34555-125">In diesem Fall ist das Profil bereits konfiguriert und enthält Einstellungen für alle Streams in der Datei.</span><span class="sxs-lookup"><span data-stu-id="34555-125">In this case, the profile is already configured and contains settings for all of the streams in the file.</span></span> <span data-ttu-id="34555-126">Dies kann hilfreich sein, wenn Sie ein vorhandenes ASF-Profil ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="34555-126">This can be useful if you want to modify an existing ASF profile.</span></span> <span data-ttu-id="34555-127">Beispielsweise möchten Sie möglicherweise eine Windows Media Video Datei mit einer niedrigeren Bitrate erneut codieren.</span><span class="sxs-lookup"><span data-stu-id="34555-127">For example, you might wish to re-encode a Windows Media Video file at a lower bit rate.</span></span>

<span data-ttu-id="34555-128">Um das Profil aus dem Präsentations Deskriptor abzurufen, müssen Sie [**mfkreateasfprofilefrompresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="34555-128">To get the profile from the presentation descriptor, call [**MFCreateASFProfileFromPresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor).</span></span> <span data-ttu-id="34555-129">Diese Funktion analysiert den Präsentations Deskriptor und füllt ein ASF-Profil mit Informationen über die Mediendatei.</span><span class="sxs-lookup"><span data-stu-id="34555-129">This function parses the presentation descriptor, and populates an ASF profile with information about the media file.</span></span> <span data-ttu-id="34555-130">Die-Funktion gibt einen Zeiger auf die imfasfprofile-Schnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="34555-130">The function returns a pointer to the IMFASFProfile interface.</span></span> <span data-ttu-id="34555-131">Anschließend können Sie diese Schnittstelle verwenden, um das Profil zu ändern.</span><span class="sxs-lookup"><span data-stu-id="34555-131">You can then use this interface to modify the profile.</span></span>

<span data-ttu-id="34555-132">Um den Präsentations Deskriptor abzurufen, wenden Sie eine der folgenden Methoden an:</span><span class="sxs-lookup"><span data-stu-id="34555-132">To get the presentation descriptor, call one of the following methods:</span></span>

-   <span data-ttu-id="34555-133">Nennen Sie aus der ASF-Medienquelle [**imfmediasource:: foratepresentationdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="34555-133">From the ASF media source, call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span>
-   <span data-ttu-id="34555-134">Nennen Sie aus dem Objekt " [ASF ContentInfo](asf-contentinfo-object.md) " [**imfasfcontentinfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="34555-134">From the [ASF ContentInfo](asf-contentinfo-object.md) object, call [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor).</span></span> <span data-ttu-id="34555-135">Stellen Sie vor dem Aufrufen dieser Methode sicher, dass das ContentInfo-Objekt zum Lesen initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="34555-135">Prior to calling this method, make sure that the ContentInfo object is initialized for reading.</span></span> <span data-ttu-id="34555-136">Weitere Informationen finden Sie unter "Initialisieren des ContentInfo-Objekts aus einer vorhandenen ASF-Datei" beim [Lesen des ASF-Header Objekts einer vorhandenen Datei](reading-the-asf-header-object-of-an-existing-file.md).</span><span class="sxs-lookup"><span data-stu-id="34555-136">For more information, see "Initializing the ContentInfo Object from an Existing ASF File" in [Reading the ASF Header Object of an Existing File](reading-the-asf-header-object-of-an-existing-file.md).</span></span> <span data-ttu-id="34555-137">Wenn Sie jedoch bereits über ein initialisiertes ContentInfo-Objekt verfügen, können Sie das Profil direkt aus dem Objekt erhalten.</span><span class="sxs-lookup"><span data-stu-id="34555-137">However, if you already have an initialized ContentInfo object, you can get the profile directly from it.</span></span> <span data-ttu-id="34555-138">Dies wird weiter unten in diesem Thema unter "erhalten des Profils aus dem ContentInfo-Objekt" beschrieben.</span><span class="sxs-lookup"><span data-stu-id="34555-138">This is described in "Getting the Profile from the ContentInfo Object " later in this topic.</span></span>

<span data-ttu-id="34555-139">Im folgenden Beispiel wird gezeigt, wie ein Profil aus einem Präsentations Deskriptor erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="34555-139">The following example shows how to create a profile from a presentation descriptor.</span></span> <span data-ttu-id="34555-140">Die-Funktion erstellt eine Medienquelle für die Datei, Ruft den Präsentations Deskriptor aus der Medienquelle ab und erstellt ein Profil.</span><span class="sxs-lookup"><span data-stu-id="34555-140">The function creates a media source for the file, gets the presentation descriptor from the media source, and creates a profile.</span></span> <span data-ttu-id="34555-141">In diesem Beispiel wird davon ausgegangen, dass *pszFileName* die URL einer ASF-Datei angibt.</span><span class="sxs-lookup"><span data-stu-id="34555-141">This example assumes that *pszFileName* specifies the URL of an ASF file.</span></span>


```C++
HRESULT GetASFProfile(PCWSTR pszFileName, IMFASFProfile** ppProfile)
{
    *ppProfile = NULL;

    IMFSourceResolver* pResolver = NULL;
    IUnknown* pSourceUnk = NULL;
    IMFMediaSource* pSource = NULL;
    IMFPresentationDescriptor* pPD = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pResolver);

    // Use the source resolver to create the media source.
    if (SUCCEEDED(hr))
    {
        MF_OBJECT_TYPE ObjectType;

        hr = pResolver->CreateObjectFromURL(
                pszFileName,
                MF_RESOLUTION_MEDIASOURCE, 
                NULL,                      
                &ObjectType,               
                &pSourceUnk   
            );
    }

    // Get the IMFMediaSource interface from the media source.
    if (SUCCEEDED(hr))
    {
        hr = pSourceUnk->QueryInterface(IID_PPV_ARGS(&pSource));
    }

    // Get the presentation desccriptor.
    if (SUCCEEDED(hr))
    {
        hr = pSource->CreatePresentationDescriptor(&pPD);
    }

    // Get the profile from the presentation descriptor.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateASFProfileFromPresentationDescriptor(pPD, ppProfile);
    }

    SafeRelease(&pResolver);
    SafeRelease(&pSourceUnk);
    SafeRelease(&pSource);
    SafeRelease(&pPD);
    return hr;
}
```



<span data-ttu-id="34555-142">In diesem Beispiel wird [saferelease](saferelease.md) verwendet, um Schnittstellen Zeiger freizugeben.</span><span class="sxs-lookup"><span data-stu-id="34555-142">This example uses [SafeRelease](saferelease.md) to release interface pointers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="34555-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="34555-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34555-144">ASF-Profil</span><span class="sxs-lookup"><span data-stu-id="34555-144">ASF Profile</span></span>](asf-profile.md)
</dt> </dl>

 

 



