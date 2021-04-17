---
title: 'Texture2DMS:: Load (int, int, int, uint)-Funktion'
description: 'Liest Textur Daten und gibt den Status des Vorgangs zurück. | Texture2DMS:: Load (int, int, int, uint)-Funktion'
ms.assetid: 4230962C-2968-4030-9770-8318F1760AEB
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
ms.openlocfilehash: e967d69929c0b20317ffb74fc97c4e60e36c2854
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352069"
---
# <a name="texture2dmsloadintintintuint-function"></a><span data-ttu-id="2890f-105">Texture2DMS:: Load (int, int, int, uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="2890f-105">Texture2DMS::Load(int,int,int,uint) function</span></span>

<span data-ttu-id="2890f-106">Liest Textur Daten und gibt den Status des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="2890f-106">Reads texture data and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="2890f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2890f-107">Syntax</span></span>


``` syntax
 Load(
  in  int2 Location,
  in  int  sampleindex,
  in  int2 Offset,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="2890f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2890f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2890f-109">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2890f-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2890f-110">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="2890f-110">Type: **int2**</span></span>

<span data-ttu-id="2890f-111">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="2890f-111">The texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="2890f-112">*sampleingedex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2890f-112">*sampleindex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2890f-113">Typ: **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2890f-113">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2890f-114">Der Beispiel Index.</span><span class="sxs-lookup"><span data-stu-id="2890f-114">The sample index.</span></span>

</dd> <dt>

<span data-ttu-id="2890f-115">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2890f-115">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2890f-116">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="2890f-116">Type: **int2**</span></span>

<span data-ttu-id="2890f-117">Ein Offset, der vor dem Laden auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="2890f-117">An offset applied to the texture coordinates before loading.</span></span>

</dd> <dt>

<span data-ttu-id="2890f-118">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2890f-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2890f-119">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="2890f-119">Type: **uint**</span></span>

<span data-ttu-id="2890f-120">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="2890f-120">The status of the operation.</span></span> <span data-ttu-id="2890f-121">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="2890f-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="2890f-122">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="2890f-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="2890f-123">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="2890f-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2890f-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2890f-124">Return value</span></span>

<span data-ttu-id="2890f-125">Typ:</span><span class="sxs-lookup"><span data-stu-id="2890f-125">Type:</span></span>

<span data-ttu-id="2890f-126">Der Rückgabetyp entspricht dem Typ in der Deklaration für das [**Texture2DMS**](sm5-object-texture2dms.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="2890f-126">The return type matches the type in the declaration for the [**Texture2DMS**](sm5-object-texture2dms.md) object.</span></span>

## <a name="see-also"></a><span data-ttu-id="2890f-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2890f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2890f-128">Lade Methoden</span><span class="sxs-lookup"><span data-stu-id="2890f-128">Load methods</span></span>](texture2dms-load.md)
</dt> <dt>

[<span data-ttu-id="2890f-129">**Texture2DMS**</span><span class="sxs-lookup"><span data-stu-id="2890f-129">**Texture2DMS**</span></span>](sm5-object-texture2dms.md)
</dt> </dl>

 

 
