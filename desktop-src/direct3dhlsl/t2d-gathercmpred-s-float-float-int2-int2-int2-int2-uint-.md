---
title: 'Texture2D:: gathercmpred (S, float, float, int2, int2, int2, int2, uint)-Funktion'
description: 'Für vier Texel-Werte, die in einem bilinearen Filter Vorgang verwendet werden, gibt einen Vergleich der roten Komponente mit einem Vergleichswert zusammen mit dem Status der Kachel Zuordnung zurück. | Texture2D:: gathercmpred (S, float, float, int2, int2, int2, int2, uint)-Funktion'
ms.assetid: 69B1F8FF-CE29-49DD-B756-3308E11D866D
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
ms.openlocfilehash: 2d872623d7dcc8ea599e3c790493f2e1a8596b91
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995382"
---
# <a name="texture2dgathercmpredsfloatfloatint2int2int2int2uint-function"></a><span data-ttu-id="482bd-105">Texture2D:: gathercmpred (S, float, float, int2, int2, int2, int2, uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="482bd-105">Texture2D::GatherCmpRed(S,float,float,int2,int2,int2,int2,uint) function</span></span>

<span data-ttu-id="482bd-106">Für vier Texel-Werte, die in einem bilinearen Filter Vorgang verwendet werden, gibt einen Vergleich der roten Komponente mit einem Vergleichswert zusammen mit dem Status der Kachel Zuordnung zurück.</span><span class="sxs-lookup"><span data-stu-id="482bd-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="482bd-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="482bd-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpRed(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int2         Offset1,
  in  int2         Offset2,
  in  int2         Offset3,
  in  int2         Offset4,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="482bd-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="482bd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="482bd-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="482bd-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="482bd-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="482bd-110">Type: **SamplerState**</span></span>

<span data-ttu-id="482bd-111">Der null basierte samplerindex.</span><span class="sxs-lookup"><span data-stu-id="482bd-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="482bd-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="482bd-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="482bd-113">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="482bd-113">Type: **float**</span></span>

<span data-ttu-id="482bd-114">Die Beispiel Koordinaten (u, v).</span><span class="sxs-lookup"><span data-stu-id="482bd-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="482bd-115">*CompareValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="482bd-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="482bd-116">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="482bd-116">Type: **float**</span></span>

<span data-ttu-id="482bd-117">Ein Wert, der jeweils mit jedem Stichproben Wert verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="482bd-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="482bd-118">*Offset1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="482bd-118">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="482bd-119">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="482bd-119">Type: **int2**</span></span>

<span data-ttu-id="482bd-120">Die erste Offset-Komponente, die vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="482bd-120">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="482bd-121">*Offset2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="482bd-121">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="482bd-122">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="482bd-122">Type: **int2**</span></span>

<span data-ttu-id="482bd-123">Die zweite Offset Komponente, die vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="482bd-123">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="482bd-124">*Offset3* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="482bd-124">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="482bd-125">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="482bd-125">Type: **int2**</span></span>

<span data-ttu-id="482bd-126">Die dritte Offset Komponente, die vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="482bd-126">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="482bd-127">*Offset4* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="482bd-127">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="482bd-128">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="482bd-128">Type: **int2**</span></span>

<span data-ttu-id="482bd-129">Die vierte Offset-Komponente, die vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="482bd-129">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="482bd-130">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="482bd-130">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="482bd-131">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="482bd-131">Type: **uint**</span></span>

<span data-ttu-id="482bd-132">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="482bd-132">The status of the operation.</span></span> <span data-ttu-id="482bd-133">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="482bd-133">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="482bd-134">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="482bd-134">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="482bd-135">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="482bd-135">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="482bd-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="482bd-136">Return value</span></span>

<span data-ttu-id="482bd-137">Type: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="482bd-137">Type: **TemplateType**</span></span>

<span data-ttu-id="482bd-138">Ein vier komponentenwert, dessen Typ mit dem Vorlagentyp identisch ist.</span><span class="sxs-lookup"><span data-stu-id="482bd-138">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="482bd-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="482bd-139">Remarks</span></span>

<span data-ttu-id="482bd-140">Die Textur Beispiele können für bilineare Interpolationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="482bd-140">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="482bd-141">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="482bd-141">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="482bd-142">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="482bd-142">Vertex</span></span> | <span data-ttu-id="482bd-143">Hülle</span><span class="sxs-lookup"><span data-stu-id="482bd-143">Hull</span></span> | <span data-ttu-id="482bd-144">Domain</span><span class="sxs-lookup"><span data-stu-id="482bd-144">Domain</span></span> | <span data-ttu-id="482bd-145">Geometrie</span><span class="sxs-lookup"><span data-stu-id="482bd-145">Geometry</span></span> | <span data-ttu-id="482bd-146">Pixel</span><span class="sxs-lookup"><span data-stu-id="482bd-146">Pixel</span></span> | <span data-ttu-id="482bd-147">Compute</span><span class="sxs-lookup"><span data-stu-id="482bd-147">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="482bd-148">x</span><span class="sxs-lookup"><span data-stu-id="482bd-148">x</span></span>      | <span data-ttu-id="482bd-149">x</span><span class="sxs-lookup"><span data-stu-id="482bd-149">x</span></span>    | <span data-ttu-id="482bd-150">x</span><span class="sxs-lookup"><span data-stu-id="482bd-150">x</span></span>      | <span data-ttu-id="482bd-151">x</span><span class="sxs-lookup"><span data-stu-id="482bd-151">x</span></span>        | <span data-ttu-id="482bd-152">x</span><span class="sxs-lookup"><span data-stu-id="482bd-152">x</span></span>     | <span data-ttu-id="482bd-153">x</span><span class="sxs-lookup"><span data-stu-id="482bd-153">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="482bd-154">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="482bd-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="482bd-155">Gathercmpred-Methoden</span><span class="sxs-lookup"><span data-stu-id="482bd-155">GatherCmpRed methods</span></span>](texture2d-gathercmpred.md)
</dt> </dl>

 

 
