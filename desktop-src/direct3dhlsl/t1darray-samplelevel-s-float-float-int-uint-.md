---
title: 'Samplelevel:: samplelevel (S, float, float, int, uint)-Funktion für Texture1DArray'
description: 'Führt eine Stichprobe für eine Textur auf der angegebenen MipMap-Ebene aus und gibt den Status des Vorgangs zurück. Für Texture1DArray. | Samplelevel:: samplelevel (S, float, float, int, uint)-Funktion'
ms.assetid: 6BF31C44-B933-481E-9FB2-D606E3F91036
keywords:
- Samplelevel-Funktion HLSL
topic_type:
- apiref
api_name:
- SampleLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6ee1248ee72044e6a7d8a688753f0a61c7fb4e60
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104356176"
---
# <a name="samplelevelsamplelevelsfloatfloatintuint-function-for-texture1darray"></a><span data-ttu-id="bf1a5-106">Samplelevel:: samplelevel (S, float, float, int, uint)-Funktion für Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="bf1a5-106">SampleLevel::SampleLevel(S,float,float,int,uint) function for Texture1DArray</span></span>

<span data-ttu-id="bf1a5-107">Führt eine Stichprobe für eine Textur auf der angegebenen MipMap-Ebene aus und gibt den Status des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="bf1a5-107">Samples a texture on the specified mipmap level and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf1a5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf1a5-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleLevel(
  in  SamplerState S,
  in  float        Location,
  in  float        LOD,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="bf1a5-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf1a5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf1a5-110">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bf1a5-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf1a5-111">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="bf1a5-111">Type: **SamplerState**</span></span>

<span data-ttu-id="bf1a5-112">Ein [samplerzustand](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="bf1a5-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="bf1a5-113">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="bf1a5-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="bf1a5-114">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bf1a5-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf1a5-115">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="bf1a5-115">Type: **float**</span></span>

<span data-ttu-id="bf1a5-116">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="bf1a5-116">The texture coordinates.</span></span> <span data-ttu-id="bf1a5-117">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="bf1a5-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="bf1a5-118">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="bf1a5-118">Texture-Object Type</span></span>                    | <span data-ttu-id="bf1a5-119">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="bf1a5-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="bf1a5-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf1a5-120">Texture1D</span></span>                              | <span data-ttu-id="bf1a5-121">float</span><span class="sxs-lookup"><span data-stu-id="bf1a5-121">float</span></span>          |
| <span data-ttu-id="bf1a5-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf1a5-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="bf1a5-123">float2</span><span class="sxs-lookup"><span data-stu-id="bf1a5-123">float2</span></span>         |
| <span data-ttu-id="bf1a5-124">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="bf1a5-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="bf1a5-125">float3</span><span class="sxs-lookup"><span data-stu-id="bf1a5-125">float3</span></span>         |
| <span data-ttu-id="bf1a5-126">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="bf1a5-126">TextureCubeArray</span></span>                       | <span data-ttu-id="bf1a5-127">float4</span><span class="sxs-lookup"><span data-stu-id="bf1a5-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="bf1a5-128">*Lod* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bf1a5-128">*LOD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf1a5-129">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="bf1a5-129">Type: **float**</span></span>

<span data-ttu-id="bf1a5-130">\[in \] einer Zahl, die die MipMap-Ebene angibt.</span><span class="sxs-lookup"><span data-stu-id="bf1a5-130">\[in\] A number that specifies the mipmap level.</span></span> <span data-ttu-id="bf1a5-131">Wenn der Wert 0 (null) ist, wird MipMap Level 0 (größte Zuordnung) verwendet.</span><span class="sxs-lookup"><span data-stu-id="bf1a5-131">If the value is ≤ 0, mipmap level 0 (biggest map) is used.</span></span> <span data-ttu-id="bf1a5-132">Der Bruch Wert (falls angegeben) wird verwendet, um zwischen zwei MipMap-Ebenen zu interpolieren.</span><span class="sxs-lookup"><span data-stu-id="bf1a5-132">The fractional value (if supplied) is used to interpolate between two mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="bf1a5-133">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bf1a5-133">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf1a5-134">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="bf1a5-134">Type: **int**</span></span>

<span data-ttu-id="bf1a5-135">Ein optionaler Offset der Textur Koordinate, der für jeden Textur Objekttyp verwendet werden kann. der Offset wird vor der Stichprobenentnahme auf den Speicherort angewendet.</span><span class="sxs-lookup"><span data-stu-id="bf1a5-135">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="bf1a5-136">Verwenden Sie einen Offset nur bei einer ganzzahligen miplevel. Andernfalls erhalten Sie möglicherweise Ergebnisse, die nicht gut in Hardware übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="bf1a5-136">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="bf1a5-137">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="bf1a5-137">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="bf1a5-138">Weitere Informationen finden Sie unter [Anwenden von ganzzahligen Offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="bf1a5-138">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="bf1a5-139">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="bf1a5-139">Texture-Object Type</span></span>           | <span data-ttu-id="bf1a5-140">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="bf1a5-140">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="bf1a5-141">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="bf1a5-141">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="bf1a5-142">INT</span><span class="sxs-lookup"><span data-stu-id="bf1a5-142">int</span></span>            |
| <span data-ttu-id="bf1a5-143">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="bf1a5-143">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="bf1a5-144">int2</span><span class="sxs-lookup"><span data-stu-id="bf1a5-144">int2</span></span>           |
| <span data-ttu-id="bf1a5-145">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf1a5-145">Texture3D</span></span>                     | <span data-ttu-id="bf1a5-146">int3</span><span class="sxs-lookup"><span data-stu-id="bf1a5-146">int3</span></span>           |
| <span data-ttu-id="bf1a5-147">Texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="bf1a5-147">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="bf1a5-148">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="bf1a5-148">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="bf1a5-149">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bf1a5-149">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf1a5-150">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="bf1a5-150">Type: **uint**</span></span>

<span data-ttu-id="bf1a5-151">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="bf1a5-151">The status of the operation.</span></span> <span data-ttu-id="bf1a5-152">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="bf1a5-152">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="bf1a5-153">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="bf1a5-153">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="bf1a5-154">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="bf1a5-154">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf1a5-155">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bf1a5-155">Return value</span></span>

<span data-ttu-id="bf1a5-156">Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="bf1a5-156">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="bf1a5-157">Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="bf1a5-157">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="bf1a5-158">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="bf1a5-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf1a5-159">Samplelevel-Methoden</span><span class="sxs-lookup"><span data-stu-id="bf1a5-159">SampleLevel methods</span></span>](texture1darray-samplelevel.md)
</dt> </dl>

 

 
