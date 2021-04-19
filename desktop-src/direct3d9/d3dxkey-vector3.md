---
description: Beschreibt einen Vektor Schlüssel zur Verwendung in Keyframe-Animationen. Gibt einen Vektor zu einem bestimmten Zeitpunkt an. Dies wird für Skalierungs-und Übersetzungsschlüssel verwendet.
ms.assetid: 7a7ba2ce-c9f3-4a04-b865-39de9070868b
title: D3DXKEY_VECTOR3-Struktur (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXKEY_VECTOR3
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 41aec16da30a6e8742290b747b844b7fb22f6650
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366639"
---
# <a name="d3dxkey_vector3-structure"></a><span data-ttu-id="fc394-105">D3DXKEY \_ VECTOR3-Struktur</span><span class="sxs-lookup"><span data-stu-id="fc394-105">D3DXKEY\_VECTOR3 structure</span></span>

<span data-ttu-id="fc394-106">Beschreibt einen Vektor Schlüssel zur Verwendung in Keyframe-Animationen.</span><span class="sxs-lookup"><span data-stu-id="fc394-106">Describes a vector key for use in key frame animation.</span></span> <span data-ttu-id="fc394-107">Gibt einen Vektor zu einem bestimmten Zeitpunkt an.</span><span class="sxs-lookup"><span data-stu-id="fc394-107">It specifies a vector at a given time.</span></span> <span data-ttu-id="fc394-108">Dies wird für Skalierungs-und Übersetzungsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="fc394-108">This is used for scale and translation keys.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc394-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="fc394-109">Syntax</span></span>


```C++
typedef struct D3DXKEY_VECTOR3 {
  FLOAT       Time;
  D3DXVECTOR3 Value;
} D3DXKEY_VECTOR3, *LPD3DXKEY_VECTOR3;
```



## <a name="members"></a><span data-ttu-id="fc394-110">Member</span><span class="sxs-lookup"><span data-stu-id="fc394-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="fc394-111">**Time**</span><span class="sxs-lookup"><span data-stu-id="fc394-111">**Time**</span></span>
</dt> <dd>

<span data-ttu-id="fc394-112">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fc394-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fc394-113">Der Keyframe-Zeitstempel.</span><span class="sxs-lookup"><span data-stu-id="fc394-113">Key frame time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="fc394-114">**Wert**</span><span class="sxs-lookup"><span data-stu-id="fc394-114">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="fc394-115">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)**</span><span class="sxs-lookup"><span data-stu-id="fc394-115">Type: **[**D3DXVECTOR3**](d3dxvector3.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fc394-116">[**D3DXVECTOR3**](d3dxvector3.md) 3D-Vektor, der Skalierungs-und/oder Übersetzungs Werte bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="fc394-116">[**D3DXVECTOR3**](d3dxvector3.md) 3D vector that supplies scale and/or translation values.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fc394-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fc394-117">Requirements</span></span>



| <span data-ttu-id="fc394-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fc394-118">Requirement</span></span> | <span data-ttu-id="fc394-119">Wert</span><span class="sxs-lookup"><span data-stu-id="fc394-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc394-120">Header</span><span class="sxs-lookup"><span data-stu-id="fc394-120">Header</span></span><br/> | <dl> <span data-ttu-id="fc394-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc394-121"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc394-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fc394-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc394-123">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="fc394-123">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
