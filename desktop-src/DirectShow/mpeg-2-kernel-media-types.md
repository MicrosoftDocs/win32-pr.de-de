---
description: Für mehrere MPEG-2-Medientyp-GUIDs definiert das Windows-DDK Namen, die sich von den in DirectShow verwendeten Namen unterscheiden. In der folgenden Tabelle sind die DirectShow-Namen (in "ksuuids. h" definiert) und die entsprechenden kernelmodusnamen (in "ksmedia. h" definiert) aufgeführt.
ms.assetid: ecf94552-5a0f-464c-9f9b-4861faa38d05
title: MPEG-2-Kernel Medientypen (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37b03e6d3cbc32c987110ceac98e6aeef6617d6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361369"
---
# <a name="mpeg-2-kernel-media-types"></a><span data-ttu-id="29427-104">MPEG-2-Kernel-Medientypen</span><span class="sxs-lookup"><span data-stu-id="29427-104">MPEG-2 Kernel Media Types</span></span>

<span data-ttu-id="29427-105">Für mehrere MPEG-2-Medientyp-GUIDs definiert das Windows-DDK Namen, die sich von den in DirectShow verwendeten Namen unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="29427-105">For several MPEG-2 media type GUIDs, the Windows DDK defines names that differ from the names used in DirectShow.</span></span> <span data-ttu-id="29427-106">In der folgenden Tabelle sind die DirectShow-Namen (in "ksuuids. h" definiert) und die entsprechenden kernelmodusnamen (in "ksmedia. h" definiert) aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="29427-106">The following table shows the DirectShow names (defined in Ksuuids.h) and the corresponding kernel-mode names (defined in Ksmedia.h).</span></span>



| <span data-ttu-id="29427-107">Name in "ksuuids. h"</span><span class="sxs-lookup"><span data-stu-id="29427-107">Name in Ksuuids.h</span></span>              | <span data-ttu-id="29427-108">Name in ksmedia. h</span><span class="sxs-lookup"><span data-stu-id="29427-108">Name in Ksmedia.h</span></span>                          |
|--------------------------------|--------------------------------------------|
| <span data-ttu-id="29427-109">Formatieren von \_ WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="29427-109">FORMAT\_WaveFormatEx</span></span>           | <span data-ttu-id="29427-110">ksdataformat- \_ Spezifizierer \_ WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="29427-110">KSDATAFORMAT\_SPECIFIER\_WAVEFORMATEX</span></span>      |
| <span data-ttu-id="29427-111">MPEG2Video formatieren \_</span><span class="sxs-lookup"><span data-stu-id="29427-111">FORMAT\_MPEG2Video</span></span>             | <span data-ttu-id="29427-112">Video zur ksdataformat- \_ Spezifizierer-Klasse \_ \_</span><span class="sxs-lookup"><span data-stu-id="29427-112">KSDATAFORMAT\_SPECIFIER\_MPEG2\_VIDEO</span></span>      |
| <span data-ttu-id="29427-113">mediasubtype \_ ATSC \_ Si</span><span class="sxs-lookup"><span data-stu-id="29427-113">MEDIASUBTYPE\_ATSC\_SI</span></span>         | <span data-ttu-id="29427-114">ksdataformat- \_ Untertyp \_ ATSC \_ Si</span><span class="sxs-lookup"><span data-stu-id="29427-114">KSDATAFORMAT\_SUBTYPE\_ATSC\_SI</span></span>            |
| <span data-ttu-id="29427-115">Mediasubtype \_ Dolby \_ AC3</span><span class="sxs-lookup"><span data-stu-id="29427-115">MEDIASUBTYPE\_DOLBY\_AC3</span></span>       | <span data-ttu-id="29427-116">Ksdataformat \_ -Untertyp \_ AC3 \_ -Audiodatei</span><span class="sxs-lookup"><span data-stu-id="29427-116">KSDATAFORMAT\_SUBTYPE\_AC3\_AUDIO</span></span>          |
| <span data-ttu-id="29427-117">mediasubtype- \_ DVB \_ Si</span><span class="sxs-lookup"><span data-stu-id="29427-117">MEDIASUBTYPE\_DVB\_SI</span></span>          | <span data-ttu-id="29427-118">ksdataformat- \_ Untertyp \_ DVB \_ Si</span><span class="sxs-lookup"><span data-stu-id="29427-118">KSDATAFORMAT\_SUBTYPE\_DVB\_SI</span></span>             |
| <span data-ttu-id="29427-119">mediasubtype \_ DVD \_ LPCM \_ -Audiodatei</span><span class="sxs-lookup"><span data-stu-id="29427-119">MEDIASUBTYPE\_DVD\_LPCM\_AUDIO</span></span> | <span data-ttu-id="29427-120">ksdataformat \_ -Untertyp \_ LPCM \_ -Audiodatei</span><span class="sxs-lookup"><span data-stu-id="29427-120">KSDATAFORMAT\_SUBTYPE\_LPCM\_AUDIO</span></span>         |
| <span data-ttu-id="29427-121">Mediasubtype \_ \_ -Audiodatei</span><span class="sxs-lookup"><span data-stu-id="29427-121">MEDIASUBTYPE\_MPEG2\_AUDIO</span></span>     | <span data-ttu-id="29427-122">"Ksdataformat" \_ -Untertyp " \_ MPEG2" \_</span><span class="sxs-lookup"><span data-stu-id="29427-122">KSDATAFORMAT\_SUBTYPE\_MPEG2\_AUDIO</span></span>        |
| <span data-ttu-id="29427-123">Mediasubtype \_ - \_ Programm</span><span class="sxs-lookup"><span data-stu-id="29427-123">MEDIASUBTYPE\_MPEG2\_PROGRAM</span></span>   | <span data-ttu-id="29427-124">Statischer \_ ksdataformat- \_ Typ " \_ MPEG2 \_ "</span><span class="sxs-lookup"><span data-stu-id="29427-124">STATIC\_KSDATAFORMAT\_TYPE\_MPEG2\_PROGRAM</span></span> |
| <span data-ttu-id="29427-125">Mediasubtype \_ MPEG2- \_ Transport</span><span class="sxs-lookup"><span data-stu-id="29427-125">MEDIASUBTYPE\_MPEG2\_TRANSPORT</span></span> | <span data-ttu-id="29427-126">Ksdataformat- \_ Typ " \_ MPEG2- \_ Transport"</span><span class="sxs-lookup"><span data-stu-id="29427-126">KSDATAFORMAT\_TYPE\_MPEG2\_TRANSPORT</span></span>       |
| <span data-ttu-id="29427-127">Video zu mediasubtype \_ MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="29427-127">MEDIASUBTYPE\_MPEG2\_VIDEO</span></span>     | <span data-ttu-id="29427-128">Ksdataformat- \_ Untertyp "MPEG2"- \_ \_ Video</span><span class="sxs-lookup"><span data-stu-id="29427-128">KSDATAFORMAT\_SUBTYPE\_MPEG2\_VIDEO</span></span>        |
| <span data-ttu-id="29427-129">Abschnitte zu "MediaType" \_ \_</span><span class="sxs-lookup"><span data-stu-id="29427-129">MEDIATYPE\_MPEG2\_SECTIONS</span></span>     | <span data-ttu-id="29427-130">"Ksdataformat"- \_ Typ " \_ MPEG2" \_</span><span class="sxs-lookup"><span data-stu-id="29427-130">KSDATAFORMAT\_TYPE\_MPEG2\_SECTIONS</span></span>        |
| <span data-ttu-id="29427-131">MediaType \_ -Audiodatei</span><span class="sxs-lookup"><span data-stu-id="29427-131">MEDIATYPE\_Audio</span></span>               | <span data-ttu-id="29427-132">ksdataformat \_ \_ -typaudiodatei</span><span class="sxs-lookup"><span data-stu-id="29427-132">KSDATAFORMAT\_TYPE\_AUDIO</span></span>                  |
| <span data-ttu-id="29427-133">MediaType \_ MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="29427-133">MEDIATYPE\_MPEG2\_PES</span></span>          | <span data-ttu-id="29427-134">Ksdataformat- \_ Typ " \_ MPEG2" \_</span><span class="sxs-lookup"><span data-stu-id="29427-134">KSDATAFORMAT\_TYPE\_MPEG2\_PES</span></span>             |
| <span data-ttu-id="29427-135">MediaType- \_ Video</span><span class="sxs-lookup"><span data-stu-id="29427-135">MEDIATYPE\_Video</span></span>               | <span data-ttu-id="29427-136">Video zu ksdataformat- \_ Typ \_</span><span class="sxs-lookup"><span data-stu-id="29427-136">KSDATAFORMAT\_TYPE\_VIDEO</span></span>                  |



 

## <a name="requirements"></a><span data-ttu-id="29427-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29427-137">Requirements</span></span>



| <span data-ttu-id="29427-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="29427-138">Requirement</span></span> | <span data-ttu-id="29427-139">Wert</span><span class="sxs-lookup"><span data-stu-id="29427-139">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="29427-140">Header</span><span class="sxs-lookup"><span data-stu-id="29427-140">Header</span></span><br/> | <dl> <span data-ttu-id="29427-141"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="29427-141"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29427-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29427-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29427-143">MPEG-2-Medientypen</span><span class="sxs-lookup"><span data-stu-id="29427-143">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 




