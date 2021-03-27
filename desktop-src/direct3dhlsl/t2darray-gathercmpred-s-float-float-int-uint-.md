---
title: 'Texture2DArray:: gathercmpred (S, float, float, int, uint)-Funktion'
description: 'Für vier Texel-Werte, die in einem bilinearen Filter Vorgang verwendet werden, gibt einen Vergleich der roten Komponente mit einem Vergleichswert zusammen mit dem Status der Kachel Zuordnung zurück. | Texture2DArray:: gathercmpred (S, float, float, int, uint)-Funktion'
ms.assetid: 83974A85-26CB-4724-A60F-64F214800723
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
ms.openlocfilehash: 79743d4d2b30049a580309aa79bf6b3d79c73d3f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981953"
---
# <a name="texture2darraygathercmpredsfloatfloatintuint-function"></a><span data-ttu-id="e10d1-105">Texture2DArray:: gathercmpred (S, float, float, int, uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="e10d1-105">Texture2DArray::GatherCmpRed(S,float,float,int,uint) function</span></span>

<span data-ttu-id="e10d1-106">Für vier Texel-Werte, die in einem bilinearen Filter Vorgang verwendet werden, gibt einen Vergleich der roten Komponente mit einem Vergleichswert zusammen mit dem Status der Kachel Zuordnung zurück.</span><span class="sxs-lookup"><span data-stu-id="e10d1-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="e10d1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e10d1-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpRed(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="e10d1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e10d1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e10d1-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e10d1-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e10d1-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="e10d1-110">Type: **SamplerState**</span></span>

<span data-ttu-id="e10d1-111">Der null basierte samplerindex.</span><span class="sxs-lookup"><span data-stu-id="e10d1-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="e10d1-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e10d1-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e10d1-113">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="e10d1-113">Type: **float**</span></span>

<span data-ttu-id="e10d1-114">Die Beispiel Koordinaten (u, v).</span><span class="sxs-lookup"><span data-stu-id="e10d1-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="e10d1-115">*CompareValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e10d1-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e10d1-116">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="e10d1-116">Type: **float**</span></span>

<span data-ttu-id="e10d1-117">Ein Wert, der jeweils mit jedem Stichproben Wert verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e10d1-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="e10d1-118">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e10d1-118">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e10d1-119">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="e10d1-119">Type: **int**</span></span>

<span data-ttu-id="e10d1-120">Der Offset, der vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="e10d1-120">The offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="e10d1-121">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e10d1-121">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e10d1-122">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="e10d1-122">Type: **uint**</span></span>

<span data-ttu-id="e10d1-123">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="e10d1-123">The status of the operation.</span></span> <span data-ttu-id="e10d1-124">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="e10d1-124">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="e10d1-125">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="e10d1-125">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="e10d1-126">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="e10d1-126">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e10d1-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e10d1-127">Return value</span></span>

<span data-ttu-id="e10d1-128">Type: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="e10d1-128">Type: **TemplateType**</span></span>

<span data-ttu-id="e10d1-129">Ein vier komponentenwert, dessen Typ mit dem Vorlagentyp identisch ist.</span><span class="sxs-lookup"><span data-stu-id="e10d1-129">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="e10d1-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e10d1-130">Remarks</span></span>

<span data-ttu-id="e10d1-131">Die Textur Beispiele können für bilineare Interpolationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e10d1-131">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="e10d1-132">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="e10d1-132">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="e10d1-133">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="e10d1-133">Vertex</span></span> | <span data-ttu-id="e10d1-134">Hülle</span><span class="sxs-lookup"><span data-stu-id="e10d1-134">Hull</span></span> | <span data-ttu-id="e10d1-135">Domain</span><span class="sxs-lookup"><span data-stu-id="e10d1-135">Domain</span></span> | <span data-ttu-id="e10d1-136">Geometrie</span><span class="sxs-lookup"><span data-stu-id="e10d1-136">Geometry</span></span> | <span data-ttu-id="e10d1-137">Pixel</span><span class="sxs-lookup"><span data-stu-id="e10d1-137">Pixel</span></span> | <span data-ttu-id="e10d1-138">Compute</span><span class="sxs-lookup"><span data-stu-id="e10d1-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e10d1-139">x</span><span class="sxs-lookup"><span data-stu-id="e10d1-139">x</span></span>      | <span data-ttu-id="e10d1-140">x</span><span class="sxs-lookup"><span data-stu-id="e10d1-140">x</span></span>    | <span data-ttu-id="e10d1-141">x</span><span class="sxs-lookup"><span data-stu-id="e10d1-141">x</span></span>      | <span data-ttu-id="e10d1-142">x</span><span class="sxs-lookup"><span data-stu-id="e10d1-142">x</span></span>        | <span data-ttu-id="e10d1-143">x</span><span class="sxs-lookup"><span data-stu-id="e10d1-143">x</span></span>     | <span data-ttu-id="e10d1-144">x</span><span class="sxs-lookup"><span data-stu-id="e10d1-144">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="e10d1-145">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e10d1-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e10d1-146">Gathercmpred-Methoden</span><span class="sxs-lookup"><span data-stu-id="e10d1-146">GatherCmpRed methods</span></span>](texture2darray-gathercmpred.md)
</dt> </dl>

 

 
