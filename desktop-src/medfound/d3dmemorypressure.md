---
description: Diese Struktur enthält Daten für die Arbeitsspeicher Auslastung.
ms.assetid: 42cf0922-53cc-48b9-8359-b88583ef5f1c
title: D3DMEMORYPRESSURE-Struktur (D3d9types. h) für Microsoft Media Foundation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMEMORYPRESSURE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 7400c4822b61a84ab288f0424cfa84e825e69dc9
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "106371590"
---
# <a name="d3dmemorypressure-structure-d3d9typesh-for-microsoft-media-foundation"></a><span data-ttu-id="8394c-103">D3DMEMORYPRESSURE-Struktur (D3d9types. h) für Microsoft Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8394c-103">D3DMEMORYPRESSURE structure (D3d9types.h) for Microsoft Media Foundation</span></span>

<span data-ttu-id="8394c-104">Enthält Daten für die Arbeitsspeicher Auslastung.</span><span class="sxs-lookup"><span data-stu-id="8394c-104">Contains data for memory pressure reporting.</span></span>

## <a name="syntax"></a><span data-ttu-id="8394c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8394c-105">Syntax</span></span>


```C++
typedef struct _D3DMEMORYPRESSURE {
  UINT64 BytesEvictedFromProcess;
  UINT64 SizeOfInefficientAllocation;
  DWORD  LevelOfEfficiency;
} D3DMEMORYPRESSURE;
```



## <a name="members"></a><span data-ttu-id="8394c-106">Member</span><span class="sxs-lookup"><span data-stu-id="8394c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8394c-107">**Bytesevictedfromprocess**</span><span class="sxs-lookup"><span data-stu-id="8394c-107">**BytesEvictedFromProcess**</span></span>
</dt> <dd>

<span data-ttu-id="8394c-108">Die Anzahl der Bytes, die während der Abfrage Dauer vom Prozess entfernt wurden.</span><span class="sxs-lookup"><span data-stu-id="8394c-108">The number of bytes that were evicted by the process during the duration of the query.</span></span>

</dd> <dt>

<span data-ttu-id="8394c-109">**Sizeofinefficientallocation**</span><span class="sxs-lookup"><span data-stu-id="8394c-109">**SizeOfInefficientAllocation**</span></span>
</dt> <dd>

<span data-ttu-id="8394c-110">Die Gesamtanzahl der Bytes, die in nicht optimalen Speicher Segmenten abgelegt werden, aufgrund unzureichenden Speicherplatzes innerhalb der bevorzugten Speichersegmente.</span><span class="sxs-lookup"><span data-stu-id="8394c-110">The total number of bytes placed in nonoptimal memory segments, due to inadequate space within the preferred memory segments.</span></span>

</dd> <dt>

<span data-ttu-id="8394c-111">**Levelofefficiency**</span><span class="sxs-lookup"><span data-stu-id="8394c-111">**LevelOfEfficiency**</span></span>
</dt> <dd>

<span data-ttu-id="8394c-112">Die Gesamteffizienz der Speicher Belegungen, die im nicht optimalen Arbeitsspeicher platziert wurden.</span><span class="sxs-lookup"><span data-stu-id="8394c-112">The overall efficiency of the memory allocations that were placed in nonoptimal memory.</span></span> <span data-ttu-id="8394c-113">Der Wert wird als Prozentsatz ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="8394c-113">The value is expressed as a percentage.</span></span> <span data-ttu-id="8394c-114">Der Wert 95 gibt beispielsweise an, dass die in nicht bevorzugten Speicher Segmenten platzierten Zuordnungen 95% effizient sind.</span><span class="sxs-lookup"><span data-stu-id="8394c-114">For example, the value 95 indicates that the allocations placed in nonpreferred memory segments are 95% efficient.</span></span> <span data-ttu-id="8394c-115">Diese Zahl sollte nicht als exakte Messung angesehen werden.</span><span class="sxs-lookup"><span data-stu-id="8394c-115">This number should not be considered an exact measurement.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8394c-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8394c-116">Requirements</span></span>



| <span data-ttu-id="8394c-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8394c-117">Requirement</span></span> | <span data-ttu-id="8394c-118">Wert</span><span class="sxs-lookup"><span data-stu-id="8394c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8394c-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8394c-119">Minimum supported client</span></span> | <span data-ttu-id="8394c-120">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8394c-120">Windows 7 \[desktop apps only\]</span></span>                                                              |
| <span data-ttu-id="8394c-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8394c-121">Minimum supported server</span></span> | <span data-ttu-id="8394c-122">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8394c-122">Windows Server 2008 R2 \[desktop apps only\]</span></span>                                                 |
| <span data-ttu-id="8394c-123">Header</span><span class="sxs-lookup"><span data-stu-id="8394c-123">Header</span></span>                  | <span data-ttu-id="8394c-124">D3d9types. h (Include d3d9. h)</span><span class="sxs-lookup"><span data-stu-id="8394c-124">D3d9types.h (include D3d9.h)</span></span> |



## <a name="see-also"></a><span data-ttu-id="8394c-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8394c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8394c-126">Direct3D-Video Strukturen</span><span class="sxs-lookup"><span data-stu-id="8394c-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="8394c-127">Berichterstellung für Speicherauslastung</span><span class="sxs-lookup"><span data-stu-id="8394c-127">Memory Pressure Reporting</span></span>](memory-pressure-reporting.md)
</dt> </dl>

 

 




