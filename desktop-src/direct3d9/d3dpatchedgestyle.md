---
description: Definiert, ob der aktuelle Mosaik Modus diskret oder kontinuierlich ist.
ms.assetid: d8055a25-6a8e-4018-a993-762f6f0e0cd3
title: D3DPATCHEDGESTYLE-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPATCHEDGESTYLE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e625b7c4ff12f9859efdcc2b10b551a2223adab6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870131"
---
# <a name="d3dpatchedgestyle-enumeration"></a><span data-ttu-id="34652-103">D3DPATCHEDGESTYLE-Enumeration</span><span class="sxs-lookup"><span data-stu-id="34652-103">D3DPATCHEDGESTYLE enumeration</span></span>

<span data-ttu-id="34652-104">Definiert, ob der aktuelle Mosaik Modus diskret oder kontinuierlich ist.</span><span class="sxs-lookup"><span data-stu-id="34652-104">Defines whether the current tessellation mode is discrete or continuous.</span></span>

## <a name="syntax"></a><span data-ttu-id="34652-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="34652-105">Syntax</span></span>


```C++
typedef enum D3DPATCHEDGESTYLE { 
  D3DPATCHEDGE_DISCRETE     = 0,
  D3DPATCHEDGE_CONTINUOUS   = 1,
  D3DPATCHEDGE_FORCE_DWORD  = 0x7fffffff
} D3DPATCHEDGESTYLE, *LPD3DPATCHEDGESTYLE;
```



## <a name="constants"></a><span data-ttu-id="34652-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="34652-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="34652-107"><span id="D3DPATCHEDGE_DISCRETE"></span><span id="d3dpatchedge_discrete"></span>**D3DPATCHEDGE \_ diskret**</span><span class="sxs-lookup"><span data-stu-id="34652-107"><span id="D3DPATCHEDGE_DISCRETE"></span><span id="d3dpatchedge_discrete"></span>**D3DPATCHEDGE\_DISCRETE**</span></span>
</dt> <dd>

<span data-ttu-id="34652-108">Diskreter Randstil.</span><span class="sxs-lookup"><span data-stu-id="34652-108">Discrete edge style.</span></span> <span data-ttu-id="34652-109">Im diskreten Modus können Sie das%%%%%%%%%%%%%%%%%%%%%%%%</span><span class="sxs-lookup"><span data-stu-id="34652-109">In discrete mode, you can specify float tessellation but it will be truncated to integers.</span></span>

</dd> <dt>

<span data-ttu-id="34652-110"><span id="D3DPATCHEDGE_CONTINUOUS"></span><span id="d3dpatchedge_continuous"></span>**D3DPATCHEDGE \_ fortlaufend**</span><span class="sxs-lookup"><span data-stu-id="34652-110"><span id="D3DPATCHEDGE_CONTINUOUS"></span><span id="d3dpatchedge_continuous"></span>**D3DPATCHEDGE\_CONTINUOUS**</span></span>
</dt> <dd>

<span data-ttu-id="34652-111">Fortlaufender Edge-Stil.</span><span class="sxs-lookup"><span data-stu-id="34652-111">Continuous edge style.</span></span> <span data-ttu-id="34652-112">Im kontinuierlichen Modus wird das Mosaik als float-Werte angegeben, die problemlos variieren können, um "Popping"-Artefakte zu verringern.</span><span class="sxs-lookup"><span data-stu-id="34652-112">In continuous mode, tessellation is specified as float values that can be smoothly varied to reduce "popping" artifacts.</span></span>

</dd> <dt>

<span data-ttu-id="34652-113"><span id="D3DPATCHEDGE_FORCE_DWORD"></span><span id="d3dpatchedge_force_dword"></span>**D3DPATCHEDGE \_ Erzwingen von \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="34652-113"><span id="D3DPATCHEDGE_FORCE_DWORD"></span><span id="d3dpatchedge_force_dword"></span>**D3DPATCHEDGE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="34652-114">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="34652-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="34652-115">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="34652-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="34652-116">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="34652-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="34652-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="34652-117">Remarks</span></span>

<span data-ttu-id="34652-118">Beachten Sie, dass das kontinuierliche Mosaik Modell ein vollkommen anderes Mosaikmuster als das diskrete Mosaikmuster für die gleichen Mosaik Werte erzeugt (Dies ist im Draht Modell deutlicher erkennbar).</span><span class="sxs-lookup"><span data-stu-id="34652-118">Note that continuous tessellation produces a completely different tessellation pattern from the discrete one for the same tessellation values (this is more apparent in wireframe mode).</span></span> <span data-ttu-id="34652-119">Daher ist 4,0 Continuous nicht mit 4 diskret identisch.</span><span class="sxs-lookup"><span data-stu-id="34652-119">Thus, 4.0 continuous is not the same as 4 discrete.</span></span>

## <a name="requirements"></a><span data-ttu-id="34652-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="34652-120">Requirements</span></span>



| <span data-ttu-id="34652-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="34652-121">Requirement</span></span> | <span data-ttu-id="34652-122">Wert</span><span class="sxs-lookup"><span data-stu-id="34652-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="34652-123">Header</span><span class="sxs-lookup"><span data-stu-id="34652-123">Header</span></span><br/> | <dl> <span data-ttu-id="34652-124"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="34652-124"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34652-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34652-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34652-126">Direct3D-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="34652-126">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




