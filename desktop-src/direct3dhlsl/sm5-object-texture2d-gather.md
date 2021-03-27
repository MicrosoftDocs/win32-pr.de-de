---
title: 'Texture2D:: Gather (S, float, int)-Funktion'
description: 'Gibt die vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden. | Texture2D:: Gather (S, float, int)-Funktion'
ms.assetid: 5d196c1c-8cc9-4add-9d33-654294314ee2
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
ms.openlocfilehash: 4d0a58be0580572441f91a3b3f637601d70cd9c8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761760"
---
# <a name="texture2dgathersfloatint-function"></a><span data-ttu-id="31b96-105">Texture2D:: Gather (S, float, int)-Funktion</span><span class="sxs-lookup"><span data-stu-id="31b96-105">Texture2D::Gather(S,float,int) function</span></span>

<span data-ttu-id="31b96-106">Gibt die vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="31b96-106">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="31b96-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="31b96-107">Syntax</span></span>

``` syntax
TemplateType Gather(
  in sampler s,
  in float2 location,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="31b96-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="31b96-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31b96-109">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="31b96-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31b96-110">Typ: **Sampler**</span><span class="sxs-lookup"><span data-stu-id="31b96-110">Type: **sampler**</span></span>

<span data-ttu-id="31b96-111">Der null basierte samplerindex.</span><span class="sxs-lookup"><span data-stu-id="31b96-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="31b96-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="31b96-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31b96-113">Typ: **float2**</span><span class="sxs-lookup"><span data-stu-id="31b96-113">Type: **float2**</span></span>

<span data-ttu-id="31b96-114">Die Beispiel Koordinaten (u, v).</span><span class="sxs-lookup"><span data-stu-id="31b96-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="31b96-115">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="31b96-115">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31b96-116">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="31b96-116">Type: **int2**</span></span>

<span data-ttu-id="31b96-117">Der Offset, der vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="31b96-117">The offset applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31b96-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="31b96-118">Return value</span></span>

<span data-ttu-id="31b96-119">Type: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="31b96-119">Type: **TemplateType**</span></span>

<span data-ttu-id="31b96-120">Ein vier komponentenwert, dessen Typ mit dem Vorlagentyp identisch ist.</span><span class="sxs-lookup"><span data-stu-id="31b96-120">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="31b96-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="31b96-121">Remarks</span></span>

<span data-ttu-id="31b96-122">Die Textur Beispiele können für bilineare Interpolationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="31b96-122">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="31b96-123">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="31b96-123">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="31b96-124">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="31b96-124">Vertex</span></span> | <span data-ttu-id="31b96-125">Hülle</span><span class="sxs-lookup"><span data-stu-id="31b96-125">Hull</span></span> | <span data-ttu-id="31b96-126">Domain</span><span class="sxs-lookup"><span data-stu-id="31b96-126">Domain</span></span> | <span data-ttu-id="31b96-127">Geometrie</span><span class="sxs-lookup"><span data-stu-id="31b96-127">Geometry</span></span> | <span data-ttu-id="31b96-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="31b96-128">Pixel</span></span> | <span data-ttu-id="31b96-129">Compute</span><span class="sxs-lookup"><span data-stu-id="31b96-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="31b96-130">x</span><span class="sxs-lookup"><span data-stu-id="31b96-130">x</span></span>      | <span data-ttu-id="31b96-131">x</span><span class="sxs-lookup"><span data-stu-id="31b96-131">x</span></span>    | <span data-ttu-id="31b96-132">x</span><span class="sxs-lookup"><span data-stu-id="31b96-132">x</span></span>      | <span data-ttu-id="31b96-133">x</span><span class="sxs-lookup"><span data-stu-id="31b96-133">x</span></span>        | <span data-ttu-id="31b96-134">x</span><span class="sxs-lookup"><span data-stu-id="31b96-134">x</span></span>     | <span data-ttu-id="31b96-135">x</span><span class="sxs-lookup"><span data-stu-id="31b96-135">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="31b96-136">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="31b96-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31b96-137">Gather-Methoden</span><span class="sxs-lookup"><span data-stu-id="31b96-137">Gather methods</span></span>](texture2d-gather.md)
</dt> <dt>

[<span data-ttu-id="31b96-138">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="31b96-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




