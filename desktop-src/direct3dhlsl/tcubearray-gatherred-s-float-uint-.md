---
title: 'Texturecubearray:: gatherred (S, float, uint)-Funktion'
description: 'Gibt die roten Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang zusammen mit dem Status der Kachel Zuordnung verwendet werden. | Texturecubearray:: gatherred (S, float, uint)-Funktion'
ms.assetid: 9776A4B5-6DDB-4B9F-96CD-F97B8908B057
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
ms.openlocfilehash: 90c6c69b8598222139a39752aefc39a0a125df2a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352639"
---
# <a name="texturecubearraygatherredsfloatuint-function"></a><span data-ttu-id="b7933-105">Texturecubearray:: gatherred (S, float, uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="b7933-105">TextureCubeArray::GatherRed(S,float,uint) function</span></span>

<span data-ttu-id="b7933-106">Gibt die roten Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang zusammen mit dem Status der Kachel Zuordnung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b7933-106">Returns the red components of the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7933-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7933-107">Syntax</span></span>


``` syntax
TemplateType GatherRed(
  in  SamplerState S,
  in  float        Location,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="b7933-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7933-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7933-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b7933-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7933-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="b7933-110">Type: **SamplerState**</span></span>

<span data-ttu-id="b7933-111">Der null basierte samplerindex.</span><span class="sxs-lookup"><span data-stu-id="b7933-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="b7933-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b7933-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7933-113">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="b7933-113">Type: **float**</span></span>

<span data-ttu-id="b7933-114">Die Beispiel Koordinaten (u, v).</span><span class="sxs-lookup"><span data-stu-id="b7933-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="b7933-115">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b7933-115">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7933-116">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="b7933-116">Type: **uint**</span></span>

<span data-ttu-id="b7933-117">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="b7933-117">The status of the operation.</span></span> <span data-ttu-id="b7933-118">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="b7933-118">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="b7933-119">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="b7933-119">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="b7933-120">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="b7933-120">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7933-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b7933-121">Return value</span></span>

<span data-ttu-id="b7933-122">Type: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="b7933-122">Type: **TemplateType**</span></span>

<span data-ttu-id="b7933-123">Ein vier komponentenwert, dessen Typ mit dem Vorlagentyp identisch ist.</span><span class="sxs-lookup"><span data-stu-id="b7933-123">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7933-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b7933-124">Remarks</span></span>

<span data-ttu-id="b7933-125">Die Textur Beispiele können für bilineare Interpolationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b7933-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="b7933-126">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="b7933-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="b7933-127">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="b7933-127">Vertex</span></span> | <span data-ttu-id="b7933-128">Hülle</span><span class="sxs-lookup"><span data-stu-id="b7933-128">Hull</span></span> | <span data-ttu-id="b7933-129">Domain</span><span class="sxs-lookup"><span data-stu-id="b7933-129">Domain</span></span> | <span data-ttu-id="b7933-130">Geometrie</span><span class="sxs-lookup"><span data-stu-id="b7933-130">Geometry</span></span> | <span data-ttu-id="b7933-131">Pixel</span><span class="sxs-lookup"><span data-stu-id="b7933-131">Pixel</span></span> | <span data-ttu-id="b7933-132">Compute</span><span class="sxs-lookup"><span data-stu-id="b7933-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="b7933-133">x</span><span class="sxs-lookup"><span data-stu-id="b7933-133">x</span></span>      | <span data-ttu-id="b7933-134">x</span><span class="sxs-lookup"><span data-stu-id="b7933-134">x</span></span>    | <span data-ttu-id="b7933-135">x</span><span class="sxs-lookup"><span data-stu-id="b7933-135">x</span></span>      | <span data-ttu-id="b7933-136">x</span><span class="sxs-lookup"><span data-stu-id="b7933-136">x</span></span>        | <span data-ttu-id="b7933-137">x</span><span class="sxs-lookup"><span data-stu-id="b7933-137">x</span></span>     | <span data-ttu-id="b7933-138">x</span><span class="sxs-lookup"><span data-stu-id="b7933-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b7933-139">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b7933-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7933-140">Gatherred-Methoden</span><span class="sxs-lookup"><span data-stu-id="b7933-140">GatherRed methods</span></span>](texturecubearray-gatherred.md)
</dt> <dt>

[<span data-ttu-id="b7933-141">**Texturecubearray**</span><span class="sxs-lookup"><span data-stu-id="b7933-141">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
