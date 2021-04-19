---
description: Gibt Gitter Gewichtungs Attribute an.
ms.assetid: 8901a0fe-e38a-4045-8e8d-584be2620cc3
title: D3DXATTRIBUTEWEIGHTS-Struktur (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXATTRIBUTEWEIGHTS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 49725e410fb700c7ecb93fd56a8db367d7f982a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367378"
---
# <a name="d3dxattributeweights-structure"></a><span data-ttu-id="f947f-103">D3DXATTRIBUTEWEIGHTS-Struktur</span><span class="sxs-lookup"><span data-stu-id="f947f-103">D3DXATTRIBUTEWEIGHTS structure</span></span>

<span data-ttu-id="f947f-104">Gibt Gitter Gewichtungs Attribute an.</span><span class="sxs-lookup"><span data-stu-id="f947f-104">Specifies mesh weight attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="f947f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f947f-105">Syntax</span></span>


```C++
typedef struct D3DXATTRIBUTEWEIGHTS {
  FLOAT Position;
  FLOAT Boundary;
  FLOAT Normal;
  FLOAT Diffuse;
  FLOAT Specular;
  FLOAT Texcoord[8];
  FLOAT Tangent;
  FLOAT Binormal;
} D3DXATTRIBUTEWEIGHTS, *LPD3DXATTRIBUTEWEIGHTS;
```



## <a name="members"></a><span data-ttu-id="f947f-106">Member</span><span class="sxs-lookup"><span data-stu-id="f947f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f947f-107">**Position**</span><span class="sxs-lookup"><span data-stu-id="f947f-107">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="f947f-108">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f947f-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f947f-109">Position</span><span class="sxs-lookup"><span data-stu-id="f947f-109">Position.</span></span>

</dd> <dt>

<span data-ttu-id="f947f-110">**Grenze**</span><span class="sxs-lookup"><span data-stu-id="f947f-110">**Boundary**</span></span>
</dt> <dd>

<span data-ttu-id="f947f-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f947f-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f947f-112">Blend-Gewichtung.</span><span class="sxs-lookup"><span data-stu-id="f947f-112">Blend weight.</span></span>

</dd> <dt>

<span data-ttu-id="f947f-113">**Normal**</span><span class="sxs-lookup"><span data-stu-id="f947f-113">**Normal**</span></span>
</dt> <dd>

<span data-ttu-id="f947f-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f947f-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f947f-115">Normal.</span><span class="sxs-lookup"><span data-stu-id="f947f-115">Normal.</span></span>

</dd> <dt>

<span data-ttu-id="f947f-116">**Diffus**</span><span class="sxs-lookup"><span data-stu-id="f947f-116">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="f947f-117">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f947f-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f947f-118">Diffuses Beleuchtungs Wert.</span><span class="sxs-lookup"><span data-stu-id="f947f-118">Diffuse lighting value.</span></span>

</dd> <dt>

<span data-ttu-id="f947f-119">**Glänzend**</span><span class="sxs-lookup"><span data-stu-id="f947f-119">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="f947f-120">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f947f-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f947f-121">Glanzlicht Wert.</span><span class="sxs-lookup"><span data-stu-id="f947f-121">Specular lighting value.</span></span>

</dd> <dt>

<span data-ttu-id="f947f-122">**Texcoord**</span><span class="sxs-lookup"><span data-stu-id="f947f-122">**Texcoord**</span></span>
</dt> <dd>

<span data-ttu-id="f947f-123">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f947f-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f947f-124">Acht Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="f947f-124">Eight texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="f947f-125">**Tangens**</span><span class="sxs-lookup"><span data-stu-id="f947f-125">**Tangent**</span></span>
</dt> <dd>

<span data-ttu-id="f947f-126">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f947f-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f947f-127">Tangens.</span><span class="sxs-lookup"><span data-stu-id="f947f-127">Tangent.</span></span>

</dd> <dt>

<span data-ttu-id="f947f-128">**Binormal**</span><span class="sxs-lookup"><span data-stu-id="f947f-128">**Binormal**</span></span>
</dt> <dd>

<span data-ttu-id="f947f-129">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f947f-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f947f-130">Binormal.</span><span class="sxs-lookup"><span data-stu-id="f947f-130">Binormal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f947f-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f947f-131">Remarks</span></span>

<span data-ttu-id="f947f-132">Diese Struktur beschreibt, wie bei einem Vereinfachungs Vorgang Scheitelpunkt Daten bei der Berechnung relativer Kosten zwischen reduzierenden Kanten berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="f947f-132">This structure describes how a simplification operation will consider vertex data when calculating relative costs between collapsing edges.</span></span> <span data-ttu-id="f947f-133">Wenn das normale Feld z. b. 0,0 ist, ignoriert der Vereinfachungs Vorgang die normale Scheitelpunkt Komponente bei der Berechnung des Fehlers für das reduzieren.</span><span class="sxs-lookup"><span data-stu-id="f947f-133">For example, if the Normal field is 0.0, the simplification operation will ignore the vertex normal component when calculating the error for the collapse.</span></span> <span data-ttu-id="f947f-134">Wenn das normale Feld jedoch 1,0 ist, wird für den Vereinfachungs Vorgang die normale Scheitelpunkt Komponente verwendet.</span><span class="sxs-lookup"><span data-stu-id="f947f-134">However, if the Normal field is 1.0, the simplification operation will use the vertex normal component.</span></span> <span data-ttu-id="f947f-135">Wenn das normale Feld 2,0 ist, doppelte die Fehler Menge. Wenn das normale Feld 4,0 ist, vervierfachen Sie die Anzahl der Fehler, usw.</span><span class="sxs-lookup"><span data-stu-id="f947f-135">If the Normal field is 2.0, double the amount of errors; if the Normal field is 4.0, then quadruple the number of errors, and so on.</span></span>

<span data-ttu-id="f947f-136">Der LPD3DXATTRIBUTEWEIGHTS-Typ wird als Zeiger auf die **D3DXATTRIBUTEWEIGHTS** -Struktur definiert.</span><span class="sxs-lookup"><span data-stu-id="f947f-136">The LPD3DXATTRIBUTEWEIGHTS type is defined as a pointer to the **D3DXATTRIBUTEWEIGHTS** structure.</span></span>


```
    
    typedef D3DXATTRIBUTEWEIGHTS* LPD3DXATTRIBUTEWEIGHTS;
```



## <a name="requirements"></a><span data-ttu-id="f947f-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f947f-137">Requirements</span></span>



| <span data-ttu-id="f947f-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f947f-138">Requirement</span></span> | <span data-ttu-id="f947f-139">Wert</span><span class="sxs-lookup"><span data-stu-id="f947f-139">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f947f-140">Header</span><span class="sxs-lookup"><span data-stu-id="f947f-140">Header</span></span><br/> | <dl> <span data-ttu-id="f947f-141"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="f947f-141"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f947f-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f947f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f947f-143">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="f947f-143">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="f947f-144">**D3DXSimplifyMesh**</span><span class="sxs-lookup"><span data-stu-id="f947f-144">**D3DXSimplifyMesh**</span></span>](d3dxsimplifymesh.md)
</dt> </dl>

 

 
