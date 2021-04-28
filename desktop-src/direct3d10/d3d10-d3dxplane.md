---
description: 'D3DXPLANE-Struktur (D3DX10Math.h): Beschreibt eine Ebene.'
ms.assetid: c6da7343-a4f3-4cac-855b-14bd70c0d3c2
title: D3DXPLANE-Struktur (D3DX10Math.h)
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
- D3DX10Math.h
ms.openlocfilehash: 440246fb47a851f9f5339c72a484a2cb59e8f662
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103328"
---
# <a name="d3dxplane-structure-d3dx10mathh"></a><span data-ttu-id="09ea2-103">D3DXPLANE-Struktur (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="09ea2-103">D3DXPLANE structure (D3DX10Math.h)</span></span>

<span data-ttu-id="09ea2-104">Beschreibt eine Ebene.</span><span class="sxs-lookup"><span data-stu-id="09ea2-104">Describes a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="09ea2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="09ea2-105">Syntax</span></span>


```C++
typedef struct D3DXPLANE {
  FLOAT a;
  FLOAT b;
  FLOAT c;
  FLOAT d;
} D3DXPLANE, *LPD3DXPLANE;
```



## <a name="members"></a><span data-ttu-id="09ea2-106">Member</span><span class="sxs-lookup"><span data-stu-id="09ea2-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="09ea2-107">**Eine**</span><span class="sxs-lookup"><span data-stu-id="09ea2-107">**a**</span></span>
</dt> <dd>

<span data-ttu-id="09ea2-108">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="09ea2-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="09ea2-109">Der Koeffizient der Clippingebene in der allgemeinen Ebenengleichung.</span><span class="sxs-lookup"><span data-stu-id="09ea2-109">The a coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="09ea2-110">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="09ea2-110">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="09ea2-111">**b**</span><span class="sxs-lookup"><span data-stu-id="09ea2-111">**b**</span></span>
</dt> <dd>

<span data-ttu-id="09ea2-112">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="09ea2-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="09ea2-113">Der b-Koeffizient der Clippingebene in der allgemeinen Ebenengleichung.</span><span class="sxs-lookup"><span data-stu-id="09ea2-113">The b coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="09ea2-114">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="09ea2-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="09ea2-115">**c**</span><span class="sxs-lookup"><span data-stu-id="09ea2-115">**c**</span></span>
</dt> <dd>

<span data-ttu-id="09ea2-116">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="09ea2-116">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="09ea2-117">Der c-Koeffizient der Clippingebene in der allgemeinen Ebenengleichung.</span><span class="sxs-lookup"><span data-stu-id="09ea2-117">The c coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="09ea2-118">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="09ea2-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="09ea2-119">**d**</span><span class="sxs-lookup"><span data-stu-id="09ea2-119">**d**</span></span>
</dt> <dd>

<span data-ttu-id="09ea2-120">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="09ea2-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="09ea2-121">Der d-Koeffizient der Clippingebene in der allgemeinen Ebenengleichung.</span><span class="sxs-lookup"><span data-stu-id="09ea2-121">The d coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="09ea2-122">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="09ea2-122">See Remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="09ea2-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="09ea2-123">Remarks</span></span>

<span data-ttu-id="09ea2-124">Die Elemente der **D3DXPLANE-Struktur** haben die Form der allgemeinen Ebenengleichung.</span><span class="sxs-lookup"><span data-stu-id="09ea2-124">The members of the **D3DXPLANE** structure take the form of the general plane equation.</span></span> <span data-ttu-id="09ea2-125">Sie passen in die allgemeine Ebenengleichung, sodass ax + by + alle + dw = 0 ist.</span><span class="sxs-lookup"><span data-stu-id="09ea2-125">They fit into the general plane equation so that ax + by + cz + dw = 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="09ea2-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="09ea2-126">Requirements</span></span>



| <span data-ttu-id="09ea2-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="09ea2-127">Requirement</span></span> | <span data-ttu-id="09ea2-128">Wert</span><span class="sxs-lookup"><span data-stu-id="09ea2-128">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="09ea2-129">Header</span><span class="sxs-lookup"><span data-stu-id="09ea2-129">Header</span></span><br/> | <dl> <span data-ttu-id="09ea2-130"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="09ea2-130"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09ea2-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="09ea2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09ea2-132">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="09ea2-132">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
