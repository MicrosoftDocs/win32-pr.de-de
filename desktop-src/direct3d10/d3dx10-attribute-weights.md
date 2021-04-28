---
description: 'D3DX10_ATTRIBUTE_WEIGHTS Struktur: Gibt Die Attribute für die Netzgewichtung an.'
ms.assetid: 554bb8f2-9e92-4e9e-b500-c3cc47d57830
title: D3DX10_ATTRIBUTE_WEIGHTS-Struktur (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_ATTRIBUTE_WEIGHTS
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: ab163149493ad73f892a251a691ad82544d7f382
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094352"
---
# <a name="d3dx10_attribute_weights-structure"></a><span data-ttu-id="5135a-103">D3DX10 \_ ATTRIBUTE \_ WEIGHTS-Struktur</span><span class="sxs-lookup"><span data-stu-id="5135a-103">D3DX10\_ATTRIBUTE\_WEIGHTS structure</span></span>

<span data-ttu-id="5135a-104">Gibt Gitternetzgewichtungsattribute an.</span><span class="sxs-lookup"><span data-stu-id="5135a-104">Specifies mesh weight attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="5135a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5135a-105">Syntax</span></span>


```C++
typedef struct D3DX10_ATTRIBUTE_WEIGHTS {
  FLOAT Position;
  FLOAT Boundary;
  FLOAT Normal;
  FLOAT Diffuse;
  FLOAT Specular;
  FLOAT Texcoord[8];
  FLOAT Tangent;
  FLOAT Binormal;
} D3DX10_ATTRIBUTE_WEIGHTS, *LPD3DX10_ATTRIBUTE_WEIGHTS;
```



## <a name="members"></a><span data-ttu-id="5135a-106">Member</span><span class="sxs-lookup"><span data-stu-id="5135a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5135a-107">**Position**</span><span class="sxs-lookup"><span data-stu-id="5135a-107">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="5135a-108">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5135a-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5135a-109">Position</span><span class="sxs-lookup"><span data-stu-id="5135a-109">Position.</span></span>

</dd> <dt>

<span data-ttu-id="5135a-110">**Grenze**</span><span class="sxs-lookup"><span data-stu-id="5135a-110">**Boundary**</span></span>
</dt> <dd>

<span data-ttu-id="5135a-111">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5135a-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5135a-112">Mischungsgewichtung.</span><span class="sxs-lookup"><span data-stu-id="5135a-112">Blend weight.</span></span>

</dd> <dt>

<span data-ttu-id="5135a-113">**Normal**</span><span class="sxs-lookup"><span data-stu-id="5135a-113">**Normal**</span></span>
</dt> <dd>

<span data-ttu-id="5135a-114">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5135a-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5135a-115">Normal.</span><span class="sxs-lookup"><span data-stu-id="5135a-115">Normal.</span></span>

</dd> <dt>

<span data-ttu-id="5135a-116">**Diffus**</span><span class="sxs-lookup"><span data-stu-id="5135a-116">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="5135a-117">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5135a-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5135a-118">Diffuser Beleuchtungswert.</span><span class="sxs-lookup"><span data-stu-id="5135a-118">Diffuse lighting value.</span></span>

</dd> <dt>

<span data-ttu-id="5135a-119">**Glänzend**</span><span class="sxs-lookup"><span data-stu-id="5135a-119">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="5135a-120">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5135a-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5135a-121">Glanzlichtwert.</span><span class="sxs-lookup"><span data-stu-id="5135a-121">Specular lighting value.</span></span>

</dd> <dt>

<span data-ttu-id="5135a-122">**Texcoord**</span><span class="sxs-lookup"><span data-stu-id="5135a-122">**Texcoord**</span></span>
</dt> <dd>

<span data-ttu-id="5135a-123">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5135a-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5135a-124">Acht Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="5135a-124">Eight texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="5135a-125">**Tangente**</span><span class="sxs-lookup"><span data-stu-id="5135a-125">**Tangent**</span></span>
</dt> <dd>

<span data-ttu-id="5135a-126">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5135a-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5135a-127">Tangente.</span><span class="sxs-lookup"><span data-stu-id="5135a-127">Tangent.</span></span>

</dd> <dt>

<span data-ttu-id="5135a-128">**Binormal**</span><span class="sxs-lookup"><span data-stu-id="5135a-128">**Binormal**</span></span>
</dt> <dd>

<span data-ttu-id="5135a-129">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5135a-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5135a-130">Binormal.</span><span class="sxs-lookup"><span data-stu-id="5135a-130">Binormal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5135a-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5135a-131">Remarks</span></span>

<span data-ttu-id="5135a-132">Diese Struktur beschreibt, wie bei einem Vereinfachungsvorgang Scheitelpunktdaten berücksichtigt werden, wenn relative Kosten zwischen reduzierenden Kanten berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="5135a-132">This structure describes how a simplification operation will consider vertex data when calculating relative costs between collapsing edges.</span></span> <span data-ttu-id="5135a-133">Wenn das Feld Normal z. B. 0,0 ist, ignoriert der Vereinfachungsvorgang die normale Scheitelpunktkomponente, wenn der Fehler für das Reduzieren berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="5135a-133">For example, if the Normal field is 0.0, the simplification operation will ignore the vertex normal component when calculating the error for the collapse.</span></span> <span data-ttu-id="5135a-134">Wenn das Feld Normal jedoch 1,0 ist, verwendet der Vereinfachungsvorgang die Scheitelpunktnorm normal-Komponente.</span><span class="sxs-lookup"><span data-stu-id="5135a-134">However, if the Normal field is 1.0, the simplification operation will use the vertex normal component.</span></span> <span data-ttu-id="5135a-135">Wenn das Feld Normal den Wert 2.0 hat, sollten Sie die Anzahl der Fehler verdoppelt. Wenn das Feld Normal 4.0 ist, verffachen Sie die Anzahl der Fehler, und so weiter.</span><span class="sxs-lookup"><span data-stu-id="5135a-135">If the Normal field is 2.0, double the amount of errors; if the Normal field is 4.0, then quadruple the number of errors, and so on.</span></span>

<span data-ttu-id="5135a-136">Der TYP LPD3DX ATTRIBUTE WEIGHTS wird als Zeiger auf die \_ \_ D3DX \_ ATTRIBUTE \_ WEIGHTS-Struktur definiert.</span><span class="sxs-lookup"><span data-stu-id="5135a-136">The LPD3DX\_ATTRIBUTE\_WEIGHTS type is defined as a pointer to the D3DX\_ATTRIBUTE\_WEIGHTS structure.</span></span>


```
    typedef D3DX_ATTRIBUTE_WEIGHTS* LPD3DX_ATTRIBUTE_WEIGHTS;
```



## <a name="requirements"></a><span data-ttu-id="5135a-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5135a-137">Requirements</span></span>



| <span data-ttu-id="5135a-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5135a-138">Requirement</span></span> | <span data-ttu-id="5135a-139">Wert</span><span class="sxs-lookup"><span data-stu-id="5135a-139">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5135a-140">Header</span><span class="sxs-lookup"><span data-stu-id="5135a-140">Header</span></span><br/> | <dl> <span data-ttu-id="5135a-141"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="5135a-141"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5135a-142">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5135a-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5135a-143">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="5135a-143">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
