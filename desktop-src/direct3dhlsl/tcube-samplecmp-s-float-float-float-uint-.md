---
title: 'Samplecmp:: samplecmp (S, float, float, float, uint)-Funktion für texturecube'
description: 'Diese Funktion prüft eine Textur mithilfe eines Vergleichs Werts, um Beispiele abzulehnen, mit einem optionalen Wert, mit dem Samplingrate-Werte (LOD-Werte) an eine Klammer mit einem optionalen Wert überstehen. | Samplecmp:: samplecmp (S, float, float, float, uint)-Funktion für texturecube'
ms.assetid: 050E2856-1E93-4C69-8213-EEC082E82D40
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
ms.openlocfilehash: b73bf86b0c24feae87ea0bb4150d313fff604002
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982660"
---
# <a name="samplecmpsamplecmpsfloatfloatfloatuint-function-for-texturecube"></a><span data-ttu-id="a60d1-105">Samplecmp:: samplecmp (S, float, float, float, uint)-Funktion für texturecube</span><span class="sxs-lookup"><span data-stu-id="a60d1-105">SampleCmp::SampleCmp(S,float,float,float,uint) function for TextureCube</span></span>

<span data-ttu-id="a60d1-106">Verwendet einen Vergleichswert zum ablehnen von Beispielen, wobei ein optionaler Wert zum Einspannen von Samplingrate-Werten (LOD) an verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a60d1-106">Samples a texture, using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="a60d1-107">Gibt den Status des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="a60d1-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="a60d1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a60d1-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmp(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="a60d1-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a60d1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a60d1-110">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a60d1-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a60d1-111">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="a60d1-111">Type: **SamplerState**</span></span>

<span data-ttu-id="a60d1-112">Ein [samplerzustand](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="a60d1-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="a60d1-113">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="a60d1-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="a60d1-114">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a60d1-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a60d1-115">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="a60d1-115">Type: **float**</span></span>

<span data-ttu-id="a60d1-116">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="a60d1-116">The texture coordinates.</span></span> <span data-ttu-id="a60d1-117">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="a60d1-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="a60d1-118">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="a60d1-118">Texture-Object Type</span></span>                    | <span data-ttu-id="a60d1-119">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="a60d1-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="a60d1-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a60d1-120">Texture1D</span></span>                              | <span data-ttu-id="a60d1-121">float</span><span class="sxs-lookup"><span data-stu-id="a60d1-121">float</span></span>          |
| <span data-ttu-id="a60d1-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="a60d1-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="a60d1-123">float2</span><span class="sxs-lookup"><span data-stu-id="a60d1-123">float2</span></span>         |
| <span data-ttu-id="a60d1-124">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="a60d1-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="a60d1-125">float3</span><span class="sxs-lookup"><span data-stu-id="a60d1-125">float3</span></span>         |
| <span data-ttu-id="a60d1-126">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="a60d1-126">TextureCubeArray</span></span>                       | <span data-ttu-id="a60d1-127">float4</span><span class="sxs-lookup"><span data-stu-id="a60d1-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="a60d1-128">*CompareValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a60d1-128">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a60d1-129">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="a60d1-129">Type: **float**</span></span>

<span data-ttu-id="a60d1-130">Ein Gleit Komma Wert, der als Vergleichswert verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a60d1-130">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="a60d1-131">*Klammer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a60d1-131">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a60d1-132">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="a60d1-132">Type: **float**</span></span>

<span data-ttu-id="a60d1-133">Ein optionaler Wert zum Einspannen von Sample-Lod-Werten.</span><span class="sxs-lookup"><span data-stu-id="a60d1-133">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="a60d1-134">Wenn Sie beispielsweise 2.0 f als Klammer Wert übergeben, stellen Sie sicher, dass kein einzelnes Beispiel auf eine MIP-Ebene kleiner als 2.0 f zugreift.</span><span class="sxs-lookup"><span data-stu-id="a60d1-134">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="a60d1-135">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a60d1-135">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a60d1-136">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="a60d1-136">Type: **uint**</span></span>

<span data-ttu-id="a60d1-137">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="a60d1-137">The status of the operation.</span></span> <span data-ttu-id="a60d1-138">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="a60d1-138">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="a60d1-139">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="a60d1-139">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="a60d1-140">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="a60d1-140">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a60d1-141">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a60d1-141">Return value</span></span>

<span data-ttu-id="a60d1-142">Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="a60d1-142">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="a60d1-143">Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="a60d1-143">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="a60d1-144">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a60d1-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a60d1-145">Samplecmp-Methoden</span><span class="sxs-lookup"><span data-stu-id="a60d1-145">SampleCmp methods</span></span>](texturecube-samplecmp.md)
</dt> <dt>

[<span data-ttu-id="a60d1-146">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="a60d1-146">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
