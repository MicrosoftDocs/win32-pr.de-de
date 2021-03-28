---
title: 'Samplecmp:: samplecmp (S, float, float, float)-Funktion für texturecube'
description: 'Verwendet einen Vergleichswert zum ablehnen von Beispielen, wobei ein optionaler Wert zum Einspannen von Samplingrate-Werten (LOD) an verwendet wird. | Samplecmp:: samplecmp (S, float, float, float)-Funktion für texturecube'
ms.assetid: FCCF12CF-3F0A-4468-9FC4-27CAAF0BEEE3
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
ms.openlocfilehash: e8a326101df26ab7f4925c9c6cce3673385309fd
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982725"
---
# <a name="samplecmpsamplecmpsfloatfloatfloat-function-for-texturecube"></a><span data-ttu-id="6d45d-105">Samplecmp:: samplecmp (S, float, float, float)-Funktion für texturecube</span><span class="sxs-lookup"><span data-stu-id="6d45d-105">SampleCmp::SampleCmp(S,float,float,float) function for TextureCube</span></span>

<span data-ttu-id="6d45d-106">Verwendet einen Vergleichswert zum ablehnen von Beispielen, wobei ein optionaler Wert zum Einspannen von Samplingrate-Werten (LOD) an verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6d45d-106">Samples a texture, using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d45d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d45d-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmp(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="6d45d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6d45d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d45d-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6d45d-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d45d-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="6d45d-110">Type: **SamplerState**</span></span>

<span data-ttu-id="6d45d-111">Ein [samplerzustand](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="6d45d-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="6d45d-112">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="6d45d-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="6d45d-113">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6d45d-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d45d-114">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="6d45d-114">Type: **float**</span></span>

<span data-ttu-id="6d45d-115">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="6d45d-115">The texture coordinates.</span></span> <span data-ttu-id="6d45d-116">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="6d45d-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="6d45d-117">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="6d45d-117">Texture-Object Type</span></span>                    | <span data-ttu-id="6d45d-118">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="6d45d-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="6d45d-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6d45d-119">Texture1D</span></span>                              | <span data-ttu-id="6d45d-120">float</span><span class="sxs-lookup"><span data-stu-id="6d45d-120">float</span></span>          |
| <span data-ttu-id="6d45d-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="6d45d-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="6d45d-122">float2</span><span class="sxs-lookup"><span data-stu-id="6d45d-122">float2</span></span>         |
| <span data-ttu-id="6d45d-123">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="6d45d-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="6d45d-124">float3</span><span class="sxs-lookup"><span data-stu-id="6d45d-124">float3</span></span>         |
| <span data-ttu-id="6d45d-125">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="6d45d-125">TextureCubeArray</span></span>                       | <span data-ttu-id="6d45d-126">float4</span><span class="sxs-lookup"><span data-stu-id="6d45d-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="6d45d-127">*CompareValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6d45d-127">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d45d-128">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="6d45d-128">Type: **float**</span></span>

<span data-ttu-id="6d45d-129">Ein Gleit Komma Wert, der als Vergleichswert verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6d45d-129">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="6d45d-130">*Klammer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6d45d-130">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d45d-131">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="6d45d-131">Type: **float**</span></span>

<span data-ttu-id="6d45d-132">Ein optionaler Wert zum Einspannen von Sample-Lod-Werten.</span><span class="sxs-lookup"><span data-stu-id="6d45d-132">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="6d45d-133">Wenn Sie beispielsweise 2.0 f als Klammer Wert übergeben, stellen Sie sicher, dass kein einzelnes Beispiel auf eine MIP-Ebene kleiner als 2.0 f zugreift.</span><span class="sxs-lookup"><span data-stu-id="6d45d-133">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d45d-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6d45d-134">Return value</span></span>

<span data-ttu-id="6d45d-135">Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="6d45d-135">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="6d45d-136">Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="6d45d-136">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="6d45d-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6d45d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d45d-138">Samplecmp-Methoden</span><span class="sxs-lookup"><span data-stu-id="6d45d-138">SampleCmp methods</span></span>](texturecube-samplecmp.md)
</dt> <dt>

[<span data-ttu-id="6d45d-139">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="6d45d-139">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
