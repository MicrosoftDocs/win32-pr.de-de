---
description: Der Microsoft AC-3-Encoder-Filter codiert Stereo PCM-Audiodaten in einen Dolby Digital Bitstream.
ms.assetid: 59d46ee2-d45f-4492-938d-39c55a7368e1
title: Microsoft AC-3 Encoder (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 160b020e07bb3ba4e4dc5636b58dd0e66f581a6f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124519"
---
# <a name="microsoft-ac-3-encoder"></a><span data-ttu-id="b713c-103">Microsoft AC-3-Encoder</span><span class="sxs-lookup"><span data-stu-id="b713c-103">Microsoft AC-3 Encoder</span></span>

<span data-ttu-id="b713c-104">Der Microsoft AC-3-Encoder-Filter codiert Stereo PCM-Audiodaten in einen Dolby Digital Bitstream.</span><span class="sxs-lookup"><span data-stu-id="b713c-104">The Microsoft AC-3 Encoder filter encodes stereo PCM audio to a Dolby Digital bitstream.</span></span>

> [!Note]  
> <span data-ttu-id="b713c-105">Die Microsoft-Implementierung der Dolby Digital-Technologie ist gemäß den Bedingungen des Dolby Digital Licensing Program eingeschränkt, das von Microsoft-Anwendungen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b713c-105">The Microsoft implementation of the Dolby Digital technology is restricted under terms of the Dolby Digital licensing program to use by Microsoft applications.</span></span>

 

> [!Note]  
> <span data-ttu-id="b713c-106">Dieser Filter wird auf IA-64-basierten Plattformen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b713c-106">This filter is not supported on IA-64-based platforms.</span></span>

 



<span data-ttu-id="b713c-107">Filter Informationen</span><span class="sxs-lookup"><span data-stu-id="b713c-107">Filter Information</span></span>

<span data-ttu-id="b713c-108">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="b713c-108">Filter Interfaces</span></span>

[<span data-ttu-id="b713c-109">**Ibasefilter**</span><span class="sxs-lookup"><span data-stu-id="b713c-109">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/>

<span data-ttu-id="b713c-110">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="b713c-110">Input Pin Media Types</span></span>

<span data-ttu-id="b713c-111">**MediaType \_ Audiodatei**, **mediasubtype \_ PCM**</span><span class="sxs-lookup"><span data-stu-id="b713c-111">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_PCM**</span></span><br/> <span data-ttu-id="b713c-112">Der Eingabetyp muss 48-kHz-Stereo, 16 Bits pro Beispiel sein.</span><span class="sxs-lookup"><span data-stu-id="b713c-112">The input type must be 48-kHz stereo, 16 bits per sample.</span></span><br/>

<span data-ttu-id="b713c-113">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="b713c-113">Input Pin Interfaces</span></span>

[<span data-ttu-id="b713c-114">**IMemInputPin**</span><span class="sxs-lookup"><span data-stu-id="b713c-114">**IMemInputPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [<span data-ttu-id="b713c-115">**IPin**</span><span class="sxs-lookup"><span data-stu-id="b713c-115">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="b713c-116">**Iqualitycontrol**</span><span class="sxs-lookup"><span data-stu-id="b713c-116">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="b713c-117">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="b713c-117">Output Pin Media Types</span></span>

<span data-ttu-id="b713c-118">**MediaType \_ Audiodatei**, **mediasubtype \_ Dolby \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="b713c-118">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DOLBY\_AC3**</span></span><br/> <span data-ttu-id="b713c-119">**MediaType \_ Stream**, **mediasubtype \_ Dolby \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="b713c-119">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_DOLBY\_AC3**</span></span><br/>

<span data-ttu-id="b713c-120">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="b713c-120">Output Pin Interfaces</span></span>

[<span data-ttu-id="b713c-121">**Imediaseeking**</span><span class="sxs-lookup"><span data-stu-id="b713c-121">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="b713c-122">**IPin**</span><span class="sxs-lookup"><span data-stu-id="b713c-122">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="b713c-123">**Iqualitycontrol**</span><span class="sxs-lookup"><span data-stu-id="b713c-123">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="b713c-124">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="b713c-124">Filter CLSID</span></span>

<span data-ttu-id="b713c-125">**CLSID \_ CMSAC3Enc** (in wmcodecdsp. h deklariert)</span><span class="sxs-lookup"><span data-stu-id="b713c-125">**CLSID\_CMSAC3Enc** (declared in wmcodecdsp.h)</span></span>

<span data-ttu-id="b713c-126">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="b713c-126">Executable</span></span>

<span data-ttu-id="b713c-127">msac3enc.dll</span><span class="sxs-lookup"><span data-stu-id="b713c-127">msac3enc.dll</span></span>

[<span data-ttu-id="b713c-128">Verdienst</span><span class="sxs-lookup"><span data-stu-id="b713c-128">Merit</span></span>](merit.md)

<span data-ttu-id="b713c-129">**das Verdienst wird \_ \_ nicht \_ verwendet.**</span><span class="sxs-lookup"><span data-stu-id="b713c-129">**MERIT\_DO\_NOT\_USE**</span></span>

[<span data-ttu-id="b713c-130">Filter Kategorie</span><span class="sxs-lookup"><span data-stu-id="b713c-130">Filter Category</span></span>](filter-categories.md)

<span data-ttu-id="b713c-131">**CLSID \_ legacyamfiltercategory**</span><span class="sxs-lookup"><span data-stu-id="b713c-131">**CLSID\_LegacyAmFilterCategory**</span></span>



 

## <a name="remarks"></a><span data-ttu-id="b713c-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b713c-132">Remarks</span></span>

<span data-ttu-id="b713c-133">Dieser Filter ist nicht zur Verwendung durch Drittanbieter Anwendungen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b713c-133">This filter is not available for use by third-party applications.</span></span>

## <a name="requirements"></a><span data-ttu-id="b713c-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b713c-134">Requirements</span></span>



| <span data-ttu-id="b713c-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b713c-135">Requirement</span></span> | <span data-ttu-id="b713c-136">Wert</span><span class="sxs-lookup"><span data-stu-id="b713c-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b713c-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b713c-137">Minimum supported client</span></span><br/> | <span data-ttu-id="b713c-138">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop Apps\]</span><span class="sxs-lookup"><span data-stu-id="b713c-138">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b713c-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b713c-139">Minimum supported server</span></span><br/> | <span data-ttu-id="b713c-140">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b713c-140">None supported</span></span><br/>                                                                                                                                                     |
| <span data-ttu-id="b713c-141">Header</span><span class="sxs-lookup"><span data-stu-id="b713c-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="b713c-142"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b713c-142"><dt>Wmcodecdsp.h</dt></span></span> </dl>                                                                                       |



## <a name="see-also"></a><span data-ttu-id="b713c-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b713c-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b713c-144">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="b713c-144">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




