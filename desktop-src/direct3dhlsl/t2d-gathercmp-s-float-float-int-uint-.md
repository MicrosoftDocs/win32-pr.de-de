---
title: 'Texture2D:: gathercmp (S, float, float, int, uint)-Funktion'
description: 'Bei vier textexwerten, die in einem bilinearen Filter Vorgang verwendet werden, wird der Vergleich mit einem Vergleichswert zusammen mit dem Status der Kachel Zuordnung zurückgegeben. | Texture2D:: gathercmp (S, float, float, int, uint)-Funktion'
ms.assetid: A6610587-97C3-4CE5-86A7-3411D422BC8F
keywords:
- Gathercmp-Funktion HLSL
topic_type:
- apiref
api_name:
- GatherCmp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: be8246053e0f7ba6357bdd68dc59059fd225bbc8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981872"
---
# <a name="texture2dgathercmpsfloatfloatintuint-function"></a><span data-ttu-id="496d5-105">Texture2D:: gathercmp (S, float, float, int, uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="496d5-105">Texture2D::GatherCmp(S,float,float,int,uint) function</span></span>

<span data-ttu-id="496d5-106">Bei vier textexwerten, die in einem bilinearen Filter Vorgang verwendet werden, wird der Vergleich mit einem Vergleichswert zusammen mit dem Status der Kachel Zuordnung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="496d5-106">For four texel values that would be used in a bi-linear filtering operation, returns their comparison against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="496d5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="496d5-107">Syntax</span></span>


``` syntax
TemplateType GatherCmp(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int2         Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="496d5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="496d5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="496d5-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="496d5-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="496d5-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="496d5-110">Type: **SamplerState**</span></span>

<span data-ttu-id="496d5-111">Der null basierte samplerindex.</span><span class="sxs-lookup"><span data-stu-id="496d5-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="496d5-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="496d5-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="496d5-113">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="496d5-113">Type: **float**</span></span>

<span data-ttu-id="496d5-114">Die Beispiel Koordinaten (u, v).</span><span class="sxs-lookup"><span data-stu-id="496d5-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="496d5-115">*CompareValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="496d5-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="496d5-116">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="496d5-116">Type: **float**</span></span>

<span data-ttu-id="496d5-117">Ein Wert, der jeweils mit jedem Stichproben Wert verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="496d5-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="496d5-118">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="496d5-118">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="496d5-119">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="496d5-119">Type: **int2**</span></span>

<span data-ttu-id="496d5-120">Der Offset in texeln, der vor der Stichprobenentnahme auf die Texturkoordinaten angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="496d5-120">The offset in texels applied to the texture coordinates before sampling.</span></span> <span data-ttu-id="496d5-121">Muss ein Literalwert sein.</span><span class="sxs-lookup"><span data-stu-id="496d5-121">Must be a literal value.</span></span>

</dd> <dt>

<span data-ttu-id="496d5-122">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="496d5-122">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="496d5-123">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="496d5-123">Type: **uint**</span></span>

<span data-ttu-id="496d5-124">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="496d5-124">The status of the operation.</span></span> <span data-ttu-id="496d5-125">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="496d5-125">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="496d5-126">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="496d5-126">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="496d5-127">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="496d5-127">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="496d5-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="496d5-128">Return value</span></span>

<span data-ttu-id="496d5-129">Type: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="496d5-129">Type: **TemplateType**</span></span>

<span data-ttu-id="496d5-130">Ein vier komponentenwert, dessen Typ mit dem Vorlagentyp identisch ist.</span><span class="sxs-lookup"><span data-stu-id="496d5-130">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="496d5-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="496d5-131">Remarks</span></span>

<span data-ttu-id="496d5-132">Die Textur Beispiele können für bilineare Interpolationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="496d5-132">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="496d5-133">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="496d5-133">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="496d5-134">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="496d5-134">Vertex</span></span> | <span data-ttu-id="496d5-135">Hülle</span><span class="sxs-lookup"><span data-stu-id="496d5-135">Hull</span></span> | <span data-ttu-id="496d5-136">Domain</span><span class="sxs-lookup"><span data-stu-id="496d5-136">Domain</span></span> | <span data-ttu-id="496d5-137">Geometrie</span><span class="sxs-lookup"><span data-stu-id="496d5-137">Geometry</span></span> | <span data-ttu-id="496d5-138">Pixel</span><span class="sxs-lookup"><span data-stu-id="496d5-138">Pixel</span></span> | <span data-ttu-id="496d5-139">Compute</span><span class="sxs-lookup"><span data-stu-id="496d5-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="496d5-140">x</span><span class="sxs-lookup"><span data-stu-id="496d5-140">x</span></span>      | <span data-ttu-id="496d5-141">x</span><span class="sxs-lookup"><span data-stu-id="496d5-141">x</span></span>    | <span data-ttu-id="496d5-142">x</span><span class="sxs-lookup"><span data-stu-id="496d5-142">x</span></span>      | <span data-ttu-id="496d5-143">x</span><span class="sxs-lookup"><span data-stu-id="496d5-143">x</span></span>        | <span data-ttu-id="496d5-144">x</span><span class="sxs-lookup"><span data-stu-id="496d5-144">x</span></span>     | <span data-ttu-id="496d5-145">x</span><span class="sxs-lookup"><span data-stu-id="496d5-145">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="496d5-146">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="496d5-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="496d5-147">Gathercmp-Methoden</span><span class="sxs-lookup"><span data-stu-id="496d5-147">GatherCmp methods</span></span>](texture2d-gathercmp.md)
</dt> </dl>

 

 
