---
title: 'Byteaddressbuffer:: Load3 (uint, uint)-Funktion'
description: Ruft drei Werte und den Status des Vorgangs ab.
ms.assetid: 6AD8E957-F646-4749-A9B4-5C0C936D90E3
keywords:
- Load3-Funktion (HLSL)
topic_type:
- apiref
api_name:
- Load3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1bf3ffda082b8d2ae9cf22db59c1c38682563136
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315177"
---
# <a name="load3uint-uint-function"></a><span data-ttu-id="d879c-104">Load3 (uint, uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="d879c-104">Load3(uint, uint) function</span></span>

<span data-ttu-id="d879c-105">Ruft drei Werte und den Status des Vorgangs ab.</span><span class="sxs-lookup"><span data-stu-id="d879c-105">Gets three values and the status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="d879c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d879c-106">Syntax</span></span>

``` syntax
uint3 Load3(
  in  uint Location,
  out uint Status
);
```

## <a name="parameters"></a><span data-ttu-id="d879c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d879c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d879c-108">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d879c-108">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d879c-109">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="d879c-109">Type: **uint**</span></span>

<span data-ttu-id="d879c-110">Die Eingabe Adresse in Byte, bei der es sich um ein Vielfaches von 4 handeln muss.</span><span class="sxs-lookup"><span data-stu-id="d879c-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="d879c-111">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d879c-111">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d879c-112">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="d879c-112">Type: **uint**</span></span>

<span data-ttu-id="d879c-113">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="d879c-113">The status of the operation.</span></span> <span data-ttu-id="d879c-114">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="d879c-114">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="d879c-115">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="d879c-115">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="d879c-116">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="d879c-116">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d879c-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d879c-117">Return value</span></span>

<span data-ttu-id="d879c-118">Typ: **uint3**</span><span class="sxs-lookup"><span data-stu-id="d879c-118">Type: **uint3**</span></span>

<span data-ttu-id="d879c-119">Drei Werte.</span><span class="sxs-lookup"><span data-stu-id="d879c-119">Three values.</span></span>

## <a name="remarks"></a><span data-ttu-id="d879c-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d879c-120">Remarks</span></span>

<span data-ttu-id="d879c-121">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="d879c-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="d879c-122">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="d879c-122">Vertex</span></span> | <span data-ttu-id="d879c-123">Hülle</span><span class="sxs-lookup"><span data-stu-id="d879c-123">Hull</span></span> | <span data-ttu-id="d879c-124">Domain</span><span class="sxs-lookup"><span data-stu-id="d879c-124">Domain</span></span> | <span data-ttu-id="d879c-125">Geometrie</span><span class="sxs-lookup"><span data-stu-id="d879c-125">Geometry</span></span> | <span data-ttu-id="d879c-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="d879c-126">Pixel</span></span> | <span data-ttu-id="d879c-127">Compute</span><span class="sxs-lookup"><span data-stu-id="d879c-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="d879c-128">x</span><span class="sxs-lookup"><span data-stu-id="d879c-128">x</span></span>      | <span data-ttu-id="d879c-129">x</span><span class="sxs-lookup"><span data-stu-id="d879c-129">x</span></span>    | <span data-ttu-id="d879c-130">x</span><span class="sxs-lookup"><span data-stu-id="d879c-130">x</span></span>      | <span data-ttu-id="d879c-131">x</span><span class="sxs-lookup"><span data-stu-id="d879c-131">x</span></span>        | <span data-ttu-id="d879c-132">x</span><span class="sxs-lookup"><span data-stu-id="d879c-132">x</span></span>     | <span data-ttu-id="d879c-133">x</span><span class="sxs-lookup"><span data-stu-id="d879c-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="d879c-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d879c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d879c-135">Load3-Methoden</span><span class="sxs-lookup"><span data-stu-id="d879c-135">Load3 methods</span></span>](byteaddressbuffer-load3.md)
</dt> <dt>

[<span data-ttu-id="d879c-136">**Byteaddressbuffer**</span><span class="sxs-lookup"><span data-stu-id="d879c-136">**ByteAddressBuffer**</span></span>](sm5-object-byteaddressbuffer.md)
</dt> </dl>

 

 