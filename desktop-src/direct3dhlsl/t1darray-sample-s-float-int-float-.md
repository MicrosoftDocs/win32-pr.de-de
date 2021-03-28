---
title: 'Texture1DArray:: Sample (S, float, int, float)-Funktion'
description: 'Gibt eine Textur mit einem optionalen Wert aus, mit dem die Werte der Sample-Ebene (LOD) an eine Klammer angezeigt werden. | Texture1DArray:: Sample (S, float, int, float)-Funktion'
ms.assetid: 3A965EEE-FCA3-4DD8-87D2-56679DFF5D3A
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
ms.openlocfilehash: 16d0a651d70aa618b9791fb760c51dfa05945752
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995662"
---
# <a name="texture1darraysamplesfloatintfloat-function"></a><span data-ttu-id="a60be-105">Texture1DArray:: Sample (S, float, int, float)-Funktion</span><span class="sxs-lookup"><span data-stu-id="a60be-105">Texture1DArray::Sample(S,float,int,float) function</span></span>

<span data-ttu-id="a60be-106">Gibt eine Textur mit einem optionalen Wert aus, mit dem die Werte der Sample-Ebene (LOD) an eine Klammer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a60be-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="a60be-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a60be-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in SamplerState S,
  in float        Location,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="a60be-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a60be-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a60be-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a60be-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a60be-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="a60be-110">Type: **SamplerState**</span></span>

<span data-ttu-id="a60be-111">Ein [samplerzustand](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="a60be-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="a60be-112">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="a60be-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="a60be-113">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a60be-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a60be-114">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="a60be-114">Type: **float**</span></span>

<span data-ttu-id="a60be-115">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="a60be-115">The texture coordinates.</span></span> <span data-ttu-id="a60be-116">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="a60be-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="a60be-117">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="a60be-117">Texture-Object Type</span></span>                    | <span data-ttu-id="a60be-118">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="a60be-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="a60be-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a60be-119">Texture1D</span></span>                              | <span data-ttu-id="a60be-120">float</span><span class="sxs-lookup"><span data-stu-id="a60be-120">float</span></span>          |
| <span data-ttu-id="a60be-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="a60be-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="a60be-122">float2</span><span class="sxs-lookup"><span data-stu-id="a60be-122">float2</span></span>         |
| <span data-ttu-id="a60be-123">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="a60be-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="a60be-124">float3</span><span class="sxs-lookup"><span data-stu-id="a60be-124">float3</span></span>         |
| <span data-ttu-id="a60be-125">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="a60be-125">TextureCubeArray</span></span>                       | <span data-ttu-id="a60be-126">float4</span><span class="sxs-lookup"><span data-stu-id="a60be-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="a60be-127">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a60be-127">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a60be-128">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="a60be-128">Type: **int**</span></span>

<span data-ttu-id="a60be-129">Ein optionaler Offset der Textur Koordinate, der für jeden Textur Objekttyp verwendet werden kann. der Offset wird vor der Stichprobenentnahme auf den Speicherort angewendet.</span><span class="sxs-lookup"><span data-stu-id="a60be-129">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="a60be-130">Verwenden Sie einen Offset nur bei einer ganzzahligen miplevel. Andernfalls erhalten Sie möglicherweise Ergebnisse, die nicht gut in Hardware übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="a60be-130">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="a60be-131">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="a60be-131">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="a60be-132">Weitere Informationen finden Sie unter [Anwenden von ganzzahligen Offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="a60be-132">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="a60be-133">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="a60be-133">Texture-Object Type</span></span>           | <span data-ttu-id="a60be-134">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="a60be-134">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="a60be-135">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="a60be-135">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="a60be-136">INT</span><span class="sxs-lookup"><span data-stu-id="a60be-136">int</span></span>            |
| <span data-ttu-id="a60be-137">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="a60be-137">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="a60be-138">int2</span><span class="sxs-lookup"><span data-stu-id="a60be-138">int2</span></span>           |
| <span data-ttu-id="a60be-139">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a60be-139">Texture3D</span></span>                     | <span data-ttu-id="a60be-140">int3</span><span class="sxs-lookup"><span data-stu-id="a60be-140">int3</span></span>           |
| <span data-ttu-id="a60be-141">Texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="a60be-141">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="a60be-142">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a60be-142">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="a60be-143">*Klammer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a60be-143">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a60be-144">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="a60be-144">Type: **float**</span></span>

<span data-ttu-id="a60be-145">Ein optionaler Wert zum Einspannen von Sample-Lod-Werten.</span><span class="sxs-lookup"><span data-stu-id="a60be-145">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="a60be-146">Wenn Sie beispielsweise 2.0 f als Klammer Wert übergeben, stellen Sie sicher, dass kein einzelnes Beispiel auf eine MIP-Ebene kleiner als 2.0 f zugreift.</span><span class="sxs-lookup"><span data-stu-id="a60be-146">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a60be-147">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a60be-147">Return value</span></span>

<span data-ttu-id="a60be-148">Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="a60be-148">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="a60be-149">Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="a60be-149">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="a60be-150">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a60be-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a60be-151">Beispiel Methoden</span><span class="sxs-lookup"><span data-stu-id="a60be-151">Sample methods</span></span>](texture1darray-sample.md)
</dt> </dl>

 

 
