---
title: 'Texture2DArray:: gatherred (S, float, int)-Funktion'
description: 'Gibt die roten Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden. | Texture2DArray:: gatherred (S, float, int)-Funktion'
ms.assetid: cb9c21ef-87f4-4c32-b41a-9fc7478713a6
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
ms.openlocfilehash: 431d08b77d13540bb48621a6d5ec76f4c775f796
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995550"
---
# <a name="texture2darraygatherredsfloatint-function"></a><span data-ttu-id="4f356-105">Texture2DArray:: gatherred (S, float, int)-Funktion</span><span class="sxs-lookup"><span data-stu-id="4f356-105">Texture2DArray::GatherRed(S,float,int) function</span></span>

<span data-ttu-id="4f356-106">Gibt die roten Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4f356-106">Returns the red components of the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f356-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f356-107">Syntax</span></span>

``` syntax
TemplateType GatherRed(
  in sampler s,
  in float3 location,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="4f356-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f356-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f356-109">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4f356-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f356-110">Typ: **Sampler**</span><span class="sxs-lookup"><span data-stu-id="4f356-110">Type: **sampler**</span></span>

<span data-ttu-id="4f356-111">Der null basierte samplerindex.</span><span class="sxs-lookup"><span data-stu-id="4f356-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="4f356-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4f356-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f356-113">Typ: **float3**</span><span class="sxs-lookup"><span data-stu-id="4f356-113">Type: **float3**</span></span>

<span data-ttu-id="4f356-114">Die Beispiel Koordinaten (u, v).</span><span class="sxs-lookup"><span data-stu-id="4f356-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="4f356-115">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4f356-115">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f356-116">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="4f356-116">Type: **int2**</span></span>

<span data-ttu-id="4f356-117">Ein Offset, der vor der Stichprobenentnahme auf die Textur Koordinate angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="4f356-117">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f356-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4f356-118">Return value</span></span>

<span data-ttu-id="4f356-119">Type: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="4f356-119">Type: **TemplateType**</span></span>

<span data-ttu-id="4f356-120">Ein vier komponentenwert, dessen Typ mit dem Vorlagentyp identisch ist.</span><span class="sxs-lookup"><span data-stu-id="4f356-120">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f356-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4f356-121">Remarks</span></span>

<span data-ttu-id="4f356-122">Die Textur Beispiele können für bilineare Interpolationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4f356-122">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="4f356-123">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="4f356-123">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="4f356-124">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="4f356-124">Vertex</span></span> | <span data-ttu-id="4f356-125">Hülle</span><span class="sxs-lookup"><span data-stu-id="4f356-125">Hull</span></span> | <span data-ttu-id="4f356-126">Domain</span><span class="sxs-lookup"><span data-stu-id="4f356-126">Domain</span></span> | <span data-ttu-id="4f356-127">Geometrie</span><span class="sxs-lookup"><span data-stu-id="4f356-127">Geometry</span></span> | <span data-ttu-id="4f356-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="4f356-128">Pixel</span></span> | <span data-ttu-id="4f356-129">Compute</span><span class="sxs-lookup"><span data-stu-id="4f356-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="4f356-130">x</span><span class="sxs-lookup"><span data-stu-id="4f356-130">x</span></span>      | <span data-ttu-id="4f356-131">x</span><span class="sxs-lookup"><span data-stu-id="4f356-131">x</span></span>    | <span data-ttu-id="4f356-132">x</span><span class="sxs-lookup"><span data-stu-id="4f356-132">x</span></span>      | <span data-ttu-id="4f356-133">x</span><span class="sxs-lookup"><span data-stu-id="4f356-133">x</span></span>        | <span data-ttu-id="4f356-134">x</span><span class="sxs-lookup"><span data-stu-id="4f356-134">x</span></span>     | <span data-ttu-id="4f356-135">x</span><span class="sxs-lookup"><span data-stu-id="4f356-135">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="4f356-136">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4f356-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f356-137">Gatherred-Methoden</span><span class="sxs-lookup"><span data-stu-id="4f356-137">GatherRed methods</span></span>](texture2darray-gatherred.md)
</dt> <dt>

[<span data-ttu-id="4f356-138">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="4f356-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




