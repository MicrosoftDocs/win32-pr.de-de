---
description: Die Bitflag-Konstanten von linedialtonemode \_ beschreiben verschiedene Typen von Wähltönen. Ein spezieller Wählton weist in der Regel eine besondere Bedeutung auf (wie beim Warten auf die Nachricht).
ms.assetid: 0b040482-35cf-42e8-84bc-33002635b591
title: LINEDIALTONEMODE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5128f2a176f3aeaf92bc3487b131b7720568085e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360297"
---
# <a name="linedialtonemode_-constants"></a><span data-ttu-id="8c84e-104">Linedialtonemode- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="8c84e-104">LINEDIALTONEMODE\_ Constants</span></span>

<span data-ttu-id="8c84e-105">Die Bitflag-Konstanten von **linedialtonemode \_** beschreiben verschiedene Typen von Wähltönen.</span><span class="sxs-lookup"><span data-stu-id="8c84e-105">The **LINEDIALTONEMODE\_** bit-flag constants describe different types of dial tones.</span></span> <span data-ttu-id="8c84e-106">Ein spezieller Wählton weist in der Regel eine besondere Bedeutung auf (wie beim Warten auf die Nachricht).</span><span class="sxs-lookup"><span data-stu-id="8c84e-106">A special dial tone typically carries a special meaning (as with message waiting).</span></span>

<dl> <dt>

<span data-ttu-id="8c84e-107"><span id="LINEDIALTONEMODE_EXTERNAL"></span><span id="linedialtonemode_external"></span>**linedialtonemode \_ extern**</span><span class="sxs-lookup"><span data-stu-id="8c84e-107"><span id="LINEDIALTONEMODE_EXTERNAL"></span><span id="linedialtonemode_external"></span>**LINEDIALTONEMODE\_EXTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8c84e-108">Dies ist ein externer (öffentlicher Netzwerk) Wählton.</span><span class="sxs-lookup"><span data-stu-id="8c84e-108">This is an external (public network) dial tone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8c84e-109"><span id="LINEDIALTONEMODE_INTERNAL"></span><span id="linedialtonemode_internal"></span>**linedialtonemode \_ intern**</span><span class="sxs-lookup"><span data-stu-id="8c84e-109"><span id="LINEDIALTONEMODE_INTERNAL"></span><span id="linedialtonemode_internal"></span>**LINEDIALTONEMODE\_INTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8c84e-110">Dies ist ein interner Wählton, wie in einer PBX.</span><span class="sxs-lookup"><span data-stu-id="8c84e-110">This is an internal dial tone, as within a PBX.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8c84e-111"><span id="LINEDIALTONEMODE_NORMAL"></span><span id="linedialtonemode_normal"></span>**linedialtonemode \_ Normal**</span><span class="sxs-lookup"><span data-stu-id="8c84e-111"><span id="LINEDIALTONEMODE_NORMAL"></span><span id="linedialtonemode_normal"></span>**LINEDIALTONEMODE\_NORMAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8c84e-112">Dies ist ein normaler Wählton, bei dem es sich in der Regel um einen kontinuierlichen Ton handelt.</span><span class="sxs-lookup"><span data-stu-id="8c84e-112">This is a normal dial tone, which typically is a continuous tone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8c84e-113"><span id="LINEDIALTONEMODE_SPECIAL"></span><span id="linedialtonemode_special"></span>**linedialtonemode \_ Special**</span><span class="sxs-lookup"><span data-stu-id="8c84e-113"><span id="LINEDIALTONEMODE_SPECIAL"></span><span id="linedialtonemode_special"></span>**LINEDIALTONEMODE\_SPECIAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8c84e-114">Dies ist ein spezieller Wählton, der angibt, dass eine bestimmte Bedingung (die vom Switch oder Netzwerk bekannt ist) zurzeit wirksam ist.</span><span class="sxs-lookup"><span data-stu-id="8c84e-114">This is a special dial tone indicating that a certain condition (known by the switch or network) is currently in effect.</span></span> <span data-ttu-id="8c84e-115">Bei speziellen Wähltönen wird normalerweise ein unterbrochener Ton verwendet.</span><span class="sxs-lookup"><span data-stu-id="8c84e-115">Special dial tones typically use an interrupted tone.</span></span> <span data-ttu-id="8c84e-116">Wie bei einem normalen Wählton zeigt dies an, dass der Switch zum Empfangen der zu wählenden Zahl bereit ist.</span><span class="sxs-lookup"><span data-stu-id="8c84e-116">As with a normal dial tone, this indicates that the switch is ready to receive the number to be dialed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8c84e-117"><span id="LINEDIALTONEMODE_UNAVAIL"></span><span id="linedialtonemode_unavail"></span>**"linedialtonemode" \_ nicht verfügbar**</span><span class="sxs-lookup"><span data-stu-id="8c84e-117"><span id="LINEDIALTONEMODE_UNAVAIL"></span><span id="linedialtonemode_unavail"></span>**LINEDIALTONEMODE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8c84e-118">Der Wähl Modus ist nicht verfügbar und wird nicht bekannt.</span><span class="sxs-lookup"><span data-stu-id="8c84e-118">The dial tone mode is unavailable and will not become known.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8c84e-119"><span id="LINEDIALTONEMODE_UNKNOWN"></span><span id="linedialtonemode_unknown"></span>**"linedialtonemode" ist \_ unbekannt.**</span><span class="sxs-lookup"><span data-stu-id="8c84e-119"><span id="LINEDIALTONEMODE_UNKNOWN"></span><span id="linedialtonemode_unknown"></span>**LINEDIALTONEMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8c84e-120">Der Dial-Tone-Modus ist zurzeit nicht bekannt, kann aber später bekannt werden.</span><span class="sxs-lookup"><span data-stu-id="8c84e-120">The dial tone mode is not currently known but may become known later.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8c84e-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8c84e-121">Remarks</span></span>

<span data-ttu-id="8c84e-122">Die höherwertigen 16 Bits können für gerätespezifische Erweiterungen zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="8c84e-122">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="8c84e-123">Die nieder wertigen 16 Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="8c84e-123">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="8c84e-124">Die **linedialtonemode- \_ Konstanten** werden in der [**linecallstatus**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) -Datenstruktur für einen-Rückruf im dialtoneverfahren-Zustand verwendet.</span><span class="sxs-lookup"><span data-stu-id="8c84e-124">The **LINEDIALTONEMODE\_constants** are used within the [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) data structure for a call in the dialtone state.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c84e-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8c84e-125">Requirements</span></span>



| <span data-ttu-id="8c84e-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8c84e-126">Requirement</span></span> | <span data-ttu-id="8c84e-127">Wert</span><span class="sxs-lookup"><span data-stu-id="8c84e-127">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="8c84e-128">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="8c84e-128">TAPI version</span></span><br/> | <span data-ttu-id="8c84e-129">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="8c84e-129">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="8c84e-130">Header</span><span class="sxs-lookup"><span data-stu-id="8c84e-130">Header</span></span><br/>       | <dl> <span data-ttu-id="8c84e-131"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c84e-131"><dt>Tapi.h</dt></span></span> </dl> |



 

 




