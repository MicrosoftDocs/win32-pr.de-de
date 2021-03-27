---
title: 'Samplebias:: samplebias (S, float, float, float, uint)-Funktion'
description: 'Gibt eine Textur aus, nachdem der Wert "Bias" auf die MipMap-Ebene angewendet wurde, mit einem optionalen Wert, mit dem Sample Level-of-Detail-Werte (LOD) an eine Klammer übergeben werden. Gibt den Status des Vorgangs zurück. | Samplebias:: samplebias (S, float, float, float, uint)-Funktion'
ms.assetid: A2F10B9B-5DF2-4389-83A9-F6A29781BF0A
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
ms.openlocfilehash: 2f3a994d7b0f0c2d55ae3203db9f3205932c1a25
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219293"
---
# <a name="samplebiassamplebiassfloatfloatfloatuint-function"></a><span data-ttu-id="1a58c-106">Samplebias:: samplebias (S, float, float, float, uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="1a58c-106">SampleBias::SampleBias(S,float,float,float,uint) function</span></span>

<span data-ttu-id="1a58c-107">Gibt eine Textur aus, nachdem der Wert "Bias" auf die MipMap-Ebene angewendet wurde, mit einem optionalen Wert, mit dem Sample Level-of-Detail-Werte (LOD) an eine Klammer übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="1a58c-107">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="1a58c-108">Gibt den Status des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="1a58c-108">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a58c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a58c-109">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in  SamplerState S,
  in  float        Location,
  in  float        Bias,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="1a58c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a58c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a58c-111">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1a58c-111">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a58c-112">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="1a58c-112">Type: **SamplerState**</span></span>

<span data-ttu-id="1a58c-113">Ein [samplerzustand](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="1a58c-113">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="1a58c-114">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="1a58c-114">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="1a58c-115">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1a58c-115">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a58c-116">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="1a58c-116">Type: **float**</span></span>

<span data-ttu-id="1a58c-117">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="1a58c-117">The texture coordinates.</span></span> <span data-ttu-id="1a58c-118">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="1a58c-118">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="1a58c-119">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="1a58c-119">Texture-Object Type</span></span>                    | <span data-ttu-id="1a58c-120">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="1a58c-120">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="1a58c-121">Texture1D</span><span class="sxs-lookup"><span data-stu-id="1a58c-121">Texture1D</span></span>                              | <span data-ttu-id="1a58c-122">float</span><span class="sxs-lookup"><span data-stu-id="1a58c-122">float</span></span>          |
| <span data-ttu-id="1a58c-123">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="1a58c-123">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="1a58c-124">float2</span><span class="sxs-lookup"><span data-stu-id="1a58c-124">float2</span></span>         |
| <span data-ttu-id="1a58c-125">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="1a58c-125">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="1a58c-126">float3</span><span class="sxs-lookup"><span data-stu-id="1a58c-126">float3</span></span>         |
| <span data-ttu-id="1a58c-127">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="1a58c-127">TextureCubeArray</span></span>                       | <span data-ttu-id="1a58c-128">float4</span><span class="sxs-lookup"><span data-stu-id="1a58c-128">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="1a58c-129">*Bias* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1a58c-129">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a58c-130">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="1a58c-130">Type: **float**</span></span>

<span data-ttu-id="1a58c-131">Der Bias-Wert, bei dem es sich um eine Gleit Komma Zahl zwischen 0,0 und 1,0 handelt, wird vor der Stichprobenentnahme auf eine MIP-Ebene angewendet.</span><span class="sxs-lookup"><span data-stu-id="1a58c-131">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="1a58c-132">*Klammer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1a58c-132">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a58c-133">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="1a58c-133">Type: **float**</span></span>

<span data-ttu-id="1a58c-134">Ein optionaler Wert zum Einspannen von Sample-Lod-Werten.</span><span class="sxs-lookup"><span data-stu-id="1a58c-134">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="1a58c-135">Wenn Sie beispielsweise 2.0 f als Klammer Wert übergeben, stellen Sie sicher, dass kein einzelnes Beispiel auf eine MIP-Ebene kleiner als 2.0 f zugreift.</span><span class="sxs-lookup"><span data-stu-id="1a58c-135">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="1a58c-136">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1a58c-136">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a58c-137">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="1a58c-137">Type: **uint**</span></span>

<span data-ttu-id="1a58c-138">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="1a58c-138">The status of the operation.</span></span> <span data-ttu-id="1a58c-139">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="1a58c-139">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="1a58c-140">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="1a58c-140">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="1a58c-141">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="1a58c-141">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a58c-142">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1a58c-142">Return value</span></span>

<span data-ttu-id="1a58c-143">Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="1a58c-143">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="1a58c-144">Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="1a58c-144">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="1a58c-145">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1a58c-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a58c-146">Samplebias-Methoden</span><span class="sxs-lookup"><span data-stu-id="1a58c-146">SampleBias methods</span></span>](texturecube-samplebias.md)
</dt> <dt>

[<span data-ttu-id="1a58c-147">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="1a58c-147">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
