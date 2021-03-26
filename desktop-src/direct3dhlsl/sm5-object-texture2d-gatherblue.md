---
title: 'Texture2D:: gatherblue (S, float, int)-Funktion'
description: 'Gibt die blauen Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden. | Texture2D:: gatherblue (S, float, int)-Funktion'
ms.assetid: 6d753ef2-2818-4990-81df-52dda044d21d
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
ms.openlocfilehash: 54885ccd8f31fdf55270b6c9ac2dbafa1805d866
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981513"
---
# <a name="texture2dgatherbluesfloatint-function"></a><span data-ttu-id="2fc12-105">Texture2D:: gatherblue (S, float, int)-Funktion</span><span class="sxs-lookup"><span data-stu-id="2fc12-105">Texture2D::GatherBlue(S,float,int) function</span></span>

<span data-ttu-id="2fc12-106">Gibt die blauen Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2fc12-106">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fc12-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2fc12-107">Syntax</span></span>

``` syntax
TemplateType GatherBlue(
  in sampler s,
  in float2 location,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="2fc12-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2fc12-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fc12-109">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2fc12-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fc12-110">Typ: **Sampler**</span><span class="sxs-lookup"><span data-stu-id="2fc12-110">Type: **sampler**</span></span>

<span data-ttu-id="2fc12-111">Der null basierte samplerindex.</span><span class="sxs-lookup"><span data-stu-id="2fc12-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="2fc12-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2fc12-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fc12-113">Typ: **float2**</span><span class="sxs-lookup"><span data-stu-id="2fc12-113">Type: **float2**</span></span>

<span data-ttu-id="2fc12-114">Die Beispiel Koordinaten (u, v).</span><span class="sxs-lookup"><span data-stu-id="2fc12-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="2fc12-115">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2fc12-115">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fc12-116">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="2fc12-116">Type: **int2**</span></span>

<span data-ttu-id="2fc12-117">Ein Offset, der vor der Stichprobenentnahme auf die Textur Koordinate angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="2fc12-117">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fc12-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2fc12-118">Return value</span></span>

<span data-ttu-id="2fc12-119">Type: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="2fc12-119">Type: **TemplateType**</span></span>

<span data-ttu-id="2fc12-120">Ein vier komponentenwert, dessen Typ mit dem Vorlagentyp identisch ist.</span><span class="sxs-lookup"><span data-stu-id="2fc12-120">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fc12-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2fc12-121">Remarks</span></span>

<span data-ttu-id="2fc12-122">Die Textur Beispiele können für bilineare Interpolationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2fc12-122">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="2fc12-123">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="2fc12-123">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="2fc12-124">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="2fc12-124">Vertex</span></span> | <span data-ttu-id="2fc12-125">Hülle</span><span class="sxs-lookup"><span data-stu-id="2fc12-125">Hull</span></span> | <span data-ttu-id="2fc12-126">Domain</span><span class="sxs-lookup"><span data-stu-id="2fc12-126">Domain</span></span> | <span data-ttu-id="2fc12-127">Geometrie</span><span class="sxs-lookup"><span data-stu-id="2fc12-127">Geometry</span></span> | <span data-ttu-id="2fc12-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="2fc12-128">Pixel</span></span> | <span data-ttu-id="2fc12-129">Compute</span><span class="sxs-lookup"><span data-stu-id="2fc12-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="2fc12-130">x</span><span class="sxs-lookup"><span data-stu-id="2fc12-130">x</span></span>      | <span data-ttu-id="2fc12-131">x</span><span class="sxs-lookup"><span data-stu-id="2fc12-131">x</span></span>    | <span data-ttu-id="2fc12-132">x</span><span class="sxs-lookup"><span data-stu-id="2fc12-132">x</span></span>      | <span data-ttu-id="2fc12-133">x</span><span class="sxs-lookup"><span data-stu-id="2fc12-133">x</span></span>        | <span data-ttu-id="2fc12-134">x</span><span class="sxs-lookup"><span data-stu-id="2fc12-134">x</span></span>     | <span data-ttu-id="2fc12-135">x</span><span class="sxs-lookup"><span data-stu-id="2fc12-135">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="2fc12-136">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2fc12-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fc12-137">Gatherblue-Methoden</span><span class="sxs-lookup"><span data-stu-id="2fc12-137">GatherBlue methods</span></span>](texture2d-gatherblue.md)
</dt> <dt>

[<span data-ttu-id="2fc12-138">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="2fc12-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




