---
title: 'Samplebias:: samplebias (S, float, float, int, float)-Funktion'
description: Abtast eine Texture2D, nachdem der Wert "Bias" auf die MipMap-Ebene angewendet wurde, mit einem optionalen Wert, um Sample Level-of-Detail-Werte (LOD) zu binden.
ms.assetid: 4E4A1188-DE45-4A43-B54D-4CA2E66707E3
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
ms.openlocfilehash: d91ce53da6dbf2c1e39f23967d1c1dc36085e764
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104039906"
---
# <a name="samplebiassamplebiassfloatfloatintfloat-function"></a><span data-ttu-id="aed19-104">Samplebias:: samplebias (S, float, float, int, float)-Funktion</span><span class="sxs-lookup"><span data-stu-id="aed19-104">SampleBias::SampleBias(S,float,float,int,float) function</span></span>

<span data-ttu-id="aed19-105">Abtast eine [**Texture2D**](sm5-object-texture2d.md), nachdem der Wert "Bias" auf die MipMap-Ebene angewendet wurde, mit einem optionalen Wert, um Sample Level-of-Detail-Werte (LOD) zu binden.</span><span class="sxs-lookup"><span data-stu-id="aed19-105">Samples a [**Texture2D**](sm5-object-texture2d.md), after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="aed19-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="aed19-106">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="aed19-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="aed19-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aed19-108">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aed19-108">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aed19-109">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="aed19-109">Type: **SamplerState**</span></span>

<span data-ttu-id="aed19-110">Ein [samplerzustand](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="aed19-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="aed19-111">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="aed19-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="aed19-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aed19-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aed19-113">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="aed19-113">Type: **float**</span></span>

<span data-ttu-id="aed19-114">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="aed19-114">The texture coordinates.</span></span> <span data-ttu-id="aed19-115">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="aed19-115">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="aed19-116">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="aed19-116">Texture-Object Type</span></span>                    | <span data-ttu-id="aed19-117">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="aed19-117">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="aed19-118">Texture1D</span><span class="sxs-lookup"><span data-stu-id="aed19-118">Texture1D</span></span>                              | <span data-ttu-id="aed19-119">float</span><span class="sxs-lookup"><span data-stu-id="aed19-119">float</span></span>          |
| <span data-ttu-id="aed19-120">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="aed19-120">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="aed19-121">float2</span><span class="sxs-lookup"><span data-stu-id="aed19-121">float2</span></span>         |
| <span data-ttu-id="aed19-122">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="aed19-122">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="aed19-123">float3</span><span class="sxs-lookup"><span data-stu-id="aed19-123">float3</span></span>         |
| <span data-ttu-id="aed19-124">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="aed19-124">TextureCubeArray</span></span>                       | <span data-ttu-id="aed19-125">float4</span><span class="sxs-lookup"><span data-stu-id="aed19-125">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="aed19-126">*Bias* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aed19-126">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aed19-127">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="aed19-127">Type: **float**</span></span>

<span data-ttu-id="aed19-128">Der Bias-Wert, bei dem es sich um eine Gleit Komma Zahl zwischen 0,0 und 1,0 handelt, wird vor der Stichprobenentnahme auf eine MIP-Ebene angewendet.</span><span class="sxs-lookup"><span data-stu-id="aed19-128">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="aed19-129">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aed19-129">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aed19-130">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="aed19-130">Type: **int**</span></span>

<span data-ttu-id="aed19-131">Ein optionaler Offset der Textur Koordinate, der für jeden Textur Objekttyp verwendet werden kann. der Offset wird vor der Stichprobenentnahme auf den Speicherort angewendet.</span><span class="sxs-lookup"><span data-stu-id="aed19-131">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="aed19-132">Verwenden Sie einen Offset nur bei einer ganzzahligen miplevel. Andernfalls erhalten Sie möglicherweise Ergebnisse, die nicht gut in Hardware übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="aed19-132">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="aed19-133">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="aed19-133">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="aed19-134">Weitere Informationen finden Sie unter [Anwenden von ganzzahligen Offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="aed19-134">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="aed19-135">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="aed19-135">Texture-Object Type</span></span>           | <span data-ttu-id="aed19-136">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="aed19-136">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="aed19-137">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="aed19-137">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="aed19-138">INT</span><span class="sxs-lookup"><span data-stu-id="aed19-138">int</span></span>            |
| <span data-ttu-id="aed19-139">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="aed19-139">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="aed19-140">int2</span><span class="sxs-lookup"><span data-stu-id="aed19-140">int2</span></span>           |
| <span data-ttu-id="aed19-141">Texture3D</span><span class="sxs-lookup"><span data-stu-id="aed19-141">Texture3D</span></span>                     | <span data-ttu-id="aed19-142">int3</span><span class="sxs-lookup"><span data-stu-id="aed19-142">int3</span></span>           |
| <span data-ttu-id="aed19-143">Texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="aed19-143">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="aed19-144">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="aed19-144">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="aed19-145">*Klammer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aed19-145">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aed19-146">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="aed19-146">Type: **float**</span></span>

<span data-ttu-id="aed19-147">Ein optionaler Wert zum Einspannen von Sample-Lod-Werten.</span><span class="sxs-lookup"><span data-stu-id="aed19-147">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="aed19-148">Wenn Sie beispielsweise 2.0 f als Klammer Wert übergeben, stellen Sie sicher, dass kein einzelnes Beispiel auf eine MIP-Ebene kleiner als 2.0 f zugreift.</span><span class="sxs-lookup"><span data-stu-id="aed19-148">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aed19-149">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aed19-149">Return value</span></span>

<span data-ttu-id="aed19-150">Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="aed19-150">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="aed19-151">Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="aed19-151">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="aed19-152">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="aed19-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aed19-153">Samplebias-Methoden</span><span class="sxs-lookup"><span data-stu-id="aed19-153">SampleBias methods</span></span>](texture2d-samplebias.md)
</dt> </dl>

 

 
