---
title: 'RWTexture2DArray:: Load (int, uint)-Funktion'
description: 'Liest Textur Daten und gibt den Status des Vorgangs zurück. | RWTexture2DArray:: Load (int, uint)-Funktion'
ms.assetid: 97D6E36A-1613-43BA-92C1-3034E0F344F0
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
ms.openlocfilehash: 969aa0a4efa62f7072c759a1f2188e4d210d8649
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981641"
---
# <a name="rwtexture2darrayloadintuint-function"></a><span data-ttu-id="8f6bc-105">RWTexture2DArray:: Load (int, uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="8f6bc-105">RWTexture2DArray::Load(int,uint) function</span></span>

<span data-ttu-id="8f6bc-106">Liest Textur Daten und gibt den Status des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="8f6bc-106">Reads texture data and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f6bc-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f6bc-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="8f6bc-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f6bc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f6bc-109">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8f6bc-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f6bc-110">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="8f6bc-110">Type: **int**</span></span>

<span data-ttu-id="8f6bc-111">Der Speicherort der Textur.</span><span class="sxs-lookup"><span data-stu-id="8f6bc-111">The location of the texture.</span></span>

</dd> <dt>

<span data-ttu-id="8f6bc-112">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8f6bc-112">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f6bc-113">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="8f6bc-113">Type: **uint**</span></span>

<span data-ttu-id="8f6bc-114">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="8f6bc-114">The status of the operation.</span></span> <span data-ttu-id="8f6bc-115">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="8f6bc-115">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="8f6bc-116">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="8f6bc-116">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="8f6bc-117">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="8f6bc-117">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f6bc-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8f6bc-118">Return value</span></span>

<span data-ttu-id="8f6bc-119">Typ:</span><span class="sxs-lookup"><span data-stu-id="8f6bc-119">Type:</span></span>

<span data-ttu-id="8f6bc-120">Der Rückgabetyp entspricht dem Typ in der Deklaration für das [**RWTexture2DArray**](sm5-object-rwtexture2darray.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="8f6bc-120">The return type matches the type in the declaration for the [**RWTexture2DArray**](sm5-object-rwtexture2darray.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f6bc-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8f6bc-121">Remarks</span></span>

<span data-ttu-id="8f6bc-122">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="8f6bc-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="8f6bc-123">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="8f6bc-123">Vertex</span></span> | <span data-ttu-id="8f6bc-124">Hülle</span><span class="sxs-lookup"><span data-stu-id="8f6bc-124">Hull</span></span> | <span data-ttu-id="8f6bc-125">Domain</span><span class="sxs-lookup"><span data-stu-id="8f6bc-125">Domain</span></span> | <span data-ttu-id="8f6bc-126">Geometrie</span><span class="sxs-lookup"><span data-stu-id="8f6bc-126">Geometry</span></span> | <span data-ttu-id="8f6bc-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="8f6bc-127">Pixel</span></span> | <span data-ttu-id="8f6bc-128">Compute</span><span class="sxs-lookup"><span data-stu-id="8f6bc-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="8f6bc-129">x</span><span class="sxs-lookup"><span data-stu-id="8f6bc-129">x</span></span>     | <span data-ttu-id="8f6bc-130">x</span><span class="sxs-lookup"><span data-stu-id="8f6bc-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="8f6bc-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8f6bc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f6bc-132">Lade Methoden</span><span class="sxs-lookup"><span data-stu-id="8f6bc-132">Load methods</span></span>](rwtexture2darray-load.md)
</dt> </dl>

 

 
