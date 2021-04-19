---
title: WMDRM_OUTPUT_PROTECTION_LEVELS Struktur (wmdrmsdk. h)
description: Die Struktur der WMDRM- \_ Ausgabe \_ Schutz \_ Ebenen enthält die von einer Lizenz für die Durchführung verschiedener Aktionen benötigten Ausgabe Schutz Ebenen (Output Protection Levels, opls).
ms.assetid: 6b284180-1033-4c57-b010-6d4ab4bc593a
keywords:
- WMDRM_OUTPUT_PROTECTION_LEVELS Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
topic_type:
- apiref
api_name:
- WMDRM_OUTPUT_PROTECTION_LEVELS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d720a8aef42178da188b71a1635d97031b138397
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358332"
---
# <a name="wmdrm_output_protection_levels-structure"></a><span data-ttu-id="4e54d-105">WMDRM- \_ Ausgabe \_ Schutz Ebenen- \_ Struktur</span><span class="sxs-lookup"><span data-stu-id="4e54d-105">WMDRM\_OUTPUT\_PROTECTION\_LEVELS structure</span></span>

<span data-ttu-id="4e54d-106">Die Struktur der **WMDRM- \_ Ausgabe \_ Schutz \_ Ebenen** enthält die von einer Lizenz für die Durchführung verschiedener Aktionen benötigten Ausgabe Schutz Ebenen (Output Protection Levels, opls).</span><span class="sxs-lookup"><span data-stu-id="4e54d-106">The **WMDRM\_OUTPUT\_PROTECTION\_LEVELS** structure contains the output protections levels (OPLs) required by a license to perform various actions.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e54d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e54d-107">Syntax</span></span>


```C++
typedef struct WMDRM_OUTPUT_PROTECTION_LEVELS {
  WORD wCompressedDigitalVideo;
  WORD wUncompressedDigitalVideo;
  WORD wAnalogVideo;
  WORD wCompressedDigitalAudio;
  WORD wUncompressedDigitalAudio;
  WORD wMinimumCopyProtectionLevel;
} ;
```



## <a name="members"></a><span data-ttu-id="4e54d-108">Member</span><span class="sxs-lookup"><span data-stu-id="4e54d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="4e54d-109">**wcompresseddigitalvideo**</span><span class="sxs-lookup"><span data-stu-id="4e54d-109">**wCompressedDigitalVideo**</span></span>
</dt> <dd>

<span data-ttu-id="4e54d-110">Mindestens erforderliche OPL für den Empfang komprimierter digitaler Videos.</span><span class="sxs-lookup"><span data-stu-id="4e54d-110">Minimum OPL required to receive compressed digital video.</span></span>

</dd> <dt>

<span data-ttu-id="4e54d-111">**wuncompresseddigitalvideo**</span><span class="sxs-lookup"><span data-stu-id="4e54d-111">**wUncompressedDigitalVideo**</span></span>
</dt> <dd>

<span data-ttu-id="4e54d-112">Mindestens erforderliche OPL für den Empfang von unkomprimiertem digitalem Video.</span><span class="sxs-lookup"><span data-stu-id="4e54d-112">Minimum OPL required to receive uncompressed digital video.</span></span>

</dd> <dt>

<span data-ttu-id="4e54d-113">**wanalogvideo**</span><span class="sxs-lookup"><span data-stu-id="4e54d-113">**wAnalogVideo**</span></span>
</dt> <dd>

<span data-ttu-id="4e54d-114">Mindestens erforderliche OPL für den Empfang von analogen Videos.</span><span class="sxs-lookup"><span data-stu-id="4e54d-114">Minimum OPL required to receive analog video.</span></span>

</dd> <dt>

<span data-ttu-id="4e54d-115">**wcompresseddigitalaudiodatei**</span><span class="sxs-lookup"><span data-stu-id="4e54d-115">**wCompressedDigitalAudio**</span></span>
</dt> <dd>

<span data-ttu-id="4e54d-116">Mindestens erforderliche OPL für den Empfang komprimierter digitaler Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="4e54d-116">Minimum OPL required to receive compressed digital audio.</span></span>

</dd> <dt>

<span data-ttu-id="4e54d-117">**wuncompresseddigitalaudiodatei**</span><span class="sxs-lookup"><span data-stu-id="4e54d-117">**wUncompressedDigitalAudio**</span></span>
</dt> <dd>

<span data-ttu-id="4e54d-118">Mindestens erforderliche OPL zum Empfangen von unkomprimiertem digitaler Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="4e54d-118">Minimum OPL required to receive uncompressed digital audio.</span></span>

</dd> <dt>

<span data-ttu-id="4e54d-119">**wminimumcopyschutzlevel**</span><span class="sxs-lookup"><span data-stu-id="4e54d-119">**wMinimumCopyProtectionLevel**</span></span>
</dt> <dd>

<span data-ttu-id="4e54d-120">Mindestens erforderliche OPL zum Kopieren des Inhalts.</span><span class="sxs-lookup"><span data-stu-id="4e54d-120">Minimum OPL required to copy the content.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4e54d-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4e54d-121">Remarks</span></span>

<span data-ttu-id="4e54d-122">Diese Struktur wird von der [**iwmdrmlicense:: getoutputschutzlevels**](iwmdrmlicense-getoutputprotectionlevels.md) -Methode verwendet.</span><span class="sxs-lookup"><span data-stu-id="4e54d-122">This structure is used by the [**IWMDRMLicense::GetOutputProtectionLevels**](iwmdrmlicense-getoutputprotectionlevels.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e54d-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4e54d-123">Requirements</span></span>



| <span data-ttu-id="4e54d-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4e54d-124">Requirement</span></span> | <span data-ttu-id="4e54d-125">Wert</span><span class="sxs-lookup"><span data-stu-id="4e54d-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4e54d-126">Header</span><span class="sxs-lookup"><span data-stu-id="4e54d-126">Header</span></span><br/> | <dl> <span data-ttu-id="4e54d-127"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e54d-127"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e54d-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e54d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e54d-129">**Strukturen**</span><span class="sxs-lookup"><span data-stu-id="4e54d-129">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





