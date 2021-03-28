---
title: 'Texturecube:: gathercmpgreen (S, float, float, uint)-Funktion'
description: 'Für vier Texel-Werte, die in einem bilinearen Filter Vorgang verwendet werden, gibt einen Vergleich der grünen Komponente mit einem Vergleichswert zusammen mit dem Status der Kachel Zuordnung zurück. | Texturecube:: gathercmpgreen (S, float, float, uint)-Funktion'
ms.assetid: 3EFCEFE1-BFE2-4448-962E-108C3C0861E5
keywords:
- Gathercmpgreen-Funktion HLSL
topic_type:
- apiref
api_name:
- GatherCmpGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 910aef93a824b2725b13a177b5bbcfc8fa99aff9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352948"
---
# <a name="texturecubegathercmpgreensfloatfloatuint-function"></a><span data-ttu-id="3d8b7-105">Texturecube:: gathercmpgreen (S, float, float, uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="3d8b7-105">TextureCube::GatherCmpGreen(S,float,float,uint) function</span></span>

<span data-ttu-id="3d8b7-106">Für vier Texel-Werte, die in einem bilinearen Filter Vorgang verwendet werden, gibt einen Vergleich der grünen Komponente mit einem Vergleichswert zusammen mit dem Status der Kachel Zuordnung zurück.</span><span class="sxs-lookup"><span data-stu-id="3d8b7-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their green component against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d8b7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d8b7-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpGreen(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="3d8b7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d8b7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d8b7-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d8b7-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d8b7-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="3d8b7-110">Type: **SamplerState**</span></span>

<span data-ttu-id="3d8b7-111">Der null basierte samplerindex.</span><span class="sxs-lookup"><span data-stu-id="3d8b7-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="3d8b7-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d8b7-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d8b7-113">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="3d8b7-113">Type: **float**</span></span>

<span data-ttu-id="3d8b7-114">Die Beispiel Koordinaten (u, v).</span><span class="sxs-lookup"><span data-stu-id="3d8b7-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="3d8b7-115">*CompareValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d8b7-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d8b7-116">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="3d8b7-116">Type: **float**</span></span>

<span data-ttu-id="3d8b7-117">Ein Wert, der jeweils mit jedem Stichproben Wert verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="3d8b7-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="3d8b7-118">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3d8b7-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3d8b7-119">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="3d8b7-119">Type: **uint**</span></span>

<span data-ttu-id="3d8b7-120">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="3d8b7-120">The status of the operation.</span></span> <span data-ttu-id="3d8b7-121">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="3d8b7-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="3d8b7-122">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="3d8b7-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="3d8b7-123">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="3d8b7-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d8b7-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3d8b7-124">Return value</span></span>

<span data-ttu-id="3d8b7-125">Type: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="3d8b7-125">Type: **TemplateType**</span></span>

<span data-ttu-id="3d8b7-126">Ein vier komponentenwert, dessen Typ mit dem Vorlagentyp identisch ist.</span><span class="sxs-lookup"><span data-stu-id="3d8b7-126">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d8b7-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3d8b7-127">Remarks</span></span>

<span data-ttu-id="3d8b7-128">Die Textur Beispiele können für bilineare Interpolationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3d8b7-128">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="3d8b7-129">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="3d8b7-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="3d8b7-130">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="3d8b7-130">Vertex</span></span> | <span data-ttu-id="3d8b7-131">Hülle</span><span class="sxs-lookup"><span data-stu-id="3d8b7-131">Hull</span></span> | <span data-ttu-id="3d8b7-132">Domain</span><span class="sxs-lookup"><span data-stu-id="3d8b7-132">Domain</span></span> | <span data-ttu-id="3d8b7-133">Geometrie</span><span class="sxs-lookup"><span data-stu-id="3d8b7-133">Geometry</span></span> | <span data-ttu-id="3d8b7-134">Pixel</span><span class="sxs-lookup"><span data-stu-id="3d8b7-134">Pixel</span></span> | <span data-ttu-id="3d8b7-135">Compute</span><span class="sxs-lookup"><span data-stu-id="3d8b7-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="3d8b7-136">x</span><span class="sxs-lookup"><span data-stu-id="3d8b7-136">x</span></span>      | <span data-ttu-id="3d8b7-137">x</span><span class="sxs-lookup"><span data-stu-id="3d8b7-137">x</span></span>    | <span data-ttu-id="3d8b7-138">x</span><span class="sxs-lookup"><span data-stu-id="3d8b7-138">x</span></span>      | <span data-ttu-id="3d8b7-139">x</span><span class="sxs-lookup"><span data-stu-id="3d8b7-139">x</span></span>        | <span data-ttu-id="3d8b7-140">x</span><span class="sxs-lookup"><span data-stu-id="3d8b7-140">x</span></span>     | <span data-ttu-id="3d8b7-141">x</span><span class="sxs-lookup"><span data-stu-id="3d8b7-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="3d8b7-142">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3d8b7-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d8b7-143">Gathercmpgreen-Methoden</span><span class="sxs-lookup"><span data-stu-id="3d8b7-143">GatherCmpGreen methods</span></span>](texturecube-gathercmpgreen.md)
</dt> <dt>

[<span data-ttu-id="3d8b7-144">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="3d8b7-144">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
