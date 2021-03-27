---
title: 'Rwbyteaddressbuffer:: Load4 (uint, uint)-Funktion'
description: Ruft vier Werte ab und gibt den Status des Vorgangs zurück.
ms.assetid: 10C21836-3CE4-4AE9-82F4-C8BBDE19CA69
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
ms.openlocfilehash: 14cb5354c21935c22833ea6f4b54b20fedc696f0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730121"
---
# <a name="load4uintuint-function"></a><span data-ttu-id="39e3d-104">Load4 (uint, uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="39e3d-104">Load4(uint,uint) function</span></span>

<span data-ttu-id="39e3d-105">Ruft vier Werte ab und gibt den Status des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="39e3d-105">Gets four values and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="39e3d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="39e3d-106">Syntax</span></span>


``` syntax
uint4 Load4(
  in  uint Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="39e3d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="39e3d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39e3d-108">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="39e3d-108">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39e3d-109">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="39e3d-109">Type: **uint**</span></span>

<span data-ttu-id="39e3d-110">Der Speicherort des Puffers.</span><span class="sxs-lookup"><span data-stu-id="39e3d-110">The location of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="39e3d-111">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="39e3d-111">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39e3d-112">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="39e3d-112">Type: **uint**</span></span>

<span data-ttu-id="39e3d-113">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="39e3d-113">The status of the operation.</span></span> <span data-ttu-id="39e3d-114">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="39e3d-114">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="39e3d-115">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="39e3d-115">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="39e3d-116">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="39e3d-116">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39e3d-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="39e3d-117">Return value</span></span>

<span data-ttu-id="39e3d-118">Typ: **uint4**</span><span class="sxs-lookup"><span data-stu-id="39e3d-118">Type: **uint4**</span></span>

<span data-ttu-id="39e3d-119">Vier Werte.</span><span class="sxs-lookup"><span data-stu-id="39e3d-119">Four values.</span></span>

## <a name="remarks"></a><span data-ttu-id="39e3d-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39e3d-120">Remarks</span></span>

<span data-ttu-id="39e3d-121">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="39e3d-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="39e3d-122">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="39e3d-122">Vertex</span></span> | <span data-ttu-id="39e3d-123">Hülle</span><span class="sxs-lookup"><span data-stu-id="39e3d-123">Hull</span></span> | <span data-ttu-id="39e3d-124">Domain</span><span class="sxs-lookup"><span data-stu-id="39e3d-124">Domain</span></span> | <span data-ttu-id="39e3d-125">Geometrie</span><span class="sxs-lookup"><span data-stu-id="39e3d-125">Geometry</span></span> | <span data-ttu-id="39e3d-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="39e3d-126">Pixel</span></span> | <span data-ttu-id="39e3d-127">Compute</span><span class="sxs-lookup"><span data-stu-id="39e3d-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="39e3d-128">x</span><span class="sxs-lookup"><span data-stu-id="39e3d-128">x</span></span>     | <span data-ttu-id="39e3d-129">x</span><span class="sxs-lookup"><span data-stu-id="39e3d-129">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="39e3d-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="39e3d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39e3d-131">Load4-Methoden</span><span class="sxs-lookup"><span data-stu-id="39e3d-131">Load4 methods</span></span>](rwbyteaddressbuffer-load4.md)
</dt> </dl>

 

 