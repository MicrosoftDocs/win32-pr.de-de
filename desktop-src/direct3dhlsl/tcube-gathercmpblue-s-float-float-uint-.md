---
title: 'Texturecube:: gathercmpblue (S, float, float, uint)-Funktion'
description: 'Für vier Texel-Werte, die in einem bilinearen Filterungs Vorgang verwendet werden, wird ein Vergleich der blauen Komponente mit einem Vergleichswert zusammen mit dem Status der Kachel Zuordnung zurückgegeben. | Texturecube:: gathercmpblue (S, float, float, uint)-Funktion'
ms.assetid: 1D1FFF0E-9CA7-48A4-A305-C0B6059056E7
keywords:
- Gathercmpblue-Funktion HLSL
topic_type:
- apiref
api_name:
- GatherCmpBlue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2022546bb01137e730b4e0f720dbb2c3c091d609
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981320"
---
# <a name="texturecubegathercmpbluesfloatfloatuint-function"></a><span data-ttu-id="adfda-105">Texturecube:: gathercmpblue (S, float, float, uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="adfda-105">TextureCube::GatherCmpBlue(S,float,float,uint) function</span></span>

<span data-ttu-id="adfda-106">Für vier Texel-Werte, die in einem bilinearen Filterungs Vorgang verwendet werden, wird ein Vergleich der blauen Komponente mit einem Vergleichswert zusammen mit dem Status der Kachel Zuordnung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="adfda-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their blue component against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="adfda-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="adfda-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpBlue(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="adfda-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="adfda-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adfda-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="adfda-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adfda-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="adfda-110">Type: **SamplerState**</span></span>

<span data-ttu-id="adfda-111">Der null basierte samplerindex.</span><span class="sxs-lookup"><span data-stu-id="adfda-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="adfda-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="adfda-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adfda-113">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="adfda-113">Type: **float**</span></span>

<span data-ttu-id="adfda-114">Die Beispiel Koordinaten (u, v).</span><span class="sxs-lookup"><span data-stu-id="adfda-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="adfda-115">*CompareValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="adfda-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adfda-116">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="adfda-116">Type: **float**</span></span>

<span data-ttu-id="adfda-117">Ein Wert, der jeweils mit jedem Stichproben Wert verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="adfda-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="adfda-118">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="adfda-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="adfda-119">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="adfda-119">Type: **uint**</span></span>

<span data-ttu-id="adfda-120">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="adfda-120">The status of the operation.</span></span> <span data-ttu-id="adfda-121">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="adfda-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="adfda-122">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="adfda-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="adfda-123">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="adfda-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adfda-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="adfda-124">Return value</span></span>

<span data-ttu-id="adfda-125">Type: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="adfda-125">Type: **TemplateType**</span></span>

<span data-ttu-id="adfda-126">Ein vier komponentenwert, dessen Typ mit dem Vorlagentyp identisch ist.</span><span class="sxs-lookup"><span data-stu-id="adfda-126">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="adfda-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="adfda-127">Remarks</span></span>

<span data-ttu-id="adfda-128">Die Textur Beispiele können für bilineare Interpolationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="adfda-128">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="adfda-129">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="adfda-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="adfda-130">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="adfda-130">Vertex</span></span> | <span data-ttu-id="adfda-131">Hülle</span><span class="sxs-lookup"><span data-stu-id="adfda-131">Hull</span></span> | <span data-ttu-id="adfda-132">Domain</span><span class="sxs-lookup"><span data-stu-id="adfda-132">Domain</span></span> | <span data-ttu-id="adfda-133">Geometrie</span><span class="sxs-lookup"><span data-stu-id="adfda-133">Geometry</span></span> | <span data-ttu-id="adfda-134">Pixel</span><span class="sxs-lookup"><span data-stu-id="adfda-134">Pixel</span></span> | <span data-ttu-id="adfda-135">Compute</span><span class="sxs-lookup"><span data-stu-id="adfda-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="adfda-136">x</span><span class="sxs-lookup"><span data-stu-id="adfda-136">x</span></span>      | <span data-ttu-id="adfda-137">x</span><span class="sxs-lookup"><span data-stu-id="adfda-137">x</span></span>    | <span data-ttu-id="adfda-138">x</span><span class="sxs-lookup"><span data-stu-id="adfda-138">x</span></span>      | <span data-ttu-id="adfda-139">x</span><span class="sxs-lookup"><span data-stu-id="adfda-139">x</span></span>        | <span data-ttu-id="adfda-140">x</span><span class="sxs-lookup"><span data-stu-id="adfda-140">x</span></span>     | <span data-ttu-id="adfda-141">x</span><span class="sxs-lookup"><span data-stu-id="adfda-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="adfda-142">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="adfda-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adfda-143">Gathercmpblue-Methoden</span><span class="sxs-lookup"><span data-stu-id="adfda-143">GatherCmpBlue methods</span></span>](texturecube-gathercmpblue.md)
</dt> <dt>

[<span data-ttu-id="adfda-144">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="adfda-144">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
