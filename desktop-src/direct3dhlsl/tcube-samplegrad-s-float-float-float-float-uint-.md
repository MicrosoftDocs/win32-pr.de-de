---
title: 'Samplegrad:: samplegrad (S, float, float, float, float, uint)-Funktion für texturecube'
description: Verwendet einen Farbverlauf, um die Art und Weise zu beeinflussen, wie der Beispiel Speicherort berechnet wird, mit einem optionalen Wert, mit dem Samplingrate-Werte (LOD-Werte) fixiert werden. Für texturecube.
ms.assetid: 36DF7846-416A-4F2F-A7F8-44EE768CDEE1
keywords:
- Samplegrad-Funktion HLSL
topic_type:
- apiref
api_name:
- SampleGrad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3e75bccaeac28aefc50620a5dea31fa62b880332
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104531094"
---
# <a name="samplegradsamplegradsfloatfloatfloatfloatuint-function-for-texturecube"></a><span data-ttu-id="66a91-105">Samplegrad:: samplegrad (S, float, float, float, float, uint)-Funktion für texturecube</span><span class="sxs-lookup"><span data-stu-id="66a91-105">SampleGrad::SampleGrad(S,float,float,float,float,uint) function for TextureCube</span></span>

<span data-ttu-id="66a91-106">Verwendet einen Farbverlauf, um die Art und Weise zu beeinflussen, wie der Beispiel Speicherort berechnet wird, mit einem optionalen Wert, mit dem Samplingrate-Werte (LOD-Werte) fixiert werden.</span><span class="sxs-lookup"><span data-stu-id="66a91-106">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="66a91-107">Gibt den Status des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="66a91-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="66a91-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="66a91-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleGrad(
  in  SamplerState S,
  in  float        Location,
  in  float        DDX,
  in  float        DDY,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="66a91-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="66a91-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66a91-110">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="66a91-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66a91-111">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="66a91-111">Type: **SamplerState**</span></span>

<span data-ttu-id="66a91-112">Ein [samplerzustand](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="66a91-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="66a91-113">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="66a91-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="66a91-114">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="66a91-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66a91-115">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="66a91-115">Type: **float**</span></span>

<span data-ttu-id="66a91-116">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="66a91-116">The texture coordinates.</span></span> <span data-ttu-id="66a91-117">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="66a91-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="66a91-118">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="66a91-118">Texture-Object Type</span></span>                    | <span data-ttu-id="66a91-119">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="66a91-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="66a91-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="66a91-120">Texture1D</span></span>                              | <span data-ttu-id="66a91-121">float</span><span class="sxs-lookup"><span data-stu-id="66a91-121">float</span></span>          |
| <span data-ttu-id="66a91-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="66a91-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="66a91-123">float2</span><span class="sxs-lookup"><span data-stu-id="66a91-123">float2</span></span>         |
| <span data-ttu-id="66a91-124">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="66a91-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="66a91-125">float3</span><span class="sxs-lookup"><span data-stu-id="66a91-125">float3</span></span>         |
| <span data-ttu-id="66a91-126">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="66a91-126">TextureCubeArray</span></span>                       | <span data-ttu-id="66a91-127">float4</span><span class="sxs-lookup"><span data-stu-id="66a91-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="66a91-128">*DDX* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="66a91-128">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66a91-129">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="66a91-129">Type: **float**</span></span>

<span data-ttu-id="66a91-130">Die Änderungs Rate der Oberflächengeometrie in der x-Richtung.</span><span class="sxs-lookup"><span data-stu-id="66a91-130">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="66a91-131">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="66a91-131">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="66a91-132">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="66a91-132">Texture-Object Type</span></span>                      | <span data-ttu-id="66a91-133">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="66a91-133">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="66a91-134">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="66a91-134">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="66a91-135">float</span><span class="sxs-lookup"><span data-stu-id="66a91-135">float</span></span>          |
| <span data-ttu-id="66a91-136">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="66a91-136">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="66a91-137">float2</span><span class="sxs-lookup"><span data-stu-id="66a91-137">float2</span></span>         |
| <span data-ttu-id="66a91-138">Texture3D, texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="66a91-138">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="66a91-139">float3</span><span class="sxs-lookup"><span data-stu-id="66a91-139">float3</span></span>         |
| <span data-ttu-id="66a91-140">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="66a91-140">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="66a91-141">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="66a91-141">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="66a91-142">Nicht mehr  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="66a91-142">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66a91-143">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="66a91-143">Type: **float**</span></span>

<span data-ttu-id="66a91-144">Die Änderungs Rate der Oberflächengeometrie in der y-Richtung.</span><span class="sxs-lookup"><span data-stu-id="66a91-144">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="66a91-145">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="66a91-145">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="66a91-146">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="66a91-146">Texture-Object Type</span></span>                      | <span data-ttu-id="66a91-147">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="66a91-147">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="66a91-148">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="66a91-148">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="66a91-149">float</span><span class="sxs-lookup"><span data-stu-id="66a91-149">float</span></span>          |
| <span data-ttu-id="66a91-150">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="66a91-150">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="66a91-151">float2</span><span class="sxs-lookup"><span data-stu-id="66a91-151">float2</span></span>         |
| <span data-ttu-id="66a91-152">Texture3D, texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="66a91-152">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="66a91-153">float3</span><span class="sxs-lookup"><span data-stu-id="66a91-153">float3</span></span>         |
| <span data-ttu-id="66a91-154">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="66a91-154">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="66a91-155">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="66a91-155">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="66a91-156">*Klammer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="66a91-156">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66a91-157">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="66a91-157">Type: **float**</span></span>

<span data-ttu-id="66a91-158">Ein optionaler Wert zum Einspannen von Sample-Lod-Werten.</span><span class="sxs-lookup"><span data-stu-id="66a91-158">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="66a91-159">Wenn Sie beispielsweise 2.0 f als Klammer Wert übergeben, stellen Sie sicher, dass kein einzelnes Beispiel auf eine MIP-Ebene kleiner als 2.0 f zugreift.</span><span class="sxs-lookup"><span data-stu-id="66a91-159">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="66a91-160">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="66a91-160">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="66a91-161">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="66a91-161">Type: **uint**</span></span>

<span data-ttu-id="66a91-162">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="66a91-162">The status of the operation.</span></span> <span data-ttu-id="66a91-163">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="66a91-163">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="66a91-164">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="66a91-164">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="66a91-165">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="66a91-165">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66a91-166">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="66a91-166">Return value</span></span>

<span data-ttu-id="66a91-167">Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="66a91-167">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="66a91-168">Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="66a91-168">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="66a91-169">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="66a91-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66a91-170">Samplegrad-Methoden</span><span class="sxs-lookup"><span data-stu-id="66a91-170">SampleGrad methods</span></span>](texturecube-samplegrad.md)
</dt> <dt>

[<span data-ttu-id="66a91-171">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="66a91-171">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
