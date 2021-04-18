---
description: Beschreibt eine Ebene.
ms.assetid: ffca4650-9788-4559-8f6b-a4e5db29ce55
title: D3DXPLANE-Struktur (D3dx9math. h)
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
ms.openlocfilehash: 260f9555313aea3443f0728f2b50189228429803
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354982"
---
# <a name="d3dxplane-structure-d3dx9mathh"></a><span data-ttu-id="acc90-103">D3DXPLANE-Struktur (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="acc90-103">D3DXPLANE structure (D3dx9math.h)</span></span>

<span data-ttu-id="acc90-104">Beschreibt eine Ebene.</span><span class="sxs-lookup"><span data-stu-id="acc90-104">Describes a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="acc90-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="acc90-105">Syntax</span></span>


```C++
typedef struct D3DXPLANE {
  FLOAT a;
  FLOAT b;
  FLOAT c;
  FLOAT d;
} D3DXPLANE, *LPD3DXPLANE;
```



## <a name="members"></a><span data-ttu-id="acc90-106">Member</span><span class="sxs-lookup"><span data-stu-id="acc90-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="acc90-107">**ein**</span><span class="sxs-lookup"><span data-stu-id="acc90-107">**a**</span></span>
</dt> <dd>

<span data-ttu-id="acc90-108">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="acc90-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="acc90-109">Der Koeffizient der Clippingebene in der Gleichung der allgemeinen Ebene.</span><span class="sxs-lookup"><span data-stu-id="acc90-109">The a coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="acc90-110">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="acc90-110">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="acc90-111">**b**</span><span class="sxs-lookup"><span data-stu-id="acc90-111">**b**</span></span>
</dt> <dd>

<span data-ttu-id="acc90-112">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="acc90-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="acc90-113">Der b-Koeffizient der Clippingebene in der Gleichung der allgemeinen Ebene.</span><span class="sxs-lookup"><span data-stu-id="acc90-113">The b coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="acc90-114">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="acc90-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="acc90-115">**c**</span><span class="sxs-lookup"><span data-stu-id="acc90-115">**c**</span></span>
</dt> <dd>

<span data-ttu-id="acc90-116">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="acc90-116">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="acc90-117">Der c-Koeffizient der Clippingebene in der Gleichung der allgemeinen Ebene.</span><span class="sxs-lookup"><span data-stu-id="acc90-117">The c coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="acc90-118">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="acc90-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="acc90-119">**d**</span><span class="sxs-lookup"><span data-stu-id="acc90-119">**d**</span></span>
</dt> <dd>

<span data-ttu-id="acc90-120">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="acc90-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="acc90-121">Der d-Koeffizient der Clippingebene in der Gleichung der allgemeinen Ebene.</span><span class="sxs-lookup"><span data-stu-id="acc90-121">The d coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="acc90-122">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="acc90-122">See Remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="acc90-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="acc90-123">Remarks</span></span>

<span data-ttu-id="acc90-124">Die Member der **D3DXPLANE** -Struktur haben die Form der allgemeinen ebenengleichung.</span><span class="sxs-lookup"><span data-stu-id="acc90-124">The members of the **D3DXPLANE** structure take the form of the general plane equation.</span></span> <span data-ttu-id="acc90-125">Sie passen in die Gleichung der allgemeinen Ebene an, sodass **ein** x + **b** y + **c** z + **d** w = 0 ist.</span><span class="sxs-lookup"><span data-stu-id="acc90-125">They fit into the general plane equation so that **a** x + **b** y + **c** z + **d** w = 0.</span></span>

<span data-ttu-id="acc90-126">C++-Programmierer können den Vorteil von Operator Überladungen und Typumwandlungen mit den [**D3DXPLANE-Erweiterungen**](d3dxplane-extensions.md) nutzen, die überladene Konstruktoren und Zuweisungs-, unäre und binäre (einschließlich Gleichheits-) Operatoren implementieren.</span><span class="sxs-lookup"><span data-stu-id="acc90-126">C++ programmers can take advantage of operator overloading and type casting with the [**D3DXPLANE Extensions**](d3dxplane-extensions.md) which implement overloaded constructors and assignment, unary, and binary (including equality) operators.</span></span>

## <a name="requirements"></a><span data-ttu-id="acc90-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="acc90-127">Requirements</span></span>



| <span data-ttu-id="acc90-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="acc90-128">Requirement</span></span> | <span data-ttu-id="acc90-129">Wert</span><span class="sxs-lookup"><span data-stu-id="acc90-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="acc90-130">Header</span><span class="sxs-lookup"><span data-stu-id="acc90-130">Header</span></span><br/> | <dl> <span data-ttu-id="acc90-131"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="acc90-131"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acc90-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="acc90-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acc90-133">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="acc90-133">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
