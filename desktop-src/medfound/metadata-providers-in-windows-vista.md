---
description: In Windows Vista macht Microsoft Media Foundation Metadaten über die IMF Metadata-Schnittstelle verfügbar.
ms.assetid: a26e40c2-1717-4a13-8bf0-e41376a8d317
title: Metadatenanbieter in Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1726e04058a7b15e387fca4f3faa94fce7c91c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356520"
---
# <a name="metadata-providers-in-windows-vista"></a><span data-ttu-id="f0055-103">Metadatenanbieter in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f0055-103">Metadata Providers in Windows Vista</span></span>

<span data-ttu-id="f0055-104">In Windows Vista macht Microsoft Media Foundation Metadaten über die [**IMF Metadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f0055-104">In Windows Vista, Microsoft Media Foundation exposes metadata through the [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) interface.</span></span>

## <a name="reading-metadata"></a><span data-ttu-id="f0055-105">Lesen von Metadaten</span><span class="sxs-lookup"><span data-stu-id="f0055-105">Reading Metadata</span></span>

<span data-ttu-id="f0055-106">Um Metadaten aus einer Medienquelle zu lesen, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="f0055-106">To read metadata from a media source, perform the following steps:</span></span>

1.  <span data-ttu-id="f0055-107">Einen Zeiger auf die [**imfmediasource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) -Schnittstelle der Medienquelle erhalten.</span><span class="sxs-lookup"><span data-stu-id="f0055-107">Get a pointer to the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface of the media source.</span></span> <span data-ttu-id="f0055-108">Sie können die [**imfsourceresolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) -Schnittstelle verwenden, um einen **imfmediasource** -Zeiger zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f0055-108">You can use the [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) interface to get an **IMFMediaSource** pointer.</span></span>
2.  <span data-ttu-id="f0055-109">Aufrufen von [**imfmediasource:: foratepresentationdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) zum Abrufen des Präsentations Deskriptors der Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="f0055-109">Call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) to get the media source's presentation descriptor.</span></span>
3.  <span data-ttu-id="f0055-110">Aufrufen von [**mfgetservice**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) für die Medienquelle, um einen Zeiger auf die [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) -Schnittstelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f0055-110">Call [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) on the media source to get a pointer to the [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) interface.</span></span> <span data-ttu-id="f0055-111">Geben Sie im *guidservice* -Parameter von **MF-Service** den Wert **MF \_ - \_ metadatenanbieterdienst \_** an.</span><span class="sxs-lookup"><span data-stu-id="f0055-111">In the *guidService* parameter of **MFGetService**, specify the value **MF\_METADATA\_PROVIDER\_SERVICE**.</span></span> <span data-ttu-id="f0055-112">Wenn die Quelle die **IMFMetadataProvider** -Schnittstelle nicht unterstützt, gibt **MF-Service** einen **\_ \_ nicht \_ unterstützten MF-Dienst** zurück.</span><span class="sxs-lookup"><span data-stu-id="f0055-112">If the source does not support the **IMFMetadataProvider** interface, **MFGetService** returns **MF\_E\_UNSUPPORTED\_SERVICE**.</span></span>
4.  <span data-ttu-id="f0055-113">Aufrufen von [**IMFMetadataProvider:: getmfmetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) und übergeben eines Zeigers an den Präsentations Deskriptor.</span><span class="sxs-lookup"><span data-stu-id="f0055-113">Call [**IMFMetadataProvider::GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) and pass in a pointer to the presentation descriptor.</span></span> <span data-ttu-id="f0055-114">Diese Methode gibt einen Zeiger auf die [**imfmetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) -Schnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="f0055-114">This method returns a pointer to the [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) interface.</span></span>
    -   <span data-ttu-id="f0055-115">Zum Abrufen von Metadaten auf Streamebene müssen Sie zuerst [**imfstreamdescriptor:: getstreamidentifier**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getstreamidentifier) aufrufen, um den Datenstrom Bezeichner zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f0055-115">To get stream-level metadata first call [**IMFStreamDescriptor::GetStreamIdentifier**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getstreamidentifier) to get the stream identifier.</span></span> <span data-ttu-id="f0055-116">Übergeben Sie dann den Datenstrom Bezeichner im *dwstreamidentifier* -Parameter von [**getmfimetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata).</span><span class="sxs-lookup"><span data-stu-id="f0055-116">Then pass the stream identifier in the *dwStreamIdentifier* parameter of [**GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata).</span></span>
    -   <span data-ttu-id="f0055-117">Legen Sie zum Aufrufen von Metadaten auf Präsentationsebene *dwstreamidentifier* auf 0 (null) fest.</span><span class="sxs-lookup"><span data-stu-id="f0055-117">To get presentation-level metadata, set *dwStreamIdentifier* to zero.</span></span>
5.  <span data-ttu-id="f0055-118">\[Optional \] [**: imfmetadata:: getalllanguages**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getalllanguages) aufrufen, um eine Liste der Sprachen zu erhalten, in denen Metadaten verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="f0055-118">\[Optional\] Call [**IMFMetadata::GetAllLanguages**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getalllanguages) to get a list of the languages in which metadata is available.</span></span> <span data-ttu-id="f0055-119">Sprachen werden mithilfe von RFC 1766-kompatiblen sprach Tags identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f0055-119">Languages are identified using RFC 1766-compliant language tags.</span></span>
6.  <span data-ttu-id="f0055-120">\[Optionaler \] Rückruf [**imfmetadata:: setLanguage**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-setlanguage) , um die Sprache auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="f0055-120">\[Optional\] Call [**IMFMetadata::SetLanguage**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-setlanguage) to select the language.</span></span>
7.  <span data-ttu-id="f0055-121">\[Optional \] [**: imfmetadata:: getallpropertynames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) aufrufen, um eine Liste der Namen aller Metadateneigenschaften für diesen Stream oder diese Präsentation abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f0055-121">\[Optional\] Call [**IMFMetadata::GetAllPropertyNames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) to get a list of the names of all the metadata properties for this stream or presentation.</span></span>
8.  <span data-ttu-id="f0055-122">Wenn Sie [**imfmetadata:: GetProperty**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) aufrufen, um einen bestimmten Wert für die Metadateneigenschaft abzurufen, übergeben Sie den Namen der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f0055-122">Call [**IMFMetadata::GetProperty**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) to get a specific metadata property value, passing in the name of the property.</span></span>

<span data-ttu-id="f0055-123">Der folgende Code zeigt die Schritte 2 – 4:</span><span class="sxs-lookup"><span data-stu-id="f0055-123">The following code shows steps 2–4:</span></span>


```C++
HRESULT GetMetadata(
    IMFMediaSource *pSource, IMFMetadata **ppMetadata, DWORD dwStream = 0)
{
    IMFPresentationDescriptor *pPD = NULL;
    IMFMetadataProvider *pProvider = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFGetService(
        pSource, MF_METADATA_PROVIDER_SERVICE, IID_PPV_ARGS(&pProvider));

    if (FAILED(hr))
    {
        goto done;
    }

    hr = pProvider->GetMFMetadata(pPD, dwStream, 0, ppMetadata);

done:
    SafeRelease(&pPD);
    SafeRelease(&pProvider);
    return hr;
}
```



<span data-ttu-id="f0055-124">Der folgende Code zeigt die Schritte 7 – 8.</span><span class="sxs-lookup"><span data-stu-id="f0055-124">The following code shows steps 7–8.</span></span> <span data-ttu-id="f0055-125">Angenommen, `DisplayProperty` Es handelt sich um eine Funktion, die einen **PROPVARIANT** -Wert anzeigt.</span><span class="sxs-lookup"><span data-stu-id="f0055-125">Assume that `DisplayProperty` is a function that displays a **PROPVARIANT** value.</span></span>


```C++
HRESULT DisplayMetadata(IMFMetadata *pMetadata)
{
    PROPVARIANT varNames;
    HRESULT hr = pMetadata->GetAllPropertyNames(&varNames);
    if (FAILED(hr))
    {
        return hr;
    }

    for (ULONG i = 0; i < varNames.calpwstr.cElems; i++)
    {
        wprintf(L"%s\n", varNames.calpwstr.pElems[i]);

        PROPVARIANT varValue;
        hr = pMetadata->GetProperty( varNames.calpwstr.pElems[i], &varValue );
        if (SUCCEEDED(hr))
        {
            DisplayProperty(varValue);
            PropVariantClear(&varValue);
        }
    }

    PropVariantClear(&varNames);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="f0055-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f0055-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0055-127">Medien Metadaten</span><span class="sxs-lookup"><span data-stu-id="f0055-127">Media Metadata</span></span>](media-metadata.md)
</dt> <dt>

[<span data-ttu-id="f0055-128">Shellmetadatenanbieter</span><span class="sxs-lookup"><span data-stu-id="f0055-128">Shell Metadata Providers</span></span>](shell-metadata-providers.md)
</dt> </dl>

 

 



