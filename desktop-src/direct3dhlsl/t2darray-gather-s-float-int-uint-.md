---
title: 'Texture2DArray:: Gather (S, float, int, uint)-Funktion'
description: 'Gibt die vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden. | Texture2DArray:: Gather (S, float, int, uint)-Funktion'
ms.assetid: 311A5042-19AA-41C7-8B22-2E34E4554250
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
ms.openlocfilehash: a1677fae87d8bbec3c0144cc8da0b5d13f0e0ae9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530695"
---
# <a name="texture2darraygathersfloatintuint-function"></a><span data-ttu-id="53936-105">Texture2DArray:: Gather (S, float, int, uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="53936-105">Texture2DArray::Gather(S,float,int,uint) function</span></span>

<span data-ttu-id="53936-106">Gibt die vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="53936-106">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="53936-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="53936-107">Syntax</span></span>


``` syntax
TemplateType Gather(
  in  SamplerState S,
  in  float        Location,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="53936-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="53936-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53936-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53936-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53936-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="53936-110">Type: **SamplerState**</span></span>

<span data-ttu-id="53936-111">Der null basierte samplerindex.</span><span class="sxs-lookup"><span data-stu-id="53936-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="53936-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53936-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53936-113">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="53936-113">Type: **float**</span></span>

<span data-ttu-id="53936-114">Die Beispiel Koordinaten (u, v).</span><span class="sxs-lookup"><span data-stu-id="53936-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="53936-115">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53936-115">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53936-116">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="53936-116">Type: **int**</span></span>

<span data-ttu-id="53936-117">Der Offset, der vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="53936-117">The offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="53936-118">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="53936-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53936-119">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="53936-119">Type: **uint**</span></span>

<span data-ttu-id="53936-120">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="53936-120">The status of the operation.</span></span> <span data-ttu-id="53936-121">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="53936-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="53936-122">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="53936-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="53936-123">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="53936-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53936-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="53936-124">Return value</span></span>

<span data-ttu-id="53936-125">Type: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="53936-125">Type: **TemplateType**</span></span>

<span data-ttu-id="53936-126">Ein vier komponentenwert, dessen Typ mit dem Vorlagentyp identisch ist.</span><span class="sxs-lookup"><span data-stu-id="53936-126">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="53936-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="53936-127">Remarks</span></span>

<span data-ttu-id="53936-128">Die Textur Beispiele können für bilineare Interpolationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="53936-128">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="53936-129">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="53936-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="53936-130">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="53936-130">Vertex</span></span> | <span data-ttu-id="53936-131">Hülle</span><span class="sxs-lookup"><span data-stu-id="53936-131">Hull</span></span> | <span data-ttu-id="53936-132">Domain</span><span class="sxs-lookup"><span data-stu-id="53936-132">Domain</span></span> | <span data-ttu-id="53936-133">Geometrie</span><span class="sxs-lookup"><span data-stu-id="53936-133">Geometry</span></span> | <span data-ttu-id="53936-134">Pixel</span><span class="sxs-lookup"><span data-stu-id="53936-134">Pixel</span></span> | <span data-ttu-id="53936-135">Compute</span><span class="sxs-lookup"><span data-stu-id="53936-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="53936-136">x</span><span class="sxs-lookup"><span data-stu-id="53936-136">x</span></span>      | <span data-ttu-id="53936-137">x</span><span class="sxs-lookup"><span data-stu-id="53936-137">x</span></span>    | <span data-ttu-id="53936-138">x</span><span class="sxs-lookup"><span data-stu-id="53936-138">x</span></span>      | <span data-ttu-id="53936-139">x</span><span class="sxs-lookup"><span data-stu-id="53936-139">x</span></span>        | <span data-ttu-id="53936-140">x</span><span class="sxs-lookup"><span data-stu-id="53936-140">x</span></span>     | <span data-ttu-id="53936-141">x</span><span class="sxs-lookup"><span data-stu-id="53936-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="53936-142">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="53936-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53936-143">Gather-Methoden</span><span class="sxs-lookup"><span data-stu-id="53936-143">Gather methods</span></span>](texture2darray-gather.md)
</dt> </dl>

 

 
