---
description: Beschreibt einen rechteckigen Patch für hohe Reihenfolge.
ms.assetid: 5f195009-d047-4dc0-a386-e1a434914e34
title: D3DRECTPATCH_INFO-Struktur (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRECTPATCH_INFO
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: a2b7fedbaac2cc9c204d4691828d31794cea1f47
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355204"
---
# <a name="d3drectpatch_info-structure"></a><span data-ttu-id="d08c9-103">D3DRECTPATCH \_ Info-Struktur</span><span class="sxs-lookup"><span data-stu-id="d08c9-103">D3DRECTPATCH\_INFO structure</span></span>

<span data-ttu-id="d08c9-104">Beschreibt einen rechteckigen Patch für hohe Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="d08c9-104">Describes a rectangular high-order patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="d08c9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d08c9-105">Syntax</span></span>


```C++
typedef struct D3DRECTPATCH_INFO {
  UINT          StartVertexOffsetWidth;
  UINT          StartVertexOffsetHeight;
  UINT          Width;
  UINT          Height;
  UINT          Stride;
  D3DBASISTYPE  Basis;
  D3DDEGREETYPE Degree;
} D3DRECTPATCH_INFO, *LPD3DRECTPATCH_INFO;
```



## <a name="members"></a><span data-ttu-id="d08c9-106">Member</span><span class="sxs-lookup"><span data-stu-id="d08c9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d08c9-107">**Startvertexoffsetwidth**</span><span class="sxs-lookup"><span data-stu-id="d08c9-107">**StartVertexOffsetWidth**</span></span>
</dt> <dd>

<span data-ttu-id="d08c9-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d08c9-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d08c9-109">Die Vertex-Offset Breite wird als Anzahl von Vertices gestartet.</span><span class="sxs-lookup"><span data-stu-id="d08c9-109">Starting vertex offset width, in number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="d08c9-110">**Startvertexoffsetheight**</span><span class="sxs-lookup"><span data-stu-id="d08c9-110">**StartVertexOffsetHeight**</span></span>
</dt> <dd>

<span data-ttu-id="d08c9-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d08c9-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d08c9-112">Die Vertex-Offset Höhe wird in der Anzahl der Scheitel Punkte gestartet.</span><span class="sxs-lookup"><span data-stu-id="d08c9-112">Starting vertex offset height, in number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="d08c9-113">**Width**</span><span class="sxs-lookup"><span data-stu-id="d08c9-113">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="d08c9-114">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d08c9-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d08c9-115">Breite der einzelnen Scheitel Punkte (in Anzahl der Vertices).</span><span class="sxs-lookup"><span data-stu-id="d08c9-115">Width of each vertex, in number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="d08c9-116">**Height**</span><span class="sxs-lookup"><span data-stu-id="d08c9-116">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="d08c9-117">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d08c9-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d08c9-118">Die Höhe der einzelnen Scheitel Punkte (in Anzahl der Vertices).</span><span class="sxs-lookup"><span data-stu-id="d08c9-118">Height of each vertex, in number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="d08c9-119">**Schritt**</span><span class="sxs-lookup"><span data-stu-id="d08c9-119">**Stride**</span></span>
</dt> <dd>

<span data-ttu-id="d08c9-120">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d08c9-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d08c9-121">Breite des imaginären zweidimensionalen Scheitelpunkt Arrays, das denselben Raum einnimmt wie der Scheitelpunkt Puffer.</span><span class="sxs-lookup"><span data-stu-id="d08c9-121">Width of the imaginary two-dimensional vertex array, which occupies the same space as the vertex buffer.</span></span> <span data-ttu-id="d08c9-122">Ein Beispiel finden Sie im folgenden Diagramm.</span><span class="sxs-lookup"><span data-stu-id="d08c9-122">For an example, see the diagram below.</span></span>

</dd> <dt>

<span data-ttu-id="d08c9-123">**Basis**</span><span class="sxs-lookup"><span data-stu-id="d08c9-123">**Basis**</span></span>
</dt> <dd>

<span data-ttu-id="d08c9-124">Typ: **[ **D3DBASISTYPE**](./d3dbasistype.md)**</span><span class="sxs-lookup"><span data-stu-id="d08c9-124">Type: **[**D3DBASISTYPE**](./d3dbasistype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d08c9-125">Member des [**D3DBASISTYPE**](./d3dbasistype.md) -Enumerationstyps, der den Basistyp für den rechteckigen hochwertigen Patch definiert.</span><span class="sxs-lookup"><span data-stu-id="d08c9-125">Member of the [**D3DBASISTYPE**](./d3dbasistype.md) enumerated type, defining the basis type for the rectangular high-order patch.</span></span>



| <span data-ttu-id="d08c9-126">Wert</span><span class="sxs-lookup"><span data-stu-id="d08c9-126">Value</span></span>                 | <span data-ttu-id="d08c9-127">Unterstützte Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="d08c9-127">Order supported</span></span>            | <span data-ttu-id="d08c9-128">Breite und Höhe</span><span class="sxs-lookup"><span data-stu-id="d08c9-128">Width and height</span></span>                  |
|-----------------------|----------------------------|-----------------------------------|
| <span data-ttu-id="d08c9-129">D3DBASIS \_ Bezier</span><span class="sxs-lookup"><span data-stu-id="d08c9-129">D3DBASIS\_BEZIER</span></span>      | <span data-ttu-id="d08c9-130">Linear, kubisch und quintisch</span><span class="sxs-lookup"><span data-stu-id="d08c9-130">Linear, cubic, and quintic</span></span> | <span data-ttu-id="d08c9-131">Width = Height = (DWORD) Reihenfolge + 1</span><span class="sxs-lookup"><span data-stu-id="d08c9-131">Width = height = (DWORD)order + 1</span></span> |
| <span data-ttu-id="d08c9-132">D3DBASIS \_ Bspline</span><span class="sxs-lookup"><span data-stu-id="d08c9-132">D3DBASIS\_BSPLINE</span></span>     | <span data-ttu-id="d08c9-133">Linear, kubisch und quintisch</span><span class="sxs-lookup"><span data-stu-id="d08c9-133">Linear, cubic, and quintic</span></span> | <span data-ttu-id="d08c9-134">Width = Height > Reihenfolge (DWORD)</span><span class="sxs-lookup"><span data-stu-id="d08c9-134">Width = height > (DWORD)order</span></span>  |
| <span data-ttu-id="d08c9-135">D3DBASIS \_ Interpolate</span><span class="sxs-lookup"><span data-stu-id="d08c9-135">D3DBASIS\_INTERPOLATE</span></span> | <span data-ttu-id="d08c9-136">Kilometern</span><span class="sxs-lookup"><span data-stu-id="d08c9-136">Cubic</span></span>                      | <span data-ttu-id="d08c9-137">Width = Height > Reihenfolge (DWORD)</span><span class="sxs-lookup"><span data-stu-id="d08c9-137">Width = height > (DWORD)order</span></span>  |



 

</dd> <dt>

<span data-ttu-id="d08c9-138">**Grad**</span><span class="sxs-lookup"><span data-stu-id="d08c9-138">**Degree**</span></span>
</dt> <dd>

<span data-ttu-id="d08c9-139">Typ: **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**</span><span class="sxs-lookup"><span data-stu-id="d08c9-139">Type: **[**D3DDEGREETYPE**](./d3ddegreetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d08c9-140">Member des [**D3DDEGREETYPE**](./d3ddegreetype.md) -Enumerationstyps, der den Grad für den rechteckigen Patch definiert.</span><span class="sxs-lookup"><span data-stu-id="d08c9-140">Member of the [**D3DDEGREETYPE**](./d3ddegreetype.md) enumerated type, defining the degree for the rectangular patch.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d08c9-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d08c9-141">Remarks</span></span>

<span data-ttu-id="d08c9-142">Im folgenden Diagramm werden die Parameter angegeben, die einen Rechteck Patch angeben.</span><span class="sxs-lookup"><span data-stu-id="d08c9-142">The following diagram identifies the parameters that specify a rectangle patch.</span></span>

![Diagramm eines rechteckigen hochwertigen Patches und der Parameter, die es angeben](images/hop-rectpatch.png)

<span data-ttu-id="d08c9-144">Alle Scheitel Punkte im Scheitelpunkt Puffer werden als schwarzer Punkt angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d08c9-144">Each of the vertices in the vertex buffer is shown as a black dot.</span></span> <span data-ttu-id="d08c9-145">In diesem Fall verfügt der Vertex-Puffer über 20 Vertices, von denen 16 im Rechteck Patch sind.</span><span class="sxs-lookup"><span data-stu-id="d08c9-145">In this case, the vertex buffer has 20 vertices in it, 16 of which are in the rectangle patch.</span></span> <span data-ttu-id="d08c9-146">Der Stride-Wert ist die Anzahl der Scheitel Punkte in der Breite des Scheitelpunkt Puffers (in diesem Fall fünf).</span><span class="sxs-lookup"><span data-stu-id="d08c9-146">The stride is the number of vertices in the width of the vertex buffer, in this case five.</span></span> <span data-ttu-id="d08c9-147">Der x-Offset bis zum ersten Scheitelpunkt wird startindexvertexwidth genannt und ist in diesem Fall 1.</span><span class="sxs-lookup"><span data-stu-id="d08c9-147">The x offset to the first vertex is called the StartIndexVertexWidth and is in this case 1.</span></span> <span data-ttu-id="d08c9-148">Der y-Offset für den ersten patchvertex heißt startindexvertexheight und ist in diesem Fall 0.</span><span class="sxs-lookup"><span data-stu-id="d08c9-148">The y offset to the first patch vertex is called the StartIndexVertexHeight and is in this case 0.</span></span>

<span data-ttu-id="d08c9-149">Wenn Sie einen Stream einzelner rechteckiger Patches (nicht-Mosaik) rendern möchten, sollten Sie die Geometrie als lange schmale (1 x N) rechteckige Patch interpretieren.</span><span class="sxs-lookup"><span data-stu-id="d08c9-149">To render a stream of individual rectangular patches (non-mosaic), you should interpret your geometry as a long narrow (1 x N) rectangular patch.</span></span> <span data-ttu-id="d08c9-150">Die **D3DRECTPATCH \_ Info** -Struktur für einen solchen Strip (kubische Bézier) würde wie folgt eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="d08c9-150">The **D3DRECTPATCH\_INFO** structure for such a strip (cubic Bézier) would be set up in the following manner.</span></span>


```
    
D3DRECTPATCH_INFO RectInfo;

RectInfo.Width = 4;
RectInfo.Height = 4;
RectInfo.Stride = 4;
RectInfo.Basis = D3DBASIS_BEZIER;
RectInfo.Order = D3DORDER_CUBIC;
RectInfo.StartVertexOffsetWidth = 0;
RectInfo.StartVertexOffsetHeight = 4*i;  // The variable i is the index of the 
//   patch you want to render.
```



## <a name="requirements"></a><span data-ttu-id="d08c9-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d08c9-151">Requirements</span></span>



| <span data-ttu-id="d08c9-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d08c9-152">Requirement</span></span> | <span data-ttu-id="d08c9-153">Wert</span><span class="sxs-lookup"><span data-stu-id="d08c9-153">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d08c9-154">Header</span><span class="sxs-lookup"><span data-stu-id="d08c9-154">Header</span></span><br/> | <dl> <span data-ttu-id="d08c9-155"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="d08c9-155"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d08c9-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d08c9-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d08c9-157">Direct3D-Strukturen</span><span class="sxs-lookup"><span data-stu-id="d08c9-157">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="d08c9-158">**Drawrectpatch**</span><span class="sxs-lookup"><span data-stu-id="d08c9-158">**DrawRectPatch**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch)
</dt> <dt>

[<span data-ttu-id="d08c9-159">**D3DXTessellateRectPatch**</span><span class="sxs-lookup"><span data-stu-id="d08c9-159">**D3DXTessellateRectPatch**</span></span>](d3dxtessellaterectpatch.md)
</dt> </dl>

 

 
