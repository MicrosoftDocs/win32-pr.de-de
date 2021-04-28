---
description: 'D3DXQUATERNION-Struktur (D3dx9math.h): Beschreibt eine Quaternion.'
ms.assetid: 3d88ed17-5b0a-46d5-8fe6-d66e1fa26c13
title: D3DXQUATERNION-Struktur (D3dx9math.h)
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
ms.openlocfilehash: f67acc6389ce809c1aa5f4987d9502735fe61e49
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115678"
---
# <a name="d3dxquaternion-structure-d3dx9mathh"></a><span data-ttu-id="150c1-103">D3DXQUATERNION-Struktur (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="150c1-103">D3DXQUATERNION structure (D3dx9math.h)</span></span>

<span data-ttu-id="150c1-104">Beschreibt eine Quaternion.</span><span class="sxs-lookup"><span data-stu-id="150c1-104">Describes a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="150c1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="150c1-105">Syntax</span></span>


```C++
typedef struct D3DXQUATERNION {
  FLOAT x;
  FLOAT y;
  FLOAT z;
  FLOAT w;
} D3DXQUATERNION, *LPD3DXQUATERNION;
```



## <a name="members"></a><span data-ttu-id="150c1-106">Member</span><span class="sxs-lookup"><span data-stu-id="150c1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="150c1-107">**x**</span><span class="sxs-lookup"><span data-stu-id="150c1-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="150c1-108">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="150c1-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="150c1-109">Die x-Komponente.</span><span class="sxs-lookup"><span data-stu-id="150c1-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="150c1-110">**y**</span><span class="sxs-lookup"><span data-stu-id="150c1-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="150c1-111">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="150c1-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="150c1-112">Die y-Komponente.</span><span class="sxs-lookup"><span data-stu-id="150c1-112">The y-component.</span></span>

</dd> <dt>

<span data-ttu-id="150c1-113">**z**</span><span class="sxs-lookup"><span data-stu-id="150c1-113">**z**</span></span>
</dt> <dd>

<span data-ttu-id="150c1-114">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="150c1-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="150c1-115">Die z-Komponente.</span><span class="sxs-lookup"><span data-stu-id="150c1-115">The z-component.</span></span>

</dd> <dt>

<span data-ttu-id="150c1-116">**w**</span><span class="sxs-lookup"><span data-stu-id="150c1-116">**w**</span></span>
</dt> <dd>

<span data-ttu-id="150c1-117">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="150c1-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="150c1-118">Die w-Komponente.</span><span class="sxs-lookup"><span data-stu-id="150c1-118">The w-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="150c1-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="150c1-119">Remarks</span></span>

<span data-ttu-id="150c1-120">Quaternionen fügen den \[ x-, y-, \] z-Werten, die einen Vektor definieren, ein viertes Element hinzu, was zu beliebigen 4D-Vektoren führt.</span><span class="sxs-lookup"><span data-stu-id="150c1-120">Quaternions add a fourth element to the \[ x, y, z\] values that define a vector, resulting in arbitrary 4D vectors.</span></span> <span data-ttu-id="150c1-121">Im Folgenden wird jedoch veranschaulicht, wie sich jedes Element einer Einheiten quaternion auf eine Achsenwinkelrotation bezieht (wobei q eine Einheiten quaternion (x, y, z, w) darstellt, die Achse normalisiert wird und theta die gewünschte CCW-Drehung um die Achse darstellt):</span><span class="sxs-lookup"><span data-stu-id="150c1-121">However, the following illustrates how each element of a unit quaternion relates to an axis-angle rotation (where q represents a unit quaternion (x, y, z, w), axis is normalized, and theta is the desired CCW rotation about the axis):</span></span>


```
q.x = sin(theta/2) * axis.x
q.y = sin(theta/2) * axis.y
q.z = sin(theta/2) * axis.z
q.w = cos(theta/2)
```



<span data-ttu-id="150c1-122">C++-Programmierer können die Vorteile der Operatorüberladung und Typcasting mit den [**D3DXQUATERNION-Erweiterungen**](d3dxquaternion-extensions.md)nutzen, die überladene Konstruktoren und Zuweisungs-, unäre und binäre Operatoren (einschließlich Gleichheitsoperatoren) implementieren.</span><span class="sxs-lookup"><span data-stu-id="150c1-122">C++ programmers can take advantage of operator overloading and type casting with the [**D3DXQUATERNION Extensions**](d3dxquaternion-extensions.md), which implement overloaded constructors and assignment, unary, and binary (including equality) operators.</span></span>

## <a name="requirements"></a><span data-ttu-id="150c1-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="150c1-123">Requirements</span></span>



| <span data-ttu-id="150c1-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="150c1-124">Requirement</span></span> | <span data-ttu-id="150c1-125">Wert</span><span class="sxs-lookup"><span data-stu-id="150c1-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="150c1-126">Header</span><span class="sxs-lookup"><span data-stu-id="150c1-126">Header</span></span><br/> | <dl> <span data-ttu-id="150c1-127"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="150c1-127"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="150c1-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="150c1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="150c1-129">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="150c1-129">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="150c1-130">Vektoren, Scheitelpunkte und Quaternionen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="150c1-130">Vectors, Vertices, and Quaternions (Direct3D 9)</span></span>](vectors--vertices--and-quaternions.md)
</dt> </dl>

 

 
