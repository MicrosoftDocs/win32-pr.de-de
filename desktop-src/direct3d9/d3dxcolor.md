---
description: 'D3DXCOLOR-Struktur (D3dx9math.h): Beschreibt Farbwerte.'
ms.assetid: 53d3176a-f727-498e-8bea-0e30e0a1c66e
title: D3DXCOLOR-Struktur (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCOLOR
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 58b02abc49b695169674a2579b73dc2359801a73
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115928"
---
# <a name="d3dxcolor-structure-d3dx9mathh"></a><span data-ttu-id="b0f91-103">D3DXCOLOR-Struktur (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="b0f91-103">D3DXCOLOR structure (D3dx9math.h)</span></span>

<span data-ttu-id="b0f91-104">Beschreibt Farbwerte.</span><span class="sxs-lookup"><span data-stu-id="b0f91-104">Describes color values.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0f91-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0f91-105">Syntax</span></span>


```C++
typedef struct D3DXCOLOR {
  FLOAT r;
  FLOAT g;
  FLOAT b;
  FLOAT a;
} D3DXCOLOR, *LPD3DXCOLOR;
```



## <a name="members"></a><span data-ttu-id="b0f91-106">Member</span><span class="sxs-lookup"><span data-stu-id="b0f91-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b0f91-107">**r**</span><span class="sxs-lookup"><span data-stu-id="b0f91-107">**r**</span></span>
</dt> <dd>

<span data-ttu-id="b0f91-108">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0f91-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b0f91-109">Rote Komponente der Farbe.</span><span class="sxs-lookup"><span data-stu-id="b0f91-109">Red component of the color.</span></span>

</dd> <dt>

<span data-ttu-id="b0f91-110">**g**</span><span class="sxs-lookup"><span data-stu-id="b0f91-110">**g**</span></span>
</dt> <dd>

<span data-ttu-id="b0f91-111">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0f91-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b0f91-112">Grüne Komponente der Farbe.</span><span class="sxs-lookup"><span data-stu-id="b0f91-112">Green component of the color.</span></span>

</dd> <dt>

<span data-ttu-id="b0f91-113">**b**</span><span class="sxs-lookup"><span data-stu-id="b0f91-113">**b**</span></span>
</dt> <dd>

<span data-ttu-id="b0f91-114">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0f91-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b0f91-115">Blaue Komponente der Farbe.</span><span class="sxs-lookup"><span data-stu-id="b0f91-115">Blue component of the color.</span></span>

</dd> <dt>

<span data-ttu-id="b0f91-116">**Eine**</span><span class="sxs-lookup"><span data-stu-id="b0f91-116">**a**</span></span>
</dt> <dd>

<span data-ttu-id="b0f91-117">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0f91-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b0f91-118">Alphakomponente der Farbe.</span><span class="sxs-lookup"><span data-stu-id="b0f91-118">Alpha component of the color.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b0f91-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b0f91-119">Remarks</span></span>

<span data-ttu-id="b0f91-120">C++-Programmierer können die Operatorüberladung und Typcasting mit den [**D3DXCOLOR-Erweiterungen**](d3dxcolor-extensions.md)nutzen, die überladene Konstruktoren sowie Zuweisungs-, unäre und binäre Operatoren (einschließlich Gleichheit) implementieren.</span><span class="sxs-lookup"><span data-stu-id="b0f91-120">C++ programmers can take advantage of operator overloading and type casting with the [**D3DXCOLOR Extensions**](d3dxcolor-extensions.md), which implement overloaded constructors, as well as assignment, unary, and binary (including equality) operators.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0f91-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b0f91-121">Requirements</span></span>



| <span data-ttu-id="b0f91-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b0f91-122">Requirement</span></span> | <span data-ttu-id="b0f91-123">Wert</span><span class="sxs-lookup"><span data-stu-id="b0f91-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0f91-124">Header</span><span class="sxs-lookup"><span data-stu-id="b0f91-124">Header</span></span><br/> | <dl> <span data-ttu-id="b0f91-125"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="b0f91-125"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0f91-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b0f91-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0f91-127">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="b0f91-127">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
