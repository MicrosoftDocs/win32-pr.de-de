---
title: DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX Struktur (wmdrmsdk. h)
description: Die DRM- \_ Video- \_ Ausgabe Schutz- \_ \_ IDs in der Struktur enthalten \_ ein Array von DRM- \_ Video- \_ Ausgabe \_ Schutzstrukturen.
ms.assetid: 89de0ade-fa86-4081-b65b-9c84fb68cf3d
keywords:
- DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
topic_type:
- apiref
api_name:
- DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2e7cc5ec0b4b14d88deb317e62e3e1cd4f92b57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106350751"
---
# <a name="drm_video_output_protection_ids_ex-structure"></a><span data-ttu-id="f428f-105">DRM- \_ Video- \_ Ausgabe Schutz- \_ \_ IDs Ex- \_ Struktur</span><span class="sxs-lookup"><span data-stu-id="f428f-105">DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS\_EX structure</span></span>

<span data-ttu-id="f428f-106">Die **DRM- \_ Video- \_ Ausgabe Schutz- \_ \_ IDs \_** in der Struktur enthalten ein Array von **DRM-Video- \_ \_ Ausgabe \_ Schutz** Strukturen.</span><span class="sxs-lookup"><span data-stu-id="f428f-106">The **DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS\_EX** structure holds an array of **DRM\_VIDEO\_OUTPUT\_PROTECTION** structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="f428f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f428f-107">Syntax</span></span>


```C++
typedef struct DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX {
  DWORD                          dwVersion;
  WORD                           cEntries;
  DRM_VIDEO_OUTPUT_PROTECTION_EX *rgVop;
} ;
```



## <a name="members"></a><span data-ttu-id="f428f-108">Member</span><span class="sxs-lookup"><span data-stu-id="f428f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="f428f-109">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="f428f-109">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="f428f-110">Versionsnummer:</span><span class="sxs-lookup"><span data-stu-id="f428f-110">Version number.</span></span>

</dd> <dt>

<span data-ttu-id="f428f-111">**centries**</span><span class="sxs-lookup"><span data-stu-id="f428f-111">**cEntries**</span></span>
</dt> <dd>

<span data-ttu-id="f428f-112">Anzahl der Elemente in dem Array, auf das von **rgvop** verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="f428f-112">Number of elements in the array referenced by **rgVop**.</span></span>

</dd> <dt>

<span data-ttu-id="f428f-113">**rgvop**</span><span class="sxs-lookup"><span data-stu-id="f428f-113">**rgVop**</span></span>
</dt> <dd>

<span data-ttu-id="f428f-114">Adresse eines Arrays von **DRM- \_ Video- \_ Ausgabe Schutz- \_ \_ Ex** -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="f428f-114">Address of an array of **DRM\_VIDEO\_OUTPUT\_PROTECTION\_EX** structures.</span></span> <span data-ttu-id="f428f-115">**DRM \_ Der Video- \_ Ausgabe \_ Schutz \_ Ex** ist ein Typ, der als [**DRM- \_ Ausgabe \_ Schutz \_ Ex**](drm-output-protection-ex.md)definiert ist.</span><span class="sxs-lookup"><span data-stu-id="f428f-115">**DRM\_VIDEO\_OUTPUT\_PROTECTION\_EX** is a type defined as [**DRM\_OUTPUT\_PROTECTION\_EX**](drm-output-protection-ex.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f428f-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f428f-116">Remarks</span></span>

<span data-ttu-id="f428f-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="f428f-117">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="f428f-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f428f-118">Requirements</span></span>



| <span data-ttu-id="f428f-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f428f-119">Requirement</span></span> | <span data-ttu-id="f428f-120">Wert</span><span class="sxs-lookup"><span data-stu-id="f428f-120">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f428f-121">Header</span><span class="sxs-lookup"><span data-stu-id="f428f-121">Header</span></span><br/> | <dl> <span data-ttu-id="f428f-122"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="f428f-122"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f428f-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f428f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f428f-124">**DRM \_ - \_ audioausgabeschutz- \_ \_ IDs \_ Ex**</span><span class="sxs-lookup"><span data-stu-id="f428f-124">**DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS\_EX**</span></span>](drm-audio-output-protection-ids-ex.md)
</dt> <dt>

[<span data-ttu-id="f428f-125">**DRM- \_ Video- \_ Ausgabe Schutz- \_ \_ IDs**</span><span class="sxs-lookup"><span data-stu-id="f428f-125">**DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS**</span></span>](drmdrm-video-output-protection-ids.md)
</dt> <dt>

[<span data-ttu-id="f428f-126">**Strukturen**</span><span class="sxs-lookup"><span data-stu-id="f428f-126">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





