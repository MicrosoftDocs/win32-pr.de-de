---
title: 'Texturecube:: gathercmpalpha (S, float, float, uint)-Funktion'
description: 'Für vier Texel-Werte, die in einem bilinearen Filter Vorgang verwendet werden, gibt einen Vergleich der Alpha Komponente mit einem Vergleichswert zusammen mit dem Status der Kachel Zuordnung zurück. | Texturecube:: gathercmpalpha (S, float, float, uint)-Funktion'
ms.assetid: 8DC43B02-0B3C-49F0-AA94-80894A1A54BD
keywords:
- Gathercmpalpha-Funktion HLSL
topic_type:
- apiref
api_name:
- GatherCmpAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cdc4ca9f7dcbe439b9d19bbc8449347d93994e23
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869903"
---
# <a name="texturecubegathercmpalphasfloatfloatuint-function"></a><span data-ttu-id="ada2a-105">Texturecube:: gathercmpalpha (S, float, float, uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="ada2a-105">TextureCube::GatherCmpAlpha(S,float,float,uint) function</span></span>

<span data-ttu-id="ada2a-106">Für vier Texel-Werte, die in einem bilinearen Filter Vorgang verwendet werden, gibt einen Vergleich der Alpha Komponente mit einem Vergleichswert zusammen mit dem Status der Kachel Zuordnung zurück.</span><span class="sxs-lookup"><span data-stu-id="ada2a-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="ada2a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ada2a-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpAlpha(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="ada2a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ada2a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ada2a-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ada2a-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ada2a-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="ada2a-110">Type: **SamplerState**</span></span>

<span data-ttu-id="ada2a-111">Der null basierte samplerindex.</span><span class="sxs-lookup"><span data-stu-id="ada2a-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="ada2a-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ada2a-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ada2a-113">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="ada2a-113">Type: **float**</span></span>

<span data-ttu-id="ada2a-114">Die Beispiel Koordinaten (u, v).</span><span class="sxs-lookup"><span data-stu-id="ada2a-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="ada2a-115">*CompareValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ada2a-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ada2a-116">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="ada2a-116">Type: **float**</span></span>

<span data-ttu-id="ada2a-117">Ein Wert, der jeweils mit jedem Stichproben Wert verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ada2a-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="ada2a-118">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ada2a-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ada2a-119">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="ada2a-119">Type: **uint**</span></span>

<span data-ttu-id="ada2a-120">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="ada2a-120">The status of the operation.</span></span> <span data-ttu-id="ada2a-121">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="ada2a-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="ada2a-122">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="ada2a-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="ada2a-123">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="ada2a-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ada2a-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ada2a-124">Return value</span></span>

<span data-ttu-id="ada2a-125">Type: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="ada2a-125">Type: **TemplateType**</span></span>

<span data-ttu-id="ada2a-126">Ein vier komponentenwert, dessen Typ mit dem Vorlagentyp identisch ist.</span><span class="sxs-lookup"><span data-stu-id="ada2a-126">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="ada2a-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ada2a-127">Remarks</span></span>

<span data-ttu-id="ada2a-128">Die Textur Beispiele können für bilineare Interpolationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ada2a-128">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="ada2a-129">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="ada2a-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="ada2a-130">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="ada2a-130">Vertex</span></span> | <span data-ttu-id="ada2a-131">Hülle</span><span class="sxs-lookup"><span data-stu-id="ada2a-131">Hull</span></span> | <span data-ttu-id="ada2a-132">Domain</span><span class="sxs-lookup"><span data-stu-id="ada2a-132">Domain</span></span> | <span data-ttu-id="ada2a-133">Geometrie</span><span class="sxs-lookup"><span data-stu-id="ada2a-133">Geometry</span></span> | <span data-ttu-id="ada2a-134">Pixel</span><span class="sxs-lookup"><span data-stu-id="ada2a-134">Pixel</span></span> | <span data-ttu-id="ada2a-135">Compute</span><span class="sxs-lookup"><span data-stu-id="ada2a-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ada2a-136">x</span><span class="sxs-lookup"><span data-stu-id="ada2a-136">x</span></span>      | <span data-ttu-id="ada2a-137">x</span><span class="sxs-lookup"><span data-stu-id="ada2a-137">x</span></span>    | <span data-ttu-id="ada2a-138">x</span><span class="sxs-lookup"><span data-stu-id="ada2a-138">x</span></span>      | <span data-ttu-id="ada2a-139">x</span><span class="sxs-lookup"><span data-stu-id="ada2a-139">x</span></span>        | <span data-ttu-id="ada2a-140">x</span><span class="sxs-lookup"><span data-stu-id="ada2a-140">x</span></span>     | <span data-ttu-id="ada2a-141">x</span><span class="sxs-lookup"><span data-stu-id="ada2a-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ada2a-142">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ada2a-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ada2a-143">Gathercmpalpha-Methoden</span><span class="sxs-lookup"><span data-stu-id="ada2a-143">GatherCmpAlpha methods</span></span>](texturecube-gathercmpalpha.md)
</dt> <dt>

[<span data-ttu-id="ada2a-144">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="ada2a-144">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
