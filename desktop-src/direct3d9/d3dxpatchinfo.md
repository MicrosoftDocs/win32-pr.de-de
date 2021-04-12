---
description: -Struktur, die die Attribute eines patchnetzes enthält.
ms.assetid: aaea69c9-2d33-46e8-bc26-95daf65abf50
title: D3DXPATCHINFO-Struktur (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPATCHINFO
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 8628cc27a0223580aa1f8072750f4c31a176533e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354146"
---
# <a name="d3dxpatchinfo-structure"></a><span data-ttu-id="fc44c-103">D3DXPATCHINFO-Struktur</span><span class="sxs-lookup"><span data-stu-id="fc44c-103">D3DXPATCHINFO structure</span></span>

<span data-ttu-id="fc44c-104">-Struktur, die die Attribute eines patchnetzes enthält.</span><span class="sxs-lookup"><span data-stu-id="fc44c-104">Structure that contains the attributes of a patch mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc44c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fc44c-105">Syntax</span></span>


```C++
typedef struct D3DXPATCHINFO {
  D3DXPATCHMESHTYPE PatchType;
  D3DDEGREETYPE     Degree;
  D3DBASISTYPE      Basis;
} D3DXPATCHINFO, *LPD3DXPATCHINFO;
```



## <a name="members"></a><span data-ttu-id="fc44c-106">Member</span><span class="sxs-lookup"><span data-stu-id="fc44c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="fc44c-107">**Patchtyp**</span><span class="sxs-lookup"><span data-stu-id="fc44c-107">**PatchType**</span></span>
</dt> <dd>

<span data-ttu-id="fc44c-108">Typ: **[ **D3DXPATCHMESHTYPE**](./d3dxpatchmeshtype.md)**</span><span class="sxs-lookup"><span data-stu-id="fc44c-108">Type: **[**D3DXPATCHMESHTYPE**](./d3dxpatchmeshtype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fc44c-109">Der patchetyp.</span><span class="sxs-lookup"><span data-stu-id="fc44c-109">The patch type.</span></span> <span data-ttu-id="fc44c-110">Weitere Informationen zu Patchtypen finden Sie unter [**D3DXPATCHMESHTYPE**](./d3dxpatchmeshtype.md).</span><span class="sxs-lookup"><span data-stu-id="fc44c-110">For information about patch types, see [**D3DXPATCHMESHTYPE**](./d3dxpatchmeshtype.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc44c-111">**Grad**</span><span class="sxs-lookup"><span data-stu-id="fc44c-111">**Degree**</span></span>
</dt> <dd>

<span data-ttu-id="fc44c-112">Typ: **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**</span><span class="sxs-lookup"><span data-stu-id="fc44c-112">Type: **[**D3DDEGREETYPE**](./d3ddegreetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fc44c-113">Grad der Kurven, die zum Erstellen des Patches verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fc44c-113">Degree of the curves used to construct the patch.</span></span> <span data-ttu-id="fc44c-114">Informationen zu den unterstützten Graden finden Sie unter [**D3DDEGREETYPE**](./d3ddegreetype.md).</span><span class="sxs-lookup"><span data-stu-id="fc44c-114">For information about the degrees supported, see [**D3DDEGREETYPE**](./d3ddegreetype.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc44c-115">**Basis**</span><span class="sxs-lookup"><span data-stu-id="fc44c-115">**Basis**</span></span>
</dt> <dd>

<span data-ttu-id="fc44c-116">Typ: **[ **D3DBASISTYPE**](./d3dbasistype.md)**</span><span class="sxs-lookup"><span data-stu-id="fc44c-116">Type: **[**D3DBASISTYPE**](./d3dbasistype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fc44c-117">Der Typ der Kurve, der zum Erstellen des Patches verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="fc44c-117">Type of curve used to construct the patch.</span></span> <span data-ttu-id="fc44c-118">Informationen zu den unterstützten Basis Typen finden Sie unter [**D3DBASISTYPE**](./d3dbasistype.md).</span><span class="sxs-lookup"><span data-stu-id="fc44c-118">For information about the basis types supported, see [**D3DBASISTYPE**](./d3dbasistype.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fc44c-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fc44c-119">Remarks</span></span>

<span data-ttu-id="fc44c-120">Ein Mesh ist ein Satz von Gesichtern, von denen jeder von einem einfachen Polygon beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="fc44c-120">A mesh is a set of faces, each of which is described by a simple polygon.</span></span> <span data-ttu-id="fc44c-121">Objekte können erstellt werden, indem mehrere Netze miteinander verbunden werden.</span><span class="sxs-lookup"><span data-stu-id="fc44c-121">Objects can be created by connecting several meshes together.</span></span> <span data-ttu-id="fc44c-122">Ein patchmesh wird aus Patches erstellt.</span><span class="sxs-lookup"><span data-stu-id="fc44c-122">A patch mesh is constructed from patches.</span></span> <span data-ttu-id="fc44c-123">Ein Patch ist ein vierseitiges Geometrie Element, das aus Kurven erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="fc44c-123">A patch is a four-sided piece of geometry constructed from curves.</span></span> <span data-ttu-id="fc44c-124">Der Typ der verwendeten Kurve und die Reihenfolge der Kurve können variiert werden, sodass die patchoberfläche fast alle Oberflächen Formen passt.</span><span class="sxs-lookup"><span data-stu-id="fc44c-124">The type of curve used and the order of the curve can be varied so that the patch surface will fit almost any surface shape.</span></span>

<span data-ttu-id="fc44c-125">Die folgenden Typen von Patchkombinationen werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="fc44c-125">The following types of patch combinations are supported:</span></span>



| <span data-ttu-id="fc44c-126">Patchetyp</span><span class="sxs-lookup"><span data-stu-id="fc44c-126">Patch Type</span></span> | <span data-ttu-id="fc44c-127">Basis</span><span class="sxs-lookup"><span data-stu-id="fc44c-127">Basis</span></span>       | <span data-ttu-id="fc44c-128">Grad</span><span class="sxs-lookup"><span data-stu-id="fc44c-128">Degree</span></span> |
|------------|-------------|--------|
| <span data-ttu-id="fc44c-129">Rechteck</span><span class="sxs-lookup"><span data-stu-id="fc44c-129">Rectangle</span></span>  | <span data-ttu-id="fc44c-130">Bézier</span><span class="sxs-lookup"><span data-stu-id="fc44c-130">Bezier</span></span>      | <span data-ttu-id="fc44c-131">2, 3, 5</span><span class="sxs-lookup"><span data-stu-id="fc44c-131">2,3,5</span></span>  |
| <span data-ttu-id="fc44c-132">Rechteck</span><span class="sxs-lookup"><span data-stu-id="fc44c-132">Rectangle</span></span>  | <span data-ttu-id="fc44c-133">B-Spline</span><span class="sxs-lookup"><span data-stu-id="fc44c-133">B-Spline</span></span>    | <span data-ttu-id="fc44c-134">2, 3, 5</span><span class="sxs-lookup"><span data-stu-id="fc44c-134">2,3,5</span></span>  |
| <span data-ttu-id="fc44c-135">Rechteck</span><span class="sxs-lookup"><span data-stu-id="fc44c-135">Rectangle</span></span>  | <span data-ttu-id="fc44c-136">Catmull-Rom</span><span class="sxs-lookup"><span data-stu-id="fc44c-136">Catmull-Rom</span></span> | <span data-ttu-id="fc44c-137">3</span><span class="sxs-lookup"><span data-stu-id="fc44c-137">3</span></span>      |
| <span data-ttu-id="fc44c-138">Triangle</span><span class="sxs-lookup"><span data-stu-id="fc44c-138">Triangle</span></span>   | <span data-ttu-id="fc44c-139">Bézier</span><span class="sxs-lookup"><span data-stu-id="fc44c-139">Bezier</span></span>      | <span data-ttu-id="fc44c-140">2, 3, 5</span><span class="sxs-lookup"><span data-stu-id="fc44c-140">2,3,5</span></span>  |
| <span data-ttu-id="fc44c-141">N-Patch</span><span class="sxs-lookup"><span data-stu-id="fc44c-141">N-patch</span></span>    | <span data-ttu-id="fc44c-142">–</span><span class="sxs-lookup"><span data-stu-id="fc44c-142">N/A</span></span>         | <span data-ttu-id="fc44c-143">3</span><span class="sxs-lookup"><span data-stu-id="fc44c-143">3</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="fc44c-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fc44c-144">Requirements</span></span>



| <span data-ttu-id="fc44c-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fc44c-145">Requirement</span></span> | <span data-ttu-id="fc44c-146">Wert</span><span class="sxs-lookup"><span data-stu-id="fc44c-146">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc44c-147">Header</span><span class="sxs-lookup"><span data-stu-id="fc44c-147">Header</span></span><br/> | <dl> <span data-ttu-id="fc44c-148"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc44c-148"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc44c-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fc44c-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc44c-150">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="fc44c-150">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="fc44c-151">**D3DRECTPATCH \_ Info**</span><span class="sxs-lookup"><span data-stu-id="fc44c-151">**D3DRECTPATCH\_INFO**</span></span>](d3drectpatch-info.md)
</dt> <dt>

[<span data-ttu-id="fc44c-152">**D3DTRIPATCH \_ Info**</span><span class="sxs-lookup"><span data-stu-id="fc44c-152">**D3DTRIPATCH\_INFO**</span></span>](d3dtripatch-info.md)
</dt> <dt>

[<span data-ttu-id="fc44c-153">**D3DXCreatePatchMesh**</span><span class="sxs-lookup"><span data-stu-id="fc44c-153">**D3DXCreatePatchMesh**</span></span>](d3dxcreatepatchmesh.md)
</dt> </dl>

 

 
