---
title: 'Texture2DArray:: gathercmp (S, float, float, int, uint)-Funktion'
description: 'Bei vier textexwerten, die in einem bilinearen Filter Vorgang verwendet werden, wird der Vergleich mit einem Vergleichswert zusammen mit dem Status der Kachel Zuordnung zurückgegeben. | Texture2DArray:: gathercmp (S, float, float, int, uint)-Funktion'
ms.assetid: E68619B2-6AB0-4C57-9604-7759FD987446
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
ms.openlocfilehash: a9ac68e6f7701ddfccf0c58321a526f33c2ceeea
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981377"
---
# <a name="texture2darraygathercmpsfloatfloatintuint-function"></a><span data-ttu-id="ae3ad-105">Texture2DArray:: gathercmp (S, float, float, int, uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="ae3ad-105">Texture2DArray::GatherCmp(S,float,float,int,uint) function</span></span>

<span data-ttu-id="ae3ad-106">Bei vier textexwerten, die in einem bilinearen Filter Vorgang verwendet werden, wird der Vergleich mit einem Vergleichswert zusammen mit dem Status der Kachel Zuordnung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ae3ad-106">For four texel values that would be used in a bi-linear filtering operation, returns their comparison against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae3ad-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae3ad-107">Syntax</span></span>


``` syntax
TemplateType GatherCmp(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="ae3ad-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae3ad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae3ad-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae3ad-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae3ad-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="ae3ad-110">Type: **SamplerState**</span></span>

<span data-ttu-id="ae3ad-111">Der null basierte samplerindex.</span><span class="sxs-lookup"><span data-stu-id="ae3ad-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="ae3ad-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae3ad-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae3ad-113">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="ae3ad-113">Type: **float**</span></span>

<span data-ttu-id="ae3ad-114">Die Beispiel Koordinaten (u, v).</span><span class="sxs-lookup"><span data-stu-id="ae3ad-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="ae3ad-115">*CompareValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae3ad-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae3ad-116">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="ae3ad-116">Type: **float**</span></span>

<span data-ttu-id="ae3ad-117">Ein Wert, der jeweils mit jedem Stichproben Wert verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ae3ad-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="ae3ad-118">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae3ad-118">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae3ad-119">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="ae3ad-119">Type: **int**</span></span>

<span data-ttu-id="ae3ad-120">Der Offset, der vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="ae3ad-120">The offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="ae3ad-121">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ae3ad-121">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae3ad-122">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="ae3ad-122">Type: **uint**</span></span>

<span data-ttu-id="ae3ad-123">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="ae3ad-123">The status of the operation.</span></span> <span data-ttu-id="ae3ad-124">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="ae3ad-124">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="ae3ad-125">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="ae3ad-125">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="ae3ad-126">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="ae3ad-126">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae3ad-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ae3ad-127">Return value</span></span>

<span data-ttu-id="ae3ad-128">Type: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="ae3ad-128">Type: **TemplateType**</span></span>

<span data-ttu-id="ae3ad-129">Ein vier komponentenwert, dessen Typ mit dem Vorlagentyp identisch ist.</span><span class="sxs-lookup"><span data-stu-id="ae3ad-129">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae3ad-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ae3ad-130">Remarks</span></span>

<span data-ttu-id="ae3ad-131">Die Textur Beispiele können für bilineare Interpolationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ae3ad-131">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="ae3ad-132">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="ae3ad-132">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="ae3ad-133">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="ae3ad-133">Vertex</span></span> | <span data-ttu-id="ae3ad-134">Hülle</span><span class="sxs-lookup"><span data-stu-id="ae3ad-134">Hull</span></span> | <span data-ttu-id="ae3ad-135">Domain</span><span class="sxs-lookup"><span data-stu-id="ae3ad-135">Domain</span></span> | <span data-ttu-id="ae3ad-136">Geometrie</span><span class="sxs-lookup"><span data-stu-id="ae3ad-136">Geometry</span></span> | <span data-ttu-id="ae3ad-137">Pixel</span><span class="sxs-lookup"><span data-stu-id="ae3ad-137">Pixel</span></span> | <span data-ttu-id="ae3ad-138">Compute</span><span class="sxs-lookup"><span data-stu-id="ae3ad-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ae3ad-139">x</span><span class="sxs-lookup"><span data-stu-id="ae3ad-139">x</span></span>      | <span data-ttu-id="ae3ad-140">x</span><span class="sxs-lookup"><span data-stu-id="ae3ad-140">x</span></span>    | <span data-ttu-id="ae3ad-141">x</span><span class="sxs-lookup"><span data-stu-id="ae3ad-141">x</span></span>      | <span data-ttu-id="ae3ad-142">x</span><span class="sxs-lookup"><span data-stu-id="ae3ad-142">x</span></span>        | <span data-ttu-id="ae3ad-143">x</span><span class="sxs-lookup"><span data-stu-id="ae3ad-143">x</span></span>     | <span data-ttu-id="ae3ad-144">x</span><span class="sxs-lookup"><span data-stu-id="ae3ad-144">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ae3ad-145">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ae3ad-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae3ad-146">Gathercmp-Methoden</span><span class="sxs-lookup"><span data-stu-id="ae3ad-146">GatherCmp methods</span></span>](texture2darray-gathercmp.md)
</dt> </dl>

 

 
