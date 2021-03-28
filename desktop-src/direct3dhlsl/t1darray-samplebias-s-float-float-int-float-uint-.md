---
title: 'Samplebias:: samplebias (S, float, float, int, float, uint)-Funktion für Texture1DArray'
description: 'Gibt eine Textur aus, nachdem der Wert "Bias" auf die MipMap-Ebene angewendet wurde, mit einem optionalen Wert, mit dem Sample Level-of-Detail-Werte (LOD) an eine Klammer übergeben werden. | Samplebias:: samplebias (S, float, float, int, float, uint)-Funktion für Texture1DArray'
ms.assetid: 6136674B-38F4-4081-82D6-0731604EB1A3
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
ms.openlocfilehash: 4050503525345803a105d7717e96f6aa7b5c43cd
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104531112"
---
# <a name="samplebiassamplebiassfloatfloatintfloatuint-function-for-texture1darray"></a><span data-ttu-id="90313-105">Samplebias:: samplebias (S, float, float, int, float, uint)-Funktion für Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="90313-105">SampleBias::SampleBias(S,float,float,int,float,uint) function for Texture1DArray</span></span>

<span data-ttu-id="90313-106">Gibt eine Textur aus, nachdem der Wert "Bias" auf die MipMap-Ebene angewendet wurde, mit einem optionalen Wert, mit dem Sample Level-of-Detail-Werte (LOD) an eine Klammer übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="90313-106">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="90313-107">Gibt den Status des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="90313-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="90313-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="90313-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in  SamplerState S,
  in  float        Location,
  in  float        Bias,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="90313-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="90313-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90313-110">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="90313-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90313-111">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="90313-111">Type: **SamplerState**</span></span>

<span data-ttu-id="90313-112">Ein [samplerzustand](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="90313-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="90313-113">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="90313-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="90313-114">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="90313-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90313-115">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="90313-115">Type: **float**</span></span>

<span data-ttu-id="90313-116">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="90313-116">The texture coordinates.</span></span> <span data-ttu-id="90313-117">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="90313-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="90313-118">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="90313-118">Texture-Object Type</span></span>                    | <span data-ttu-id="90313-119">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="90313-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="90313-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="90313-120">Texture1D</span></span>                              | <span data-ttu-id="90313-121">float</span><span class="sxs-lookup"><span data-stu-id="90313-121">float</span></span>          |
| <span data-ttu-id="90313-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="90313-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="90313-123">float2</span><span class="sxs-lookup"><span data-stu-id="90313-123">float2</span></span>         |
| <span data-ttu-id="90313-124">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="90313-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="90313-125">float3</span><span class="sxs-lookup"><span data-stu-id="90313-125">float3</span></span>         |
| <span data-ttu-id="90313-126">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="90313-126">TextureCubeArray</span></span>                       | <span data-ttu-id="90313-127">float4</span><span class="sxs-lookup"><span data-stu-id="90313-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="90313-128">*Bias* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="90313-128">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90313-129">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="90313-129">Type: **float**</span></span>

<span data-ttu-id="90313-130">Der Bias-Wert, bei dem es sich um eine Gleit Komma Zahl zwischen 0,0 und 1,0 handelt, wird vor der Stichprobenentnahme auf eine MIP-Ebene angewendet.</span><span class="sxs-lookup"><span data-stu-id="90313-130">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="90313-131">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="90313-131">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90313-132">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="90313-132">Type: **int**</span></span>

<span data-ttu-id="90313-133">Ein optionaler Offset der Textur Koordinate, der für jeden Textur Objekttyp verwendet werden kann. der Offset wird vor der Stichprobenentnahme auf den Speicherort angewendet.</span><span class="sxs-lookup"><span data-stu-id="90313-133">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="90313-134">Verwenden Sie einen Offset nur bei einer ganzzahligen miplevel. Andernfalls erhalten Sie möglicherweise Ergebnisse, die nicht gut in Hardware übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="90313-134">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="90313-135">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="90313-135">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="90313-136">Weitere Informationen finden Sie unter [Anwenden von ganzzahligen Offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="90313-136">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="90313-137">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="90313-137">Texture-Object Type</span></span>           | <span data-ttu-id="90313-138">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="90313-138">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="90313-139">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="90313-139">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="90313-140">INT</span><span class="sxs-lookup"><span data-stu-id="90313-140">int</span></span>            |
| <span data-ttu-id="90313-141">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="90313-141">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="90313-142">int2</span><span class="sxs-lookup"><span data-stu-id="90313-142">int2</span></span>           |
| <span data-ttu-id="90313-143">Texture3D</span><span class="sxs-lookup"><span data-stu-id="90313-143">Texture3D</span></span>                     | <span data-ttu-id="90313-144">int3</span><span class="sxs-lookup"><span data-stu-id="90313-144">int3</span></span>           |
| <span data-ttu-id="90313-145">Texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="90313-145">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="90313-146">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="90313-146">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="90313-147">*Klammer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="90313-147">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90313-148">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="90313-148">Type: **float**</span></span>

<span data-ttu-id="90313-149">Ein optionaler Wert zum Einspannen von Sample-Lod-Werten.</span><span class="sxs-lookup"><span data-stu-id="90313-149">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="90313-150">Wenn Sie beispielsweise 2.0 f als Klammer Wert übergeben, stellen Sie sicher, dass kein einzelnes Beispiel auf eine MIP-Ebene kleiner als 2.0 f zugreift.</span><span class="sxs-lookup"><span data-stu-id="90313-150">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="90313-151">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="90313-151">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90313-152">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="90313-152">Type: **uint**</span></span>

<span data-ttu-id="90313-153">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="90313-153">The status of the operation.</span></span> <span data-ttu-id="90313-154">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="90313-154">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="90313-155">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="90313-155">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="90313-156">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="90313-156">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90313-157">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="90313-157">Return value</span></span>

<span data-ttu-id="90313-158">Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="90313-158">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="90313-159">Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="90313-159">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="90313-160">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="90313-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90313-161">Samplebias-Methoden</span><span class="sxs-lookup"><span data-stu-id="90313-161">SampleBias methods</span></span>](texture1darray-samplebias.md)
</dt> </dl>

 

 
