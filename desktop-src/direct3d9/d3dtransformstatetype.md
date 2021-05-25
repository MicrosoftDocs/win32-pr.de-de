---
description: Definiert Konstanten, die Transformationszustandswerte beschreiben.
ms.assetid: 53535d9f-246a-42cf-82a2-fb3cf6d4ebac
title: D3DTRANSFORMSTATETYPE-Enumeration (D3D9Types.h)
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
ms.openlocfilehash: 022aa20fab0739b32aa75eb5f4bc575c0a8ad853
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342995"
---
# <a name="d3dtransformstatetype-enumeration"></a><span data-ttu-id="bd1c5-103">D3DTRANSFORMSTATETYPE-Enumeration</span><span class="sxs-lookup"><span data-stu-id="bd1c5-103">D3DTRANSFORMSTATETYPE enumeration</span></span>

<span data-ttu-id="bd1c5-104">Definiert Konstanten, die Transformationszustandswerte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="bd1c5-104">Defines constants that describe transformation state values.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd1c5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd1c5-105">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="bd1c5-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="bd1c5-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="bd1c5-107"><span id="D3DTS_VIEW"></span><span id="d3dts_view"></span>**\_D3DTS-ANSICHT**</span><span class="sxs-lookup"><span data-stu-id="bd1c5-107"><span id="D3DTS_VIEW"></span><span id="d3dts_view"></span>**D3DTS\_VIEW**</span></span>
</dt> <dd>

<span data-ttu-id="bd1c5-108">Identifiziert die Transformationsmatrix, die als Transformationsmatrix für die Ansicht festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="bd1c5-108">Identifies the transformation matrix being set as the view transformation matrix.</span></span> <span data-ttu-id="bd1c5-109">Der Standardwert ist **NULL** (die Identitätsmatrix).</span><span class="sxs-lookup"><span data-stu-id="bd1c5-109">The default value is **NULL** (the identity matrix).</span></span>

</dd> <dt>

<span data-ttu-id="bd1c5-110"><span id="D3DTS_PROJECTION"></span><span id="d3dts_projection"></span>**\_D3DTS-PROJEKTION**</span><span class="sxs-lookup"><span data-stu-id="bd1c5-110"><span id="D3DTS_PROJECTION"></span><span id="d3dts_projection"></span>**D3DTS\_PROJECTION**</span></span>
</dt> <dd>

<span data-ttu-id="bd1c5-111">Identifiziert die Transformationsmatrix, die als Projektionstransformationsmatrix festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="bd1c5-111">Identifies the transformation matrix being set as the projection transformation matrix.</span></span> <span data-ttu-id="bd1c5-112">Der Standardwert ist **NULL** (die Identitätsmatrix).</span><span class="sxs-lookup"><span data-stu-id="bd1c5-112">The default value is **NULL** (the identity matrix).</span></span>

</dd> <dt>

<span data-ttu-id="bd1c5-113"><span id="D3DTS_TEXTURE0"></span><span id="d3dts_texture0"></span>**D3DTS \_ TEXTURE0**</span><span class="sxs-lookup"><span data-stu-id="bd1c5-113"><span id="D3DTS_TEXTURE0"></span><span id="d3dts_texture0"></span>**D3DTS\_TEXTURE0**</span></span>
</dt> <dd>

<span data-ttu-id="bd1c5-114">Identifiziert die Transformationsmatrix, die für die angegebene Texturphase festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="bd1c5-114">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="bd1c5-115"><span id="D3DTS_TEXTURE1"></span><span id="d3dts_texture1"></span>**D3DTS \_ TEXTURE1**</span><span class="sxs-lookup"><span data-stu-id="bd1c5-115"><span id="D3DTS_TEXTURE1"></span><span id="d3dts_texture1"></span>**D3DTS\_TEXTURE1**</span></span>
</dt> <dd>

<span data-ttu-id="bd1c5-116">Identifiziert die Transformationsmatrix, die für die angegebene Texturphase festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="bd1c5-116">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="bd1c5-117"><span id="D3DTS_TEXTURE2"></span><span id="d3dts_texture2"></span>**D3DTS \_ TEXTURE2**</span><span class="sxs-lookup"><span data-stu-id="bd1c5-117"><span id="D3DTS_TEXTURE2"></span><span id="d3dts_texture2"></span>**D3DTS\_TEXTURE2**</span></span>
</dt> <dd>

<span data-ttu-id="bd1c5-118">Identifiziert die Transformationsmatrix, die für die angegebene Texturphase festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="bd1c5-118">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="bd1c5-119"><span id="D3DTS_TEXTURE3"></span><span id="d3dts_texture3"></span>**D3DTS \_ TEXTURE3**</span><span class="sxs-lookup"><span data-stu-id="bd1c5-119"><span id="D3DTS_TEXTURE3"></span><span id="d3dts_texture3"></span>**D3DTS\_TEXTURE3**</span></span>
</dt> <dd>

<span data-ttu-id="bd1c5-120">Identifiziert die Transformationsmatrix, die für die angegebene Texturphase festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="bd1c5-120">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="bd1c5-121"><span id="D3DTS_TEXTURE4"></span><span id="d3dts_texture4"></span>**D3DTS \_ TEXTURE4**</span><span class="sxs-lookup"><span data-stu-id="bd1c5-121"><span id="D3DTS_TEXTURE4"></span><span id="d3dts_texture4"></span>**D3DTS\_TEXTURE4**</span></span>
</dt> <dd>

<span data-ttu-id="bd1c5-122">Identifiziert die Transformationsmatrix, die für die angegebene Texturphase festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="bd1c5-122">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="bd1c5-123"><span id="D3DTS_TEXTURE5"></span><span id="d3dts_texture5"></span>**D3DTS \_ TEXTURE5**</span><span class="sxs-lookup"><span data-stu-id="bd1c5-123"><span id="D3DTS_TEXTURE5"></span><span id="d3dts_texture5"></span>**D3DTS\_TEXTURE5**</span></span>
</dt> <dd>

<span data-ttu-id="bd1c5-124">Identifiziert die Transformationsmatrix, die für die angegebene Texturphase festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="bd1c5-124">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="bd1c5-125"><span id="D3DTS_TEXTURE6"></span><span id="d3dts_texture6"></span>**D3DTS \_ TEXTURE6**</span><span class="sxs-lookup"><span data-stu-id="bd1c5-125"><span id="D3DTS_TEXTURE6"></span><span id="d3dts_texture6"></span>**D3DTS\_TEXTURE6**</span></span>
</dt> <dd>

<span data-ttu-id="bd1c5-126">Identifiziert die Transformationsmatrix, die für die angegebene Texturphase festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="bd1c5-126">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="bd1c5-127"><span id="D3DTS_TEXTURE7"></span><span id="d3dts_texture7"></span>**D3DTS \_ TEXTURE7**</span><span class="sxs-lookup"><span data-stu-id="bd1c5-127"><span id="D3DTS_TEXTURE7"></span><span id="d3dts_texture7"></span>**D3DTS\_TEXTURE7**</span></span>
</dt> <dd>

<span data-ttu-id="bd1c5-128">Identifiziert die Transformationsmatrix, die für die angegebene Texturphase festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="bd1c5-128">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="bd1c5-129"><span id="D3DTS_FORCE_DWORD"></span><span id="d3dts_force_dword"></span>**D3DTS \_ FORCE \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="bd1c5-129"><span id="D3DTS_FORCE_DWORD"></span><span id="d3dts_force_dword"></span>**D3DTS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="bd1c5-130">Erzwingt, dass diese Enumeration auf eine Größe von 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="bd1c5-130">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="bd1c5-131">Ohne diesen Wert würden einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="bd1c5-131">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="bd1c5-132">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="bd1c5-132">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bd1c5-133">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bd1c5-133">Remarks</span></span>

<span data-ttu-id="bd1c5-134">Die Transformationszustände im Bereich von 256 bis 511 sind für die Speicherung von bis zu 256 Weltmatrizen reserviert, die mithilfe der D3DTS \_ WORLDMATRIX- und D3DTS WORLD-Makros indiziert werden \_ können.</span><span class="sxs-lookup"><span data-stu-id="bd1c5-134">The transform states in the range 256 through 511 are reserved to store up to 256 world matrices that can be indexed using the D3DTS\_WORLDMATRIX and D3DTS\_WORLD macros.</span></span>



| <span data-ttu-id="bd1c5-135">Makros</span><span class="sxs-lookup"><span data-stu-id="bd1c5-135">Macros</span></span>                                                  | <span data-ttu-id="bd1c5-136">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bd1c5-136">Description</span></span>                                                                                                                                                                      |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bd1c5-137">**D3DTS \_ WORLD**</span><span class="sxs-lookup"><span data-stu-id="bd1c5-137">**D3DTS\_WORLD**</span></span>](d3dts-world.md)                     | <span data-ttu-id="bd1c5-138">Entspricht D3DTS \_ WORLDMATRIX(0).</span><span class="sxs-lookup"><span data-stu-id="bd1c5-138">Equivalent to D3DTS\_WORLDMATRIX(0).</span></span>                                                                                                                                  |
| <span data-ttu-id="bd1c5-139">[**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) (Index)</span><span class="sxs-lookup"><span data-stu-id="bd1c5-139">[**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) (index)</span></span> | <span data-ttu-id="bd1c5-140">Identifiziert die Transformationsmatrix, die für die Weltmatrix am Index festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bd1c5-140">Identifies the transform matrix to set for the world matrix at index.</span></span> <span data-ttu-id="bd1c5-141">Mehrere Weltmatrizen werden nur für Scheitelpunktmischungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="bd1c5-141">Multiple world matrices are used only for vertex blending.</span></span> <span data-ttu-id="bd1c5-142">Andernfalls wird nur D3DTS \_ WORLD verwendet.</span><span class="sxs-lookup"><span data-stu-id="bd1c5-142">Otherwise only D3DTS\_WORLD is used.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="bd1c5-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bd1c5-143">Requirements</span></span>



| <span data-ttu-id="bd1c5-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bd1c5-144">Requirement</span></span> | <span data-ttu-id="bd1c5-145">Wert</span><span class="sxs-lookup"><span data-stu-id="bd1c5-145">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd1c5-146">Header</span><span class="sxs-lookup"><span data-stu-id="bd1c5-146">Header</span></span><br/> | <dl> <span data-ttu-id="bd1c5-147"><dt>D3D9Types.h</dt></span><span class="sxs-lookup"><span data-stu-id="bd1c5-147"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd1c5-148">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="bd1c5-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd1c5-149">Direct3D-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="bd1c5-149">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="bd1c5-150">**IDirect3DDevice9::GetTransform**</span><span class="sxs-lookup"><span data-stu-id="bd1c5-150">**IDirect3DDevice9::GetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettransform)
</dt> <dt>

[<span data-ttu-id="bd1c5-151">**IDirect3DDevice9::MultiplyTransform**</span><span class="sxs-lookup"><span data-stu-id="bd1c5-151">**IDirect3DDevice9::MultiplyTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-multiplytransform)
</dt> <dt>

[<span data-ttu-id="bd1c5-152">**IDirect3DDevice9::SetTransform**</span><span class="sxs-lookup"><span data-stu-id="bd1c5-152">**IDirect3DDevice9::SetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

[<span data-ttu-id="bd1c5-153">**D3DTS \_ WORLD**</span><span class="sxs-lookup"><span data-stu-id="bd1c5-153">**D3DTS\_WORLD**</span></span>](d3dts-world.md)
</dt> <dt>

[<span data-ttu-id="bd1c5-154">**D3DTS \_ WORLDn**</span><span class="sxs-lookup"><span data-stu-id="bd1c5-154">**D3DTS\_WORLDn**</span></span>](d3dts-worldn.md)
</dt> <dt>

[<span data-ttu-id="bd1c5-155">**D3DTS \_ WORLDMATRIX**</span><span class="sxs-lookup"><span data-stu-id="bd1c5-155">**D3DTS\_WORLDMATRIX**</span></span>](d3dts-worldmatrix.md)
</dt> </dl>

 

 
