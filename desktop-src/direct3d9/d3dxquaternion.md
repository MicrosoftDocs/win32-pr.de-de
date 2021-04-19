---
description: Beschreibt eine Quaternion.
ms.assetid: 3d88ed17-5b0a-46d5-8fe6-d66e1fa26c13
title: D3DXQUATERNION-Struktur (D3dx9math. h)
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
- d3dx9math.h
ms.openlocfilehash: 59d3f147e8eb233b9197394bad738d19d9ceba5d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370424"
---
# <a name="d3dxquaternion-structure-d3dx9mathh"></a><span data-ttu-id="27135-103">D3DXQUATERNION-Struktur (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="27135-103">D3DXQUATERNION structure (D3dx9math.h)</span></span>

<span data-ttu-id="27135-104">Beschreibt eine Quaternion.</span><span class="sxs-lookup"><span data-stu-id="27135-104">Describes a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="27135-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="27135-105">Syntax</span></span>


```C++
typedef struct D3DXQUATERNION {
  FLOAT x;
  FLOAT y;
  FLOAT z;
  FLOAT w;
} D3DXQUATERNION, *LPD3DXQUATERNION;
```



## <a name="members"></a><span data-ttu-id="27135-106">Member</span><span class="sxs-lookup"><span data-stu-id="27135-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="27135-107">**x**</span><span class="sxs-lookup"><span data-stu-id="27135-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="27135-108">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="27135-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="27135-109">Die x-Komponente.</span><span class="sxs-lookup"><span data-stu-id="27135-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="27135-110">**y**</span><span class="sxs-lookup"><span data-stu-id="27135-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="27135-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="27135-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="27135-112">Die y-Komponente.</span><span class="sxs-lookup"><span data-stu-id="27135-112">The y-component.</span></span>

</dd> <dt>

<span data-ttu-id="27135-113">**z**</span><span class="sxs-lookup"><span data-stu-id="27135-113">**z**</span></span>
</dt> <dd>

<span data-ttu-id="27135-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="27135-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="27135-115">Die z-Komponente.</span><span class="sxs-lookup"><span data-stu-id="27135-115">The z-component.</span></span>

</dd> <dt>

<span data-ttu-id="27135-116">**w**</span><span class="sxs-lookup"><span data-stu-id="27135-116">**w**</span></span>
</dt> <dd>

<span data-ttu-id="27135-117">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="27135-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="27135-118">Die w-Komponente.</span><span class="sxs-lookup"><span data-stu-id="27135-118">The w-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="27135-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="27135-119">Remarks</span></span>

<span data-ttu-id="27135-120">Quaternionen fügen den \[ x-, y-, z- \] Werten, die einen Vektor definieren, ein viertes Element hinzu, was zu beliebigen 4D-Vektoren führt.</span><span class="sxs-lookup"><span data-stu-id="27135-120">Quaternions add a fourth element to the \[ x, y, z\] values that define a vector, resulting in arbitrary 4D vectors.</span></span> <span data-ttu-id="27135-121">Im folgenden wird jedoch veranschaulicht, wie sich die einzelnen Elemente einer Einheits-Quaternion auf eine Achse-Winkel Drehung beziehen (wobei q eine Einheits Quaternion (x, y, z, w), die Achse normalisiert und die gewünschte CCW-Drehung der Achse darstellt):</span><span class="sxs-lookup"><span data-stu-id="27135-121">However, the following illustrates how each element of a unit quaternion relates to an axis-angle rotation (where q represents a unit quaternion (x, y, z, w), axis is normalized, and theta is the desired CCW rotation about the axis):</span></span>


```
q.x = sin(theta/2) * axis.x
q.y = sin(theta/2) * axis.y
q.z = sin(theta/2) * axis.z
q.w = cos(theta/2)
```



<span data-ttu-id="27135-122">C++-Programmierer können das Überladen von Operatoren und die Typumwandlung mit den [**D3DXQUATERNION-Erweiterungen**](d3dxquaternion-extensions.md)nutzen, die überladene Konstruktoren und Zuweisungs-, unäre und binäre (einschließlich Gleichheits-) Operatoren implementieren.</span><span class="sxs-lookup"><span data-stu-id="27135-122">C++ programmers can take advantage of operator overloading and type casting with the [**D3DXQUATERNION Extensions**](d3dxquaternion-extensions.md), which implement overloaded constructors and assignment, unary, and binary (including equality) operators.</span></span>

## <a name="requirements"></a><span data-ttu-id="27135-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="27135-123">Requirements</span></span>



| <span data-ttu-id="27135-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="27135-124">Requirement</span></span> | <span data-ttu-id="27135-125">Wert</span><span class="sxs-lookup"><span data-stu-id="27135-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="27135-126">Header</span><span class="sxs-lookup"><span data-stu-id="27135-126">Header</span></span><br/> | <dl> <span data-ttu-id="27135-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="27135-127"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27135-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27135-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27135-129">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="27135-129">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="27135-130">Vektoren, Vertices und Quaternionen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="27135-130">Vectors, Vertices, and Quaternions (Direct3D 9)</span></span>](vectors--vertices--and-quaternions.md)
</dt> </dl>

 

 
