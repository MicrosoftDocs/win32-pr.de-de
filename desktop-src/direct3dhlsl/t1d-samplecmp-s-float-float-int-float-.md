---
title: 'Samplecmp:: samplecmp (S, float, float, int, float)-Funktion für Texture1D'
description: 'Verwendet einen Vergleichswert zum ablehnen von Beispielen, wobei ein optionaler Wert zum Einspannen von Samplingrate-Werten (LOD) an verwendet wird. | Samplecmp:: samplecmp (S, float, float, int, float)-Funktion für Texture1D'
ms.assetid: 91AD0B59-D3F0-4A0D-8825-17282815D64B
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
ms.openlocfilehash: 811636e7e7002afedf026d4e3955f08f647c2c5d
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104996386"
---
# <a name="samplecmpsamplecmpsfloatfloatintfloat-function-for-texture1d"></a><span data-ttu-id="12fa8-105">Samplecmp:: samplecmp (S, float, float, int, float)-Funktion für Texture1D</span><span class="sxs-lookup"><span data-stu-id="12fa8-105">SampleCmp::SampleCmp(S,float,float,int,float) function for Texture1D</span></span>

<span data-ttu-id="12fa8-106">Verwendet einen Vergleichswert zum ablehnen von Beispielen, wobei ein optionaler Wert zum Einspannen von Samplingrate-Werten (LOD) an verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="12fa8-106">Samples a texture, using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="12fa8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="12fa8-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmp(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="12fa8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="12fa8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12fa8-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12fa8-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12fa8-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="12fa8-110">Type: **SamplerState**</span></span>

<span data-ttu-id="12fa8-111">Ein [samplerzustand](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="12fa8-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="12fa8-112">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="12fa8-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="12fa8-113">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12fa8-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12fa8-114">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="12fa8-114">Type: **float**</span></span>

<span data-ttu-id="12fa8-115">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="12fa8-115">The texture coordinates.</span></span> <span data-ttu-id="12fa8-116">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="12fa8-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="12fa8-117">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="12fa8-117">Texture-Object Type</span></span>                    | <span data-ttu-id="12fa8-118">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="12fa8-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="12fa8-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="12fa8-119">Texture1D</span></span>                              | <span data-ttu-id="12fa8-120">float</span><span class="sxs-lookup"><span data-stu-id="12fa8-120">float</span></span>          |
| <span data-ttu-id="12fa8-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="12fa8-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="12fa8-122">float2</span><span class="sxs-lookup"><span data-stu-id="12fa8-122">float2</span></span>         |
| <span data-ttu-id="12fa8-123">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="12fa8-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="12fa8-124">float3</span><span class="sxs-lookup"><span data-stu-id="12fa8-124">float3</span></span>         |
| <span data-ttu-id="12fa8-125">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="12fa8-125">TextureCubeArray</span></span>                       | <span data-ttu-id="12fa8-126">float4</span><span class="sxs-lookup"><span data-stu-id="12fa8-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="12fa8-127">*CompareValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12fa8-127">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12fa8-128">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="12fa8-128">Type: **float**</span></span>

<span data-ttu-id="12fa8-129">Ein Gleit Komma Wert, der als Vergleichswert verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="12fa8-129">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="12fa8-130">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12fa8-130">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12fa8-131">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="12fa8-131">Type: **int**</span></span>

<span data-ttu-id="12fa8-132">Ein optionaler Offset der Textur Koordinate, der für jeden Textur Objekttyp verwendet werden kann. der Offset wird vor der Stichprobenentnahme auf den Speicherort angewendet.</span><span class="sxs-lookup"><span data-stu-id="12fa8-132">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="12fa8-133">Verwenden Sie einen Offset nur bei einer ganzzahligen miplevel. Andernfalls erhalten Sie möglicherweise Ergebnisse, die nicht gut in Hardware übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="12fa8-133">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="12fa8-134">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="12fa8-134">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="12fa8-135">Weitere Informationen finden Sie unter [Anwenden von ganzzahligen Offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="12fa8-135">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="12fa8-136">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="12fa8-136">Texture-Object Type</span></span>           | <span data-ttu-id="12fa8-137">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="12fa8-137">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="12fa8-138">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="12fa8-138">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="12fa8-139">INT</span><span class="sxs-lookup"><span data-stu-id="12fa8-139">int</span></span>            |
| <span data-ttu-id="12fa8-140">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="12fa8-140">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="12fa8-141">int2</span><span class="sxs-lookup"><span data-stu-id="12fa8-141">int2</span></span>           |
| <span data-ttu-id="12fa8-142">Texture3D</span><span class="sxs-lookup"><span data-stu-id="12fa8-142">Texture3D</span></span>                     | <span data-ttu-id="12fa8-143">int3</span><span class="sxs-lookup"><span data-stu-id="12fa8-143">int3</span></span>           |
| <span data-ttu-id="12fa8-144">Texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="12fa8-144">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="12fa8-145">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="12fa8-145">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="12fa8-146">*Klammer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12fa8-146">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12fa8-147">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="12fa8-147">Type: **float**</span></span>

<span data-ttu-id="12fa8-148">Ein optionaler Wert zum Einspannen von Sample-Lod-Werten.</span><span class="sxs-lookup"><span data-stu-id="12fa8-148">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="12fa8-149">Wenn Sie beispielsweise 2.0 f als Klammer Wert übergeben, stellen Sie sicher, dass kein einzelnes Beispiel auf eine MIP-Ebene kleiner als 2.0 f zugreift.</span><span class="sxs-lookup"><span data-stu-id="12fa8-149">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12fa8-150">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="12fa8-150">Return value</span></span>

<span data-ttu-id="12fa8-151">Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="12fa8-151">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="12fa8-152">Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="12fa8-152">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="12fa8-153">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="12fa8-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12fa8-154">Samplecmp-Methoden</span><span class="sxs-lookup"><span data-stu-id="12fa8-154">SampleCmp methods</span></span>](texture1d-samplecmp.md)
</dt> </dl>

 

 
