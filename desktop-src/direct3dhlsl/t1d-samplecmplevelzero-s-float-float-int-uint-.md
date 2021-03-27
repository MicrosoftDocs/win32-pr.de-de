---
title: 'Samplecmplevelzero:: samplecmplevelzero (S, float, float, int, uint)-Funktion für Texture1D'
description: Vergleicht nur eine Textur auf MipMap-Ebene 0 und vergleicht das Ergebnis mit einem Vergleichswert und gibt dann den Status des Vorgangs zurück. Für Texture1D.
ms.assetid: A2F7FD4A-49D8-41B3-A5AF-7B54A8B5266C
keywords:
- Samplecmplevelzero-Funktion HLSL
topic_type:
- apiref
api_name:
- SampleCmpLevelZero
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a63644cff0bcc5a437ff4ae3e1dffba8f5a0676c
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104219737"
---
# <a name="samplecmplevelzerosamplecmplevelzerosfloatfloatintuint-function-for-texture1d"></a><span data-ttu-id="3ca52-105">Samplecmplevelzero:: samplecmplevelzero (S, float, float, int, uint)-Funktion für Texture1D</span><span class="sxs-lookup"><span data-stu-id="3ca52-105">SampleCmpLevelZero::SampleCmpLevelZero(S,float,float,int,uint) function for Texture1D</span></span>

<span data-ttu-id="3ca52-106">Vergleicht nur eine Textur auf MipMap-Ebene 0 und vergleicht das Ergebnis mit einem Vergleichswert.</span><span class="sxs-lookup"><span data-stu-id="3ca52-106">Samples a texture on mipmap level 0 only and compares the result to a comparison value.</span></span> <span data-ttu-id="3ca52-107">Gibt den Status des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="3ca52-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ca52-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3ca52-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmpLevelZero(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="3ca52-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3ca52-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ca52-110">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ca52-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ca52-111">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="3ca52-111">Type: **SamplerState**</span></span>

<span data-ttu-id="3ca52-112">Ein [samplerzustand](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="3ca52-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="3ca52-113">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="3ca52-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="3ca52-114">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ca52-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ca52-115">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="3ca52-115">Type: **float**</span></span>

<span data-ttu-id="3ca52-116">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="3ca52-116">The texture coordinates.</span></span> <span data-ttu-id="3ca52-117">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="3ca52-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="3ca52-118">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="3ca52-118">Texture-Object Type</span></span>                    | <span data-ttu-id="3ca52-119">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="3ca52-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="3ca52-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3ca52-120">Texture1D</span></span>                              | <span data-ttu-id="3ca52-121">float</span><span class="sxs-lookup"><span data-stu-id="3ca52-121">float</span></span>          |
| <span data-ttu-id="3ca52-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="3ca52-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="3ca52-123">float2</span><span class="sxs-lookup"><span data-stu-id="3ca52-123">float2</span></span>         |
| <span data-ttu-id="3ca52-124">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="3ca52-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="3ca52-125">float3</span><span class="sxs-lookup"><span data-stu-id="3ca52-125">float3</span></span>         |
| <span data-ttu-id="3ca52-126">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="3ca52-126">TextureCubeArray</span></span>                       | <span data-ttu-id="3ca52-127">float4</span><span class="sxs-lookup"><span data-stu-id="3ca52-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="3ca52-128">*CompareValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ca52-128">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ca52-129">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="3ca52-129">Type: **float**</span></span>

<span data-ttu-id="3ca52-130">Ein Gleit Komma Wert, der als Vergleichswert verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3ca52-130">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="3ca52-131">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ca52-131">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ca52-132">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="3ca52-132">Type: **int**</span></span>

<span data-ttu-id="3ca52-133">Ein optionaler Offset der Textur Koordinate, der für jeden Textur Objekttyp verwendet werden kann. der Offset wird vor der Stichprobenentnahme auf den Speicherort angewendet.</span><span class="sxs-lookup"><span data-stu-id="3ca52-133">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="3ca52-134">Verwenden Sie einen Offset nur bei einer ganzzahligen miplevel. Andernfalls erhalten Sie möglicherweise Ergebnisse, die nicht gut in Hardware übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="3ca52-134">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="3ca52-135">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="3ca52-135">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="3ca52-136">Weitere Informationen finden Sie unter [Anwenden von ganzzahligen Offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="3ca52-136">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="3ca52-137">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="3ca52-137">Texture-Object Type</span></span>           | <span data-ttu-id="3ca52-138">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="3ca52-138">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="3ca52-139">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="3ca52-139">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="3ca52-140">INT</span><span class="sxs-lookup"><span data-stu-id="3ca52-140">int</span></span>            |
| <span data-ttu-id="3ca52-141">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="3ca52-141">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="3ca52-142">int2</span><span class="sxs-lookup"><span data-stu-id="3ca52-142">int2</span></span>           |
| <span data-ttu-id="3ca52-143">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3ca52-143">Texture3D</span></span>                     | <span data-ttu-id="3ca52-144">int3</span><span class="sxs-lookup"><span data-stu-id="3ca52-144">int3</span></span>           |
| <span data-ttu-id="3ca52-145">Texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="3ca52-145">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="3ca52-146">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="3ca52-146">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="3ca52-147">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3ca52-147">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ca52-148">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="3ca52-148">Type: **uint**</span></span>

<span data-ttu-id="3ca52-149">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="3ca52-149">The status of the operation.</span></span> <span data-ttu-id="3ca52-150">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="3ca52-150">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="3ca52-151">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="3ca52-151">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="3ca52-152">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="3ca52-152">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ca52-153">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3ca52-153">Return value</span></span>

<span data-ttu-id="3ca52-154">Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="3ca52-154">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="3ca52-155">Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="3ca52-155">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="3ca52-156">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3ca52-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ca52-157">Samplecmplevelzero-Methoden</span><span class="sxs-lookup"><span data-stu-id="3ca52-157">SampleCmpLevelZero methods</span></span>](texture1d-samplecmplevelzero.md)
</dt> </dl>

 

 
