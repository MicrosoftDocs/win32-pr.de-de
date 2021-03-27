---
title: 'RWTexture1DArray:: Load (int, uint)-Funktion'
description: 'Liest Textur Daten und gibt den Status des Vorgangs zurück. | RWTexture1DArray:: Load (int, uint)-Funktion'
ms.assetid: EF1D51CC-E037-4E04-9DD6-6A9C5950E5B5
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
ms.openlocfilehash: 5a46dde9b75d3194cc081409fe2b450c5453d7c1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981240"
---
# <a name="rwtexture1darrayloadintuint-function"></a><span data-ttu-id="ad660-105">RWTexture1DArray:: Load (int, uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="ad660-105">RWTexture1DArray::Load(int,uint) function</span></span>

<span data-ttu-id="ad660-106">Liest Textur Daten und gibt den Status des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="ad660-106">Reads texture data and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad660-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad660-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="ad660-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad660-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad660-109">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ad660-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad660-110">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="ad660-110">Type: **int**</span></span>

<span data-ttu-id="ad660-111">Der Speicherort der Textur.</span><span class="sxs-lookup"><span data-stu-id="ad660-111">The location of the texture.</span></span>

</dd> <dt>

<span data-ttu-id="ad660-112">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ad660-112">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad660-113">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="ad660-113">Type: **uint**</span></span>

<span data-ttu-id="ad660-114">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="ad660-114">The status of the operation.</span></span> <span data-ttu-id="ad660-115">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="ad660-115">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="ad660-116">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="ad660-116">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="ad660-117">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="ad660-117">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad660-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ad660-118">Return value</span></span>

<span data-ttu-id="ad660-119">Typ:</span><span class="sxs-lookup"><span data-stu-id="ad660-119">Type:</span></span>

<span data-ttu-id="ad660-120">Der Rückgabetyp entspricht dem Typ in der Deklaration für das [**RWTexture1DArray**](sm5-object-rwtexture1darray.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="ad660-120">The return type matches the type in the declaration for the [**RWTexture1DArray**](sm5-object-rwtexture1darray.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad660-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ad660-121">Remarks</span></span>

<span data-ttu-id="ad660-122">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="ad660-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="ad660-123">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="ad660-123">Vertex</span></span> | <span data-ttu-id="ad660-124">Hülle</span><span class="sxs-lookup"><span data-stu-id="ad660-124">Hull</span></span> | <span data-ttu-id="ad660-125">Domain</span><span class="sxs-lookup"><span data-stu-id="ad660-125">Domain</span></span> | <span data-ttu-id="ad660-126">Geometrie</span><span class="sxs-lookup"><span data-stu-id="ad660-126">Geometry</span></span> | <span data-ttu-id="ad660-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="ad660-127">Pixel</span></span> | <span data-ttu-id="ad660-128">Compute</span><span class="sxs-lookup"><span data-stu-id="ad660-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="ad660-129">x</span><span class="sxs-lookup"><span data-stu-id="ad660-129">x</span></span>     | <span data-ttu-id="ad660-130">x</span><span class="sxs-lookup"><span data-stu-id="ad660-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ad660-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ad660-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad660-132">Lade Methoden</span><span class="sxs-lookup"><span data-stu-id="ad660-132">Load methods</span></span>](rwtexture1darray-load.md)
</dt> </dl>

 

 
