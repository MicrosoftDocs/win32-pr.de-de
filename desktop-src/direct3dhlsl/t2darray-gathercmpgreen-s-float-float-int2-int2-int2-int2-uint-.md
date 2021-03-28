---
title: 'Texture2DArray:: gathercmpgreen (S, float, float, int2, int2, int2, int2, uint)-Funktion'
description: 'Für vier Texel-Werte, die in einem bilinearen Filter Vorgang verwendet werden, gibt einen Vergleich der grünen Komponente mit einem Vergleichswert zusammen mit dem Status der Kachel Zuordnung zurück. | Texture2DArray:: gathercmpgreen (S, float, float, int2, int2, int2, int2, uint)-Funktion'
ms.assetid: 53AC1FE7-ECC8-489B-8FEF-5028009BC080
keywords:
- Gathercmpgreen-Funktion HLSL
topic_type:
- apiref
api_name:
- GatherCmpGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9878e5e9474717be9842887b2945591d5883cb07
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981981"
---
# <a name="texture2darraygathercmpgreensfloatfloatint2int2int2int2uint-function"></a><span data-ttu-id="ed203-105">Texture2DArray:: gathercmpgreen (S, float, float, int2, int2, int2, int2, uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="ed203-105">Texture2DArray::GatherCmpGreen(S,float,float,int2,int2,int2,int2,uint) function</span></span>

<span data-ttu-id="ed203-106">Für vier Texel-Werte, die in einem bilinearen Filter Vorgang verwendet werden, gibt einen Vergleich der grünen Komponente mit einem Vergleichswert zusammen mit dem Status der Kachel Zuordnung zurück.</span><span class="sxs-lookup"><span data-stu-id="ed203-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their green component against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed203-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed203-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpGreen(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int2         Offset1,
  in  int2         Offset2,
  in  int2         Offset3,
  in  int2         Offset4,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="ed203-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed203-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed203-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed203-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed203-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="ed203-110">Type: **SamplerState**</span></span>

<span data-ttu-id="ed203-111">Der null basierte samplerindex.</span><span class="sxs-lookup"><span data-stu-id="ed203-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="ed203-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed203-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed203-113">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="ed203-113">Type: **float**</span></span>

<span data-ttu-id="ed203-114">Die Beispiel Koordinaten (u, v).</span><span class="sxs-lookup"><span data-stu-id="ed203-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="ed203-115">*CompareValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed203-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed203-116">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="ed203-116">Type: **float**</span></span>

<span data-ttu-id="ed203-117">Ein Wert, der jeweils mit jedem Stichproben Wert verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ed203-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="ed203-118">*Offset1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed203-118">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed203-119">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="ed203-119">Type: **int2**</span></span>

<span data-ttu-id="ed203-120">Die erste Offset-Komponente, die vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="ed203-120">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="ed203-121">*Offset2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed203-121">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed203-122">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="ed203-122">Type: **int2**</span></span>

<span data-ttu-id="ed203-123">Die zweite Offset Komponente, die vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="ed203-123">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="ed203-124">*Offset3* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed203-124">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed203-125">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="ed203-125">Type: **int2**</span></span>

<span data-ttu-id="ed203-126">Die dritte Offset Komponente, die vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="ed203-126">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="ed203-127">*Offset4* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed203-127">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed203-128">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="ed203-128">Type: **int2**</span></span>

<span data-ttu-id="ed203-129">Die vierte Offset-Komponente, die vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="ed203-129">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="ed203-130">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ed203-130">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed203-131">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="ed203-131">Type: **uint**</span></span>

<span data-ttu-id="ed203-132">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="ed203-132">The status of the operation.</span></span> <span data-ttu-id="ed203-133">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="ed203-133">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="ed203-134">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="ed203-134">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="ed203-135">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="ed203-135">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed203-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ed203-136">Return value</span></span>

<span data-ttu-id="ed203-137">Type: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="ed203-137">Type: **TemplateType**</span></span>

<span data-ttu-id="ed203-138">Ein vier komponentenwert, dessen Typ mit dem Vorlagentyp identisch ist.</span><span class="sxs-lookup"><span data-stu-id="ed203-138">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed203-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ed203-139">Remarks</span></span>

<span data-ttu-id="ed203-140">Die Textur Beispiele können für bilineare Interpolationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ed203-140">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="ed203-141">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="ed203-141">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="ed203-142">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="ed203-142">Vertex</span></span> | <span data-ttu-id="ed203-143">Hülle</span><span class="sxs-lookup"><span data-stu-id="ed203-143">Hull</span></span> | <span data-ttu-id="ed203-144">Domain</span><span class="sxs-lookup"><span data-stu-id="ed203-144">Domain</span></span> | <span data-ttu-id="ed203-145">Geometrie</span><span class="sxs-lookup"><span data-stu-id="ed203-145">Geometry</span></span> | <span data-ttu-id="ed203-146">Pixel</span><span class="sxs-lookup"><span data-stu-id="ed203-146">Pixel</span></span> | <span data-ttu-id="ed203-147">Compute</span><span class="sxs-lookup"><span data-stu-id="ed203-147">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ed203-148">x</span><span class="sxs-lookup"><span data-stu-id="ed203-148">x</span></span>      | <span data-ttu-id="ed203-149">x</span><span class="sxs-lookup"><span data-stu-id="ed203-149">x</span></span>    | <span data-ttu-id="ed203-150">x</span><span class="sxs-lookup"><span data-stu-id="ed203-150">x</span></span>      | <span data-ttu-id="ed203-151">x</span><span class="sxs-lookup"><span data-stu-id="ed203-151">x</span></span>        | <span data-ttu-id="ed203-152">x</span><span class="sxs-lookup"><span data-stu-id="ed203-152">x</span></span>     | <span data-ttu-id="ed203-153">x</span><span class="sxs-lookup"><span data-stu-id="ed203-153">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ed203-154">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ed203-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed203-155">Gathercmpgreen-Methoden</span><span class="sxs-lookup"><span data-stu-id="ed203-155">GatherCmpGreen methods</span></span>](texture2darray-gathercmpgreen.md)
</dt> </dl>

 

 
