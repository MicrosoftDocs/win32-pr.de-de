---
description: Definiert Texturfiltermodi für eine Texturphase.
ms.assetid: 4e0420fa-ac76-4be4-90d7-944d8d5a5de1
title: D3DTEXTUREFILTERTYPE-Enumeration (D3D9Types.h)
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
ms.openlocfilehash: bd6038e1b3d2b2f85e5766605583db9879427343
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343005"
---
# <a name="d3dtexturefiltertype-enumeration"></a><span data-ttu-id="76feb-103">D3DTEXTUREFILTERTYPE-Enumeration</span><span class="sxs-lookup"><span data-stu-id="76feb-103">D3DTEXTUREFILTERTYPE enumeration</span></span>

<span data-ttu-id="76feb-104">Definiert Texturfiltermodi für eine Texturphase.</span><span class="sxs-lookup"><span data-stu-id="76feb-104">Defines texture filtering modes for a texture stage.</span></span>

## <a name="syntax"></a><span data-ttu-id="76feb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="76feb-105">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="76feb-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="76feb-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="76feb-107"><span id="D3DTEXF_NONE"></span><span id="d3dtexf_none"></span>**D3DTEXF \_ NONE**</span><span class="sxs-lookup"><span data-stu-id="76feb-107"><span id="D3DTEXF_NONE"></span><span id="d3dtexf_none"></span>**D3DTEXF\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="76feb-108">Bei Verwendung mit [**D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md)deaktiviert mipmapping.</span><span class="sxs-lookup"><span data-stu-id="76feb-108">When used with [**D3DSAMP\_MIPFILTER**](./d3dsamplerstatetype.md), disables mipmapping.</span></span>

</dd> <dt>

<span data-ttu-id="76feb-109"><span id="D3DTEXF_POINT"></span><span id="d3dtexf_point"></span>**D3DTEXF \_ POINT**</span><span class="sxs-lookup"><span data-stu-id="76feb-109"><span id="D3DTEXF_POINT"></span><span id="d3dtexf_point"></span>**D3DTEXF\_POINT**</span></span>
</dt> <dd>

<span data-ttu-id="76feb-110">Gibt bei Verwendung mit [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) oder [**D3DSAMP \_ MINFILTER**](./d3dsamplerstatetype.md)an, dass die Punktfilterung als Texturvergrößerungs- bzw. Minierungsfilter verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="76feb-110">When used with [**D3DSAMP\_ MAGFILTER**](./d3dsamplerstatetype.md) or [**D3DSAMP\_MINFILTER**](./d3dsamplerstatetype.md), specifies that point filtering is to be used as the texture magnification or minification filter respectively.</span></span> <span data-ttu-id="76feb-111">Bei Verwendung mit **D3DSAMP \_ MIPFILTER** aktiviert mipmapping und gibt an, dass der Rasterizer die Farbe aus dem Texel der nächsten MIP-Ebene auswählt.</span><span class="sxs-lookup"><span data-stu-id="76feb-111">When used with **D3DSAMP\_MIPFILTER**, enables mipmapping and specifies that the rasterizer chooses the color from the texel of the nearest mip level.</span></span>

</dd> <dt>

<span data-ttu-id="76feb-112"><span id="D3DTEXF_LINEAR"></span><span id="d3dtexf_linear"></span>**D3DTEXF \_ LINEAR**</span><span class="sxs-lookup"><span data-stu-id="76feb-112"><span id="D3DTEXF_LINEAR"></span><span id="d3dtexf_linear"></span>**D3DTEXF\_LINEAR**</span></span>
</dt> <dd>

<span data-ttu-id="76feb-113">Gibt bei Verwendung mit [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) oder [**D3DSAMP \_ MINFILTER**](./d3dsamplerstatetype.md)an, dass die lineare Filterung als Texturvergrößerungs- bzw. Minierungsfilter verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="76feb-113">When used with [**D3DSAMP\_ MAGFILTER**](./d3dsamplerstatetype.md) or [**D3DSAMP\_MINFILTER**](./d3dsamplerstatetype.md), specifies that linear filtering is to be used as the texture magnification or minification filter respectively.</span></span> <span data-ttu-id="76feb-114">Bei Verwendung mit **D3DSAMP \_ MIPFILTER** ermöglicht mipmapping und trilineare Filterung. Es gibt an, dass der Rasterizer zwischen den beiden nächsten MIP-Ebenen interpoliert.</span><span class="sxs-lookup"><span data-stu-id="76feb-114">When used with **D3DSAMP\_MIPFILTER**, enables mipmapping and trilinear filtering; it specifies that the rasterizer interpolates between the two nearest mip levels.</span></span>

</dd> <dt>

<span data-ttu-id="76feb-115"><span id="D3DTEXF_ANISOTROPIC"></span><span id="d3dtexf_anisotropic"></span>**D3DTEXF \_ ANISOTROPIC**</span><span class="sxs-lookup"><span data-stu-id="76feb-115"><span id="D3DTEXF_ANISOTROPIC"></span><span id="d3dtexf_anisotropic"></span>**D3DTEXF\_ANISOTROPIC**</span></span>
</dt> <dd>

<span data-ttu-id="76feb-116">Gibt bei Verwendung mit [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) oder [**D3DSAMP \_ MINFILTER**](./d3dsamplerstatetype.md)an, dass die anisotrope Texturfilterung als Texturvergrößerungs- bzw. Minierungsfilter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="76feb-116">When used with [**D3DSAMP\_ MAGFILTER**](./d3dsamplerstatetype.md) or [**D3DSAMP\_MINFILTER**](./d3dsamplerstatetype.md), specifies that anisotropic texture filtering used as a texture magnification or minification filter respectively.</span></span> <span data-ttu-id="76feb-117">Gleicht die Verzerrung aus, die durch den Unterschied im Winkel zwischen dem Texturpolygon und der Bildschirmebene verursacht wird.</span><span class="sxs-lookup"><span data-stu-id="76feb-117">Compensates for distortion caused by the difference in angle between the texture polygon and the plane of the screen.</span></span> <span data-ttu-id="76feb-118">Die Verwendung **mit D3DSAMP \_ MIPFILTER** ist nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="76feb-118">Use with **D3DSAMP\_MIPFILTER** is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="76feb-119"><span id="D3DTEXF_PYRAMIDALQUAD"></span><span id="d3dtexf_pyramidalquad"></span>**D3DTEXF \_ PYRAMIDALQUAD**</span><span class="sxs-lookup"><span data-stu-id="76feb-119"><span id="D3DTEXF_PYRAMIDALQUAD"></span><span id="d3dtexf_pyramidalquad"></span>**D3DTEXF\_PYRAMIDALQUAD**</span></span>
</dt> <dd>

<span data-ttu-id="76feb-120">Ein 4-Beispiel-Festzeltfilter, der als Texturvergrößerungs- oder Minierungsfilter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="76feb-120">A 4-sample tent filter used as a texture magnification or minification filter.</span></span> <span data-ttu-id="76feb-121">Die Verwendung [**mit D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md) ist nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="76feb-121">Use with [**D3DSAMP\_MIPFILTER**](./d3dsamplerstatetype.md) is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="76feb-122"><span id="D3DTEXF_GAUSSIANQUAD"></span><span id="d3dtexf_gaussianquad"></span>**D3DTEXF \_ GASSIANQUAD**</span><span class="sxs-lookup"><span data-stu-id="76feb-122"><span id="D3DTEXF_GAUSSIANQUAD"></span><span id="d3dtexf_gaussianquad"></span>**D3DTEXF\_GAUSSIANQUAD**</span></span>
</dt> <dd>

<span data-ttu-id="76feb-123">Ein 4-Stichproben-Filter, der als Texturvergrößerungs- oder Vergrößerungsfilter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="76feb-123">A 4-sample Gaussian filter used as a texture magnification or minification filter.</span></span> <span data-ttu-id="76feb-124">Die Verwendung mit [**D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md) ist nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="76feb-124">Use with [**D3DSAMP\_MIPFILTER**](./d3dsamplerstatetype.md) is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="76feb-125"><span id="D3DTEXF_CONVOLUTIONMONO"></span><span id="d3dtexf_convolutionmono"></span>**D3DTEXF \_ CONVOLUTIONMONO**</span><span class="sxs-lookup"><span data-stu-id="76feb-125"><span id="D3DTEXF_CONVOLUTIONMONO"></span><span id="d3dtexf_convolutionmono"></span>**D3DTEXF\_CONVOLUTIONMONO**</span></span>
</dt> <dd>

<span data-ttu-id="76feb-126">Konvolutionsfilter für monocolore Texturen.</span><span class="sxs-lookup"><span data-stu-id="76feb-126">Convolution filter for monochrome textures.</span></span> <span data-ttu-id="76feb-127">Weitere Informationen finden Sie unter [D3DFMT \_ A1.](d3dformat.md)</span><span class="sxs-lookup"><span data-stu-id="76feb-127">See [D3DFMT\_A1](d3dformat.md).</span></span>

<span data-ttu-id="76feb-128">Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="76feb-128">Differences between Direct3D 9 and Direct3D 9Ex:</span></span>

- <span data-ttu-id="76feb-129">Dieses Flag ist nur in Direct3D 9Ex verfügbar.</span><span class="sxs-lookup"><span data-stu-id="76feb-129">This flag is available in Direct3D 9Ex only.</span></span>



 

<span data-ttu-id="76feb-130">Die Verwendung mit [**D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md) ist nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="76feb-130">Use with [**D3DSAMP\_MIPFILTER**](./d3dsamplerstatetype.md) is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="76feb-131"><span id="D3DTEXF_FORCE_DWORD"></span><span id="d3dtexf_force_dword"></span>**D3DTEXF \_ FORCE \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="76feb-131"><span id="D3DTEXF_FORCE_DWORD"></span><span id="d3dtexf_force_dword"></span>**D3DTEXF\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="76feb-132">Erzwingt, dass diese Enumeration in eine Größe von 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="76feb-132">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="76feb-133">Ohne diesen Wert würden einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="76feb-133">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="76feb-134">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="76feb-134">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="76feb-135">Hinweise</span><span class="sxs-lookup"><span data-stu-id="76feb-135">Remarks</span></span>

<span data-ttu-id="76feb-136">D3DTEXTUREFILTERTYPE wird von [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) zusammen mit [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md) verwendet, um Texturfilterungsmodi für eine Texturphase zu definieren.</span><span class="sxs-lookup"><span data-stu-id="76feb-136">D3DTEXTUREFILTERTYPE is used by [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) along with [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md) to define texture filtering modes for a texture stage.</span></span>

<span data-ttu-id="76feb-137">Um zu überprüfen, ob ein Format andere Texturfiltertypen als D3DTEXF POINT unterstützt \_ (was immer unterstützt wird), rufen Sie [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) mit D3DUSAGE \_ QUERY FILTER \_ auf.</span><span class="sxs-lookup"><span data-stu-id="76feb-137">To check if a format supports texture filter types other than D3DTEXF\_POINT (which is always supported), call [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) with D3DUSAGE\_QUERY\_FILTER.</span></span>

<span data-ttu-id="76feb-138">Legen Sie den Vergrößerungsfilter einer Texturstufe fest, indem [**Sie IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) mit dem D3DSAMP \_ MAGFILTER-Wert als zweiten Parameter und einem Member dieser Enumeration als dritten Parameter aufrufen.</span><span class="sxs-lookup"><span data-stu-id="76feb-138">Set a texture stage's magnification filter by calling [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) with the D3DSAMP\_MAGFILTER value as the second parameter and one member of this enumeration as the third parameter.</span></span>

<span data-ttu-id="76feb-139">Legen Sie den Qualifizierungsfilter einer Texturstufe fest, indem [**Sie IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) mit dem D3DSAMP \_ MINFILTER-Wert als zweiten Parameter und einem Member dieser Enumeration als dritten Parameter aufrufen.</span><span class="sxs-lookup"><span data-stu-id="76feb-139">Set a texture stage's minification filter by calling [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) with the D3DSAMP\_MINFILTER value as the second parameter and one member of this enumeration as the third parameter.</span></span>

<span data-ttu-id="76feb-140">Legen Sie den Texturfilter für die Verwendung zwischen MIPMAP-Ebenen fest, indem [**Sie IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) mit dem D3DSAMP \_ MIPFILTER-Wert als zweiten Parameter und einem Member dieser Enumeration als dritten Parameter aufrufen.</span><span class="sxs-lookup"><span data-stu-id="76feb-140">Set the texture filter to use between-mipmap levels by calling [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) with the D3DSAMP\_MIPFILTER value as the second parameter and one member of this enumeration as the third parameter.</span></span>

<span data-ttu-id="76feb-141">Nicht alle gültigen Filtermodi für ein Gerät gelten für Volumezuordnungen.</span><span class="sxs-lookup"><span data-stu-id="76feb-141">Not all valid filtering modes for a device will apply to volume maps.</span></span> <span data-ttu-id="76feb-142">Im Allgemeinen werden die Vergrößerungsfilter D3DTEXF \_ POINT und D3DTEXF \_ LINEAR für Volumezuordnungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="76feb-142">In general, D3DTEXF\_POINT and D3DTEXF\_LINEAR magnification filters will be supported for volume maps.</span></span> <span data-ttu-id="76feb-143">Wenn D3DPTEXTURECAPS MIPVOLUMEMAP festgelegt ist, werden die Filter \_ D3DTEXF \_ POINT mipmap und D3DTEXF POINT und \_ D3DTEXF LINEAR minification für Volumezuordnungen \_ unterstützt.</span><span class="sxs-lookup"><span data-stu-id="76feb-143">If D3DPTEXTURECAPS\_MIPVOLUMEMAP is set, then the D3DTEXF\_POINT mipmap filter and D3DTEXF\_POINT and D3DTEXF\_LINEAR minification filters will be supported for volume maps.</span></span> <span data-ttu-id="76feb-144">Das Gerät unterstützt möglicherweise den D3DTEXF \_ LINEAR mipmap-Filter für Volumezuordnungen.</span><span class="sxs-lookup"><span data-stu-id="76feb-144">The device may or may not support the D3DTEXF\_LINEAR mipmap filter for volume maps.</span></span> <span data-ttu-id="76feb-145">Geräte, die die anisotrope Filterung für 2D-Karten unterstützen, unterstützen nicht notwendigerweise die anisotrope Filterung für Volumezuordnungen.</span><span class="sxs-lookup"><span data-stu-id="76feb-145">Devices that support anisotropic filtering for 2D maps do not necessarily support anisotropic filtering for volume maps.</span></span> <span data-ttu-id="76feb-146">Anwendungen, die die anisotrope Filterung aktivieren, erhalten jedoch die beste verfügbare Filterung (wahrscheinlich linear), wenn die anisotrope Filterung nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="76feb-146">However, applications that enable anisotropic filtering will receive the best available filtering (probably linear) if anisotropic filtering is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="76feb-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76feb-147">Requirements</span></span>



| <span data-ttu-id="76feb-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="76feb-148">Requirement</span></span> | <span data-ttu-id="76feb-149">Wert</span><span class="sxs-lookup"><span data-stu-id="76feb-149">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="76feb-150">Header</span><span class="sxs-lookup"><span data-stu-id="76feb-150">Header</span></span><br/> | <dl> <span data-ttu-id="76feb-151"><dt>D3D9Types.h</dt></span><span class="sxs-lookup"><span data-stu-id="76feb-151"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76feb-152">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="76feb-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76feb-153">Direct3D-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="76feb-153">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="76feb-154">**ID3DXPatchMesh::GetDisplaceParam**</span><span class="sxs-lookup"><span data-stu-id="76feb-154">**ID3DXPatchMesh::GetDisplaceParam**</span></span>](id3dxpatchmesh--getdisplaceparam.md)
</dt> <dt>

[<span data-ttu-id="76feb-155">**ID3DXPatchMesh::SetDisplaceParam**</span><span class="sxs-lookup"><span data-stu-id="76feb-155">**ID3DXPatchMesh::SetDisplaceParam**</span></span>](id3dxpatchmesh--setdisplaceparam.md)
</dt> <dt>

[<span data-ttu-id="76feb-156">**D3DSAMPLERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="76feb-156">**D3DSAMPLERSTATETYPE**</span></span>](./d3dsamplerstatetype.md)
</dt> <dt>

[<span data-ttu-id="76feb-157">**IDirect3DDevice9::SetSamplerState**</span><span class="sxs-lookup"><span data-stu-id="76feb-157">**IDirect3DDevice9::SetSamplerState**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)
</dt> </dl>

 

 
