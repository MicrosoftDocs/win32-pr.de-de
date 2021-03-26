---
title: 'Texturecubearray:: gathergreen (S, float, uint)-Funktion'
description: 'Gibt die grünen Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang zusammen mit dem Status der Kachel Zuordnung verwendet werden. | Texturecubearray:: gathergreen (S, float, uint)-Funktion'
ms.assetid: 0DEB1810-F2C7-4097-B2D3-20ED4E297561
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
ms.openlocfilehash: 6c6809f56c8b589c97b103fdd71ccbd1292110ad
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981497"
---
# <a name="texturecubearraygathergreensfloatuint-function"></a><span data-ttu-id="590e5-105">Texturecubearray:: gathergreen (S, float, uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="590e5-105">TextureCubeArray::GatherGreen(S,float,uint) function</span></span>

<span data-ttu-id="590e5-106">Gibt die grünen Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang zusammen mit dem Status der Kachel Zuordnung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="590e5-106">Returns the green components of the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="590e5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="590e5-107">Syntax</span></span>


``` syntax
TemplateType GatherGreen(
  in  SamplerState S,
  in  float        Location,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="590e5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="590e5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="590e5-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="590e5-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="590e5-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="590e5-110">Type: **SamplerState**</span></span>

<span data-ttu-id="590e5-111">Der null basierte samplerindex.</span><span class="sxs-lookup"><span data-stu-id="590e5-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="590e5-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="590e5-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="590e5-113">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="590e5-113">Type: **float**</span></span>

<span data-ttu-id="590e5-114">Die Beispiel Koordinaten (u, v).</span><span class="sxs-lookup"><span data-stu-id="590e5-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="590e5-115">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="590e5-115">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="590e5-116">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="590e5-116">Type: **uint**</span></span>

<span data-ttu-id="590e5-117">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="590e5-117">The status of the operation.</span></span> <span data-ttu-id="590e5-118">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="590e5-118">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="590e5-119">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="590e5-119">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="590e5-120">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="590e5-120">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="590e5-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="590e5-121">Return value</span></span>

<span data-ttu-id="590e5-122">Type: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="590e5-122">Type: **TemplateType**</span></span>

<span data-ttu-id="590e5-123">Ein vier komponentenwert, dessen Typ mit dem Vorlagentyp identisch ist.</span><span class="sxs-lookup"><span data-stu-id="590e5-123">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="590e5-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="590e5-124">Remarks</span></span>

<span data-ttu-id="590e5-125">Die Textur Beispiele können für bilineare Interpolationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="590e5-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="590e5-126">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="590e5-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="590e5-127">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="590e5-127">Vertex</span></span> | <span data-ttu-id="590e5-128">Hülle</span><span class="sxs-lookup"><span data-stu-id="590e5-128">Hull</span></span> | <span data-ttu-id="590e5-129">Domain</span><span class="sxs-lookup"><span data-stu-id="590e5-129">Domain</span></span> | <span data-ttu-id="590e5-130">Geometrie</span><span class="sxs-lookup"><span data-stu-id="590e5-130">Geometry</span></span> | <span data-ttu-id="590e5-131">Pixel</span><span class="sxs-lookup"><span data-stu-id="590e5-131">Pixel</span></span> | <span data-ttu-id="590e5-132">Compute</span><span class="sxs-lookup"><span data-stu-id="590e5-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="590e5-133">x</span><span class="sxs-lookup"><span data-stu-id="590e5-133">x</span></span>      | <span data-ttu-id="590e5-134">x</span><span class="sxs-lookup"><span data-stu-id="590e5-134">x</span></span>    | <span data-ttu-id="590e5-135">x</span><span class="sxs-lookup"><span data-stu-id="590e5-135">x</span></span>      | <span data-ttu-id="590e5-136">x</span><span class="sxs-lookup"><span data-stu-id="590e5-136">x</span></span>        | <span data-ttu-id="590e5-137">x</span><span class="sxs-lookup"><span data-stu-id="590e5-137">x</span></span>     | <span data-ttu-id="590e5-138">x</span><span class="sxs-lookup"><span data-stu-id="590e5-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="590e5-139">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="590e5-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="590e5-140">Gathergreen-Methoden</span><span class="sxs-lookup"><span data-stu-id="590e5-140">GatherGreen methods</span></span>](texturecubearray-gathergreen.md)
</dt> <dt>

[<span data-ttu-id="590e5-141">**Texturecubearray**</span><span class="sxs-lookup"><span data-stu-id="590e5-141">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
