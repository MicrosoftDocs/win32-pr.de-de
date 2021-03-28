---
title: 'Texture1D:: Sample (S, float, int, float)-Funktion'
description: 'Gibt eine Textur mit einem optionalen Wert aus, mit dem die Werte der Sample-Ebene (LOD) an eine Klammer angezeigt werden. | Texture1D:: Sample (S, float, int, float)-Funktion'
ms.assetid: D2E2E143-8240-43AA-AD70-BD793B3CFD19
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
ms.openlocfilehash: f119955a66f7aec336ce52d730d54a5f11756527
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104050794"
---
# <a name="texture1dsamplesfloatintfloat-function"></a><span data-ttu-id="a315b-105">Texture1D:: Sample (S, float, int, float)-Funktion</span><span class="sxs-lookup"><span data-stu-id="a315b-105">Texture1D::Sample(S,float,int,float) function</span></span>

<span data-ttu-id="a315b-106">Gibt eine Textur mit einem optionalen Wert aus, mit dem die Werte der Sample-Ebene (LOD) an eine Klammer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a315b-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="a315b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a315b-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in SamplerState S,
  in float        Location,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="a315b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a315b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a315b-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a315b-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a315b-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="a315b-110">Type: **SamplerState**</span></span>

<span data-ttu-id="a315b-111">Ein [samplerzustand](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="a315b-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="a315b-112">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="a315b-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="a315b-113">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a315b-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a315b-114">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="a315b-114">Type: **float**</span></span>

<span data-ttu-id="a315b-115">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="a315b-115">The texture coordinates.</span></span> <span data-ttu-id="a315b-116">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="a315b-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="a315b-117">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="a315b-117">Texture-Object Type</span></span>                    | <span data-ttu-id="a315b-118">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="a315b-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="a315b-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a315b-119">Texture1D</span></span>                              | <span data-ttu-id="a315b-120">float</span><span class="sxs-lookup"><span data-stu-id="a315b-120">float</span></span>          |
| <span data-ttu-id="a315b-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="a315b-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="a315b-122">float2</span><span class="sxs-lookup"><span data-stu-id="a315b-122">float2</span></span>         |
| <span data-ttu-id="a315b-123">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="a315b-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="a315b-124">float3</span><span class="sxs-lookup"><span data-stu-id="a315b-124">float3</span></span>         |
| <span data-ttu-id="a315b-125">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="a315b-125">TextureCubeArray</span></span>                       | <span data-ttu-id="a315b-126">float4</span><span class="sxs-lookup"><span data-stu-id="a315b-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="a315b-127">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a315b-127">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a315b-128">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="a315b-128">Type: **int**</span></span>

<span data-ttu-id="a315b-129">Ein optionaler Offset der Textur Koordinate, der für jeden Textur Objekttyp verwendet werden kann. der Offset wird vor der Stichprobenentnahme auf den Speicherort angewendet.</span><span class="sxs-lookup"><span data-stu-id="a315b-129">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="a315b-130">Verwenden Sie einen Offset nur bei einer ganzzahligen miplevel. Andernfalls erhalten Sie möglicherweise Ergebnisse, die nicht gut in Hardware übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="a315b-130">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="a315b-131">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="a315b-131">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="a315b-132">Weitere Informationen finden Sie unter [Anwenden von ganzzahligen Offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="a315b-132">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="a315b-133">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="a315b-133">Texture-Object Type</span></span>           | <span data-ttu-id="a315b-134">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="a315b-134">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="a315b-135">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="a315b-135">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="a315b-136">INT</span><span class="sxs-lookup"><span data-stu-id="a315b-136">int</span></span>            |
| <span data-ttu-id="a315b-137">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="a315b-137">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="a315b-138">int2</span><span class="sxs-lookup"><span data-stu-id="a315b-138">int2</span></span>           |
| <span data-ttu-id="a315b-139">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a315b-139">Texture3D</span></span>                     | <span data-ttu-id="a315b-140">int3</span><span class="sxs-lookup"><span data-stu-id="a315b-140">int3</span></span>           |
| <span data-ttu-id="a315b-141">Texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="a315b-141">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="a315b-142">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a315b-142">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="a315b-143">*Klammer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a315b-143">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a315b-144">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="a315b-144">Type: **float**</span></span>

<span data-ttu-id="a315b-145">Ein optionaler Wert zum Einspannen von Sample-Lod-Werten.</span><span class="sxs-lookup"><span data-stu-id="a315b-145">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="a315b-146">Wenn Sie beispielsweise 2.0 f als Klammer Wert übergeben, stellen Sie sicher, dass kein einzelnes Beispiel auf eine MIP-Ebene kleiner als 2.0 f zugreift.</span><span class="sxs-lookup"><span data-stu-id="a315b-146">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a315b-147">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a315b-147">Return value</span></span>

<span data-ttu-id="a315b-148">Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="a315b-148">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="a315b-149">Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="a315b-149">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="a315b-150">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a315b-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a315b-151">Beispiel Methoden</span><span class="sxs-lookup"><span data-stu-id="a315b-151">Sample methods</span></span>](texture1d-sample.md)
</dt> </dl>

 

 
