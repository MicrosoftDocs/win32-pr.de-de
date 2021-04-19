---
description: Beschreibt einen 16-Bit-Gleit Komma Vektor.
ms.assetid: f823a327-f07a-44e9-b58a-7865e11e80eb
title: D3DXFLOAT16-Struktur (D3dx9math. h)
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
ms.openlocfilehash: 4b469c770b811ed11ec21b21d2b449df1fd75b1c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355189"
---
# <a name="d3dxfloat16-structure-d3dx9mathh"></a><span data-ttu-id="84b3e-103">D3DXFLOAT16-Struktur (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="84b3e-103">D3DXFLOAT16 structure (D3dx9math.h)</span></span>

<span data-ttu-id="84b3e-104">Beschreibt einen 16-Bit-Gleit Komma Vektor.</span><span class="sxs-lookup"><span data-stu-id="84b3e-104">Describes a 16-bit floating point vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="84b3e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="84b3e-105">Syntax</span></span>


```C++
typedef struct D3DXFLOAT16 {
  WORD Value;
} D3DXFLOAT16, *LPD3DXFLOAT16;
```



## <a name="members"></a><span data-ttu-id="84b3e-106">Member</span><span class="sxs-lookup"><span data-stu-id="84b3e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="84b3e-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="84b3e-107">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="84b3e-108">Typ: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="84b3e-108">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="84b3e-109">Die 16-Bit-Daten.</span><span class="sxs-lookup"><span data-stu-id="84b3e-109">The 16-bit data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="84b3e-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="84b3e-110">Remarks</span></span>

<span data-ttu-id="84b3e-111">C++-Programmierer können das Überladen von Operatoren und die Typumwandlung mit den [**D3DXFLOAT16-Erweiterungen**](d3dxfloat16-extensions.md)nutzen, die überladene Konstruktoren und Zuweisungs-, unäre und binäre (einschließlich Gleichheits-) Operatoren implementieren.</span><span class="sxs-lookup"><span data-stu-id="84b3e-111">C++ programmers can take advantage of operator overloading and type casting with the [**D3DXFLOAT16 Extensions**](d3dxfloat16-extensions.md), which implement overloaded constructors and assignment, unary, and binary (including equality) operators.</span></span>

## <a name="requirements"></a><span data-ttu-id="84b3e-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="84b3e-112">Requirements</span></span>



| <span data-ttu-id="84b3e-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="84b3e-113">Requirement</span></span> | <span data-ttu-id="84b3e-114">Wert</span><span class="sxs-lookup"><span data-stu-id="84b3e-114">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="84b3e-115">Header</span><span class="sxs-lookup"><span data-stu-id="84b3e-115">Header</span></span><br/> | <dl> <span data-ttu-id="84b3e-116"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="84b3e-116"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84b3e-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84b3e-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84b3e-118">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="84b3e-118">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
