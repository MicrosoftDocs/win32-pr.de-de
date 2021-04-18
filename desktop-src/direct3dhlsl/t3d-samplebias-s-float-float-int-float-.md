---
title: 'Samplebias:: samplebias (S, float, float, int, float)-Funktion für Texture3D'
description: 'Die samplebias:: samplebias (S, float, float, int, float)-Funktion für Texture3D gibt eine Textur aus, nachdem der Wert des Bias auf die MipMap-Ebene angewendet wurde.'
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
ms.openlocfilehash: c7ef038a3faa4cb0a208e9a9d05de230d2b87231
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "106355076"
---
# <a name="samplebiassamplebiassfloatfloatintfloat-function-for-texture3d"></a><span data-ttu-id="6268b-104">Samplebias:: samplebias (S, float, float, int, float)-Funktion für Texture3D</span><span class="sxs-lookup"><span data-stu-id="6268b-104">SampleBias::SampleBias(S,float,float,int,float) function for Texture3D</span></span>

<span data-ttu-id="6268b-105">Gibt eine Textur aus, nachdem der Wert "Bias" auf die MipMap-Ebene angewendet wurde, mit einem optionalen Wert, mit dem Sample Level-of-Detail-Werte (LOD) an eine Klammer übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="6268b-105">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="6268b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6268b-106">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="6268b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="6268b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6268b-108">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6268b-108">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6268b-109">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="6268b-109">Type: **SamplerState**</span></span>

<span data-ttu-id="6268b-110">Ein [samplerzustand](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="6268b-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="6268b-111">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="6268b-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="6268b-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6268b-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6268b-113">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="6268b-113">Type: **float**</span></span>

<span data-ttu-id="6268b-114">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="6268b-114">The texture coordinates.</span></span> <span data-ttu-id="6268b-115">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="6268b-115">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="6268b-116">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="6268b-116">Texture-Object Type</span></span>                    | <span data-ttu-id="6268b-117">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="6268b-117">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="6268b-118">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6268b-118">Texture1D</span></span>                              | <span data-ttu-id="6268b-119">float</span><span class="sxs-lookup"><span data-stu-id="6268b-119">float</span></span>          |
| <span data-ttu-id="6268b-120">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="6268b-120">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="6268b-121">float2</span><span class="sxs-lookup"><span data-stu-id="6268b-121">float2</span></span>         |
| <span data-ttu-id="6268b-122">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="6268b-122">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="6268b-123">float3</span><span class="sxs-lookup"><span data-stu-id="6268b-123">float3</span></span>         |
| <span data-ttu-id="6268b-124">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="6268b-124">TextureCubeArray</span></span>                       | <span data-ttu-id="6268b-125">float4</span><span class="sxs-lookup"><span data-stu-id="6268b-125">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="6268b-126">*Bias* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6268b-126">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6268b-127">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="6268b-127">Type: **float**</span></span>

<span data-ttu-id="6268b-128">Der Bias-Wert, bei dem es sich um eine Gleit Komma Zahl zwischen 0,0 und 1,0 handelt, wird vor der Stichprobenentnahme auf eine MIP-Ebene angewendet.</span><span class="sxs-lookup"><span data-stu-id="6268b-128">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="6268b-129">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6268b-129">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6268b-130">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="6268b-130">Type: **int**</span></span>

<span data-ttu-id="6268b-131">Ein optionaler Offset der Textur Koordinate, der für jeden Textur Objekttyp verwendet werden kann. der Offset wird vor der Stichprobenentnahme auf den Speicherort angewendet.</span><span class="sxs-lookup"><span data-stu-id="6268b-131">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="6268b-132">Verwenden Sie einen Offset nur bei einer ganzzahligen miplevel. Andernfalls erhalten Sie möglicherweise Ergebnisse, die nicht gut in Hardware übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="6268b-132">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="6268b-133">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="6268b-133">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="6268b-134">Weitere Informationen finden Sie unter [Anwenden von ganzzahligen Offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="6268b-134">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="6268b-135">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="6268b-135">Texture-Object Type</span></span>           | <span data-ttu-id="6268b-136">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="6268b-136">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="6268b-137">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="6268b-137">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="6268b-138">INT</span><span class="sxs-lookup"><span data-stu-id="6268b-138">int</span></span>            |
| <span data-ttu-id="6268b-139">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="6268b-139">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="6268b-140">int2</span><span class="sxs-lookup"><span data-stu-id="6268b-140">int2</span></span>           |
| <span data-ttu-id="6268b-141">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6268b-141">Texture3D</span></span>                     | <span data-ttu-id="6268b-142">int3</span><span class="sxs-lookup"><span data-stu-id="6268b-142">int3</span></span>           |
| <span data-ttu-id="6268b-143">Texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="6268b-143">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="6268b-144">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6268b-144">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="6268b-145">*Klammer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6268b-145">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6268b-146">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="6268b-146">Type: **float**</span></span>

<span data-ttu-id="6268b-147">Ein optionaler Wert zum Einspannen von Sample-Lod-Werten.</span><span class="sxs-lookup"><span data-stu-id="6268b-147">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="6268b-148">Wenn Sie beispielsweise 2.0 f als Klammer Wert übergeben, stellen Sie sicher, dass kein einzelnes Beispiel auf eine MIP-Ebene kleiner als 2.0 f zugreift.</span><span class="sxs-lookup"><span data-stu-id="6268b-148">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6268b-149">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6268b-149">Return value</span></span>

<span data-ttu-id="6268b-150">Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="6268b-150">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="6268b-151">Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="6268b-151">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="6268b-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6268b-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6268b-153">Samplebias-Methoden</span><span class="sxs-lookup"><span data-stu-id="6268b-153">SampleBias methods</span></span>](texture3d-samplebias.md)
</dt> <dt>

[<span data-ttu-id="6268b-154">**Texture3D**</span><span class="sxs-lookup"><span data-stu-id="6268b-154">**Texture3D**</span></span>](sm5-object-texture3d.md)
</dt> </dl>

 

 
