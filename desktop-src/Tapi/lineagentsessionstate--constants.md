---
description: Die lineagentsessionstate- \_ Konstanten beschreiben verschiedene agentsitzungszustände.
ms.assetid: 8a0d06bb-51ba-4eaf-8719-120aed817f63
title: LINEAGENTSESSIONSTATE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdfd1be8cf846d0e23828f0a3540960a86a83ef1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364948"
---
# <a name="lineagentsessionstate_-constants"></a><span data-ttu-id="eb4de-103">Lineagentsessionstate- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="eb4de-103">LINEAGENTSESSIONSTATE\_ Constants</span></span>

<span data-ttu-id="eb4de-104">Die **lineagentsessionstate- \_ Konstanten** beschreiben verschiedene agentsitzungszustände.</span><span class="sxs-lookup"><span data-stu-id="eb4de-104">The **LINEAGENTSESSIONSTATE\_ constants** describe various agent session states.</span></span>

<dl> <dt>

<span data-ttu-id="eb4de-105"><span id="LINEAGENTSESSIONSTATE_BUSYONCALL"></span><span id="lineagentsessionstate_busyoncall"></span>**lineagentsessionstate \_ busyoncallcenter**</span><span class="sxs-lookup"><span data-stu-id="eb4de-105"><span id="LINEAGENTSESSIONSTATE_BUSYONCALL"></span><span id="lineagentsessionstate_busyoncall"></span>**LINEAGENTSESSIONSTATE\_BUSYONCALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="eb4de-106">Der Agent ist mit der Verarbeitung eines Aufrufes ausgelastet.</span><span class="sxs-lookup"><span data-stu-id="eb4de-106">The agent is busy handling a call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb4de-107"><span id="LINEAGENTSESSIONSTATE_BUSYWRAPUP"></span><span id="lineagentsessionstate_busywrapup"></span>**lineagentsessionstate \_ busywrapup**</span><span class="sxs-lookup"><span data-stu-id="eb4de-107"><span id="LINEAGENTSESSIONSTATE_BUSYWRAPUP"></span><span id="lineagentsessionstate_busywrapup"></span>**LINEAGENTSESSIONSTATE\_BUSYWRAPUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="eb4de-108">Der Agent ist ausgelastet, um die Zusammenfassung des Aufrufes aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="eb4de-108">The agent is busy handling the wrap-up of the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb4de-109"><span id="LINEAGENTSESSIONSTATE_ENDED"></span><span id="lineagentsessionstate_ended"></span>**lineagentsessionstate wurde \_ beendet.**</span><span class="sxs-lookup"><span data-stu-id="eb4de-109"><span id="LINEAGENTSESSIONSTATE_ENDED"></span><span id="lineagentsessionstate_ended"></span>**LINEAGENTSESSIONSTATE\_ENDED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="eb4de-110">Die Agentsitzung wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="eb4de-110">The agent session has ended.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb4de-111"><span id="LINEAGENTSESSIONSTATE_NOTREADY"></span><span id="lineagentsessionstate_notready"></span>**lineagentsessionstate \_ notready**</span><span class="sxs-lookup"><span data-stu-id="eb4de-111"><span id="LINEAGENTSESSIONSTATE_NOTREADY"></span><span id="lineagentsessionstate_notready"></span>**LINEAGENTSESSIONSTATE\_NOTREADY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="eb4de-112">Der Agent ist angemeldet, aber mit einer anderen Aufgabe als dem Ausführen eines Aufrufens (z. b. bei einer Unterbrechung) beschäftigt.</span><span class="sxs-lookup"><span data-stu-id="eb4de-112">The agent is logged in, but occupied with a task other than serving a call (such as on a break).</span></span> <span data-ttu-id="eb4de-113">Es sollten keine weiteren Aufrufe an den Agent weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="eb4de-113">No additional calls should be routed to the agent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb4de-114"><span id="LINEAGENTSESSIONSTATE_READY"></span><span id="lineagentsessionstate_ready"></span>**lineagentsessionstate ist \_ bereit**</span><span class="sxs-lookup"><span data-stu-id="eb4de-114"><span id="LINEAGENTSESSIONSTATE_READY"></span><span id="lineagentsessionstate_ready"></span>**LINEAGENTSESSIONSTATE\_READY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="eb4de-115">Der Agent ist zum Akzeptieren von Aufrufen bereit.</span><span class="sxs-lookup"><span data-stu-id="eb4de-115">The agent is ready to accept calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb4de-116"><span id="LINEAGENTSESSIONSTATE_RELEASED"></span><span id="lineagentsessionstate_released"></span>**lineagentsessionstate \_ veröffentlicht**</span><span class="sxs-lookup"><span data-stu-id="eb4de-116"><span id="LINEAGENTSESSIONSTATE_RELEASED"></span><span id="lineagentsessionstate_released"></span>**LINEAGENTSESSIONSTATE\_RELEASED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="eb4de-117">Die Agentsitzung wurde freigegeben.</span><span class="sxs-lookup"><span data-stu-id="eb4de-117">The agent session has been released.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eb4de-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eb4de-118">Requirements</span></span>



| <span data-ttu-id="eb4de-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eb4de-119">Requirement</span></span> | <span data-ttu-id="eb4de-120">Wert</span><span class="sxs-lookup"><span data-stu-id="eb4de-120">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="eb4de-121">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="eb4de-121">TAPI version</span></span><br/> | <span data-ttu-id="eb4de-122">Erfordert TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="eb4de-122">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="eb4de-123">Header</span><span class="sxs-lookup"><span data-stu-id="eb4de-123">Header</span></span><br/>       | <dl> <span data-ttu-id="eb4de-124"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb4de-124"><dt>Tapi.h</dt></span></span> </dl> |



 

 




