---
title: 'Samplebias:: samplebias (S, float, float, int, float, uint)-Funktion für Texture3D'
description: 'Gibt eine Textur aus, nachdem der Wert "Bias" auf die MipMap-Ebene angewendet wurde, mit einem optionalen Wert, mit dem Sample Level-of-Detail-Werte (LOD) an eine Klammer übergeben werden. | Samplebias:: samplebias (S, float, float, int, float, uint)-Funktion für Texture3D'
ms.assetid: 87B06414-F1A3-4BC8-B7DE-137B2156CFA7
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
ms.openlocfilehash: e6155bbd4a3b21b86add57d13bc14a1185c76b73
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982669"
---
# <a name="samplebiassamplebiassfloatfloatintfloatuint-function-for-texture3d"></a><span data-ttu-id="05407-105">Samplebias:: samplebias (S, float, float, int, float, uint)-Funktion für Texture3D</span><span class="sxs-lookup"><span data-stu-id="05407-105">SampleBias::SampleBias(S,float,float,int,float,uint) function for Texture3D</span></span>

<span data-ttu-id="05407-106">Gibt eine Textur aus, nachdem der Wert "Bias" auf die MipMap-Ebene angewendet wurde, mit einem optionalen Wert, mit dem Sample Level-of-Detail-Werte (LOD) an eine Klammer übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="05407-106">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="05407-107">Gibt den Status des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="05407-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="05407-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="05407-108">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="05407-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="05407-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05407-110">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="05407-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05407-111">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="05407-111">Type: **SamplerState**</span></span>

<span data-ttu-id="05407-112">Ein [samplerzustand](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="05407-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="05407-113">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="05407-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="05407-114">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="05407-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05407-115">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="05407-115">Type: **float**</span></span>

<span data-ttu-id="05407-116">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="05407-116">The texture coordinates.</span></span> <span data-ttu-id="05407-117">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="05407-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="05407-118">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="05407-118">Texture-Object Type</span></span>                    | <span data-ttu-id="05407-119">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="05407-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="05407-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="05407-120">Texture1D</span></span>                              | <span data-ttu-id="05407-121">float</span><span class="sxs-lookup"><span data-stu-id="05407-121">float</span></span>          |
| <span data-ttu-id="05407-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="05407-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="05407-123">float2</span><span class="sxs-lookup"><span data-stu-id="05407-123">float2</span></span>         |
| <span data-ttu-id="05407-124">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="05407-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="05407-125">float3</span><span class="sxs-lookup"><span data-stu-id="05407-125">float3</span></span>         |
| <span data-ttu-id="05407-126">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="05407-126">TextureCubeArray</span></span>                       | <span data-ttu-id="05407-127">float4</span><span class="sxs-lookup"><span data-stu-id="05407-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="05407-128">*Bias* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="05407-128">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05407-129">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="05407-129">Type: **float**</span></span>

<span data-ttu-id="05407-130">Der Bias-Wert, bei dem es sich um eine Gleit Komma Zahl zwischen 0,0 und 1,0 handelt, wird vor der Stichprobenentnahme auf eine MIP-Ebene angewendet.</span><span class="sxs-lookup"><span data-stu-id="05407-130">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="05407-131">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="05407-131">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05407-132">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="05407-132">Type: **int**</span></span>

<span data-ttu-id="05407-133">Ein optionaler Offset der Textur Koordinate, der für jeden Textur Objekttyp verwendet werden kann. der Offset wird vor der Stichprobenentnahme auf den Speicherort angewendet.</span><span class="sxs-lookup"><span data-stu-id="05407-133">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="05407-134">Verwenden Sie einen Offset nur bei einer ganzzahligen miplevel. Andernfalls erhalten Sie möglicherweise Ergebnisse, die nicht gut in Hardware übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="05407-134">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="05407-135">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="05407-135">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="05407-136">Weitere Informationen finden Sie unter [Anwenden von ganzzahligen Offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="05407-136">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="05407-137">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="05407-137">Texture-Object Type</span></span>           | <span data-ttu-id="05407-138">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="05407-138">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="05407-139">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="05407-139">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="05407-140">INT</span><span class="sxs-lookup"><span data-stu-id="05407-140">int</span></span>            |
| <span data-ttu-id="05407-141">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="05407-141">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="05407-142">int2</span><span class="sxs-lookup"><span data-stu-id="05407-142">int2</span></span>           |
| <span data-ttu-id="05407-143">Texture3D</span><span class="sxs-lookup"><span data-stu-id="05407-143">Texture3D</span></span>                     | <span data-ttu-id="05407-144">int3</span><span class="sxs-lookup"><span data-stu-id="05407-144">int3</span></span>           |
| <span data-ttu-id="05407-145">Texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="05407-145">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="05407-146">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="05407-146">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="05407-147">*Klammer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="05407-147">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05407-148">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="05407-148">Type: **float**</span></span>

<span data-ttu-id="05407-149">Ein optionaler Wert zum Einspannen von Sample-Lod-Werten.</span><span class="sxs-lookup"><span data-stu-id="05407-149">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="05407-150">Wenn Sie beispielsweise 2.0 f als Klammer Wert übergeben, stellen Sie sicher, dass kein einzelnes Beispiel auf eine MIP-Ebene kleiner als 2.0 f zugreift.</span><span class="sxs-lookup"><span data-stu-id="05407-150">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="05407-151">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="05407-151">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05407-152">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="05407-152">Type: **uint**</span></span>

<span data-ttu-id="05407-153">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="05407-153">The status of the operation.</span></span> <span data-ttu-id="05407-154">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="05407-154">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="05407-155">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="05407-155">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="05407-156">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="05407-156">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05407-157">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="05407-157">Return value</span></span>

<span data-ttu-id="05407-158">Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="05407-158">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="05407-159">Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="05407-159">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="05407-160">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="05407-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05407-161">Samplebias-Methoden</span><span class="sxs-lookup"><span data-stu-id="05407-161">SampleBias methods</span></span>](texture3d-samplebias.md)
</dt> <dt>

[<span data-ttu-id="05407-162">**Texture3D**</span><span class="sxs-lookup"><span data-stu-id="05407-162">**Texture3D**</span></span>](sm5-object-texture3d.md)
</dt> </dl>

 

 
