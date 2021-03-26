---
title: 'Texture2DArray:: gathercmpalpha (S, float, float, int, uint)-Funktion'
description: 'Für vier Texel-Werte, die in einem bilinearen Filter Vorgang verwendet werden, gibt einen Vergleich der Alpha Komponente mit einem Vergleichswert zusammen mit dem Status der Kachel Zuordnung zurück. | Texture2DArray:: gathercmpalpha (S, float, float, int, uint)-Funktion'
ms.assetid: DCCF7F40-8A0D-47B8-910A-508382D3AE3F
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
ms.openlocfilehash: afd427c5af46f333deb0b05de551f8081d9bd9c8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352649"
---
# <a name="texture2darraygathercmpalphasfloatfloatintuint-function"></a><span data-ttu-id="658d9-105">Texture2DArray:: gathercmpalpha (S, float, float, int, uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="658d9-105">Texture2DArray::GatherCmpAlpha(S,float,float,int,uint) function</span></span>

<span data-ttu-id="658d9-106">Für vier Texel-Werte, die in einem bilinearen Filter Vorgang verwendet werden, gibt einen Vergleich der Alpha Komponente mit einem Vergleichswert zusammen mit dem Status der Kachel Zuordnung zurück.</span><span class="sxs-lookup"><span data-stu-id="658d9-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="658d9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="658d9-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpAlpha(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="658d9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="658d9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="658d9-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="658d9-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="658d9-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="658d9-110">Type: **SamplerState**</span></span>

<span data-ttu-id="658d9-111">Der null basierte samplerindex.</span><span class="sxs-lookup"><span data-stu-id="658d9-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="658d9-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="658d9-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="658d9-113">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="658d9-113">Type: **float**</span></span>

<span data-ttu-id="658d9-114">Die Beispiel Koordinaten (u, v).</span><span class="sxs-lookup"><span data-stu-id="658d9-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="658d9-115">*CompareValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="658d9-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="658d9-116">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="658d9-116">Type: **float**</span></span>

<span data-ttu-id="658d9-117">Ein Wert, der jeweils mit jedem Stichproben Wert verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="658d9-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="658d9-118">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="658d9-118">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="658d9-119">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="658d9-119">Type: **int**</span></span>

<span data-ttu-id="658d9-120">Der Offset, der vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="658d9-120">The offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="658d9-121">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="658d9-121">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="658d9-122">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="658d9-122">Type: **uint**</span></span>

<span data-ttu-id="658d9-123">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="658d9-123">The status of the operation.</span></span> <span data-ttu-id="658d9-124">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="658d9-124">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="658d9-125">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="658d9-125">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="658d9-126">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="658d9-126">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="658d9-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="658d9-127">Return value</span></span>

<span data-ttu-id="658d9-128">Type: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="658d9-128">Type: **TemplateType**</span></span>

<span data-ttu-id="658d9-129">Ein vier komponentenwert, dessen Typ mit dem Vorlagentyp identisch ist.</span><span class="sxs-lookup"><span data-stu-id="658d9-129">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="658d9-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="658d9-130">Remarks</span></span>

<span data-ttu-id="658d9-131">Die Textur Beispiele können für bilineare Interpolationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="658d9-131">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="658d9-132">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="658d9-132">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="658d9-133">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="658d9-133">Vertex</span></span> | <span data-ttu-id="658d9-134">Hülle</span><span class="sxs-lookup"><span data-stu-id="658d9-134">Hull</span></span> | <span data-ttu-id="658d9-135">Domain</span><span class="sxs-lookup"><span data-stu-id="658d9-135">Domain</span></span> | <span data-ttu-id="658d9-136">Geometrie</span><span class="sxs-lookup"><span data-stu-id="658d9-136">Geometry</span></span> | <span data-ttu-id="658d9-137">Pixel</span><span class="sxs-lookup"><span data-stu-id="658d9-137">Pixel</span></span> | <span data-ttu-id="658d9-138">Compute</span><span class="sxs-lookup"><span data-stu-id="658d9-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="658d9-139">x</span><span class="sxs-lookup"><span data-stu-id="658d9-139">x</span></span>      | <span data-ttu-id="658d9-140">x</span><span class="sxs-lookup"><span data-stu-id="658d9-140">x</span></span>    | <span data-ttu-id="658d9-141">x</span><span class="sxs-lookup"><span data-stu-id="658d9-141">x</span></span>      | <span data-ttu-id="658d9-142">x</span><span class="sxs-lookup"><span data-stu-id="658d9-142">x</span></span>        | <span data-ttu-id="658d9-143">x</span><span class="sxs-lookup"><span data-stu-id="658d9-143">x</span></span>     | <span data-ttu-id="658d9-144">x</span><span class="sxs-lookup"><span data-stu-id="658d9-144">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="658d9-145">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="658d9-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="658d9-146">Gathercmpalpha-Methoden</span><span class="sxs-lookup"><span data-stu-id="658d9-146">GatherCmpAlpha methods</span></span>](texture2darray-gathercmpalpha.md)
</dt> </dl>

 

 
