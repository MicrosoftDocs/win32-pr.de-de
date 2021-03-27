---
title: 'Texturecubearray:: Sample (S, float, float, uint)-Funktion'
description: 'Führt eine Stichprobe für eine Textur mit einem optionalen Wert aus, um die Samplingrate-Werte (LOD) zu binden, und gibt den Status des Vorgangs zurück. | Texturecubearray:: Sample (S, float, float, uint)-Funktion'
ms.assetid: 5645841D-A32E-452E-873C-E070CF6A4C00
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
ms.openlocfilehash: 24e6d77698507f0d1673b66954db8e78466ac728
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761703"
---
# <a name="texturecubearraysamplesfloatfloatuint-function"></a><span data-ttu-id="1dda1-105">Texturecubearray:: Sample (S, float, float, uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="1dda1-105">TextureCubeArray::Sample(S,float,float,uint) function</span></span>

<span data-ttu-id="1dda1-106">Führt eine Stichprobe für eine Textur mit einem optionalen Wert aus, um die Samplingrate-Werte (LOD) zu binden, und gibt den Status des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="1dda1-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to, and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dda1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1dda1-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float        Location,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="1dda1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1dda1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1dda1-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1dda1-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1dda1-110">Ein [samplerzustand](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="1dda1-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="1dda1-111">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="1dda1-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="1dda1-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1dda1-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1dda1-113">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="1dda1-113">The texture coordinates.</span></span> <span data-ttu-id="1dda1-114">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="1dda1-114">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="1dda1-115">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="1dda1-115">Texture-Object Type</span></span>                    | <span data-ttu-id="1dda1-116">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="1dda1-116">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="1dda1-117">Texture1D</span><span class="sxs-lookup"><span data-stu-id="1dda1-117">Texture1D</span></span>                              | <span data-ttu-id="1dda1-118">float</span><span class="sxs-lookup"><span data-stu-id="1dda1-118">float</span></span>          |
| <span data-ttu-id="1dda1-119">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="1dda1-119">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="1dda1-120">float2</span><span class="sxs-lookup"><span data-stu-id="1dda1-120">float2</span></span>         |
| <span data-ttu-id="1dda1-121">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="1dda1-121">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="1dda1-122">float3</span><span class="sxs-lookup"><span data-stu-id="1dda1-122">float3</span></span>         |
| <span data-ttu-id="1dda1-123">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="1dda1-123">TextureCubeArray</span></span>                       | <span data-ttu-id="1dda1-124">float4</span><span class="sxs-lookup"><span data-stu-id="1dda1-124">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="1dda1-125">*Klammer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1dda1-125">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1dda1-126">Ein optionaler Wert zum Einspannen von Sample-Lod-Werten.</span><span class="sxs-lookup"><span data-stu-id="1dda1-126">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="1dda1-127">Wenn Sie beispielsweise 2.0 f als Klammer Wert übergeben, stellen Sie sicher, dass kein einzelnes Beispiel auf eine MIP-Ebene kleiner als 2.0 f zugreift.</span><span class="sxs-lookup"><span data-stu-id="1dda1-127">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="1dda1-128">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1dda1-128">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1dda1-129">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="1dda1-129">The status of the operation.</span></span> <span data-ttu-id="1dda1-130">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="1dda1-130">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="1dda1-131">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="1dda1-131">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="1dda1-132">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="1dda1-132">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1dda1-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1dda1-133">Return value</span></span>

<span data-ttu-id="1dda1-134">Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="1dda1-134">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="1dda1-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1dda1-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dda1-136">Beispiel Methoden</span><span class="sxs-lookup"><span data-stu-id="1dda1-136">Sample methods</span></span>](texturecubearray-sample.md)
</dt> <dt>

[<span data-ttu-id="1dda1-137">**Texturecubearray**</span><span class="sxs-lookup"><span data-stu-id="1dda1-137">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
