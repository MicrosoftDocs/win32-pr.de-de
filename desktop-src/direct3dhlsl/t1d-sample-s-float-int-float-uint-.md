---
title: 'Texture1D:: Sample (S, float, int, float, uint)-Funktion'
description: 'Führt eine Stichprobe für eine Textur mit einem optionalen Wert aus, um die Samplingrate-Werte (LOD) zu binden, und gibt den Status des Vorgangs zurück. | Texture1D:: Sample (S, float, int, float, uint)-Funktion'
ms.assetid: AF987A41-385D-4A77-B3FD-FE5523A6CC5C
keywords:
- Beispiel Funktion HLSL
topic_type:
- apiref
api_name:
- Sample
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9fad13781cbf862e386293ff96f8e99b57603c76
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995527"
---
# <a name="texture1dsamplesfloatintfloatuint-function"></a><span data-ttu-id="fd9cf-105">Texture1D:: Sample (S, float, int, float, uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd9cf-105">Texture1D::Sample(S,float,int,float,uint) function</span></span>

<span data-ttu-id="fd9cf-106">Führt eine Stichprobe für eine Textur mit einem optionalen Wert aus, um die Samplingrate-Werte (LOD) zu binden, und gibt den Status des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="fd9cf-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to, and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd9cf-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd9cf-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float        Location,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="fd9cf-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd9cf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd9cf-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd9cf-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd9cf-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="fd9cf-110">Type: **SamplerState**</span></span>

<span data-ttu-id="fd9cf-111">Ein [samplerzustand](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="fd9cf-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="fd9cf-112">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="fd9cf-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="fd9cf-113">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd9cf-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd9cf-114">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="fd9cf-114">Type: **float**</span></span>

<span data-ttu-id="fd9cf-115">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="fd9cf-115">The texture coordinates.</span></span> <span data-ttu-id="fd9cf-116">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="fd9cf-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="fd9cf-117">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="fd9cf-117">Texture-Object Type</span></span>                    | <span data-ttu-id="fd9cf-118">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="fd9cf-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="fd9cf-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fd9cf-119">Texture1D</span></span>                              | <span data-ttu-id="fd9cf-120">float</span><span class="sxs-lookup"><span data-stu-id="fd9cf-120">float</span></span>          |
| <span data-ttu-id="fd9cf-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="fd9cf-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="fd9cf-122">float2</span><span class="sxs-lookup"><span data-stu-id="fd9cf-122">float2</span></span>         |
| <span data-ttu-id="fd9cf-123">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="fd9cf-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="fd9cf-124">float3</span><span class="sxs-lookup"><span data-stu-id="fd9cf-124">float3</span></span>         |
| <span data-ttu-id="fd9cf-125">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="fd9cf-125">TextureCubeArray</span></span>                       | <span data-ttu-id="fd9cf-126">float4</span><span class="sxs-lookup"><span data-stu-id="fd9cf-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="fd9cf-127">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd9cf-127">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd9cf-128">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="fd9cf-128">Type: **int**</span></span>

<span data-ttu-id="fd9cf-129">Ein optionaler Offset der Textur Koordinate, der für jeden Textur Objekttyp verwendet werden kann. der Offset wird vor der Stichprobenentnahme auf den Speicherort angewendet.</span><span class="sxs-lookup"><span data-stu-id="fd9cf-129">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="fd9cf-130">Verwenden Sie einen Offset nur bei einer ganzzahligen miplevel. Andernfalls erhalten Sie möglicherweise Ergebnisse, die nicht gut in Hardware übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="fd9cf-130">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="fd9cf-131">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="fd9cf-131">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="fd9cf-132">Weitere Informationen finden Sie unter [Anwenden von ganzzahligen Offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="fd9cf-132">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="fd9cf-133">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="fd9cf-133">Texture-Object Type</span></span>           | <span data-ttu-id="fd9cf-134">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="fd9cf-134">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="fd9cf-135">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="fd9cf-135">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="fd9cf-136">INT</span><span class="sxs-lookup"><span data-stu-id="fd9cf-136">int</span></span>            |
| <span data-ttu-id="fd9cf-137">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="fd9cf-137">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="fd9cf-138">int2</span><span class="sxs-lookup"><span data-stu-id="fd9cf-138">int2</span></span>           |
| <span data-ttu-id="fd9cf-139">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fd9cf-139">Texture3D</span></span>                     | <span data-ttu-id="fd9cf-140">int3</span><span class="sxs-lookup"><span data-stu-id="fd9cf-140">int3</span></span>           |
| <span data-ttu-id="fd9cf-141">Texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="fd9cf-141">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="fd9cf-142">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="fd9cf-142">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="fd9cf-143">*Klammer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd9cf-143">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd9cf-144">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="fd9cf-144">Type: **float**</span></span>

<span data-ttu-id="fd9cf-145">Ein optionaler Wert zum Einspannen von Sample-Lod-Werten.</span><span class="sxs-lookup"><span data-stu-id="fd9cf-145">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="fd9cf-146">Wenn Sie beispielsweise 2.0 f als Klammer Wert übergeben, stellen Sie sicher, dass kein einzelnes Beispiel auf eine MIP-Ebene kleiner als 2.0 f zugreift.</span><span class="sxs-lookup"><span data-stu-id="fd9cf-146">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="fd9cf-147">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fd9cf-147">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd9cf-148">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="fd9cf-148">Type: **uint**</span></span>

<span data-ttu-id="fd9cf-149">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="fd9cf-149">The status of the operation.</span></span> <span data-ttu-id="fd9cf-150">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="fd9cf-150">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="fd9cf-151">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="fd9cf-151">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="fd9cf-152">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="fd9cf-152">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd9cf-153">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fd9cf-153">Return value</span></span>

<span data-ttu-id="fd9cf-154">Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="fd9cf-154">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="fd9cf-155">Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="fd9cf-155">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="fd9cf-156">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="fd9cf-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd9cf-157">Beispiel Methoden</span><span class="sxs-lookup"><span data-stu-id="fd9cf-157">Sample methods</span></span>](texture1d-sample.md)
</dt> </dl>

 

 
