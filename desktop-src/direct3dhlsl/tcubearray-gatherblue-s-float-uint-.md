---
title: 'Texturecubearray:: gatherblue (S, float, uint)-Funktion'
description: 'Gibt die blauen Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang zusammen mit dem Status der Kachel Zuordnung verwendet werden. | Texturecubearray:: gatherblue (S, float, uint)-Funktion'
ms.assetid: 85606EE7-9B05-439F-B525-A1CD42FE32F6
keywords:
- Gatherblue-Funktion HLSL
topic_type:
- apiref
api_name:
- GatherBlue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b96282bd57b6cbef248a7090ad4a297cd5a81740
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104393994"
---
# <a name="texturecubearraygatherbluesfloatuint-function"></a><span data-ttu-id="8f491-105">Texturecubearray:: gatherblue (S, float, uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="8f491-105">TextureCubeArray::GatherBlue(S,float,uint) function</span></span>

<span data-ttu-id="8f491-106">Gibt die blauen Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang zusammen mit dem Status der Kachel Zuordnung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8f491-106">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f491-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f491-107">Syntax</span></span>


``` syntax
TemplateType GatherBlue(
  in  SamplerState S,
  in  float        Location,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="8f491-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f491-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f491-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8f491-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f491-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="8f491-110">Type: **SamplerState**</span></span>

<span data-ttu-id="8f491-111">Der null basierte samplerindex.</span><span class="sxs-lookup"><span data-stu-id="8f491-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="8f491-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8f491-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f491-113">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="8f491-113">Type: **float**</span></span>

<span data-ttu-id="8f491-114">Die Beispiel Koordinaten (u, v).</span><span class="sxs-lookup"><span data-stu-id="8f491-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="8f491-115">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8f491-115">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f491-116">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="8f491-116">Type: **uint**</span></span>

<span data-ttu-id="8f491-117">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="8f491-117">The status of the operation.</span></span> <span data-ttu-id="8f491-118">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="8f491-118">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="8f491-119">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="8f491-119">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="8f491-120">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="8f491-120">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f491-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8f491-121">Return value</span></span>

<span data-ttu-id="8f491-122">Type: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="8f491-122">Type: **TemplateType**</span></span>

<span data-ttu-id="8f491-123">Ein vier komponentenwert, dessen Typ mit dem Vorlagentyp identisch ist.</span><span class="sxs-lookup"><span data-stu-id="8f491-123">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f491-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8f491-124">Remarks</span></span>

<span data-ttu-id="8f491-125">Die Textur Beispiele können für bilineare Interpolationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8f491-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="8f491-126">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="8f491-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="8f491-127">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="8f491-127">Vertex</span></span> | <span data-ttu-id="8f491-128">Hülle</span><span class="sxs-lookup"><span data-stu-id="8f491-128">Hull</span></span> | <span data-ttu-id="8f491-129">Domain</span><span class="sxs-lookup"><span data-stu-id="8f491-129">Domain</span></span> | <span data-ttu-id="8f491-130">Geometrie</span><span class="sxs-lookup"><span data-stu-id="8f491-130">Geometry</span></span> | <span data-ttu-id="8f491-131">Pixel</span><span class="sxs-lookup"><span data-stu-id="8f491-131">Pixel</span></span> | <span data-ttu-id="8f491-132">Compute</span><span class="sxs-lookup"><span data-stu-id="8f491-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="8f491-133">x</span><span class="sxs-lookup"><span data-stu-id="8f491-133">x</span></span>      | <span data-ttu-id="8f491-134">x</span><span class="sxs-lookup"><span data-stu-id="8f491-134">x</span></span>    | <span data-ttu-id="8f491-135">x</span><span class="sxs-lookup"><span data-stu-id="8f491-135">x</span></span>      | <span data-ttu-id="8f491-136">x</span><span class="sxs-lookup"><span data-stu-id="8f491-136">x</span></span>        | <span data-ttu-id="8f491-137">x</span><span class="sxs-lookup"><span data-stu-id="8f491-137">x</span></span>     | <span data-ttu-id="8f491-138">x</span><span class="sxs-lookup"><span data-stu-id="8f491-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="8f491-139">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8f491-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f491-140">Gatherblue-Methoden</span><span class="sxs-lookup"><span data-stu-id="8f491-140">GatherBlue methods</span></span>](texturecubearray-gatherblue.md)
</dt> <dt>

[<span data-ttu-id="8f491-141">**Texturecubearray**</span><span class="sxs-lookup"><span data-stu-id="8f491-141">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
