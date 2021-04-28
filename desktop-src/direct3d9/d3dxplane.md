---
description: 'D3DXPLANE-Struktur (D3dx9math.h): Beschreibt eine Ebene.'
ms.assetid: ffca4650-9788-4559-8f6b-a4e5db29ce55
title: D3DXPLANE-Struktur (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPLANE
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 3df0c94dbd49cf38d9230a2c5392df8497c64761
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115718"
---
# <a name="d3dxplane-structure-d3dx9mathh"></a><span data-ttu-id="6153a-103">D3DXPLANE-Struktur (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="6153a-103">D3DXPLANE structure (D3dx9math.h)</span></span>

<span data-ttu-id="6153a-104">Beschreibt eine Ebene.</span><span class="sxs-lookup"><span data-stu-id="6153a-104">Describes a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="6153a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6153a-105">Syntax</span></span>


```C++
typedef struct D3DXPLANE {
  FLOAT a;
  FLOAT b;
  FLOAT c;
  FLOAT d;
} D3DXPLANE, *LPD3DXPLANE;
```



## <a name="members"></a><span data-ttu-id="6153a-106">Member</span><span class="sxs-lookup"><span data-stu-id="6153a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="6153a-107">**Eine**</span><span class="sxs-lookup"><span data-stu-id="6153a-107">**a**</span></span>
</dt> <dd>

<span data-ttu-id="6153a-108">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6153a-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6153a-109">Der Koeffizienten der Clippingebene in der allgemeinen Ebenengleichung.</span><span class="sxs-lookup"><span data-stu-id="6153a-109">The a coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="6153a-110">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="6153a-110">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="6153a-111">**b**</span><span class="sxs-lookup"><span data-stu-id="6153a-111">**b**</span></span>
</dt> <dd>

<span data-ttu-id="6153a-112">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6153a-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6153a-113">Der b-Koeffizient der Clippingebene in der allgemeinen Ebenengleichung.</span><span class="sxs-lookup"><span data-stu-id="6153a-113">The b coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="6153a-114">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="6153a-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="6153a-115">**c**</span><span class="sxs-lookup"><span data-stu-id="6153a-115">**c**</span></span>
</dt> <dd>

<span data-ttu-id="6153a-116">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6153a-116">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6153a-117">Der c-Koeffizient der Clippingebene in der allgemeinen Ebenengleichung.</span><span class="sxs-lookup"><span data-stu-id="6153a-117">The c coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="6153a-118">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="6153a-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="6153a-119">**d**</span><span class="sxs-lookup"><span data-stu-id="6153a-119">**d**</span></span>
</dt> <dd>

<span data-ttu-id="6153a-120">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6153a-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6153a-121">Der d-Koeffizient der Clippingebene in der allgemeinen Ebenengleichung.</span><span class="sxs-lookup"><span data-stu-id="6153a-121">The d coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="6153a-122">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="6153a-122">See Remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6153a-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6153a-123">Remarks</span></span>

<span data-ttu-id="6153a-124">Die Member der **D3DXPLANE-Struktur** haben die Form der allgemeinen Ebenengleichung.</span><span class="sxs-lookup"><span data-stu-id="6153a-124">The members of the **D3DXPLANE** structure take the form of the general plane equation.</span></span> <span data-ttu-id="6153a-125">Sie passen in die allgemeine Ebenengleichung, sodass **ein** x + **b** y + **c** z + **d** w = 0 ist.</span><span class="sxs-lookup"><span data-stu-id="6153a-125">They fit into the general plane equation so that **a** x + **b** y + **c** z + **d** w = 0.</span></span>

<span data-ttu-id="6153a-126">C++-Programmierer können die Vorteile der Operatorüberladung und Typcasting mit den [**D3DXPLANE-Erweiterungen**](d3dxplane-extensions.md) nutzen, die überladene Konstruktoren und Zuweisungs-, unäre und binäre Operatoren (einschließlich Gleichheitsoperatoren) implementieren.</span><span class="sxs-lookup"><span data-stu-id="6153a-126">C++ programmers can take advantage of operator overloading and type casting with the [**D3DXPLANE Extensions**](d3dxplane-extensions.md) which implement overloaded constructors and assignment, unary, and binary (including equality) operators.</span></span>

## <a name="requirements"></a><span data-ttu-id="6153a-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6153a-127">Requirements</span></span>



| <span data-ttu-id="6153a-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6153a-128">Requirement</span></span> | <span data-ttu-id="6153a-129">Wert</span><span class="sxs-lookup"><span data-stu-id="6153a-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6153a-130">Header</span><span class="sxs-lookup"><span data-stu-id="6153a-130">Header</span></span><br/> | <dl> <span data-ttu-id="6153a-131"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="6153a-131"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6153a-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6153a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6153a-133">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="6153a-133">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
