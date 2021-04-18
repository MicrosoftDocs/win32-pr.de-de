---
description: Die linecallreason \_ -bitflagkonstanten beschreiben den Grund für einen-Befehl.
ms.assetid: 16278146-886f-433a-afe5-64f4894b1428
title: LINECALLREASON_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab6d2411c652c13add1620ca6029cabbf2b878e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358239"
---
# <a name="linecallreason_-constants"></a><span data-ttu-id="fd126-103">Linecallreason- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="fd126-103">LINECALLREASON\_ Constants</span></span>

<span data-ttu-id="fd126-104">Die **linecallreason \_** -bitflagkonstanten beschreiben den Grund für einen-Befehl.</span><span class="sxs-lookup"><span data-stu-id="fd126-104">The **LINECALLREASON\_** bit-flag constants describe the reason for a call.</span></span>

<dl> <dt>

<span data-ttu-id="fd126-105"><span id="LINECALLREASON_CALLCOMPLETION"></span><span id="linecallreason_callcompletion"></span>**linecallreason \_ callcompletion**</span><span class="sxs-lookup"><span data-stu-id="fd126-105"><span id="LINECALLREASON_CALLCOMPLETION"></span><span id="linecallreason_callcompletion"></span>**LINECALLREASON\_CALLCOMPLETION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fd126-106">Der-Befehl war das Ergebnis einer Anforderung zum Abschluss des Aufrufes.</span><span class="sxs-lookup"><span data-stu-id="fd126-106">The call was the result of a call completion request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd126-107"><span id="LINECALLREASON_CAMPEDON"></span><span id="linecallreason_campedon"></span>**linecallreason \_ campep**</span><span class="sxs-lookup"><span data-stu-id="fd126-107"><span id="LINECALLREASON_CAMPEDON"></span><span id="linecallreason_campedon"></span>**LINECALLREASON\_CAMPEDON**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fd126-108">Der-Befehl wurde für die Adresse gecampt.</span><span class="sxs-lookup"><span data-stu-id="fd126-108">The call was camped on the address.</span></span> <span data-ttu-id="fd126-109">Normalerweise wird Sie anfänglich im OnHold-Zustand angezeigt und kann mithilfe von [**lineswaphold**](/windows/desktop/api/Tapi/nf-tapi-lineswaphold)auf gewechselt werden.</span><span class="sxs-lookup"><span data-stu-id="fd126-109">Usually, it appears initially in the onhold state, and can be switched to using [**lineSwapHold**](/windows/desktop/api/Tapi/nf-tapi-lineswaphold).</span></span> <span data-ttu-id="fd126-110">Wenn ein aktiver-Vorgang in den Leerlauf wechselt, kann der gefragte-Befehl in den Angebots Status wechseln, und das Gerät beginnt mit dem Klingeln.</span><span class="sxs-lookup"><span data-stu-id="fd126-110">If an active call becomes idle, the camped-on call may change to the offering state and the device start ringing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd126-111"><span id="LINECALLREASON_DIRECT"></span><span id="linecallreason_direct"></span>**linecallreason \_ Direct**</span><span class="sxs-lookup"><span data-stu-id="fd126-111"><span id="LINECALLREASON_DIRECT"></span><span id="linecallreason_direct"></span>**LINECALLREASON\_DIRECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fd126-112">Dabei handelt es sich um einen direkten oder ausgehenden-Rückruf.</span><span class="sxs-lookup"><span data-stu-id="fd126-112">This is a direct incoming or outgoing call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd126-113"><span id="LINECALLREASON_FWDBUSY"></span><span id="linecallreason_fwdbusy"></span>**linecallreason \_ f wdbusy**</span><span class="sxs-lookup"><span data-stu-id="fd126-113"><span id="LINECALLREASON_FWDBUSY"></span><span id="linecallreason_fwdbusy"></span>**LINECALLREASON\_FWDBUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fd126-114">Dieser Aufruf wurde von einer anderen Erweiterung weitergeleitet, die zum Zeitpunkt des Aufrufes ausgelastet war.</span><span class="sxs-lookup"><span data-stu-id="fd126-114">This call was forwarded from another extension that was busy at the time of the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd126-115"><span id="LINECALLREASON_FWDNOANSWER"></span><span id="linecallreason_fwdnoanswer"></span>**linecallreason \_ f wdnoanswer**</span><span class="sxs-lookup"><span data-stu-id="fd126-115"><span id="LINECALLREASON_FWDNOANSWER"></span><span id="linecallreason_fwdnoanswer"></span>**LINECALLREASON\_FWDNOANSWER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fd126-116">Der Anruf wurde von einer anderen Erweiterung weitergeleitet, die den Anruf nach einigen Ringen nicht beantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="fd126-116">The call was forwarded from another extension that didn't answer the call after some number of rings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd126-117"><span id="LINECALLREASON_FWDUNCOND"></span><span id="linecallreason_fwduncond"></span>**linecallreason \_ f wdund**</span><span class="sxs-lookup"><span data-stu-id="fd126-117"><span id="LINECALLREASON_FWDUNCOND"></span><span id="linecallreason_fwduncond"></span>**LINECALLREASON\_FWDUNCOND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fd126-118">Der-Befehl wurde von einer anderen Zahl uneingeschränkt weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="fd126-118">The call was forwarded unconditionally from another number.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd126-119"><span id="LINECALLREASON_INTRUDE"></span><span id="linecallreason_intrude"></span>**linecallreason \_ Intrude**</span><span class="sxs-lookup"><span data-stu-id="fd126-119"><span id="LINECALLREASON_INTRUDE"></span><span id="linecallreason_intrude"></span>**LINECALLREASON\_INTRUDE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fd126-120">Der Aufruf wurde in die Zeile eingedrungen, entweder durch eine Aktion zum Aufrufen des Vorgangs, die durch eine andere Station oder durch eine Operator Aktion aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="fd126-120">The call intruded onto the line, either by a call completion action invoked by another station or by operator action.</span></span> <span data-ttu-id="fd126-121">Abhängig von der Switch-Implementierung kann der-Befehl entweder im verbundenen Zustand oder mit einem vorhandenen aktiven-Befehl in der Zeile angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="fd126-121">Depending on switch implementation, the call may appear either in the connected state, or conferenced with an existing active call on the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd126-122"><span id="LINECALLREASON_PARKED"></span><span id="linecallreason_parked"></span>**linecallreason ist \_ geparkt.**</span><span class="sxs-lookup"><span data-stu-id="fd126-122"><span id="LINECALLREASON_PARKED"></span><span id="linecallreason_parked"></span>**LINECALLREASON\_PARKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fd126-123">Der-Befehl wurde für die Adresse geparkt.</span><span class="sxs-lookup"><span data-stu-id="fd126-123">The call was parked on the address.</span></span> <span data-ttu-id="fd126-124">Normalerweise wird Sie anfänglich im OnHold-Zustand angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fd126-124">Usually, it appears initially in the onhold state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd126-125"><span id="LINECALLREASON_PICKUP"></span><span id="linecallreason_pickup"></span>**linecallreason \_ Pickup**</span><span class="sxs-lookup"><span data-stu-id="fd126-125"><span id="LINECALLREASON_PICKUP"></span><span id="linecallreason_pickup"></span>**LINECALLREASON\_PICKUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fd126-126">Der-Befehl wurde aus einer anderen Erweiterung abgerufen.</span><span class="sxs-lookup"><span data-stu-id="fd126-126">The call was picked up from another extension.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd126-127"><span id="LINECALLREASON_REDIRECT"></span><span id="linecallreason_redirect"></span>**linecallreason- \_ Umleitung**</span><span class="sxs-lookup"><span data-stu-id="fd126-127"><span id="LINECALLREASON_REDIRECT"></span><span id="linecallreason_redirect"></span>**LINECALLREASON\_REDIRECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fd126-128">Der-Befehl wurde an diese Station umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="fd126-128">The call was redirected to this station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd126-129"><span id="LINECALLREASON_REMINDER"></span><span id="linecallreason_reminder"></span>**linecallreason- \_ Erinnerung**</span><span class="sxs-lookup"><span data-stu-id="fd126-129"><span id="LINECALLREASON_REMINDER"></span><span id="linecallreason_reminder"></span>**LINECALLREASON\_REMINDER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fd126-130">Der Aufruf ist eine Erinnerung (oder "Rückruf"), für die der Benutzer einen Aufruf hat oder für (potenziell) eine lange Zeit hält.</span><span class="sxs-lookup"><span data-stu-id="fd126-130">The call is a reminder (or "recall") that the user has a call parked or on hold for (potentially) a long time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd126-131"><span id="LINECALLREASON_ROUTEREQUEST"></span><span id="linecallreason_routerequest"></span>**linecallreason \_ RouteRequest**</span><span class="sxs-lookup"><span data-stu-id="fd126-131"><span id="LINECALLREASON_ROUTEREQUEST"></span><span id="linecallreason_routerequest"></span>**LINECALLREASON\_ROUTEREQUEST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fd126-132">Der-Befehl wird für die Adresse angezeigt, da der Switch Weiterleitungs Anweisungen aus der Anwendung benötigt.</span><span class="sxs-lookup"><span data-stu-id="fd126-132">The call appears on the address because the switch needs routing instructions from the application.</span></span> <span data-ttu-id="fd126-133">Die Anwendung sollte das **calledid** -Element in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)untersuchen und die [**lineredirect**](/windows/desktop/api/Tapi/nf-tapi-lineredirect) -Funktion verwenden, um eine neue, für den Aufruf angeforderte Adresse anzugeben.</span><span class="sxs-lookup"><span data-stu-id="fd126-133">The application should examine the **CalledID** member in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo), and use the [**lineRedirect**](/windows/desktop/api/Tapi/nf-tapi-lineredirect) function to provide a new dialable address for the call.</span></span> <span data-ttu-id="fd126-134">Wenn der-Befehl stattdessen blockiert werden soll, ruft die Anwendung möglicherweise [**linedrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop)auf.</span><span class="sxs-lookup"><span data-stu-id="fd126-134">If the call is to be blocked instead, the application may call [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop).</span></span> <span data-ttu-id="fd126-135">Wenn die Anwendung innerhalb eines von einem Switch definierten Timeout Zeitraums keine Maßnahmen ergreifen kann, wird eine Standardaktion ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fd126-135">If the application fails to take action within a switch-defined timeout period, a default action will be taken.</span></span> <span data-ttu-id="fd126-136">Ein Dienstanbieter kann diese Konstante nur verwenden, wenn die ausgehandelte Version in der Zeile 2,0 oder höher ist.</span><span class="sxs-lookup"><span data-stu-id="fd126-136">A service provider can use this constant only if the negotiated version on the line is 2.0 or higher.</span></span> <span data-ttu-id="fd126-137">Andernfalls sollte der Dienstanbieter den linecallreason- \_ nicht Gebrauch ersetzen.</span><span class="sxs-lookup"><span data-stu-id="fd126-137">Otherwise the service provider should substitute LINECALLREASON\_UNAVAIL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd126-138"><span id="LINECALLREASON_TRANSFER"></span><span id="linecallreason_transfer"></span>**linecallreason- \_ Übertragung**</span><span class="sxs-lookup"><span data-stu-id="fd126-138"><span id="LINECALLREASON_TRANSFER"></span><span id="linecallreason_transfer"></span>**LINECALLREASON\_TRANSFER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fd126-139">Der-Befehl wurde von einer anderen Zahl übertragen.</span><span class="sxs-lookup"><span data-stu-id="fd126-139">The call has been transferred from another number.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd126-140"><span id="LINECALLREASON_UNAVAIL"></span><span id="linecallreason_unavail"></span>**linecallreason \_ nicht erreichbar**</span><span class="sxs-lookup"><span data-stu-id="fd126-140"><span id="LINECALLREASON_UNAVAIL"></span><span id="linecallreason_unavail"></span>**LINECALLREASON\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fd126-141">Der Grund für den-Aufrufvorgang ist nicht verfügbar und wird später noch nicht bekannt werden.</span><span class="sxs-lookup"><span data-stu-id="fd126-141">The reason for the call is unavailable and will not become known later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd126-142"><span id="LINECALLREASON_UNKNOWN"></span><span id="linecallreason_unknown"></span>**linecallreason \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="fd126-142"><span id="LINECALLREASON_UNKNOWN"></span><span id="linecallreason_unknown"></span>**LINECALLREASON\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fd126-143">Der Grund für den-aufrufsvorgang ist derzeit unbekannt, kann aber später bekannt werden.</span><span class="sxs-lookup"><span data-stu-id="fd126-143">The reason for the call is currently unknown but may become known later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd126-144"><span id="LINECALLREASON_UNPARK"></span><span id="linecallreason_unpark"></span>**linecallreason \_ unpark**</span><span class="sxs-lookup"><span data-stu-id="fd126-144"><span id="LINECALLREASON_UNPARK"></span><span id="linecallreason_unpark"></span>**LINECALLREASON\_UNPARK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fd126-145">Der-Rückruf wurde als geparkter-Befehl abgerufen.</span><span class="sxs-lookup"><span data-stu-id="fd126-145">The call was retrieved as a parked call.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fd126-146">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd126-146">Remarks</span></span>

<span data-ttu-id="fd126-147">Keine Erweiterbarkeit.</span><span class="sxs-lookup"><span data-stu-id="fd126-147">No extensibility.</span></span> <span data-ttu-id="fd126-148">Alle 32 Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="fd126-148">All 32 bits are reserved.</span></span>

<span data-ttu-id="fd126-149">Die linecallreason- \_ Konstanten werden im **dwReason** -Member der [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) -Datenstruktur verwendet.</span><span class="sxs-lookup"><span data-stu-id="fd126-149">The LINECALLREASON\_ constants are used in the **dwReason** member of the [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) data structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd126-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fd126-150">Requirements</span></span>



| <span data-ttu-id="fd126-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fd126-151">Requirement</span></span> | <span data-ttu-id="fd126-152">Wert</span><span class="sxs-lookup"><span data-stu-id="fd126-152">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="fd126-153">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="fd126-153">TAPI version</span></span><br/> | <span data-ttu-id="fd126-154">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="fd126-154">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="fd126-155">Header</span><span class="sxs-lookup"><span data-stu-id="fd126-155">Header</span></span><br/>       | <dl> <span data-ttu-id="fd126-156"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd126-156"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd126-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd126-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd126-158">**LINECALLINFO**</span><span class="sxs-lookup"><span data-stu-id="fd126-158">**LINECALLINFO**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)
</dt> <dt>

[<span data-ttu-id="fd126-159">**linedrop**</span><span class="sxs-lookup"><span data-stu-id="fd126-159">**lineDrop**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedrop)
</dt> <dt>

[<span data-ttu-id="fd126-160">**lineredirect**</span><span class="sxs-lookup"><span data-stu-id="fd126-160">**lineRedirect**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineredirect)
</dt> <dt>

[<span data-ttu-id="fd126-161">**lineswaphold**</span><span class="sxs-lookup"><span data-stu-id="fd126-161">**lineSwapHold**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineswaphold)
</dt> </dl>

 

 




