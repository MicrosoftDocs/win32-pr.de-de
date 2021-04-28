---
description: 'D3DXATTRIBUTEWEIGHTS-Struktur: Gibt Meshgewichtungsattribute an.'
ms.assetid: 8901a0fe-e38a-4045-8e8d-584be2620cc3
title: D3DXATTRIBUTEWEIGHTS-Struktur (D3dx9mesh.h)
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
ms.openlocfilehash: 7a833d2a58db0f434f836126926e461cd2ee3ea0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115968"
---
# <a name="d3dxattributeweights-structure"></a><span data-ttu-id="f60d1-103">D3DXATTRIBUTEWEIGHTS-Struktur</span><span class="sxs-lookup"><span data-stu-id="f60d1-103">D3DXATTRIBUTEWEIGHTS structure</span></span>

<span data-ttu-id="f60d1-104">Gibt Gitternetzgewichtungsattribute an.</span><span class="sxs-lookup"><span data-stu-id="f60d1-104">Specifies mesh weight attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="f60d1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f60d1-105">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="f60d1-106">Member</span><span class="sxs-lookup"><span data-stu-id="f60d1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f60d1-107">**Position**</span><span class="sxs-lookup"><span data-stu-id="f60d1-107">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="f60d1-108">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f60d1-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f60d1-109">Position</span><span class="sxs-lookup"><span data-stu-id="f60d1-109">Position.</span></span>

</dd> <dt>

<span data-ttu-id="f60d1-110">**Grenze**</span><span class="sxs-lookup"><span data-stu-id="f60d1-110">**Boundary**</span></span>
</dt> <dd>

<span data-ttu-id="f60d1-111">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f60d1-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f60d1-112">Mischungsgewichtung.</span><span class="sxs-lookup"><span data-stu-id="f60d1-112">Blend weight.</span></span>

</dd> <dt>

<span data-ttu-id="f60d1-113">**Normal**</span><span class="sxs-lookup"><span data-stu-id="f60d1-113">**Normal**</span></span>
</dt> <dd>

<span data-ttu-id="f60d1-114">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f60d1-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f60d1-115">Normal.</span><span class="sxs-lookup"><span data-stu-id="f60d1-115">Normal.</span></span>

</dd> <dt>

<span data-ttu-id="f60d1-116">**Diffus**</span><span class="sxs-lookup"><span data-stu-id="f60d1-116">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="f60d1-117">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f60d1-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f60d1-118">Diffuser Beleuchtungswert.</span><span class="sxs-lookup"><span data-stu-id="f60d1-118">Diffuse lighting value.</span></span>

</dd> <dt>

<span data-ttu-id="f60d1-119">**Glänzend**</span><span class="sxs-lookup"><span data-stu-id="f60d1-119">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="f60d1-120">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f60d1-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f60d1-121">Glanzlichtwert.</span><span class="sxs-lookup"><span data-stu-id="f60d1-121">Specular lighting value.</span></span>

</dd> <dt>

<span data-ttu-id="f60d1-122">**Texcoord**</span><span class="sxs-lookup"><span data-stu-id="f60d1-122">**Texcoord**</span></span>
</dt> <dd>

<span data-ttu-id="f60d1-123">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f60d1-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f60d1-124">Acht Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="f60d1-124">Eight texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="f60d1-125">**Tangente**</span><span class="sxs-lookup"><span data-stu-id="f60d1-125">**Tangent**</span></span>
</dt> <dd>

<span data-ttu-id="f60d1-126">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f60d1-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f60d1-127">Tangente.</span><span class="sxs-lookup"><span data-stu-id="f60d1-127">Tangent.</span></span>

</dd> <dt>

<span data-ttu-id="f60d1-128">**Binormal**</span><span class="sxs-lookup"><span data-stu-id="f60d1-128">**Binormal**</span></span>
</dt> <dd>

<span data-ttu-id="f60d1-129">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f60d1-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f60d1-130">Binormal.</span><span class="sxs-lookup"><span data-stu-id="f60d1-130">Binormal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f60d1-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f60d1-131">Remarks</span></span>

<span data-ttu-id="f60d1-132">Diese Struktur beschreibt, wie bei einem Vereinfachungsvorgang Scheitelpunktdaten berücksichtigt werden, wenn relative Kosten zwischen reduzierenden Kanten berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="f60d1-132">This structure describes how a simplification operation will consider vertex data when calculating relative costs between collapsing edges.</span></span> <span data-ttu-id="f60d1-133">Wenn das Feld Normal z. B. 0,0 ist, ignoriert der Vereinfachungsvorgang die Vertexnorm normal-Komponente beim Berechnen des Fehlers für das Reduzieren.</span><span class="sxs-lookup"><span data-stu-id="f60d1-133">For example, if the Normal field is 0.0, the simplification operation will ignore the vertex normal component when calculating the error for the collapse.</span></span> <span data-ttu-id="f60d1-134">Wenn das Feld Normal jedoch 1,0 ist, verwendet der Vereinfachungsvorgang die Vertex normal-Komponente.</span><span class="sxs-lookup"><span data-stu-id="f60d1-134">However, if the Normal field is 1.0, the simplification operation will use the vertex normal component.</span></span> <span data-ttu-id="f60d1-135">Wenn das Feld Normal 2,0 ist, doppelt so viele Fehler. , wenn das Feld Normal den Wert 4,0 aufweist, verdreiffachen Sie die Anzahl der Fehler usw.</span><span class="sxs-lookup"><span data-stu-id="f60d1-135">If the Normal field is 2.0, double the amount of errors; if the Normal field is 4.0, then quadruple the number of errors, and so on.</span></span>

<span data-ttu-id="f60d1-136">Der LPD3DXATTRIBUTEWEIGHTS-Typ wird als Zeiger auf die **D3DXATTRIBUTEWEIGHTS-Struktur** definiert.</span><span class="sxs-lookup"><span data-stu-id="f60d1-136">The LPD3DXATTRIBUTEWEIGHTS type is defined as a pointer to the **D3DXATTRIBUTEWEIGHTS** structure.</span></span>


```
    
    typedef D3DXATTRIBUTEWEIGHTS* LPD3DXATTRIBUTEWEIGHTS;
```



## <a name="requirements"></a><span data-ttu-id="f60d1-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f60d1-137">Requirements</span></span>



| <span data-ttu-id="f60d1-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f60d1-138">Requirement</span></span> | <span data-ttu-id="f60d1-139">Wert</span><span class="sxs-lookup"><span data-stu-id="f60d1-139">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f60d1-140">Header</span><span class="sxs-lookup"><span data-stu-id="f60d1-140">Header</span></span><br/> | <dl> <span data-ttu-id="f60d1-141"><dt>D3dx9mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="f60d1-141"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f60d1-142">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f60d1-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f60d1-143">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="f60d1-143">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="f60d1-144">**D3DXSimplifyMesh**</span><span class="sxs-lookup"><span data-stu-id="f60d1-144">**D3DXSimplifyMesh**</span></span>](d3dxsimplifymesh.md)
</dt> </dl>

 

 
