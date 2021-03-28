---
title: 'Texture1D:: Load (int, int, uint)-Funktion'
description: 'Liest Textur Daten und gibt den Status des Vorgangs zurück. | Texture1D:: Load (int, int, uint)-Funktion'
ms.assetid: 5C489CBD-E4F6-4CB5-8E7E-EC34633D75B0
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
ms.openlocfilehash: 0c7733ab4802037d83dbb2b4ce523ff7bb57f729
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981617"
---
# <a name="texture1dloadintintuint-function"></a><span data-ttu-id="1f725-105">Texture1D:: Load (int, int, uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="1f725-105">Texture1D::Load(int,int,uint) function</span></span>

<span data-ttu-id="1f725-106">Liest Textur Daten und gibt den Status des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="1f725-106">Reads texture data and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f725-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f725-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  in  int  Offset,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="1f725-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f725-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f725-109">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1f725-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f725-110">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="1f725-110">Type: **int**</span></span>

<span data-ttu-id="1f725-111">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="1f725-111">The texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="1f725-112">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1f725-112">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f725-113">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="1f725-113">Type: **int**</span></span>

<span data-ttu-id="1f725-114">Ein Offset, der vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="1f725-114">An offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="1f725-115">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1f725-115">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f725-116">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="1f725-116">Type: **uint**</span></span>

<span data-ttu-id="1f725-117">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="1f725-117">The status of the operation.</span></span> <span data-ttu-id="1f725-118">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="1f725-118">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="1f725-119">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="1f725-119">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="1f725-120">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="1f725-120">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f725-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1f725-121">Return value</span></span>

<span data-ttu-id="1f725-122">Typ:</span><span class="sxs-lookup"><span data-stu-id="1f725-122">Type:</span></span>

<span data-ttu-id="1f725-123">Der Rückgabetyp entspricht dem Typ in der Deklaration für das [**Texture1D**](sm5-object-texture1d.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="1f725-123">The return type matches the type in the declaration for the [**Texture1D**](sm5-object-texture1d.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f725-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f725-124">Remarks</span></span>

<span data-ttu-id="1f725-125">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="1f725-125">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="1f725-126">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="1f725-126">Vertex</span></span> | <span data-ttu-id="1f725-127">Hülle</span><span class="sxs-lookup"><span data-stu-id="1f725-127">Hull</span></span> | <span data-ttu-id="1f725-128">Domain</span><span class="sxs-lookup"><span data-stu-id="1f725-128">Domain</span></span> | <span data-ttu-id="1f725-129">Geometrie</span><span class="sxs-lookup"><span data-stu-id="1f725-129">Geometry</span></span> | <span data-ttu-id="1f725-130">Pixel</span><span class="sxs-lookup"><span data-stu-id="1f725-130">Pixel</span></span> | <span data-ttu-id="1f725-131">Compute</span><span class="sxs-lookup"><span data-stu-id="1f725-131">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="1f725-132">x</span><span class="sxs-lookup"><span data-stu-id="1f725-132">x</span></span>      | <span data-ttu-id="1f725-133">x</span><span class="sxs-lookup"><span data-stu-id="1f725-133">x</span></span>    | <span data-ttu-id="1f725-134">x</span><span class="sxs-lookup"><span data-stu-id="1f725-134">x</span></span>      | <span data-ttu-id="1f725-135">x</span><span class="sxs-lookup"><span data-stu-id="1f725-135">x</span></span>        | <span data-ttu-id="1f725-136">x</span><span class="sxs-lookup"><span data-stu-id="1f725-136">x</span></span>     | <span data-ttu-id="1f725-137">x</span><span class="sxs-lookup"><span data-stu-id="1f725-137">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="1f725-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1f725-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f725-139">Lade Methoden</span><span class="sxs-lookup"><span data-stu-id="1f725-139">Load methods</span></span>](texture1d-load.md)
</dt> <dt>

[<span data-ttu-id="1f725-140">**Texture1D**</span><span class="sxs-lookup"><span data-stu-id="1f725-140">**Texture1D**</span></span>](sm5-object-texture1d.md)
</dt> </dl>

 

 
