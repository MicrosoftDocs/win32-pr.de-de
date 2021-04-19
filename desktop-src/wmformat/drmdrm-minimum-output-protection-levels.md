---
title: DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS Struktur (wmdrmsdk. h)
description: Die minimale DRM- \_ \_ Ausgabe \_ Schutz \_ Ebenen-Struktur enthält die minimalen Ausgabe Schutz Ebenen (opls) für die Wiedergabe verschiedener Inhaltstypen. Ein Gerät muss den minimalen OPL-Wert für einen Datentyp unterstützen, um diese Art von Daten vom Reader empfangen zu können.
ms.assetid: 6232ecd4-9829-4de3-9810-70e3d3c129a9
keywords:
- DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
topic_type:
- apiref
api_name:
- DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 060fdda4cd1c3cc665e396a72d46ac05e721abe4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353808"
---
# <a name="drm_minimum_output_protection_levels-structure"></a><span data-ttu-id="5b55f-106">DRM- \_ minimale \_ Ausgabe \_ Schutz Ebenen- \_ Struktur</span><span class="sxs-lookup"><span data-stu-id="5b55f-106">DRM\_MINIMUM\_OUTPUT\_PROTECTION\_LEVELS structure</span></span>

<span data-ttu-id="5b55f-107">Die **minimale DRM- \_ \_ Ausgabe \_ Schutz \_ Ebenen** -Struktur enthält die minimalen Ausgabe Schutz Ebenen (opls) für die Wiedergabe verschiedener Inhaltstypen.</span><span class="sxs-lookup"><span data-stu-id="5b55f-107">The **DRM\_MINIMUM\_OUTPUT\_PROTECTION\_LEVELS** structure holds the minimum output protection levels (OPLs) for playback of various types of content.</span></span> <span data-ttu-id="5b55f-108">Ein Gerät muss den minimalen OPL-Wert für einen Datentyp unterstützen, um diese Art von Daten vom Reader empfangen zu können.</span><span class="sxs-lookup"><span data-stu-id="5b55f-108">A device must support the minimum OPL for a type of data to receive that type of data from the reader.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b55f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b55f-109">Syntax</span></span>


```C++
typedef struct DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS {
  WORD wCompressedDigitalVideo;
  WORD wUncompressedDigitalVideo;
  WORD wAnalogVideo;
  WORD wCompressedDigitalAudio;
  WORD wUncompressedDigitalAudio;
} ;
```



## <a name="members"></a><span data-ttu-id="5b55f-110">Member</span><span class="sxs-lookup"><span data-stu-id="5b55f-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="5b55f-111">**wcompresseddigitalvideo**</span><span class="sxs-lookup"><span data-stu-id="5b55f-111">**wCompressedDigitalVideo**</span></span>
</dt> <dd>

<span data-ttu-id="5b55f-112">Mindestens erforderliche OPL für den Empfang komprimierter digitaler Videos.</span><span class="sxs-lookup"><span data-stu-id="5b55f-112">Minimum OPL required to receive compressed digital video.</span></span>

</dd> <dt>

<span data-ttu-id="5b55f-113">**wuncompresseddigitalvideo**</span><span class="sxs-lookup"><span data-stu-id="5b55f-113">**wUncompressedDigitalVideo**</span></span>
</dt> <dd>

<span data-ttu-id="5b55f-114">Mindestens erforderliche OPL für den Empfang von unkomprimiertem digitalem Video.</span><span class="sxs-lookup"><span data-stu-id="5b55f-114">Minimum OPL required to receive uncompressed digital video.</span></span>

</dd> <dt>

<span data-ttu-id="5b55f-115">**wanalogvideo**</span><span class="sxs-lookup"><span data-stu-id="5b55f-115">**wAnalogVideo**</span></span>
</dt> <dd>

<span data-ttu-id="5b55f-116">Mindestens erforderliche OPL für den Empfang von analogen Videos.</span><span class="sxs-lookup"><span data-stu-id="5b55f-116">Minimum OPL required to receive analog video.</span></span>

</dd> <dt>

<span data-ttu-id="5b55f-117">**wcompresseddigitalaudiodatei**</span><span class="sxs-lookup"><span data-stu-id="5b55f-117">**wCompressedDigitalAudio**</span></span>
</dt> <dd>

<span data-ttu-id="5b55f-118">Mindestens erforderliche OPL für den Empfang komprimierter digitaler Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="5b55f-118">Minimum OPL required to receive compressed digital audio.</span></span>

</dd> <dt>

<span data-ttu-id="5b55f-119">**wuncompresseddigitalaudiodatei**</span><span class="sxs-lookup"><span data-stu-id="5b55f-119">**wUncompressedDigitalAudio**</span></span>
</dt> <dd>

<span data-ttu-id="5b55f-120">Mindestens erforderliche OPL zum Empfangen von unkomprimiertem digitaler Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="5b55f-120">Minimum OPL required to receive uncompressed digital audio.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5b55f-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5b55f-121">Remarks</span></span>

<span data-ttu-id="5b55f-122">Diese Struktur wird als Mitglied der [**DRM-Wiedergabe- \_ \_ OPL**](drmdrm-play-opl.md) -Struktur verwendet.</span><span class="sxs-lookup"><span data-stu-id="5b55f-122">This structure is used as a member of the [**DRM\_PLAY\_OPL**](drmdrm-play-opl.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b55f-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5b55f-123">Requirements</span></span>



| <span data-ttu-id="5b55f-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5b55f-124">Requirement</span></span> | <span data-ttu-id="5b55f-125">Wert</span><span class="sxs-lookup"><span data-stu-id="5b55f-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5b55f-126">Header</span><span class="sxs-lookup"><span data-stu-id="5b55f-126">Header</span></span><br/> | <dl> <span data-ttu-id="5b55f-127"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b55f-127"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b55f-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b55f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b55f-129">**Strukturen**</span><span class="sxs-lookup"><span data-stu-id="5b55f-129">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





