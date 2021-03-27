---
title: 'Samplecmp:: samplecmp (S, float, float, int, float)-Funktion für Texture2DArray'
description: Erfahren Sie, wie diese Funktion eine Textur mithilfe eines Vergleichs Werts zum ablehnen von Beispielen als Stichprobe verwendet, mit einem optionalen Wert, um Sample Level-of-Detail-Werte (LOD) zu binden. Für Texture2DArray.
ms.assetid: 6455BF80-2A22-43BB-80A2-61FBEC66C348
keywords:
- Samplecmp-Funktion HLSL
topic_type:
- apiref
api_name:
- SampleCmp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0692166766b9f52a1b6b13719c2427438b59835f
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "103762429"
---
# <a name="samplecmpsamplecmpsfloatfloatintfloat-function-for-texture2darray"></a><span data-ttu-id="4c52f-105">Samplecmp:: samplecmp (S, float, float, int, float)-Funktion für Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="4c52f-105">SampleCmp::SampleCmp(S,float,float,int,float) function for Texture2DArray</span></span>

<span data-ttu-id="4c52f-106">Verwendet einen Vergleichswert zum ablehnen von Beispielen, wobei ein optionaler Wert zum Einspannen von Samplingrate-Werten (LOD) an verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4c52f-106">Samples a texture, using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c52f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c52f-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmp(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="4c52f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4c52f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c52f-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4c52f-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c52f-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="4c52f-110">Type: **SamplerState**</span></span>

<span data-ttu-id="4c52f-111">Ein [samplerzustand](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="4c52f-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="4c52f-112">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="4c52f-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="4c52f-113">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4c52f-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c52f-114">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="4c52f-114">Type: **float**</span></span>

<span data-ttu-id="4c52f-115">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="4c52f-115">The texture coordinates.</span></span> <span data-ttu-id="4c52f-116">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="4c52f-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="4c52f-117">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="4c52f-117">Texture-Object Type</span></span>                    | <span data-ttu-id="4c52f-118">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="4c52f-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="4c52f-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4c52f-119">Texture1D</span></span>                              | <span data-ttu-id="4c52f-120">float</span><span class="sxs-lookup"><span data-stu-id="4c52f-120">float</span></span>          |
| <span data-ttu-id="4c52f-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="4c52f-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="4c52f-122">float2</span><span class="sxs-lookup"><span data-stu-id="4c52f-122">float2</span></span>         |
| <span data-ttu-id="4c52f-123">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="4c52f-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="4c52f-124">float3</span><span class="sxs-lookup"><span data-stu-id="4c52f-124">float3</span></span>         |
| <span data-ttu-id="4c52f-125">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="4c52f-125">TextureCubeArray</span></span>                       | <span data-ttu-id="4c52f-126">float4</span><span class="sxs-lookup"><span data-stu-id="4c52f-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="4c52f-127">*CompareValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4c52f-127">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c52f-128">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="4c52f-128">Type: **float**</span></span>

<span data-ttu-id="4c52f-129">Ein Gleit Komma Wert, der als Vergleichswert verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4c52f-129">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="4c52f-130">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4c52f-130">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c52f-131">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="4c52f-131">Type: **int**</span></span>

<span data-ttu-id="4c52f-132">Ein optionaler Offset der Textur Koordinate, der für jeden Textur Objekttyp verwendet werden kann. der Offset wird vor der Stichprobenentnahme auf den Speicherort angewendet.</span><span class="sxs-lookup"><span data-stu-id="4c52f-132">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="4c52f-133">Verwenden Sie einen Offset nur bei einer ganzzahligen miplevel. Andernfalls erhalten Sie möglicherweise Ergebnisse, die nicht gut in Hardware übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="4c52f-133">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="4c52f-134">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="4c52f-134">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="4c52f-135">Weitere Informationen finden Sie unter [Anwenden von ganzzahligen Offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="4c52f-135">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="4c52f-136">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="4c52f-136">Texture-Object Type</span></span>           | <span data-ttu-id="4c52f-137">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="4c52f-137">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="4c52f-138">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="4c52f-138">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="4c52f-139">INT</span><span class="sxs-lookup"><span data-stu-id="4c52f-139">int</span></span>            |
| <span data-ttu-id="4c52f-140">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="4c52f-140">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="4c52f-141">int2</span><span class="sxs-lookup"><span data-stu-id="4c52f-141">int2</span></span>           |
| <span data-ttu-id="4c52f-142">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4c52f-142">Texture3D</span></span>                     | <span data-ttu-id="4c52f-143">int3</span><span class="sxs-lookup"><span data-stu-id="4c52f-143">int3</span></span>           |
| <span data-ttu-id="4c52f-144">Texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="4c52f-144">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="4c52f-145">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="4c52f-145">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="4c52f-146">*Klammer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4c52f-146">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c52f-147">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="4c52f-147">Type: **float**</span></span>

<span data-ttu-id="4c52f-148">Ein optionaler Wert zum Einspannen von Sample-Lod-Werten.</span><span class="sxs-lookup"><span data-stu-id="4c52f-148">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="4c52f-149">Wenn Sie beispielsweise 2.0 f als Klammer Wert übergeben, stellen Sie sicher, dass kein einzelnes Beispiel auf eine MIP-Ebene kleiner als 2.0 f zugreift.</span><span class="sxs-lookup"><span data-stu-id="4c52f-149">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c52f-150">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4c52f-150">Return value</span></span>

<span data-ttu-id="4c52f-151">Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="4c52f-151">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="4c52f-152">Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="4c52f-152">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="4c52f-153">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4c52f-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c52f-154">Samplecmp-Methoden</span><span class="sxs-lookup"><span data-stu-id="4c52f-154">SampleCmp methods</span></span>](texture2darray-samplecmp.md)
</dt> </dl>

 

 
