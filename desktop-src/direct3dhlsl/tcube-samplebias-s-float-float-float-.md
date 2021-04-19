---
title: 'Samplebias:: samplebias (S, float, float, float)-Funktion für texturecube'
description: 'Die samplebias:: samplebias (S, float, float, float)-Funktion für texturecube gibt eine Textur aus, nachdem der Bias-Wert auf die MipMap-Ebene angewendet wurde.'
ms.assetid: BCDDADD9-D8B0-47C9-A312-5E6AF9C3C07B
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
ms.openlocfilehash: 55404f2e32f45e5b19e7b0cd4c109a6d5a8bcc13
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "106370897"
---
# <a name="samplebiassamplebiassfloatfloatfloat-function-for-texturecube"></a><span data-ttu-id="3e460-104">Samplebias:: samplebias (S, float, float, float)-Funktion für texturecube</span><span class="sxs-lookup"><span data-stu-id="3e460-104">SampleBias::SampleBias(S,float,float,float) function for TextureCube</span></span>

<span data-ttu-id="3e460-105">Gibt eine Textur aus, nachdem der Wert "Bias" auf die MipMap-Ebene angewendet wurde, mit einem optionalen Wert, mit dem Sample Level-of-Detail-Werte (LOD) an eine Klammer übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="3e460-105">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e460-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e460-106">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="3e460-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e460-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e460-108">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3e460-108">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e460-109">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="3e460-109">Type: **SamplerState**</span></span>

<span data-ttu-id="3e460-110">Ein [samplerzustand](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="3e460-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="3e460-111">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="3e460-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="3e460-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3e460-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e460-113">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="3e460-113">Type: **float**</span></span>

<span data-ttu-id="3e460-114">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="3e460-114">The texture coordinates.</span></span> <span data-ttu-id="3e460-115">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="3e460-115">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="3e460-116">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="3e460-116">Texture-Object Type</span></span>                    | <span data-ttu-id="3e460-117">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="3e460-117">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="3e460-118">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3e460-118">Texture1D</span></span>                              | <span data-ttu-id="3e460-119">float</span><span class="sxs-lookup"><span data-stu-id="3e460-119">float</span></span>          |
| <span data-ttu-id="3e460-120">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="3e460-120">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="3e460-121">float2</span><span class="sxs-lookup"><span data-stu-id="3e460-121">float2</span></span>         |
| <span data-ttu-id="3e460-122">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="3e460-122">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="3e460-123">float3</span><span class="sxs-lookup"><span data-stu-id="3e460-123">float3</span></span>         |
| <span data-ttu-id="3e460-124">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="3e460-124">TextureCubeArray</span></span>                       | <span data-ttu-id="3e460-125">float4</span><span class="sxs-lookup"><span data-stu-id="3e460-125">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="3e460-126">*Bias* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3e460-126">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e460-127">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="3e460-127">Type: **float**</span></span>

<span data-ttu-id="3e460-128">Der Bias-Wert, bei dem es sich um eine Gleit Komma Zahl zwischen 0,0 und 1,0 handelt, wird vor der Stichprobenentnahme auf eine MIP-Ebene angewendet.</span><span class="sxs-lookup"><span data-stu-id="3e460-128">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="3e460-129">*Klammer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3e460-129">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e460-130">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="3e460-130">Type: **float**</span></span>

<span data-ttu-id="3e460-131">Ein optionaler Wert zum Einspannen von Sample-Lod-Werten.</span><span class="sxs-lookup"><span data-stu-id="3e460-131">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="3e460-132">Wenn Sie beispielsweise 2.0 f als Klammer Wert übergeben, stellen Sie sicher, dass kein einzelnes Beispiel auf eine MIP-Ebene kleiner als 2.0 f zugreift.</span><span class="sxs-lookup"><span data-stu-id="3e460-132">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e460-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3e460-133">Return value</span></span>

<span data-ttu-id="3e460-134">Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="3e460-134">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="3e460-135">Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="3e460-135">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="3e460-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e460-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e460-137">Samplebias-Methoden</span><span class="sxs-lookup"><span data-stu-id="3e460-137">SampleBias methods</span></span>](texturecube-samplebias.md)
</dt> <dt>

[<span data-ttu-id="3e460-138">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="3e460-138">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
