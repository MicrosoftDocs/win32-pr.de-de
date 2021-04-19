---
description: Definiert die Fenster Dimensionen einer Renderziel-Oberfläche, auf die ein 3D-Volume projiziert wird.
ms.assetid: fb2c6048-f837-497d-8e4f-e18942d37899
title: D3DVIEWPORT9-Struktur (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVIEWPORT9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3d96000de50934ebdc893ffc3866dd3252703bdc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367382"
---
# <a name="d3dviewport9-structure"></a><span data-ttu-id="3bae9-103">D3DVIEWPORT9-Struktur</span><span class="sxs-lookup"><span data-stu-id="3bae9-103">D3DVIEWPORT9 structure</span></span>

<span data-ttu-id="3bae9-104">Definiert die Fenster Dimensionen einer Renderziel-Oberfläche, auf die ein 3D-Volume projiziert wird.</span><span class="sxs-lookup"><span data-stu-id="3bae9-104">Defines the window dimensions of a render-target surface onto which a 3D volume projects.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bae9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3bae9-105">Syntax</span></span>


```C++
typedef struct D3DVIEWPORT9 {
  DWORD X;
  DWORD Y;
  DWORD Width;
  DWORD Height;
  float MinZ;
  float MaxZ;
} D3DVIEWPORT9, *LPD3DVIEWPORT9;
```



## <a name="members"></a><span data-ttu-id="3bae9-106">Member</span><span class="sxs-lookup"><span data-stu-id="3bae9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="3bae9-107">**X**</span><span class="sxs-lookup"><span data-stu-id="3bae9-107">**X**</span></span>
</dt> <dd>

<span data-ttu-id="3bae9-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3bae9-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3bae9-109">Die Pixel Koordinate der oberen linken Ecke des Viewports auf der renderzieloberfläche.</span><span class="sxs-lookup"><span data-stu-id="3bae9-109">Pixel coordinate of the upper-left corner of the viewport on the render-target surface.</span></span> <span data-ttu-id="3bae9-110">Dieser Member kann auf 0 festgelegt werden, es sei denn, Sie möchten zu einer Teilmenge der-Oberfläche rendert werden.</span><span class="sxs-lookup"><span data-stu-id="3bae9-110">Unless you want to render to a subset of the surface, this member can be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="3bae9-111">**J**</span><span class="sxs-lookup"><span data-stu-id="3bae9-111">**Y**</span></span>
</dt> <dd>

<span data-ttu-id="3bae9-112">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3bae9-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3bae9-113">Die Pixel Koordinate der oberen linken Ecke des Viewports auf der renderzieloberfläche.</span><span class="sxs-lookup"><span data-stu-id="3bae9-113">Pixel coordinate of the upper-left corner of the viewport on the render-target surface.</span></span> <span data-ttu-id="3bae9-114">Dieser Member kann auf 0 festgelegt werden, es sei denn, Sie möchten zu einer Teilmenge der-Oberfläche rendert werden.</span><span class="sxs-lookup"><span data-stu-id="3bae9-114">Unless you want to render to a subset of the surface, this member can be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="3bae9-115">**Width**</span><span class="sxs-lookup"><span data-stu-id="3bae9-115">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="3bae9-116">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3bae9-116">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3bae9-117">Die Width-Dimension des Clip-Volumes in Pixel.</span><span class="sxs-lookup"><span data-stu-id="3bae9-117">Width dimension of the clip volume, in pixels.</span></span> <span data-ttu-id="3bae9-118">Wenn Sie nur eine Teilmenge der-Oberfläche rendern, sollte dieser Member auf die Width-Dimension der renderzieloberfläche festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3bae9-118">Unless you are rendering only to a subset of the surface, this member should be set to the width dimension of the render-target surface.</span></span>

</dd> <dt>

<span data-ttu-id="3bae9-119">**Height**</span><span class="sxs-lookup"><span data-stu-id="3bae9-119">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="3bae9-120">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3bae9-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3bae9-121">Height-Dimension des Clip Volumes in Pixel.</span><span class="sxs-lookup"><span data-stu-id="3bae9-121">Height dimension of the clip volume, in pixels.</span></span> <span data-ttu-id="3bae9-122">Wenn Sie nur eine Teilmenge der-Oberfläche rendern, sollte dieser Member auf die Height-Dimension der renderzieloberfläche festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3bae9-122">Unless you are rendering only to a subset of the surface, this member should be set to the height dimension of the render-target surface.</span></span>

</dd> <dt>

<span data-ttu-id="3bae9-123">**Minz**</span><span class="sxs-lookup"><span data-stu-id="3bae9-123">**MinZ**</span></span>
</dt> <dd>

<span data-ttu-id="3bae9-124">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="3bae9-124">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="3bae9-125">Mit MaxZ können Sie den Bereich der tiefen Werte beschreiben, in die eine Szene gerendert werden soll, den minimalen und maximalen Wert des Clip-Volumes.</span><span class="sxs-lookup"><span data-stu-id="3bae9-125">Together with MaxZ, value describing the range of depth values into which a scene is to be rendered, the minimum and maximum values of the clip volume.</span></span> <span data-ttu-id="3bae9-126">Die meisten Anwendungen legen diesen Wert auf 0,0 fest.</span><span class="sxs-lookup"><span data-stu-id="3bae9-126">Most applications set this value to 0.0.</span></span> <span data-ttu-id="3bae9-127">Das Clipping erfolgt nach dem Anwenden der Projektions Matrix.</span><span class="sxs-lookup"><span data-stu-id="3bae9-127">Clipping is performed after applying the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="3bae9-128">**MaxZ**</span><span class="sxs-lookup"><span data-stu-id="3bae9-128">**MaxZ**</span></span>
</dt> <dd>

<span data-ttu-id="3bae9-129">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="3bae9-129">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="3bae9-130">Mit Minz, dem Wert, der den Bereich der tiefen Werte beschreibt, in den eine Szene gerendert werden soll, dem minimalen und maximalen Wert des Clip-Volumes.</span><span class="sxs-lookup"><span data-stu-id="3bae9-130">Together with MinZ, value describing the range of depth values into which a scene is to be rendered, the minimum and maximum values of the clip volume.</span></span> <span data-ttu-id="3bae9-131">Die meisten Anwendungen legen diesen Wert auf 1,0 fest.</span><span class="sxs-lookup"><span data-stu-id="3bae9-131">Most applications set this value to 1.0.</span></span> <span data-ttu-id="3bae9-132">Das Clipping erfolgt nach dem Anwenden der Projektions Matrix.</span><span class="sxs-lookup"><span data-stu-id="3bae9-132">Clipping is performed after applying the projection matrix.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3bae9-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3bae9-133">Remarks</span></span>

<span data-ttu-id="3bae9-134">Die Elemente X, Y, Width und Height beschreiben die Position und die Dimensionen des Viewports auf der renderzieloberfläche.</span><span class="sxs-lookup"><span data-stu-id="3bae9-134">The X, Y, Width, and Height members describe the position and dimensions of the viewport on the render-target surface.</span></span> <span data-ttu-id="3bae9-135">Normalerweise renderanwendungen auf der gesamten Ziel Oberfläche. beim Rendern auf einer 640 x 480-Oberfläche sollten diese Member jeweils 0, 0, 640 und 480 sein.</span><span class="sxs-lookup"><span data-stu-id="3bae9-135">Usually, applications render to the entire target surface; when rendering on a 640 x 480 surface, these members should be 0, 0, 640, and 480, respectively.</span></span> <span data-ttu-id="3bae9-136">Minz und MaxZ sind in der Regel auf 0,0 und 1,0 festgelegt, können jedoch auf andere Werte festgelegt werden, um bestimmte Effekte zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="3bae9-136">The MinZ and MaxZ are typically set to 0.0 and 1.0 but can be set to other values to achieve specific effects.</span></span> <span data-ttu-id="3bae9-137">Sie können Sie z. b. auf 0,0 festlegen, um zu erzwingen, dass das Systemobjekte im Vordergrund einer Szene oder beides auf 1,0, um die Objekte im Hintergrund zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="3bae9-137">For example, you might set them both to 0.0 to force the system to render objects to the foreground of a scene, or both to 1.0 to force the objects into the background.</span></span>

<span data-ttu-id="3bae9-138">Wenn die Viewport-Parameter für ein Gerät geändert werden (aufgrund eines Aufrufes der [**setviewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport) -Methode), erstellt der Treiber eine neue Transformationsmatrix.</span><span class="sxs-lookup"><span data-stu-id="3bae9-138">When the viewport parameters for a device change (because of a call to the [**SetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport) method), the driver builds a new transformation matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bae9-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3bae9-139">Requirements</span></span>



| <span data-ttu-id="3bae9-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3bae9-140">Requirement</span></span> | <span data-ttu-id="3bae9-141">Wert</span><span class="sxs-lookup"><span data-stu-id="3bae9-141">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3bae9-142">Header</span><span class="sxs-lookup"><span data-stu-id="3bae9-142">Header</span></span><br/> | <dl> <span data-ttu-id="3bae9-143"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="3bae9-143"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bae9-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3bae9-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bae9-145">Direct3D-Strukturen</span><span class="sxs-lookup"><span data-stu-id="3bae9-145">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="3bae9-146">**Getviewport**</span><span class="sxs-lookup"><span data-stu-id="3bae9-146">**GetViewport**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getviewport)
</dt> <dt>

[<span data-ttu-id="3bae9-147">**Setviewport**</span><span class="sxs-lookup"><span data-stu-id="3bae9-147">**SetViewport**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport)
</dt> </dl>

 

 
