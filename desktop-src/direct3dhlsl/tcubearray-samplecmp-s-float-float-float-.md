---
title: 'Samplecmp:: samplecmp (S, float, float, float)-Funktion für texturecubearray'
description: 'Verwendet einen Vergleichswert zum ablehnen von Beispielen, wobei ein optionaler Wert zum Einspannen von Samplingrate-Werten (LOD) an verwendet wird. | Samplecmp:: samplecmp (S, float, float, float)-Funktion für texturecubearray'
ms.assetid: A8824A82-A3FD-4FEE-BC10-56843997BBCE
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
ms.openlocfilehash: e65b1747d03b3a0555267f7b57e95a4d5aba54da
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982644"
---
# <a name="samplecmpsamplecmpsfloatfloatfloat-function-for-texturecubearray"></a><span data-ttu-id="53850-105">Samplecmp:: samplecmp (S, float, float, float)-Funktion für texturecubearray</span><span class="sxs-lookup"><span data-stu-id="53850-105">SampleCmp::SampleCmp(S,float,float,float) function for TextureCubeArray</span></span>

<span data-ttu-id="53850-106">Verwendet einen Vergleichswert zum ablehnen von Beispielen, wobei ein optionaler Wert zum Einspannen von Samplingrate-Werten (LOD) an verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="53850-106">Samples a texture, using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="53850-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="53850-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmp(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="53850-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="53850-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53850-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53850-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53850-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="53850-110">Type: **SamplerState**</span></span>

<span data-ttu-id="53850-111">Ein [samplerzustand](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="53850-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="53850-112">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="53850-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="53850-113">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53850-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53850-114">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="53850-114">Type: **float**</span></span>

<span data-ttu-id="53850-115">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="53850-115">The texture coordinates.</span></span> <span data-ttu-id="53850-116">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="53850-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="53850-117">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="53850-117">Texture-Object Type</span></span>                    | <span data-ttu-id="53850-118">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="53850-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="53850-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="53850-119">Texture1D</span></span>                              | <span data-ttu-id="53850-120">float</span><span class="sxs-lookup"><span data-stu-id="53850-120">float</span></span>          |
| <span data-ttu-id="53850-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="53850-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="53850-122">float2</span><span class="sxs-lookup"><span data-stu-id="53850-122">float2</span></span>         |
| <span data-ttu-id="53850-123">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="53850-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="53850-124">float3</span><span class="sxs-lookup"><span data-stu-id="53850-124">float3</span></span>         |
| <span data-ttu-id="53850-125">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="53850-125">TextureCubeArray</span></span>                       | <span data-ttu-id="53850-126">float4</span><span class="sxs-lookup"><span data-stu-id="53850-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="53850-127">*CompareValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53850-127">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53850-128">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="53850-128">Type: **float**</span></span>

<span data-ttu-id="53850-129">Ein Gleit Komma Wert, der als Vergleichswert verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="53850-129">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="53850-130">*Klammer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53850-130">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53850-131">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="53850-131">Type: **float**</span></span>

<span data-ttu-id="53850-132">Ein optionaler Wert zum Einspannen von Sample-Lod-Werten.</span><span class="sxs-lookup"><span data-stu-id="53850-132">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="53850-133">Wenn Sie beispielsweise 2.0 f als Klammer Wert übergeben, stellen Sie sicher, dass kein einzelnes Beispiel auf eine MIP-Ebene kleiner als 2.0 f zugreift.</span><span class="sxs-lookup"><span data-stu-id="53850-133">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53850-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="53850-134">Return value</span></span>

<span data-ttu-id="53850-135">Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="53850-135">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="53850-136">Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="53850-136">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="53850-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="53850-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53850-138">Samplecmp-Methoden</span><span class="sxs-lookup"><span data-stu-id="53850-138">SampleCmp methods</span></span>](texturecubearray-samplecmp.md)
</dt> <dt>

[<span data-ttu-id="53850-139">**Texturecubearray**</span><span class="sxs-lookup"><span data-stu-id="53850-139">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
