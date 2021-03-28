---
title: 'RWTexture1D:: Load (int, uint)-Funktion'
description: 'Liest Textur Daten und gibt den Status des Vorgangs zurück. | RWTexture1D:: Load (int, uint)-Funktion'
ms.assetid: 3BF2397D-400C-48EE-8D45-872BA61F007B
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
ms.openlocfilehash: afba9445d152810e5776ae0ee7f603bb7ee55ac2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981248"
---
# <a name="rwtexture1dloadintuint-function"></a><span data-ttu-id="8503a-105">RWTexture1D:: Load (int, uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="8503a-105">RWTexture1D::Load(int,uint) function</span></span>

<span data-ttu-id="8503a-106">Liest Textur Daten und gibt den Status des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="8503a-106">Reads texture data and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="8503a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8503a-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="8503a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8503a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8503a-109">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8503a-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8503a-110">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="8503a-110">Type: **int**</span></span>

<span data-ttu-id="8503a-111">Der Speicherort der Textur.</span><span class="sxs-lookup"><span data-stu-id="8503a-111">The location of the texture.</span></span>

</dd> <dt>

<span data-ttu-id="8503a-112">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8503a-112">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8503a-113">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="8503a-113">Type: **uint**</span></span>

<span data-ttu-id="8503a-114">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="8503a-114">The status of the operation.</span></span> <span data-ttu-id="8503a-115">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="8503a-115">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="8503a-116">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="8503a-116">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="8503a-117">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="8503a-117">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8503a-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8503a-118">Return value</span></span>

<span data-ttu-id="8503a-119">Typ:</span><span class="sxs-lookup"><span data-stu-id="8503a-119">Type:</span></span>

<span data-ttu-id="8503a-120">Der Rückgabetyp entspricht dem Typ in der Deklaration für das [**RWTexture1D**](sm5-object-rwtexture1d.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="8503a-120">The return type matches the type in the declaration for the [**RWTexture1D**](sm5-object-rwtexture1d.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8503a-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8503a-121">Remarks</span></span>

<span data-ttu-id="8503a-122">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="8503a-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="8503a-123">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="8503a-123">Vertex</span></span> | <span data-ttu-id="8503a-124">Hülle</span><span class="sxs-lookup"><span data-stu-id="8503a-124">Hull</span></span> | <span data-ttu-id="8503a-125">Domain</span><span class="sxs-lookup"><span data-stu-id="8503a-125">Domain</span></span> | <span data-ttu-id="8503a-126">Geometrie</span><span class="sxs-lookup"><span data-stu-id="8503a-126">Geometry</span></span> | <span data-ttu-id="8503a-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="8503a-127">Pixel</span></span> | <span data-ttu-id="8503a-128">Compute</span><span class="sxs-lookup"><span data-stu-id="8503a-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="8503a-129">x</span><span class="sxs-lookup"><span data-stu-id="8503a-129">x</span></span>     | <span data-ttu-id="8503a-130">x</span><span class="sxs-lookup"><span data-stu-id="8503a-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="8503a-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8503a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8503a-132">Lade Methoden</span><span class="sxs-lookup"><span data-stu-id="8503a-132">Load methods</span></span>](rwtexture1d-load.md)
</dt> </dl>

 

 
