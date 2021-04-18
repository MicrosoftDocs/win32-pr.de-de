---
title: DRM_PLAY_OPL_EX Struktur (wmdrmsdk. h)
description: Die DRM \_ Play \_ OPL \_ Ex-Struktur enthält Informationen zu den in einer Lizenz für Wiedergabe Aktionen angegebenen Ausgabe Schutz Ebenen (opls).
ms.assetid: 287f6681-f12e-4ef3-b802-24ee7b94bc7f
keywords:
- DRM_PLAY_OPL_EX Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
topic_type:
- apiref
api_name:
- DRM_PLAY_OPL_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edf85ee664b33df9c63c390a870401b100327f53
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368469"
---
# <a name="drm_play_opl_ex-structure"></a><span data-ttu-id="e2f9f-105">DRM \_ Play \_ OPL \_ Ex-Struktur</span><span class="sxs-lookup"><span data-stu-id="e2f9f-105">DRM\_PLAY\_OPL\_EX structure</span></span>

<span data-ttu-id="e2f9f-106">Die **DRM \_ Play \_ OPL \_ Ex** -Struktur enthält Informationen zu den in einer Lizenz für Wiedergabe Aktionen angegebenen Ausgabe Schutz Ebenen (opls).</span><span class="sxs-lookup"><span data-stu-id="e2f9f-106">The **DRM\_PLAY\_OPL\_EX** structure holds information about the output protection levels (OPLs) specified in a license for play actions.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2f9f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2f9f-107">Syntax</span></span>


```C++
typedef struct DRM_PLAY_OPL_EX {
  DWORD                                dwVersion;
  DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS minOPL;
  DRM_OPL_OUTPUT_IDS                   oplIdReserved;
  DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX   vopi;
} ;
```



## <a name="members"></a><span data-ttu-id="e2f9f-108">Member</span><span class="sxs-lookup"><span data-stu-id="e2f9f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="e2f9f-109">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="e2f9f-109">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="e2f9f-110">Versionsnummer:</span><span class="sxs-lookup"><span data-stu-id="e2f9f-110">Version number.</span></span>

</dd> <dt>

<span data-ttu-id="e2f9f-111">**minopl**</span><span class="sxs-lookup"><span data-stu-id="e2f9f-111">**minOPL**</span></span>
</dt> <dd>

<span data-ttu-id="e2f9f-112">[**DRM \_ Minimale \_ Ausgabe \_ Schutz \_ Ebenen**](drmdrm-minimum-output-protection-levels.md) -Struktur, die die minimale OPL enthält, die für die Wiedergabe von Inhalten in verschiedenen Formaten erforderlich</span><span class="sxs-lookup"><span data-stu-id="e2f9f-112">[**DRM\_MINIMUM\_OUTPUT\_PROTECTION\_LEVELS**](drmdrm-minimum-output-protection-levels.md) structure containing the minimum OPL required to play content in different formats.</span></span>

</dd> <dt>

<span data-ttu-id="e2f9f-113">**oplidreserved**</span><span class="sxs-lookup"><span data-stu-id="e2f9f-113">**oplIdReserved**</span></span>
</dt> <dd>

<span data-ttu-id="e2f9f-114">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="e2f9f-114">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="e2f9f-115">**vopi**</span><span class="sxs-lookup"><span data-stu-id="e2f9f-115">**vopi**</span></span>
</dt> <dd>

<span data-ttu-id="e2f9f-116">[**DRM \_ Die Video- \_ Ausgabe \_ Schutz- \_ IDs**](drmdrm-video-output-protection-ids.md) -Struktur, die die für die Wiedergabe des Inhalts geltenden Video-Ausgabe Schutz Bezeichner enthält.</span><span class="sxs-lookup"><span data-stu-id="e2f9f-116">[**DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS**](drmdrm-video-output-protection-ids.md) structure containing the video output protection identifiers that apply to playback of the content.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e2f9f-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e2f9f-117">Remarks</span></span>

<span data-ttu-id="e2f9f-118">Diese Struktur ist mit der **DRM- \_ Wiedergabe- \_ OPL** -Struktur identisch, mit der Ausnahme, dass Sie eine Versionsnummer enthält.</span><span class="sxs-lookup"><span data-stu-id="e2f9f-118">This structure is identical to the **DRM\_PLAY\_OPL** structure, except that it includes a version number.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2f9f-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2f9f-119">Requirements</span></span>



| <span data-ttu-id="e2f9f-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e2f9f-120">Requirement</span></span> | <span data-ttu-id="e2f9f-121">Wert</span><span class="sxs-lookup"><span data-stu-id="e2f9f-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e2f9f-122">Header</span><span class="sxs-lookup"><span data-stu-id="e2f9f-122">Header</span></span><br/> | <dl> <span data-ttu-id="e2f9f-123"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2f9f-123"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2f9f-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2f9f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2f9f-125">**DRM- \_ Wiedergabe- \_ OPL**</span><span class="sxs-lookup"><span data-stu-id="e2f9f-125">**DRM\_PLAY\_OPL**</span></span>](drmdrm-play-opl.md)
</dt> <dt>

[<span data-ttu-id="e2f9f-126">**Strukturen**</span><span class="sxs-lookup"><span data-stu-id="e2f9f-126">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





