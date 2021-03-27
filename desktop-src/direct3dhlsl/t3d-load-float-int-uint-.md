---
title: 'Texture3D:: Load (int, int, uint)-Funktion'
description: 'Liest Textur Daten und gibt den Status des Vorgangs zurück. | Texture3D:: Load (int, int, uint)-Funktion'
ms.assetid: 3F562ADB-225F-462B-A7AC-40797BBB632A
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
ms.openlocfilehash: 19522fe60567e55565265ce0c8b5051c7bf7ccdd
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995326"
---
# <a name="texture3dloadintintuint-function"></a><span data-ttu-id="f64cd-105">Texture3D:: Load (int, int, uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="f64cd-105">Texture3D::Load(int,int,uint) function</span></span>

<span data-ttu-id="f64cd-106">Liest Textur Daten und gibt den Status des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="f64cd-106">Reads texture data and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="f64cd-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f64cd-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  in  int  Offset,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="f64cd-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f64cd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f64cd-109">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f64cd-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f64cd-110">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="f64cd-110">Type: **int**</span></span>

<span data-ttu-id="f64cd-111">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="f64cd-111">The texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="f64cd-112">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f64cd-112">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f64cd-113">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="f64cd-113">Type: **int**</span></span>

<span data-ttu-id="f64cd-114">Ein Offset, der vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="f64cd-114">An offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="f64cd-115">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f64cd-115">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f64cd-116">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="f64cd-116">Type: **uint**</span></span>

<span data-ttu-id="f64cd-117">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="f64cd-117">The status of the operation.</span></span> <span data-ttu-id="f64cd-118">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="f64cd-118">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="f64cd-119">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="f64cd-119">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="f64cd-120">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="f64cd-120">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f64cd-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f64cd-121">Return value</span></span>

<span data-ttu-id="f64cd-122">Typ:</span><span class="sxs-lookup"><span data-stu-id="f64cd-122">Type:</span></span>

<span data-ttu-id="f64cd-123">Der Rückgabetyp entspricht dem Typ in der Deklaration für das [**Texture3D**](sm5-object-texture3d.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="f64cd-123">The return type matches the type in the declaration for the [**Texture3D**](sm5-object-texture3d.md) object.</span></span>

## <a name="see-also"></a><span data-ttu-id="f64cd-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f64cd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f64cd-125">Lade Methoden</span><span class="sxs-lookup"><span data-stu-id="f64cd-125">Load methods</span></span>](texture3d-load.md)
</dt> <dt>

[<span data-ttu-id="f64cd-126">**Texture3D**</span><span class="sxs-lookup"><span data-stu-id="f64cd-126">**Texture3D**</span></span>](sm5-object-texture3d.md)
</dt> </dl>

 

 
