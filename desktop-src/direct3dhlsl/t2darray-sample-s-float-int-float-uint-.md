---
title: 'Texture2DArray:: Sample (S, float, int, float, uint)-Funktion'
description: 'Führt eine Stichprobe für eine Textur mit einem optionalen Wert aus, um die Samplingrate-Werte (LOD) zu binden, und gibt den Status des Vorgangs zurück. | Texture2DArray:: Sample (S, float, int, float, uint)-Funktion'
ms.assetid: 0F9DBC0D-F35D-4A7A-B8F5-1EFBF7E14615
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
ms.openlocfilehash: e2027377a1659aa46fcf10e39f39b21e2243c943
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981193"
---
# <a name="texture2darraysamplesfloatintfloatuint-function"></a><span data-ttu-id="c9792-105">Texture2DArray:: Sample (S, float, int, float, uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="c9792-105">Texture2DArray::Sample(S,float,int,float,uint) function</span></span>

<span data-ttu-id="c9792-106">Führt eine Stichprobe für eine Textur mit einem optionalen Wert aus, um die Samplingrate-Werte (LOD) zu binden, und gibt den Status des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="c9792-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to, and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9792-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9792-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float        Location,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="c9792-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9792-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9792-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c9792-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9792-110">Ein [samplerzustand](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="c9792-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="c9792-111">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="c9792-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="c9792-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c9792-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9792-113">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="c9792-113">The texture coordinates.</span></span> <span data-ttu-id="c9792-114">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="c9792-114">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="c9792-115">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="c9792-115">Texture-Object Type</span></span>                    | <span data-ttu-id="c9792-116">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="c9792-116">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="c9792-117">Texture1D</span><span class="sxs-lookup"><span data-stu-id="c9792-117">Texture1D</span></span>                              | <span data-ttu-id="c9792-118">float</span><span class="sxs-lookup"><span data-stu-id="c9792-118">float</span></span>          |
| <span data-ttu-id="c9792-119">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="c9792-119">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="c9792-120">float2</span><span class="sxs-lookup"><span data-stu-id="c9792-120">float2</span></span>         |
| <span data-ttu-id="c9792-121">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="c9792-121">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="c9792-122">float3</span><span class="sxs-lookup"><span data-stu-id="c9792-122">float3</span></span>         |
| <span data-ttu-id="c9792-123">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="c9792-123">TextureCubeArray</span></span>                       | <span data-ttu-id="c9792-124">float4</span><span class="sxs-lookup"><span data-stu-id="c9792-124">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="c9792-125">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c9792-125">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9792-126">Ein optionaler Offset der Textur Koordinate, der für jeden Textur Objekttyp verwendet werden kann. der Offset wird vor der Stichprobenentnahme auf den Speicherort angewendet.</span><span class="sxs-lookup"><span data-stu-id="c9792-126">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="c9792-127">Verwenden Sie einen Offset nur bei einer ganzzahligen miplevel. Andernfalls erhalten Sie möglicherweise Ergebnisse, die nicht gut in Hardware übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="c9792-127">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="c9792-128">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="c9792-128">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="c9792-129">Weitere Informationen finden Sie unter [Anwenden von ganzzahligen Offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="c9792-129">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="c9792-130">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="c9792-130">Texture-Object Type</span></span>           | <span data-ttu-id="c9792-131">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="c9792-131">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="c9792-132">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="c9792-132">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="c9792-133">INT</span><span class="sxs-lookup"><span data-stu-id="c9792-133">int</span></span>            |
| <span data-ttu-id="c9792-134">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="c9792-134">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="c9792-135">int2</span><span class="sxs-lookup"><span data-stu-id="c9792-135">int2</span></span>           |
| <span data-ttu-id="c9792-136">Texture3D</span><span class="sxs-lookup"><span data-stu-id="c9792-136">Texture3D</span></span>                     | <span data-ttu-id="c9792-137">int3</span><span class="sxs-lookup"><span data-stu-id="c9792-137">int3</span></span>           |
| <span data-ttu-id="c9792-138">Texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="c9792-138">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="c9792-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c9792-139">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="c9792-140">*Klammer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c9792-140">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9792-141">Ein optionaler Wert zum Einspannen von Sample-Lod-Werten.</span><span class="sxs-lookup"><span data-stu-id="c9792-141">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="c9792-142">Wenn Sie beispielsweise 2.0 f als Klammer Wert übergeben, stellen Sie sicher, dass kein einzelnes Beispiel auf eine MIP-Ebene kleiner als 2.0 f zugreift.</span><span class="sxs-lookup"><span data-stu-id="c9792-142">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="c9792-143">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c9792-143">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9792-144">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="c9792-144">The status of the operation.</span></span> <span data-ttu-id="c9792-145">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="c9792-145">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="c9792-146">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="c9792-146">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="c9792-147">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="c9792-147">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9792-148">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c9792-148">Return value</span></span>

<span data-ttu-id="c9792-149">Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="c9792-149">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="c9792-150">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c9792-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9792-151">Beispiel Methoden</span><span class="sxs-lookup"><span data-stu-id="c9792-151">Sample methods</span></span>](texture2darray-sample.md)
</dt> </dl>

 

 
