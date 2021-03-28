---
title: 'Structuredbuffer:: Load (int, uint)-Funktion'
description: 'Liest Puffer Daten und gibt den Status des Vorgangs zurück. | Structuredbuffer:: Load (int, uint)-Funktion'
ms.assetid: d71c6057-6651-4b70-91cf-892fde6d0188
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
ms.openlocfilehash: 957b85631bbd19742cb7afe52f6bf061de323614
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219226"
---
# <a name="structuredbufferloadintuint-function"></a><span data-ttu-id="9b49f-105">Structuredbuffer:: Load (int, uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="9b49f-105">StructuredBuffer::Load(int,uint) function</span></span>

<span data-ttu-id="9b49f-106">Liest Puffer Daten und gibt den Status des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="9b49f-106">Reads buffer data and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b49f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b49f-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="9b49f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b49f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b49f-109">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9b49f-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b49f-110">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="9b49f-110">Type: **int**</span></span>

<span data-ttu-id="9b49f-111">Der Speicherort des Puffers.</span><span class="sxs-lookup"><span data-stu-id="9b49f-111">The location of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="9b49f-112">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9b49f-112">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b49f-113">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="9b49f-113">Type: **uint**</span></span>

<span data-ttu-id="9b49f-114">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="9b49f-114">The status of the operation.</span></span> <span data-ttu-id="9b49f-115">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="9b49f-115">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="9b49f-116">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="9b49f-116">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="9b49f-117">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="9b49f-117">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b49f-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9b49f-118">Return value</span></span>

<span data-ttu-id="9b49f-119">Typ:</span><span class="sxs-lookup"><span data-stu-id="9b49f-119">Type:</span></span>

<span data-ttu-id="9b49f-120">Der Rückgabetyp entspricht dem Typ in der Deklaration für das [**structuredbuffer**](sm5-object-structuredbuffer.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="9b49f-120">The return type matches the type in the declaration for the [**StructuredBuffer**](sm5-object-structuredbuffer.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b49f-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9b49f-121">Remarks</span></span>

<span data-ttu-id="9b49f-122">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="9b49f-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="9b49f-123">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="9b49f-123">Vertex</span></span> | <span data-ttu-id="9b49f-124">Hülle</span><span class="sxs-lookup"><span data-stu-id="9b49f-124">Hull</span></span> | <span data-ttu-id="9b49f-125">Domain</span><span class="sxs-lookup"><span data-stu-id="9b49f-125">Domain</span></span> | <span data-ttu-id="9b49f-126">Geometrie</span><span class="sxs-lookup"><span data-stu-id="9b49f-126">Geometry</span></span> | <span data-ttu-id="9b49f-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="9b49f-127">Pixel</span></span> | <span data-ttu-id="9b49f-128">Compute</span><span class="sxs-lookup"><span data-stu-id="9b49f-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="9b49f-129">x</span><span class="sxs-lookup"><span data-stu-id="9b49f-129">x</span></span>     | <span data-ttu-id="9b49f-130">x</span><span class="sxs-lookup"><span data-stu-id="9b49f-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="9b49f-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9b49f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b49f-132">Lade Methoden</span><span class="sxs-lookup"><span data-stu-id="9b49f-132">Load methods</span></span>](structuredbuffer-load.md)
</dt> </dl>

 

 
