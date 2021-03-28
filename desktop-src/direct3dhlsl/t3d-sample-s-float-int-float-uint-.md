---
title: 'Texture3D:: Sample (S, float, int, float, uint)-Funktion'
description: 'Führt eine Stichprobe für eine Textur mit einem optionalen Wert aus, um die Samplingrate-Werte (LOD) zu binden, und gibt den Status des Vorgangs zurück. | Texture3D:: Sample (S, float, int, float, uint)-Funktion'
ms.assetid: DB8401A1-1065-4616-BDDE-9ADB59B09C8B
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
ms.openlocfilehash: 1f1704a30ba689d50bc9c551ac6a43a4a38f90a9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995342"
---
# <a name="texture3dsamplesfloatintfloatuint-function"></a><span data-ttu-id="5091c-105">Texture3D:: Sample (S, float, int, float, uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="5091c-105">Texture3D::Sample(S,float,int,float,uint) function</span></span>

<span data-ttu-id="5091c-106">Führt eine Stichprobe für eine Textur mit einem optionalen Wert aus, um die Samplingrate-Werte (LOD) zu binden, und gibt den Status des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="5091c-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to, and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="5091c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5091c-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float        Location,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="5091c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5091c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5091c-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5091c-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5091c-110">Ein [samplerzustand](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="5091c-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="5091c-111">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="5091c-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="5091c-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5091c-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5091c-113">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="5091c-113">The texture coordinates.</span></span> <span data-ttu-id="5091c-114">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="5091c-114">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="5091c-115">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="5091c-115">Texture-Object Type</span></span>                    | <span data-ttu-id="5091c-116">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="5091c-116">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="5091c-117">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5091c-117">Texture1D</span></span>                              | <span data-ttu-id="5091c-118">float</span><span class="sxs-lookup"><span data-stu-id="5091c-118">float</span></span>          |
| <span data-ttu-id="5091c-119">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="5091c-119">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="5091c-120">float2</span><span class="sxs-lookup"><span data-stu-id="5091c-120">float2</span></span>         |
| <span data-ttu-id="5091c-121">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="5091c-121">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="5091c-122">float3</span><span class="sxs-lookup"><span data-stu-id="5091c-122">float3</span></span>         |
| <span data-ttu-id="5091c-123">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="5091c-123">TextureCubeArray</span></span>                       | <span data-ttu-id="5091c-124">float4</span><span class="sxs-lookup"><span data-stu-id="5091c-124">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="5091c-125">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5091c-125">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5091c-126">Ein optionaler Offset der Textur Koordinate, der für jeden Textur Objekttyp verwendet werden kann. der Offset wird vor der Stichprobenentnahme auf den Speicherort angewendet.</span><span class="sxs-lookup"><span data-stu-id="5091c-126">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="5091c-127">Verwenden Sie einen Offset nur bei einer ganzzahligen miplevel. Andernfalls erhalten Sie möglicherweise Ergebnisse, die nicht gut in Hardware übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="5091c-127">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="5091c-128">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="5091c-128">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="5091c-129">Weitere Informationen finden Sie unter [Anwenden von ganzzahligen Offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="5091c-129">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="5091c-130">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="5091c-130">Texture-Object Type</span></span>           | <span data-ttu-id="5091c-131">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="5091c-131">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="5091c-132">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="5091c-132">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="5091c-133">INT</span><span class="sxs-lookup"><span data-stu-id="5091c-133">int</span></span>            |
| <span data-ttu-id="5091c-134">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="5091c-134">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="5091c-135">int2</span><span class="sxs-lookup"><span data-stu-id="5091c-135">int2</span></span>           |
| <span data-ttu-id="5091c-136">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5091c-136">Texture3D</span></span>                     | <span data-ttu-id="5091c-137">int3</span><span class="sxs-lookup"><span data-stu-id="5091c-137">int3</span></span>           |
| <span data-ttu-id="5091c-138">Texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="5091c-138">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="5091c-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="5091c-139">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="5091c-140">*Klammer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5091c-140">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5091c-141">Ein optionaler Wert zum Einspannen von Sample-Lod-Werten.</span><span class="sxs-lookup"><span data-stu-id="5091c-141">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="5091c-142">Wenn Sie beispielsweise 2.0 f als Klammer Wert übergeben, stellen Sie sicher, dass kein einzelnes Beispiel auf eine MIP-Ebene kleiner als 2.0 f zugreift.</span><span class="sxs-lookup"><span data-stu-id="5091c-142">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="5091c-143">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5091c-143">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5091c-144">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="5091c-144">The status of the operation.</span></span> <span data-ttu-id="5091c-145">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="5091c-145">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="5091c-146">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="5091c-146">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="5091c-147">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="5091c-147">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5091c-148">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5091c-148">Return value</span></span>

<span data-ttu-id="5091c-149">Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="5091c-149">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="5091c-150">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5091c-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5091c-151">Beispiel Methoden</span><span class="sxs-lookup"><span data-stu-id="5091c-151">Sample methods</span></span>](texture3d-sample.md)
</dt> <dt>

[<span data-ttu-id="5091c-152">**Texture3D**</span><span class="sxs-lookup"><span data-stu-id="5091c-152">**Texture3D**</span></span>](sm5-object-texture3d.md)
</dt> </dl>

 

 
