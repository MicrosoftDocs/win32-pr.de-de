---
title: 'Samplebias:: samplebias (S, float, float, int, float)-Funktion'
description: 'Gibt eine Textur aus, nachdem der Wert "Bias" auf die MipMap-Ebene angewendet wurde, mit einem optionalen Wert, mit dem Sample Level-of-Detail-Werte (LOD) an eine Klammer übergeben werden. | Samplebias:: samplebias (S, float, float, int, float)-Funktion'
ms.assetid: 88BC4E99-B33D-4DAA-9A77-849B2F5FE6A7
keywords:
- Samplebias-Funktion HLSL
topic_type:
- apiref
api_name:
- SampleBias
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3af7ddaf3c015c2254761cce1d7cd30a2a68629b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995526"
---
# <a name="samplebiassamplebiassfloatfloatintfloat-function"></a><span data-ttu-id="1ada3-105">Samplebias:: samplebias (S, float, float, int, float)-Funktion</span><span class="sxs-lookup"><span data-stu-id="1ada3-105">SampleBias::SampleBias(S,float,float,int,float) function</span></span>

<span data-ttu-id="1ada3-106">Gibt eine Textur aus, nachdem der Wert "Bias" auf die MipMap-Ebene angewendet wurde, mit einem optionalen Wert, mit dem Sample Level-of-Detail-Werte (LOD) an eine Klammer übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="1ada3-106">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ada3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ada3-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="1ada3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ada3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ada3-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ada3-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ada3-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="1ada3-110">Type: **SamplerState**</span></span>

<span data-ttu-id="1ada3-111">Ein [samplerzustand](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="1ada3-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="1ada3-112">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="1ada3-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="1ada3-113">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ada3-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ada3-114">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="1ada3-114">Type: **float**</span></span>

<span data-ttu-id="1ada3-115">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="1ada3-115">The texture coordinates.</span></span> <span data-ttu-id="1ada3-116">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="1ada3-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="1ada3-117">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="1ada3-117">Texture-Object Type</span></span>                    | <span data-ttu-id="1ada3-118">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="1ada3-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="1ada3-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="1ada3-119">Texture1D</span></span>                              | <span data-ttu-id="1ada3-120">float</span><span class="sxs-lookup"><span data-stu-id="1ada3-120">float</span></span>          |
| <span data-ttu-id="1ada3-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="1ada3-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="1ada3-122">float2</span><span class="sxs-lookup"><span data-stu-id="1ada3-122">float2</span></span>         |
| <span data-ttu-id="1ada3-123">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="1ada3-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="1ada3-124">float3</span><span class="sxs-lookup"><span data-stu-id="1ada3-124">float3</span></span>         |
| <span data-ttu-id="1ada3-125">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="1ada3-125">TextureCubeArray</span></span>                       | <span data-ttu-id="1ada3-126">float4</span><span class="sxs-lookup"><span data-stu-id="1ada3-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="1ada3-127">*Bias* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ada3-127">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ada3-128">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="1ada3-128">Type: **float**</span></span>

<span data-ttu-id="1ada3-129">Der Bias-Wert, bei dem es sich um eine Gleit Komma Zahl zwischen 0,0 und 1,0 handelt, wird vor der Stichprobenentnahme auf eine MIP-Ebene angewendet.</span><span class="sxs-lookup"><span data-stu-id="1ada3-129">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="1ada3-130">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ada3-130">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ada3-131">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="1ada3-131">Type: **int**</span></span>

<span data-ttu-id="1ada3-132">Ein optionaler Offset der Textur Koordinate, der für jeden Textur Objekttyp verwendet werden kann. der Offset wird vor der Stichprobenentnahme auf den Speicherort angewendet.</span><span class="sxs-lookup"><span data-stu-id="1ada3-132">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="1ada3-133">Verwenden Sie einen Offset nur bei einer ganzzahligen miplevel. Andernfalls erhalten Sie möglicherweise Ergebnisse, die nicht gut in Hardware übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="1ada3-133">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="1ada3-134">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="1ada3-134">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="1ada3-135">Weitere Informationen finden Sie unter [Anwenden von ganzzahligen Offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="1ada3-135">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="1ada3-136">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="1ada3-136">Texture-Object Type</span></span>           | <span data-ttu-id="1ada3-137">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="1ada3-137">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="1ada3-138">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="1ada3-138">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="1ada3-139">INT</span><span class="sxs-lookup"><span data-stu-id="1ada3-139">int</span></span>            |
| <span data-ttu-id="1ada3-140">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="1ada3-140">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="1ada3-141">int2</span><span class="sxs-lookup"><span data-stu-id="1ada3-141">int2</span></span>           |
| <span data-ttu-id="1ada3-142">Texture3D</span><span class="sxs-lookup"><span data-stu-id="1ada3-142">Texture3D</span></span>                     | <span data-ttu-id="1ada3-143">int3</span><span class="sxs-lookup"><span data-stu-id="1ada3-143">int3</span></span>           |
| <span data-ttu-id="1ada3-144">Texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="1ada3-144">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="1ada3-145">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1ada3-145">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="1ada3-146">*Klammer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ada3-146">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ada3-147">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="1ada3-147">Type: **float**</span></span>

<span data-ttu-id="1ada3-148">Ein optionaler Wert zum Einspannen von Sample-Lod-Werten.</span><span class="sxs-lookup"><span data-stu-id="1ada3-148">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="1ada3-149">Wenn Sie beispielsweise 2.0 f als Klammer Wert übergeben, stellen Sie sicher, dass kein einzelnes Beispiel auf eine MIP-Ebene kleiner als 2.0 f zugreift.</span><span class="sxs-lookup"><span data-stu-id="1ada3-149">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ada3-150">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1ada3-150">Return value</span></span>

<span data-ttu-id="1ada3-151">Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="1ada3-151">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="1ada3-152">Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="1ada3-152">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="1ada3-153">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1ada3-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ada3-154">Samplebias-Methoden</span><span class="sxs-lookup"><span data-stu-id="1ada3-154">SampleBias methods</span></span>](texture1d-samplebias.md)
</dt> </dl>

 

 
