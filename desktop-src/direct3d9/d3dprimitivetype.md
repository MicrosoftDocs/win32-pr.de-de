---
description: Definiert die primitiven, die von Direct3D unterstützt werden.
ms.assetid: 89e697f9-02b9-4ae1-9e86-6178da0cb008
title: D3DPRIMITIVETYPE-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPRIMITIVETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 933bbec72950bd2c73fda8b3781dd46393ca4c96
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132357"
---
# <a name="d3dprimitivetype-enumeration"></a><span data-ttu-id="d2b3a-103">D3DPRIMITIVETYPE-Enumeration</span><span class="sxs-lookup"><span data-stu-id="d2b3a-103">D3DPRIMITIVETYPE enumeration</span></span>

<span data-ttu-id="d2b3a-104">Definiert die primitiven, die von Direct3D unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="d2b3a-104">Defines the primitives supported by Direct3D.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2b3a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2b3a-105">Syntax</span></span>


```C++
typedef enum D3DPRIMITIVETYPE { 
  D3DPT_POINTLIST      = 1,
  D3DPT_LINELIST       = 2,
  D3DPT_LINESTRIP      = 3,
  D3DPT_TRIANGLELIST   = 4,
  D3DPT_TRIANGLESTRIP  = 5,
  D3DPT_TRIANGLEFAN    = 6,
  D3DPT_FORCE_DWORD    = 0x7fffffff
} D3DPRIMITIVETYPE, *LPD3DPRIMITIVETYPE;
```



## <a name="constants"></a><span data-ttu-id="d2b3a-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="d2b3a-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d2b3a-107"><span id="D3DPT_POINTLIST"></span><span id="d3dpt_pointlist"></span>**D3DPT \_ PointList**</span><span class="sxs-lookup"><span data-stu-id="d2b3a-107"><span id="D3DPT_POINTLIST"></span><span id="d3dpt_pointlist"></span>**D3DPT\_POINTLIST**</span></span>
</dt> <dd>

<span data-ttu-id="d2b3a-108">Rendert die Scheitel Punkte als Auflistung isolierter Punkte.</span><span class="sxs-lookup"><span data-stu-id="d2b3a-108">Renders the vertices as a collection of isolated points.</span></span> <span data-ttu-id="d2b3a-109">Dieser Wert wird für indizierte primitive nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d2b3a-109">This value is unsupported for indexed primitives.</span></span>

</dd> <dt>

<span data-ttu-id="d2b3a-110"><span id="D3DPT_LINELIST"></span><span id="d3dpt_linelist"></span>**D3DPT- \_ LineList**</span><span class="sxs-lookup"><span data-stu-id="d2b3a-110"><span id="D3DPT_LINELIST"></span><span id="d3dpt_linelist"></span>**D3DPT\_LINELIST**</span></span>
</dt> <dd>

<span data-ttu-id="d2b3a-111">Rendert die Scheitel Punkte als Liste der isolierten geraden Liniensegmente.</span><span class="sxs-lookup"><span data-stu-id="d2b3a-111">Renders the vertices as a list of isolated straight line segments.</span></span>

</dd> <dt>

<span data-ttu-id="d2b3a-112"><span id="D3DPT_LINESTRIP"></span><span id="d3dpt_linestrip"></span>**D3DPT \_ linestrip**</span><span class="sxs-lookup"><span data-stu-id="d2b3a-112"><span id="D3DPT_LINESTRIP"></span><span id="d3dpt_linestrip"></span>**D3DPT\_LINESTRIP**</span></span>
</dt> <dd>

<span data-ttu-id="d2b3a-113">Rendert die Scheitel Punkte als eine einzelne Polylinie.</span><span class="sxs-lookup"><span data-stu-id="d2b3a-113">Renders the vertices as a single polyline.</span></span>

</dd> <dt>

<span data-ttu-id="d2b3a-114"><span id="D3DPT_TRIANGLELIST"></span><span id="d3dpt_trianglelist"></span>**D3DPT- \_ Liste**</span><span class="sxs-lookup"><span data-stu-id="d2b3a-114"><span id="D3DPT_TRIANGLELIST"></span><span id="d3dpt_trianglelist"></span>**D3DPT\_TRIANGLELIST**</span></span>
</dt> <dd>

<span data-ttu-id="d2b3a-115">Rendert die angegebenen Scheitel Punkte als Sequenz isolierter Dreiecke.</span><span class="sxs-lookup"><span data-stu-id="d2b3a-115">Renders the specified vertices as a sequence of isolated triangles.</span></span> <span data-ttu-id="d2b3a-116">Jede Gruppe von drei Vertices definiert ein separates Dreieck.</span><span class="sxs-lookup"><span data-stu-id="d2b3a-116">Each group of three vertices defines a separate triangle.</span></span>

<span data-ttu-id="d2b3a-117">Der aktuelle renderingstatus wirkt sich auf die Hintergrund Erkennung aus.</span><span class="sxs-lookup"><span data-stu-id="d2b3a-117">Back-face culling is affected by the current winding-order render state.</span></span>

</dd> <dt>

<span data-ttu-id="d2b3a-118"><span id="D3DPT_TRIANGLESTRIP"></span><span id="d3dpt_trianglestrip"></span>**D3DPT-Test \_ Strip**</span><span class="sxs-lookup"><span data-stu-id="d2b3a-118"><span id="D3DPT_TRIANGLESTRIP"></span><span id="d3dpt_trianglestrip"></span>**D3DPT\_TRIANGLESTRIP**</span></span>
</dt> <dd>

<span data-ttu-id="d2b3a-119">Rendert die Scheitel Punkte als Dreiecks Streifen.</span><span class="sxs-lookup"><span data-stu-id="d2b3a-119">Renders the vertices as a triangle strip.</span></span> <span data-ttu-id="d2b3a-120">Das Flag für die Hintergrund Erkennung wird automatisch bei geraden Dreiecke gekippt.</span><span class="sxs-lookup"><span data-stu-id="d2b3a-120">The backface-culling flag is automatically flipped on even-numbered triangles.</span></span>

</dd> <dt>

<span data-ttu-id="d2b3a-121"><span id="D3DPT_TRIANGLEFAN"></span><span id="d3dpt_trianglefan"></span>**D3DPT \_ -Test**</span><span class="sxs-lookup"><span data-stu-id="d2b3a-121"><span id="D3DPT_TRIANGLEFAN"></span><span id="d3dpt_trianglefan"></span>**D3DPT\_TRIANGLEFAN**</span></span>
</dt> <dd>

<span data-ttu-id="d2b3a-122">Rendert die Scheitel Punkte als Dreiecks Lüfter.</span><span class="sxs-lookup"><span data-stu-id="d2b3a-122">Renders the vertices as a triangle fan.</span></span>

</dd> <dt>

<span data-ttu-id="d2b3a-123"><span id="D3DPT_FORCE_DWORD"></span><span id="d3dpt_force_dword"></span>**D3DPT \_ Erzwingen von \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="d2b3a-123"><span id="D3DPT_FORCE_DWORD"></span><span id="d3dpt_force_dword"></span>**D3DPT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="d2b3a-124">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="d2b3a-124">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="d2b3a-125">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="d2b3a-125">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="d2b3a-126">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d2b3a-126">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d2b3a-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d2b3a-127">Remarks</span></span>

<span data-ttu-id="d2b3a-128">Die Verwendung von [Dreiecks Streifen](triangle-strips.md) oder [Dreiecks Lüfter (Direct3D 9)](triangle-fans.md) ist oft effizienter als die Verwendung von Dreiecks Listen, da weniger Vertices dupliziert werden.</span><span class="sxs-lookup"><span data-stu-id="d2b3a-128">Using [Triangle Strips](triangle-strips.md) or [Triangle Fans (Direct3D 9)](triangle-fans.md) is often more efficient than using triangle lists because fewer vertices are duplicated.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2b3a-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d2b3a-129">Requirements</span></span>



| <span data-ttu-id="d2b3a-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d2b3a-130">Requirement</span></span> | <span data-ttu-id="d2b3a-131">Wert</span><span class="sxs-lookup"><span data-stu-id="d2b3a-131">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2b3a-132">Header</span><span class="sxs-lookup"><span data-stu-id="d2b3a-132">Header</span></span><br/> | <dl> <span data-ttu-id="d2b3a-133"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2b3a-133"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2b3a-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d2b3a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2b3a-135">Direct3D-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="d2b3a-135">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="d2b3a-136">**IDirect3DDevice9::D rawindexedprimitiv**</span><span class="sxs-lookup"><span data-stu-id="d2b3a-136">**IDirect3DDevice9::DrawIndexedPrimitive**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)
</dt> <dt>

[<span data-ttu-id="d2b3a-137">**IDirect3DDevice9::D rawindexedprimitiveup**</span><span class="sxs-lookup"><span data-stu-id="d2b3a-137">**IDirect3DDevice9::DrawIndexedPrimitiveUP**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitiveup)
</dt> <dt>

[<span data-ttu-id="d2b3a-138">**IDirect3DDevice9::D rawprimitiv**</span><span class="sxs-lookup"><span data-stu-id="d2b3a-138">**IDirect3DDevice9::DrawPrimitive**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)
</dt> <dt>

[<span data-ttu-id="d2b3a-139">**IDirect3DDevice9::D rawprimitiveup**</span><span class="sxs-lookup"><span data-stu-id="d2b3a-139">**IDirect3DDevice9::DrawPrimitiveUP**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitiveup)
</dt> </dl>

 

 
