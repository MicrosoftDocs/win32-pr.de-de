---
title: DRM_VIDEO_OUTPUT_PROTECTION_IDS Struktur (wmdrmsdk. h)
description: Die Struktur der DRM- \_ Video- \_ Ausgabe \_ Schutz- \_ IDs enthält ein Array von DRM- \_ Video- \_ Ausgabe \_ Schutzstrukturen.
ms.assetid: 9f206a7e-c92b-4f29-a591-72784086d1db
keywords:
- DRM_VIDEO_OUTPUT_PROTECTION_IDS Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
topic_type:
- apiref
api_name:
- DRM_VIDEO_OUTPUT_PROTECTION_IDS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51af3ccebec52ab6f6863aeb376ed27f8c8e2467
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364423"
---
# <a name="drm_video_output_protection_ids-structure"></a><span data-ttu-id="16348-105">Struktur der DRM- \_ Video- \_ Ausgabe \_ Schutz- \_ IDs</span><span class="sxs-lookup"><span data-stu-id="16348-105">DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS structure</span></span>

<span data-ttu-id="16348-106">Die Struktur der **DRM- \_ Video- \_ Ausgabe Schutz- \_ \_ IDs** enthält ein Array von **DRM-Video- \_ \_ Ausgabe \_ Schutz** Strukturen.</span><span class="sxs-lookup"><span data-stu-id="16348-106">The **DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS** structure holds an array of **DRM\_VIDEO\_OUTPUT\_PROTECTION** structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="16348-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="16348-107">Syntax</span></span>


```C++
typedef struct DRM_VIDEO_OUTPUT_PROTECTION_IDS {
  WORD                        cEntries;
  DRM_VIDEO_OUTPUT_PROTECTION *rgVop;
} ;
```



## <a name="members"></a><span data-ttu-id="16348-108">Member</span><span class="sxs-lookup"><span data-stu-id="16348-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="16348-109">**centries**</span><span class="sxs-lookup"><span data-stu-id="16348-109">**cEntries**</span></span>
</dt> <dd>

<span data-ttu-id="16348-110">Anzahl der Elemente in dem Array, auf das von **rgvop** verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="16348-110">Number of elements in the array referenced by **rgVop**.</span></span>

</dd> <dt>

<span data-ttu-id="16348-111">**rgvop**</span><span class="sxs-lookup"><span data-stu-id="16348-111">**rgVop**</span></span>
</dt> <dd>

<span data-ttu-id="16348-112">Die Adresse eines Arrays von **DRM- \_ Video- \_ ausgabeschutzstrukturen \_** .</span><span class="sxs-lookup"><span data-stu-id="16348-112">Address of an array of **DRM\_VIDEO\_OUTPUT\_PROTECTION** structures.</span></span> <span data-ttu-id="16348-113">**DRM \_ Der Video \_ Ausgabe \_ Schutz** ist ein Typ, der als [**DRM- \_ Ausgabe \_ Schutz**](drm-output-protection.md)definiert ist.</span><span class="sxs-lookup"><span data-stu-id="16348-113">**DRM\_VIDEO\_OUTPUT\_PROTECTION** is a type defined as [**DRM\_OUTPUT\_PROTECTION**](drm-output-protection.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="16348-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="16348-114">Remarks</span></span>

<span data-ttu-id="16348-115">Diese Struktur wird als Mitglied der [**DRM-Wiedergabe- \_ \_ OPL**](drmdrm-play-opl.md) -Struktur verwendet.</span><span class="sxs-lookup"><span data-stu-id="16348-115">This structure is used as a member of the [**DRM\_PLAY\_OPL**](drmdrm-play-opl.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="16348-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="16348-116">Requirements</span></span>



| <span data-ttu-id="16348-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="16348-117">Requirement</span></span> | <span data-ttu-id="16348-118">Wert</span><span class="sxs-lookup"><span data-stu-id="16348-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="16348-119">Header</span><span class="sxs-lookup"><span data-stu-id="16348-119">Header</span></span><br/> | <dl> <span data-ttu-id="16348-120"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="16348-120"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16348-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="16348-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16348-122">**DRM \_ - \_ Audioausgabe- \_ Schutz- \_ IDs**</span><span class="sxs-lookup"><span data-stu-id="16348-122">**DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS**</span></span>](drm-audio-output-protection-ids.md)
</dt> <dt>

[<span data-ttu-id="16348-123">**DRM- \_ Video- \_ Ausgabe Schutz- \_ \_ IDs \_ Ex**</span><span class="sxs-lookup"><span data-stu-id="16348-123">**DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS\_EX**</span></span>](drm-video-output-protection-ids-ex.md)
</dt> <dt>

[<span data-ttu-id="16348-124">**Strukturen**</span><span class="sxs-lookup"><span data-stu-id="16348-124">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





