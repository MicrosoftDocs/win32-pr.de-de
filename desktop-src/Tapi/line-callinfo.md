---
description: Die TAPI-zeilige \_ CallInfo-Meldung wird gesendet, wenn sich die Aufruf Informationen über den angegebenen Aufruf geändert haben. Die Anwendung kann linegetcallinfo aufrufen, um die aktuellen Aufruf Informationen zu bestimmen.
ms.assetid: eb882409-6842-434e-9f93-61cf0c11d1d0
title: LINE_CALLINFO Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6005ab5383816ead440f5a1a7d580bfaccb5c1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356482"
---
# <a name="line_callinfo-message"></a><span data-ttu-id="098db-104">Zeile \_ CallInfo-Meldung</span><span class="sxs-lookup"><span data-stu-id="098db-104">LINE\_CALLINFO message</span></span>

<span data-ttu-id="098db-105">Die TAPI- **zeilige \_ CallInfo** -Meldung wird gesendet, wenn sich die Aufruf Informationen über den angegebenen Aufruf geändert haben.</span><span class="sxs-lookup"><span data-stu-id="098db-105">The TAPI **LINE\_CALLINFO** message is sent when the call information about the specified call has changed.</span></span> <span data-ttu-id="098db-106">Die Anwendung kann [**linegetcallinfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) aufrufen, um die aktuellen Aufruf Informationen zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="098db-106">The application can invoke [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) to determine the current call information.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="098db-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="098db-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="098db-108">*hdevice*</span><span class="sxs-lookup"><span data-stu-id="098db-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="098db-109">Ein Handle für den-Befehl.</span><span class="sxs-lookup"><span data-stu-id="098db-109">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="098db-110">*dwcallbackinstance*</span><span class="sxs-lookup"><span data-stu-id="098db-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="098db-111">Die beim Öffnen der Zeile des Aufrufs angegebene Rückruf Instanz.</span><span class="sxs-lookup"><span data-stu-id="098db-111">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="098db-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="098db-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="098db-113">Das aufrufinformationselement, das geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="098db-113">The call information item that has changed.</span></span> <span data-ttu-id="098db-114">Kann eine oder mehrere der [**linecallinfostate- \_ Konstanten**](linecallinfostate--constants.md)sein.</span><span class="sxs-lookup"><span data-stu-id="098db-114">Can be one or more of the [**LINECALLINFOSTATE\_ constants**](linecallinfostate--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="098db-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="098db-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="098db-116">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="098db-116">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="098db-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="098db-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="098db-118">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="098db-118">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="098db-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="098db-119">Return value</span></span>

<span data-ttu-id="098db-120">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="098db-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="098db-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="098db-121">Remarks</span></span>

<span data-ttu-id="098db-122">An Anwendungen, die bereits über ein Handle für den Aufruf verfügen, wird eine **Zeile " \_ CallInfo** " mit dem Hinweis " *nuwnersincr*", " *numuwnersdecr*" und/oder " *nummonitorschge* " gesendet.</span><span class="sxs-lookup"><span data-stu-id="098db-122">A **LINE\_CALLINFO** message with a *NumOwnersIncr*, *NumOwnersDecr*, and/or *NumMonitorsChanged* indication is sent to applications that already have a handle for the call.</span></span> <span data-ttu-id="098db-123">Dies kann das Ergebnis einer anderen Anwendung sein, die den Besitz ändert oder eine Überwachung für einen Aufruf mit [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen), [**lineclose**](/windows/desktop/api/Tapi/nf-tapi-lineclose), [**LineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown), [**linesetcallprivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege), [**linegetnewcalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls)und [**linegetconfig frelatedcalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)durchführt.</span><span class="sxs-lookup"><span data-stu-id="098db-123">This can be the result of another application changing ownership or monitorship to a call with [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen), [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose), [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown), [**lineSetCallPrivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege), [**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls), and [**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls).</span></span>

<span data-ttu-id="098db-124">Diese **Zeilen- \_ CallInfo** -Meldungen werden nicht gesendet, wenn eine Benachrichtigung über einen neuen Aufruf in [**einer \_ zeilencallstate**](line-callstate.md) -Nachricht bereitgestellt wird, da die Aufruf Informationen bereits die richtige Anzahl von Besitzern und Monitoren zum Zeitpunkt der Übermittlung der Zeilen Aufruf \_ Zustands Meldungen widerspiegeln.</span><span class="sxs-lookup"><span data-stu-id="098db-124">These **LINE\_CALLINFO** messages are not sent when a notification of a new call is provided in a [**LINE\_CALLSTATE**](line-callstate.md) message, because the call information already reflects the correct number of owners and monitors at the time the LINE\_CALLSTATE messages are sent.</span></span> <span data-ttu-id="098db-125">**Zeile \_ CallInfo** -Meldungen werden auch dann unterdrückt, wenn TAPI von TAPI zum Überwachen des nicht unbekannten Mechanismus linecallstate angeboten wird \_ .</span><span class="sxs-lookup"><span data-stu-id="098db-125">**LINE\_CALLINFO** messages are also suppressed in the case where a call is offered by TAPI to monitors through the LINECALLSTATE\_UNKNOWN mechanism.</span></span>

> [!Note]  
> <span data-ttu-id="098db-126">Die Anwendung, die eine Änderung in der Anzahl von Besitzern oder Monitoren bewirkt (z. b. durch Aufrufen von [**linedezugecall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) oder [**linesetcallprivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege)), empfängt nicht selbst eine Meldung, die angibt, dass die Änderung abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="098db-126">The application that causes a change in the number of owners or monitors (for example, by invoking [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) or [**lineSetCallPrivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege)) does not itself receive a message indicating that the change has been done.</span></span>

 

<span data-ttu-id="098db-127">Für einen Aufruf werden keine **Zeilen- \_ CallInfo** -Meldungen gesendet, nachdem der Aufruf in den *Leerlauf* Zustand wechselt.</span><span class="sxs-lookup"><span data-stu-id="098db-127">No **LINE\_CALLINFO** messages are sent for a call after the call has entered the *idle* state.</span></span> <span data-ttu-id="098db-128">Insbesondere werden Änderungen an der Anzahl von Besitzern und Monitoren nicht gemeldet, wenn Anwendungen ihre Handles für den Leerlauf aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="098db-128">Specifically, changes in the number of owners and monitors are not reported as applications deallocate their handles for the idle call.</span></span>

## <a name="requirements"></a><span data-ttu-id="098db-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="098db-129">Requirements</span></span>



| <span data-ttu-id="098db-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="098db-130">Requirement</span></span> | <span data-ttu-id="098db-131">Wert</span><span class="sxs-lookup"><span data-stu-id="098db-131">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="098db-132">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="098db-132">TAPI version</span></span><br/> | <span data-ttu-id="098db-133">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="098db-133">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="098db-134">Header</span><span class="sxs-lookup"><span data-stu-id="098db-134">Header</span></span><br/>       | <dl> <span data-ttu-id="098db-135"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="098db-135"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="098db-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="098db-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="098db-137">**lineclose**</span><span class="sxs-lookup"><span data-stu-id="098db-137">**lineClose**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[<span data-ttu-id="098db-138">**linedezugewiesene eCall**</span><span class="sxs-lookup"><span data-stu-id="098db-138">**lineDeallocateCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall)
</dt> <dt>

[<span data-ttu-id="098db-139">**linegetcallinfo**</span><span class="sxs-lookup"><span data-stu-id="098db-139">**lineGetCallInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)
</dt> <dt>

[<span data-ttu-id="098db-140">**lineget-frelatedcalls**</span><span class="sxs-lookup"><span data-stu-id="098db-140">**lineGetConfRelatedCalls**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)
</dt> <dt>

[<span data-ttu-id="098db-141">**linegetnewcalls**</span><span class="sxs-lookup"><span data-stu-id="098db-141">**lineGetNewCalls**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls)
</dt> <dt>

[<span data-ttu-id="098db-142">**lineOpen**</span><span class="sxs-lookup"><span data-stu-id="098db-142">**lineOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[<span data-ttu-id="098db-143">**linesetcallprivilege**</span><span class="sxs-lookup"><span data-stu-id="098db-143">**lineSetCallPrivilege**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege)
</dt> <dt>

[<span data-ttu-id="098db-144">**LineShutdown**</span><span class="sxs-lookup"><span data-stu-id="098db-144">**lineShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)
</dt> </dl>

 

 




