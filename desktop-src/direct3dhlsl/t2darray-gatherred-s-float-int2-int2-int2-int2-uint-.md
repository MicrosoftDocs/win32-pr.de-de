---
title: 'Texture2DArray:: gatherred (S, float, int2, int2, int2, int2, uint)-Funktion'
description: 'Gibt die roten Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang zusammen mit dem Status der Kachel Zuordnung verwendet werden. | Texture2DArray:: gatherred (S, float, int2, int2, int2, int2, uint)-Funktion'
ms.assetid: 9DD399A4-E6ED-499B-ACA3-28028C0AB271
keywords:
- Gatherrote Funktion HLSL
topic_type:
- apiref
api_name:
- GatherRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ce2ce0ab8b79a2335cc8e02d89751da3b30d856
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995406"
---
# <a name="texture2darraygatherredsfloatint2int2int2int2uint-function"></a><span data-ttu-id="13efe-105">Texture2DArray:: gatherred (S, float, int2, int2, int2, int2, uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="13efe-105">Texture2DArray::GatherRed(S,float,int2,int2,int2,int2,uint) function</span></span>

<span data-ttu-id="13efe-106">Gibt die roten Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang zusammen mit dem Status der Kachel Zuordnung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="13efe-106">Returns the red components of the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="13efe-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="13efe-107">Syntax</span></span>


``` syntax
TemplateType GatherRed(
  in  SamplerState S,
  in  float        Location,
  in  int2         Offset1,
  in  int2         Offset2,
  in  int2         Offset3,
  in  int2         Offset4,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="13efe-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="13efe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13efe-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="13efe-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13efe-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="13efe-110">Type: **SamplerState**</span></span>

<span data-ttu-id="13efe-111">Der null basierte samplerindex.</span><span class="sxs-lookup"><span data-stu-id="13efe-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="13efe-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="13efe-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13efe-113">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="13efe-113">Type: **float**</span></span>

<span data-ttu-id="13efe-114">Die Beispiel Koordinaten (u, v).</span><span class="sxs-lookup"><span data-stu-id="13efe-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="13efe-115">*Offset1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="13efe-115">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13efe-116">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="13efe-116">Type: **int2**</span></span>

<span data-ttu-id="13efe-117">Die erste Offset-Komponente, die vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="13efe-117">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="13efe-118">*Offset2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="13efe-118">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13efe-119">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="13efe-119">Type: **int2**</span></span>

<span data-ttu-id="13efe-120">Die zweite Offset Komponente, die vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="13efe-120">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="13efe-121">*Offset3* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="13efe-121">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13efe-122">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="13efe-122">Type: **int2**</span></span>

<span data-ttu-id="13efe-123">Die dritte Offset Komponente, die vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="13efe-123">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="13efe-124">*Offset4* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="13efe-124">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13efe-125">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="13efe-125">Type: **int2**</span></span>

<span data-ttu-id="13efe-126">Die vierte Offset-Komponente, die vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="13efe-126">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="13efe-127">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="13efe-127">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13efe-128">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="13efe-128">Type: **uint**</span></span>

<span data-ttu-id="13efe-129">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="13efe-129">The status of the operation.</span></span> <span data-ttu-id="13efe-130">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="13efe-130">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="13efe-131">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="13efe-131">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="13efe-132">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="13efe-132">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13efe-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="13efe-133">Return value</span></span>

<span data-ttu-id="13efe-134">Type: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="13efe-134">Type: **TemplateType**</span></span>

<span data-ttu-id="13efe-135">Ein vier komponentenwert, dessen Typ mit dem Vorlagentyp identisch ist.</span><span class="sxs-lookup"><span data-stu-id="13efe-135">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="13efe-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="13efe-136">Remarks</span></span>

<span data-ttu-id="13efe-137">Die Textur Beispiele können für bilineare Interpolationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="13efe-137">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="13efe-138">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="13efe-138">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="13efe-139">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="13efe-139">Vertex</span></span> | <span data-ttu-id="13efe-140">Hülle</span><span class="sxs-lookup"><span data-stu-id="13efe-140">Hull</span></span> | <span data-ttu-id="13efe-141">Domain</span><span class="sxs-lookup"><span data-stu-id="13efe-141">Domain</span></span> | <span data-ttu-id="13efe-142">Geometrie</span><span class="sxs-lookup"><span data-stu-id="13efe-142">Geometry</span></span> | <span data-ttu-id="13efe-143">Pixel</span><span class="sxs-lookup"><span data-stu-id="13efe-143">Pixel</span></span> | <span data-ttu-id="13efe-144">Compute</span><span class="sxs-lookup"><span data-stu-id="13efe-144">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="13efe-145">x</span><span class="sxs-lookup"><span data-stu-id="13efe-145">x</span></span>      | <span data-ttu-id="13efe-146">x</span><span class="sxs-lookup"><span data-stu-id="13efe-146">x</span></span>    | <span data-ttu-id="13efe-147">x</span><span class="sxs-lookup"><span data-stu-id="13efe-147">x</span></span>      | <span data-ttu-id="13efe-148">x</span><span class="sxs-lookup"><span data-stu-id="13efe-148">x</span></span>        | <span data-ttu-id="13efe-149">x</span><span class="sxs-lookup"><span data-stu-id="13efe-149">x</span></span>     | <span data-ttu-id="13efe-150">x</span><span class="sxs-lookup"><span data-stu-id="13efe-150">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="13efe-151">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="13efe-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13efe-152">Gatherred-Methoden</span><span class="sxs-lookup"><span data-stu-id="13efe-152">GatherRed methods</span></span>](texture2darray-gatherred.md)
</dt> </dl>

 

 
