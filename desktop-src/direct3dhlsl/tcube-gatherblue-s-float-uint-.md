---
title: 'Texturecube:: gatherblue (S, float, uint)-Funktion'
description: 'Gibt die blauen Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang zusammen mit dem Status der Kachel Zuordnung verwendet werden. | Texturecube:: gatherblue (S, float, uint)-Funktion'
ms.assetid: B2099321-3E81-4A77-A023-AF73594C68C8
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
ms.openlocfilehash: 59378e3a5754dbd55298d6040b40076a9e54eb74
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981896"
---
# <a name="texturecubegatherbluesfloatuint-function"></a><span data-ttu-id="f98c2-105">Texturecube:: gatherblue (S, float, uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="f98c2-105">TextureCube::GatherBlue(S,float,uint) function</span></span>

<span data-ttu-id="f98c2-106">Gibt die blauen Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang zusammen mit dem Status der Kachel Zuordnung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f98c2-106">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="f98c2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f98c2-107">Syntax</span></span>


``` syntax
TemplateType GatherBlue(
  in  SamplerState S,
  in  float        Location,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="f98c2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f98c2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f98c2-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f98c2-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f98c2-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="f98c2-110">Type: **SamplerState**</span></span>

<span data-ttu-id="f98c2-111">Der null basierte samplerindex.</span><span class="sxs-lookup"><span data-stu-id="f98c2-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="f98c2-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f98c2-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f98c2-113">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="f98c2-113">Type: **float**</span></span>

<span data-ttu-id="f98c2-114">Die Beispiel Koordinaten (u, v).</span><span class="sxs-lookup"><span data-stu-id="f98c2-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="f98c2-115">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f98c2-115">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f98c2-116">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="f98c2-116">Type: **uint**</span></span>

<span data-ttu-id="f98c2-117">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="f98c2-117">The status of the operation.</span></span> <span data-ttu-id="f98c2-118">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="f98c2-118">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="f98c2-119">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="f98c2-119">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="f98c2-120">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="f98c2-120">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f98c2-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f98c2-121">Return value</span></span>

<span data-ttu-id="f98c2-122">Type: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="f98c2-122">Type: **TemplateType**</span></span>

<span data-ttu-id="f98c2-123">Ein vier komponentenwert, dessen Typ mit dem Vorlagentyp identisch ist.</span><span class="sxs-lookup"><span data-stu-id="f98c2-123">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="f98c2-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f98c2-124">Remarks</span></span>

<span data-ttu-id="f98c2-125">Die Textur Beispiele können für bilineare Interpolationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f98c2-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="f98c2-126">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="f98c2-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="f98c2-127">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="f98c2-127">Vertex</span></span> | <span data-ttu-id="f98c2-128">Hülle</span><span class="sxs-lookup"><span data-stu-id="f98c2-128">Hull</span></span> | <span data-ttu-id="f98c2-129">Domain</span><span class="sxs-lookup"><span data-stu-id="f98c2-129">Domain</span></span> | <span data-ttu-id="f98c2-130">Geometrie</span><span class="sxs-lookup"><span data-stu-id="f98c2-130">Geometry</span></span> | <span data-ttu-id="f98c2-131">Pixel</span><span class="sxs-lookup"><span data-stu-id="f98c2-131">Pixel</span></span> | <span data-ttu-id="f98c2-132">Compute</span><span class="sxs-lookup"><span data-stu-id="f98c2-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f98c2-133">x</span><span class="sxs-lookup"><span data-stu-id="f98c2-133">x</span></span>      | <span data-ttu-id="f98c2-134">x</span><span class="sxs-lookup"><span data-stu-id="f98c2-134">x</span></span>    | <span data-ttu-id="f98c2-135">x</span><span class="sxs-lookup"><span data-stu-id="f98c2-135">x</span></span>      | <span data-ttu-id="f98c2-136">x</span><span class="sxs-lookup"><span data-stu-id="f98c2-136">x</span></span>        | <span data-ttu-id="f98c2-137">x</span><span class="sxs-lookup"><span data-stu-id="f98c2-137">x</span></span>     | <span data-ttu-id="f98c2-138">x</span><span class="sxs-lookup"><span data-stu-id="f98c2-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="f98c2-139">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f98c2-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f98c2-140">Gatherblue-Methoden</span><span class="sxs-lookup"><span data-stu-id="f98c2-140">GatherBlue methods</span></span>](texturecube-gatherblue.md)
</dt> <dt>

[<span data-ttu-id="f98c2-141">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="f98c2-141">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
