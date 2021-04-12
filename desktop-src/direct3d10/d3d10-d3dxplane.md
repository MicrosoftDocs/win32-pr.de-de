---
description: Beschreibt eine Ebene.
ms.assetid: c6da7343-a4f3-4cac-855b-14bd70c0d3c2
title: D3DXPLANE-Struktur (D3DX10Math. h)
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
ms.openlocfilehash: 9949aec16e90a53e01e536255c20f442052bb98b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355656"
---
# <a name="d3dxplane-structure-d3dx10mathh"></a><span data-ttu-id="771ce-103">D3DXPLANE-Struktur (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="771ce-103">D3DXPLANE structure (D3DX10Math.h)</span></span>

<span data-ttu-id="771ce-104">Beschreibt eine Ebene.</span><span class="sxs-lookup"><span data-stu-id="771ce-104">Describes a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="771ce-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="771ce-105">Syntax</span></span>


```C++
typedef struct D3DXPLANE {
  FLOAT a;
  FLOAT b;
  FLOAT c;
  FLOAT d;
} D3DXPLANE, *LPD3DXPLANE;
```



## <a name="members"></a><span data-ttu-id="771ce-106">Member</span><span class="sxs-lookup"><span data-stu-id="771ce-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="771ce-107">**ein**</span><span class="sxs-lookup"><span data-stu-id="771ce-107">**a**</span></span>
</dt> <dd>

<span data-ttu-id="771ce-108">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="771ce-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="771ce-109">Der Koeffizient der Clippingebene in der Gleichung der allgemeinen Ebene.</span><span class="sxs-lookup"><span data-stu-id="771ce-109">The a coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="771ce-110">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="771ce-110">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="771ce-111">**b**</span><span class="sxs-lookup"><span data-stu-id="771ce-111">**b**</span></span>
</dt> <dd>

<span data-ttu-id="771ce-112">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="771ce-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="771ce-113">Der b-Koeffizient der Clippingebene in der Gleichung der allgemeinen Ebene.</span><span class="sxs-lookup"><span data-stu-id="771ce-113">The b coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="771ce-114">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="771ce-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="771ce-115">**c**</span><span class="sxs-lookup"><span data-stu-id="771ce-115">**c**</span></span>
</dt> <dd>

<span data-ttu-id="771ce-116">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="771ce-116">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="771ce-117">Der c-Koeffizient der Clippingebene in der Gleichung der allgemeinen Ebene.</span><span class="sxs-lookup"><span data-stu-id="771ce-117">The c coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="771ce-118">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="771ce-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="771ce-119">**d**</span><span class="sxs-lookup"><span data-stu-id="771ce-119">**d**</span></span>
</dt> <dd>

<span data-ttu-id="771ce-120">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="771ce-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="771ce-121">Der d-Koeffizient der Clippingebene in der Gleichung der allgemeinen Ebene.</span><span class="sxs-lookup"><span data-stu-id="771ce-121">The d coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="771ce-122">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="771ce-122">See Remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="771ce-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="771ce-123">Remarks</span></span>

<span data-ttu-id="771ce-124">Die Member der **D3DXPLANE** -Struktur haben die Form der allgemeinen ebenengleichung.</span><span class="sxs-lookup"><span data-stu-id="771ce-124">The members of the **D3DXPLANE** structure take the form of the general plane equation.</span></span> <span data-ttu-id="771ce-125">Sie passen in die Gleichung der allgemeinen Ebene, sodass AX + by + CZ + DW = 0 ist.</span><span class="sxs-lookup"><span data-stu-id="771ce-125">They fit into the general plane equation so that ax + by + cz + dw = 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="771ce-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="771ce-126">Requirements</span></span>



| <span data-ttu-id="771ce-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="771ce-127">Requirement</span></span> | <span data-ttu-id="771ce-128">Wert</span><span class="sxs-lookup"><span data-stu-id="771ce-128">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="771ce-129">Header</span><span class="sxs-lookup"><span data-stu-id="771ce-129">Header</span></span><br/> | <dl> <span data-ttu-id="771ce-130"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="771ce-130"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="771ce-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="771ce-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="771ce-132">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="771ce-132">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
