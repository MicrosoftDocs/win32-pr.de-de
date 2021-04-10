---
title: 'Byteaddressbuffer:: Load2 (uint, uint)-Funktion'
description: Ruft zwei Werte und den Status des Vorgangs ab.
ms.assetid: EE6FA09D-0C86-499D-86F9-EAA56125EB91
keywords:
- Load2-Funktion (HLSL)
topic_type:
- apiref
api_name:
- Load2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 662e40789f59b75e53111fbab6d24288f27c8e35
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039376"
---
# <a name="load2uint-uint-function"></a><span data-ttu-id="fcd09-104">Load2 (uint, uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="fcd09-104">Load2(uint, uint) function</span></span>

<span data-ttu-id="fcd09-105">Ruft zwei Werte und den Status des Vorgangs ab.</span><span class="sxs-lookup"><span data-stu-id="fcd09-105">Gets two values and the status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcd09-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="fcd09-106">Syntax</span></span>

``` syntax
uint2 Load2(
  in  uint Location,
  out uint Status
);
```

## <a name="parameters"></a><span data-ttu-id="fcd09-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="fcd09-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcd09-108">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fcd09-108">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcd09-109">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="fcd09-109">Type: **uint**</span></span>

<span data-ttu-id="fcd09-110">Die Eingabe Adresse in Byte, bei der es sich um ein Vielfaches von 4 handeln muss.</span><span class="sxs-lookup"><span data-stu-id="fcd09-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="fcd09-111">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fcd09-111">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fcd09-112">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="fcd09-112">Type: **uint**</span></span>

<span data-ttu-id="fcd09-113">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="fcd09-113">The status of the operation.</span></span> <span data-ttu-id="fcd09-114">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="fcd09-114">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="fcd09-115">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="fcd09-115">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="fcd09-116">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="fcd09-116">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcd09-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fcd09-117">Return value</span></span>

<span data-ttu-id="fcd09-118">Typ: **uint2**</span><span class="sxs-lookup"><span data-stu-id="fcd09-118">Type: **uint2**</span></span>

<span data-ttu-id="fcd09-119">Zwei-Werte.</span><span class="sxs-lookup"><span data-stu-id="fcd09-119">Two values.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcd09-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fcd09-120">Remarks</span></span>

<span data-ttu-id="fcd09-121">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="fcd09-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="fcd09-122">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="fcd09-122">Vertex</span></span> | <span data-ttu-id="fcd09-123">Hülle</span><span class="sxs-lookup"><span data-stu-id="fcd09-123">Hull</span></span> | <span data-ttu-id="fcd09-124">Domain</span><span class="sxs-lookup"><span data-stu-id="fcd09-124">Domain</span></span> | <span data-ttu-id="fcd09-125">Geometrie</span><span class="sxs-lookup"><span data-stu-id="fcd09-125">Geometry</span></span> | <span data-ttu-id="fcd09-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="fcd09-126">Pixel</span></span> | <span data-ttu-id="fcd09-127">Compute</span><span class="sxs-lookup"><span data-stu-id="fcd09-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="fcd09-128">x</span><span class="sxs-lookup"><span data-stu-id="fcd09-128">x</span></span>      | <span data-ttu-id="fcd09-129">x</span><span class="sxs-lookup"><span data-stu-id="fcd09-129">x</span></span>    | <span data-ttu-id="fcd09-130">x</span><span class="sxs-lookup"><span data-stu-id="fcd09-130">x</span></span>      | <span data-ttu-id="fcd09-131">x</span><span class="sxs-lookup"><span data-stu-id="fcd09-131">x</span></span>        | <span data-ttu-id="fcd09-132">x</span><span class="sxs-lookup"><span data-stu-id="fcd09-132">x</span></span>     | <span data-ttu-id="fcd09-133">x</span><span class="sxs-lookup"><span data-stu-id="fcd09-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="fcd09-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="fcd09-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcd09-135">Load2-Methoden</span><span class="sxs-lookup"><span data-stu-id="fcd09-135">Load2 methods</span></span>](byteaddressbuffer-load2.md)
</dt> <dt>

[<span data-ttu-id="fcd09-136">**Byteaddressbuffer**</span><span class="sxs-lookup"><span data-stu-id="fcd09-136">**ByteAddressBuffer**</span></span>](sm5-object-byteaddressbuffer.md)
</dt> </dl>

 

 