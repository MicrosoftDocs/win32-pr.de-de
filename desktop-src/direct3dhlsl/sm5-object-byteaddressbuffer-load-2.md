---
title: 'Byteaddressbuffer:: Load (int, uint)-Funktion'
description: Ruft einen Wert und den Status des Vorgangs ab.
ms.assetid: 8F90671B-CEEB-4F8C-9469-D85940568872
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
ms.openlocfilehash: 319daad35da0256a4d36ef4580df62fd4d295854
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102647"
---
# <a name="byteaddressbufferloadint-uint-function"></a><span data-ttu-id="8fda3-104">Byteaddressbuffer:: Load (int, uint)-Funktion</span><span class="sxs-lookup"><span data-stu-id="8fda3-104">ByteAddressBuffer::Load(int, uint) function</span></span>

<span data-ttu-id="8fda3-105">Ruft einen Wert und den Status des Vorgangs ab.</span><span class="sxs-lookup"><span data-stu-id="8fda3-105">Gets one value and the status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fda3-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8fda3-106">Syntax</span></span>

``` syntax
uint Load(
  in  int Location,
  out uint Status
);
```

## <a name="parameters"></a><span data-ttu-id="8fda3-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8fda3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fda3-108">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8fda3-108">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fda3-109">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="8fda3-109">Type: **int**</span></span>

<span data-ttu-id="8fda3-110">Die Eingabe Adresse in Byte, bei der es sich um ein Vielfaches von 4 handeln muss.</span><span class="sxs-lookup"><span data-stu-id="8fda3-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="8fda3-111">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8fda3-111">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8fda3-112">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="8fda3-112">Type: **uint**</span></span>

<span data-ttu-id="8fda3-113">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="8fda3-113">The status of the operation.</span></span> <span data-ttu-id="8fda3-114">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="8fda3-114">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="8fda3-115">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="8fda3-115">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="8fda3-116">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="8fda3-116">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fda3-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8fda3-117">Return value</span></span>

<span data-ttu-id="8fda3-118">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="8fda3-118">Type: **uint**</span></span>

<span data-ttu-id="8fda3-119">Ein-Wert.</span><span class="sxs-lookup"><span data-stu-id="8fda3-119">One value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fda3-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8fda3-120">Remarks</span></span>

<span data-ttu-id="8fda3-121">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="8fda3-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="8fda3-122">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="8fda3-122">Vertex</span></span> | <span data-ttu-id="8fda3-123">Hülle</span><span class="sxs-lookup"><span data-stu-id="8fda3-123">Hull</span></span> | <span data-ttu-id="8fda3-124">Domain</span><span class="sxs-lookup"><span data-stu-id="8fda3-124">Domain</span></span> | <span data-ttu-id="8fda3-125">Geometrie</span><span class="sxs-lookup"><span data-stu-id="8fda3-125">Geometry</span></span> | <span data-ttu-id="8fda3-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="8fda3-126">Pixel</span></span> | <span data-ttu-id="8fda3-127">Compute</span><span class="sxs-lookup"><span data-stu-id="8fda3-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="8fda3-128">x</span><span class="sxs-lookup"><span data-stu-id="8fda3-128">x</span></span>      | <span data-ttu-id="8fda3-129">x</span><span class="sxs-lookup"><span data-stu-id="8fda3-129">x</span></span>    | <span data-ttu-id="8fda3-130">x</span><span class="sxs-lookup"><span data-stu-id="8fda3-130">x</span></span>      | <span data-ttu-id="8fda3-131">x</span><span class="sxs-lookup"><span data-stu-id="8fda3-131">x</span></span>        | <span data-ttu-id="8fda3-132">x</span><span class="sxs-lookup"><span data-stu-id="8fda3-132">x</span></span>     | <span data-ttu-id="8fda3-133">x</span><span class="sxs-lookup"><span data-stu-id="8fda3-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="8fda3-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8fda3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fda3-135">Lade Methoden</span><span class="sxs-lookup"><span data-stu-id="8fda3-135">Load methods</span></span>](byteaddressbuffer-load.md)
</dt> <dt>

[<span data-ttu-id="8fda3-136">**Byteaddressbuffer**</span><span class="sxs-lookup"><span data-stu-id="8fda3-136">**ByteAddressBuffer**</span></span>](sm5-object-byteaddressbuffer.md)
</dt> </dl>

 

 
