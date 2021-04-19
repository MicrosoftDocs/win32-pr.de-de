---
title: DRM_PLAY_OPL Struktur (wmdrmsdk. h)
description: Die DRM- \_ Wiedergabe- \_ OPL-Struktur enthält Informationen zu den in einer Lizenz für Wiedergabe Aktionen angegebenen Ausgabe Schutz Ebenen (opls).
ms.assetid: 10703893-630c-4cbe-a0b0-d2890905daba
keywords:
- DRM_PLAY_OPL Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
topic_type:
- apiref
api_name:
- DRM_PLAY_OPL
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a40d8fe4e8b3c820f9d7bcb405b5c0806040182
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365424"
---
# <a name="drm_play_opl-structure"></a><span data-ttu-id="f59d3-105">DRM- \_ Wiedergabe- \_ OPL-Struktur</span><span class="sxs-lookup"><span data-stu-id="f59d3-105">DRM\_PLAY\_OPL structure</span></span>

<span data-ttu-id="f59d3-106">Die **DRM- \_ Wiedergabe- \_ OPL** -Struktur enthält Informationen zu den in einer Lizenz für Wiedergabe Aktionen angegebenen Ausgabe Schutz Ebenen (opls).</span><span class="sxs-lookup"><span data-stu-id="f59d3-106">The **DRM\_PLAY\_OPL** structure holds information about the output protection levels (OPLs) specified in a license for play actions.</span></span>

## <a name="syntax"></a><span data-ttu-id="f59d3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f59d3-107">Syntax</span></span>


```C++
typedef struct DRM_PLAY_OPL {
  DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS minOPL;
  DRM_OPL_OUTPUT_IDS                   oplIdReserved;
  DRM_VIDEO_OUTPUT_PROTECTION_IDS      vopi;
} ;
```



## <a name="members"></a><span data-ttu-id="f59d3-108">Member</span><span class="sxs-lookup"><span data-stu-id="f59d3-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="f59d3-109">**minopl**</span><span class="sxs-lookup"><span data-stu-id="f59d3-109">**minOPL**</span></span>
</dt> <dd>

<span data-ttu-id="f59d3-110">[**DRM \_ Minimale \_ Ausgabe \_ Schutz \_ Ebenen**](drmdrm-minimum-output-protection-levels.md) -Struktur, die die minimale OPL enthält, die für die Wiedergabe von Inhalten in verschiedenen Formaten erforderlich</span><span class="sxs-lookup"><span data-stu-id="f59d3-110">[**DRM\_MINIMUM\_OUTPUT\_PROTECTION\_LEVELS**](drmdrm-minimum-output-protection-levels.md) structure containing the minimum OPL required to play content in different formats.</span></span>

</dd> <dt>

<span data-ttu-id="f59d3-111">**oplidreserved**</span><span class="sxs-lookup"><span data-stu-id="f59d3-111">**oplIdReserved**</span></span>
</dt> <dd>

<span data-ttu-id="f59d3-112">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="f59d3-112">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="f59d3-113">**vopi**</span><span class="sxs-lookup"><span data-stu-id="f59d3-113">**vopi**</span></span>
</dt> <dd>

<span data-ttu-id="f59d3-114">[**DRM \_ Die Video- \_ Ausgabe \_ Schutz- \_ IDs**](drmdrm-video-output-protection-ids.md) -Struktur, die die für die Wiedergabe des Inhalts geltenden Video-Ausgabe Schutz Bezeichner enthält.</span><span class="sxs-lookup"><span data-stu-id="f59d3-114">[**DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS**](drmdrm-video-output-protection-ids.md) structure containing the video output protection identifiers that apply to playback of the content.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f59d3-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f59d3-115">Requirements</span></span>



| <span data-ttu-id="f59d3-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f59d3-116">Requirement</span></span> | <span data-ttu-id="f59d3-117">Wert</span><span class="sxs-lookup"><span data-stu-id="f59d3-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f59d3-118">Header</span><span class="sxs-lookup"><span data-stu-id="f59d3-118">Header</span></span><br/> | <dl> <span data-ttu-id="f59d3-119"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="f59d3-119"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f59d3-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f59d3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f59d3-121">**DRM- \_ Kopier- \_ OPL**</span><span class="sxs-lookup"><span data-stu-id="f59d3-121">**DRM\_COPY\_OPL**</span></span>](drmdrm-copy-opl.md)
</dt> <dt>

[<span data-ttu-id="f59d3-122">**DRM \_ Play \_ OPL \_ Ex**</span><span class="sxs-lookup"><span data-stu-id="f59d3-122">**DRM\_PLAY\_OPL\_EX**</span></span>](drm-play-opl-ex.md)
</dt> <dt>

[<span data-ttu-id="f59d3-123">**Strukturen**</span><span class="sxs-lookup"><span data-stu-id="f59d3-123">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





