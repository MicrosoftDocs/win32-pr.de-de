---
title: Gatherblue (S, float, int2, int2, int2, int2)-Funktion (HLSL-Referenz)
description: Gibt die blauen Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden. | Gatherblue (S, float, int2, int2, int2, int2)-Funktion (HLSL-Referenz)
ms.assetid: 0DDD3235-4F12-4D74-975A-F70A271C1FC0
keywords:
- Gatherblue-Funktion HLSL
topic_type:
- apiref
api_name:
- GatherBlue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a5676d9d6b25c6e67123c59dac14efa234386d4e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353539"
---
# <a name="gatherbluesfloatint2int2int2int2-function-hlsl-reference"></a><span data-ttu-id="d1168-105">Gatherblue (S, float, int2, int2, int2, int2)-Funktion (HLSL-Referenz)</span><span class="sxs-lookup"><span data-stu-id="d1168-105">GatherBlue(S,float,int2,int2,int2,int2) function (HLSL reference)</span></span>

<span data-ttu-id="d1168-106">Gibt die blauen Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d1168-106">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1168-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1168-107">Syntax</span></span>


``` syntax
TemplateType GatherBlue(
  in SamplerState S,
  in float        Location,
  in int2         Offset1,
  in int2         Offset2,
  in int2         Offset3,
  in int2         Offset4
);
```



## <a name="parameters"></a><span data-ttu-id="d1168-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1168-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1168-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d1168-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1168-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="d1168-110">Type: **SamplerState**</span></span>

<span data-ttu-id="d1168-111">Der null basierte samplerindex.</span><span class="sxs-lookup"><span data-stu-id="d1168-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="d1168-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d1168-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1168-113">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="d1168-113">Type: **float**</span></span>

<span data-ttu-id="d1168-114">Die Beispiel Koordinaten (u, v).</span><span class="sxs-lookup"><span data-stu-id="d1168-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="d1168-115">*Offset1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d1168-115">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1168-116">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="d1168-116">Type: **int2**</span></span>

<span data-ttu-id="d1168-117">Die erste Offset-Komponente, die vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="d1168-117">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="d1168-118">*Offset2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d1168-118">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1168-119">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="d1168-119">Type: **int2**</span></span>

<span data-ttu-id="d1168-120">Die zweite Offset Komponente, die vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="d1168-120">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="d1168-121">*Offset3* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d1168-121">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1168-122">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="d1168-122">Type: **int2**</span></span>

<span data-ttu-id="d1168-123">Die dritte Offset Komponente, die vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="d1168-123">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="d1168-124">*Offset4* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d1168-124">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1168-125">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="d1168-125">Type: **int2**</span></span>

<span data-ttu-id="d1168-126">Die vierte Offset-Komponente, die vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="d1168-126">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1168-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d1168-127">Return value</span></span>

<span data-ttu-id="d1168-128">Type: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="d1168-128">Type: **TemplateType**</span></span>

<span data-ttu-id="d1168-129">Ein vier komponentenwert, dessen Typ mit dem Vorlagentyp identisch ist.</span><span class="sxs-lookup"><span data-stu-id="d1168-129">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1168-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d1168-130">Remarks</span></span>

<span data-ttu-id="d1168-131">Die Textur Beispiele können für bilineare Interpolationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d1168-131">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="d1168-132">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="d1168-132">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="d1168-133">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="d1168-133">Vertex</span></span> | <span data-ttu-id="d1168-134">Hülle</span><span class="sxs-lookup"><span data-stu-id="d1168-134">Hull</span></span> | <span data-ttu-id="d1168-135">Domain</span><span class="sxs-lookup"><span data-stu-id="d1168-135">Domain</span></span> | <span data-ttu-id="d1168-136">Geometrie</span><span class="sxs-lookup"><span data-stu-id="d1168-136">Geometry</span></span> | <span data-ttu-id="d1168-137">Pixel</span><span class="sxs-lookup"><span data-stu-id="d1168-137">Pixel</span></span> | <span data-ttu-id="d1168-138">Compute</span><span class="sxs-lookup"><span data-stu-id="d1168-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="d1168-139">x</span><span class="sxs-lookup"><span data-stu-id="d1168-139">x</span></span>      | <span data-ttu-id="d1168-140">x</span><span class="sxs-lookup"><span data-stu-id="d1168-140">x</span></span>    | <span data-ttu-id="d1168-141">x</span><span class="sxs-lookup"><span data-stu-id="d1168-141">x</span></span>      | <span data-ttu-id="d1168-142">x</span><span class="sxs-lookup"><span data-stu-id="d1168-142">x</span></span>        | <span data-ttu-id="d1168-143">x</span><span class="sxs-lookup"><span data-stu-id="d1168-143">x</span></span>     | <span data-ttu-id="d1168-144">x</span><span class="sxs-lookup"><span data-stu-id="d1168-144">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="d1168-145">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d1168-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1168-146">Gatherblue-Methoden</span><span class="sxs-lookup"><span data-stu-id="d1168-146">GatherBlue methods</span></span>](texture2darray-gatherblue.md)
</dt> </dl>

 

 




