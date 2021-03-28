---
title: 'Texturecubearray:: gatheralpha (S, float, uint)-Funktion'
description: 'Gibt die Alpha Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang zusammen mit dem Status der Kachel Zuordnung verwendet werden. | Texturecubearray:: gatheralpha (S, float, uint)-Funktion'
ms.assetid: C6AF896A-C68E-44EA-A779-DD9DBA30A039
keywords:
- Gatheralpha-Funktion HLSL
topic_type:
- apiref
api_name:
- GatherAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c1f9b692d81f6e26753496bb58ac114145ed21de
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530749"
---
# <a name="texturecubearraygatheralphasfloatuint-function"></a><span data-ttu-id="cf151-105">Texturecubearray:: gatheralpha (S, float, uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="cf151-105">TextureCubeArray::GatherAlpha(S,float,uint) function</span></span>

<span data-ttu-id="cf151-106">Gibt die Alpha Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang zusammen mit dem Status der Kachel Zuordnung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cf151-106">Returns the alpha components of the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf151-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf151-107">Syntax</span></span>


``` syntax
TemplateType GatherAlpha(
  in  SamplerState S,
  in  float        Location,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="cf151-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf151-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf151-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cf151-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf151-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="cf151-110">Type: **SamplerState**</span></span>

<span data-ttu-id="cf151-111">Der null basierte samplerindex.</span><span class="sxs-lookup"><span data-stu-id="cf151-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="cf151-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cf151-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf151-113">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="cf151-113">Type: **float**</span></span>

<span data-ttu-id="cf151-114">Die Beispiel Koordinaten (u, v).</span><span class="sxs-lookup"><span data-stu-id="cf151-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="cf151-115">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cf151-115">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf151-116">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="cf151-116">Type: **uint**</span></span>

<span data-ttu-id="cf151-117">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="cf151-117">The status of the operation.</span></span> <span data-ttu-id="cf151-118">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="cf151-118">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="cf151-119">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="cf151-119">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="cf151-120">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="cf151-120">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf151-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cf151-121">Return value</span></span>

<span data-ttu-id="cf151-122">Type: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="cf151-122">Type: **TemplateType**</span></span>

<span data-ttu-id="cf151-123">Ein vier komponentenwert, dessen Typ mit dem Vorlagentyp identisch ist.</span><span class="sxs-lookup"><span data-stu-id="cf151-123">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf151-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf151-124">Remarks</span></span>

<span data-ttu-id="cf151-125">Die Textur Beispiele können für bilineare Interpolationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cf151-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="cf151-126">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="cf151-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="cf151-127">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="cf151-127">Vertex</span></span> | <span data-ttu-id="cf151-128">Hülle</span><span class="sxs-lookup"><span data-stu-id="cf151-128">Hull</span></span> | <span data-ttu-id="cf151-129">Domain</span><span class="sxs-lookup"><span data-stu-id="cf151-129">Domain</span></span> | <span data-ttu-id="cf151-130">Geometrie</span><span class="sxs-lookup"><span data-stu-id="cf151-130">Geometry</span></span> | <span data-ttu-id="cf151-131">Pixel</span><span class="sxs-lookup"><span data-stu-id="cf151-131">Pixel</span></span> | <span data-ttu-id="cf151-132">Compute</span><span class="sxs-lookup"><span data-stu-id="cf151-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="cf151-133">x</span><span class="sxs-lookup"><span data-stu-id="cf151-133">x</span></span>      | <span data-ttu-id="cf151-134">x</span><span class="sxs-lookup"><span data-stu-id="cf151-134">x</span></span>    | <span data-ttu-id="cf151-135">x</span><span class="sxs-lookup"><span data-stu-id="cf151-135">x</span></span>      | <span data-ttu-id="cf151-136">x</span><span class="sxs-lookup"><span data-stu-id="cf151-136">x</span></span>        | <span data-ttu-id="cf151-137">x</span><span class="sxs-lookup"><span data-stu-id="cf151-137">x</span></span>     | <span data-ttu-id="cf151-138">x</span><span class="sxs-lookup"><span data-stu-id="cf151-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="cf151-139">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cf151-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf151-140">Gatheralpha-Methoden</span><span class="sxs-lookup"><span data-stu-id="cf151-140">GatherAlpha methods</span></span>](texturecubearray-gatheralpha.md)
</dt> <dt>

[<span data-ttu-id="cf151-141">**Texturecubearray**</span><span class="sxs-lookup"><span data-stu-id="cf151-141">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
