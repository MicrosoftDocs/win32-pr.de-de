---
title: 'Texturecubearray:: gathercmp (S, float, float, uint)-Funktion'
description: 'Bei vier textexwerten, die in einem bilinearen Filter Vorgang verwendet werden, wird der Vergleich mit einem Vergleichswert zusammen mit dem Status der Kachel Zuordnung zurückgegeben. | Texturecubearray:: gathercmp (S, float, float, uint)-Funktion'
ms.assetid: 758CD159-58B6-42AE-92B3-5AA3C72FD0F1
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
ms.openlocfilehash: 73ef87805fa69529e1790c3ac2fed539cac57b0c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352819"
---
# <a name="texturecubearraygathercmpsfloatfloatuint-function"></a><span data-ttu-id="f0260-105">Texturecubearray:: gathercmp (S, float, float, uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="f0260-105">TextureCubeArray::GatherCmp(S,float,float,uint) function</span></span>

<span data-ttu-id="f0260-106">Bei vier textexwerten, die in einem bilinearen Filter Vorgang verwendet werden, wird der Vergleich mit einem Vergleichswert zusammen mit dem Status der Kachel Zuordnung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f0260-106">For four texel values that would be used in a bi-linear filtering operation, returns their comparison against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0260-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0260-107">Syntax</span></span>


``` syntax
TemplateType GatherCmp(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="f0260-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0260-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0260-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f0260-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0260-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="f0260-110">Type: **SamplerState**</span></span>

<span data-ttu-id="f0260-111">Der null basierte samplerindex.</span><span class="sxs-lookup"><span data-stu-id="f0260-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="f0260-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f0260-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0260-113">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="f0260-113">Type: **float**</span></span>

<span data-ttu-id="f0260-114">Die Beispiel Koordinaten (u, v).</span><span class="sxs-lookup"><span data-stu-id="f0260-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="f0260-115">*CompareValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f0260-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0260-116">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="f0260-116">Type: **float**</span></span>

<span data-ttu-id="f0260-117">Ein Wert, der jeweils mit jedem Stichproben Wert verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f0260-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="f0260-118">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f0260-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0260-119">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="f0260-119">Type: **uint**</span></span>

<span data-ttu-id="f0260-120">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="f0260-120">The status of the operation.</span></span> <span data-ttu-id="f0260-121">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="f0260-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="f0260-122">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="f0260-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="f0260-123">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="f0260-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0260-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f0260-124">Return value</span></span>

<span data-ttu-id="f0260-125">Type: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="f0260-125">Type: **TemplateType**</span></span>

<span data-ttu-id="f0260-126">Ein vier komponentenwert, dessen Typ mit dem Vorlagentyp identisch ist.</span><span class="sxs-lookup"><span data-stu-id="f0260-126">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0260-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f0260-127">Remarks</span></span>

<span data-ttu-id="f0260-128">Die Textur Beispiele können für bilineare Interpolationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f0260-128">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="f0260-129">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="f0260-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="f0260-130">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="f0260-130">Vertex</span></span> | <span data-ttu-id="f0260-131">Hülle</span><span class="sxs-lookup"><span data-stu-id="f0260-131">Hull</span></span> | <span data-ttu-id="f0260-132">Domain</span><span class="sxs-lookup"><span data-stu-id="f0260-132">Domain</span></span> | <span data-ttu-id="f0260-133">Geometrie</span><span class="sxs-lookup"><span data-stu-id="f0260-133">Geometry</span></span> | <span data-ttu-id="f0260-134">Pixel</span><span class="sxs-lookup"><span data-stu-id="f0260-134">Pixel</span></span> | <span data-ttu-id="f0260-135">Compute</span><span class="sxs-lookup"><span data-stu-id="f0260-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f0260-136">x</span><span class="sxs-lookup"><span data-stu-id="f0260-136">x</span></span>      | <span data-ttu-id="f0260-137">x</span><span class="sxs-lookup"><span data-stu-id="f0260-137">x</span></span>    | <span data-ttu-id="f0260-138">x</span><span class="sxs-lookup"><span data-stu-id="f0260-138">x</span></span>      | <span data-ttu-id="f0260-139">x</span><span class="sxs-lookup"><span data-stu-id="f0260-139">x</span></span>        | <span data-ttu-id="f0260-140">x</span><span class="sxs-lookup"><span data-stu-id="f0260-140">x</span></span>     | <span data-ttu-id="f0260-141">x</span><span class="sxs-lookup"><span data-stu-id="f0260-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="f0260-142">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f0260-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0260-143">Gathercmp-Methoden</span><span class="sxs-lookup"><span data-stu-id="f0260-143">GatherCmp methods</span></span>](texturecubearray-gathercmp.md)
</dt> <dt>

[<span data-ttu-id="f0260-144">**Texturecubearray**</span><span class="sxs-lookup"><span data-stu-id="f0260-144">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
