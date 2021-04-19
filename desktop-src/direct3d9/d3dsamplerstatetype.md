---
description: Samplerzustände definieren Textur-samplingvorgänge wie Textur Adressierung und Textur Filterung.
ms.assetid: 03a6a5f1-5e4f-4ba8-be4a-74d78fbc85d0
title: D3DSAMPLERSTATETYPE-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSAMPLERSTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3e12764db306e61422f8c06ef514f6fad59b3ed8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366449"
---
# <a name="d3dsamplerstatetype-enumeration"></a><span data-ttu-id="44247-103">D3DSAMPLERSTATETYPE-Enumeration</span><span class="sxs-lookup"><span data-stu-id="44247-103">D3DSAMPLERSTATETYPE enumeration</span></span>

<span data-ttu-id="44247-104">Samplerzustände definieren Textur-samplingvorgänge wie Textur Adressierung und Textur Filterung.</span><span class="sxs-lookup"><span data-stu-id="44247-104">Sampler states define texture sampling operations such as texture addressing and texture filtering.</span></span> <span data-ttu-id="44247-105">In einigen samplerzuständen ist die Vertexverarbeitung und einige Setup Pixel Verarbeitung eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="44247-105">Some sampler states set-up vertex processing, and some set-up pixel processing.</span></span> <span data-ttu-id="44247-106">Samplerzustände können mithilfe von stateblocks gespeichert und wieder hergestellt werden (siehe [Status Blöcke speichern und Wiederherstellen (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span><span class="sxs-lookup"><span data-stu-id="44247-106">Sampler states can be saved and restored using stateblocks (see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span></span>

## <a name="syntax"></a><span data-ttu-id="44247-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="44247-107">Syntax</span></span>


```C++
typedef enum D3DSAMPLERSTATETYPE { 
  D3DSAMP_ADDRESSU       = 1,
  D3DSAMP_ADDRESSV       = 2,
  D3DSAMP_ADDRESSW       = 3,
  D3DSAMP_BORDERCOLOR    = 4,
  D3DSAMP_MAGFILTER      = 5,
  D3DSAMP_MINFILTER      = 6,
  D3DSAMP_MIPFILTER      = 7,
  D3DSAMP_MIPMAPLODBIAS  = 8,
  D3DSAMP_MAXMIPLEVEL    = 9,
  D3DSAMP_MAXANISOTROPY  = 10,
  D3DSAMP_SRGBTEXTURE    = 11,
  D3DSAMP_ELEMENTINDEX   = 12,
  D3DSAMP_DMAPOFFSET     = 13,
  D3DSAMP_FORCE_DWORD    = 0x7fffffff
} D3DSAMPLERSTATETYPE, *LPD3DSAMPLERSTATETYPE;
```



## <a name="constants"></a><span data-ttu-id="44247-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="44247-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="44247-109"><span id="D3DSAMP_ADDRESSU"></span><span id="d3dsamp_addressu"></span>**D3DSAMP \_ adressu**</span><span class="sxs-lookup"><span data-stu-id="44247-109"><span id="D3DSAMP_ADDRESSU"></span><span id="d3dsamp_addressu"></span>**D3DSAMP\_ADDRESSU**</span></span>
</dt> <dd>

<span data-ttu-id="44247-110">Der Textur Adress Modus für die u-Koordinate.</span><span class="sxs-lookup"><span data-stu-id="44247-110">Texture-address mode for the u coordinate.</span></span> <span data-ttu-id="44247-111">Der Standardwert ist D3DTADDRESS \_ Wrap.</span><span class="sxs-lookup"><span data-stu-id="44247-111">The default is D3DTADDRESS\_WRAP.</span></span> <span data-ttu-id="44247-112">Weitere Informationen finden Sie unter [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span><span class="sxs-lookup"><span data-stu-id="44247-112">For more information, see [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span></span>

</dd> <dt>

<span data-ttu-id="44247-113"><span id="D3DSAMP_ADDRESSV"></span><span id="d3dsamp_addressv"></span>**D3DSAMP \_ adressssv**</span><span class="sxs-lookup"><span data-stu-id="44247-113"><span id="D3DSAMP_ADDRESSV"></span><span id="d3dsamp_addressv"></span>**D3DSAMP\_ADDRESSV**</span></span>
</dt> <dd>

<span data-ttu-id="44247-114">Der Textur Adress Modus für die v-Koordinate.</span><span class="sxs-lookup"><span data-stu-id="44247-114">Texture-address mode for the v coordinate.</span></span> <span data-ttu-id="44247-115">Der Standardwert ist D3DTADDRESS \_ Wrap.</span><span class="sxs-lookup"><span data-stu-id="44247-115">The default is D3DTADDRESS\_WRAP.</span></span> <span data-ttu-id="44247-116">Weitere Informationen finden Sie unter [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span><span class="sxs-lookup"><span data-stu-id="44247-116">For more information, see [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span></span>

</dd> <dt>

<span data-ttu-id="44247-117"><span id="D3DSAMP_ADDRESSW"></span><span id="d3dsamp_addressw"></span>**D3DSAMP \_ AddressW**</span><span class="sxs-lookup"><span data-stu-id="44247-117"><span id="D3DSAMP_ADDRESSW"></span><span id="d3dsamp_addressw"></span>**D3DSAMP\_ADDRESSW**</span></span>
</dt> <dd>

<span data-ttu-id="44247-118">Der Textur Adress Modus für die w-Koordinate.</span><span class="sxs-lookup"><span data-stu-id="44247-118">Texture-address mode for the w coordinate.</span></span> <span data-ttu-id="44247-119">Der Standardwert ist D3DTADDRESS \_ Wrap.</span><span class="sxs-lookup"><span data-stu-id="44247-119">The default is D3DTADDRESS\_WRAP.</span></span> <span data-ttu-id="44247-120">Weitere Informationen finden Sie unter [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span><span class="sxs-lookup"><span data-stu-id="44247-120">For more information, see [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span></span>

</dd> <dt>

<span data-ttu-id="44247-121"><span id="D3DSAMP_BORDERCOLOR"></span><span id="d3dsamp_bordercolor"></span>**D3DSAMP \_ BorderColor**</span><span class="sxs-lookup"><span data-stu-id="44247-121"><span id="D3DSAMP_BORDERCOLOR"></span><span id="d3dsamp_bordercolor"></span>**D3DSAMP\_BORDERCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="44247-122">Rahmenfarbe oder Typ [**D3DCOLOR**](d3dcolor.md).</span><span class="sxs-lookup"><span data-stu-id="44247-122">Border color or type [**D3DCOLOR**](d3dcolor.md).</span></span> <span data-ttu-id="44247-123">Die Standardfarbe ist 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="44247-123">The default color is 0x00000000.</span></span>

</dd> <dt>

<span data-ttu-id="44247-124"><span id="D3DSAMP_MAGFILTER"></span><span id="d3dsamp_magfilter"></span>**D3DSAMP- \_ MagFilter**</span><span class="sxs-lookup"><span data-stu-id="44247-124"><span id="D3DSAMP_MAGFILTER"></span><span id="d3dsamp_magfilter"></span>**D3DSAMP\_MAGFILTER**</span></span>
</dt> <dd>

<span data-ttu-id="44247-125">Vergrößerungs Filter vom Typ [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span><span class="sxs-lookup"><span data-stu-id="44247-125">Magnification filter of type [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span> <span data-ttu-id="44247-126">Der Standardwert ist D3DTEXF \_ Point.</span><span class="sxs-lookup"><span data-stu-id="44247-126">The default value is D3DTEXF\_POINT.</span></span>

</dd> <dt>

<span data-ttu-id="44247-127"><span id="D3DSAMP_MINFILTER"></span><span id="d3dsamp_minfilter"></span>**D3DSAMP \_ MinFilter**</span><span class="sxs-lookup"><span data-stu-id="44247-127"><span id="D3DSAMP_MINFILTER"></span><span id="d3dsamp_minfilter"></span>**D3DSAMP\_MINFILTER**</span></span>
</dt> <dd>

<span data-ttu-id="44247-128">Minification Filter vom Typ [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span><span class="sxs-lookup"><span data-stu-id="44247-128">Minification filter of type [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span> <span data-ttu-id="44247-129">Der Standardwert ist D3DTEXF \_ Point.</span><span class="sxs-lookup"><span data-stu-id="44247-129">The default value is D3DTEXF\_POINT.</span></span>

</dd> <dt>

<span data-ttu-id="44247-130"><span id="D3DSAMP_MIPFILTER"></span><span id="d3dsamp_mipfilter"></span>**D3DSAMP \_ MipFilter**</span><span class="sxs-lookup"><span data-stu-id="44247-130"><span id="D3DSAMP_MIPFILTER"></span><span id="d3dsamp_mipfilter"></span>**D3DSAMP\_MIPFILTER**</span></span>
</dt> <dd>

<span data-ttu-id="44247-131">Der während der Minimierung zu verwendende Mipmap-Filter.</span><span class="sxs-lookup"><span data-stu-id="44247-131">Mipmap filter to use during minification.</span></span> <span data-ttu-id="44247-132">Siehe [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span><span class="sxs-lookup"><span data-stu-id="44247-132">See [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span> <span data-ttu-id="44247-133">Der Standardwert ist D3DTEXF \_ None.</span><span class="sxs-lookup"><span data-stu-id="44247-133">The default value is D3DTEXF\_NONE.</span></span>

</dd> <dt>

<span data-ttu-id="44247-134"><span id="D3DSAMP_MIPMAPLODBIAS"></span><span id="d3dsamp_mipmaplodbias"></span>**D3DSAMP \_ mipmaplodbias**</span><span class="sxs-lookup"><span data-stu-id="44247-134"><span id="D3DSAMP_MIPMAPLODBIAS"></span><span id="d3dsamp_mipmaplodbias"></span>**D3DSAMP\_MIPMAPLODBIAS**</span></span>
</dt> <dd>

<span data-ttu-id="44247-135">MipMap-Ebenen-Detail-Bias.</span><span class="sxs-lookup"><span data-stu-id="44247-135">Mipmap level-of-detail bias.</span></span> <span data-ttu-id="44247-136">Der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="44247-136">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="44247-137"><span id="D3DSAMP_MAXMIPLEVEL"></span><span id="d3dsamp_maxmiplevel"></span>**D3DSAMP \_ MaxMipLevel**</span><span class="sxs-lookup"><span data-stu-id="44247-137"><span id="D3DSAMP_MAXMIPLEVEL"></span><span id="d3dsamp_maxmiplevel"></span>**D3DSAMP\_MAXMIPLEVEL**</span></span>
</dt> <dd>

<span data-ttu-id="44247-138">Detail Index der größten zu verwendenden Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="44247-138">level-of-detail index of largest map to use.</span></span> <span data-ttu-id="44247-139">Die Werte liegen im Bereich von 0 bis (n-1), wobei 0 das größte ist.</span><span class="sxs-lookup"><span data-stu-id="44247-139">Values range from 0 to (n - 1) where 0 is the largest.</span></span> <span data-ttu-id="44247-140">Der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="44247-140">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="44247-141"><span id="D3DSAMP_MAXANISOTROPY"></span><span id="d3dsamp_maxanisotropy"></span>**D3DSAMP \_ MaxAnisotropy**</span><span class="sxs-lookup"><span data-stu-id="44247-141"><span id="D3DSAMP_MAXANISOTROPY"></span><span id="d3dsamp_maxanisotropy"></span>**D3DSAMP\_MAXANISOTROPY**</span></span>
</dt> <dd>

<span data-ttu-id="44247-142">DWORD Maximum Anisotropy.</span><span class="sxs-lookup"><span data-stu-id="44247-142">DWORD maximum anisotropy.</span></span> <span data-ttu-id="44247-143">Werte liegen zwischen 1 und dem Wert, der im **MaxAnisotropy** -Member der [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) -Struktur angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="44247-143">Values range from 1 to the value that is specified in the **MaxAnisotropy** member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure.</span></span> <span data-ttu-id="44247-144">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="44247-144">The default value is 1.</span></span>

</dd> <dt>

<span data-ttu-id="44247-145"><span id="D3DSAMP_SRGBTEXTURE"></span><span id="d3dsamp_srgbtexture"></span>**D3DSAMP \_ srgbtexture**</span><span class="sxs-lookup"><span data-stu-id="44247-145"><span id="D3DSAMP_SRGBTEXTURE"></span><span id="d3dsamp_srgbtexture"></span>**D3DSAMP\_SRGBTEXTURE**</span></span>
</dt> <dd>

<span data-ttu-id="44247-146">Gamma Korrekturwert.</span><span class="sxs-lookup"><span data-stu-id="44247-146">Gamma correction value.</span></span> <span data-ttu-id="44247-147">Der Standardwert ist 0 (null). das bedeutet, dass Gamma 1,0 ist und keine Korrektur erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="44247-147">The default value is 0, which means gamma is 1.0 and no correction is required.</span></span> <span data-ttu-id="44247-148">Andernfalls bedeutet dieser Wert, dass der Sampler Gamma von 2,2 für den Inhalt annehmen und in linear (Gamma 1,0) konvertieren muss, bevor er dem Pixelshader präsentiert wird.</span><span class="sxs-lookup"><span data-stu-id="44247-148">Otherwise, this value means that the sampler should assume gamma of 2.2 on the content and convert it to linear (gamma 1.0) before presenting it to the pixel shader.</span></span>

</dd> <dt>

<span data-ttu-id="44247-149"><span id="D3DSAMP_ELEMENTINDEX"></span><span id="d3dsamp_elementindex"></span>**D3DSAMP \_ Elementindex**</span><span class="sxs-lookup"><span data-stu-id="44247-149"><span id="D3DSAMP_ELEMENTINDEX"></span><span id="d3dsamp_elementindex"></span>**D3DSAMP\_ELEMENTINDEX**</span></span>
</dt> <dd>

<span data-ttu-id="44247-150">Wenn dem Sampler eine multielementtextur zugewiesen wird, gibt dies an, welcher Element Index verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="44247-150">When a multielement texture is assigned to the sampler, this indicates which element index to use.</span></span> <span data-ttu-id="44247-151">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="44247-151">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="44247-152"><span id="D3DSAMP_DMAPOFFSET"></span><span id="d3dsamp_dmapoffset"></span>**D3DSAMP \_ dmapoffset**</span><span class="sxs-lookup"><span data-stu-id="44247-152"><span id="D3DSAMP_DMAPOFFSET"></span><span id="d3dsamp_dmapoffset"></span>**D3DSAMP\_DMAPOFFSET**</span></span>
</dt> <dd>

<span data-ttu-id="44247-153">Vertexoffset in der vorab komprimierten Verschiebungs Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="44247-153">Vertex offset in the presampled displacement map.</span></span> <span data-ttu-id="44247-154">Dies ist eine Konstante, die vom Mosaik Prozess verwendet wird. der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="44247-154">This is a constant used by the tessellator, its default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="44247-155"><span id="D3DSAMP_FORCE_DWORD"></span><span id="d3dsamp_force_dword"></span>**D3DSAMP \_ Erzwingen von \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="44247-155"><span id="D3DSAMP_FORCE_DWORD"></span><span id="d3dsamp_force_dword"></span>**D3DSAMP\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="44247-156">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="44247-156">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="44247-157">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="44247-157">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="44247-158">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="44247-158">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="44247-159">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="44247-159">Requirements</span></span>



| <span data-ttu-id="44247-160">Anforderung</span><span class="sxs-lookup"><span data-stu-id="44247-160">Requirement</span></span> | <span data-ttu-id="44247-161">Wert</span><span class="sxs-lookup"><span data-stu-id="44247-161">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="44247-162">Header</span><span class="sxs-lookup"><span data-stu-id="44247-162">Header</span></span><br/> | <dl> <span data-ttu-id="44247-163"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="44247-163"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44247-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44247-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44247-165">Direct3D-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="44247-165">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 
