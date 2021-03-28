---
title: 'Texture1DArray:: Sample (S, float, int, float, uint)-Funktion'
description: 'Führt eine Stichprobe für eine Textur mit einem optionalen Wert aus, um die Samplingrate-Werte (LOD) zu binden, und gibt den Status des Vorgangs zurück. | Texture1DArray:: Sample (S, float, int, float, uint)-Funktion'
ms.assetid: 584901B7-4F58-4491-9543-F27433386292
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
ms.openlocfilehash: 4a2f608d7dbbd4eec51139b6f285529849f708af
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995751"
---
# <a name="texture1darraysamplesfloatintfloatuint-function"></a><span data-ttu-id="6cc31-105">Texture1DArray:: Sample (S, float, int, float, uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="6cc31-105">Texture1DArray::Sample(S,float,int,float,uint) function</span></span>

<span data-ttu-id="6cc31-106">Führt eine Stichprobe für eine Textur mit einem optionalen Wert aus, um die Samplingrate-Werte (LOD) zu binden, und gibt den Status des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="6cc31-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to, and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cc31-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6cc31-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float        Location,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="6cc31-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6cc31-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cc31-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6cc31-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cc31-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="6cc31-110">Type: **SamplerState**</span></span>

<span data-ttu-id="6cc31-111">Ein [samplerzustand](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="6cc31-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="6cc31-112">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="6cc31-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="6cc31-113">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6cc31-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cc31-114">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="6cc31-114">Type: **float**</span></span>

<span data-ttu-id="6cc31-115">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="6cc31-115">The texture coordinates.</span></span> <span data-ttu-id="6cc31-116">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="6cc31-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="6cc31-117">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="6cc31-117">Texture-Object Type</span></span>                    | <span data-ttu-id="6cc31-118">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="6cc31-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="6cc31-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6cc31-119">Texture1D</span></span>                              | <span data-ttu-id="6cc31-120">float</span><span class="sxs-lookup"><span data-stu-id="6cc31-120">float</span></span>          |
| <span data-ttu-id="6cc31-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="6cc31-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="6cc31-122">float2</span><span class="sxs-lookup"><span data-stu-id="6cc31-122">float2</span></span>         |
| <span data-ttu-id="6cc31-123">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="6cc31-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="6cc31-124">float3</span><span class="sxs-lookup"><span data-stu-id="6cc31-124">float3</span></span>         |
| <span data-ttu-id="6cc31-125">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="6cc31-125">TextureCubeArray</span></span>                       | <span data-ttu-id="6cc31-126">float4</span><span class="sxs-lookup"><span data-stu-id="6cc31-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="6cc31-127">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6cc31-127">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cc31-128">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="6cc31-128">Type: **int**</span></span>

<span data-ttu-id="6cc31-129">Ein optionaler Offset der Textur Koordinate, der für jeden Textur Objekttyp verwendet werden kann. der Offset wird vor der Stichprobenentnahme auf den Speicherort angewendet.</span><span class="sxs-lookup"><span data-stu-id="6cc31-129">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="6cc31-130">Verwenden Sie einen Offset nur bei einer ganzzahligen miplevel. Andernfalls erhalten Sie möglicherweise Ergebnisse, die nicht gut in Hardware übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="6cc31-130">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="6cc31-131">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="6cc31-131">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="6cc31-132">Weitere Informationen finden Sie unter [Anwenden von ganzzahligen Offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="6cc31-132">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="6cc31-133">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="6cc31-133">Texture-Object Type</span></span>           | <span data-ttu-id="6cc31-134">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="6cc31-134">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="6cc31-135">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="6cc31-135">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="6cc31-136">INT</span><span class="sxs-lookup"><span data-stu-id="6cc31-136">int</span></span>            |
| <span data-ttu-id="6cc31-137">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="6cc31-137">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="6cc31-138">int2</span><span class="sxs-lookup"><span data-stu-id="6cc31-138">int2</span></span>           |
| <span data-ttu-id="6cc31-139">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6cc31-139">Texture3D</span></span>                     | <span data-ttu-id="6cc31-140">int3</span><span class="sxs-lookup"><span data-stu-id="6cc31-140">int3</span></span>           |
| <span data-ttu-id="6cc31-141">Texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="6cc31-141">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="6cc31-142">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6cc31-142">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="6cc31-143">*Klammer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6cc31-143">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cc31-144">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="6cc31-144">Type: **float**</span></span>

<span data-ttu-id="6cc31-145">Ein optionaler Wert zum Einspannen von Sample-Lod-Werten.</span><span class="sxs-lookup"><span data-stu-id="6cc31-145">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="6cc31-146">Wenn Sie beispielsweise 2.0 f als Klammer Wert übergeben, stellen Sie sicher, dass kein einzelnes Beispiel auf eine MIP-Ebene kleiner als 2.0 f zugreift.</span><span class="sxs-lookup"><span data-stu-id="6cc31-146">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="6cc31-147">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6cc31-147">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6cc31-148">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="6cc31-148">Type: **uint**</span></span>

<span data-ttu-id="6cc31-149">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="6cc31-149">The status of the operation.</span></span> <span data-ttu-id="6cc31-150">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="6cc31-150">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="6cc31-151">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="6cc31-151">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="6cc31-152">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="6cc31-152">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cc31-153">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6cc31-153">Return value</span></span>

<span data-ttu-id="6cc31-154">Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="6cc31-154">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="6cc31-155">Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="6cc31-155">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="6cc31-156">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6cc31-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cc31-157">Beispiel Methoden</span><span class="sxs-lookup"><span data-stu-id="6cc31-157">Sample methods</span></span>](texture1darray-sample.md)
</dt> </dl>

 

 
