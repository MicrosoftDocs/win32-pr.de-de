---
description: Die Bit-Flag-Konstanten von linecallcomplmode \_ beschreiben verschiedene Methoden, mit denen ein-Vorgang abgeschlossen werden kann.
ms.assetid: 68f755a1-586b-4c5b-b8e8-c8b40eb71685
title: LINECALLCOMPLMODE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 373a66b6ce13b7bfba00303bea824f542bf0016a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372346"
---
# <a name="linecallcomplmode_-constants"></a><span data-ttu-id="5286e-103">Linecallcomplmode- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="5286e-103">LINECALLCOMPLMODE\_ Constants</span></span>

<span data-ttu-id="5286e-104">Die Bit-Flag-Konstanten von **linecallcomplmode \_** beschreiben verschiedene Methoden, mit denen ein-Vorgang abgeschlossen werden kann.</span><span class="sxs-lookup"><span data-stu-id="5286e-104">The **LINECALLCOMPLMODE\_** bit-flag constants describe different ways in which a call can be completed.</span></span>

<dl> <dt>

<span data-ttu-id="5286e-105"><span id="LINECALLCOMPLMODE_CALLBACK"></span><span id="linecallcomplmode_callback"></span>**linecallcomplmode- \_ Rückruf**</span><span class="sxs-lookup"><span data-stu-id="5286e-105"><span id="LINECALLCOMPLMODE_CALLBACK"></span><span id="linecallcomplmode_callback"></span>**LINECALLCOMPLMODE\_CALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5286e-106">Fordert an, dass die aufgerufene Station den Aufruf zurückgibt, wenn Sie in den Leerlauf kehrt.</span><span class="sxs-lookup"><span data-stu-id="5286e-106">Requests the called station to return the call when it returns to idle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5286e-107"><span id="LINECALLCOMPLMODE_CAMPON"></span><span id="linecallcomplmode_campon"></span>**linecallcomplmode- \_ Campon**</span><span class="sxs-lookup"><span data-stu-id="5286e-107"><span id="LINECALLCOMPLMODE_CAMPON"></span><span id="linecallcomplmode_campon"></span>**LINECALLCOMPLMODE\_CAMPON**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5286e-108">Fügt den-aufruder in die Warteschlange ein, bis der-</span><span class="sxs-lookup"><span data-stu-id="5286e-108">Queues the call until the call can be completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5286e-109"><span id="LINECALLCOMPLMODE_INTRUDE"></span><span id="linecallcomplmode_intrude"></span>**Eingriff in linecallcomplmode \_**</span><span class="sxs-lookup"><span data-stu-id="5286e-109"><span id="LINECALLCOMPLMODE_INTRUDE"></span><span id="linecallcomplmode_intrude"></span>**LINECALLCOMPLMODE\_INTRUDE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5286e-110">Fügt die Anwendung dem vorhandenen Aufruf an der aufgerufenen Station hinzu (Barge in).</span><span class="sxs-lookup"><span data-stu-id="5286e-110">Adds the application to the existing call at the called station (barge in).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5286e-111"><span id="LINECALLCOMPLMODE_MESSAGE"></span><span id="linecallcomplmode_message"></span>**linecallcomplmode- \_ Meldung**</span><span class="sxs-lookup"><span data-stu-id="5286e-111"><span id="LINECALLCOMPLMODE_MESSAGE"></span><span id="linecallcomplmode_message"></span>**LINECALLCOMPLMODE\_MESSAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5286e-112">Hinterlässt eine kurze vordefinierte Meldung für die aufgerufene Station (Wort Aufruf durchlassen).</span><span class="sxs-lookup"><span data-stu-id="5286e-112">Leaves a short predefined message for the called station (Leave Word Calling).</span></span> <span data-ttu-id="5286e-113">Die zu sendende Nachricht wird separat angegeben.</span><span class="sxs-lookup"><span data-stu-id="5286e-113">The message to be sent is specified separately.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5286e-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5286e-114">Remarks</span></span>

<span data-ttu-id="5286e-115">Keine Erweiterbarkeit.</span><span class="sxs-lookup"><span data-stu-id="5286e-115">No extensibility.</span></span> <span data-ttu-id="5286e-116">Alle 32 Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="5286e-116">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="5286e-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5286e-117">Requirements</span></span>



| <span data-ttu-id="5286e-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5286e-118">Requirement</span></span> | <span data-ttu-id="5286e-119">Wert</span><span class="sxs-lookup"><span data-stu-id="5286e-119">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5286e-120">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="5286e-120">TAPI version</span></span><br/> | <span data-ttu-id="5286e-121">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="5286e-121">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="5286e-122">Header</span><span class="sxs-lookup"><span data-stu-id="5286e-122">Header</span></span><br/>       | <dl> <span data-ttu-id="5286e-123"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="5286e-123"><dt>Tapi.h</dt></span></span> </dl> |



 

 




