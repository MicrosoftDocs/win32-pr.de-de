---
description: Beschreibt einen Quaternion-Schlüssel zur Verwendung in der Keyframe-Animation. Ein Quaternion-Schlüssel ist ein Quaternion-Wert zu einem bestimmten Zeitpunkt.
ms.assetid: 8f5b74a3-f712-40ac-942c-a2189c2327c8
title: D3DXKEY_QUATERNION-Struktur (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXKEY_QUATERNION
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 12e4deead606c1a2c5b103ed9fd0e31e23515982
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354807"
---
# <a name="d3dxkey_quaternion-structure"></a><span data-ttu-id="4edc2-104">D3DXKEY \_ Quaternion-Struktur</span><span class="sxs-lookup"><span data-stu-id="4edc2-104">D3DXKEY\_QUATERNION structure</span></span>

<span data-ttu-id="4edc2-105">Beschreibt einen Quaternion-Schlüssel zur Verwendung in der Keyframe-Animation.</span><span class="sxs-lookup"><span data-stu-id="4edc2-105">Describes a quaternion key for use in key frame animation.</span></span> <span data-ttu-id="4edc2-106">Ein Quaternion-Schlüssel ist ein Quaternion-Wert zu einem bestimmten Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="4edc2-106">A quaternion key is a quaternion value at a given time.</span></span>

## <a name="syntax"></a><span data-ttu-id="4edc2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4edc2-107">Syntax</span></span>


```C++
typedef struct D3DXKEY_QUATERNION {
  FLOAT          Time;
  D3DXQUATERNION Value;
} D3DXKEY_QUATERNION, *LPD3DXKEY_QUATERNION;
```



## <a name="members"></a><span data-ttu-id="4edc2-108">Member</span><span class="sxs-lookup"><span data-stu-id="4edc2-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="4edc2-109">**Time**</span><span class="sxs-lookup"><span data-stu-id="4edc2-109">**Time**</span></span>
</dt> <dd>

<span data-ttu-id="4edc2-110">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4edc2-110">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4edc2-111">Zeitwert.</span><span class="sxs-lookup"><span data-stu-id="4edc2-111">Time value.</span></span>

</dd> <dt>

<span data-ttu-id="4edc2-112">**Wert**</span><span class="sxs-lookup"><span data-stu-id="4edc2-112">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="4edc2-113">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)**</span><span class="sxs-lookup"><span data-stu-id="4edc2-113">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4edc2-114">[**D3DXQUATERNION**](d3dxquaternion.md) Quaternion, das Rotations Werte bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="4edc2-114">[**D3DXQUATERNION**](d3dxquaternion.md) quaternion that supplies rotation values.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4edc2-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4edc2-115">Requirements</span></span>



| <span data-ttu-id="4edc2-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4edc2-116">Requirement</span></span> | <span data-ttu-id="4edc2-117">Wert</span><span class="sxs-lookup"><span data-stu-id="4edc2-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4edc2-118">Header</span><span class="sxs-lookup"><span data-stu-id="4edc2-118">Header</span></span><br/> | <dl> <span data-ttu-id="4edc2-119"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="4edc2-119"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4edc2-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4edc2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4edc2-121">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="4edc2-121">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
