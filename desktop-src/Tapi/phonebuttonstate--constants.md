---
description: Die "phonebuttonstate"-bitflagkonstanten beschreiben die Positionen der Schaltflächen.
ms.assetid: f1196e31-65c6-4ade-a0b7-c7758ce97be1
title: PHONEBUTTONSTATE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b1cc2f669fb5c1171834f46e11a161e9390eab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365439"
---
# <a name="phonebuttonstate_-constants"></a><span data-ttu-id="59431-103">PHONEBUTTONSTATE_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="59431-103">PHONEBUTTONSTATE_ Constants</span></span>

<span data-ttu-id="59431-104">Die **PHONEBUTTONSTATE_** bitflagkonstanten beschreiben die Positionen der Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="59431-104">The **PHONEBUTTONSTATE_** bit-flag constants describe the button's positions.</span></span>

<dl> <dt>

<span data-ttu-id="59431-105"><span id="PHONEBUTTONSTATE_DOWN"></span><span id="phonebuttonstate_down"></span>**PHONEBUTTONSTATE_DOWN**</span><span class="sxs-lookup"><span data-stu-id="59431-105"><span id="PHONEBUTTONSTATE_DOWN"></span><span id="phonebuttonstate_down"></span>**PHONEBUTTONSTATE_DOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59431-106">Die Schaltfläche befindet sich im Zustand "nach unten" (gedrückt).</span><span class="sxs-lookup"><span data-stu-id="59431-106">The button is in the "down" state (pressed down).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59431-107"><span id="PHONEBUTTONSTATE_UNAVAIL"></span><span id="phonebuttonstate_unavail"></span>**PHONEBUTTONSTATE_UNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="59431-107"><span id="PHONEBUTTONSTATE_UNAVAIL"></span><span id="phonebuttonstate_unavail"></span>**PHONEBUTTONSTATE_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59431-108">Gibt an, dass der Status der Schaltfläche für den Dienstanbieter nicht bekannt ist und zu einem späteren Zeitpunkt nicht bekannt wird.</span><span class="sxs-lookup"><span data-stu-id="59431-108">Indicates that the up or down state of the button is not known to the service provider, and will not become known at a future time.</span></span> <span data-ttu-id="59431-109">(TAPI-Versionen 1,4 und höher)</span><span class="sxs-lookup"><span data-stu-id="59431-109">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59431-110"><span id="PHONEBUTTONSTATE_UNKNOWN"></span><span id="phonebuttonstate_unknown"></span>**PHONEBUTTONSTATE_UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="59431-110"><span id="PHONEBUTTONSTATE_UNKNOWN"></span><span id="phonebuttonstate_unknown"></span>**PHONEBUTTONSTATE_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59431-111">Gibt an, dass der Zustand der Schaltfläche zurzeit nicht bekannt ist, aber zu einem späteren Zeitpunkt bekannt werden kann.</span><span class="sxs-lookup"><span data-stu-id="59431-111">Indicates that the up or down state of the button is not known at this time, but may become known at a future time.</span></span> <span data-ttu-id="59431-112">(TAPI-Versionen 1,4 und höher)</span><span class="sxs-lookup"><span data-stu-id="59431-112">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59431-113"><span id="PHONEBUTTONSTATE_UP"></span><span id="phonebuttonstate_up"></span>**PHONEBUTTONSTATE_UP**</span><span class="sxs-lookup"><span data-stu-id="59431-113"><span id="PHONEBUTTONSTATE_UP"></span><span id="phonebuttonstate_up"></span>**PHONEBUTTONSTATE_UP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="59431-114">Die Schaltfläche befindet sich im Status "up".</span><span class="sxs-lookup"><span data-stu-id="59431-114">The button is in the "up" state.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="59431-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="59431-115">Remarks</span></span>

<span data-ttu-id="59431-116">Keine Erweiterbarkeit.</span><span class="sxs-lookup"><span data-stu-id="59431-116">No extensibility.</span></span> <span data-ttu-id="59431-117">Alle 32 Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="59431-117">All 32 bits are reserved.</span></span>

<span data-ttu-id="59431-118">Aus Gründen der Abwärtskompatibilität liegt es in der Verantwortung des Dienstanbieters, die ausgehandelte API-Version auf dem Telefon zu untersuchen und diese PHONEBUTTONSTATE_ Werte zu verwenden, die von der ausgehandelten Version nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="59431-118">For backward compatibility, it is the responsibility of the service provider to examine the negotiated API version on the phone, and to not use those PHONEBUTTONSTATE_ values that the negotiated version does not support.</span></span>

## <a name="requirements"></a><span data-ttu-id="59431-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="59431-119">Requirements</span></span>



| <span data-ttu-id="59431-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="59431-120">Requirement</span></span> | <span data-ttu-id="59431-121">Wert</span><span class="sxs-lookup"><span data-stu-id="59431-121">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="59431-122">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="59431-122">TAPI version</span></span><br/> | <span data-ttu-id="59431-123">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="59431-123">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="59431-124">Header</span><span class="sxs-lookup"><span data-stu-id="59431-124">Header</span></span><br/>       | <dl> <span data-ttu-id="59431-125"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="59431-125"><dt>Tapi.h</dt></span></span> </dl> |



 

 




