---
title: 'Samplecmp:: samplecmp (S, float, float, int, float)-Funktion) für Texture2D'
description: Diese Funktion ist ein Beispiel für eine Texture2D, die einen Vergleichswert verwendet, um Beispiele abzulehnen, mit einem optionalen Wert, mit dem Samplingrate-Werte (LOD-Werte) an eine Klammer.
ms.assetid: 1B5E6559-2524-4557-8F43-7AF258C39FB2
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
ms.openlocfilehash: 9df6a84fff7c6988ed9333584a7196fa06ad30ec
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982781"
---
# <a name="samplecmpsamplecmpsfloatfloatintfloat-function-for-texture2d"></a><span data-ttu-id="cc708-104">Samplecmp:: samplecmp (S, float, float, int, float)-Funktion für Texture2D</span><span class="sxs-lookup"><span data-stu-id="cc708-104">SampleCmp::SampleCmp(S,float,float,int,float) function for Texture2D</span></span>

<span data-ttu-id="cc708-105">Stichproben [**Texture2D**](sm5-object-texture2d.md)mit einem Vergleichswert zum ablehnen von Beispielen, mit einem optionalen Wert, mit dem Samplingrate-Werte (LOD-Werte) an eine Klammer überstehen.</span><span class="sxs-lookup"><span data-stu-id="cc708-105">Samples a [**Texture2D**](sm5-object-texture2d.md), using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc708-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc708-106">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmp(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="cc708-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc708-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc708-108">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cc708-108">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc708-109">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="cc708-109">Type: **SamplerState**</span></span>

<span data-ttu-id="cc708-110">Ein [samplerzustand](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="cc708-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="cc708-111">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="cc708-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="cc708-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cc708-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc708-113">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="cc708-113">Type: **float**</span></span>

<span data-ttu-id="cc708-114">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="cc708-114">The texture coordinates.</span></span> <span data-ttu-id="cc708-115">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="cc708-115">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="cc708-116">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="cc708-116">Texture-Object Type</span></span>                    | <span data-ttu-id="cc708-117">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="cc708-117">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="cc708-118">Texture1D</span><span class="sxs-lookup"><span data-stu-id="cc708-118">Texture1D</span></span>                              | <span data-ttu-id="cc708-119">float</span><span class="sxs-lookup"><span data-stu-id="cc708-119">float</span></span>          |
| <span data-ttu-id="cc708-120">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="cc708-120">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="cc708-121">float2</span><span class="sxs-lookup"><span data-stu-id="cc708-121">float2</span></span>         |
| <span data-ttu-id="cc708-122">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="cc708-122">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="cc708-123">float3</span><span class="sxs-lookup"><span data-stu-id="cc708-123">float3</span></span>         |
| <span data-ttu-id="cc708-124">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="cc708-124">TextureCubeArray</span></span>                       | <span data-ttu-id="cc708-125">float4</span><span class="sxs-lookup"><span data-stu-id="cc708-125">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="cc708-126">*CompareValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cc708-126">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc708-127">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="cc708-127">Type: **float**</span></span>

<span data-ttu-id="cc708-128">Ein Gleit Komma Wert, der als Vergleichswert verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc708-128">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="cc708-129">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cc708-129">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc708-130">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="cc708-130">Type: **int**</span></span>

<span data-ttu-id="cc708-131">Ein optionaler Offset der Textur Koordinate, der für jeden Textur Objekttyp verwendet werden kann. der Offset wird vor der Stichprobenentnahme auf den Speicherort angewendet.</span><span class="sxs-lookup"><span data-stu-id="cc708-131">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="cc708-132">Verwenden Sie einen Offset nur bei einer ganzzahligen miplevel. Andernfalls erhalten Sie möglicherweise Ergebnisse, die nicht gut in Hardware übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="cc708-132">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="cc708-133">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="cc708-133">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="cc708-134">Weitere Informationen finden Sie unter [Anwenden von ganzzahligen Offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="cc708-134">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="cc708-135">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="cc708-135">Texture-Object Type</span></span>           | <span data-ttu-id="cc708-136">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="cc708-136">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="cc708-137">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="cc708-137">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="cc708-138">INT</span><span class="sxs-lookup"><span data-stu-id="cc708-138">int</span></span>            |
| <span data-ttu-id="cc708-139">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="cc708-139">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="cc708-140">int2</span><span class="sxs-lookup"><span data-stu-id="cc708-140">int2</span></span>           |
| <span data-ttu-id="cc708-141">Texture3D</span><span class="sxs-lookup"><span data-stu-id="cc708-141">Texture3D</span></span>                     | <span data-ttu-id="cc708-142">int3</span><span class="sxs-lookup"><span data-stu-id="cc708-142">int3</span></span>           |
| <span data-ttu-id="cc708-143">Texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="cc708-143">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="cc708-144">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cc708-144">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="cc708-145">*Klammer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cc708-145">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc708-146">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="cc708-146">Type: **float**</span></span>

<span data-ttu-id="cc708-147">Ein optionaler Wert zum Einspannen von Sample-Lod-Werten.</span><span class="sxs-lookup"><span data-stu-id="cc708-147">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="cc708-148">Wenn Sie beispielsweise 2.0 f als Klammer Wert übergeben, stellen Sie sicher, dass kein einzelnes Beispiel auf eine MIP-Ebene kleiner als 2.0 f zugreift.</span><span class="sxs-lookup"><span data-stu-id="cc708-148">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc708-149">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cc708-149">Return value</span></span>

<span data-ttu-id="cc708-150">Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="cc708-150">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="cc708-151">Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="cc708-151">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="cc708-152">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cc708-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc708-153">Samplecmp-Methoden</span><span class="sxs-lookup"><span data-stu-id="cc708-153">SampleCmp methods</span></span>](texture2d-samplecmp.md)
</dt> </dl>

 

 
