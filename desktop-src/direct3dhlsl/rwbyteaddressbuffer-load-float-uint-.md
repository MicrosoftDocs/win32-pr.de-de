---
title: 'Rwbyteaddressbuffer:: Load (int, uint)-Funktion'
description: Ruft einen Wert ab und gibt den Status des Vorgangs zurück.
ms.assetid: E3FD0FFA-6A9B-4B44-A90D-47270326F9BA
keywords:
- Ladefunktion HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 71f142d35ae8be3800ccf85b5e8114d5e85c44ac
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103858574"
---
# <a name="rwbyteaddressbufferloadintuint-function"></a><span data-ttu-id="e31a6-104">Rwbyteaddressbuffer:: Load (int, uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="e31a6-104">RWByteAddressBuffer::Load(int,uint) function</span></span>

<span data-ttu-id="e31a6-105">Ruft einen Wert ab und gibt den Status des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="e31a6-105">Gets one value and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="e31a6-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e31a6-106">Syntax</span></span>


``` syntax
uint Load(
  in  int  Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="e31a6-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e31a6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e31a6-108">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e31a6-108">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e31a6-109">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="e31a6-109">Type: **int**</span></span>

<span data-ttu-id="e31a6-110">Der Speicherort des Puffers.</span><span class="sxs-lookup"><span data-stu-id="e31a6-110">The location of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="e31a6-111">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e31a6-111">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e31a6-112">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="e31a6-112">Type: **uint**</span></span>

<span data-ttu-id="e31a6-113">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="e31a6-113">The status of the operation.</span></span> <span data-ttu-id="e31a6-114">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="e31a6-114">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="e31a6-115">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="e31a6-115">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="e31a6-116">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="e31a6-116">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e31a6-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e31a6-117">Return value</span></span>

<span data-ttu-id="e31a6-118">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="e31a6-118">Type: **uint**</span></span>

<span data-ttu-id="e31a6-119">Ein-Wert.</span><span class="sxs-lookup"><span data-stu-id="e31a6-119">One value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e31a6-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e31a6-120">Remarks</span></span>

<span data-ttu-id="e31a6-121">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="e31a6-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="e31a6-122">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="e31a6-122">Vertex</span></span> | <span data-ttu-id="e31a6-123">Hülle</span><span class="sxs-lookup"><span data-stu-id="e31a6-123">Hull</span></span> | <span data-ttu-id="e31a6-124">Domain</span><span class="sxs-lookup"><span data-stu-id="e31a6-124">Domain</span></span> | <span data-ttu-id="e31a6-125">Geometrie</span><span class="sxs-lookup"><span data-stu-id="e31a6-125">Geometry</span></span> | <span data-ttu-id="e31a6-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="e31a6-126">Pixel</span></span> | <span data-ttu-id="e31a6-127">Compute</span><span class="sxs-lookup"><span data-stu-id="e31a6-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="e31a6-128">x</span><span class="sxs-lookup"><span data-stu-id="e31a6-128">x</span></span>     | <span data-ttu-id="e31a6-129">x</span><span class="sxs-lookup"><span data-stu-id="e31a6-129">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="e31a6-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e31a6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e31a6-131">Lade Methoden</span><span class="sxs-lookup"><span data-stu-id="e31a6-131">Load methods</span></span>](rwbyteaddressbuffer-load.md)
</dt> </dl>

 

 
