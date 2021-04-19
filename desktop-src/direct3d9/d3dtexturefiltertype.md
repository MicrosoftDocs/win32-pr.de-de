---
description: Definiert die Textur Filtermodi für eine Textur Phase.
ms.assetid: 4e0420fa-ac76-4be4-90d7-944d8d5a5de1
title: D3DTEXTUREFILTERTYPE-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTUREFILTERTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 212fd05755ebf554c3c57e7ac45dcf8947f2d753
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366626"
---
# <a name="d3dtexturefiltertype-enumeration"></a><span data-ttu-id="a359c-103">D3DTEXTUREFILTERTYPE-Enumeration</span><span class="sxs-lookup"><span data-stu-id="a359c-103">D3DTEXTUREFILTERTYPE enumeration</span></span>

<span data-ttu-id="a359c-104">Definiert die Textur Filtermodi für eine Textur Phase.</span><span class="sxs-lookup"><span data-stu-id="a359c-104">Defines texture filtering modes for a texture stage.</span></span>

## <a name="syntax"></a><span data-ttu-id="a359c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a359c-105">Syntax</span></span>


```C++
typedef enum D3DTEXTUREFILTERTYPE { 
  D3DTEXF_NONE             = 0,
  D3DTEXF_POINT            = 1,
  D3DTEXF_LINEAR           = 2,
  D3DTEXF_ANISOTROPIC      = 3,
  D3DTEXF_PYRAMIDALQUAD    = 6,
  D3DTEXF_GAUSSIANQUAD     = 7,
  D3DTEXF_CONVOLUTIONMONO  = 8,
  D3DTEXF_FORCE_DWORD      = 0x7fffffff
} D3DTEXTUREFILTERTYPE, *LPD3DTEXTUREFILTERTYPE;
```



## <a name="constants"></a><span data-ttu-id="a359c-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="a359c-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a359c-107"><span id="D3DTEXF_NONE"></span><span id="d3dtexf_none"></span>**D3DTEXF \_ None**</span><span class="sxs-lookup"><span data-stu-id="a359c-107"><span id="D3DTEXF_NONE"></span><span id="d3dtexf_none"></span>**D3DTEXF\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="a359c-108">Deaktiviert bei Verwendung mit [**D3DSAMP \_ MipFilter**](./d3dsamplerstatetype.md)Mipmapping.</span><span class="sxs-lookup"><span data-stu-id="a359c-108">When used with [**D3DSAMP\_MIPFILTER**](./d3dsamplerstatetype.md), disables mipmapping.</span></span>

</dd> <dt>

<span data-ttu-id="a359c-109"><span id="D3DTEXF_POINT"></span><span id="d3dtexf_point"></span>**D3DTEXF \_ Punkt**</span><span class="sxs-lookup"><span data-stu-id="a359c-109"><span id="D3DTEXF_POINT"></span><span id="d3dtexf_point"></span>**D3DTEXF\_POINT**</span></span>
</dt> <dd>

<span data-ttu-id="a359c-110">Gibt bei Verwendung mit [**D3DSAMP \_ MagFilter**](./d3dsamplerstatetype.md) oder [**D3DSAMP \_ MinFilter**](./d3dsamplerstatetype.md)an, dass die Punkt Filterung als Textur Vergrößerung bzw. minierungs Filter verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a359c-110">When used with [**D3DSAMP\_ MAGFILTER**](./d3dsamplerstatetype.md) or [**D3DSAMP\_MINFILTER**](./d3dsamplerstatetype.md), specifies that point filtering is to be used as the texture magnification or minification filter respectively.</span></span> <span data-ttu-id="a359c-111">Bei Verwendung mit **D3DSAMP \_ MipFilter** aktiviert Mipmapping und gibt an, dass der Raster die Farbe aus dem textsder nächstgelegenen MIP-Ebene auswählt.</span><span class="sxs-lookup"><span data-stu-id="a359c-111">When used with **D3DSAMP\_MIPFILTER**, enables mipmapping and specifies that the rasterizer chooses the color from the texel of the nearest mip level.</span></span>

</dd> <dt>

<span data-ttu-id="a359c-112"><span id="D3DTEXF_LINEAR"></span><span id="d3dtexf_linear"></span>**D3DTEXF \_ linear**</span><span class="sxs-lookup"><span data-stu-id="a359c-112"><span id="D3DTEXF_LINEAR"></span><span id="d3dtexf_linear"></span>**D3DTEXF\_LINEAR**</span></span>
</dt> <dd>

<span data-ttu-id="a359c-113">Gibt bei Verwendung mit [**D3DSAMP \_ MagFilter**](./d3dsamplerstatetype.md) oder [**D3DSAMP \_ MinFilter**](./d3dsamplerstatetype.md)an, dass die lineare Filterung als Textur Vergrößerung bzw. minierungs Filter verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a359c-113">When used with [**D3DSAMP\_ MAGFILTER**](./d3dsamplerstatetype.md) or [**D3DSAMP\_MINFILTER**](./d3dsamplerstatetype.md), specifies that linear filtering is to be used as the texture magnification or minification filter respectively.</span></span> <span data-ttu-id="a359c-114">Bei Verwendung mit **D3DSAMP \_ MipFilter** aktiviert Mipmapping und die drei lineare Filterung. es gibt an, dass der Raster zwischen den beiden nächsten MIP-Ebenen interpoliert.</span><span class="sxs-lookup"><span data-stu-id="a359c-114">When used with **D3DSAMP\_MIPFILTER**, enables mipmapping and trilinear filtering; it specifies that the rasterizer interpolates between the two nearest mip levels.</span></span>

</dd> <dt>

<span data-ttu-id="a359c-115"><span id="D3DTEXF_ANISOTROPIC"></span><span id="d3dtexf_anisotropic"></span>**D3DTEXF \_ anisotrope**</span><span class="sxs-lookup"><span data-stu-id="a359c-115"><span id="D3DTEXF_ANISOTROPIC"></span><span id="d3dtexf_anisotropic"></span>**D3DTEXF\_ANISOTROPIC**</span></span>
</dt> <dd>

<span data-ttu-id="a359c-116">Gibt bei Verwendung mit [**D3DSAMP \_ MagFilter**](./d3dsamplerstatetype.md) oder [**D3DSAMP \_ MinFilter**](./d3dsamplerstatetype.md)an, dass die anisotrope Textur Filterung als Textur Vergrößerung bzw. minierungs Filter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a359c-116">When used with [**D3DSAMP\_ MAGFILTER**](./d3dsamplerstatetype.md) or [**D3DSAMP\_MINFILTER**](./d3dsamplerstatetype.md), specifies that anisotropic texture filtering used as a texture magnification or minification filter respectively.</span></span> <span data-ttu-id="a359c-117">Kompensiert die Verzerrung, die durch den Unterschied in der Spitze zwischen dem Textur Polygon und der Ebene des Bildschirms verursacht wird.</span><span class="sxs-lookup"><span data-stu-id="a359c-117">Compensates for distortion caused by the difference in angle between the texture polygon and the plane of the screen.</span></span> <span data-ttu-id="a359c-118">Die Verwendung mit **D3DSAMP \_ MipFilter** ist nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="a359c-118">Use with **D3DSAMP\_MIPFILTER** is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="a359c-119"><span id="D3DTEXF_PYRAMIDALQUAD"></span><span id="d3dtexf_pyramidalquad"></span>**D3DTEXF \_ pyramidalquad**</span><span class="sxs-lookup"><span data-stu-id="a359c-119"><span id="D3DTEXF_PYRAMIDALQUAD"></span><span id="d3dtexf_pyramidalquad"></span>**D3DTEXF\_PYRAMIDALQUAD**</span></span>
</dt> <dd>

<span data-ttu-id="a359c-120">Ein vier-Stichproben-Zelt Filter, der als Textur Vergrößerungs-oder minierungs Filter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a359c-120">A 4-sample tent filter used as a texture magnification or minification filter.</span></span> <span data-ttu-id="a359c-121">Die Verwendung mit [**D3DSAMP \_ MipFilter**](./d3dsamplerstatetype.md) ist nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="a359c-121">Use with [**D3DSAMP\_MIPFILTER**](./d3dsamplerstatetype.md) is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="a359c-122"><span id="D3DTEXF_GAUSSIANQUAD"></span><span id="d3dtexf_gaussianquad"></span>**D3DTEXF \_ gausianquad**</span><span class="sxs-lookup"><span data-stu-id="a359c-122"><span id="D3DTEXF_GAUSSIANQUAD"></span><span id="d3dtexf_gaussianquad"></span>**D3DTEXF\_GAUSSIANQUAD**</span></span>
</dt> <dd>

<span data-ttu-id="a359c-123">Ein Gaußscher vier-Stichproben Filter, der als Textur Vergrößerungs-oder minierungs Filter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a359c-123">A 4-sample Gaussian filter used as a texture magnification or minification filter.</span></span> <span data-ttu-id="a359c-124">Die Verwendung mit [**D3DSAMP \_ MipFilter**](./d3dsamplerstatetype.md) ist nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="a359c-124">Use with [**D3DSAMP\_MIPFILTER**](./d3dsamplerstatetype.md) is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="a359c-125"><span id="D3DTEXF_CONVOLUTIONMONO"></span><span id="d3dtexf_convolutionmono"></span>**D3DTEXF \_ -Konstante**</span><span class="sxs-lookup"><span data-stu-id="a359c-125"><span id="D3DTEXF_CONVOLUTIONMONO"></span><span id="d3dtexf_convolutionmono"></span>**D3DTEXF\_CONVOLUTIONMONO**</span></span>
</dt> <dd>

<span data-ttu-id="a359c-126">Der Konfigurations Filter für monochrome Texturen.</span><span class="sxs-lookup"><span data-stu-id="a359c-126">Convolution filter for monochrome textures.</span></span> <span data-ttu-id="a359c-127">Siehe [D3DFMT \_ a1](d3dformat.md).</span><span class="sxs-lookup"><span data-stu-id="a359c-127">See [D3DFMT\_A1](d3dformat.md).</span></span>



|                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a359c-128">Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="a359c-128">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="a359c-129">Dieses Flag ist nur in Direct3D 9Ex verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a359c-129">This flag is available in Direct3D 9Ex only.</span></span><br/> |



 

<span data-ttu-id="a359c-130">Die Verwendung mit [**D3DSAMP \_ MipFilter**](./d3dsamplerstatetype.md) ist nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="a359c-130">Use with [**D3DSAMP\_MIPFILTER**](./d3dsamplerstatetype.md) is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="a359c-131"><span id="D3DTEXF_FORCE_DWORD"></span><span id="d3dtexf_force_dword"></span>**D3DTEXF \_ Erzwingen von \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="a359c-131"><span id="D3DTEXF_FORCE_DWORD"></span><span id="d3dtexf_force_dword"></span>**D3DTEXF\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="a359c-132">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="a359c-132">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="a359c-133">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="a359c-133">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="a359c-134">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a359c-134">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a359c-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a359c-135">Remarks</span></span>

<span data-ttu-id="a359c-136">D3DTEXTUREFILTERTYPE wird von [**IDirect3DDevice9:: setsamplerstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) zusammen mit [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md) verwendet, um die Textur Filtermodi für eine Textur Phase zu definieren.</span><span class="sxs-lookup"><span data-stu-id="a359c-136">D3DTEXTUREFILTERTYPE is used by [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) along with [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md) to define texture filtering modes for a texture stage.</span></span>

<span data-ttu-id="a359c-137">Um zu überprüfen, ob ein Format andere Textur Filtertypen als D3DTEXF Point unterstützt \_ (was immer unterstützt wird), wenden Sie [**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) mit dem D3DUSAGE- \_ Abfrage \_ Filter an.</span><span class="sxs-lookup"><span data-stu-id="a359c-137">To check if a format supports texture filter types other than D3DTEXF\_POINT (which is always supported), call [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) with D3DUSAGE\_QUERY\_FILTER.</span></span>

<span data-ttu-id="a359c-138">Legen Sie den Vergrößerungs Filter einer Textur Phase fest, indem Sie [**IDirect3DDevice9:: setsamplerstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) mit dem D3DSAMP \_ MagFilter-Wert als zweiten Parameter und einem Member dieser Enumeration als dritten Parameter aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a359c-138">Set a texture stage's magnification filter by calling [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) with the D3DSAMP\_MAGFILTER value as the second parameter and one member of this enumeration as the third parameter.</span></span>

<span data-ttu-id="a359c-139">Legen Sie den Minimierung Filter für die Textur Phase fest, indem Sie [**IDirect3DDevice9:: setsamplerstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) mit dem D3DSAMP \_ MinFilter-Wert als zweiten Parameter und einem Member dieser Enumeration als dritten Parameter aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a359c-139">Set a texture stage's minification filter by calling [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) with the D3DSAMP\_MINFILTER value as the second parameter and one member of this enumeration as the third parameter.</span></span>

<span data-ttu-id="a359c-140">Legen Sie den Textur Filter so fest, dass er zwischen-MipMap-Ebenen verwendet wird, indem Sie [**IDirect3DDevice9:: setsamplerstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) mit dem D3DSAMP \_ MipFilter-Wert als zweiten Parameter und einem Member dieser Enumeration als dritten Parameter aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a359c-140">Set the texture filter to use between-mipmap levels by calling [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) with the D3DSAMP\_MIPFILTER value as the second parameter and one member of this enumeration as the third parameter.</span></span>

<span data-ttu-id="a359c-141">Nicht alle gültigen Filtermodi für ein Gerät gelten für volumenmaps.</span><span class="sxs-lookup"><span data-stu-id="a359c-141">Not all valid filtering modes for a device will apply to volume maps.</span></span> <span data-ttu-id="a359c-142">Im Allgemeinen werden D3DTEXF \_ Punkt-und D3DTEXF- \_ lineare Vergrößerungs Filter für Volume Maps unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a359c-142">In general, D3DTEXF\_POINT and D3DTEXF\_LINEAR magnification filters will be supported for volume maps.</span></span> <span data-ttu-id="a359c-143">Wenn D3DPTEXTURECAPS \_ mipvolumemap festgelegt ist, werden die \_ Filter D3DTEXF Point MipMap und D3DTEXF \_ Point und D3DTEXF \_ linear Minimierung für Volume Maps unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a359c-143">If D3DPTEXTURECAPS\_MIPVOLUMEMAP is set, then the D3DTEXF\_POINT mipmap filter and D3DTEXF\_POINT and D3DTEXF\_LINEAR minification filters will be supported for volume maps.</span></span> <span data-ttu-id="a359c-144">Das Gerät unterstützt den linearen D3DTEXF- \_ Mipmap-Filter für Volume Maps möglicherweise nicht.</span><span class="sxs-lookup"><span data-stu-id="a359c-144">The device may or may not support the D3DTEXF\_LINEAR mipmap filter for volume maps.</span></span> <span data-ttu-id="a359c-145">Geräte, die die anisotrope Filterung für 2D-Zuordnungen unterstützen, unterstützen nicht notwendigerweise die anisotrope Filterung für Volume Maps.</span><span class="sxs-lookup"><span data-stu-id="a359c-145">Devices that support anisotropic filtering for 2D maps do not necessarily support anisotropic filtering for volume maps.</span></span> <span data-ttu-id="a359c-146">Anwendungen, die die anisotrope Filterung aktivieren, erhalten jedoch die beste verfügbare Filterung (wahrscheinlich linear), wenn die anisotrope Filterung nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="a359c-146">However, applications that enable anisotropic filtering will receive the best available filtering (probably linear) if anisotropic filtering is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="a359c-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a359c-147">Requirements</span></span>



| <span data-ttu-id="a359c-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a359c-148">Requirement</span></span> | <span data-ttu-id="a359c-149">Wert</span><span class="sxs-lookup"><span data-stu-id="a359c-149">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a359c-150">Header</span><span class="sxs-lookup"><span data-stu-id="a359c-150">Header</span></span><br/> | <dl> <span data-ttu-id="a359c-151"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="a359c-151"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a359c-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a359c-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a359c-153">Direct3D-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="a359c-153">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="a359c-154">**ID3DXPatchMesh:: getverdräneparam**</span><span class="sxs-lookup"><span data-stu-id="a359c-154">**ID3DXPatchMesh::GetDisplaceParam**</span></span>](id3dxpatchmesh--getdisplaceparam.md)
</dt> <dt>

[<span data-ttu-id="a359c-155">**ID3DXPatchMesh:: setverdräneparam**</span><span class="sxs-lookup"><span data-stu-id="a359c-155">**ID3DXPatchMesh::SetDisplaceParam**</span></span>](id3dxpatchmesh--setdisplaceparam.md)
</dt> <dt>

[<span data-ttu-id="a359c-156">**D3DSAMPLERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="a359c-156">**D3DSAMPLERSTATETYPE**</span></span>](./d3dsamplerstatetype.md)
</dt> <dt>

[<span data-ttu-id="a359c-157">**IDirect3DDevice9:: setsamplerstate**</span><span class="sxs-lookup"><span data-stu-id="a359c-157">**IDirect3DDevice9::SetSamplerState**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)
</dt> </dl>

 

 
