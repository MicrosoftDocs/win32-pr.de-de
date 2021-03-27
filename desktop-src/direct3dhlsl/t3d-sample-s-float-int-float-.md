---
title: 'Texture3D:: Sample (S, float, int, float)-Funktion'
description: 'Gibt eine Textur mit einem optionalen Wert aus, mit dem die Werte der Sample-Ebene (LOD) an eine Klammer angezeigt werden. | Texture3D:: Sample (S, float, int, float)-Funktion'
ms.assetid: A1114A4A-16B9-4A5D-9A9D-262D6BAA9F2E
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
ms.openlocfilehash: 11577e6151d2353477a70e6ef2873d287eb71a87
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995343"
---
# <a name="texture3dsamplesfloatintfloat-function"></a><span data-ttu-id="b3ed1-105">Texture3D:: Sample (S, float, int, float)-Funktion</span><span class="sxs-lookup"><span data-stu-id="b3ed1-105">Texture3D::Sample(S,float,int,float) function</span></span>

<span data-ttu-id="b3ed1-106">Gibt eine Textur mit einem optionalen Wert aus, mit dem die Werte der Sample-Ebene (LOD) an eine Klammer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b3ed1-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3ed1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3ed1-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in SamplerState S,
  in float        Location,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="b3ed1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3ed1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3ed1-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b3ed1-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3ed1-110">Ein [samplerzustand](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="b3ed1-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="b3ed1-111">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="b3ed1-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="b3ed1-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b3ed1-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3ed1-113">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="b3ed1-113">The texture coordinates.</span></span> <span data-ttu-id="b3ed1-114">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="b3ed1-114">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="b3ed1-115">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="b3ed1-115">Texture-Object Type</span></span>                    | <span data-ttu-id="b3ed1-116">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="b3ed1-116">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="b3ed1-117">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b3ed1-117">Texture1D</span></span>                              | <span data-ttu-id="b3ed1-118">float</span><span class="sxs-lookup"><span data-stu-id="b3ed1-118">float</span></span>          |
| <span data-ttu-id="b3ed1-119">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="b3ed1-119">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="b3ed1-120">float2</span><span class="sxs-lookup"><span data-stu-id="b3ed1-120">float2</span></span>         |
| <span data-ttu-id="b3ed1-121">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="b3ed1-121">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="b3ed1-122">float3</span><span class="sxs-lookup"><span data-stu-id="b3ed1-122">float3</span></span>         |
| <span data-ttu-id="b3ed1-123">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="b3ed1-123">TextureCubeArray</span></span>                       | <span data-ttu-id="b3ed1-124">float4</span><span class="sxs-lookup"><span data-stu-id="b3ed1-124">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="b3ed1-125">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b3ed1-125">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3ed1-126">Ein optionaler Offset der Textur Koordinate, der für jeden Textur Objekttyp verwendet werden kann. der Offset wird vor der Stichprobenentnahme auf den Speicherort angewendet.</span><span class="sxs-lookup"><span data-stu-id="b3ed1-126">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="b3ed1-127">Verwenden Sie einen Offset nur bei einer ganzzahligen miplevel. Andernfalls erhalten Sie möglicherweise Ergebnisse, die nicht gut in Hardware übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="b3ed1-127">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="b3ed1-128">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="b3ed1-128">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="b3ed1-129">Weitere Informationen finden Sie unter [Anwenden von ganzzahligen Offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="b3ed1-129">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="b3ed1-130">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="b3ed1-130">Texture-Object Type</span></span>           | <span data-ttu-id="b3ed1-131">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="b3ed1-131">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="b3ed1-132">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="b3ed1-132">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="b3ed1-133">INT</span><span class="sxs-lookup"><span data-stu-id="b3ed1-133">int</span></span>            |
| <span data-ttu-id="b3ed1-134">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="b3ed1-134">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="b3ed1-135">int2</span><span class="sxs-lookup"><span data-stu-id="b3ed1-135">int2</span></span>           |
| <span data-ttu-id="b3ed1-136">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b3ed1-136">Texture3D</span></span>                     | <span data-ttu-id="b3ed1-137">int3</span><span class="sxs-lookup"><span data-stu-id="b3ed1-137">int3</span></span>           |
| <span data-ttu-id="b3ed1-138">Texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="b3ed1-138">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="b3ed1-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b3ed1-139">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="b3ed1-140">*Klammer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b3ed1-140">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3ed1-141">Ein optionaler Wert zum Einspannen von Sample-Lod-Werten.</span><span class="sxs-lookup"><span data-stu-id="b3ed1-141">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="b3ed1-142">Wenn Sie beispielsweise 2.0 f als Klammer Wert übergeben, stellen Sie sicher, dass kein einzelnes Beispiel auf eine MIP-Ebene kleiner als 2.0 f zugreift.</span><span class="sxs-lookup"><span data-stu-id="b3ed1-142">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3ed1-143">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b3ed1-143">Return value</span></span>

<span data-ttu-id="b3ed1-144">Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="b3ed1-144">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="b3ed1-145">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b3ed1-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3ed1-146">Beispiel Methoden</span><span class="sxs-lookup"><span data-stu-id="b3ed1-146">Sample methods</span></span>](texture3d-sample.md)
</dt> <dt>

[<span data-ttu-id="b3ed1-147">**Texture3D**</span><span class="sxs-lookup"><span data-stu-id="b3ed1-147">**Texture3D**</span></span>](sm5-object-texture3d.md)
</dt> </dl>

 

 
