---
title: 'Samplebias:: samplebias (S, float, float, int, float, uint)-Funktion für Texture2DArray'
description: 'Die samplebias:: samplebias (S, float, float, int, float, uint)-Funktion für Texture2DArray Samples eine Textur, nachdem der Bias-Wert auf die MipMap-Ebene angewendet wurde.'
ms.assetid: 38DC341D-477A-4709-AC97-EB796A40C4B2
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
ms.openlocfilehash: ab86510f1450080844a6fe7e476381e81bed1ce1
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982772"
---
# <a name="samplebiassamplebiassfloatfloatintfloatuint-function-for-texture2darray"></a><span data-ttu-id="83290-104">Samplebias:: samplebias (S, float, float, int, float, uint)-Funktion für Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="83290-104">SampleBias::SampleBias(S,float,float,int,float,uint) function for Texture2DArray</span></span>

<span data-ttu-id="83290-105">Gibt eine Textur aus, nachdem der Wert "Bias" auf die MipMap-Ebene angewendet wurde, mit einem optionalen Wert, mit dem Sample Level-of-Detail-Werte (LOD) an eine Klammer übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="83290-105">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="83290-106">Gibt den Status des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="83290-106">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="83290-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="83290-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="83290-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="83290-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83290-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="83290-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83290-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="83290-110">Type: **SamplerState**</span></span>

<span data-ttu-id="83290-111">Ein [samplerzustand](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="83290-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="83290-112">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="83290-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="83290-113">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="83290-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83290-114">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="83290-114">Type: **float**</span></span>

<span data-ttu-id="83290-115">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="83290-115">The texture coordinates.</span></span> <span data-ttu-id="83290-116">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="83290-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="83290-117">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="83290-117">Texture-Object Type</span></span>                    | <span data-ttu-id="83290-118">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="83290-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="83290-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="83290-119">Texture1D</span></span>                              | <span data-ttu-id="83290-120">float</span><span class="sxs-lookup"><span data-stu-id="83290-120">float</span></span>          |
| <span data-ttu-id="83290-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="83290-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="83290-122">float2</span><span class="sxs-lookup"><span data-stu-id="83290-122">float2</span></span>         |
| <span data-ttu-id="83290-123">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="83290-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="83290-124">float3</span><span class="sxs-lookup"><span data-stu-id="83290-124">float3</span></span>         |
| <span data-ttu-id="83290-125">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="83290-125">TextureCubeArray</span></span>                       | <span data-ttu-id="83290-126">float4</span><span class="sxs-lookup"><span data-stu-id="83290-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="83290-127">*Bias* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="83290-127">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83290-128">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="83290-128">Type: **float**</span></span>

<span data-ttu-id="83290-129">Der Bias-Wert, bei dem es sich um eine Gleit Komma Zahl zwischen 0,0 und 1,0 handelt, wird vor der Stichprobenentnahme auf eine MIP-Ebene angewendet.</span><span class="sxs-lookup"><span data-stu-id="83290-129">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="83290-130">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="83290-130">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83290-131">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="83290-131">Type: **int**</span></span>

<span data-ttu-id="83290-132">Ein optionaler Offset der Textur Koordinate, der für jeden Textur Objekttyp verwendet werden kann. der Offset wird vor der Stichprobenentnahme auf den Speicherort angewendet.</span><span class="sxs-lookup"><span data-stu-id="83290-132">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="83290-133">Verwenden Sie einen Offset nur bei einer ganzzahligen miplevel. Andernfalls erhalten Sie möglicherweise Ergebnisse, die nicht gut in Hardware übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="83290-133">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="83290-134">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="83290-134">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="83290-135">Weitere Informationen finden Sie unter [Anwenden von ganzzahligen Offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="83290-135">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="83290-136">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="83290-136">Texture-Object Type</span></span>           | <span data-ttu-id="83290-137">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="83290-137">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="83290-138">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="83290-138">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="83290-139">INT</span><span class="sxs-lookup"><span data-stu-id="83290-139">int</span></span>            |
| <span data-ttu-id="83290-140">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="83290-140">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="83290-141">int2</span><span class="sxs-lookup"><span data-stu-id="83290-141">int2</span></span>           |
| <span data-ttu-id="83290-142">Texture3D</span><span class="sxs-lookup"><span data-stu-id="83290-142">Texture3D</span></span>                     | <span data-ttu-id="83290-143">int3</span><span class="sxs-lookup"><span data-stu-id="83290-143">int3</span></span>           |
| <span data-ttu-id="83290-144">Texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="83290-144">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="83290-145">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="83290-145">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="83290-146">*Klammer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="83290-146">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83290-147">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="83290-147">Type: **float**</span></span>

<span data-ttu-id="83290-148">Ein optionaler Wert zum Einspannen von Sample-Lod-Werten.</span><span class="sxs-lookup"><span data-stu-id="83290-148">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="83290-149">Wenn Sie beispielsweise 2.0 f als Klammer Wert übergeben, stellen Sie sicher, dass kein einzelnes Beispiel auf eine MIP-Ebene kleiner als 2.0 f zugreift.</span><span class="sxs-lookup"><span data-stu-id="83290-149">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="83290-150">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="83290-150">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="83290-151">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="83290-151">Type: **uint**</span></span>

<span data-ttu-id="83290-152">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="83290-152">The status of the operation.</span></span> <span data-ttu-id="83290-153">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="83290-153">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="83290-154">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="83290-154">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="83290-155">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="83290-155">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83290-156">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="83290-156">Return value</span></span>

<span data-ttu-id="83290-157">Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="83290-157">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="83290-158">Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="83290-158">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="83290-159">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="83290-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83290-160">Samplebias-Methoden</span><span class="sxs-lookup"><span data-stu-id="83290-160">SampleBias methods</span></span>](texture2darray-samplebias.md)
</dt> </dl>

 

 
