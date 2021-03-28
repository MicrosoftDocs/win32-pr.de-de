---
title: 'Texture2DArray:: gathercmpalpha (S, float, float, int2, int2, int2, int2)-Funktion'
description: 'Für vier textexwerte, die in einem bilinearen Filter Vorgang verwendet werden, wird ein Vergleich der Alpha Komponente mit einem Vergleichswert zurückgegeben. | Texture2DArray:: gathercmpalpha (S, float, float, int2, int2, int2, int2)-Funktion'
ms.assetid: 0D6EC888-AB90-47C8-87D1-7B25E3EEB436
keywords:
- Gathercmpalpha-Funktion HLSL
topic_type:
- apiref
api_name:
- GatherCmpAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e4fd93ed3925d9eaa27b369ffa44b2cc2ffde0f2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981601"
---
# <a name="texture2darraygathercmpalphasfloatfloatint2int2int2int2-function"></a><span data-ttu-id="97731-105">Texture2DArray:: gathercmpalpha (S, float, float, int2, int2, int2, int2)-Funktion</span><span class="sxs-lookup"><span data-stu-id="97731-105">Texture2DArray::GatherCmpAlpha(S,float,float,int2,int2,int2,int2) function</span></span>

<span data-ttu-id="97731-106">Für vier textexwerte, die in einem bilinearen Filter Vorgang verwendet werden, wird ein Vergleich der Alpha Komponente mit einem Vergleichswert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="97731-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="97731-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="97731-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpAlpha(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
  in int2         Offset1,
  in int2         Offset2,
  in int2         Offset3,
  in int2         Offset4
);
```



## <a name="parameters"></a><span data-ttu-id="97731-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="97731-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97731-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97731-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97731-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="97731-110">Type: **SamplerState**</span></span>

<span data-ttu-id="97731-111">Der null basierte samplerindex.</span><span class="sxs-lookup"><span data-stu-id="97731-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="97731-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97731-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97731-113">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="97731-113">Type: **float**</span></span>

<span data-ttu-id="97731-114">Die Beispiel Koordinaten (u, v).</span><span class="sxs-lookup"><span data-stu-id="97731-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="97731-115">*CompareValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97731-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97731-116">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="97731-116">Type: **float**</span></span>

<span data-ttu-id="97731-117">Ein Wert, der jeweils mit jedem Stichproben Wert verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="97731-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="97731-118">*Offset1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97731-118">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97731-119">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="97731-119">Type: **int2**</span></span>

<span data-ttu-id="97731-120">Die erste Offset-Komponente, die vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="97731-120">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="97731-121">*Offset2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97731-121">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97731-122">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="97731-122">Type: **int2**</span></span>

<span data-ttu-id="97731-123">Die zweite Offset Komponente, die vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="97731-123">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="97731-124">*Offset3* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97731-124">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97731-125">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="97731-125">Type: **int2**</span></span>

<span data-ttu-id="97731-126">Die dritte Offset Komponente, die vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="97731-126">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="97731-127">*Offset4* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97731-127">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97731-128">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="97731-128">Type: **int2**</span></span>

<span data-ttu-id="97731-129">Die vierte Offset-Komponente, die vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="97731-129">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97731-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="97731-130">Return value</span></span>

<span data-ttu-id="97731-131">Type: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="97731-131">Type: **TemplateType**</span></span>

<span data-ttu-id="97731-132">Ein vier komponentenwert, dessen Typ mit dem Vorlagentyp identisch ist.</span><span class="sxs-lookup"><span data-stu-id="97731-132">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="97731-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="97731-133">Remarks</span></span>

<span data-ttu-id="97731-134">Die Textur Beispiele können für bilineare Interpolationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="97731-134">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="97731-135">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="97731-135">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="97731-136">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="97731-136">Vertex</span></span> | <span data-ttu-id="97731-137">Hülle</span><span class="sxs-lookup"><span data-stu-id="97731-137">Hull</span></span> | <span data-ttu-id="97731-138">Domain</span><span class="sxs-lookup"><span data-stu-id="97731-138">Domain</span></span> | <span data-ttu-id="97731-139">Geometrie</span><span class="sxs-lookup"><span data-stu-id="97731-139">Geometry</span></span> | <span data-ttu-id="97731-140">Pixel</span><span class="sxs-lookup"><span data-stu-id="97731-140">Pixel</span></span> | <span data-ttu-id="97731-141">Compute</span><span class="sxs-lookup"><span data-stu-id="97731-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="97731-142">x</span><span class="sxs-lookup"><span data-stu-id="97731-142">x</span></span>      | <span data-ttu-id="97731-143">x</span><span class="sxs-lookup"><span data-stu-id="97731-143">x</span></span>    | <span data-ttu-id="97731-144">x</span><span class="sxs-lookup"><span data-stu-id="97731-144">x</span></span>      | <span data-ttu-id="97731-145">x</span><span class="sxs-lookup"><span data-stu-id="97731-145">x</span></span>        | <span data-ttu-id="97731-146">x</span><span class="sxs-lookup"><span data-stu-id="97731-146">x</span></span>     | <span data-ttu-id="97731-147">x</span><span class="sxs-lookup"><span data-stu-id="97731-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="97731-148">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="97731-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97731-149">Gathercmpalpha-Methoden</span><span class="sxs-lookup"><span data-stu-id="97731-149">GatherCmpAlpha methods</span></span>](texture2darray-gathercmpalpha.md)
</dt> </dl>

 

 




