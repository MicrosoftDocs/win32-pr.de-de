---
title: 'Samplecmp:: samplecmp (S, float, float, float, uint)-Funktion für texturecubearray'
description: 'Verwendet einen Vergleichswert zum ablehnen von Beispielen, wobei ein optionaler Wert zum Einspannen von Samplingrate-Werten (LOD) an verwendet wird. | Samplecmp:: samplecmp (S, float, float, float, uint)-Funktion für texturecubearray'
ms.assetid: 5596D341-C057-414D-B1EC-7AA78693D32C
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
ms.openlocfilehash: 20626fe9d209ef4bfb64805f1a12561fd324f5a2
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104996354"
---
# <a name="samplecmpsamplecmpsfloatfloatfloatuint-function-for-texturecubearray"></a><span data-ttu-id="c5a9e-105">Samplecmp:: samplecmp (S, float, float, float, uint)-Funktion für texturecubearray</span><span class="sxs-lookup"><span data-stu-id="c5a9e-105">SampleCmp::SampleCmp(S,float,float,float,uint) function for TextureCubeArray</span></span>

<span data-ttu-id="c5a9e-106">Verwendet einen Vergleichswert zum ablehnen von Beispielen, wobei ein optionaler Wert zum Einspannen von Samplingrate-Werten (LOD) an verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c5a9e-106">Samples a texture, using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="c5a9e-107">Gibt den Status des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="c5a9e-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5a9e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5a9e-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmp(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="c5a9e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5a9e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5a9e-110">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5a9e-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5a9e-111">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="c5a9e-111">Type: **SamplerState**</span></span>

<span data-ttu-id="c5a9e-112">Ein [samplerzustand](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="c5a9e-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="c5a9e-113">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="c5a9e-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="c5a9e-114">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5a9e-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5a9e-115">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="c5a9e-115">Type: **float**</span></span>

<span data-ttu-id="c5a9e-116">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="c5a9e-116">The texture coordinates.</span></span> <span data-ttu-id="c5a9e-117">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="c5a9e-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="c5a9e-118">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="c5a9e-118">Texture-Object Type</span></span>                    | <span data-ttu-id="c5a9e-119">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="c5a9e-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="c5a9e-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="c5a9e-120">Texture1D</span></span>                              | <span data-ttu-id="c5a9e-121">float</span><span class="sxs-lookup"><span data-stu-id="c5a9e-121">float</span></span>          |
| <span data-ttu-id="c5a9e-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="c5a9e-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="c5a9e-123">float2</span><span class="sxs-lookup"><span data-stu-id="c5a9e-123">float2</span></span>         |
| <span data-ttu-id="c5a9e-124">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="c5a9e-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="c5a9e-125">float3</span><span class="sxs-lookup"><span data-stu-id="c5a9e-125">float3</span></span>         |
| <span data-ttu-id="c5a9e-126">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="c5a9e-126">TextureCubeArray</span></span>                       | <span data-ttu-id="c5a9e-127">float4</span><span class="sxs-lookup"><span data-stu-id="c5a9e-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="c5a9e-128">*CompareValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5a9e-128">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5a9e-129">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="c5a9e-129">Type: **float**</span></span>

<span data-ttu-id="c5a9e-130">Ein Gleit Komma Wert, der als Vergleichswert verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c5a9e-130">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="c5a9e-131">*Klammer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5a9e-131">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5a9e-132">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="c5a9e-132">Type: **float**</span></span>

<span data-ttu-id="c5a9e-133">Ein optionaler Wert zum Einspannen von Sample-Lod-Werten.</span><span class="sxs-lookup"><span data-stu-id="c5a9e-133">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="c5a9e-134">Wenn Sie beispielsweise 2.0 f als Klammer Wert übergeben, stellen Sie sicher, dass kein einzelnes Beispiel auf eine MIP-Ebene kleiner als 2.0 f zugreift.</span><span class="sxs-lookup"><span data-stu-id="c5a9e-134">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="c5a9e-135">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c5a9e-135">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5a9e-136">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="c5a9e-136">Type: **uint**</span></span>

<span data-ttu-id="c5a9e-137">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="c5a9e-137">The status of the operation.</span></span> <span data-ttu-id="c5a9e-138">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="c5a9e-138">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="c5a9e-139">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="c5a9e-139">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="c5a9e-140">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="c5a9e-140">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5a9e-141">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c5a9e-141">Return value</span></span>

<span data-ttu-id="c5a9e-142">Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="c5a9e-142">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="c5a9e-143">Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="c5a9e-143">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="c5a9e-144">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c5a9e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5a9e-145">Samplecmp-Methoden</span><span class="sxs-lookup"><span data-stu-id="c5a9e-145">SampleCmp methods</span></span>](texturecubearray-samplecmp.md)
</dt> <dt>

[<span data-ttu-id="c5a9e-146">**Texturecubearray**</span><span class="sxs-lookup"><span data-stu-id="c5a9e-146">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
