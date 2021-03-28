---
title: 'Texturecube:: Gather (S, float, uint)-Funktion'
description: 'Gibt die vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden. | Texturecube:: Gather (S, float, uint)-Funktion'
ms.assetid: 23FA8135-ECF0-4CAE-9A1C-B05DA3676453
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
ms.openlocfilehash: e9710343ff9b09e4425bc133db6dab4d118d807e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981184"
---
# <a name="texturecubegathersfloatuint-function"></a><span data-ttu-id="5a6c3-105">Texturecube:: Gather (S, float, uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="5a6c3-105">TextureCube::Gather(S,float,uint) function</span></span>

<span data-ttu-id="5a6c3-106">Gibt die vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5a6c3-106">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a6c3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a6c3-107">Syntax</span></span>


``` syntax
TemplateType Gather(
  in  SamplerState S,
  in  float        Location,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="5a6c3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a6c3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a6c3-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5a6c3-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a6c3-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="5a6c3-110">Type: **SamplerState**</span></span>

<span data-ttu-id="5a6c3-111">Der null basierte samplerindex.</span><span class="sxs-lookup"><span data-stu-id="5a6c3-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="5a6c3-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5a6c3-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a6c3-113">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="5a6c3-113">Type: **float**</span></span>

<span data-ttu-id="5a6c3-114">Die Beispiel Koordinaten (u, v).</span><span class="sxs-lookup"><span data-stu-id="5a6c3-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="5a6c3-115">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5a6c3-115">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a6c3-116">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="5a6c3-116">Type: **uint**</span></span>

<span data-ttu-id="5a6c3-117">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="5a6c3-117">The status of the operation.</span></span> <span data-ttu-id="5a6c3-118">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="5a6c3-118">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="5a6c3-119">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="5a6c3-119">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="5a6c3-120">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="5a6c3-120">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a6c3-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5a6c3-121">Return value</span></span>

<span data-ttu-id="5a6c3-122">Type: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="5a6c3-122">Type: **TemplateType**</span></span>

<span data-ttu-id="5a6c3-123">Ein vier komponentenwert, dessen Typ mit dem Vorlagentyp identisch ist.</span><span class="sxs-lookup"><span data-stu-id="5a6c3-123">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a6c3-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5a6c3-124">Remarks</span></span>

<span data-ttu-id="5a6c3-125">Die Textur Beispiele können für bilineare Interpolationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5a6c3-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="5a6c3-126">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="5a6c3-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="5a6c3-127">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="5a6c3-127">Vertex</span></span> | <span data-ttu-id="5a6c3-128">Hülle</span><span class="sxs-lookup"><span data-stu-id="5a6c3-128">Hull</span></span> | <span data-ttu-id="5a6c3-129">Domain</span><span class="sxs-lookup"><span data-stu-id="5a6c3-129">Domain</span></span> | <span data-ttu-id="5a6c3-130">Geometrie</span><span class="sxs-lookup"><span data-stu-id="5a6c3-130">Geometry</span></span> | <span data-ttu-id="5a6c3-131">Pixel</span><span class="sxs-lookup"><span data-stu-id="5a6c3-131">Pixel</span></span> | <span data-ttu-id="5a6c3-132">Compute</span><span class="sxs-lookup"><span data-stu-id="5a6c3-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="5a6c3-133">x</span><span class="sxs-lookup"><span data-stu-id="5a6c3-133">x</span></span>      | <span data-ttu-id="5a6c3-134">x</span><span class="sxs-lookup"><span data-stu-id="5a6c3-134">x</span></span>    | <span data-ttu-id="5a6c3-135">x</span><span class="sxs-lookup"><span data-stu-id="5a6c3-135">x</span></span>      | <span data-ttu-id="5a6c3-136">x</span><span class="sxs-lookup"><span data-stu-id="5a6c3-136">x</span></span>        | <span data-ttu-id="5a6c3-137">x</span><span class="sxs-lookup"><span data-stu-id="5a6c3-137">x</span></span>     | <span data-ttu-id="5a6c3-138">x</span><span class="sxs-lookup"><span data-stu-id="5a6c3-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="5a6c3-139">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5a6c3-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a6c3-140">Gather-Methoden</span><span class="sxs-lookup"><span data-stu-id="5a6c3-140">Gather methods</span></span>](texturecube-gather.md)
</dt> <dt>

[<span data-ttu-id="5a6c3-141">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="5a6c3-141">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
