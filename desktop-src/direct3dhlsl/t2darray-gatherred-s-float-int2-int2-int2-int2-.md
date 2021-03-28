---
title: 'Texture2DArray:: gatherred (S, float, int2, int2, int2, int2)-Funktion'
description: 'Gibt die roten Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden. | Texture2DArray:: gatherred (S, float, int2, int2, int2, int2)-Funktion'
ms.assetid: EB367373-D798-4CBA-AEB6-8BF89371D765
keywords:
- Gatherrote Funktion HLSL
topic_type:
- apiref
api_name:
- GatherRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a080580c3735018c9e6459acd6b742ce45e933d3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103961294"
---
# <a name="texture2darraygatherredsfloatint2int2int2int2-function"></a><span data-ttu-id="220f3-105">Texture2DArray:: gatherred (S, float, int2, int2, int2, int2)-Funktion</span><span class="sxs-lookup"><span data-stu-id="220f3-105">Texture2DArray::GatherRed(S,float,int2,int2,int2,int2) function</span></span>

<span data-ttu-id="220f3-106">Gibt die roten Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="220f3-106">Returns the red components of the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="220f3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="220f3-107">Syntax</span></span>


``` syntax
TemplateType GatherRed(
  in SamplerState S,
  in float        Location,
  in int2         Offset1,
  in int2         Offset2,
  in int2         Offset3,
  in int2         Offset4
);
```



## <a name="parameters"></a><span data-ttu-id="220f3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="220f3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="220f3-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="220f3-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="220f3-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="220f3-110">Type: **SamplerState**</span></span>

<span data-ttu-id="220f3-111">Der null basierte samplerindex.</span><span class="sxs-lookup"><span data-stu-id="220f3-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="220f3-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="220f3-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="220f3-113">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="220f3-113">Type: **float**</span></span>

<span data-ttu-id="220f3-114">Die Beispiel Koordinaten (u, v).</span><span class="sxs-lookup"><span data-stu-id="220f3-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="220f3-115">*Offset1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="220f3-115">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="220f3-116">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="220f3-116">Type: **int2**</span></span>

<span data-ttu-id="220f3-117">Die erste Offset-Komponente, die vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="220f3-117">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="220f3-118">*Offset2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="220f3-118">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="220f3-119">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="220f3-119">Type: **int2**</span></span>

<span data-ttu-id="220f3-120">Die zweite Offset Komponente, die vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="220f3-120">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="220f3-121">*Offset3* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="220f3-121">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="220f3-122">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="220f3-122">Type: **int2**</span></span>

<span data-ttu-id="220f3-123">Die dritte Offset Komponente, die vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="220f3-123">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="220f3-124">*Offset4* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="220f3-124">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="220f3-125">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="220f3-125">Type: **int2**</span></span>

<span data-ttu-id="220f3-126">Die vierte Offset-Komponente, die vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="220f3-126">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="220f3-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="220f3-127">Return value</span></span>

<span data-ttu-id="220f3-128">Type: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="220f3-128">Type: **TemplateType**</span></span>

<span data-ttu-id="220f3-129">Ein vier komponentenwert, dessen Typ mit dem Vorlagentyp identisch ist.</span><span class="sxs-lookup"><span data-stu-id="220f3-129">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="220f3-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="220f3-130">Remarks</span></span>

<span data-ttu-id="220f3-131">Die Textur Beispiele können für bilineare Interpolationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="220f3-131">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="220f3-132">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="220f3-132">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="220f3-133">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="220f3-133">Vertex</span></span> | <span data-ttu-id="220f3-134">Hülle</span><span class="sxs-lookup"><span data-stu-id="220f3-134">Hull</span></span> | <span data-ttu-id="220f3-135">Domain</span><span class="sxs-lookup"><span data-stu-id="220f3-135">Domain</span></span> | <span data-ttu-id="220f3-136">Geometrie</span><span class="sxs-lookup"><span data-stu-id="220f3-136">Geometry</span></span> | <span data-ttu-id="220f3-137">Pixel</span><span class="sxs-lookup"><span data-stu-id="220f3-137">Pixel</span></span> | <span data-ttu-id="220f3-138">Compute</span><span class="sxs-lookup"><span data-stu-id="220f3-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="220f3-139">x</span><span class="sxs-lookup"><span data-stu-id="220f3-139">x</span></span>      | <span data-ttu-id="220f3-140">x</span><span class="sxs-lookup"><span data-stu-id="220f3-140">x</span></span>    | <span data-ttu-id="220f3-141">x</span><span class="sxs-lookup"><span data-stu-id="220f3-141">x</span></span>      | <span data-ttu-id="220f3-142">x</span><span class="sxs-lookup"><span data-stu-id="220f3-142">x</span></span>        | <span data-ttu-id="220f3-143">x</span><span class="sxs-lookup"><span data-stu-id="220f3-143">x</span></span>     | <span data-ttu-id="220f3-144">x</span><span class="sxs-lookup"><span data-stu-id="220f3-144">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="220f3-145">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="220f3-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="220f3-146">Gatherred-Methoden</span><span class="sxs-lookup"><span data-stu-id="220f3-146">GatherRed methods</span></span>](texture2darray-gatherred.md)
</dt> </dl>

 

 




