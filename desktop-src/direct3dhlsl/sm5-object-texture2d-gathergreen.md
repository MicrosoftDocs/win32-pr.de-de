---
title: 'Texture2D:: gathergreen (S, float, int)-Funktion'
description: 'Für vier textexwerte, die in einem bilinearen Filterungs Vorgang verwendet werden, wird ein Vergleich der grünen Komponente mit einem Vergleichswert zurückgegeben. | Texture2D:: gathergreen (S, float, int)-Funktion'
ms.assetid: 97e1fb52-75f4-4e73-93f1-98b7a5925efc
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
ms.openlocfilehash: 722d7a3ac90fa3083b8f42f7704f5c9e0aeb1829
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995558"
---
# <a name="texture2dgathergreensfloatint-function"></a><span data-ttu-id="722cd-105">Texture2D:: gathergreen (S, float, int)-Funktion</span><span class="sxs-lookup"><span data-stu-id="722cd-105">Texture2D::GatherGreen(S,float,int) function</span></span>

<span data-ttu-id="722cd-106">Für vier textexwerte, die in einem bilinearen Filterungs Vorgang verwendet werden, wird ein Vergleich der grünen Komponente mit einem Vergleichswert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="722cd-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their green component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="722cd-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="722cd-107">Syntax</span></span>

``` syntax
TemplateType GatherGreen(
  in sampler s,
  in float2 location,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="722cd-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="722cd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="722cd-109">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="722cd-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="722cd-110">Typ: **Sampler**</span><span class="sxs-lookup"><span data-stu-id="722cd-110">Type: **sampler**</span></span>

<span data-ttu-id="722cd-111">Der null basierte samplerindex.</span><span class="sxs-lookup"><span data-stu-id="722cd-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="722cd-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="722cd-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="722cd-113">Typ: **float2**</span><span class="sxs-lookup"><span data-stu-id="722cd-113">Type: **float2**</span></span>

<span data-ttu-id="722cd-114">Die Beispiel Koordinaten (u, v).</span><span class="sxs-lookup"><span data-stu-id="722cd-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="722cd-115">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="722cd-115">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="722cd-116">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="722cd-116">Type: **int2**</span></span>

<span data-ttu-id="722cd-117">Ein Offset, der vor der Stichprobenentnahme auf die Textur Koordinate angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="722cd-117">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="722cd-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="722cd-118">Return value</span></span>

<span data-ttu-id="722cd-119">Type: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="722cd-119">Type: **TemplateType**</span></span>

<span data-ttu-id="722cd-120">Ein vier komponentenwert, dessen Typ mit dem Vorlagentyp identisch ist.</span><span class="sxs-lookup"><span data-stu-id="722cd-120">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="722cd-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="722cd-121">Remarks</span></span>

<span data-ttu-id="722cd-122">Die Textur Beispiele können für bilineare Interpolationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="722cd-122">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="722cd-123">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="722cd-123">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="722cd-124">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="722cd-124">Vertex</span></span> | <span data-ttu-id="722cd-125">Hülle</span><span class="sxs-lookup"><span data-stu-id="722cd-125">Hull</span></span> | <span data-ttu-id="722cd-126">Domain</span><span class="sxs-lookup"><span data-stu-id="722cd-126">Domain</span></span> | <span data-ttu-id="722cd-127">Geometrie</span><span class="sxs-lookup"><span data-stu-id="722cd-127">Geometry</span></span> | <span data-ttu-id="722cd-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="722cd-128">Pixel</span></span> | <span data-ttu-id="722cd-129">Compute</span><span class="sxs-lookup"><span data-stu-id="722cd-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="722cd-130">x</span><span class="sxs-lookup"><span data-stu-id="722cd-130">x</span></span>      | <span data-ttu-id="722cd-131">x</span><span class="sxs-lookup"><span data-stu-id="722cd-131">x</span></span>    | <span data-ttu-id="722cd-132">x</span><span class="sxs-lookup"><span data-stu-id="722cd-132">x</span></span>      | <span data-ttu-id="722cd-133">x</span><span class="sxs-lookup"><span data-stu-id="722cd-133">x</span></span>        | <span data-ttu-id="722cd-134">x</span><span class="sxs-lookup"><span data-stu-id="722cd-134">x</span></span>     | <span data-ttu-id="722cd-135">x</span><span class="sxs-lookup"><span data-stu-id="722cd-135">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="722cd-136">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="722cd-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="722cd-137">Gathergreen-Methoden</span><span class="sxs-lookup"><span data-stu-id="722cd-137">GatherGreen methods</span></span>](texture2d-gathergreen.md)
</dt> <dt>

[<span data-ttu-id="722cd-138">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="722cd-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




