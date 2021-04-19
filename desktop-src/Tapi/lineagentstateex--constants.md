---
description: Die lineagentstateex- \_ Konstanten beschreiben den Status eines Agents für eine Adresse.
ms.assetid: d49025c5-f1db-4b71-a2d5-1cf3df66f3e5
title: LINEAGENTSTATEEX_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 214b816a35e3fdb420a9d95772c466791c6d2f2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352130"
---
# <a name="lineagentstateex_-constants"></a><span data-ttu-id="9dbc5-103">Lineagentstateex- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="9dbc5-103">LINEAGENTSTATEEX\_ Constants</span></span>

<span data-ttu-id="9dbc5-104">Die **lineagentstateex- \_ Konstanten** beschreiben den Status eines Agents für eine Adresse.</span><span class="sxs-lookup"><span data-stu-id="9dbc5-104">The **LINEAGENTSTATEEX\_ constants** describe the state of an agent on an address.</span></span>

<dl> <dt>

<span data-ttu-id="9dbc5-105"><span id="LINEAGENTSTATEEX_BUSYACD"></span><span id="lineagentstateex_busyacd"></span>**lineagentstateex \_ busyacd**</span><span class="sxs-lookup"><span data-stu-id="9dbc5-105"><span id="LINEAGENTSTATEEX_BUSYACD"></span><span id="lineagentstateex_busyacd"></span>**LINEAGENTSTATEEX\_BUSYACD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9dbc5-106">Der Agent ist ausgelastet, um einen von einer ACD-Warteschlange gerouteten Befehl zu verarbeiten</span><span class="sxs-lookup"><span data-stu-id="9dbc5-106">The agent is busy handling a call routed from an ACD queue.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dbc5-107"><span id="LINEAGENTSTATEEX_BUSYINCOMING"></span><span id="lineagentstateex_busyincoming"></span>**lineagentstateex \_ busyincoming**</span><span class="sxs-lookup"><span data-stu-id="9dbc5-107"><span id="LINEAGENTSTATEEX_BUSYINCOMING"></span><span id="lineagentstateex_busyincoming"></span>**LINEAGENTSTATEEX\_BUSYINCOMING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9dbc5-108">Der Agent verarbeitet einen eingehenden-Befehl, der nicht aus einer ACD-Warteschlange, in der der Agent angemeldet ist, an den Agent übertragen wurde.</span><span class="sxs-lookup"><span data-stu-id="9dbc5-108">The agent is busy handling an incoming call that was not transferred to the agent from an ACD queue in which the agent is logged in.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dbc5-109"><span id="LINEAGENTSTATEEX_BUSYOUTGOING"></span><span id="lineagentstateex_busyoutgoing"></span>**lineagentstateex \_ busyoutgoing**</span><span class="sxs-lookup"><span data-stu-id="9dbc5-109"><span id="LINEAGENTSTATEEX_BUSYOUTGOING"></span><span id="lineagentstateex_busyoutgoing"></span>**LINEAGENTSTATEEX\_BUSYOUTGOING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9dbc5-110">Der Agent ist ausgelastet, um einen ausgehenden-Befehl zu verarbeiten</span><span class="sxs-lookup"><span data-stu-id="9dbc5-110">The agent is busy handling an outgoing call, such as one routed from a predictive dialing queue.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dbc5-111"><span id="LINEAGENTSTATEEX_NOTREADY"></span><span id="lineagentstateex_notready"></span>**lineagentstateex \_ notready**</span><span class="sxs-lookup"><span data-stu-id="9dbc5-111"><span id="LINEAGENTSTATEEX_NOTREADY"></span><span id="lineagentstateex_notready"></span>**LINEAGENTSTATEEX\_NOTREADY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9dbc5-112">Der Agent ist angemeldet, aber mit einer anderen Aufgabe als dem Ausführen eines Aufrufens (z. b. bei einer Unterbrechung) beschäftigt.</span><span class="sxs-lookup"><span data-stu-id="9dbc5-112">The agent is logged in, but occupied with a task other than serving a call (such as on a break).</span></span> <span data-ttu-id="9dbc5-113">Es sollten keine weiteren Aufrufe an den Agent weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="9dbc5-113">No additional calls should be routed to the agent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dbc5-114"><span id="LINEAGENTSTATEEX_READY"></span><span id="lineagentstateex_ready"></span>**lineagentstateex ist \_ bereit**</span><span class="sxs-lookup"><span data-stu-id="9dbc5-114"><span id="LINEAGENTSTATEEX_READY"></span><span id="lineagentstateex_ready"></span>**LINEAGENTSTATEEX\_READY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9dbc5-115">Der Agent ist zum Akzeptieren von Aufrufen bereit.</span><span class="sxs-lookup"><span data-stu-id="9dbc5-115">The agent is ready to accept calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dbc5-116"><span id="LINEAGENTSTATEEX_RELEASED"></span><span id="lineagentstateex_released"></span>**lineagentstateex \_ veröffentlicht**</span><span class="sxs-lookup"><span data-stu-id="9dbc5-116"><span id="LINEAGENTSTATEEX_RELEASED"></span><span id="lineagentstateex_released"></span>**LINEAGENTSTATEEX\_RELEASED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9dbc5-117">Der Agent wurde freigegeben, wahrscheinlich weil Sie sich abgemeldet haben.</span><span class="sxs-lookup"><span data-stu-id="9dbc5-117">The agent has been released, probably because they logged off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dbc5-118"><span id="LINEAGENTSTATEEX_UNKNOWN"></span><span id="lineagentstateex_unknown"></span>**lineagentstateex \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="9dbc5-118"><span id="LINEAGENTSTATEEX_UNKNOWN"></span><span id="lineagentstateex_unknown"></span>**LINEAGENTSTATEEX\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9dbc5-119">Der Agent-Status ist zurzeit unbekannt, kann aber später bekannt werden.</span><span class="sxs-lookup"><span data-stu-id="9dbc5-119">The agent state is currently unknown, but may become known later.</span></span> <span data-ttu-id="9dbc5-120">Dies kann ein Übergangszustand sein, wenn eine Zeile oder Adresse zum ersten Mal geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="9dbc5-120">This can be a transitional state when a line or address is first opened.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9dbc5-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9dbc5-121">Requirements</span></span>



| <span data-ttu-id="9dbc5-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9dbc5-122">Requirement</span></span> | <span data-ttu-id="9dbc5-123">Wert</span><span class="sxs-lookup"><span data-stu-id="9dbc5-123">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="9dbc5-124">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="9dbc5-124">TAPI version</span></span><br/> | <span data-ttu-id="9dbc5-125">Erfordert TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="9dbc5-125">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="9dbc5-126">Header</span><span class="sxs-lookup"><span data-stu-id="9dbc5-126">Header</span></span><br/>       | <dl> <span data-ttu-id="9dbc5-127"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="9dbc5-127"><dt>Tapi.h</dt></span></span> </dl> |



 

 




