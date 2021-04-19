---
description: Enthält Daten für die Arbeitsspeicher Auslastung.
ms.assetid: bdf65d35-281f-4795-a2c1-0d4e91bfa7bc
title: D3DMEMORYPRESSURE-Struktur (D3d9types. h)
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
ms.openlocfilehash: 5917d1e61817f401106ae14aa5a0f98cd75b0d42
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363150"
---
# <a name="d3dmemorypressure-structure-d3d9typesh"></a><span data-ttu-id="1ab0f-103">D3DMEMORYPRESSURE-Struktur (D3d9types. h)</span><span class="sxs-lookup"><span data-stu-id="1ab0f-103">D3DMEMORYPRESSURE structure (D3d9types.h)</span></span>

<span data-ttu-id="1ab0f-104">Enthält Daten für die Arbeitsspeicher Auslastung.</span><span class="sxs-lookup"><span data-stu-id="1ab0f-104">Contains data for memory pressure reporting.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ab0f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ab0f-105">Syntax</span></span>


```C++
typedef struct _D3DMEMORYPRESSURE {
  UINT64 BytesEvictedFromProcess;
  UINT64 SizeOfInefficientAllocation;
  DWORD  LevelOfEfficiency;
} D3DMEMORYPRESSURE;
```



## <a name="members"></a><span data-ttu-id="1ab0f-106">Member</span><span class="sxs-lookup"><span data-stu-id="1ab0f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1ab0f-107">**Bytesevictedfromprocess**</span><span class="sxs-lookup"><span data-stu-id="1ab0f-107">**BytesEvictedFromProcess**</span></span>
</dt> <dd>

<span data-ttu-id="1ab0f-108">Typ: **[ **UINT64**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ab0f-108">Type: **[**UINT64**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1ab0f-109">Die Anzahl der Bytes, die während der Abfrage Dauer vom Prozess entfernt wurden.</span><span class="sxs-lookup"><span data-stu-id="1ab0f-109">The number of bytes that were evicted by the process during the duration of the query.</span></span>

</dd> <dt>

<span data-ttu-id="1ab0f-110">**Sizeofinefficientallocation**</span><span class="sxs-lookup"><span data-stu-id="1ab0f-110">**SizeOfInefficientAllocation**</span></span>
</dt> <dd>

<span data-ttu-id="1ab0f-111">Typ: **[ **UINT64**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ab0f-111">Type: **[**UINT64**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1ab0f-112">Die Gesamtanzahl der Bytes, die in nicht optimalen Speicher Segmenten abgelegt werden, aufgrund unzureichenden Speicherplatzes innerhalb der bevorzugten Speichersegmente.</span><span class="sxs-lookup"><span data-stu-id="1ab0f-112">The total number of bytes placed in nonoptimal memory segments, due to inadequate space within the preferred memory segments.</span></span>

</dd> <dt>

<span data-ttu-id="1ab0f-113">**Levelofefficiency**</span><span class="sxs-lookup"><span data-stu-id="1ab0f-113">**LevelOfEfficiency**</span></span>
</dt> <dd>

<span data-ttu-id="1ab0f-114">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ab0f-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1ab0f-115">Die Gesamteffizienz der Speicher Belegungen, die im nicht optimalen Arbeitsspeicher platziert wurden.</span><span class="sxs-lookup"><span data-stu-id="1ab0f-115">The overall efficiency of the memory allocations that were placed in nonoptimal memory.</span></span> <span data-ttu-id="1ab0f-116">Der Wert wird als Prozentsatz ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="1ab0f-116">The value is expressed as a percentage.</span></span> <span data-ttu-id="1ab0f-117">Der Wert 95 gibt beispielsweise an, dass die in nicht bevorzugten Speicher Segmenten platzierten Zuordnungen 95% effizient sind.</span><span class="sxs-lookup"><span data-stu-id="1ab0f-117">For example, the value 95 indicates that the allocations placed in nonpreferred memory segments are 95% efficient.</span></span> <span data-ttu-id="1ab0f-118">Diese Zahl sollte nicht als exakte Messung angesehen werden.</span><span class="sxs-lookup"><span data-stu-id="1ab0f-118">This number should not be considered an exact measurement.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1ab0f-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1ab0f-119">Requirements</span></span>



| <span data-ttu-id="1ab0f-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1ab0f-120">Requirement</span></span> | <span data-ttu-id="1ab0f-121">Wert</span><span class="sxs-lookup"><span data-stu-id="1ab0f-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ab0f-122">Header</span><span class="sxs-lookup"><span data-stu-id="1ab0f-122">Header</span></span><br/> | <dl> <span data-ttu-id="1ab0f-123"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ab0f-123"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ab0f-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ab0f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ab0f-125">Direct3D-Strukturen</span><span class="sxs-lookup"><span data-stu-id="1ab0f-125">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
