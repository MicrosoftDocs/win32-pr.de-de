---
description: Beschreibt einen dreieckigen Patch für hohe Reihenfolge.
ms.assetid: 3f97120b-3b32-4f95-8614-7b263ff330db
title: D3DTRIPATCH_INFO-Struktur (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTRIPATCH_INFO
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b910d38025c44d6157a76aa3e3425ba46d628787
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355826"
---
# <a name="d3dtripatch_info-structure"></a><span data-ttu-id="0fdf7-103">D3DTRIPATCH \_ Info-Struktur</span><span class="sxs-lookup"><span data-stu-id="0fdf7-103">D3DTRIPATCH\_INFO structure</span></span>

<span data-ttu-id="0fdf7-104">Beschreibt einen dreieckigen Patch für hohe Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="0fdf7-104">Describes a triangular high-order patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fdf7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0fdf7-105">Syntax</span></span>


```C++
typedef struct D3DTRIPATCH_INFO {
  UINT          StartVertexOffset;
  UINT          NumVertices;
  D3DBASISTYPE  Basis;
  D3DDEGREETYPE Degree;
} D3DTRIPATCH_INFO, *LPD3DTRIPATCH_INFO;
```



## <a name="members"></a><span data-ttu-id="0fdf7-106">Member</span><span class="sxs-lookup"><span data-stu-id="0fdf7-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0fdf7-107">**Startvertexoffset**</span><span class="sxs-lookup"><span data-stu-id="0fdf7-107">**StartVertexOffset**</span></span>
</dt> <dd>

<span data-ttu-id="0fdf7-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0fdf7-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0fdf7-109">Der Vertex-Offset wird als Anzahl von Vertices gestartet.</span><span class="sxs-lookup"><span data-stu-id="0fdf7-109">Starting vertex offset, in number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="0fdf7-110">**Numvertices**</span><span class="sxs-lookup"><span data-stu-id="0fdf7-110">**NumVertices**</span></span>
</dt> <dd>

<span data-ttu-id="0fdf7-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0fdf7-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0fdf7-112">Anzahl der Scheitel Punkte.</span><span class="sxs-lookup"><span data-stu-id="0fdf7-112">Number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="0fdf7-113">**Basis**</span><span class="sxs-lookup"><span data-stu-id="0fdf7-113">**Basis**</span></span>
</dt> <dd>

<span data-ttu-id="0fdf7-114">Typ: **[ **D3DBASISTYPE**](./d3dbasistype.md)**</span><span class="sxs-lookup"><span data-stu-id="0fdf7-114">Type: **[**D3DBASISTYPE**](./d3dbasistype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0fdf7-115">Member des [**D3DBASISTYPE**](./d3dbasistype.md) -Enumerationstyps, der den Basistyp für den dreieckigen Patch für hohe Reihenfolge definiert.</span><span class="sxs-lookup"><span data-stu-id="0fdf7-115">Member of the [**D3DBASISTYPE**](./d3dbasistype.md) enumerated type, which defines the basis type for the triangular high-order patch.</span></span> <span data-ttu-id="0fdf7-116">Der einzige gültige Wert für diesen Member ist D3DBASIS \_ Bezier.</span><span class="sxs-lookup"><span data-stu-id="0fdf7-116">The only valid value for this member is D3DBASIS\_BEZIER.</span></span>

</dd> <dt>

<span data-ttu-id="0fdf7-117">**Grad**</span><span class="sxs-lookup"><span data-stu-id="0fdf7-117">**Degree**</span></span>
</dt> <dd>

<span data-ttu-id="0fdf7-118">Typ: **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**</span><span class="sxs-lookup"><span data-stu-id="0fdf7-118">Type: **[**D3DDEGREETYPE**](./d3ddegreetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0fdf7-119">Member des [**D3DDEGREETYPE**](./d3ddegreetype.md) -Enumerationstyps, der den gradtyp für den dreieckigen Patch für hohe Reihenfolge definiert.</span><span class="sxs-lookup"><span data-stu-id="0fdf7-119">Member of the [**D3DDEGREETYPE**](./d3ddegreetype.md) enumerated type, defining the degree type for the triangular high-order patch.</span></span>



| <span data-ttu-id="0fdf7-120">Wert</span><span class="sxs-lookup"><span data-stu-id="0fdf7-120">Value</span></span>                | <span data-ttu-id="0fdf7-121">Anzahl von Vertices</span><span class="sxs-lookup"><span data-stu-id="0fdf7-121">Number of vertices</span></span> |
|----------------------|--------------------|
| <span data-ttu-id="0fdf7-122">D3DDEGREE \_ kubisch</span><span class="sxs-lookup"><span data-stu-id="0fdf7-122">D3DDEGREE\_CUBIC</span></span>     | <span data-ttu-id="0fdf7-123">10</span><span class="sxs-lookup"><span data-stu-id="0fdf7-123">10</span></span>                 |
| <span data-ttu-id="0fdf7-124">D3DDEGREE \_ linear</span><span class="sxs-lookup"><span data-stu-id="0fdf7-124">D3DDEGREE\_LINEAR</span></span>    | <span data-ttu-id="0fdf7-125">3</span><span class="sxs-lookup"><span data-stu-id="0fdf7-125">3</span></span>                  |
| <span data-ttu-id="0fdf7-126">D3DDEGREE \_ quadratisch</span><span class="sxs-lookup"><span data-stu-id="0fdf7-126">D3DDEGREE\_QUADRATIC</span></span> | <span data-ttu-id="0fdf7-127">–</span><span class="sxs-lookup"><span data-stu-id="0fdf7-127">N/A</span></span>                |
| <span data-ttu-id="0fdf7-128">D3DDEGREE \_ Quintic</span><span class="sxs-lookup"><span data-stu-id="0fdf7-128">D3DDEGREE\_QUINTIC</span></span>   | <span data-ttu-id="0fdf7-129">21</span><span class="sxs-lookup"><span data-stu-id="0fdf7-129">21</span></span>                 |



 

<span data-ttu-id="0fdf7-130">Nicht verfügbar-nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0fdf7-130">N/A - Not available.</span></span> <span data-ttu-id="0fdf7-131">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0fdf7-131">Not supported.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0fdf7-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0fdf7-132">Remarks</span></span>

<span data-ttu-id="0fdf7-133">Im folgenden Diagramm werden z. b. die Scheitelpunkt Reihenfolge und die Segment Nummern für einen kubischen Bézier-Dreiecks Patch identifiziert.</span><span class="sxs-lookup"><span data-stu-id="0fdf7-133">For example, the following diagram identifies the vertex order and segment numbers for a cubic Bézier triangle patch.</span></span> <span data-ttu-id="0fdf7-134">Die Scheitelpunkt Reihenfolge bestimmt die Segment Nummern, die von [**drawdreipatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0fdf7-134">The vertex order determines the segment numbers used by [**DrawTriPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch).</span></span> <span data-ttu-id="0fdf7-135">Der Offset ist die Anzahl der Bytes für den ersten Dreiecks patchscheitel Punkt im Scheitelpunkt Puffer.</span><span class="sxs-lookup"><span data-stu-id="0fdf7-135">The offset is the number of bytes to the first triangle patch vertex in the vertex buffer.</span></span>

![Diagramm eines dreieckigen hochwertigen Patches mit neun Vertices](images/hop-tripatch-info.png)

## <a name="requirements"></a><span data-ttu-id="0fdf7-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0fdf7-137">Requirements</span></span>



| <span data-ttu-id="0fdf7-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0fdf7-138">Requirement</span></span> | <span data-ttu-id="0fdf7-139">Wert</span><span class="sxs-lookup"><span data-stu-id="0fdf7-139">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0fdf7-140">Header</span><span class="sxs-lookup"><span data-stu-id="0fdf7-140">Header</span></span><br/> | <dl> <span data-ttu-id="0fdf7-141"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="0fdf7-141"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fdf7-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0fdf7-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fdf7-143">Direct3D-Strukturen</span><span class="sxs-lookup"><span data-stu-id="0fdf7-143">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="0fdf7-144">**Drawtrick Patch**</span><span class="sxs-lookup"><span data-stu-id="0fdf7-144">**DrawTriPatch**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch)
</dt> <dt>

[<span data-ttu-id="0fdf7-145">**D3DXTessellateTriPatch**</span><span class="sxs-lookup"><span data-stu-id="0fdf7-145">**D3DXTessellateTriPatch**</span></span>](d3dxtessellatetripatch.md)
</dt> </dl>

 

 
