---
title: 'Texture2D:: gathercmpalpha (S, float, float, int2, int2, int2, int2)-Funktion'
description: 'Für vier textexwerte, die in einem bilinearen Filter Vorgang verwendet werden, wird ein Vergleich der Alpha Komponente mit einem Vergleichswert zurückgegeben. | Texture2D:: gathercmpalpha (S, float, float, int2, int2, int2, int2)-Funktion'
ms.assetid: C8325626-F281-4D10-9299-0E5DA01BB1BD
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
ms.openlocfilehash: f5095fdb83814ab8c7d52add0fba05cbbf876678
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981849"
---
# <a name="texture2dgathercmpalphasfloatfloatint2int2int2int2-function"></a><span data-ttu-id="7fe18-105">Texture2D:: gathercmpalpha (S, float, float, int2, int2, int2, int2)-Funktion</span><span class="sxs-lookup"><span data-stu-id="7fe18-105">Texture2D::GatherCmpAlpha(S,float,float,int2,int2,int2,int2) function</span></span>

<span data-ttu-id="7fe18-106">Für vier textexwerte, die in einem bilinearen Filter Vorgang verwendet werden, wird ein Vergleich der Alpha Komponente mit einem Vergleichswert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7fe18-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fe18-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7fe18-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="7fe18-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7fe18-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fe18-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7fe18-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fe18-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="7fe18-110">Type: **SamplerState**</span></span>

<span data-ttu-id="7fe18-111">Der null basierte samplerindex.</span><span class="sxs-lookup"><span data-stu-id="7fe18-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="7fe18-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7fe18-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fe18-113">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="7fe18-113">Type: **float**</span></span>

<span data-ttu-id="7fe18-114">Die Beispiel Koordinaten (u, v).</span><span class="sxs-lookup"><span data-stu-id="7fe18-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="7fe18-115">*CompareValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7fe18-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fe18-116">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="7fe18-116">Type: **float**</span></span>

<span data-ttu-id="7fe18-117">Ein Wert, der jeweils mit jedem Stichproben Wert verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="7fe18-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="7fe18-118">*Offset1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7fe18-118">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fe18-119">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="7fe18-119">Type: **int2**</span></span>

<span data-ttu-id="7fe18-120">Die erste Offset-Komponente, die vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="7fe18-120">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="7fe18-121">*Offset2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7fe18-121">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fe18-122">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="7fe18-122">Type: **int2**</span></span>

<span data-ttu-id="7fe18-123">Die zweite Offset Komponente, die vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="7fe18-123">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="7fe18-124">*Offset3* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7fe18-124">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fe18-125">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="7fe18-125">Type: **int2**</span></span>

<span data-ttu-id="7fe18-126">Die dritte Offset Komponente, die vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="7fe18-126">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="7fe18-127">*Offset4* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7fe18-127">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fe18-128">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="7fe18-128">Type: **int2**</span></span>

<span data-ttu-id="7fe18-129">Die vierte Offset-Komponente, die vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="7fe18-129">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fe18-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7fe18-130">Return value</span></span>

<span data-ttu-id="7fe18-131">Type: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="7fe18-131">Type: **TemplateType**</span></span>

<span data-ttu-id="7fe18-132">Ein vier komponentenwert, dessen Typ mit dem Vorlagentyp identisch ist.</span><span class="sxs-lookup"><span data-stu-id="7fe18-132">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fe18-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7fe18-133">Remarks</span></span>

<span data-ttu-id="7fe18-134">Die Textur Beispiele können für bilineare Interpolationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7fe18-134">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="7fe18-135">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="7fe18-135">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="7fe18-136">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="7fe18-136">Vertex</span></span> | <span data-ttu-id="7fe18-137">Hülle</span><span class="sxs-lookup"><span data-stu-id="7fe18-137">Hull</span></span> | <span data-ttu-id="7fe18-138">Domain</span><span class="sxs-lookup"><span data-stu-id="7fe18-138">Domain</span></span> | <span data-ttu-id="7fe18-139">Geometrie</span><span class="sxs-lookup"><span data-stu-id="7fe18-139">Geometry</span></span> | <span data-ttu-id="7fe18-140">Pixel</span><span class="sxs-lookup"><span data-stu-id="7fe18-140">Pixel</span></span> | <span data-ttu-id="7fe18-141">Compute</span><span class="sxs-lookup"><span data-stu-id="7fe18-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="7fe18-142">x</span><span class="sxs-lookup"><span data-stu-id="7fe18-142">x</span></span>      | <span data-ttu-id="7fe18-143">x</span><span class="sxs-lookup"><span data-stu-id="7fe18-143">x</span></span>    | <span data-ttu-id="7fe18-144">x</span><span class="sxs-lookup"><span data-stu-id="7fe18-144">x</span></span>      | <span data-ttu-id="7fe18-145">x</span><span class="sxs-lookup"><span data-stu-id="7fe18-145">x</span></span>        | <span data-ttu-id="7fe18-146">x</span><span class="sxs-lookup"><span data-stu-id="7fe18-146">x</span></span>     | <span data-ttu-id="7fe18-147">x</span><span class="sxs-lookup"><span data-stu-id="7fe18-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="7fe18-148">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7fe18-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fe18-149">Gathercmpalpha-Methoden</span><span class="sxs-lookup"><span data-stu-id="7fe18-149">GatherCmpAlpha methods</span></span>](texture2d-gathercmpalpha.md)
</dt> </dl>

 

 




