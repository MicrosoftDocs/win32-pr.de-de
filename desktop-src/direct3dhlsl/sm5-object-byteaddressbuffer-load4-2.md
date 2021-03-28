---
title: 'Byteaddressbuffer:: Load4 (uint, uint)-Funktion'
description: Ruft vier Werte und den Status des Vorgangs ab.
ms.assetid: C814F717-9FD4-4BFC-A91B-319477B7F3DE
keywords:
- Load4-Funktion (HLSL)
topic_type:
- apiref
api_name:
- Load4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ab27ed9002562643ddf4df6b33efe9d8f0454d94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039014"
---
# <a name="load4uint-uint-function"></a><span data-ttu-id="c3d6f-104">Load4 (uint, uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="c3d6f-104">Load4(uint, uint) function</span></span>

<span data-ttu-id="c3d6f-105">Ruft vier Werte und den Status des Vorgangs ab.</span><span class="sxs-lookup"><span data-stu-id="c3d6f-105">Gets four values and the status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3d6f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3d6f-106">Syntax</span></span>

``` syntax
uint4 Load4(
  in  uint Location,
  out uint Status
);
```

## <a name="parameters"></a><span data-ttu-id="c3d6f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3d6f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3d6f-108">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c3d6f-108">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3d6f-109">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="c3d6f-109">Type: **uint**</span></span>

<span data-ttu-id="c3d6f-110">Die Eingabe Adresse in Byte, bei der es sich um ein Vielfaches von 4 handeln muss.</span><span class="sxs-lookup"><span data-stu-id="c3d6f-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="c3d6f-111">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c3d6f-111">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3d6f-112">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="c3d6f-112">Type: **uint**</span></span>

<span data-ttu-id="c3d6f-113">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="c3d6f-113">The status of the operation.</span></span> <span data-ttu-id="c3d6f-114">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="c3d6f-114">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="c3d6f-115">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="c3d6f-115">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="c3d6f-116">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="c3d6f-116">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3d6f-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c3d6f-117">Return value</span></span>

<span data-ttu-id="c3d6f-118">Typ: **uint4**</span><span class="sxs-lookup"><span data-stu-id="c3d6f-118">Type: **uint4**</span></span>

<span data-ttu-id="c3d6f-119">Vier Werte.</span><span class="sxs-lookup"><span data-stu-id="c3d6f-119">Four values.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3d6f-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c3d6f-120">Remarks</span></span>

<span data-ttu-id="c3d6f-121">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="c3d6f-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="c3d6f-122">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="c3d6f-122">Vertex</span></span> | <span data-ttu-id="c3d6f-123">Hülle</span><span class="sxs-lookup"><span data-stu-id="c3d6f-123">Hull</span></span> | <span data-ttu-id="c3d6f-124">Domain</span><span class="sxs-lookup"><span data-stu-id="c3d6f-124">Domain</span></span> | <span data-ttu-id="c3d6f-125">Geometrie</span><span class="sxs-lookup"><span data-stu-id="c3d6f-125">Geometry</span></span> | <span data-ttu-id="c3d6f-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="c3d6f-126">Pixel</span></span> | <span data-ttu-id="c3d6f-127">Compute</span><span class="sxs-lookup"><span data-stu-id="c3d6f-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="c3d6f-128">x</span><span class="sxs-lookup"><span data-stu-id="c3d6f-128">x</span></span>      | <span data-ttu-id="c3d6f-129">x</span><span class="sxs-lookup"><span data-stu-id="c3d6f-129">x</span></span>    | <span data-ttu-id="c3d6f-130">x</span><span class="sxs-lookup"><span data-stu-id="c3d6f-130">x</span></span>      | <span data-ttu-id="c3d6f-131">x</span><span class="sxs-lookup"><span data-stu-id="c3d6f-131">x</span></span>        | <span data-ttu-id="c3d6f-132">x</span><span class="sxs-lookup"><span data-stu-id="c3d6f-132">x</span></span>     | <span data-ttu-id="c3d6f-133">x</span><span class="sxs-lookup"><span data-stu-id="c3d6f-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="c3d6f-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c3d6f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3d6f-135">Load4-Methoden</span><span class="sxs-lookup"><span data-stu-id="c3d6f-135">Load4 methods</span></span>](byteaddressbuffer-load4.md)
</dt> <dt>

[<span data-ttu-id="c3d6f-136">**Byteaddressbuffer**</span><span class="sxs-lookup"><span data-stu-id="c3d6f-136">**ByteAddressBuffer**</span></span>](sm5-object-byteaddressbuffer.md)
</dt> </dl>

 

 