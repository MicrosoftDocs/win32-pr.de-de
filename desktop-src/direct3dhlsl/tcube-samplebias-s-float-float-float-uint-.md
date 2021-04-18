---
title: 'Samplebias:: samplebias (S, float, float, float, uint)-Funktion für texturecube'
description: 'Die samplebias:: samplebias (S, float, float, float, uint)-Funktion für texturecube gibt eine Textur aus, nachdem der Bias-Wert auf die MipMap-Ebene angewendet wurde.'
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
ms.openlocfilehash: 116749acdc23bb8ac2fd057139bf8ef7c8f5ddcc
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "106368704"
---
# <a name="samplebiassamplebiassfloatfloatfloatuint-function-for-texturecube"></a><span data-ttu-id="5680d-104">Samplebias:: samplebias (S, float, float, float, uint)-Funktion für texturecube</span><span class="sxs-lookup"><span data-stu-id="5680d-104">SampleBias::SampleBias(S,float,float,float,uint) function for TextureCube</span></span>

<span data-ttu-id="5680d-105">Gibt eine Textur aus, nachdem der Wert "Bias" auf die MipMap-Ebene angewendet wurde, mit einem optionalen Wert, mit dem Sample Level-of-Detail-Werte (LOD) an eine Klammer übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="5680d-105">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="5680d-106">Gibt den Status des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="5680d-106">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="5680d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5680d-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in  SamplerState S,
  in  float        Location,
  in  float        Bias,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="5680d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5680d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5680d-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5680d-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5680d-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="5680d-110">Type: **SamplerState**</span></span>

<span data-ttu-id="5680d-111">Ein [samplerzustand](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="5680d-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="5680d-112">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="5680d-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="5680d-113">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5680d-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5680d-114">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="5680d-114">Type: **float**</span></span>

<span data-ttu-id="5680d-115">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="5680d-115">The texture coordinates.</span></span> <span data-ttu-id="5680d-116">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="5680d-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="5680d-117">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="5680d-117">Texture-Object Type</span></span>                    | <span data-ttu-id="5680d-118">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="5680d-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="5680d-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5680d-119">Texture1D</span></span>                              | <span data-ttu-id="5680d-120">float</span><span class="sxs-lookup"><span data-stu-id="5680d-120">float</span></span>          |
| <span data-ttu-id="5680d-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="5680d-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="5680d-122">float2</span><span class="sxs-lookup"><span data-stu-id="5680d-122">float2</span></span>         |
| <span data-ttu-id="5680d-123">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="5680d-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="5680d-124">float3</span><span class="sxs-lookup"><span data-stu-id="5680d-124">float3</span></span>         |
| <span data-ttu-id="5680d-125">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="5680d-125">TextureCubeArray</span></span>                       | <span data-ttu-id="5680d-126">float4</span><span class="sxs-lookup"><span data-stu-id="5680d-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="5680d-127">*Bias* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5680d-127">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5680d-128">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="5680d-128">Type: **float**</span></span>

<span data-ttu-id="5680d-129">Der Bias-Wert, bei dem es sich um eine Gleit Komma Zahl zwischen 0,0 und 1,0 handelt, wird vor der Stichprobenentnahme auf eine MIP-Ebene angewendet.</span><span class="sxs-lookup"><span data-stu-id="5680d-129">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="5680d-130">*Klammer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5680d-130">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5680d-131">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="5680d-131">Type: **float**</span></span>

<span data-ttu-id="5680d-132">Ein optionaler Wert zum Einspannen von Sample-Lod-Werten.</span><span class="sxs-lookup"><span data-stu-id="5680d-132">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="5680d-133">Wenn Sie beispielsweise 2.0 f als Klammer Wert übergeben, stellen Sie sicher, dass kein einzelnes Beispiel auf eine MIP-Ebene kleiner als 2.0 f zugreift.</span><span class="sxs-lookup"><span data-stu-id="5680d-133">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="5680d-134">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5680d-134">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5680d-135">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="5680d-135">Type: **uint**</span></span>

<span data-ttu-id="5680d-136">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="5680d-136">The status of the operation.</span></span> <span data-ttu-id="5680d-137">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="5680d-137">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="5680d-138">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="5680d-138">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="5680d-139">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="5680d-139">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5680d-140">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5680d-140">Return value</span></span>

<span data-ttu-id="5680d-141">Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="5680d-141">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="5680d-142">Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="5680d-142">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="5680d-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5680d-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5680d-144">Samplebias-Methoden</span><span class="sxs-lookup"><span data-stu-id="5680d-144">SampleBias methods</span></span>](texturecube-samplebias.md)
</dt> <dt>

[<span data-ttu-id="5680d-145">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="5680d-145">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
