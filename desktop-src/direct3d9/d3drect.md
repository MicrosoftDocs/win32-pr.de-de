---
description: Definiert ein Rechteck.
ms.assetid: a8590411-fd34-4048-a41f-b4155d955573
title: D3DRECT-Struktur (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRECT
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 9a22b74869afa16ca0c55ac50975eb36ba590c7a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762099"
---
# <a name="d3drect-structure"></a><span data-ttu-id="80c4d-103">D3DRECT-Struktur</span><span class="sxs-lookup"><span data-stu-id="80c4d-103">D3DRECT structure</span></span>

<span data-ttu-id="80c4d-104">Definiert ein Rechteck.</span><span class="sxs-lookup"><span data-stu-id="80c4d-104">Defines a rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="80c4d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="80c4d-105">Syntax</span></span>


```C++
typedef struct D3DRECT {
  LONG x1;
  LONG y1;
  LONG x2;
  LONG y2;
} D3DRECT;
```



## <a name="members"></a><span data-ttu-id="80c4d-106">Member</span><span class="sxs-lookup"><span data-stu-id="80c4d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="80c4d-107">**x1**</span><span class="sxs-lookup"><span data-stu-id="80c4d-107">**x1**</span></span>
</dt> <dd>

<span data-ttu-id="80c4d-108">Type: **[ **Long**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="80c4d-108">Type: **[**LONG**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="80c4d-109">Die x-Koordinate der linken oberen Ecke des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="80c4d-109">The x-coordinate of the upper-left corner of the rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="80c4d-110">**y1**</span><span class="sxs-lookup"><span data-stu-id="80c4d-110">**y1**</span></span>
</dt> <dd>

<span data-ttu-id="80c4d-111">Type: **[ **Long**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="80c4d-111">Type: **[**LONG**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="80c4d-112">Die y-Koordinate der linken oberen Ecke des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="80c4d-112">The y-coordinate of the upper-left corner of the rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="80c4d-113">**x2**</span><span class="sxs-lookup"><span data-stu-id="80c4d-113">**x2**</span></span>
</dt> <dd>

<span data-ttu-id="80c4d-114">Type: **[ **Long**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="80c4d-114">Type: **[**LONG**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="80c4d-115">Die x-Koordinate der unteren rechten Ecke des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="80c4d-115">The x-coordinate of the lower-right corner of the rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="80c4d-116">**Y2**</span><span class="sxs-lookup"><span data-stu-id="80c4d-116">**y2**</span></span>
</dt> <dd>

<span data-ttu-id="80c4d-117">Type: **[ **Long**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="80c4d-117">Type: **[**LONG**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="80c4d-118">Die y-Koordinate der unteren rechten Ecke des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="80c4d-118">The y-coordinate of the lower-right corner of the rectangle.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="80c4d-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="80c4d-119">Requirements</span></span>



| <span data-ttu-id="80c4d-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="80c4d-120">Requirement</span></span> | <span data-ttu-id="80c4d-121">Wert</span><span class="sxs-lookup"><span data-stu-id="80c4d-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="80c4d-122">Header</span><span class="sxs-lookup"><span data-stu-id="80c4d-122">Header</span></span><br/> | <dl> <span data-ttu-id="80c4d-123"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="80c4d-123"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80c4d-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="80c4d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80c4d-125">Direct3D-Strukturen</span><span class="sxs-lookup"><span data-stu-id="80c4d-125">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="80c4d-126">**Klartext**</span><span class="sxs-lookup"><span data-stu-id="80c4d-126">**Clear**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear)
</dt> </dl>

 

 
