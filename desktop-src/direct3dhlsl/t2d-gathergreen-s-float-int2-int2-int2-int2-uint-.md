---
title: 'Texture2D:: gathergreen (S, float, int2, int2, int2, int2, uint)-Funktion'
description: 'Gibt die grünen Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang zusammen mit dem Status der Kachel Zuordnung verwendet werden. | Texture2D:: gathergreen (S, float, int2, int2, int2, int2, uint)-Funktion'
ms.assetid: 61AAC31F-28BC-4DF8-A416-CBAD150829D8
keywords:
- Gathergreen-Funktion HLSL
topic_type:
- apiref
api_name:
- GatherGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e98bc8b34514cf2ac54e7fd96916c66c9f2a53d1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981744"
---
# <a name="texture2dgathergreensfloatint2int2int2int2uint-function"></a><span data-ttu-id="4cc4b-105">Texture2D:: gathergreen (S, float, int2, int2, int2, int2, uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="4cc4b-105">Texture2D::GatherGreen(S,float,int2,int2,int2,int2,uint) function</span></span>

<span data-ttu-id="4cc4b-106">Gibt die grünen Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang zusammen mit dem Status der Kachel Zuordnung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4cc4b-106">Returns the green components of the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cc4b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4cc4b-107">Syntax</span></span>


``` syntax
TemplateType GatherGreen(
  in  SamplerState S,
  in  float        Location,
  in  int2         Offset1,
  in  int2         Offset2,
  in  int2         Offset3,
  in  int2         Offset4,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="4cc4b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4cc4b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cc4b-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4cc4b-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cc4b-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="4cc4b-110">Type: **SamplerState**</span></span>

<span data-ttu-id="4cc4b-111">Der null basierte samplerindex.</span><span class="sxs-lookup"><span data-stu-id="4cc4b-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="4cc4b-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4cc4b-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cc4b-113">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="4cc4b-113">Type: **float**</span></span>

<span data-ttu-id="4cc4b-114">Die Beispiel Koordinaten (u, v).</span><span class="sxs-lookup"><span data-stu-id="4cc4b-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="4cc4b-115">*Offset1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4cc4b-115">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cc4b-116">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="4cc4b-116">Type: **int2**</span></span>

<span data-ttu-id="4cc4b-117">Die erste Offset-Komponente, die vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="4cc4b-117">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="4cc4b-118">*Offset2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4cc4b-118">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cc4b-119">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="4cc4b-119">Type: **int2**</span></span>

<span data-ttu-id="4cc4b-120">Die zweite Offset Komponente, die vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="4cc4b-120">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="4cc4b-121">*Offset3* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4cc4b-121">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cc4b-122">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="4cc4b-122">Type: **int2**</span></span>

<span data-ttu-id="4cc4b-123">Die dritte Offset Komponente, die vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="4cc4b-123">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="4cc4b-124">*Offset4* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4cc4b-124">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cc4b-125">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="4cc4b-125">Type: **int2**</span></span>

<span data-ttu-id="4cc4b-126">Die vierte Offset-Komponente, die vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="4cc4b-126">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="4cc4b-127">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4cc4b-127">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4cc4b-128">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="4cc4b-128">Type: **uint**</span></span>

<span data-ttu-id="4cc4b-129">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="4cc4b-129">The status of the operation.</span></span> <span data-ttu-id="4cc4b-130">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="4cc4b-130">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="4cc4b-131">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="4cc4b-131">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="4cc4b-132">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="4cc4b-132">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cc4b-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4cc4b-133">Return value</span></span>

<span data-ttu-id="4cc4b-134">Type: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="4cc4b-134">Type: **TemplateType**</span></span>

<span data-ttu-id="4cc4b-135">Ein vier komponentenwert, dessen Typ mit dem Vorlagentyp identisch ist.</span><span class="sxs-lookup"><span data-stu-id="4cc4b-135">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cc4b-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4cc4b-136">Remarks</span></span>

<span data-ttu-id="4cc4b-137">Die Textur Beispiele können für bilineare Interpolationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4cc4b-137">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="4cc4b-138">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="4cc4b-138">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="4cc4b-139">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="4cc4b-139">Vertex</span></span> | <span data-ttu-id="4cc4b-140">Hülle</span><span class="sxs-lookup"><span data-stu-id="4cc4b-140">Hull</span></span> | <span data-ttu-id="4cc4b-141">Domain</span><span class="sxs-lookup"><span data-stu-id="4cc4b-141">Domain</span></span> | <span data-ttu-id="4cc4b-142">Geometrie</span><span class="sxs-lookup"><span data-stu-id="4cc4b-142">Geometry</span></span> | <span data-ttu-id="4cc4b-143">Pixel</span><span class="sxs-lookup"><span data-stu-id="4cc4b-143">Pixel</span></span> | <span data-ttu-id="4cc4b-144">Compute</span><span class="sxs-lookup"><span data-stu-id="4cc4b-144">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="4cc4b-145">x</span><span class="sxs-lookup"><span data-stu-id="4cc4b-145">x</span></span>      | <span data-ttu-id="4cc4b-146">x</span><span class="sxs-lookup"><span data-stu-id="4cc4b-146">x</span></span>    | <span data-ttu-id="4cc4b-147">x</span><span class="sxs-lookup"><span data-stu-id="4cc4b-147">x</span></span>      | <span data-ttu-id="4cc4b-148">x</span><span class="sxs-lookup"><span data-stu-id="4cc4b-148">x</span></span>        | <span data-ttu-id="4cc4b-149">x</span><span class="sxs-lookup"><span data-stu-id="4cc4b-149">x</span></span>     | <span data-ttu-id="4cc4b-150">x</span><span class="sxs-lookup"><span data-stu-id="4cc4b-150">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="4cc4b-151">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4cc4b-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cc4b-152">Gathergreen-Methoden</span><span class="sxs-lookup"><span data-stu-id="4cc4b-152">GatherGreen methods</span></span>](texture2d-gathergreen.md)
</dt> </dl>

 

 
