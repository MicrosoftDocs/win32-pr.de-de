---
title: 'Texturecubearray:: Gather (S, float, uint)-Funktion'
description: 'Gibt die vier texelwerte zurück, die in einem bilinearen Filter Vorgang zusammen mit dem Status der Kachel Zuordnung verwendet werden. | Texturecubearray:: Gather (S, float, uint)-Funktion'
ms.assetid: B5C1843C-8DE4-4007-B619-2CC09B8A023B
keywords:
- Funktion "HLSL" erfassen
topic_type:
- apiref
api_name:
- Gather
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b9c3f7be9189daa045f378f62856ddb68a2be89
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869975"
---
# <a name="texturecubearraygathersfloatuint-function"></a><span data-ttu-id="17a86-105">Texturecubearray:: Gather (S, float, uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="17a86-105">TextureCubeArray::Gather(S,float,uint) function</span></span>

<span data-ttu-id="17a86-106">Gibt die vier texelwerte zurück, die in einem bilinearen Filter Vorgang zusammen mit dem Status der Kachel Zuordnung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="17a86-106">Returns the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="17a86-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="17a86-107">Syntax</span></span>


``` syntax
TemplateType Gather(
  in  SamplerState S,
  in  float        Location,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="17a86-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="17a86-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17a86-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="17a86-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17a86-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="17a86-110">Type: **SamplerState**</span></span>

<span data-ttu-id="17a86-111">Der null basierte samplerindex.</span><span class="sxs-lookup"><span data-stu-id="17a86-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="17a86-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="17a86-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17a86-113">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="17a86-113">Type: **float**</span></span>

<span data-ttu-id="17a86-114">Die Beispiel Koordinaten (u, v).</span><span class="sxs-lookup"><span data-stu-id="17a86-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="17a86-115">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="17a86-115">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17a86-116">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="17a86-116">Type: **uint**</span></span>

<span data-ttu-id="17a86-117">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="17a86-117">The status of the operation.</span></span> <span data-ttu-id="17a86-118">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="17a86-118">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="17a86-119">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="17a86-119">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="17a86-120">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="17a86-120">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17a86-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="17a86-121">Return value</span></span>

<span data-ttu-id="17a86-122">Type: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="17a86-122">Type: **TemplateType**</span></span>

<span data-ttu-id="17a86-123">Ein vier komponentenwert, dessen Typ mit dem Vorlagentyp identisch ist.</span><span class="sxs-lookup"><span data-stu-id="17a86-123">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="17a86-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="17a86-124">Remarks</span></span>

<span data-ttu-id="17a86-125">Die Textur Beispiele können für bilineare Interpolationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="17a86-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="17a86-126">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="17a86-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="17a86-127">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="17a86-127">Vertex</span></span> | <span data-ttu-id="17a86-128">Hülle</span><span class="sxs-lookup"><span data-stu-id="17a86-128">Hull</span></span> | <span data-ttu-id="17a86-129">Domain</span><span class="sxs-lookup"><span data-stu-id="17a86-129">Domain</span></span> | <span data-ttu-id="17a86-130">Geometrie</span><span class="sxs-lookup"><span data-stu-id="17a86-130">Geometry</span></span> | <span data-ttu-id="17a86-131">Pixel</span><span class="sxs-lookup"><span data-stu-id="17a86-131">Pixel</span></span> | <span data-ttu-id="17a86-132">Compute</span><span class="sxs-lookup"><span data-stu-id="17a86-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="17a86-133">x</span><span class="sxs-lookup"><span data-stu-id="17a86-133">x</span></span>      | <span data-ttu-id="17a86-134">x</span><span class="sxs-lookup"><span data-stu-id="17a86-134">x</span></span>    | <span data-ttu-id="17a86-135">x</span><span class="sxs-lookup"><span data-stu-id="17a86-135">x</span></span>      | <span data-ttu-id="17a86-136">x</span><span class="sxs-lookup"><span data-stu-id="17a86-136">x</span></span>        | <span data-ttu-id="17a86-137">x</span><span class="sxs-lookup"><span data-stu-id="17a86-137">x</span></span>     | <span data-ttu-id="17a86-138">x</span><span class="sxs-lookup"><span data-stu-id="17a86-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="17a86-139">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="17a86-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17a86-140">Gather-Methoden</span><span class="sxs-lookup"><span data-stu-id="17a86-140">Gather methods</span></span>](texturecubearray-gather.md)
</dt> <dt>

[<span data-ttu-id="17a86-141">**Texturecubearray**</span><span class="sxs-lookup"><span data-stu-id="17a86-141">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
