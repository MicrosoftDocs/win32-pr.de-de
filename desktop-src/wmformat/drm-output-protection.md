---
title: DRM_OUTPUT_PROTECTION Struktur (wmdrmsdk. h)
description: Die DRM- \_ Ausgabe \_ Schutz Struktur enthält Informationen zu einer Ausgabe Schutz Technologie.
ms.assetid: e458013d-b77e-4e03-bff9-e3ecfc72ebdb
keywords:
- DRM_OUTPUT_PROTECTION Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
topic_type:
- apiref
api_name:
- DRM_OUTPUT_PROTECTION
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a10428d86503e952dc82a7d45bddc11f5dd1286
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371155"
---
# <a name="drm_output_protection-structure"></a><span data-ttu-id="49781-105">DRM- \_ Ausgabe \_ Schutz Struktur</span><span class="sxs-lookup"><span data-stu-id="49781-105">DRM\_OUTPUT\_PROTECTION structure</span></span>

<span data-ttu-id="49781-106">Die **DRM- \_ Ausgabe \_ Schutz** Struktur enthält Informationen zu einer Ausgabe Schutz Technologie.</span><span class="sxs-lookup"><span data-stu-id="49781-106">The **DRM\_OUTPUT\_PROTECTION** structure holds information about an output protection technology.</span></span>

## <a name="syntax"></a><span data-ttu-id="49781-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="49781-107">Syntax</span></span>


```C++
typedef struct DRM_OUTPUT_PROTECTION {
  GUID guidId;
  BYTE bConfigData;
} ;
```



## <a name="members"></a><span data-ttu-id="49781-108">Member</span><span class="sxs-lookup"><span data-stu-id="49781-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="49781-109">**guidid darf**</span><span class="sxs-lookup"><span data-stu-id="49781-109">**guidId**</span></span>
</dt> <dd>

<span data-ttu-id="49781-110">GUID, die die Ausgabe Schutz Technologie identifiziert.</span><span class="sxs-lookup"><span data-stu-id="49781-110">GUID identifying the output protection technology.</span></span>

</dd> <dt>

<span data-ttu-id="49781-111">**bconfigdata**</span><span class="sxs-lookup"><span data-stu-id="49781-111">**bConfigData**</span></span>
</dt> <dd>

<span data-ttu-id="49781-112">Konfigurationsdaten für die Technologie.</span><span class="sxs-lookup"><span data-stu-id="49781-112">Configuration data for the technology.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="49781-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="49781-113">Remarks</span></span>

<span data-ttu-id="49781-114">**DRM \_ Der \_ \_ audioausgabeschutz** und der **DRM- \_ Video \_ Ausgabe \_ Schutz** werden in **typedef** -Anweisungen als **DRM- \_ Ausgabe \_ Schutz** definiert.</span><span class="sxs-lookup"><span data-stu-id="49781-114">**DRM\_AUDIO\_OUTPUT\_PROTECTION** and **DRM\_VIDEO\_OUTPUT\_PROTECTION** are both defined as **DRM\_OUTPUT\_PROTECTION** in **typedef** statements.</span></span>

## <a name="requirements"></a><span data-ttu-id="49781-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="49781-115">Requirements</span></span>



| <span data-ttu-id="49781-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="49781-116">Requirement</span></span> | <span data-ttu-id="49781-117">Wert</span><span class="sxs-lookup"><span data-stu-id="49781-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="49781-118">Header</span><span class="sxs-lookup"><span data-stu-id="49781-118">Header</span></span><br/> | <dl> <span data-ttu-id="49781-119"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="49781-119"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49781-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="49781-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49781-121">**DRM- \_ Ausgabe \_ Schutz ( \_ Ex)**</span><span class="sxs-lookup"><span data-stu-id="49781-121">**DRM\_OUTPUT\_PROTECTION\_EX**</span></span>](drm-output-protection-ex.md)
</dt> <dt>

[<span data-ttu-id="49781-122">**Strukturen**</span><span class="sxs-lookup"><span data-stu-id="49781-122">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





