---
description: 'D3DXFLOAT16-Struktur (D3dx9math.h): Beschreibt einen 16-Bit-Gleitkommavektor.'
ms.assetid: f823a327-f07a-44e9-b58a-7865e11e80eb
title: D3DXFLOAT16-Struktur (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFLOAT16
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: dc878575de4338a2a399f329362d79ff2e7654f0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094268"
---
# <a name="d3dxfloat16-structure-d3dx9mathh"></a><span data-ttu-id="661a1-103">D3DXFLOAT16-Struktur (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="661a1-103">D3DXFLOAT16 structure (D3dx9math.h)</span></span>

<span data-ttu-id="661a1-104">Beschreibt einen 16-Bit-Gleitkommavektor.</span><span class="sxs-lookup"><span data-stu-id="661a1-104">Describes a 16-bit floating point vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="661a1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="661a1-105">Syntax</span></span>


```C++
typedef struct D3DXFLOAT16 {
  WORD Value;
} D3DXFLOAT16, *LPD3DXFLOAT16;
```



## <a name="members"></a><span data-ttu-id="661a1-106">Member</span><span class="sxs-lookup"><span data-stu-id="661a1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="661a1-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="661a1-107">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="661a1-108">Typ: **[ **WORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="661a1-108">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="661a1-109">Die 16-Bit-Daten.</span><span class="sxs-lookup"><span data-stu-id="661a1-109">The 16-bit data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="661a1-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="661a1-110">Remarks</span></span>

<span data-ttu-id="661a1-111">C++-Programmierer können die Vorteile der Operatorüberladung und Typcasting mit den [**D3DXFLOAT16-Erweiterungen**](d3dxfloat16-extensions.md)nutzen, die überladene Konstruktoren und Zuweisungs-, unäre und binäre Operatoren (einschließlich Gleichheitsoperatoren) implementieren.</span><span class="sxs-lookup"><span data-stu-id="661a1-111">C++ programmers can take advantage of operator overloading and type casting with the [**D3DXFLOAT16 Extensions**](d3dxfloat16-extensions.md), which implement overloaded constructors and assignment, unary, and binary (including equality) operators.</span></span>

## <a name="requirements"></a><span data-ttu-id="661a1-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="661a1-112">Requirements</span></span>



| <span data-ttu-id="661a1-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="661a1-113">Requirement</span></span> | <span data-ttu-id="661a1-114">Wert</span><span class="sxs-lookup"><span data-stu-id="661a1-114">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="661a1-115">Header</span><span class="sxs-lookup"><span data-stu-id="661a1-115">Header</span></span><br/> | <dl> <span data-ttu-id="661a1-116"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="661a1-116"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="661a1-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="661a1-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="661a1-118">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="661a1-118">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
