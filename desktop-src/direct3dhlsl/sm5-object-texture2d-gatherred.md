---
title: 'Texture2D:: gatherred (S, float, int)-Funktion'
description: 'Für vier textexwerte, die in einem bilinearen Filter Vorgang verwendet werden, wird ein Vergleich der roten Komponente mit einem Vergleichswert zurückgegeben. | Texture2D:: gatherred (S, float, int)-Funktion'
ms.assetid: 6d2d1556-d52f-4625-93ca-34da399f9a8b
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
ms.openlocfilehash: f05196063f6a17cc34865157c17a92bc2bb116bf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981705"
---
# <a name="texture2dgatherredsfloatint-function"></a><span data-ttu-id="999f0-105">Texture2D:: gatherred (S, float, int)-Funktion</span><span class="sxs-lookup"><span data-stu-id="999f0-105">Texture2D::GatherRed(S,float,int) function</span></span>

<span data-ttu-id="999f0-106">Für vier textexwerte, die in einem bilinearen Filter Vorgang verwendet werden, wird ein Vergleich der roten Komponente mit einem Vergleichswert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="999f0-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="999f0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="999f0-107">Syntax</span></span>

``` syntax
TemplateType GatherRed(
  in sampler s,
  in float2 location,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="999f0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="999f0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="999f0-109">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="999f0-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="999f0-110">Typ: **Sampler**</span><span class="sxs-lookup"><span data-stu-id="999f0-110">Type: **sampler**</span></span>

<span data-ttu-id="999f0-111">Der null basierte samplerindex.</span><span class="sxs-lookup"><span data-stu-id="999f0-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="999f0-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="999f0-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="999f0-113">Typ: **float2**</span><span class="sxs-lookup"><span data-stu-id="999f0-113">Type: **float2**</span></span>

<span data-ttu-id="999f0-114">Die Beispiel Koordinaten (u, v).</span><span class="sxs-lookup"><span data-stu-id="999f0-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="999f0-115">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="999f0-115">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="999f0-116">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="999f0-116">Type: **int2**</span></span>

<span data-ttu-id="999f0-117">Ein Offset, der vor der Stichprobenentnahme auf die Textur Koordinate angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="999f0-117">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="999f0-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="999f0-118">Return value</span></span>

<span data-ttu-id="999f0-119">Type: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="999f0-119">Type: **TemplateType**</span></span>

<span data-ttu-id="999f0-120">Ein vier komponentenwert, dessen Typ mit dem Vorlagentyp identisch ist.</span><span class="sxs-lookup"><span data-stu-id="999f0-120">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="999f0-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="999f0-121">Remarks</span></span>

<span data-ttu-id="999f0-122">Die Textur Beispiele können für bilineare Interpolationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="999f0-122">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="999f0-123">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="999f0-123">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="999f0-124">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="999f0-124">Vertex</span></span> | <span data-ttu-id="999f0-125">Hülle</span><span class="sxs-lookup"><span data-stu-id="999f0-125">Hull</span></span> | <span data-ttu-id="999f0-126">Domain</span><span class="sxs-lookup"><span data-stu-id="999f0-126">Domain</span></span> | <span data-ttu-id="999f0-127">Geometrie</span><span class="sxs-lookup"><span data-stu-id="999f0-127">Geometry</span></span> | <span data-ttu-id="999f0-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="999f0-128">Pixel</span></span> | <span data-ttu-id="999f0-129">Compute</span><span class="sxs-lookup"><span data-stu-id="999f0-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="999f0-130">x</span><span class="sxs-lookup"><span data-stu-id="999f0-130">x</span></span>      | <span data-ttu-id="999f0-131">x</span><span class="sxs-lookup"><span data-stu-id="999f0-131">x</span></span>    | <span data-ttu-id="999f0-132">x</span><span class="sxs-lookup"><span data-stu-id="999f0-132">x</span></span>      | <span data-ttu-id="999f0-133">x</span><span class="sxs-lookup"><span data-stu-id="999f0-133">x</span></span>        | <span data-ttu-id="999f0-134">x</span><span class="sxs-lookup"><span data-stu-id="999f0-134">x</span></span>     | <span data-ttu-id="999f0-135">x</span><span class="sxs-lookup"><span data-stu-id="999f0-135">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="999f0-136">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="999f0-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="999f0-137">Gatherred-Methoden</span><span class="sxs-lookup"><span data-stu-id="999f0-137">GatherRed methods</span></span>](texture2d-gatherred.md)
</dt> <dt>

[<span data-ttu-id="999f0-138">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="999f0-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




