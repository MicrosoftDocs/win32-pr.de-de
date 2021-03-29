---
title: 'Texturecube:: Sample (S, float, float)-Funktion'
description: 'Gibt eine Textur mit einem optionalen Wert aus, mit dem die Werte der Sample-Ebene (LOD) an eine Klammer angezeigt werden. | Texturecube:: Sample (S, float, float)-Funktion'
ms.assetid: 7DB25135-46B5-48E2-91D0-A45D355179D6
keywords:
- Beispiel Funktion HLSL
topic_type:
- apiref
api_name:
- Sample
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2ce841eb68e426fc76032d45353f2b439f0f3e4b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219133"
---
# <a name="texturecubesamplesfloatfloat-function"></a><span data-ttu-id="33a7f-105">Texturecube:: Sample (S, float, float)-Funktion</span><span class="sxs-lookup"><span data-stu-id="33a7f-105">TextureCube::Sample(S,float,float) function</span></span>

<span data-ttu-id="33a7f-106">Gibt eine Textur mit einem optionalen Wert aus, mit dem die Werte der Sample-Ebene (LOD) an eine Klammer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="33a7f-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="33a7f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="33a7f-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in SamplerState S,
  in float        Location,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="33a7f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="33a7f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33a7f-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="33a7f-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33a7f-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="33a7f-110">Type: **SamplerState**</span></span>

<span data-ttu-id="33a7f-111">Ein [samplerzustand](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="33a7f-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="33a7f-112">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="33a7f-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="33a7f-113">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="33a7f-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33a7f-114">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="33a7f-114">Type: **float**</span></span>

<span data-ttu-id="33a7f-115">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="33a7f-115">The texture coordinates.</span></span> <span data-ttu-id="33a7f-116">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="33a7f-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="33a7f-117">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="33a7f-117">Texture-Object Type</span></span>                    | <span data-ttu-id="33a7f-118">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="33a7f-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="33a7f-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="33a7f-119">Texture1D</span></span>                              | <span data-ttu-id="33a7f-120">float</span><span class="sxs-lookup"><span data-stu-id="33a7f-120">float</span></span>          |
| <span data-ttu-id="33a7f-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="33a7f-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="33a7f-122">float2</span><span class="sxs-lookup"><span data-stu-id="33a7f-122">float2</span></span>         |
| <span data-ttu-id="33a7f-123">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="33a7f-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="33a7f-124">float3</span><span class="sxs-lookup"><span data-stu-id="33a7f-124">float3</span></span>         |
| <span data-ttu-id="33a7f-125">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="33a7f-125">TextureCubeArray</span></span>                       | <span data-ttu-id="33a7f-126">float4</span><span class="sxs-lookup"><span data-stu-id="33a7f-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="33a7f-127">*Klammer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="33a7f-127">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33a7f-128">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="33a7f-128">Type: **float**</span></span>

<span data-ttu-id="33a7f-129">Ein optionaler Wert zum Einspannen von Sample-Lod-Werten.</span><span class="sxs-lookup"><span data-stu-id="33a7f-129">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="33a7f-130">Wenn Sie beispielsweise 2.0 f als Klammer Wert übergeben, stellen Sie sicher, dass kein einzelnes Beispiel auf eine MIP-Ebene kleiner als 2.0 f zugreift.</span><span class="sxs-lookup"><span data-stu-id="33a7f-130">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33a7f-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="33a7f-131">Return value</span></span>

<span data-ttu-id="33a7f-132">Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="33a7f-132">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="33a7f-133">Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="33a7f-133">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="33a7f-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="33a7f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33a7f-135">Beispiel Methoden</span><span class="sxs-lookup"><span data-stu-id="33a7f-135">Sample methods</span></span>](texturecube-sample.md)
</dt> <dt>

[<span data-ttu-id="33a7f-136">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="33a7f-136">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
