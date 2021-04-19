---
title: DRM_OPL_OUTPUT_IDS Struktur (wmdrmsdk. h)
description: Die Struktur der DRM- \_ OPL- \_ Ausgabe- \_ IDs enthält eine Reihe von OPL-Ausgabe bezeichlern (Output Protection Level).
ms.assetid: 3627f2a7-1cea-400b-82e7-678898ccc386
keywords:
- DRM_OPL_OUTPUT_IDS Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
topic_type:
- apiref
api_name:
- DRM_OPL_OUTPUT_IDS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 802787c5e373c837d639e0225bf650d80c105970
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365532"
---
# <a name="drm_opl_output_ids-structure"></a><span data-ttu-id="380ee-105">Struktur der DRM- \_ OPL- \_ Ausgabe- \_ IDs</span><span class="sxs-lookup"><span data-stu-id="380ee-105">DRM\_OPL\_OUTPUT\_IDS structure</span></span>

<span data-ttu-id="380ee-106">Die Struktur der **DRM- \_ OPL- \_ Ausgabe- \_ IDs** enthält eine Reihe von OPL-Ausgabe bezeichlern (Output Protection Level).</span><span class="sxs-lookup"><span data-stu-id="380ee-106">The **DRM\_OPL\_OUTPUT\_IDS** structure holds a number of output protection level (OPL) output identifiers.</span></span>

## <a name="syntax"></a><span data-ttu-id="380ee-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="380ee-107">Syntax</span></span>


```C++
typedef struct DRM_OPL_OUTPUT_IDS {
  WORD cIds;
  GUID *rgIds;
} ;
```



## <a name="members"></a><span data-ttu-id="380ee-108">Member</span><span class="sxs-lookup"><span data-stu-id="380ee-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="380ee-109">**cIds**</span><span class="sxs-lookup"><span data-stu-id="380ee-109">**cIds**</span></span>
</dt> <dd>

<span data-ttu-id="380ee-110">Anzahl der Bezeichner in dem Array, auf das von **rgids** verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="380ee-110">Number of identifiers in the array referenced by **rgIds**.</span></span>

</dd> <dt>

<span data-ttu-id="380ee-111">**rgids**</span><span class="sxs-lookup"><span data-stu-id="380ee-111">**rgIds**</span></span>
</dt> <dd>

<span data-ttu-id="380ee-112">Adresse eines Arrays von GUIDs.</span><span class="sxs-lookup"><span data-stu-id="380ee-112">Address of an array of GUIDs.</span></span> <span data-ttu-id="380ee-113">Jeder Member des Arrays enthält einen OPL-Ausgabe Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="380ee-113">Each member of the array contains an OPL output identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="380ee-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="380ee-114">Remarks</span></span>

<span data-ttu-id="380ee-115">Diese Struktur wird als Mitglied der [**DRM-Kopier- \_ \_ OPL**](drmdrm-copy-opl.md) -und [**DRM \_ Play \_ OPL**](drmdrm-play-opl.md) -Strukturen verwendet, um Gruppen von Ausgabe bezeichatoren zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="380ee-115">This structure is used as a member of the [**DRM\_COPY\_OPL**](drmdrm-copy-opl.md) and [**DRM\_PLAY\_OPL**](drmdrm-play-opl.md) structures to identify groups of output identifiers.</span></span>

## <a name="requirements"></a><span data-ttu-id="380ee-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="380ee-116">Requirements</span></span>



| <span data-ttu-id="380ee-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="380ee-117">Requirement</span></span> | <span data-ttu-id="380ee-118">Wert</span><span class="sxs-lookup"><span data-stu-id="380ee-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="380ee-119">Header</span><span class="sxs-lookup"><span data-stu-id="380ee-119">Header</span></span><br/> | <dl> <span data-ttu-id="380ee-120"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="380ee-120"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="380ee-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="380ee-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="380ee-122">**Strukturen**</span><span class="sxs-lookup"><span data-stu-id="380ee-122">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





