---
title: 'Texture2DArray:: gathergreen (S, float, int, uint)-Funktion'
description: 'Gibt die grünen Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang zusammen mit dem Status der Kachel Zuordnung verwendet werden. | Texture2DArray:: gathergreen (S, float, int, uint)-Funktion'
ms.assetid: 90BEB8B3-F851-469B-B55A-E51CB8463CC8
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
ms.openlocfilehash: 3f34470e589ac2d8155124d51813213869bbdfd6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981952"
---
# <a name="texture2darraygathergreensfloatintuint-function"></a><span data-ttu-id="c8d71-105">Texture2DArray:: gathergreen (S, float, int, uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="c8d71-105">Texture2DArray::GatherGreen(S,float,int,uint) function</span></span>

<span data-ttu-id="c8d71-106">Gibt die grünen Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang zusammen mit dem Status der Kachel Zuordnung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c8d71-106">Returns the green components of the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8d71-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8d71-107">Syntax</span></span>


``` syntax
TemplateType GatherGreen(
  in  SamplerState S,
  in  float        Location,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="c8d71-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8d71-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8d71-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8d71-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8d71-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="c8d71-110">Type: **SamplerState**</span></span>

<span data-ttu-id="c8d71-111">Der null basierte samplerindex.</span><span class="sxs-lookup"><span data-stu-id="c8d71-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="c8d71-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8d71-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8d71-113">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="c8d71-113">Type: **float**</span></span>

<span data-ttu-id="c8d71-114">Die Beispiel Koordinaten (u, v).</span><span class="sxs-lookup"><span data-stu-id="c8d71-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="c8d71-115">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8d71-115">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8d71-116">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="c8d71-116">Type: **int**</span></span>

<span data-ttu-id="c8d71-117">Der Offset, der vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="c8d71-117">The offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="c8d71-118">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c8d71-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8d71-119">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="c8d71-119">Type: **uint**</span></span>

<span data-ttu-id="c8d71-120">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="c8d71-120">The status of the operation.</span></span> <span data-ttu-id="c8d71-121">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="c8d71-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="c8d71-122">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="c8d71-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="c8d71-123">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="c8d71-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8d71-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c8d71-124">Return value</span></span>

<span data-ttu-id="c8d71-125">Type: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="c8d71-125">Type: **TemplateType**</span></span>

<span data-ttu-id="c8d71-126">Ein vier komponentenwert, dessen Typ mit dem Vorlagentyp identisch ist.</span><span class="sxs-lookup"><span data-stu-id="c8d71-126">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8d71-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c8d71-127">Remarks</span></span>

<span data-ttu-id="c8d71-128">Die Textur Beispiele können für bilineare Interpolationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c8d71-128">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="c8d71-129">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="c8d71-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="c8d71-130">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="c8d71-130">Vertex</span></span> | <span data-ttu-id="c8d71-131">Hülle</span><span class="sxs-lookup"><span data-stu-id="c8d71-131">Hull</span></span> | <span data-ttu-id="c8d71-132">Domain</span><span class="sxs-lookup"><span data-stu-id="c8d71-132">Domain</span></span> | <span data-ttu-id="c8d71-133">Geometrie</span><span class="sxs-lookup"><span data-stu-id="c8d71-133">Geometry</span></span> | <span data-ttu-id="c8d71-134">Pixel</span><span class="sxs-lookup"><span data-stu-id="c8d71-134">Pixel</span></span> | <span data-ttu-id="c8d71-135">Compute</span><span class="sxs-lookup"><span data-stu-id="c8d71-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="c8d71-136">x</span><span class="sxs-lookup"><span data-stu-id="c8d71-136">x</span></span>      | <span data-ttu-id="c8d71-137">x</span><span class="sxs-lookup"><span data-stu-id="c8d71-137">x</span></span>    | <span data-ttu-id="c8d71-138">x</span><span class="sxs-lookup"><span data-stu-id="c8d71-138">x</span></span>      | <span data-ttu-id="c8d71-139">x</span><span class="sxs-lookup"><span data-stu-id="c8d71-139">x</span></span>        | <span data-ttu-id="c8d71-140">x</span><span class="sxs-lookup"><span data-stu-id="c8d71-140">x</span></span>     | <span data-ttu-id="c8d71-141">x</span><span class="sxs-lookup"><span data-stu-id="c8d71-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="c8d71-142">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c8d71-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8d71-143">Gathergreen-Methoden</span><span class="sxs-lookup"><span data-stu-id="c8d71-143">GatherGreen methods</span></span>](texture2darray-gathergreen.md)
</dt> </dl>

 

 
