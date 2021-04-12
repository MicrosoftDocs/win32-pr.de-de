---
title: 'Rwbyteaddressbuffer:: Load3 (uint, uint)-Funktion'
description: Ruft drei Werte ab und gibt den Status des Vorgangs zurück.
ms.assetid: EBCCDAF3-69B9-4132-85EC-82759F292811
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
ms.openlocfilehash: 8451abe17c3ff74a1906828b3570dc6ee98782f1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315974"
---
# <a name="load3uintuint-function"></a><span data-ttu-id="ce236-104">Load3 (uint, uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="ce236-104">Load3(uint,uint) function</span></span>

<span data-ttu-id="ce236-105">Ruft drei Werte ab und gibt den Status des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="ce236-105">Gets three values and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce236-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce236-106">Syntax</span></span>


``` syntax
uint3 Load3(
  in  uint Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="ce236-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce236-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce236-108">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce236-108">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce236-109">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="ce236-109">Type: **uint**</span></span>

<span data-ttu-id="ce236-110">Der Speicherort des Puffers.</span><span class="sxs-lookup"><span data-stu-id="ce236-110">The location of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="ce236-111">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ce236-111">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce236-112">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="ce236-112">Type: **uint**</span></span>

<span data-ttu-id="ce236-113">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="ce236-113">The status of the operation.</span></span> <span data-ttu-id="ce236-114">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="ce236-114">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="ce236-115">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="ce236-115">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="ce236-116">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="ce236-116">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce236-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ce236-117">Return value</span></span>

<span data-ttu-id="ce236-118">Typ: **uint3**</span><span class="sxs-lookup"><span data-stu-id="ce236-118">Type: **uint3**</span></span>

<span data-ttu-id="ce236-119">Drei Werte.</span><span class="sxs-lookup"><span data-stu-id="ce236-119">Three values.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce236-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ce236-120">Remarks</span></span>

<span data-ttu-id="ce236-121">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="ce236-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="ce236-122">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="ce236-122">Vertex</span></span> | <span data-ttu-id="ce236-123">Hülle</span><span class="sxs-lookup"><span data-stu-id="ce236-123">Hull</span></span> | <span data-ttu-id="ce236-124">Domain</span><span class="sxs-lookup"><span data-stu-id="ce236-124">Domain</span></span> | <span data-ttu-id="ce236-125">Geometrie</span><span class="sxs-lookup"><span data-stu-id="ce236-125">Geometry</span></span> | <span data-ttu-id="ce236-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="ce236-126">Pixel</span></span> | <span data-ttu-id="ce236-127">Compute</span><span class="sxs-lookup"><span data-stu-id="ce236-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="ce236-128">x</span><span class="sxs-lookup"><span data-stu-id="ce236-128">x</span></span>     | <span data-ttu-id="ce236-129">x</span><span class="sxs-lookup"><span data-stu-id="ce236-129">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ce236-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ce236-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce236-131">Load3-Methoden</span><span class="sxs-lookup"><span data-stu-id="ce236-131">Load3 methods</span></span>](rwbyteaddressbuffer-load3.md)
</dt> </dl>

 

 