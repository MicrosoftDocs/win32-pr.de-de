---
description: Die TAPI-zeilige \_ CallState-Nachricht wird gesendet, wenn sich der Status des angegebenen Aufrufes geändert hat.
ms.assetid: 7b24e3c3-bc69-488b-a698-cf17875bc3c5
title: LINE_CALLSTATE Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4159037c448307c99e759d8741ed19a14ab2562f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358066"
---
# <a name="line_callstate-message"></a><span data-ttu-id="2380e-103">Zeilen \_ Aufruf Zustands Meldung</span><span class="sxs-lookup"><span data-stu-id="2380e-103">LINE\_CALLSTATE message</span></span>

<span data-ttu-id="2380e-104">Die TAPI- **zeilige \_ CallState** -Nachricht wird gesendet, wenn sich der Status des angegebenen Aufrufes geändert hat.</span><span class="sxs-lookup"><span data-stu-id="2380e-104">The TAPI **LINE\_CALLSTATE** message is sent when the status of the specified call has changed.</span></span> <span data-ttu-id="2380e-105">In der Regel werden während der Lebensdauer eines Aufrufes einige dieser Nachrichten empfangen.</span><span class="sxs-lookup"><span data-stu-id="2380e-105">Typically, several such messages are received during the lifetime of a call.</span></span> <span data-ttu-id="2380e-106">Anwendungen werden über neue eingehende Anrufe mit dieser Nachricht benachrichtigt. der neue-Befehl befindet sich im *Angebots* Zustand.</span><span class="sxs-lookup"><span data-stu-id="2380e-106">Applications are notified of new incoming calls with this message; the new call is in the *offering* state.</span></span> <span data-ttu-id="2380e-107">Die Anwendung kann [**linegetcallstatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus) verwenden, um ausführlichere Informationen zum aktuellen Status des Aufrufes abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2380e-107">The application can use [**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus) to retrieve more detailed information about the current status of the call.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="2380e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2380e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2380e-109">*hdevice*</span><span class="sxs-lookup"><span data-stu-id="2380e-109">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="2380e-110">Ein Handle für den-Befehl.</span><span class="sxs-lookup"><span data-stu-id="2380e-110">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="2380e-111">*dwcallbackinstance*</span><span class="sxs-lookup"><span data-stu-id="2380e-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="2380e-112">Die beim Öffnen der Zeile des Aufrufs angegebene Rückruf Instanz.</span><span class="sxs-lookup"><span data-stu-id="2380e-112">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="2380e-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="2380e-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="2380e-114">Der neue Status des Aufrufes.</span><span class="sxs-lookup"><span data-stu-id="2380e-114">The new call state.</span></span> <span data-ttu-id="2380e-115">Dieser Parameter darf nur eine der folgenden [**linecallstate- \_ Konstanten**](linecallstate--constants.md)sein.</span><span class="sxs-lookup"><span data-stu-id="2380e-115">This parameter must be one and only one of the following [**LINECALLSTATE\_ constants**](linecallstate--constants.md).</span></span>



| <span data-ttu-id="2380e-116">dwParam1</span><span class="sxs-lookup"><span data-stu-id="2380e-116">dwParam1</span></span>                                                                                                                                                                                             | <span data-ttu-id="2380e-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="2380e-117">Meaning</span></span>                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LINECALLSTATE_BUSY"></span><span id="linecallstate_busy"></span><dl> <span data-ttu-id="2380e-118"><dt>**linecallstate \_ ausgelastet**</dt></span><span class="sxs-lookup"><span data-stu-id="2380e-118"><dt>**LINECALLSTATE\_BUSY**</dt></span></span> </dl>                         | <span data-ttu-id="2380e-119">*dwParam2* enthält Details zum ausgelasteten Modus.</span><span class="sxs-lookup"><span data-stu-id="2380e-119">*dwParam2* contains details about the busy mode.</span></span> <span data-ttu-id="2380e-120">Dieser Parameter verwendet eine der [**linebusymode- \_ Konstanten**](linebusymode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="2380e-120">This parameter uses one of the [**LINEBUSYMODE\_ constants**](linebusymode--constants.md).</span></span><br/>                          |
| <span id="LINECALLSTATE_CONNECTED"></span><span id="linecallstate_connected"></span><dl> <span data-ttu-id="2380e-121"><dt>**linecallstate \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="2380e-121"><dt>**LINECALLSTATE\_CONNECTED**</dt></span></span> </dl>          | <span data-ttu-id="2380e-122">*dwParam2* enthält Details zum verbundenen Modus.</span><span class="sxs-lookup"><span data-stu-id="2380e-122">*dwParam2* contains details about the connected mode.</span></span> <span data-ttu-id="2380e-123">Dieser Parameter verwendet eine der [**lineconnectedmode- \_ Konstanten**](lineconnectedmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="2380e-123">This parameter uses one of the [**LINECONNECTEDMODE\_ constants**](lineconnectedmode--constants.md).</span></span><br/>           |
| <span id="LINECALLSTATE_DIALTONE"></span><span id="linecallstate_dialtone"></span><dl> <span data-ttu-id="2380e-124"><dt>**linecallstate \_ Dialtone**</dt></span><span class="sxs-lookup"><span data-stu-id="2380e-124"><dt>**LINECALLSTATE\_DIALTONE**</dt></span></span> </dl>             | <span data-ttu-id="2380e-125">*dwParam2* enthält Details zum wählermodusmodus.</span><span class="sxs-lookup"><span data-stu-id="2380e-125">*dwParam2* contains details about the dial tone mode.</span></span> <span data-ttu-id="2380e-126">Dieser Parameter verwendet eine der [**linedialtonemode- \_ Konstanten**](linedialtonemode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="2380e-126">This parameter uses one of the [**LINEDIALTONEMODE\_ constants**](linedialtonemode--constants.md).</span></span><br/>             |
| <span id="LINECALLSTATE_OFFERING"></span><span id="linecallstate_offering"></span><dl> <span data-ttu-id="2380e-127"><dt>**linecallstate- \_ Angebot**</dt></span><span class="sxs-lookup"><span data-stu-id="2380e-127"><dt>**LINECALLSTATE\_OFFERING**</dt></span></span> </dl>             | <span data-ttu-id="2380e-128">*dwParam2* enthält Details zum verbundenen Modus.</span><span class="sxs-lookup"><span data-stu-id="2380e-128">*dwParam2* contains details about the connected mode.</span></span> <span data-ttu-id="2380e-129">Dieser Parameter verwendet eine der [**lineofferingmode- \_ Konstanten**](lineofferingmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="2380e-129">This parameter uses one of the [**LINEOFFERINGMODE\_ constants**](lineofferingmode--constants.md).</span></span><br/>             |
| <span id="LINECALLSTATE_SPECIALINFO"></span><span id="linecallstate_specialinfo"></span><dl> <span data-ttu-id="2380e-130"><dt>**linecallstate \_ specialinfo**</dt></span><span class="sxs-lookup"><span data-stu-id="2380e-130"><dt>**LINECALLSTATE\_SPECIALINFO**</dt></span></span> </dl>    | <span data-ttu-id="2380e-131">*dwParam2* enthält die Details zum speziellen Informationsmodus.</span><span class="sxs-lookup"><span data-stu-id="2380e-131">*dwParam2* contains the details about the special information mode.</span></span> <span data-ttu-id="2380e-132">Dieser Parameter verwendet eine der [**linespecialinfo- \_ Konstanten**](linespecialinfo--constants.md).</span><span class="sxs-lookup"><span data-stu-id="2380e-132">This parameter uses one of the [**LINESPECIALINFO\_ constants**](linespecialinfo--constants.md).</span></span><br/> |
| <span id="LINECALLSTATE_DISCONNECTED"></span><span id="linecallstate_disconnected"></span><dl> <span data-ttu-id="2380e-133"><dt>**linecallstate \_ getrennt**</dt></span><span class="sxs-lookup"><span data-stu-id="2380e-133"><dt>**LINECALLSTATE\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="2380e-134">*dwParam2* enthält Details zum Disconnect-Modus.</span><span class="sxs-lookup"><span data-stu-id="2380e-134">*dwParam2* contains details about the disconnect mode.</span></span> <span data-ttu-id="2380e-135">Dieser Parameter verwendet eine der [**linedisconnectmode- \_ Konstanten**](linedisconnectmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="2380e-135">This parameter uses one of the [**LINEDISCONNECTMODE\_ constants**](linedisconnectmode--constants.md).</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="2380e-136">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="2380e-136">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="2380e-137">Aufrufzustands abhängige Informationen.</span><span class="sxs-lookup"><span data-stu-id="2380e-137">Call-state-dependent information.</span></span> <span data-ttu-id="2380e-138">Siehe *dwParam1*.</span><span class="sxs-lookup"><span data-stu-id="2380e-138">See *dwParam1*.</span></span>

> [!Note]  
> <span data-ttu-id="2380e-139">In Fällen, in denen eine *verzögerte* Antwort angemessen ist, verwenden Sie den linedisconnectmode- \_ tempfailure.</span><span class="sxs-lookup"><span data-stu-id="2380e-139">In circumstances where a *delayed* response is appropriate, use LINEDISCONNECTMODE\_TEMPFAILURE.</span></span> <span data-ttu-id="2380e-140">Wenn eine *Blockierungs* Antwort angemessen ist, verwenden Sie "linedisconnect \_ blockiert".</span><span class="sxs-lookup"><span data-stu-id="2380e-140">Where a *blocklisted* response is appropriate, use LINEDISCONNECT\_BLOCKED.</span></span> <span data-ttu-id="2380e-141">Weitere Informationen finden Sie unter [**linedisconnectmode- \_ Konstanten**](linedisconnectmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="2380e-141">For further information, see [**LINEDISCONNECTMODE\_ Constants**](linedisconnectmode--constants.md).</span></span>

 

<span data-ttu-id="2380e-142">Wenn *dwParam1* auf linecallstate zuweist \_ , enthält *dwParam2* den *hconfcallparameter* des übergeordneten Aufrufens der Konferenz, von der der Betreff- *hcallmember* ist.</span><span class="sxs-lookup"><span data-stu-id="2380e-142">If *dwParam1* is LINECALLSTATE\_CONFERENCED, *dwParam2* contains the *hConfCall* parameter of the parent call of the conference of which the subject *hCall* is a member.</span></span> <span data-ttu-id="2380e-143">Wenn der in *dwParam2* angegebene-Befehl nicht zuvor von der Anwendung als übergeordnete Konferenz aufgerufen wurde (*hconfcallcenter*), muss die Anwendung dies als Ergebnis dieser Nachricht ausführen.</span><span class="sxs-lookup"><span data-stu-id="2380e-143">If the call specified in *dwParam2* was not previously considered by the application to be a parent conference call (*hConfCall*, the application must do so as a result of this message.</span></span> <span data-ttu-id="2380e-144">Wenn die Anwendung kein Handle für den übergeordneten Aufruf der Konferenz hat (weil Sie zuvor [**linedezugecall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) für dieses Handle aufgerufen hat), wird *dwParam2* auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2380e-144">If the application does not have a handle to the parent call of the conference (because it has previously called [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) on that handle) *dwParam2* is set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2380e-145">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="2380e-145">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="2380e-146">Wenn der Wert NULL ist, gibt dieser Parameter an, dass die Berechtigung der Anwendung für den-Befehl nicht geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="2380e-146">If zero, this parameter indicates that there has been no change in the application's privilege for the call.</span></span>

<span data-ttu-id="2380e-147">Wenn ungleich 0 (null) angegeben ist, wird die Berechtigung der Anwendung für den-Befehl angegeben.</span><span class="sxs-lookup"><span data-stu-id="2380e-147">If nonzero, it specifies the application's privilege for the call.</span></span> <span data-ttu-id="2380e-148">Dies tritt in den folgenden Situationen auf: (1), wenn der Anwendung das erste Mal ein Handle für diesen Aufruf zugewiesen wird. (2), wenn die Anwendung das Ziel einer callhandoff ist (selbst wenn die Anwendung bereits Besitzer des Aufrufes ist).</span><span class="sxs-lookup"><span data-stu-id="2380e-148">This occurs in the following situations: (1) The first time that the application is given a handle to this call; (2) When the application is the target of a call handoff (even if the application already was an owner of the call).</span></span> <span data-ttu-id="2380e-149">Dieser Parameter verwendet eine der folgenden [**linecallprivilege- \_ Konstanten**](linecallprivilege--constants.md).</span><span class="sxs-lookup"><span data-stu-id="2380e-149">This parameter uses one of the following [**LINECALLPRIVILEGE\_ constants**](linecallprivilege--constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2380e-150">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2380e-150">Return value</span></span>

<span data-ttu-id="2380e-151">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="2380e-151">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2380e-152">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2380e-152">Remarks</span></span>

<span data-ttu-id="2380e-153">Diese Meldung wird an jede Anwendung gesendet, die über ein Handle für den-Befehl verfügt.</span><span class="sxs-lookup"><span data-stu-id="2380e-153">This message is sent to any application that has a handle for the call.</span></span> <span data-ttu-id="2380e-154">In der **Zeile \_ CallState** werden auch Anwendungen benachrichtigt, die Aufrufe in einer Zeile über das vorhanden sein und den Status der ausgehenden Aufrufe, die von anderen Anwendungen oder manuell durch den Benutzer (z. b. auf einem angeschlossenen Telefongerät), überwachen.</span><span class="sxs-lookup"><span data-stu-id="2380e-154">The **LINE\_CALLSTATE** message also notifies applications that monitor calls on a line about the existence and state of outbound calls established by other applications or manually by the user (for example, on an attached phone device).</span></span> <span data-ttu-id="2380e-155">Der Aufruf Zustand solcher Aufrufe gibt den tatsächlichen Status des Aufrufs an, der nicht *angeboten* wird.</span><span class="sxs-lookup"><span data-stu-id="2380e-155">The call state of such calls reflects the actual state of the call, which is not *offering*.</span></span> <span data-ttu-id="2380e-156">Durch die Untersuchung des aufrufzustands kann die Anwendung bestimmen, ob der-Rückruf ein eingehender-Befehl ist, der beantwortet werden muss.</span><span class="sxs-lookup"><span data-stu-id="2380e-156">By examining the call state, the application can determine whether the call is an inbound call that needs to be answered or not.</span></span>

<span data-ttu-id="2380e-157">Eine **Zeilen Aufruf \_ Zustands** Meldung mit einem unbekannten Aufruf Zustand kann als Ergebnis eines erfolgreichen [**linemakecall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), [**lineforward**](/windows/desktop/api/Tapi/nf-tapi-lineforward), [**lineunpark**](/windows/desktop/api/Tapi/nf-tapi-lineunpark), [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer), [**linepickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup), [**linesetupconference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)oder [**lineprepareadddeconference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference) , das von einer anderen Anwendung angefordert wurde, an eine Überwachungsanwendung gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="2380e-157">A **LINE\_CALLSTATE** message with an unknown call state can be sent to a monitoring application as the result of a successful [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward), [**lineUnpark**](/windows/desktop/api/Tapi/nf-tapi-lineunpark), [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer), [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup), [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference), or [**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference) that has been requested by another application.</span></span> <span data-ttu-id="2380e-158">Gleichzeitig, dass die anfordernde Anwendung für den angeforderten Vorgang eine [**Zeilen \_ Antwort**](line-reply.md) (Erfolg) sendet, wird allen Überwachungsanwendungen in der Zeile die **Zeile \_ CallState** (unknown) zugestellt.</span><span class="sxs-lookup"><span data-stu-id="2380e-158">At the same time that the requesting application is sent a [**LINE\_REPLY**](line-reply.md) (success) for the requested operation, any monitoring applications on the line are sent the **LINE\_CALLSTATE** (unknown) message.</span></span> <span data-ttu-id="2380e-159">Eine **line \_ CallState** -Meldung, die angibt, dass der "Real"-Aufruf Zustand des neu generierten Aufrufes gesendet wird (mithilfe der vom Dienstanbieter bereitgestellten Informationen), kurz danach an die Anforderungs-und Überwachungsanwendungen.</span><span class="sxs-lookup"><span data-stu-id="2380e-159">A **LINE\_CALLSTATE** message indicating the "real" call state of the newly generated call is sent (using information provided by the service provider) to the requesting and monitoring applications shortly thereafter.</span></span>

<span data-ttu-id="2380e-160">Eine Nachricht vom Typ " **\_ CallState** " (unbekannt) wird nur dann an Überwachungsanwendungen gesendet, wenn " [**linecompletetransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) " bewirkt, dass Aufrufe in eine drei-Wege-Konferenz aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="2380e-160">A **LINE\_CALLSTATE** (unknown) message is sent to monitoring applications only if [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) causes calls to be resolved into a three-way conference.</span></span>

<span data-ttu-id="2380e-161">Aus Gründen der Abwärtskompatibilität erwarten ältere Anwendungen keinen bestimmten Wert in *dwParam2* einer mit linecallstate zugewandten \_ Nachricht.</span><span class="sxs-lookup"><span data-stu-id="2380e-161">For backward compatibility, older applications are not expecting any particular value in *dwParam2* of a LINECALLSTATE\_CONFERENCED message.</span></span> <span data-ttu-id="2380e-162">TAPI übergibt daher unabhängig von der API-Version der Anwendung, die die Nachricht empfängt, den übergeordneten Befehl " *hconfcall"* in *dwParam2* .</span><span class="sxs-lookup"><span data-stu-id="2380e-162">TAPI therefore passes the parent call *hConfCall* in *dwParam2* regardless of the API version of the application receiving the message.</span></span> <span data-ttu-id="2380e-163">Im Fall eines Konferenz Aufrufs, der vom Dienstanbieter initiiert wurde, weiß die ältere Anwendung nicht, dass der übergeordnete Aufruf zu einem Konferenz Aufruf geworden ist, es sei denn, es erfolgt eine spontane Untersuchung anderer Informationen (z. b. [**linegetanfrelatedcalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)).</span><span class="sxs-lookup"><span data-stu-id="2380e-163">In the case of a conference call initiated by the service provider, the older application is not aware that the parent call has become a conference call unless it happens to spontaneously examine other information (for example, call [**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)).</span></span>

<span data-ttu-id="2380e-164">Diese Meldung kann nicht deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="2380e-164">This message cannot be disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="2380e-165">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2380e-165">Requirements</span></span>



| <span data-ttu-id="2380e-166">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2380e-166">Requirement</span></span> | <span data-ttu-id="2380e-167">Wert</span><span class="sxs-lookup"><span data-stu-id="2380e-167">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="2380e-168">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="2380e-168">TAPI version</span></span><br/> | <span data-ttu-id="2380e-169">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="2380e-169">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="2380e-170">Header</span><span class="sxs-lookup"><span data-stu-id="2380e-170">Header</span></span><br/>       | <dl> <span data-ttu-id="2380e-171"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="2380e-171"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2380e-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2380e-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2380e-173">**Zeilen \_ Antwort**</span><span class="sxs-lookup"><span data-stu-id="2380e-173">**LINE\_REPLY**</span></span>](line-reply.md)
</dt> <dt>

[<span data-ttu-id="2380e-174">**linecompletetransfer**</span><span class="sxs-lookup"><span data-stu-id="2380e-174">**lineCompleteTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer)
</dt> <dt>

[<span data-ttu-id="2380e-175">**linedezugewiesene eCall**</span><span class="sxs-lookup"><span data-stu-id="2380e-175">**lineDeallocateCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall)
</dt> <dt>

[<span data-ttu-id="2380e-176">**Linedialpara**</span><span class="sxs-lookup"><span data-stu-id="2380e-176">**LINEDIALPARAMS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedialparams)
</dt> <dt>

[<span data-ttu-id="2380e-177">**lineforward**</span><span class="sxs-lookup"><span data-stu-id="2380e-177">**lineForward**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineforward)
</dt> <dt>

[<span data-ttu-id="2380e-178">**linegeneratedigits**</span><span class="sxs-lookup"><span data-stu-id="2380e-178">**lineGenerateDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits)
</dt> <dt>

[<span data-ttu-id="2380e-179">**linegetcallstatus**</span><span class="sxs-lookup"><span data-stu-id="2380e-179">**lineGetCallStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)
</dt> <dt>

[<span data-ttu-id="2380e-180">**lineget-frelatedcalls**</span><span class="sxs-lookup"><span data-stu-id="2380e-180">**lineGetConfRelatedCalls**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)
</dt> <dt>

[<span data-ttu-id="2380e-181">**linemakecall**</span><span class="sxs-lookup"><span data-stu-id="2380e-181">**lineMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[<span data-ttu-id="2380e-182">**linepickup**</span><span class="sxs-lookup"><span data-stu-id="2380e-182">**linePickup**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linepickup)
</dt> <dt>

[<span data-ttu-id="2380e-183">**lineprepareaddumconference**</span><span class="sxs-lookup"><span data-stu-id="2380e-183">**linePrepareAddToConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference)
</dt> <dt>

[<span data-ttu-id="2380e-184">**lineSetupTransfer**</span><span class="sxs-lookup"><span data-stu-id="2380e-184">**lineSetupTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)
</dt> <dt>

[<span data-ttu-id="2380e-185">**lineunpark**</span><span class="sxs-lookup"><span data-stu-id="2380e-185">**lineUnpark**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineunpark)
</dt> </dl>

 

 




