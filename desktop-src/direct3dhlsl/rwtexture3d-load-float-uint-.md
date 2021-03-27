---
title: 'RWTexture3D:: Load (int, uint)-Funktion'
description: 'Liest Textur Daten und gibt den Status des Vorgangs zurück. | RWTexture3D:: Load (int, uint)-Funktion'
ms.assetid: 7BC334D3-217A-454F-B205-A9D7D66B5E99
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
ms.openlocfilehash: 69b70f6db45a9020e558fadcd1347cc29948ed46
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981208"
---
# <a name="rwtexture3dloadintuint-function"></a><span data-ttu-id="bc982-105">RWTexture3D:: Load (int, uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="bc982-105">RWTexture3D::Load(int,uint) function</span></span>

<span data-ttu-id="bc982-106">Liest Textur Daten und gibt den Status des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="bc982-106">Reads texture data and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc982-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc982-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="bc982-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc982-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc982-109">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc982-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc982-110">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="bc982-110">Type: **int**</span></span>

<span data-ttu-id="bc982-111">Der Speicherort der Textur.</span><span class="sxs-lookup"><span data-stu-id="bc982-111">The location of the texture.</span></span>

</dd> <dt>

<span data-ttu-id="bc982-112">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bc982-112">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc982-113">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="bc982-113">Type: **uint**</span></span>

<span data-ttu-id="bc982-114">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="bc982-114">The status of the operation.</span></span> <span data-ttu-id="bc982-115">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="bc982-115">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="bc982-116">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="bc982-116">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="bc982-117">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="bc982-117">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc982-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bc982-118">Return value</span></span>

<span data-ttu-id="bc982-119">Typ:</span><span class="sxs-lookup"><span data-stu-id="bc982-119">Type:</span></span>

<span data-ttu-id="bc982-120">Der Rückgabetyp entspricht dem Typ in der Deklaration für das [**RWTexture3D**](sm5-object-rwtexture3d.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="bc982-120">The return type matches the type in the declaration for the [**RWTexture3D**](sm5-object-rwtexture3d.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc982-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bc982-121">Remarks</span></span>

<span data-ttu-id="bc982-122">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="bc982-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="bc982-123">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="bc982-123">Vertex</span></span> | <span data-ttu-id="bc982-124">Hülle</span><span class="sxs-lookup"><span data-stu-id="bc982-124">Hull</span></span> | <span data-ttu-id="bc982-125">Domain</span><span class="sxs-lookup"><span data-stu-id="bc982-125">Domain</span></span> | <span data-ttu-id="bc982-126">Geometrie</span><span class="sxs-lookup"><span data-stu-id="bc982-126">Geometry</span></span> | <span data-ttu-id="bc982-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="bc982-127">Pixel</span></span> | <span data-ttu-id="bc982-128">Compute</span><span class="sxs-lookup"><span data-stu-id="bc982-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="bc982-129">x</span><span class="sxs-lookup"><span data-stu-id="bc982-129">x</span></span>     | <span data-ttu-id="bc982-130">x</span><span class="sxs-lookup"><span data-stu-id="bc982-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="bc982-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="bc982-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc982-132">Lade Methoden</span><span class="sxs-lookup"><span data-stu-id="bc982-132">Load methods</span></span>](rwtexture3d-load.md)
</dt> </dl>

 

 
