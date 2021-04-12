---
description: Gibt Gitter Gewichtungs Attribute an.
ms.assetid: 554bb8f2-9e92-4e9e-b500-c3cc47d57830
title: D3DX10_ATTRIBUTE_WEIGHTS-Struktur (d3dx10. h)
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
ms.openlocfilehash: 4f137c1ecc29c184c4dec3995fb0202741ce9f09
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355107"
---
# <a name="d3dx10_attribute_weights-structure"></a><span data-ttu-id="46c42-103">D3dx10- \_ Attribut \_ Gewichtungs Struktur</span><span class="sxs-lookup"><span data-stu-id="46c42-103">D3DX10\_ATTRIBUTE\_WEIGHTS structure</span></span>

<span data-ttu-id="46c42-104">Gibt Gitter Gewichtungs Attribute an.</span><span class="sxs-lookup"><span data-stu-id="46c42-104">Specifies mesh weight attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="46c42-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="46c42-105">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="46c42-106">Member</span><span class="sxs-lookup"><span data-stu-id="46c42-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="46c42-107">**Position**</span><span class="sxs-lookup"><span data-stu-id="46c42-107">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="46c42-108">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46c42-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="46c42-109">Position</span><span class="sxs-lookup"><span data-stu-id="46c42-109">Position.</span></span>

</dd> <dt>

<span data-ttu-id="46c42-110">**Grenze**</span><span class="sxs-lookup"><span data-stu-id="46c42-110">**Boundary**</span></span>
</dt> <dd>

<span data-ttu-id="46c42-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46c42-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="46c42-112">Blend-Gewichtung.</span><span class="sxs-lookup"><span data-stu-id="46c42-112">Blend weight.</span></span>

</dd> <dt>

<span data-ttu-id="46c42-113">**Normal**</span><span class="sxs-lookup"><span data-stu-id="46c42-113">**Normal**</span></span>
</dt> <dd>

<span data-ttu-id="46c42-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46c42-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="46c42-115">Normal.</span><span class="sxs-lookup"><span data-stu-id="46c42-115">Normal.</span></span>

</dd> <dt>

<span data-ttu-id="46c42-116">**Diffus**</span><span class="sxs-lookup"><span data-stu-id="46c42-116">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="46c42-117">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46c42-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="46c42-118">Diffuses Beleuchtungs Wert.</span><span class="sxs-lookup"><span data-stu-id="46c42-118">Diffuse lighting value.</span></span>

</dd> <dt>

<span data-ttu-id="46c42-119">**Glänzend**</span><span class="sxs-lookup"><span data-stu-id="46c42-119">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="46c42-120">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46c42-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="46c42-121">Glanzlicht Wert.</span><span class="sxs-lookup"><span data-stu-id="46c42-121">Specular lighting value.</span></span>

</dd> <dt>

<span data-ttu-id="46c42-122">**Texcoord**</span><span class="sxs-lookup"><span data-stu-id="46c42-122">**Texcoord**</span></span>
</dt> <dd>

<span data-ttu-id="46c42-123">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46c42-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="46c42-124">Acht Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="46c42-124">Eight texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="46c42-125">**Tangens**</span><span class="sxs-lookup"><span data-stu-id="46c42-125">**Tangent**</span></span>
</dt> <dd>

<span data-ttu-id="46c42-126">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46c42-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="46c42-127">Tangens.</span><span class="sxs-lookup"><span data-stu-id="46c42-127">Tangent.</span></span>

</dd> <dt>

<span data-ttu-id="46c42-128">**Binormal**</span><span class="sxs-lookup"><span data-stu-id="46c42-128">**Binormal**</span></span>
</dt> <dd>

<span data-ttu-id="46c42-129">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46c42-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="46c42-130">Binormal.</span><span class="sxs-lookup"><span data-stu-id="46c42-130">Binormal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="46c42-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="46c42-131">Remarks</span></span>

<span data-ttu-id="46c42-132">Diese Struktur beschreibt, wie bei einem Vereinfachungs Vorgang Scheitelpunkt Daten bei der Berechnung relativer Kosten zwischen reduzierenden Kanten berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="46c42-132">This structure describes how a simplification operation will consider vertex data when calculating relative costs between collapsing edges.</span></span> <span data-ttu-id="46c42-133">Wenn das normale Feld z. b. 0,0 ist, ignoriert der Vereinfachungs Vorgang die normale Scheitelpunkt Komponente bei der Berechnung des Fehlers für das reduzieren.</span><span class="sxs-lookup"><span data-stu-id="46c42-133">For example, if the Normal field is 0.0, the simplification operation will ignore the vertex normal component when calculating the error for the collapse.</span></span> <span data-ttu-id="46c42-134">Wenn das normale Feld jedoch 1,0 ist, wird für den Vereinfachungs Vorgang die normale Scheitelpunkt Komponente verwendet.</span><span class="sxs-lookup"><span data-stu-id="46c42-134">However, if the Normal field is 1.0, the simplification operation will use the vertex normal component.</span></span> <span data-ttu-id="46c42-135">Wenn das normale Feld 2,0 ist, doppelte die Fehler Menge. Wenn das normale Feld 4,0 ist, vervierfachen Sie die Anzahl der Fehler, usw.</span><span class="sxs-lookup"><span data-stu-id="46c42-135">If the Normal field is 2.0, double the amount of errors; if the Normal field is 4.0, then quadruple the number of errors, and so on.</span></span>

<span data-ttu-id="46c42-136">Der LPD3DX- \_ Attribut \_ Gewichtungs Typ wird als Zeiger auf die D3DX- \_ Attribut \_ Gewichtungs Struktur definiert.</span><span class="sxs-lookup"><span data-stu-id="46c42-136">The LPD3DX\_ATTRIBUTE\_WEIGHTS type is defined as a pointer to the D3DX\_ATTRIBUTE\_WEIGHTS structure.</span></span>


```
    typedef D3DX_ATTRIBUTE_WEIGHTS* LPD3DX_ATTRIBUTE_WEIGHTS;
```



## <a name="requirements"></a><span data-ttu-id="46c42-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46c42-137">Requirements</span></span>



| <span data-ttu-id="46c42-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="46c42-138">Requirement</span></span> | <span data-ttu-id="46c42-139">Wert</span><span class="sxs-lookup"><span data-stu-id="46c42-139">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="46c42-140">Header</span><span class="sxs-lookup"><span data-stu-id="46c42-140">Header</span></span><br/> | <dl> <span data-ttu-id="46c42-141"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="46c42-141"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46c42-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46c42-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46c42-143">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="46c42-143">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
