---
title: 'Texturecubearray:: gathercmpalpha (S, float, float, uint)-Funktion'
description: 'Für vier Texel-Werte, die in einem bilinearen Filter Vorgang verwendet werden, gibt einen Vergleich der Alpha Komponente mit einem Vergleichswert zusammen mit dem Status der Kachel Zuordnung zurück. | Texturecubearray:: gathercmpalpha (S, float, float, uint)-Funktion'
ms.assetid: EA1D7176-3F70-4867-9854-80206A871B23
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
ms.openlocfilehash: 198179b67a2812417e60a0a1e1512b686d52e98a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995622"
---
# <a name="texturecubearraygathercmpalphasfloatfloatuint-function"></a><span data-ttu-id="1d0ae-105">Texturecubearray:: gathercmpalpha (S, float, float, uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="1d0ae-105">TextureCubeArray::GatherCmpAlpha(S,float,float,uint) function</span></span>

<span data-ttu-id="1d0ae-106">Für vier Texel-Werte, die in einem bilinearen Filter Vorgang verwendet werden, gibt einen Vergleich der Alpha Komponente mit einem Vergleichswert zusammen mit dem Status der Kachel Zuordnung zurück.</span><span class="sxs-lookup"><span data-stu-id="1d0ae-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d0ae-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d0ae-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpAlpha(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="1d0ae-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d0ae-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d0ae-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1d0ae-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d0ae-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="1d0ae-110">Type: **SamplerState**</span></span>

<span data-ttu-id="1d0ae-111">Der null basierte samplerindex.</span><span class="sxs-lookup"><span data-stu-id="1d0ae-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="1d0ae-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1d0ae-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d0ae-113">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="1d0ae-113">Type: **float**</span></span>

<span data-ttu-id="1d0ae-114">Die Beispiel Koordinaten (u, v).</span><span class="sxs-lookup"><span data-stu-id="1d0ae-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="1d0ae-115">*CompareValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1d0ae-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d0ae-116">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="1d0ae-116">Type: **float**</span></span>

<span data-ttu-id="1d0ae-117">Ein Wert, der jeweils mit jedem Stichproben Wert verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="1d0ae-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="1d0ae-118">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1d0ae-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d0ae-119">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="1d0ae-119">Type: **uint**</span></span>

<span data-ttu-id="1d0ae-120">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="1d0ae-120">The status of the operation.</span></span> <span data-ttu-id="1d0ae-121">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="1d0ae-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="1d0ae-122">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="1d0ae-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="1d0ae-123">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="1d0ae-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d0ae-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1d0ae-124">Return value</span></span>

<span data-ttu-id="1d0ae-125">Type: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="1d0ae-125">Type: **TemplateType**</span></span>

<span data-ttu-id="1d0ae-126">Ein vier komponentenwert, dessen Typ mit dem Vorlagentyp identisch ist.</span><span class="sxs-lookup"><span data-stu-id="1d0ae-126">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d0ae-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1d0ae-127">Remarks</span></span>

<span data-ttu-id="1d0ae-128">Die Textur Beispiele können für bilineare Interpolationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1d0ae-128">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="1d0ae-129">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="1d0ae-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="1d0ae-130">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="1d0ae-130">Vertex</span></span> | <span data-ttu-id="1d0ae-131">Hülle</span><span class="sxs-lookup"><span data-stu-id="1d0ae-131">Hull</span></span> | <span data-ttu-id="1d0ae-132">Domain</span><span class="sxs-lookup"><span data-stu-id="1d0ae-132">Domain</span></span> | <span data-ttu-id="1d0ae-133">Geometrie</span><span class="sxs-lookup"><span data-stu-id="1d0ae-133">Geometry</span></span> | <span data-ttu-id="1d0ae-134">Pixel</span><span class="sxs-lookup"><span data-stu-id="1d0ae-134">Pixel</span></span> | <span data-ttu-id="1d0ae-135">Compute</span><span class="sxs-lookup"><span data-stu-id="1d0ae-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="1d0ae-136">x</span><span class="sxs-lookup"><span data-stu-id="1d0ae-136">x</span></span>      | <span data-ttu-id="1d0ae-137">x</span><span class="sxs-lookup"><span data-stu-id="1d0ae-137">x</span></span>    | <span data-ttu-id="1d0ae-138">x</span><span class="sxs-lookup"><span data-stu-id="1d0ae-138">x</span></span>      | <span data-ttu-id="1d0ae-139">x</span><span class="sxs-lookup"><span data-stu-id="1d0ae-139">x</span></span>        | <span data-ttu-id="1d0ae-140">x</span><span class="sxs-lookup"><span data-stu-id="1d0ae-140">x</span></span>     | <span data-ttu-id="1d0ae-141">x</span><span class="sxs-lookup"><span data-stu-id="1d0ae-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="1d0ae-142">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1d0ae-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d0ae-143">Gathercmpalpha-Methoden</span><span class="sxs-lookup"><span data-stu-id="1d0ae-143">GatherCmpAlpha methods</span></span>](texturecubearray-gathercmpalpha.md)
</dt> <dt>

[<span data-ttu-id="1d0ae-144">**Texturecubearray**</span><span class="sxs-lookup"><span data-stu-id="1d0ae-144">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
