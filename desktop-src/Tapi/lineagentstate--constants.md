---
description: Die lineagentstate- \_ Konstanten beschreiben den Status eines Agents für eine Adresse.
ms.assetid: 1dbc33e7-05cc-4cb9-8904-f495b884b8db
title: LINEAGENTSTATE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90b5afa8f93cfde5529f8f57fd8e48d37ecd415b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362132"
---
# <a name="lineagentstate_-constants"></a><span data-ttu-id="0ac70-103">Lineagentstate- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="0ac70-103">LINEAGENTSTATE\_ Constants</span></span>

<span data-ttu-id="0ac70-104">Die **lineagentstate- \_ Konstanten** beschreiben den Status eines Agents für eine Adresse.</span><span class="sxs-lookup"><span data-stu-id="0ac70-104">The **LINEAGENTSTATE\_ constants** describe the state of an agent on an address.</span></span>

<dl> <dt>

<span data-ttu-id="0ac70-105"><span id="LINEAGENTSTATE_BUSYACD"></span><span id="lineagentstate_busyacd"></span>**lineagentstate \_ busyacd**</span><span class="sxs-lookup"><span data-stu-id="0ac70-105"><span id="LINEAGENTSTATE_BUSYACD"></span><span id="lineagentstate_busyacd"></span>**LINEAGENTSTATE\_BUSYACD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0ac70-106">Der Agent ist ausgelastet, um einen von einer ACD-Warteschlange gerouteten Befehl zu verarbeiten</span><span class="sxs-lookup"><span data-stu-id="0ac70-106">The agent is busy handling a call routed from an ACD queue.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0ac70-107"><span id="LINEAGENTSTATE_BUSYINCOMING"></span><span id="lineagentstate_busyincoming"></span>**lineagentstate \_ busyincoming**</span><span class="sxs-lookup"><span data-stu-id="0ac70-107"><span id="LINEAGENTSTATE_BUSYINCOMING"></span><span id="lineagentstate_busyincoming"></span>**LINEAGENTSTATE\_BUSYINCOMING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0ac70-108">Der Agent verarbeitet einen eingehenden-Befehl, der nicht aus einer ACD-Warteschlange, in der der Agent angemeldet ist, an den Agent übertragen wurde.</span><span class="sxs-lookup"><span data-stu-id="0ac70-108">The agent is busy handling an incoming call that was not transferred to the agent from an ACD queue in which the agent is logged in.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0ac70-109"><span id="LINEAGENTSTATE_BUSYOTHER"></span><span id="lineagentstate_busyother"></span>**lineagentstate- \_ busyother**</span><span class="sxs-lookup"><span data-stu-id="0ac70-109"><span id="LINEAGENTSTATE_BUSYOTHER"></span><span id="lineagentstate_busyother"></span>**LINEAGENTSTATE\_BUSYOTHER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0ac70-110">Der Agent beschäftigt sich mit der Verarbeitung eines anderen Typs, z. b. eines ausgehenden persönlichen Aufrufes, der nicht von einer Vorhersage Dialer an den Agent übertragen</span><span class="sxs-lookup"><span data-stu-id="0ac70-110">The agent is busy handling another type of call, such as an outgoing personal call not transferred to the agent by a predictive dialer.</span></span> <span data-ttu-id="0ac70-111">Dieser Wert kann auch verwendet werden, wenn bekannt ist, dass der Agent bei einem-Befehl ausgelastet ist, aber der Typ des Aufrufes unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="0ac70-111">This value can also be used when the agent is known to be busy on a call but the type of call is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0ac70-112"><span id="LINEAGENTSTATE_BUSYOUTBOUND"></span><span id="lineagentstate_busyoutbound"></span>**lineagentstate \_ busyoutbound**</span><span class="sxs-lookup"><span data-stu-id="0ac70-112"><span id="LINEAGENTSTATE_BUSYOUTBOUND"></span><span id="lineagentstate_busyoutbound"></span>**LINEAGENTSTATE\_BUSYOUTBOUND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0ac70-113">Der Agent ist ausgelastet, um einen ausgehenden-Befehl zu verarbeiten</span><span class="sxs-lookup"><span data-stu-id="0ac70-113">The agent is busy handling an outgoing call, such as one routed from a predictive dialing queue.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0ac70-114"><span id="LINEAGENTSTATE_LOGGEDOFF"></span><span id="lineagentstate_loggedoff"></span>**lineagentstate \_ loggedoff**</span><span class="sxs-lookup"><span data-stu-id="0ac70-114"><span id="LINEAGENTSTATE_LOGGEDOFF"></span><span id="lineagentstate_loggedoff"></span>**LINEAGENTSTATE\_LOGGEDOFF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0ac70-115">Es ist kein Agent für die Adresse angemeldet.</span><span class="sxs-lookup"><span data-stu-id="0ac70-115">No agent is logged in on the address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0ac70-116"><span id="LINEAGENTSTATE_NOTREADY"></span><span id="lineagentstate_notready"></span>**lineagentstate \_ notready**</span><span class="sxs-lookup"><span data-stu-id="0ac70-116"><span id="LINEAGENTSTATE_NOTREADY"></span><span id="lineagentstate_notready"></span>**LINEAGENTSTATE\_NOTREADY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0ac70-117">Der Agent ist angemeldet, aber mit einer anderen Aufgabe als dem Ausführen eines Aufrufens (z. b. bei einer Unterbrechung) beschäftigt.</span><span class="sxs-lookup"><span data-stu-id="0ac70-117">The agent is logged in, but occupied with a task other than serving a call (such as on a break).</span></span> <span data-ttu-id="0ac70-118">Es sollten keine weiteren Aufrufe an den Agent weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="0ac70-118">No additional calls should be routed to the agent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0ac70-119"><span id="LINEAGENTSTATE_READY"></span><span id="lineagentstate_ready"></span>**lineagentstate ist \_ bereit**</span><span class="sxs-lookup"><span data-stu-id="0ac70-119"><span id="LINEAGENTSTATE_READY"></span><span id="lineagentstate_ready"></span>**LINEAGENTSTATE\_READY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0ac70-120">Der Agent ist zum Akzeptieren von Aufrufen bereit.</span><span class="sxs-lookup"><span data-stu-id="0ac70-120">The agent is ready to accept calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0ac70-121"><span id="LINEAGENTSTATE_UNAVAIL"></span><span id="lineagentstate_unavail"></span>**"lineagentstate" \_ nicht erreichbar**</span><span class="sxs-lookup"><span data-stu-id="0ac70-121"><span id="LINEAGENTSTATE_UNAVAIL"></span><span id="lineagentstate_unavail"></span>**LINEAGENTSTATE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0ac70-122">Der Agent-Status ist unbekannt und wird nie bekannt werden.</span><span class="sxs-lookup"><span data-stu-id="0ac70-122">The agent state is unknown and will never become known.</span></span> <span data-ttu-id="0ac70-123">In [**lineaddressstatus**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)kann diese Bedingung auch durch das Mitglied " **dwagentstate** " dargestellt werden, das auf "0" festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="0ac70-123">In [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus), this condition can also be represented by the **dwAgentState** member being set to 0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0ac70-124"><span id="LINEAGENTSTATE_UNKNOWN"></span><span id="lineagentstate_unknown"></span>**lineagentstate \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="0ac70-124"><span id="LINEAGENTSTATE_UNKNOWN"></span><span id="lineagentstate_unknown"></span>**LINEAGENTSTATE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0ac70-125">Der Agent-Status ist zurzeit unbekannt, kann aber später bekannt werden.</span><span class="sxs-lookup"><span data-stu-id="0ac70-125">The agent state is currently unknown, but may become known later.</span></span> <span data-ttu-id="0ac70-126">Dies kann ein Übergangszustand sein, wenn eine Zeile oder Adresse zum ersten Mal geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="0ac70-126">This can be a transitional state when a line or address is first opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0ac70-127"><span id="LINEAGENTSTATE_WORKINGAFTERCALL"></span><span id="lineagentstate_workingaftercall"></span>**lineagentstate \_ workingaftercall**</span><span class="sxs-lookup"><span data-stu-id="0ac70-127"><span id="LINEAGENTSTATE_WORKINGAFTERCALL"></span><span id="lineagentstate_workingaftercall"></span>**LINEAGENTSTATE\_WORKINGAFTERCALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0ac70-128">Der Agent hat den vorangehenden-Befehl abgeschlossen, ist aber noch mit der Arbeit im Zusammenhang mit diesem-Befehl beschäftigt.</span><span class="sxs-lookup"><span data-stu-id="0ac70-128">The agent has completed the preceding call, but is still occupied with work related to that call.</span></span> <span data-ttu-id="0ac70-129">Der Agent sollte keine weiteren Aufrufe empfangen.</span><span class="sxs-lookup"><span data-stu-id="0ac70-129">The agent should not receive additional calls.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0ac70-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0ac70-130">Remarks</span></span>

<span data-ttu-id="0ac70-131">Die oberen 16 Bits dieses Satzes von Konstanten sind für gerätespezifische Erweiterungen reserviert.</span><span class="sxs-lookup"><span data-stu-id="0ac70-131">The upper 16 bits of this set of constants are reserved for device-specific extensions.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ac70-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ac70-132">Requirements</span></span>



| <span data-ttu-id="0ac70-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0ac70-133">Requirement</span></span> | <span data-ttu-id="0ac70-134">Wert</span><span class="sxs-lookup"><span data-stu-id="0ac70-134">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="0ac70-135">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="0ac70-135">TAPI version</span></span><br/> | <span data-ttu-id="0ac70-136">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="0ac70-136">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="0ac70-137">Header</span><span class="sxs-lookup"><span data-stu-id="0ac70-137">Header</span></span><br/>       | <dl> <span data-ttu-id="0ac70-138"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ac70-138"><dt>Tapi.h</dt></span></span> </dl> |



 

 




