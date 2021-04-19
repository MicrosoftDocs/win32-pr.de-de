---
description: Vertex-Cache Optimierungs Hinweise.
ms.assetid: 891624cd-03dd-4ddd-93f5-4899e1470325
title: D3DDEVINFO_VCACHE-Struktur (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_VCACHE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 80870c330adf185a869ac5e3543055c82fc7115c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367357"
---
# <a name="d3ddevinfo_vcache-structure"></a><span data-ttu-id="887d3-103">D3DDEVINFO \_ VCACHE-Struktur</span><span class="sxs-lookup"><span data-stu-id="887d3-103">D3DDEVINFO\_VCACHE structure</span></span>

<span data-ttu-id="887d3-104">Vertex-Cache Optimierungs Hinweise.</span><span class="sxs-lookup"><span data-stu-id="887d3-104">Vertex cache optimization hints.</span></span>

## <a name="syntax"></a><span data-ttu-id="887d3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="887d3-105">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_VCACHE {
  DWORD Pattern;
  DWORD OptMethod;
  DWORD CacheSize;
  DWORD MagicNumber;
} D3DDEVINFO_VCACHE, *LPD3DDEVINFO_VCACHE;
```



## <a name="members"></a><span data-ttu-id="887d3-106">Member</span><span class="sxs-lookup"><span data-stu-id="887d3-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="887d3-107">**Muster**</span><span class="sxs-lookup"><span data-stu-id="887d3-107">**Pattern**</span></span>
</dt> <dd>

<span data-ttu-id="887d3-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="887d3-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="887d3-109">Bitmuster.</span><span class="sxs-lookup"><span data-stu-id="887d3-109">Bit pattern.</span></span> <span data-ttu-id="887d3-110">Der Rückgabewert muss "FourCC" ("c", "A", "c", "H") sein.</span><span class="sxs-lookup"><span data-stu-id="887d3-110">Return value must be the FOURCC ('C', 'A', 'C', 'H').</span></span>

</dd> <dt>

<span data-ttu-id="887d3-111">**Optmethod**</span><span class="sxs-lookup"><span data-stu-id="887d3-111">**OptMethod**</span></span>
</dt> <dd>

<span data-ttu-id="887d3-112">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="887d3-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="887d3-113">Optimierungsmethode.</span><span class="sxs-lookup"><span data-stu-id="887d3-113">Optimizations method.</span></span> <span data-ttu-id="887d3-114">Verwenden Sie 0, um die längsten Striche zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="887d3-114">Use 0 to get the longest strips.</span></span> <span data-ttu-id="887d3-115">Verwenden Sie 1, um die Vertex-Cache Verwendung zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="887d3-115">Use 1 to optimize the vertex cache usage.</span></span>

</dd> <dt>

<span data-ttu-id="887d3-116">**CacheSize**</span><span class="sxs-lookup"><span data-stu-id="887d3-116">**CacheSize**</span></span>
</dt> <dd>

<span data-ttu-id="887d3-117">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="887d3-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="887d3-118">Cache Größe, die als Ziel für die Optimierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="887d3-118">Cache size used as a target for optimization.</span></span> <span data-ttu-id="887d3-119">Dies ist nur erforderlich, wenn optmethod den Wert 1 hat.</span><span class="sxs-lookup"><span data-stu-id="887d3-119">This is required only if OptMethod is 1.</span></span>

</dd> <dt>

<span data-ttu-id="887d3-120">**MagicNumber**</span><span class="sxs-lookup"><span data-stu-id="887d3-120">**MagicNumber**</span></span>
</dt> <dd>

<span data-ttu-id="887d3-121">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="887d3-121">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="887d3-122">Wird von internen Optimierungsmethoden verwendet, um zu bestimmen, wann Striche neu gestartet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="887d3-122">Used by internal optimization methods to determine when to restart strips.</span></span> <span data-ttu-id="887d3-123">Dies kann von einem Benutzer nicht festgelegt oder geändert werden.</span><span class="sxs-lookup"><span data-stu-id="887d3-123">This cannot be set or modified by a user.</span></span> <span data-ttu-id="887d3-124">Dies ist nur erforderlich, wenn optmethod den Wert 1 hat.</span><span class="sxs-lookup"><span data-stu-id="887d3-124">This is required only if OptMethod is 1.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="887d3-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="887d3-125">Requirements</span></span>



| <span data-ttu-id="887d3-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="887d3-126">Requirement</span></span> | <span data-ttu-id="887d3-127">Wert</span><span class="sxs-lookup"><span data-stu-id="887d3-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="887d3-128">Header</span><span class="sxs-lookup"><span data-stu-id="887d3-128">Header</span></span><br/> | <dl> <span data-ttu-id="887d3-129"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="887d3-129"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="887d3-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="887d3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="887d3-131">Direct3D-Strukturen</span><span class="sxs-lookup"><span data-stu-id="887d3-131">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="887d3-132">**GetData**</span><span class="sxs-lookup"><span data-stu-id="887d3-132">**GetData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
