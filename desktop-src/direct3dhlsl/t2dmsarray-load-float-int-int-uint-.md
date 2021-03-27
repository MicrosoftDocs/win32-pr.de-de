---
title: 'Texture2DMSArray:: Load (int, int, int, uint)-Funktion'
description: 'Liest Textur Daten und gibt den Status des Vorgangs zurück. | Texture2DMSArray:: Load (int, int, int, uint)-Funktion'
ms.assetid: F5EA2FFF-7E43-4A34-9358-EA54382641DC
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
ms.openlocfilehash: 0065ee5e420c67876b87c67be1f5e5c8ff10e65b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995350"
---
# <a name="texture2dmsarrayloadintintintuint-function"></a><span data-ttu-id="59176-105">Texture2DMSArray:: Load (int, int, int, uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="59176-105">Texture2DMSArray::Load(int,int,int,uint) function</span></span>

<span data-ttu-id="59176-106">Liest Textur Daten und gibt den Status des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="59176-106">Reads texture data and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="59176-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="59176-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  in  int  sampleindex,
  in  int  Offset,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="59176-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="59176-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59176-109">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59176-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59176-110">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="59176-110">Type: **int**</span></span>

<span data-ttu-id="59176-111">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="59176-111">The texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="59176-112">*sampleingedex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59176-112">*sampleindex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59176-113">Typ: **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="59176-113">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="59176-114">Der Beispiel Index.</span><span class="sxs-lookup"><span data-stu-id="59176-114">The sample index.</span></span>

</dd> <dt>

<span data-ttu-id="59176-115">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59176-115">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59176-116">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="59176-116">Type: **int**</span></span>

<span data-ttu-id="59176-117">Ein Offset, der vor dem Sampling auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="59176-117">An offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="59176-118">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="59176-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59176-119">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="59176-119">Type: **uint**</span></span>

<span data-ttu-id="59176-120">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="59176-120">The status of the operation.</span></span> <span data-ttu-id="59176-121">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="59176-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="59176-122">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="59176-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="59176-123">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="59176-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59176-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="59176-124">Return value</span></span>

<span data-ttu-id="59176-125">Typ:</span><span class="sxs-lookup"><span data-stu-id="59176-125">Type:</span></span>

<span data-ttu-id="59176-126">Der Rückgabetyp entspricht dem Typ in der Deklaration für das [**Texture2DMSArray**](sm5-object-texture2dmsarray.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="59176-126">The return type matches the type in the declaration for the [**Texture2DMSArray**](sm5-object-texture2dmsarray.md) object.</span></span>

## <a name="see-also"></a><span data-ttu-id="59176-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="59176-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59176-128">Lade Methoden</span><span class="sxs-lookup"><span data-stu-id="59176-128">Load methods</span></span>](texture2dmsarray-load.md)
</dt> <dt>

[<span data-ttu-id="59176-129">**Texture2DMSArray**</span><span class="sxs-lookup"><span data-stu-id="59176-129">**Texture2DMSArray**</span></span>](sm5-object-texture2dmsarray.md)
</dt> </dl>

 

 
