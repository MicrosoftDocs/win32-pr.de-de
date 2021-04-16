---
description: Definiert den Prioritäts Typen, dem eine Animations Spur zugewiesen wird.
ms.assetid: 7bd83e31-09c4-4376-a22d-ed8023b78e84
title: D3DXPRIORITY_TYPE-Enumeration (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPRIORITY_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 5e6d82807cbd0e93e7a1127db80726c0ec06b5da
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394109"
---
# <a name="d3dxpriority_type-enumeration"></a><span data-ttu-id="86aed-103">D3DXPRIORITY- \_ Typenumeration</span><span class="sxs-lookup"><span data-stu-id="86aed-103">D3DXPRIORITY\_TYPE enumeration</span></span>

<span data-ttu-id="86aed-104">Definiert den Prioritäts Typen, dem eine Animations Spur zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="86aed-104">Defines the priority type to which an animation track is assigned.</span></span>

## <a name="syntax"></a><span data-ttu-id="86aed-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="86aed-105">Syntax</span></span>


```C++
typedef enum D3DXPRIORITY_TYPE { 
  D3DXPRIORITY_LOW          = 0,
  D3DXPRIORITY_HIGH         = 1,
  D3DXPRIORITY_FORCE_DWORD  = 0x7fffffff
} D3DXPRIORITY_TYPE, *LPD3DXPRIORITY_TYPE;
```



## <a name="constants"></a><span data-ttu-id="86aed-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="86aed-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="86aed-107"><span id="D3DXPRIORITY_LOW"></span><span id="d3dxpriority_low"></span>**D3DXPRIORITY \_ niedrig**</span><span class="sxs-lookup"><span data-stu-id="86aed-107"><span id="D3DXPRIORITY_LOW"></span><span id="d3dxpriority_low"></span>**D3DXPRIORITY\_LOW**</span></span>
</dt> <dd>

<span data-ttu-id="86aed-108">Die Nachverfolgung sollte mit allen Spuren mit niedriger Priorität gemischt werden, bevor die Blend-Mischung mit niedriger Priorität mit der Mischung mit hoher Priorität gemischt wird.</span><span class="sxs-lookup"><span data-stu-id="86aed-108">Track should be blended with all the low-priority tracks before the low-priority blend is mixed with the high-priority blend.</span></span>

</dd> <dt>

<span data-ttu-id="86aed-109"><span id="D3DXPRIORITY_HIGH"></span><span id="d3dxpriority_high"></span>**D3DXPRIORITY \_ hoch**</span><span class="sxs-lookup"><span data-stu-id="86aed-109"><span id="D3DXPRIORITY_HIGH"></span><span id="d3dxpriority_high"></span>**D3DXPRIORITY\_HIGH**</span></span>
</dt> <dd>

<span data-ttu-id="86aed-110">Die Nachverfolgung sollte mit allen Titeln mit hoher Priorität gemischt werden, bevor die Blend-Mischung mit hoher Priorität mit der Mischung mit niedriger Priorität gemischt wird.</span><span class="sxs-lookup"><span data-stu-id="86aed-110">Track should be blended with all the high-priority tracks before the high-priority blend is mixed with the low-priority blend.</span></span>

</dd> <dt>

<span data-ttu-id="86aed-111"><span id="D3DXPRIORITY_FORCE_DWORD"></span><span id="d3dxpriority_force_dword"></span>**D3DXPRIORITY \_ Erzwingen von \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="86aed-111"><span id="D3DXPRIORITY_FORCE_DWORD"></span><span id="d3dxpriority_force_dword"></span>**D3DXPRIORITY\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="86aed-112">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="86aed-112">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="86aed-113">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="86aed-113">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="86aed-114">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="86aed-114">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="86aed-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="86aed-115">Remarks</span></span>

<span data-ttu-id="86aed-116">Spuren mit der gleichen Priorität werden kombiniert, und die beiden resultierenden Werte werden dann mithilfe des Prioritäts-Blend-Faktors gemischt.</span><span class="sxs-lookup"><span data-stu-id="86aed-116">Tracks with the same priority are blended together, and the two resulting values are then blended using the priority blend factor.</span></span>

## <a name="requirements"></a><span data-ttu-id="86aed-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="86aed-117">Requirements</span></span>



| <span data-ttu-id="86aed-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="86aed-118">Requirement</span></span> | <span data-ttu-id="86aed-119">Wert</span><span class="sxs-lookup"><span data-stu-id="86aed-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="86aed-120">Header</span><span class="sxs-lookup"><span data-stu-id="86aed-120">Header</span></span><br/> | <dl> <span data-ttu-id="86aed-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="86aed-121"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86aed-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="86aed-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86aed-123">D3DX-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="86aed-123">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




