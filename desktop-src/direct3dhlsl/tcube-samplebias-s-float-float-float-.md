---
title: 'Samplebias:: samplebias (S, float, float, float)-Funktion'
description: 'Gibt eine Textur aus, nachdem der Wert "Bias" auf die MipMap-Ebene angewendet wurde, mit einem optionalen Wert, mit dem Sample Level-of-Detail-Werte (LOD) an eine Klammer übergeben werden. | Samplebias:: samplebias (S, float, float, float)-Funktion'
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
ms.openlocfilehash: ae1c14903748f53d9890ff1a4dd9bd806caececf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104050799"
---
# <a name="samplebiassamplebiassfloatfloatfloat-function"></a><span data-ttu-id="193fa-105">Samplebias:: samplebias (S, float, float, float)-Funktion</span><span class="sxs-lookup"><span data-stu-id="193fa-105">SampleBias::SampleBias(S,float,float,float) function</span></span>

<span data-ttu-id="193fa-106">Gibt eine Textur aus, nachdem der Wert "Bias" auf die MipMap-Ebene angewendet wurde, mit einem optionalen Wert, mit dem Sample Level-of-Detail-Werte (LOD) an eine Klammer übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="193fa-106">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="193fa-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="193fa-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="193fa-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="193fa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="193fa-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="193fa-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="193fa-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="193fa-110">Type: **SamplerState**</span></span>

<span data-ttu-id="193fa-111">Ein [samplerzustand](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="193fa-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="193fa-112">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="193fa-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="193fa-113">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="193fa-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="193fa-114">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="193fa-114">Type: **float**</span></span>

<span data-ttu-id="193fa-115">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="193fa-115">The texture coordinates.</span></span> <span data-ttu-id="193fa-116">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="193fa-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="193fa-117">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="193fa-117">Texture-Object Type</span></span>                    | <span data-ttu-id="193fa-118">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="193fa-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="193fa-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="193fa-119">Texture1D</span></span>                              | <span data-ttu-id="193fa-120">float</span><span class="sxs-lookup"><span data-stu-id="193fa-120">float</span></span>          |
| <span data-ttu-id="193fa-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="193fa-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="193fa-122">float2</span><span class="sxs-lookup"><span data-stu-id="193fa-122">float2</span></span>         |
| <span data-ttu-id="193fa-123">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="193fa-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="193fa-124">float3</span><span class="sxs-lookup"><span data-stu-id="193fa-124">float3</span></span>         |
| <span data-ttu-id="193fa-125">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="193fa-125">TextureCubeArray</span></span>                       | <span data-ttu-id="193fa-126">float4</span><span class="sxs-lookup"><span data-stu-id="193fa-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="193fa-127">*Bias* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="193fa-127">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="193fa-128">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="193fa-128">Type: **float**</span></span>

<span data-ttu-id="193fa-129">Der Bias-Wert, bei dem es sich um eine Gleit Komma Zahl zwischen 0,0 und 1,0 handelt, wird vor der Stichprobenentnahme auf eine MIP-Ebene angewendet.</span><span class="sxs-lookup"><span data-stu-id="193fa-129">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="193fa-130">*Klammer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="193fa-130">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="193fa-131">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="193fa-131">Type: **float**</span></span>

<span data-ttu-id="193fa-132">Ein optionaler Wert zum Einspannen von Sample-Lod-Werten.</span><span class="sxs-lookup"><span data-stu-id="193fa-132">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="193fa-133">Wenn Sie beispielsweise 2.0 f als Klammer Wert übergeben, stellen Sie sicher, dass kein einzelnes Beispiel auf eine MIP-Ebene kleiner als 2.0 f zugreift.</span><span class="sxs-lookup"><span data-stu-id="193fa-133">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="193fa-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="193fa-134">Return value</span></span>

<span data-ttu-id="193fa-135">Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="193fa-135">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="193fa-136">Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="193fa-136">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="193fa-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="193fa-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="193fa-138">Samplebias-Methoden</span><span class="sxs-lookup"><span data-stu-id="193fa-138">SampleBias methods</span></span>](texturecube-samplebias.md)
</dt> <dt>

[<span data-ttu-id="193fa-139">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="193fa-139">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
