---
title: 'Texturecubearray:: gathercmpred (S, float, float, uint)-Funktion'
description: 'Für vier Texel-Werte, die in einem bilinearen Filter Vorgang verwendet werden, gibt einen Vergleich der roten Komponente mit einem Vergleichswert zusammen mit dem Status der Kachel Zuordnung zurück. | Texturecubearray:: gathercmpred (S, float, float, uint)-Funktion'
ms.assetid: 2474ECF6-DA85-406F-8212-D71AD90730FD
keywords:
- Gathercmpred-Funktion HLSL
topic_type:
- apiref
api_name:
- GatherCmpRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b64c32a5525faf3484715871b4fc0c4fb6470886
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352648"
---
# <a name="texturecubearraygathercmpredsfloatfloatuint-function"></a><span data-ttu-id="1b883-105">Texturecubearray:: gathercmpred (S, float, float, uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="1b883-105">TextureCubeArray::GatherCmpRed(S,float,float,uint) function</span></span>

<span data-ttu-id="1b883-106">Für vier Texel-Werte, die in einem bilinearen Filter Vorgang verwendet werden, gibt einen Vergleich der roten Komponente mit einem Vergleichswert zusammen mit dem Status der Kachel Zuordnung zurück.</span><span class="sxs-lookup"><span data-stu-id="1b883-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b883-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b883-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpRed(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="1b883-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b883-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b883-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b883-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b883-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="1b883-110">Type: **SamplerState**</span></span>

<span data-ttu-id="1b883-111">Der null basierte samplerindex.</span><span class="sxs-lookup"><span data-stu-id="1b883-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="1b883-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b883-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b883-113">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="1b883-113">Type: **float**</span></span>

<span data-ttu-id="1b883-114">Die Beispiel Koordinaten (u, v).</span><span class="sxs-lookup"><span data-stu-id="1b883-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="1b883-115">*CompareValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b883-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b883-116">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="1b883-116">Type: **float**</span></span>

<span data-ttu-id="1b883-117">Ein Wert, der jeweils mit jedem Stichproben Wert verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="1b883-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="1b883-118">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1b883-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b883-119">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="1b883-119">Type: **uint**</span></span>

<span data-ttu-id="1b883-120">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="1b883-120">The status of the operation.</span></span> <span data-ttu-id="1b883-121">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="1b883-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="1b883-122">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="1b883-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="1b883-123">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="1b883-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b883-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1b883-124">Return value</span></span>

<span data-ttu-id="1b883-125">Type: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="1b883-125">Type: **TemplateType**</span></span>

<span data-ttu-id="1b883-126">Ein vier komponentenwert, dessen Typ mit dem Vorlagentyp identisch ist.</span><span class="sxs-lookup"><span data-stu-id="1b883-126">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b883-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1b883-127">Remarks</span></span>

<span data-ttu-id="1b883-128">Die Textur Beispiele können für bilineare Interpolationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1b883-128">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="1b883-129">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="1b883-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="1b883-130">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="1b883-130">Vertex</span></span> | <span data-ttu-id="1b883-131">Hülle</span><span class="sxs-lookup"><span data-stu-id="1b883-131">Hull</span></span> | <span data-ttu-id="1b883-132">Domain</span><span class="sxs-lookup"><span data-stu-id="1b883-132">Domain</span></span> | <span data-ttu-id="1b883-133">Geometrie</span><span class="sxs-lookup"><span data-stu-id="1b883-133">Geometry</span></span> | <span data-ttu-id="1b883-134">Pixel</span><span class="sxs-lookup"><span data-stu-id="1b883-134">Pixel</span></span> | <span data-ttu-id="1b883-135">Compute</span><span class="sxs-lookup"><span data-stu-id="1b883-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="1b883-136">x</span><span class="sxs-lookup"><span data-stu-id="1b883-136">x</span></span>      | <span data-ttu-id="1b883-137">x</span><span class="sxs-lookup"><span data-stu-id="1b883-137">x</span></span>    | <span data-ttu-id="1b883-138">x</span><span class="sxs-lookup"><span data-stu-id="1b883-138">x</span></span>      | <span data-ttu-id="1b883-139">x</span><span class="sxs-lookup"><span data-stu-id="1b883-139">x</span></span>        | <span data-ttu-id="1b883-140">x</span><span class="sxs-lookup"><span data-stu-id="1b883-140">x</span></span>     | <span data-ttu-id="1b883-141">x</span><span class="sxs-lookup"><span data-stu-id="1b883-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="1b883-142">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1b883-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b883-143">Gathercmpred-Methoden</span><span class="sxs-lookup"><span data-stu-id="1b883-143">GatherCmpRed methods</span></span>](texturecubearray-gathercmpred.md)
</dt> <dt>

[<span data-ttu-id="1b883-144">**Texturecubearray**</span><span class="sxs-lookup"><span data-stu-id="1b883-144">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
