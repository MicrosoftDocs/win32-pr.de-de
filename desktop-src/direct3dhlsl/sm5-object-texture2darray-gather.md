---
title: 'Texture2DArray:: Gather (S, float, int)-Funktion'
description: 'Gibt die vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden. | Texture2DArray:: Gather (S, float, int)-Funktion'
ms.assetid: b0355158-01c8-45a1-bb5d-29a8c43b1685
keywords:
- Funktion "HLSL" erfassen
topic_type:
- apiref
api_name:
- Gather
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 46866df18a0836b311443a3dd411d74dfa7fb126
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995327"
---
# <a name="texture2darraygathersfloatint-function"></a><span data-ttu-id="4d621-105">Texture2DArray:: Gather (S, float, int)-Funktion</span><span class="sxs-lookup"><span data-stu-id="4d621-105">Texture2DArray::Gather(S,float,int) function</span></span>

<span data-ttu-id="4d621-106">Gibt die vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4d621-106">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d621-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d621-107">Syntax</span></span>

``` syntax
TemplateType Gather(
  in sampler s,
  in float3 location,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="4d621-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d621-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d621-109">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4d621-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d621-110">Typ: **Sampler**</span><span class="sxs-lookup"><span data-stu-id="4d621-110">Type: **sampler**</span></span>

<span data-ttu-id="4d621-111">Der null basierte samplerindex.</span><span class="sxs-lookup"><span data-stu-id="4d621-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="4d621-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4d621-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d621-113">Typ: **float3**</span><span class="sxs-lookup"><span data-stu-id="4d621-113">Type: **float3**</span></span>

<span data-ttu-id="4d621-114">Die Beispiel Koordinaten (u, v).</span><span class="sxs-lookup"><span data-stu-id="4d621-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="4d621-115">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4d621-115">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d621-116">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="4d621-116">Type: **int2**</span></span>

<span data-ttu-id="4d621-117">Der Offset, der vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="4d621-117">The offset applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d621-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4d621-118">Return value</span></span>

<span data-ttu-id="4d621-119">Type: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="4d621-119">Type: **TemplateType**</span></span>

<span data-ttu-id="4d621-120">Ein vier komponentenwert, dessen Typ mit dem Vorlagentyp identisch ist.</span><span class="sxs-lookup"><span data-stu-id="4d621-120">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d621-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4d621-121">Remarks</span></span>

<span data-ttu-id="4d621-122">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="4d621-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="4d621-123">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="4d621-123">Vertex</span></span> | <span data-ttu-id="4d621-124">Hülle</span><span class="sxs-lookup"><span data-stu-id="4d621-124">Hull</span></span> | <span data-ttu-id="4d621-125">Domain</span><span class="sxs-lookup"><span data-stu-id="4d621-125">Domain</span></span> | <span data-ttu-id="4d621-126">Geometrie</span><span class="sxs-lookup"><span data-stu-id="4d621-126">Geometry</span></span> | <span data-ttu-id="4d621-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="4d621-127">Pixel</span></span> | <span data-ttu-id="4d621-128">Compute</span><span class="sxs-lookup"><span data-stu-id="4d621-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="4d621-129">x</span><span class="sxs-lookup"><span data-stu-id="4d621-129">x</span></span>      | <span data-ttu-id="4d621-130">x</span><span class="sxs-lookup"><span data-stu-id="4d621-130">x</span></span>    | <span data-ttu-id="4d621-131">x</span><span class="sxs-lookup"><span data-stu-id="4d621-131">x</span></span>      | <span data-ttu-id="4d621-132">x</span><span class="sxs-lookup"><span data-stu-id="4d621-132">x</span></span>        | <span data-ttu-id="4d621-133">x</span><span class="sxs-lookup"><span data-stu-id="4d621-133">x</span></span>     | <span data-ttu-id="4d621-134">x</span><span class="sxs-lookup"><span data-stu-id="4d621-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="4d621-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4d621-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d621-136">Gather-Methoden</span><span class="sxs-lookup"><span data-stu-id="4d621-136">Gather methods</span></span>](texture2darray-gather.md)
</dt> <dt>

[<span data-ttu-id="4d621-137">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="4d621-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




