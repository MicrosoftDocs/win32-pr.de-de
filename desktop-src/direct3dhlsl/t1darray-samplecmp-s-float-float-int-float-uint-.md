---
title: 'Samplecmp:: samplecmp (S, float, float, int, float, uint)-Funktion für Texture1DArray'
description: Erfahren Sie, wie diese Funktion eine Textur mithilfe eines Vergleichs Werts zum ablehnen von Beispielen als Stichprobe verwendet, mit einem optionalen Wert, um Sample Level-of-Detail-Werte (LOD) zu binden. Für Texture1DArray.
ms.assetid: 33F15F14-EA14-448B-8D45-F6A3932FECD0
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
ms.openlocfilehash: e3415539cc59b156c99492d3a4174d171bb5e8c3
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104356177"
---
# <a name="samplecmpsamplecmpsfloatfloatintfloatuint-function-for-texture1darray"></a><span data-ttu-id="5ccf0-105">Samplecmp:: samplecmp (S, float, float, int, float, uint)-Funktion für Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="5ccf0-105">SampleCmp::SampleCmp(S,float,float,int,float,uint) function for Texture1DArray</span></span>

<span data-ttu-id="5ccf0-106">Verwendet einen Vergleichswert zum ablehnen von Beispielen, wobei ein optionaler Wert zum Einspannen von Samplingrate-Werten (LOD) an verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5ccf0-106">Samples a texture, using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="5ccf0-107">Gibt den Status des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="5ccf0-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ccf0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ccf0-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmp(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="5ccf0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ccf0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ccf0-110">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ccf0-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ccf0-111">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="5ccf0-111">Type: **SamplerState**</span></span>

<span data-ttu-id="5ccf0-112">Ein [samplerzustand](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="5ccf0-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="5ccf0-113">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="5ccf0-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="5ccf0-114">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ccf0-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ccf0-115">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="5ccf0-115">Type: **float**</span></span>

<span data-ttu-id="5ccf0-116">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="5ccf0-116">The texture coordinates.</span></span> <span data-ttu-id="5ccf0-117">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="5ccf0-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="5ccf0-118">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="5ccf0-118">Texture-Object Type</span></span>                    | <span data-ttu-id="5ccf0-119">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="5ccf0-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="5ccf0-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5ccf0-120">Texture1D</span></span>                              | <span data-ttu-id="5ccf0-121">float</span><span class="sxs-lookup"><span data-stu-id="5ccf0-121">float</span></span>          |
| <span data-ttu-id="5ccf0-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="5ccf0-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="5ccf0-123">float2</span><span class="sxs-lookup"><span data-stu-id="5ccf0-123">float2</span></span>         |
| <span data-ttu-id="5ccf0-124">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="5ccf0-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="5ccf0-125">float3</span><span class="sxs-lookup"><span data-stu-id="5ccf0-125">float3</span></span>         |
| <span data-ttu-id="5ccf0-126">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="5ccf0-126">TextureCubeArray</span></span>                       | <span data-ttu-id="5ccf0-127">float4</span><span class="sxs-lookup"><span data-stu-id="5ccf0-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="5ccf0-128">*CompareValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ccf0-128">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ccf0-129">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="5ccf0-129">Type: **float**</span></span>

<span data-ttu-id="5ccf0-130">Ein Gleit Komma Wert, der als Vergleichswert verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5ccf0-130">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="5ccf0-131">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ccf0-131">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ccf0-132">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="5ccf0-132">Type: **int**</span></span>

<span data-ttu-id="5ccf0-133">Ein optionaler Offset der Textur Koordinate, der für jeden Textur Objekttyp verwendet werden kann. der Offset wird vor der Stichprobenentnahme auf den Speicherort angewendet.</span><span class="sxs-lookup"><span data-stu-id="5ccf0-133">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="5ccf0-134">Verwenden Sie einen Offset nur bei einer ganzzahligen miplevel. Andernfalls erhalten Sie möglicherweise Ergebnisse, die nicht gut in Hardware übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="5ccf0-134">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="5ccf0-135">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="5ccf0-135">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="5ccf0-136">Weitere Informationen finden Sie unter [Anwenden von ganzzahligen Offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="5ccf0-136">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="5ccf0-137">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="5ccf0-137">Texture-Object Type</span></span>           | <span data-ttu-id="5ccf0-138">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="5ccf0-138">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="5ccf0-139">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="5ccf0-139">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="5ccf0-140">INT</span><span class="sxs-lookup"><span data-stu-id="5ccf0-140">int</span></span>            |
| <span data-ttu-id="5ccf0-141">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="5ccf0-141">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="5ccf0-142">int2</span><span class="sxs-lookup"><span data-stu-id="5ccf0-142">int2</span></span>           |
| <span data-ttu-id="5ccf0-143">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5ccf0-143">Texture3D</span></span>                     | <span data-ttu-id="5ccf0-144">int3</span><span class="sxs-lookup"><span data-stu-id="5ccf0-144">int3</span></span>           |
| <span data-ttu-id="5ccf0-145">Texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="5ccf0-145">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="5ccf0-146">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="5ccf0-146">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="5ccf0-147">*Klammer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ccf0-147">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ccf0-148">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="5ccf0-148">Type: **float**</span></span>

<span data-ttu-id="5ccf0-149">Ein optionaler Wert zum Einspannen von Sample-Lod-Werten.</span><span class="sxs-lookup"><span data-stu-id="5ccf0-149">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="5ccf0-150">Wenn Sie beispielsweise 2.0 f als Klammer Wert übergeben, stellen Sie sicher, dass kein einzelnes Beispiel auf eine MIP-Ebene kleiner als 2.0 f zugreift.</span><span class="sxs-lookup"><span data-stu-id="5ccf0-150">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="5ccf0-151">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5ccf0-151">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ccf0-152">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="5ccf0-152">Type: **uint**</span></span>

<span data-ttu-id="5ccf0-153">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="5ccf0-153">The status of the operation.</span></span> <span data-ttu-id="5ccf0-154">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="5ccf0-154">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="5ccf0-155">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="5ccf0-155">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="5ccf0-156">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="5ccf0-156">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ccf0-157">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5ccf0-157">Return value</span></span>

<span data-ttu-id="5ccf0-158">Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="5ccf0-158">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="5ccf0-159">Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="5ccf0-159">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="5ccf0-160">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5ccf0-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ccf0-161">Samplecmp-Methoden</span><span class="sxs-lookup"><span data-stu-id="5ccf0-161">SampleCmp methods</span></span>](texture1darray-samplecmp.md)
</dt> </dl>

 

 
