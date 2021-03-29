---
title: 'Samplelevel:: samplelevel (S, float, float, int, uint)-Funktion für Texture2D'
description: Prüft eine Texture2D auf der angegebenen MipMap-Ebene und gibt den Status des Vorgangs zurück.
ms.assetid: B021D42E-9F63-4CCE-939B-F93D91F7CB80
keywords:
- Samplelevel-Funktion HLSL
topic_type:
- apiref
api_name:
- SampleLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1455454649e24bd984948a81837181a7bcdba11a
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104996410"
---
# <a name="samplelevelsamplelevelsfloatfloatintuint-function-for-texture2d"></a><span data-ttu-id="d6b09-104">Samplelevel:: samplelevel (S, float, float, int, uint)-Funktion für Texture2D</span><span class="sxs-lookup"><span data-stu-id="d6b09-104">SampleLevel::SampleLevel(S,float,float,int,uint) function for Texture2D</span></span>

<span data-ttu-id="d6b09-105">Prüft eine [**Texture2D**](sm5-object-texture2d.md) auf der angegebenen MipMap-Ebene und gibt den Status des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="d6b09-105">Samples a [**Texture2D**](sm5-object-texture2d.md) on the specified mipmap level and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6b09-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6b09-106">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleLevel(
  in  SamplerState S,
  in  float        Location,
  in  float        LOD,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="d6b09-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6b09-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6b09-108">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d6b09-108">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6b09-109">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="d6b09-109">Type: **SamplerState**</span></span>

<span data-ttu-id="d6b09-110">Ein [samplerzustand](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="d6b09-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="d6b09-111">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="d6b09-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="d6b09-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d6b09-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6b09-113">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="d6b09-113">Type: **float**</span></span>

<span data-ttu-id="d6b09-114">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="d6b09-114">The texture coordinates.</span></span> <span data-ttu-id="d6b09-115">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="d6b09-115">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="d6b09-116">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="d6b09-116">Texture-Object Type</span></span>                    | <span data-ttu-id="d6b09-117">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="d6b09-117">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="d6b09-118">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d6b09-118">Texture1D</span></span>                              | <span data-ttu-id="d6b09-119">float</span><span class="sxs-lookup"><span data-stu-id="d6b09-119">float</span></span>          |
| <span data-ttu-id="d6b09-120">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="d6b09-120">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="d6b09-121">float2</span><span class="sxs-lookup"><span data-stu-id="d6b09-121">float2</span></span>         |
| <span data-ttu-id="d6b09-122">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="d6b09-122">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="d6b09-123">float3</span><span class="sxs-lookup"><span data-stu-id="d6b09-123">float3</span></span>         |
| <span data-ttu-id="d6b09-124">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="d6b09-124">TextureCubeArray</span></span>                       | <span data-ttu-id="d6b09-125">float4</span><span class="sxs-lookup"><span data-stu-id="d6b09-125">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="d6b09-126">*Lod* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d6b09-126">*LOD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6b09-127">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="d6b09-127">Type: **float**</span></span>

<span data-ttu-id="d6b09-128">\[in \] einer Zahl, die die MipMap-Ebene angibt.</span><span class="sxs-lookup"><span data-stu-id="d6b09-128">\[in\] A number that specifies the mipmap level.</span></span> <span data-ttu-id="d6b09-129">Wenn der Wert 0 (null) ist, wird MipMap Level 0 (größte Zuordnung) verwendet.</span><span class="sxs-lookup"><span data-stu-id="d6b09-129">If the value is ≤ 0, mipmap level 0 (biggest map) is used.</span></span> <span data-ttu-id="d6b09-130">Der Bruch Wert (falls angegeben) wird verwendet, um zwischen zwei MipMap-Ebenen zu interpolieren.</span><span class="sxs-lookup"><span data-stu-id="d6b09-130">The fractional value (if supplied) is used to interpolate between two mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="d6b09-131">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d6b09-131">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6b09-132">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="d6b09-132">Type: **int**</span></span>

<span data-ttu-id="d6b09-133">Ein optionaler Offset der Textur Koordinate, der für jeden Textur Objekttyp verwendet werden kann. der Offset wird vor der Stichprobenentnahme auf den Speicherort angewendet.</span><span class="sxs-lookup"><span data-stu-id="d6b09-133">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="d6b09-134">Verwenden Sie einen Offset nur bei einer ganzzahligen miplevel. Andernfalls erhalten Sie möglicherweise Ergebnisse, die nicht gut in Hardware übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="d6b09-134">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="d6b09-135">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="d6b09-135">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="d6b09-136">Weitere Informationen finden Sie unter [Anwenden von ganzzahligen Offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="d6b09-136">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="d6b09-137">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="d6b09-137">Texture-Object Type</span></span>           | <span data-ttu-id="d6b09-138">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="d6b09-138">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="d6b09-139">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="d6b09-139">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="d6b09-140">INT</span><span class="sxs-lookup"><span data-stu-id="d6b09-140">int</span></span>            |
| <span data-ttu-id="d6b09-141">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="d6b09-141">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="d6b09-142">int2</span><span class="sxs-lookup"><span data-stu-id="d6b09-142">int2</span></span>           |
| <span data-ttu-id="d6b09-143">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d6b09-143">Texture3D</span></span>                     | <span data-ttu-id="d6b09-144">int3</span><span class="sxs-lookup"><span data-stu-id="d6b09-144">int3</span></span>           |
| <span data-ttu-id="d6b09-145">Texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="d6b09-145">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="d6b09-146">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d6b09-146">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="d6b09-147">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d6b09-147">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6b09-148">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="d6b09-148">Type: **uint**</span></span>

<span data-ttu-id="d6b09-149">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="d6b09-149">The status of the operation.</span></span> <span data-ttu-id="d6b09-150">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="d6b09-150">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="d6b09-151">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="d6b09-151">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="d6b09-152">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="d6b09-152">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6b09-153">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d6b09-153">Return value</span></span>

<span data-ttu-id="d6b09-154">Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="d6b09-154">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="d6b09-155">Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="d6b09-155">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="d6b09-156">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d6b09-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6b09-157">Samplelevel-Methoden</span><span class="sxs-lookup"><span data-stu-id="d6b09-157">SampleLevel methods</span></span>](texture2d-samplelevel.md)
</dt> </dl>

 

 
