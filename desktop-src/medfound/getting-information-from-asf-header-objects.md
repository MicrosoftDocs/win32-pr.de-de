---
description: Die Informationen zum ASF-Header werden in den ASF-Header Objekten einer Mediendatei gespeichert.
ms.assetid: 1654af97-f4fe-427f-b562-3b109e921719
title: Informationen aus den ASF-Header Objekten werden erhalten.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f25155929c9e3ba7e59ee1b5f46ea7c5930c3e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344632"
---
# <a name="getting-information-from-asf-header-objects"></a><span data-ttu-id="f88ea-103">Informationen aus den ASF-Header Objekten werden erhalten.</span><span class="sxs-lookup"><span data-stu-id="f88ea-103">Getting Information from ASF Header Objects</span></span>

<span data-ttu-id="f88ea-104">Die Informationen zum ASF-Header werden in den ASF-Header Objekten einer Mediendatei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f88ea-104">ASF header information is stored in the ASF Header Objects of a media file.</span></span> <span data-ttu-id="f88ea-105">Media Foundation stellt das [Objekt "ASF ContentInfo](asf-contentinfo-object.md) " bereit, um mit dem Header Objekt zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="f88ea-105">Media Foundation provides the [ASF ContentInfo Object](asf-contentinfo-object.md) to work with the Header Object.</span></span> <span data-ttu-id="f88ea-106">Ein aufgefülltes ContentInfo-Objekt ist erforderlich, damit die Anwendung Header Informationen einer vorhandenen Datei lesen kann.</span><span class="sxs-lookup"><span data-stu-id="f88ea-106">A populated ContentInfo object is required in order for the application to read header information of an existing file.</span></span> <span data-ttu-id="f88ea-107">Dies wird erreicht, indem [**imfasfcontentinfo::P arsetheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f88ea-107">This is achieved by calling [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader).</span></span> <span data-ttu-id="f88ea-108">Wenn die Verarbeitung erfolgreich abgeschlossen wird, wird die ASF-Bibliothek für die Datei, die intern von Media Foundation verwaltet wird, mit Header Informationen aus verschiedenen Header Objekten aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="f88ea-108">If parsing completes successfully, the ASF library for the file, which is maintained internally by Media Foundation, is populated with header information from various Header Objects.</span></span> <span data-ttu-id="f88ea-109">Einige dieser Eigenschaften werden für die Anwendung verfügbar gemacht, die Sie über Attribute auf den Präsentations Deskriptoren, den Datenstrom Deskriptor, das Profil und die Metadateneigenschaften abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="f88ea-109">Some of these properties are exposed to the application, which it can retrieve through attributes on the presentation descriptor, stream descriptor, the profile, and metadata properties.</span></span>

<span data-ttu-id="f88ea-110">Eine umfassende Liste der Attribute finden Sie unter [Media Foundation Attribute für ASF-Header Objekte](media-foundation-attributes-for-asf-header-objects.md).</span><span class="sxs-lookup"><span data-stu-id="f88ea-110">For the complete list of attributes, see [Media Foundation Attributes for ASF Header Objects](media-foundation-attributes-for-asf-header-objects.md).</span></span>

## <a name="retrieving-header-information-from-a-presentation-descriptor"></a><span data-ttu-id="f88ea-111">Abrufen von Header Informationen von einem Präsentations Deskriptor</span><span class="sxs-lookup"><span data-stu-id="f88ea-111">Retrieving Header Information from a Presentation Descriptor</span></span>

<span data-ttu-id="f88ea-112">Ein Präsentations deskriptorobjekt enthält die Beschreibung einer bestimmten Medienquelle, in diesem Fall die ASF-Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="f88ea-112">A presentation descriptor object contains the description of a particular media source, in this case the ASF media source.</span></span> <span data-ttu-id="f88ea-113">Wenn der " **Parser Header** "-Rückruf erfolgreich abgeschlossen wird, werden Informationen auf Dateiebene aus dem Header Objekt als Attribute im Präsentations Deskriptor gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f88ea-113">If the **ParseHeader** call completes successfully, file-level information from the Header Object is stored as attributes on the presentation descriptor.</span></span> <span data-ttu-id="f88ea-114">Um den Präsentations Deskriptor zu erstellen, rufen Sie [**imfasfcontentinfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)auf.</span><span class="sxs-lookup"><span data-stu-id="f88ea-114">To create the presentation descriptor, call [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor).</span></span> <span data-ttu-id="f88ea-115">Diese Methode gibt einen Zeiger auf ein aufgefülltes Präsentations deskriptorobjekt zurück, das diese Attribute für die dem ContentInfo-Objekt zugeordnete ASF-Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="f88ea-115">This method returns a pointer to a populated presentation descriptor object that contains these attributes for the ASF file associated with the ContentInfo object.</span></span> <span data-ttu-id="f88ea-116">Um Werte für bestimmte Attribute abzurufen, nennen Sie **imfattributes:: GetXXX** -Methoden für den Präsentations Deskriptor, und geben Sie das MF PD-Attribut "- **\_ \_ ASF \_ xxx** " an.</span><span class="sxs-lookup"><span data-stu-id="f88ea-116">To get values for specific attributes, call **IMFAttributes::Getxxx** methods on the presentation descriptor and specify the **MF\_PD\_ASF\_xxx** attribute.</span></span>

<span data-ttu-id="f88ea-117">Der folgende Beispielcode ruft die Wiedergabedauer einer ASF-Datei ab, die durch ein ContentInfo-Objekt angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f88ea-117">The following example code retrieves the play duration of an ASF file, specified by a ContentInfo object.</span></span>


```C++
HRESULT GetPlayDuration(
    IMFASFContentInfo *pContentInfo,  // An initialized ContentInfo object. 
    UINT64 *pcbPlayDuration           // Receives the play duration.
    )
{
    IMFPresentationDescriptor* pPD = NULL;

    HRESULT hr = pContentInfo->GeneratePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_ASF_FILEPROPERTIES_PLAY_DURATION, pcbPlayDuration);
        pPD->Release();
    }
    return hr;
}

```



<span data-ttu-id="f88ea-118">Weitere Informationen zu Präsentations Deskriptoren im Allgemeinen finden Sie unter [Präsentations Deskriptoren](presentation-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="f88ea-118">For more information about presentation descriptors in general, see [Presentation Descriptors](presentation-descriptors.md).</span></span>

<span data-ttu-id="f88ea-119">Den gesamten Satz von Präsentations deskriptorattributen finden Sie unter [Präsentations deskriptorattribute](presentation-descriptor-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="f88ea-119">For the complete set of presentation descriptor attributes, see [Presentation Descriptor Attributes](presentation-descriptor-attributes.md).</span></span>

## <a name="retrieving-header-information-from-a-stream-descriptor"></a><span data-ttu-id="f88ea-120">Abrufen von Header Informationen aus einem Datenstrom Deskriptor</span><span class="sxs-lookup"><span data-stu-id="f88ea-120">Retrieving Header Information from a Stream Descriptor</span></span>

<span data-ttu-id="f88ea-121">Ein Datenstrom Deskriptor-Objekt macht die [**IMF streamdescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) -Schnittstelle verfügbar und beschreibt die Merkmale der Datenströme in der Datei.</span><span class="sxs-lookup"><span data-stu-id="f88ea-121">A stream descriptor object exposes the [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) interface and describes the characteristics of the streams in the file.</span></span> <span data-ttu-id="f88ea-122">Der Präsentations Deskriptor für den ASF-Inhalt enthält einen oder mehrere streamdeskriptoren, die die im Header Objekt aufgelisteten Streams darstellen.</span><span class="sxs-lookup"><span data-stu-id="f88ea-122">The presentation descriptor for the ASF content contains one or more stream descriptors that represent the streams listed in the Header Object.</span></span> <span data-ttu-id="f88ea-123">Nachdem der Aufruf von [**imfasfcontentinfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) erfolgreich abgeschlossen wurde, werden die zugrunde liegenden streamdeskriptoren mit Informationen auf Streamebene aus den verschiedenen Header Objekten aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="f88ea-123">After the call to [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) completes successfully, the underlying stream descriptors are populated with stream-level information from the various Header Objects.</span></span> <span data-ttu-id="f88ea-124">Um einen Datenstrom Deskriptor für einen ASF-Stream abzurufen, nennen Sie [**imfpresentationdescriptor:: getstreamdescriptorbyindex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) für den Präsentations Deskriptor, der aus dem ContentInfo-Objekt generiert wird.</span><span class="sxs-lookup"><span data-stu-id="f88ea-124">To get a stream descriptor for an ASF stream, call [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) on the presentation descriptor that is generated from the ContentInfo object.</span></span>

<span data-ttu-id="f88ea-125">Einige der streameigenschaften werden als Attribute für streamdeskriptoren festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f88ea-125">Some of the stream properties are set as attributes on stream descriptors.</span></span> <span data-ttu-id="f88ea-126">Aufrufen von **imfattributes:: GetXXX** -Methoden für einen Datenstrom Deskriptor und angeben des **MF SD-Attribut \_ \_ \_ xxx** .</span><span class="sxs-lookup"><span data-stu-id="f88ea-126">Call **IMFAttributes::Getxxx** methods on a stream descriptor and specify the **MF\_SD\_ASF\_xxx** attribute.</span></span>

<span data-ttu-id="f88ea-127">Die gesamten Datenstrom deskriptorattribute finden Sie unter den in den [streamdeskriptorattributen](stream-descriptor-attributes.md)aufgeführten Attributen für den ASF-spezifischen streamdeskriptor.</span><span class="sxs-lookup"><span data-stu-id="f88ea-127">For the complete set of stream descriptor attributes, see "ASF-Specific Stream Descriptor" attributes listed in [Stream Descriptor Attributes](stream-descriptor-attributes.md).</span></span>

## <a name="retrieving-header-information-from-the-profile-object"></a><span data-ttu-id="f88ea-128">Abrufen von Header Informationen aus dem Profil Objekt</span><span class="sxs-lookup"><span data-stu-id="f88ea-128">Retrieving Header Information from the Profile Object</span></span>

<span data-ttu-id="f88ea-129">Zusätzlich zu den streamdeskriptoren beschreibt das ASF-Profil Objekt auch die streameigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f88ea-129">In addition to stream descriptors, the ASF profile object also describes the stream properties.</span></span> <span data-ttu-id="f88ea-130">Um das Profil einer vorhandenen ASF-Datei abzurufen, nennen Sie [**imfasfcontentinfo:: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span><span class="sxs-lookup"><span data-stu-id="f88ea-130">To get the profile of an existing ASF file, call [**IMFASFContentInfo::GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span></span> <span data-ttu-id="f88ea-131">Das von dieser Methode zurückgegebene ASF-Profil Objekt enthält keines der **MF \_ PD- \_ ASF \_ xxx** -Attribute.</span><span class="sxs-lookup"><span data-stu-id="f88ea-131">The ASF profile object returned by this method does not include any of the **MF\_PD\_ASF\_xxx** attributes.</span></span> <span data-ttu-id="f88ea-132">Diese Attribute sind nur für die Anwendung verfügbar, nachdem Sie [**mfkreateasfprofilefrompresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor) aufgerufen hat, um das Profil Objekt aus einem Präsentations Deskriptor zu generieren.</span><span class="sxs-lookup"><span data-stu-id="f88ea-132">These attributes are available to the application only after it calls [**MFCreateASFProfileFromPresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor) to generate the profile object from a presentation descriptor.</span></span> <span data-ttu-id="f88ea-133">Sie können das Profil verwenden, um Zeiger auf den gegenseitigen Ausschluss und streampriorisierungsobjekte zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f88ea-133">You can use the profile to get pointers to the mutual exclusion and stream prioritization objects.</span></span>

<span data-ttu-id="f88ea-134">Weitere Informationen zum Profil Objekt finden Sie unter [ASF-Profil](asf-profile.md) .</span><span class="sxs-lookup"><span data-stu-id="f88ea-134">For information about the profile object, see [ASF Profile](asf-profile.md) .</span></span>

## <a name="retrieving-metadata-from-header-objects"></a><span data-ttu-id="f88ea-135">Abrufen von Metadaten aus Header Objekten</span><span class="sxs-lookup"><span data-stu-id="f88ea-135">Retrieving Metadata from Header Objects</span></span>

<span data-ttu-id="f88ea-136">Eine ASF-Datei kann mehrere Metadateneigenschaften enthalten, die während der Datei Codierung festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f88ea-136">An ASF file can contain several metadata properties that are set during file encoding.</span></span> <span data-ttu-id="f88ea-137">Eine Anwendung kann diese Eigenschaften mit dem ContentInfo-Objekt auflisten.</span><span class="sxs-lookup"><span data-stu-id="f88ea-137">An application can enumerate these properties with the ContentInfo object.</span></span> <span data-ttu-id="f88ea-138">Einige dieser Eigenschaften, z. b. Informationen zu Variablen Bitraten (VBR), sind für die Anwendung über Attribute auf dem Präsentations Deskriptor, streamdeskriptoren und Medientypen für die Mediendatei verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f88ea-138">Some of these properties, such as variable bit rate (VBR) information, are available to the application through attributes on presentation descriptor, stream descriptors, and media types for the media file.</span></span> <span data-ttu-id="f88ea-139">Diese Attribute werden für das ContentInfo-Objekt während der Initialisierung durch den Parameter " [**parameseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) " festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f88ea-139">These attributes are set on the ContentInfo object during initialization through the [**ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) call.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f88ea-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f88ea-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f88ea-141">ASF-ContentInfo-Objekt</span><span class="sxs-lookup"><span data-stu-id="f88ea-141">ASF ContentInfo Object</span></span>](asf-contentinfo-object.md)
</dt> </dl>

 

 



