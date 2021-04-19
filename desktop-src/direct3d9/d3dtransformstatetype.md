---
description: Definiert Konstanten, die Transformations Zustands Werte beschreiben.
ms.assetid: 53535d9f-246a-42cf-82a2-fb3cf6d4ebac
title: D3DTRANSFORMSTATETYPE-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTRANSFORMSTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: c618e0e19bf7dd01dec73d35436f23189f9e78a6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366631"
---
# <a name="d3dtransformstatetype-enumeration"></a><span data-ttu-id="8216a-103">D3DTRANSFORMSTATETYPE-Enumeration</span><span class="sxs-lookup"><span data-stu-id="8216a-103">D3DTRANSFORMSTATETYPE enumeration</span></span>

<span data-ttu-id="8216a-104">Definiert Konstanten, die Transformations Zustands Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="8216a-104">Defines constants that describe transformation state values.</span></span>

## <a name="syntax"></a><span data-ttu-id="8216a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8216a-105">Syntax</span></span>


```C++
typedef enum D3DTRANSFORMSTATETYPE { 
  D3DTS_VIEW         = 2,
  D3DTS_PROJECTION   = 3,
  D3DTS_TEXTURE0     = 16,
  D3DTS_TEXTURE1     = 17,
  D3DTS_TEXTURE2     = 18,
  D3DTS_TEXTURE3     = 19,
  D3DTS_TEXTURE4     = 20,
  D3DTS_TEXTURE5     = 21,
  D3DTS_TEXTURE6     = 22,
  D3DTS_TEXTURE7     = 23,
  D3DTS_FORCE_DWORD  = 0x7fffffff
} D3DTRANSFORMSTATETYPE, *LPD3DTRANSFORMSTATETYPE;
```



## <a name="constants"></a><span data-ttu-id="8216a-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="8216a-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8216a-107"><span id="D3DTS_VIEW"></span><span id="d3dts_view"></span>**D3DTS- \_ Sicht**</span><span class="sxs-lookup"><span data-stu-id="8216a-107"><span id="D3DTS_VIEW"></span><span id="d3dts_view"></span>**D3DTS\_VIEW**</span></span>
</dt> <dd>

<span data-ttu-id="8216a-108">Gibt an, dass die Transformationsmatrix als Transformationsmatrix der Sicht festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="8216a-108">Identifies the transformation matrix being set as the view transformation matrix.</span></span> <span data-ttu-id="8216a-109">Der Standardwert ist **null** (die Identitätsmatrix).</span><span class="sxs-lookup"><span data-stu-id="8216a-109">The default value is **NULL** (the identity matrix).</span></span>

</dd> <dt>

<span data-ttu-id="8216a-110"><span id="D3DTS_PROJECTION"></span><span id="d3dts_projection"></span>**D3DTS- \_ Projektion**</span><span class="sxs-lookup"><span data-stu-id="8216a-110"><span id="D3DTS_PROJECTION"></span><span id="d3dts_projection"></span>**D3DTS\_PROJECTION**</span></span>
</dt> <dd>

<span data-ttu-id="8216a-111">Gibt an, dass die Transformationsmatrix als Projektions Transformationsmatrix festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="8216a-111">Identifies the transformation matrix being set as the projection transformation matrix.</span></span> <span data-ttu-id="8216a-112">Der Standardwert ist **null** (die Identitätsmatrix).</span><span class="sxs-lookup"><span data-stu-id="8216a-112">The default value is **NULL** (the identity matrix).</span></span>

</dd> <dt>

<span data-ttu-id="8216a-113"><span id="D3DTS_TEXTURE0"></span><span id="d3dts_texture0"></span>**D3DTS \_ TEXTURE0**</span><span class="sxs-lookup"><span data-stu-id="8216a-113"><span id="D3DTS_TEXTURE0"></span><span id="d3dts_texture0"></span>**D3DTS\_TEXTURE0**</span></span>
</dt> <dd>

<span data-ttu-id="8216a-114">Gibt die Transformationsmatrix an, die für die angegebene Textur Phase festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="8216a-114">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="8216a-115"><span id="D3DTS_TEXTURE1"></span><span id="d3dts_texture1"></span>**D3DTS \_ TEXTURE1**</span><span class="sxs-lookup"><span data-stu-id="8216a-115"><span id="D3DTS_TEXTURE1"></span><span id="d3dts_texture1"></span>**D3DTS\_TEXTURE1**</span></span>
</dt> <dd>

<span data-ttu-id="8216a-116">Gibt die Transformationsmatrix an, die für die angegebene Textur Phase festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="8216a-116">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="8216a-117"><span id="D3DTS_TEXTURE2"></span><span id="d3dts_texture2"></span>**D3DTS \_ Texture2 fest**</span><span class="sxs-lookup"><span data-stu-id="8216a-117"><span id="D3DTS_TEXTURE2"></span><span id="d3dts_texture2"></span>**D3DTS\_TEXTURE2**</span></span>
</dt> <dd>

<span data-ttu-id="8216a-118">Gibt die Transformationsmatrix an, die für die angegebene Textur Phase festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="8216a-118">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="8216a-119"><span id="D3DTS_TEXTURE3"></span><span id="d3dts_texture3"></span>**D3DTS \_ TEXTURE3**</span><span class="sxs-lookup"><span data-stu-id="8216a-119"><span id="D3DTS_TEXTURE3"></span><span id="d3dts_texture3"></span>**D3DTS\_TEXTURE3**</span></span>
</dt> <dd>

<span data-ttu-id="8216a-120">Gibt die Transformationsmatrix an, die für die angegebene Textur Phase festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="8216a-120">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="8216a-121"><span id="D3DTS_TEXTURE4"></span><span id="d3dts_texture4"></span>**D3DTS \_ TEXTURE4**</span><span class="sxs-lookup"><span data-stu-id="8216a-121"><span id="D3DTS_TEXTURE4"></span><span id="d3dts_texture4"></span>**D3DTS\_TEXTURE4**</span></span>
</dt> <dd>

<span data-ttu-id="8216a-122">Gibt die Transformationsmatrix an, die für die angegebene Textur Phase festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="8216a-122">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="8216a-123"><span id="D3DTS_TEXTURE5"></span><span id="d3dts_texture5"></span>**D3DTS \_ TEXTURE5**</span><span class="sxs-lookup"><span data-stu-id="8216a-123"><span id="D3DTS_TEXTURE5"></span><span id="d3dts_texture5"></span>**D3DTS\_TEXTURE5**</span></span>
</dt> <dd>

<span data-ttu-id="8216a-124">Gibt die Transformationsmatrix an, die für die angegebene Textur Phase festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="8216a-124">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="8216a-125"><span id="D3DTS_TEXTURE6"></span><span id="d3dts_texture6"></span>**D3DTS \_ TEXTURE6**</span><span class="sxs-lookup"><span data-stu-id="8216a-125"><span id="D3DTS_TEXTURE6"></span><span id="d3dts_texture6"></span>**D3DTS\_TEXTURE6**</span></span>
</dt> <dd>

<span data-ttu-id="8216a-126">Gibt die Transformationsmatrix an, die für die angegebene Textur Phase festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="8216a-126">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="8216a-127"><span id="D3DTS_TEXTURE7"></span><span id="d3dts_texture7"></span>**D3DTS \_ TEXTURE7**</span><span class="sxs-lookup"><span data-stu-id="8216a-127"><span id="D3DTS_TEXTURE7"></span><span id="d3dts_texture7"></span>**D3DTS\_TEXTURE7**</span></span>
</dt> <dd>

<span data-ttu-id="8216a-128">Gibt die Transformationsmatrix an, die für die angegebene Textur Phase festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="8216a-128">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="8216a-129"><span id="D3DTS_FORCE_DWORD"></span><span id="d3dts_force_dword"></span>**D3DTS \_ Erzwingen von \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="8216a-129"><span id="D3DTS_FORCE_DWORD"></span><span id="d3dts_force_dword"></span>**D3DTS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="8216a-130">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="8216a-130">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="8216a-131">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="8216a-131">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="8216a-132">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="8216a-132">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8216a-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8216a-133">Remarks</span></span>

<span data-ttu-id="8216a-134">Die Transformations Zustände im Bereich 256 bis 511 sind zum Speichern von bis zu 256 World Matrizen reserviert, die mithilfe der \_ Makros D3DTS worldmatrix und D3DTS World indiziert werden können \_ .</span><span class="sxs-lookup"><span data-stu-id="8216a-134">The transform states in the range 256 through 511 are reserved to store up to 256 world matrices that can be indexed using the D3DTS\_WORLDMATRIX and D3DTS\_WORLD macros.</span></span>



| <span data-ttu-id="8216a-135">Makros</span><span class="sxs-lookup"><span data-stu-id="8216a-135">Macros</span></span>                                                  |                                                                                                                                                                       |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8216a-136">**D3DTS \_ Welt**</span><span class="sxs-lookup"><span data-stu-id="8216a-136">**D3DTS\_WORLD**</span></span>](d3dts-world.md)                     | <span data-ttu-id="8216a-137">Entspricht D3DTS \_ worldmatrix (0).</span><span class="sxs-lookup"><span data-stu-id="8216a-137">Equivalent to D3DTS\_WORLDMATRIX(0).</span></span>                                                                                                                                  |
| <span data-ttu-id="8216a-138">[**D3DTS \_ Worldmatrix**](d3dts-worldmatrix.md) (Index)</span><span class="sxs-lookup"><span data-stu-id="8216a-138">[**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) (index)</span></span> | <span data-ttu-id="8216a-139">Gibt die Transformationsmatrix an, die für die Weltmatrix beim Index festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8216a-139">Identifies the transform matrix to set for the world matrix at index.</span></span> <span data-ttu-id="8216a-140">Mehrere Welt Matrizen werden nur für Vertex-Blending verwendet.</span><span class="sxs-lookup"><span data-stu-id="8216a-140">Multiple world matrices are used only for vertex blending.</span></span> <span data-ttu-id="8216a-141">Andernfalls wird nur D3DTS \_ World verwendet.</span><span class="sxs-lookup"><span data-stu-id="8216a-141">Otherwise only D3DTS\_WORLD is used.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="8216a-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8216a-142">Requirements</span></span>



| <span data-ttu-id="8216a-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8216a-143">Requirement</span></span> | <span data-ttu-id="8216a-144">Wert</span><span class="sxs-lookup"><span data-stu-id="8216a-144">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8216a-145">Header</span><span class="sxs-lookup"><span data-stu-id="8216a-145">Header</span></span><br/> | <dl> <span data-ttu-id="8216a-146"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="8216a-146"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8216a-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8216a-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8216a-148">Direct3D-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="8216a-148">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="8216a-149">**IDirect3DDevice9:: GetTransform**</span><span class="sxs-lookup"><span data-stu-id="8216a-149">**IDirect3DDevice9::GetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettransform)
</dt> <dt>

[<span data-ttu-id="8216a-150">**IDirect3DDevice9:: MultiplyTransform**</span><span class="sxs-lookup"><span data-stu-id="8216a-150">**IDirect3DDevice9::MultiplyTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-multiplytransform)
</dt> <dt>

[<span data-ttu-id="8216a-151">**IDirect3DDevice9:: setTransform**</span><span class="sxs-lookup"><span data-stu-id="8216a-151">**IDirect3DDevice9::SetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

[<span data-ttu-id="8216a-152">**D3DTS \_ Welt**</span><span class="sxs-lookup"><span data-stu-id="8216a-152">**D3DTS\_WORLD**</span></span>](d3dts-world.md)
</dt> <dt>

[<span data-ttu-id="8216a-153">**D3DTS \_ worldn**</span><span class="sxs-lookup"><span data-stu-id="8216a-153">**D3DTS\_WORLDn**</span></span>](d3dts-worldn.md)
</dt> <dt>

[<span data-ttu-id="8216a-154">**D3DTS \_ worldmatrix**</span><span class="sxs-lookup"><span data-stu-id="8216a-154">**D3DTS\_WORLDMATRIX**</span></span>](d3dts-worldmatrix.md)
</dt> </dl>

 

 
