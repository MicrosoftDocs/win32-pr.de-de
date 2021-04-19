---
title: 'Samplebias:: samplebias (S, float, float, float)-Funktion für texturecubearray'
description: 'Die samplebias:: samplebias (S, float, float, float)-Funktion für texturecubearray gibt eine Textur aus, nachdem der Wert für den Wert auf MipMap-Ebene angewendet wurde.'
ms.assetid: 6683F115-4F81-4C24-B735-67DB4B52455B
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
ms.openlocfilehash: 0c57eec224ca92b2584ba7262488530ea7080939
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "106372032"
---
# <a name="samplebiassamplebiassfloatfloatfloat-function-for-texturecubearray"></a><span data-ttu-id="5b0bb-104">Samplebias:: samplebias (S, float, float, float)-Funktion für texturecubearray</span><span class="sxs-lookup"><span data-stu-id="5b0bb-104">SampleBias::SampleBias(S,float,float,float) function for TextureCubeArray</span></span>

<span data-ttu-id="5b0bb-105">Gibt eine Textur aus, nachdem der Wert "Bias" auf die MipMap-Ebene angewendet wurde, mit einem optionalen Wert, mit dem Sample Level-of-Detail-Werte (LOD) an eine Klammer übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="5b0bb-105">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b0bb-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b0bb-106">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="5b0bb-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b0bb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b0bb-108">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b0bb-108">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b0bb-109">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="5b0bb-109">Type: **SamplerState**</span></span>

<span data-ttu-id="5b0bb-110">Ein [samplerzustand](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="5b0bb-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="5b0bb-111">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="5b0bb-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="5b0bb-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b0bb-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b0bb-113">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="5b0bb-113">Type: **float**</span></span>

<span data-ttu-id="5b0bb-114">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="5b0bb-114">The texture coordinates.</span></span> <span data-ttu-id="5b0bb-115">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="5b0bb-115">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="5b0bb-116">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="5b0bb-116">Texture-Object Type</span></span>                    | <span data-ttu-id="5b0bb-117">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="5b0bb-117">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="5b0bb-118">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5b0bb-118">Texture1D</span></span>                              | <span data-ttu-id="5b0bb-119">float</span><span class="sxs-lookup"><span data-stu-id="5b0bb-119">float</span></span>          |
| <span data-ttu-id="5b0bb-120">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="5b0bb-120">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="5b0bb-121">float2</span><span class="sxs-lookup"><span data-stu-id="5b0bb-121">float2</span></span>         |
| <span data-ttu-id="5b0bb-122">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="5b0bb-122">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="5b0bb-123">float3</span><span class="sxs-lookup"><span data-stu-id="5b0bb-123">float3</span></span>         |
| <span data-ttu-id="5b0bb-124">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="5b0bb-124">TextureCubeArray</span></span>                       | <span data-ttu-id="5b0bb-125">float4</span><span class="sxs-lookup"><span data-stu-id="5b0bb-125">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="5b0bb-126">*Bias* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b0bb-126">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b0bb-127">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="5b0bb-127">Type: **float**</span></span>

<span data-ttu-id="5b0bb-128">Der Bias-Wert, bei dem es sich um eine Gleit Komma Zahl zwischen 0,0 und 1,0 handelt, wird vor der Stichprobenentnahme auf eine MIP-Ebene angewendet.</span><span class="sxs-lookup"><span data-stu-id="5b0bb-128">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="5b0bb-129">*Klammer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b0bb-129">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b0bb-130">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="5b0bb-130">Type: **float**</span></span>

<span data-ttu-id="5b0bb-131">Ein optionaler Wert zum Einspannen von Sample-Lod-Werten.</span><span class="sxs-lookup"><span data-stu-id="5b0bb-131">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="5b0bb-132">Wenn Sie beispielsweise 2.0 f als Klammer Wert übergeben, stellen Sie sicher, dass kein einzelnes Beispiel auf eine MIP-Ebene kleiner als 2.0 f zugreift.</span><span class="sxs-lookup"><span data-stu-id="5b0bb-132">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b0bb-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5b0bb-133">Return value</span></span>

<span data-ttu-id="5b0bb-134">Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="5b0bb-134">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="5b0bb-135">Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="5b0bb-135">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="5b0bb-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b0bb-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b0bb-137">Samplebias-Methoden</span><span class="sxs-lookup"><span data-stu-id="5b0bb-137">SampleBias methods</span></span>](texturecubearray-samplebias.md)
</dt> <dt>

[<span data-ttu-id="5b0bb-138">**Texturecubearray**</span><span class="sxs-lookup"><span data-stu-id="5b0bb-138">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
