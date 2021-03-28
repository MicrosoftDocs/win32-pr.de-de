---
title: 'Samplebias:: samplebias (S, float, float, int, float, uint)-Funktion für Texture2D'
description: 'Die samplebias:: samplebias (S, float, float, int, float, uint)-Funktion Stichproben ein Texture2D, nachdem der Bias-Wert auf die MipMap-Ebene angewendet wurde.'
ms.assetid: ACABF551-1DBF-4979-B0B1-D025E04EC08C
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
ms.openlocfilehash: 86840748d12a92eca24b8d0d2bfba26eee69cff5
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982788"
---
# <a name="samplebiassamplebiassfloatfloatintfloatuint-function-for-texture2d"></a><span data-ttu-id="085b9-104">Samplebias:: samplebias (S, float, float, int, float, uint)-Funktion für Texture2D</span><span class="sxs-lookup"><span data-stu-id="085b9-104">SampleBias::SampleBias(S,float,float,int,float,uint) function for Texture2D</span></span>

<span data-ttu-id="085b9-105">Abtast eine [**Texture2D**](sm5-object-texture2d.md), nachdem der Wert "Bias" auf die MipMap-Ebene angewendet wurde, mit einem optionalen Wert, um Sample Level-of-Detail-Werte (LOD) zu binden.</span><span class="sxs-lookup"><span data-stu-id="085b9-105">Samples a [**Texture2D**](sm5-object-texture2d.md), after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="085b9-106">Gibt den Status des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="085b9-106">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="085b9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="085b9-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="085b9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="085b9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="085b9-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="085b9-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="085b9-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="085b9-110">Type: **SamplerState**</span></span>

<span data-ttu-id="085b9-111">Ein [samplerzustand](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="085b9-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="085b9-112">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="085b9-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="085b9-113">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="085b9-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="085b9-114">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="085b9-114">Type: **float**</span></span>

<span data-ttu-id="085b9-115">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="085b9-115">The texture coordinates.</span></span> <span data-ttu-id="085b9-116">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="085b9-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="085b9-117">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="085b9-117">Texture-Object Type</span></span>                    | <span data-ttu-id="085b9-118">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="085b9-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="085b9-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="085b9-119">Texture1D</span></span>                              | <span data-ttu-id="085b9-120">float</span><span class="sxs-lookup"><span data-stu-id="085b9-120">float</span></span>          |
| <span data-ttu-id="085b9-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="085b9-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="085b9-122">float2</span><span class="sxs-lookup"><span data-stu-id="085b9-122">float2</span></span>         |
| <span data-ttu-id="085b9-123">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="085b9-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="085b9-124">float3</span><span class="sxs-lookup"><span data-stu-id="085b9-124">float3</span></span>         |
| <span data-ttu-id="085b9-125">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="085b9-125">TextureCubeArray</span></span>                       | <span data-ttu-id="085b9-126">float4</span><span class="sxs-lookup"><span data-stu-id="085b9-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="085b9-127">*Bias* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="085b9-127">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="085b9-128">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="085b9-128">Type: **float**</span></span>

<span data-ttu-id="085b9-129">Der Bias-Wert, bei dem es sich um eine Gleit Komma Zahl zwischen 0,0 und 1,0 handelt, wird vor der Stichprobenentnahme auf eine MIP-Ebene angewendet.</span><span class="sxs-lookup"><span data-stu-id="085b9-129">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="085b9-130">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="085b9-130">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="085b9-131">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="085b9-131">Type: **int**</span></span>

<span data-ttu-id="085b9-132">Ein optionaler Offset der Textur Koordinate, der für jeden Textur Objekttyp verwendet werden kann. der Offset wird vor der Stichprobenentnahme auf den Speicherort angewendet.</span><span class="sxs-lookup"><span data-stu-id="085b9-132">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="085b9-133">Verwenden Sie einen Offset nur bei einer ganzzahligen miplevel. Andernfalls erhalten Sie möglicherweise Ergebnisse, die nicht gut in Hardware übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="085b9-133">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="085b9-134">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="085b9-134">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="085b9-135">Weitere Informationen finden Sie unter [Anwenden von ganzzahligen Offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="085b9-135">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="085b9-136">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="085b9-136">Texture-Object Type</span></span>           | <span data-ttu-id="085b9-137">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="085b9-137">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="085b9-138">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="085b9-138">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="085b9-139">INT</span><span class="sxs-lookup"><span data-stu-id="085b9-139">int</span></span>            |
| <span data-ttu-id="085b9-140">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="085b9-140">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="085b9-141">int2</span><span class="sxs-lookup"><span data-stu-id="085b9-141">int2</span></span>           |
| <span data-ttu-id="085b9-142">Texture3D</span><span class="sxs-lookup"><span data-stu-id="085b9-142">Texture3D</span></span>                     | <span data-ttu-id="085b9-143">int3</span><span class="sxs-lookup"><span data-stu-id="085b9-143">int3</span></span>           |
| <span data-ttu-id="085b9-144">Texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="085b9-144">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="085b9-145">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="085b9-145">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="085b9-146">*Klammer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="085b9-146">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="085b9-147">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="085b9-147">Type: **float**</span></span>

<span data-ttu-id="085b9-148">Ein optionaler Wert zum Einspannen von Sample-Lod-Werten.</span><span class="sxs-lookup"><span data-stu-id="085b9-148">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="085b9-149">Wenn Sie beispielsweise 2.0 f als Klammer Wert übergeben, stellen Sie sicher, dass kein einzelnes Beispiel auf eine MIP-Ebene kleiner als 2.0 f zugreift.</span><span class="sxs-lookup"><span data-stu-id="085b9-149">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="085b9-150">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="085b9-150">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="085b9-151">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="085b9-151">Type: **uint**</span></span>

<span data-ttu-id="085b9-152">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="085b9-152">The status of the operation.</span></span> <span data-ttu-id="085b9-153">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="085b9-153">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="085b9-154">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="085b9-154">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="085b9-155">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="085b9-155">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="085b9-156">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="085b9-156">Return value</span></span>

<span data-ttu-id="085b9-157">Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="085b9-157">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="085b9-158">Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="085b9-158">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="085b9-159">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="085b9-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="085b9-160">Samplebias-Methoden</span><span class="sxs-lookup"><span data-stu-id="085b9-160">SampleBias methods</span></span>](texture2d-samplebias.md)
</dt> </dl>

 

 
