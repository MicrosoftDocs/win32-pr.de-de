---
title: 'Texture2DArray:: gatheralpha (S, float, int, uint)-Funktion'
description: 'Gibt die vier texelwerte zurück, die in einem bilinearen Filter Vorgang zusammen mit dem Status der Kachel Zuordnung verwendet werden. | Texture2DArray:: gatheralpha (S, float, int, uint)-Funktion'
ms.assetid: B04F29A7-0EC9-49F0-9662-00F1DD0F3E5B
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
ms.openlocfilehash: 59f5ead36b4880ba02fc50691e634fc477efea6f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103961387"
---
# <a name="texture2darraygatheralphasfloatintuint-function"></a><span data-ttu-id="e721a-105">Texture2DArray:: gatheralpha (S, float, int, uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="e721a-105">Texture2DArray::GatherAlpha(S,float,int,uint) function</span></span>

<span data-ttu-id="e721a-106">Gibt die vier texelwerte zurück, die in einem bilinearen Filter Vorgang zusammen mit dem Status der Kachel Zuordnung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e721a-106">Returns the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="e721a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e721a-107">Syntax</span></span>


``` syntax
TemplateType GatherAlpha(
  in  SamplerState S,
  in  float        Location,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="e721a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e721a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e721a-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e721a-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e721a-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="e721a-110">Type: **SamplerState**</span></span>

<span data-ttu-id="e721a-111">Der null basierte samplerindex.</span><span class="sxs-lookup"><span data-stu-id="e721a-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="e721a-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e721a-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e721a-113">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="e721a-113">Type: **float**</span></span>

<span data-ttu-id="e721a-114">Die Beispiel Koordinaten (u, v).</span><span class="sxs-lookup"><span data-stu-id="e721a-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="e721a-115">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e721a-115">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e721a-116">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="e721a-116">Type: **int**</span></span>

<span data-ttu-id="e721a-117">Der Offset, der vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="e721a-117">The offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="e721a-118">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e721a-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e721a-119">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="e721a-119">Type: **uint**</span></span>

<span data-ttu-id="e721a-120">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="e721a-120">The status of the operation.</span></span> <span data-ttu-id="e721a-121">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="e721a-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="e721a-122">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="e721a-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="e721a-123">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="e721a-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e721a-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e721a-124">Return value</span></span>

<span data-ttu-id="e721a-125">Type: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="e721a-125">Type: **TemplateType**</span></span>

<span data-ttu-id="e721a-126">Ein vier komponentenwert, dessen Typ mit dem Vorlagentyp identisch ist.</span><span class="sxs-lookup"><span data-stu-id="e721a-126">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="e721a-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e721a-127">Remarks</span></span>

<span data-ttu-id="e721a-128">Die Textur Beispiele können für bilineare Interpolationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e721a-128">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="e721a-129">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="e721a-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="e721a-130">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="e721a-130">Vertex</span></span> | <span data-ttu-id="e721a-131">Hülle</span><span class="sxs-lookup"><span data-stu-id="e721a-131">Hull</span></span> | <span data-ttu-id="e721a-132">Domain</span><span class="sxs-lookup"><span data-stu-id="e721a-132">Domain</span></span> | <span data-ttu-id="e721a-133">Geometrie</span><span class="sxs-lookup"><span data-stu-id="e721a-133">Geometry</span></span> | <span data-ttu-id="e721a-134">Pixel</span><span class="sxs-lookup"><span data-stu-id="e721a-134">Pixel</span></span> | <span data-ttu-id="e721a-135">Compute</span><span class="sxs-lookup"><span data-stu-id="e721a-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e721a-136">x</span><span class="sxs-lookup"><span data-stu-id="e721a-136">x</span></span>      | <span data-ttu-id="e721a-137">x</span><span class="sxs-lookup"><span data-stu-id="e721a-137">x</span></span>    | <span data-ttu-id="e721a-138">x</span><span class="sxs-lookup"><span data-stu-id="e721a-138">x</span></span>      | <span data-ttu-id="e721a-139">x</span><span class="sxs-lookup"><span data-stu-id="e721a-139">x</span></span>        | <span data-ttu-id="e721a-140">x</span><span class="sxs-lookup"><span data-stu-id="e721a-140">x</span></span>     | <span data-ttu-id="e721a-141">x</span><span class="sxs-lookup"><span data-stu-id="e721a-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="e721a-142">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e721a-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e721a-143">Gatheralpha-Methoden</span><span class="sxs-lookup"><span data-stu-id="e721a-143">GatherAlpha methods</span></span>](texture2darray-gatheralpha.md)
</dt> </dl>

 

 
