---
title: 'Texture2DArray:: gathergreen (S, float, int2, int2, int2, int2)-Funktion'
description: 'Gibt die grünen Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden. | Texture2DArray:: gathergreen (S, float, int2, int2, int2, int2)-Funktion'
ms.assetid: 7E79442E-286F-4BDB-8D7A-2C20A0933585
keywords:
- Gathergreen-Funktion HLSL
topic_type:
- apiref
api_name:
- GatherGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 12e8649882c7e3c8fd4d9f88cd37d1a27952eb2b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103961489"
---
# <a name="texture2darraygathergreensfloatint2int2int2int2-function"></a><span data-ttu-id="e3eec-105">Texture2DArray:: gathergreen (S, float, int2, int2, int2, int2)-Funktion</span><span class="sxs-lookup"><span data-stu-id="e3eec-105">Texture2DArray::GatherGreen(S,float,int2,int2,int2,int2) function</span></span>

<span data-ttu-id="e3eec-106">Gibt die grünen Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e3eec-106">Returns the green components of the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3eec-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3eec-107">Syntax</span></span>


``` syntax
TemplateType GatherGreen(
  in SamplerState S,
  in float        Location,
  in int2         Offset1,
  in int2         Offset2,
  in int2         Offset3,
  in int2         Offset4
);
```



## <a name="parameters"></a><span data-ttu-id="e3eec-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3eec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3eec-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3eec-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3eec-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="e3eec-110">Type: **SamplerState**</span></span>

<span data-ttu-id="e3eec-111">Der null basierte samplerindex.</span><span class="sxs-lookup"><span data-stu-id="e3eec-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="e3eec-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3eec-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3eec-113">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="e3eec-113">Type: **float**</span></span>

<span data-ttu-id="e3eec-114">Die Beispiel Koordinaten (u, v).</span><span class="sxs-lookup"><span data-stu-id="e3eec-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="e3eec-115">*Offset1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3eec-115">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3eec-116">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="e3eec-116">Type: **int2**</span></span>

<span data-ttu-id="e3eec-117">Die erste Offset-Komponente, die vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="e3eec-117">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="e3eec-118">*Offset2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3eec-118">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3eec-119">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="e3eec-119">Type: **int2**</span></span>

<span data-ttu-id="e3eec-120">Die zweite Offset Komponente, die vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="e3eec-120">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="e3eec-121">*Offset3* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3eec-121">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3eec-122">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="e3eec-122">Type: **int2**</span></span>

<span data-ttu-id="e3eec-123">Die dritte Offset Komponente, die vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="e3eec-123">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="e3eec-124">*Offset4* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3eec-124">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3eec-125">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="e3eec-125">Type: **int2**</span></span>

<span data-ttu-id="e3eec-126">Die vierte Offset-Komponente, die vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="e3eec-126">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3eec-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e3eec-127">Return value</span></span>

<span data-ttu-id="e3eec-128">Type: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="e3eec-128">Type: **TemplateType**</span></span>

<span data-ttu-id="e3eec-129">Ein vier komponentenwert, dessen Typ mit dem Vorlagentyp identisch ist.</span><span class="sxs-lookup"><span data-stu-id="e3eec-129">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3eec-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e3eec-130">Remarks</span></span>

<span data-ttu-id="e3eec-131">Die Textur Beispiele können für bilineare Interpolationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e3eec-131">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="e3eec-132">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="e3eec-132">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="e3eec-133">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="e3eec-133">Vertex</span></span> | <span data-ttu-id="e3eec-134">Hülle</span><span class="sxs-lookup"><span data-stu-id="e3eec-134">Hull</span></span> | <span data-ttu-id="e3eec-135">Domain</span><span class="sxs-lookup"><span data-stu-id="e3eec-135">Domain</span></span> | <span data-ttu-id="e3eec-136">Geometrie</span><span class="sxs-lookup"><span data-stu-id="e3eec-136">Geometry</span></span> | <span data-ttu-id="e3eec-137">Pixel</span><span class="sxs-lookup"><span data-stu-id="e3eec-137">Pixel</span></span> | <span data-ttu-id="e3eec-138">Compute</span><span class="sxs-lookup"><span data-stu-id="e3eec-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e3eec-139">x</span><span class="sxs-lookup"><span data-stu-id="e3eec-139">x</span></span>      | <span data-ttu-id="e3eec-140">x</span><span class="sxs-lookup"><span data-stu-id="e3eec-140">x</span></span>    | <span data-ttu-id="e3eec-141">x</span><span class="sxs-lookup"><span data-stu-id="e3eec-141">x</span></span>      | <span data-ttu-id="e3eec-142">x</span><span class="sxs-lookup"><span data-stu-id="e3eec-142">x</span></span>        | <span data-ttu-id="e3eec-143">x</span><span class="sxs-lookup"><span data-stu-id="e3eec-143">x</span></span>     | <span data-ttu-id="e3eec-144">x</span><span class="sxs-lookup"><span data-stu-id="e3eec-144">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="e3eec-145">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e3eec-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3eec-146">Gathergreen-Methoden</span><span class="sxs-lookup"><span data-stu-id="e3eec-146">GatherGreen methods</span></span>](texture2darray-gathergreen.md)
</dt> </dl>

 

 




