---
title: DRM_OUTPUT_PROTECTION_EX Struktur (wmdrmsdk. h)
description: Die DRM- \_ Ausgabe \_ Schutz-Ex- \_ Struktur enthält Informationen zu einer Ausgabe Schutz Technologie. Diese Struktur erweitert den DRM- \_ Ausgabe \_ Schutz durch Hinzufügen einer Versionsnummer.
ms.assetid: eeebf5da-172b-4781-8c44-00504a6961bf
keywords:
- DRM_OUTPUT_PROTECTION_EX Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
topic_type:
- apiref
api_name:
- DRM_OUTPUT_PROTECTION_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aeadbb845dc115b1faff858fe3a6ba0064eb425e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371758"
---
# <a name="drm_output_protection_ex-structure"></a><span data-ttu-id="9b2d5-106">DRM- \_ Ausgabe \_ Schutz-Ex- \_ Struktur</span><span class="sxs-lookup"><span data-stu-id="9b2d5-106">DRM\_OUTPUT\_PROTECTION\_EX structure</span></span>

<span data-ttu-id="9b2d5-107">Die **DRM- \_ Ausgabe \_ Schutz- \_ Ex** -Struktur enthält Informationen zu einer Ausgabe Schutz Technologie.</span><span class="sxs-lookup"><span data-stu-id="9b2d5-107">The **DRM\_OUTPUT\_PROTECTION\_EX** structure holds information about an output protection technology.</span></span> <span data-ttu-id="9b2d5-108">Diese Struktur erweitert den **DRM- \_ Ausgabe \_ Schutz** durch Hinzufügen einer Versionsnummer.</span><span class="sxs-lookup"><span data-stu-id="9b2d5-108">This structure extends **DRM\_OUTPUT\_PROTECTION** by adding a version number.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b2d5-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b2d5-109">Syntax</span></span>


```C++
typedef struct DRM_OUTPUT_PROTECTION_EX {
  DWORD dwVersion;
  GUID  guidId;
  DWORD dwConfigData;
} ;
```



## <a name="members"></a><span data-ttu-id="9b2d5-110">Member</span><span class="sxs-lookup"><span data-stu-id="9b2d5-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="9b2d5-111">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="9b2d5-111">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="9b2d5-112">Versionsnummer:</span><span class="sxs-lookup"><span data-stu-id="9b2d5-112">Version number.</span></span>

</dd> <dt>

<span data-ttu-id="9b2d5-113">**guidid darf**</span><span class="sxs-lookup"><span data-stu-id="9b2d5-113">**guidId**</span></span>
</dt> <dd>

<span data-ttu-id="9b2d5-114">GUID, die die Ausgabe Schutz Technologie identifiziert.</span><span class="sxs-lookup"><span data-stu-id="9b2d5-114">GUID identifying the output protection technology.</span></span>

</dd> <dt>

<span data-ttu-id="9b2d5-115">**dwconfigdata**</span><span class="sxs-lookup"><span data-stu-id="9b2d5-115">**dwConfigData**</span></span>
</dt> <dd>

<span data-ttu-id="9b2d5-116">Konfigurationsdaten für die Technologie.</span><span class="sxs-lookup"><span data-stu-id="9b2d5-116">Configuration data for the technology.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9b2d5-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9b2d5-117">Remarks</span></span>

<span data-ttu-id="9b2d5-118">**DRM \_ Der \_ audioausgabeschutz \_ \_ Ex** und der **DRM-Video-Ausgabe Schutz \_ \_ \_ \_ Ex** sind beide als **DRM- \_ Ausgabe \_ Schutz** in **typedef** -Anweisungen definiert.</span><span class="sxs-lookup"><span data-stu-id="9b2d5-118">**DRM\_AUDIO\_OUTPUT\_PROTECTION\_EX** and **DRM\_VIDEO\_OUTPUT\_PROTECTION\_EX** are both defined as **DRM\_OUTPUT\_PROTECTION** in **typedef** statements.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b2d5-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9b2d5-119">Requirements</span></span>



| <span data-ttu-id="9b2d5-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9b2d5-120">Requirement</span></span> | <span data-ttu-id="9b2d5-121">Wert</span><span class="sxs-lookup"><span data-stu-id="9b2d5-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9b2d5-122">Header</span><span class="sxs-lookup"><span data-stu-id="9b2d5-122">Header</span></span><br/> | <dl> <span data-ttu-id="9b2d5-123"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b2d5-123"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b2d5-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9b2d5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b2d5-125">**DRM- \_ Ausgabe \_ Schutz**</span><span class="sxs-lookup"><span data-stu-id="9b2d5-125">**DRM\_OUTPUT\_PROTECTION**</span></span>](drm-output-protection.md)
</dt> <dt>

[<span data-ttu-id="9b2d5-126">**Strukturen**</span><span class="sxs-lookup"><span data-stu-id="9b2d5-126">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





