---
description: 'D3DXQUATERNION-Struktur (D3DX10Math.h): Beschreibt eine Quaternion.'
ms.assetid: e6cb45b2-3132-4315-b02d-a3dfc444f8cc
title: D3DXQUATERNION-Struktur (D3DX10Math.h)
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
ms.openlocfilehash: dac880607cf482b409c407b43992747af4aa39a9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103248"
---
# <a name="d3dxquaternion-structure-d3dx10mathh"></a><span data-ttu-id="7dcd1-103">D3DXQUATERNION-Struktur (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="7dcd1-103">D3DXQUATERNION structure (D3DX10Math.h)</span></span>

<span data-ttu-id="7dcd1-104">Beschreibt eine Quaternion.</span><span class="sxs-lookup"><span data-stu-id="7dcd1-104">Describes a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dcd1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7dcd1-105">Syntax</span></span>


```C++
typedef struct D3DXQUATERNION {
  FLOAT x;
  FLOAT y;
  FLOAT z;
  FLOAT w;
} D3DXQUATERNION, *LPD3DXQUATERNION;
```



## <a name="members"></a><span data-ttu-id="7dcd1-106">Member</span><span class="sxs-lookup"><span data-stu-id="7dcd1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7dcd1-107">**x**</span><span class="sxs-lookup"><span data-stu-id="7dcd1-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="7dcd1-108">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7dcd1-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7dcd1-109">Die x-Komponente.</span><span class="sxs-lookup"><span data-stu-id="7dcd1-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="7dcd1-110">**y**</span><span class="sxs-lookup"><span data-stu-id="7dcd1-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="7dcd1-111">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7dcd1-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7dcd1-112">Die y-Komponente.</span><span class="sxs-lookup"><span data-stu-id="7dcd1-112">The y-component.</span></span>

</dd> <dt>

<span data-ttu-id="7dcd1-113">**z**</span><span class="sxs-lookup"><span data-stu-id="7dcd1-113">**z**</span></span>
</dt> <dd>

<span data-ttu-id="7dcd1-114">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7dcd1-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7dcd1-115">Die z-Komponente.</span><span class="sxs-lookup"><span data-stu-id="7dcd1-115">The z-component.</span></span>

</dd> <dt>

<span data-ttu-id="7dcd1-116">**w**</span><span class="sxs-lookup"><span data-stu-id="7dcd1-116">**w**</span></span>
</dt> <dd>

<span data-ttu-id="7dcd1-117">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7dcd1-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7dcd1-118">Die w-Komponente.</span><span class="sxs-lookup"><span data-stu-id="7dcd1-118">The w-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7dcd1-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7dcd1-119">Remarks</span></span>

<span data-ttu-id="7dcd1-120">Quaternionen fügen den \[ x-, y-, \] z-Werten, die einen Vektor definieren, ein viertes Element hinzu, was zu beliebigen 4D-Vektoren führt.</span><span class="sxs-lookup"><span data-stu-id="7dcd1-120">Quaternions add a fourth element to the \[ x, y, z\] values that define a vector, resulting in arbitrary 4D vectors.</span></span> <span data-ttu-id="7dcd1-121">Im Folgenden wird jedoch veranschaulicht, wie sich jedes Element einer Einheiten quaternion auf eine Achsenwinkelrotation bezieht (wobei q eine Einheiten quaternion (x, y, z, w) darstellt, die Achse normalisiert wird und theta die gewünschte CCW-Drehung um die Achse darstellt):</span><span class="sxs-lookup"><span data-stu-id="7dcd1-121">However, the following illustrates how each element of a unit quaternion relates to an axis-angle rotation (where q represents a unit quaternion (x, y, z, w), axis is normalized, and theta is the desired CCW rotation about the axis):</span></span>


```
q.x = sin(theta/2) * axis.x
q.y = sin(theta/2) * axis.y
q.z = sin(theta/2) * axis.z
q.w = cos(theta/2)
```



## <a name="requirements"></a><span data-ttu-id="7dcd1-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7dcd1-122">Requirements</span></span>



| <span data-ttu-id="7dcd1-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7dcd1-123">Requirement</span></span> | <span data-ttu-id="7dcd1-124">Wert</span><span class="sxs-lookup"><span data-stu-id="7dcd1-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7dcd1-125">Header</span><span class="sxs-lookup"><span data-stu-id="7dcd1-125">Header</span></span><br/> | <dl> <span data-ttu-id="7dcd1-126"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="7dcd1-126"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7dcd1-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7dcd1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dcd1-128">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="7dcd1-128">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
