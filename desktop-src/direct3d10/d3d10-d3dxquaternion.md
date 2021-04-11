---
description: Beschreibt eine Quaternion.
ms.assetid: e6cb45b2-3132-4315-b02d-a3dfc444f8cc
title: D3DXQUATERNION-Struktur (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQUATERNION
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 405e48c99d7298708af193016930a8defdf9d600
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355327"
---
# <a name="d3dxquaternion-structure-d3dx10mathh"></a><span data-ttu-id="b0835-103">D3DXQUATERNION-Struktur (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="b0835-103">D3DXQUATERNION structure (D3DX10Math.h)</span></span>

<span data-ttu-id="b0835-104">Beschreibt eine Quaternion.</span><span class="sxs-lookup"><span data-stu-id="b0835-104">Describes a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0835-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0835-105">Syntax</span></span>


```C++
typedef struct D3DXQUATERNION {
  FLOAT x;
  FLOAT y;
  FLOAT z;
  FLOAT w;
} D3DXQUATERNION, *LPD3DXQUATERNION;
```



## <a name="members"></a><span data-ttu-id="b0835-106">Member</span><span class="sxs-lookup"><span data-stu-id="b0835-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b0835-107">**x**</span><span class="sxs-lookup"><span data-stu-id="b0835-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="b0835-108">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0835-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b0835-109">Die x-Komponente.</span><span class="sxs-lookup"><span data-stu-id="b0835-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="b0835-110">**y**</span><span class="sxs-lookup"><span data-stu-id="b0835-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="b0835-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0835-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b0835-112">Die y-Komponente.</span><span class="sxs-lookup"><span data-stu-id="b0835-112">The y-component.</span></span>

</dd> <dt>

<span data-ttu-id="b0835-113">**z**</span><span class="sxs-lookup"><span data-stu-id="b0835-113">**z**</span></span>
</dt> <dd>

<span data-ttu-id="b0835-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0835-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b0835-115">Die z-Komponente.</span><span class="sxs-lookup"><span data-stu-id="b0835-115">The z-component.</span></span>

</dd> <dt>

<span data-ttu-id="b0835-116">**w**</span><span class="sxs-lookup"><span data-stu-id="b0835-116">**w**</span></span>
</dt> <dd>

<span data-ttu-id="b0835-117">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0835-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b0835-118">Die w-Komponente.</span><span class="sxs-lookup"><span data-stu-id="b0835-118">The w-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b0835-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b0835-119">Remarks</span></span>

<span data-ttu-id="b0835-120">Quaternionen fügen den \[ x-, y-, z- \] Werten, die einen Vektor definieren, ein viertes Element hinzu, was zu beliebigen 4D-Vektoren führt.</span><span class="sxs-lookup"><span data-stu-id="b0835-120">Quaternions add a fourth element to the \[ x, y, z\] values that define a vector, resulting in arbitrary 4D vectors.</span></span> <span data-ttu-id="b0835-121">Im folgenden wird jedoch veranschaulicht, wie sich die einzelnen Elemente einer Einheits-Quaternion auf eine Achse-Winkel Drehung beziehen (wobei q eine Einheits Quaternion (x, y, z, w), die Achse normalisiert und die gewünschte CCW-Drehung der Achse darstellt):</span><span class="sxs-lookup"><span data-stu-id="b0835-121">However, the following illustrates how each element of a unit quaternion relates to an axis-angle rotation (where q represents a unit quaternion (x, y, z, w), axis is normalized, and theta is the desired CCW rotation about the axis):</span></span>


```
q.x = sin(theta/2) * axis.x
q.y = sin(theta/2) * axis.y
q.z = sin(theta/2) * axis.z
q.w = cos(theta/2)
```



## <a name="requirements"></a><span data-ttu-id="b0835-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b0835-122">Requirements</span></span>



| <span data-ttu-id="b0835-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b0835-123">Requirement</span></span> | <span data-ttu-id="b0835-124">Wert</span><span class="sxs-lookup"><span data-stu-id="b0835-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0835-125">Header</span><span class="sxs-lookup"><span data-stu-id="b0835-125">Header</span></span><br/> | <dl> <span data-ttu-id="b0835-126"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0835-126"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0835-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b0835-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0835-128">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="b0835-128">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
