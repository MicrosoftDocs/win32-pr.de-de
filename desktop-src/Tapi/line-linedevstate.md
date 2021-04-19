---
description: Die TAPI- \_ linienlinedevstate-Nachricht wird gesendet, wenn sich der Status eines Zeilen Geräts geändert hat. Die Anwendung kann linegetlinedevstatus aufrufen, um den neuen Status der Zeile zu ermitteln.
ms.assetid: 15f616de-db47-4577-9a47-94f9292253dd
title: LINE_LINEDEVSTATE Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 079e4494b7eb2e1bfe46b5470138e4e9f44fbb0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372352"
---
# <a name="line_linedevstate-message"></a><span data-ttu-id="e6a04-104">\_Linienlinedevstate-Meldung</span><span class="sxs-lookup"><span data-stu-id="e6a04-104">LINE\_LINEDEVSTATE message</span></span>

<span data-ttu-id="e6a04-105">Die TAPI **- \_ linienlinedevstate** -Nachricht wird gesendet, wenn sich der Status eines Zeilen Geräts geändert hat.</span><span class="sxs-lookup"><span data-stu-id="e6a04-105">The TAPI **LINE\_LINEDEVSTATE** message is sent when the state of a line device has changed.</span></span> <span data-ttu-id="e6a04-106">Die Anwendung kann [**linegetlinedevstatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus) aufrufen, um den neuen Status der Zeile zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="e6a04-106">The application can invoke [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus) to determine the new status of the line.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="e6a04-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6a04-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6a04-108">*hdevice*</span><span class="sxs-lookup"><span data-stu-id="e6a04-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="e6a04-109">Ein Handle für das liniengerät.</span><span class="sxs-lookup"><span data-stu-id="e6a04-109">A handle to the line device.</span></span> <span data-ttu-id="e6a04-110">Dieser Parameter ist **null** , wenn *dwParam1* linedevstate \_ REIT ist.</span><span class="sxs-lookup"><span data-stu-id="e6a04-110">This parameter is **NULL** when *dwParam1* is LINEDEVSTATE\_REINIT.</span></span>

</dd> <dt>

<span data-ttu-id="e6a04-111">*dwcallbackinstance*</span><span class="sxs-lookup"><span data-stu-id="e6a04-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="e6a04-112">Die beim Öffnen der Zeile angegebene Rückruf Instanz.</span><span class="sxs-lookup"><span data-stu-id="e6a04-112">The callback instance supplied when opening the line.</span></span> <span data-ttu-id="e6a04-113">Wenn der *dwParam1* -Parameter linedevstate \_ REIT ist, ist der *dwcallbackinstance* -Parameter ungültig und auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e6a04-113">If the *dwParam1* parameter is LINEDEVSTATE\_REINIT, the *dwCallbackInstance* parameter is not valid and is set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="e6a04-114">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="e6a04-114">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="e6a04-115">Das Element des Zeilen Gerätestatus, das geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="e6a04-115">The line device status item that has changed.</span></span> <span data-ttu-id="e6a04-116">Der-Parameter kann eine oder mehrere der [**linedevstate- \_ Konstanten**](linedevstate--constants.md)sein.</span><span class="sxs-lookup"><span data-stu-id="e6a04-116">The parameter can be one or more of the [**LINEDEVSTATE\_ constants**](linedevstate--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="e6a04-117">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="e6a04-117">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="e6a04-118">Die Interpretation dieses Parameters hängt vom Wert von *dwParam1* ab.</span><span class="sxs-lookup"><span data-stu-id="e6a04-118">The interpretation of this parameter depends on the value of *dwParam1*.</span></span> <span data-ttu-id="e6a04-119">Wenn *dwParam1* ein linedevstate- \_ Klingeln ist, enthält *dwParam2* den Ring Modus, mit dem der Schalter die Zeile an den Ring anweist.</span><span class="sxs-lookup"><span data-stu-id="e6a04-119">If *dwParam1* is LINEDEVSTATE\_RINGING, *dwParam2* contains the ring mode with which the switch instructs the line to ring.</span></span> <span data-ttu-id="e6a04-120">Gültige ringmodi sind Zahlen im Bereich von 1 bis **dwnumringmodi**, wobei **dwnumringmodes** eine Linien Geräte Funktion ist.</span><span class="sxs-lookup"><span data-stu-id="e6a04-120">Valid ring modes are numbers in the range one to **dwNumRingModes**, where **dwNumRingModes** is a line device capability.</span></span>

<span data-ttu-id="e6a04-121">Wenn *dwParam1* "linedevstate" ist \_ und die Meldung von TAPI als Ergebnis der Übersetzung einer neuen API-Nachricht in eine REIT-Nachricht ausgegeben wurde, enthält *dwParam2* den *dwmsg* -Parameter der ursprünglichen Nachricht (z. b. [**line \_ Create**](line-create.md) oder line \_ linedevstate).</span><span class="sxs-lookup"><span data-stu-id="e6a04-121">If *dwParam1* is LINEDEVSTATE\_REINIT, and the message was issued by TAPI as a result of translation of a new API message into a REINIT message, then *dwParam2* contains the *dwMsg* parameter of the original message (for example, [**LINE\_CREATE**](line-create.md) or LINE\_LINEDEVSTATE).</span></span> <span data-ttu-id="e6a04-122">Wenn *dwParam2* NULL ist, weist dies darauf hin, dass die REIT-Nachricht eine "Real"-REIT-Nachricht ist, die erfordert, dass die Anwendung [**LineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown) zu dem frühestmöglichen Zweck aufruft.</span><span class="sxs-lookup"><span data-stu-id="e6a04-122">If *dwParam2* is zero, this indicates that the REINIT message is a "real" REINIT message that requires the application to call [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown) at its earliest convenience.</span></span>

</dd> <dt>

<span data-ttu-id="e6a04-123">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="e6a04-123">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="e6a04-124">Die Interpretation dieses Parameters hängt vom Wert von *dwParam1* ab.</span><span class="sxs-lookup"><span data-stu-id="e6a04-124">The interpretation of this parameter depends on the value of *dwParam1*.</span></span> <span data-ttu-id="e6a04-125">Wenn *dwParam1* ein linedevstate- \_ Klingeln ist, enthält *dwParam3* die Ring Anzahl für dieses Ring Ereignis.</span><span class="sxs-lookup"><span data-stu-id="e6a04-125">If *dwParam1* is LINEDEVSTATE\_RINGING, *dwParam3* contains the ring count for this ring event.</span></span> <span data-ttu-id="e6a04-126">Die Ring Anzahl beginnt bei 0 (null).</span><span class="sxs-lookup"><span data-stu-id="e6a04-126">The ring count starts at zero.</span></span>

<span data-ttu-id="e6a04-127">Wenn *dwParam1* linedevstate \_ REIT ist, und die Nachricht wurde von TAPI als Ergebnis der Übersetzung einer neuen API-Nachricht in eine REIT-Nachricht ausgegeben. anschließend enthält *dwParam3* den *dwParam1* -Parameter der ursprünglichen Nachricht (z. b. linedevstate \_ translatechange oder einen anderen Wert von linedevstate \_ , wenn *dwParam2* line \_ linedevstate ist, oder der neue Geräte Bezeichner, wenn *dwParam2* [**line \_ Create**](line-create.md)ist).</span><span class="sxs-lookup"><span data-stu-id="e6a04-127">If *dwParam1* is LINEDEVSTATE\_REINIT, and the message was issued by TAPI as a result of translation of a new API message into a REINIT message, then *dwParam3* contains the *dwParam1* parameter of the original message (for example, LINEDEVSTATE\_TRANSLATECHANGE or some other LINEDEVSTATE\_ value, if *dwParam2* is LINE\_LINEDEVSTATE, or the new device identifier, if *dwParam2* is [**LINE\_CREATE**](line-create.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6a04-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e6a04-128">Return value</span></span>

<span data-ttu-id="e6a04-129">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="e6a04-129">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6a04-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e6a04-130">Remarks</span></span>

<span data-ttu-id="e6a04-131">Das Senden der **\_ linienlinedevstate** -Nachricht kann mit [**linesetstatusmessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages)gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="e6a04-131">The sending of the **LINE\_LINEDEVSTATE** message can be controlled with [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages).</span></span> <span data-ttu-id="e6a04-132">Eine Anwendung kann Status Element Änderungen anzeigen, über die Sie benachrichtigt werden möchten.</span><span class="sxs-lookup"><span data-stu-id="e6a04-132">An application can indicate status item changes about which it wants to be notified.</span></span> <span data-ttu-id="e6a04-133">Standardmäßig ist die gesamte Status Berichterstattung deaktiviert, mit Ausnahme von linedevstate \_ , die nicht deaktiviert werden kann.</span><span class="sxs-lookup"><span data-stu-id="e6a04-133">By default, all status reporting is disabled except for LINEDEVSTATE\_REINIT, which cannot be disabled.</span></span> <span data-ttu-id="e6a04-134">Diese Nachricht wird an alle Anwendungen gesendet, die über ein Handle für die Zeile verfügen, einschließlich derjenigen, die [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) aufgerufen haben, wobei der *dwprivileges* -Parameter auf linecallprivilege \_ None, linecallprivilege \_ Owner, linecallprivilege \_ Monitor oder zulässige Kombinationen von diesen festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e6a04-134">This message is sent to all applications that have a handle to the line, including those that called [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) with the *dwPrivileges* parameter set to LINECALLPRIVILEGE\_NONE, LINECALLPRIVILEGE\_OWNER, LINECALLPRIVILEGE\_MONITOR, or permitted combinations of these.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6a04-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e6a04-135">Requirements</span></span>



| <span data-ttu-id="e6a04-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e6a04-136">Requirement</span></span> | <span data-ttu-id="e6a04-137">Wert</span><span class="sxs-lookup"><span data-stu-id="e6a04-137">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e6a04-138">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="e6a04-138">TAPI version</span></span><br/> | <span data-ttu-id="e6a04-139">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="e6a04-139">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="e6a04-140">Header</span><span class="sxs-lookup"><span data-stu-id="e6a04-140">Header</span></span><br/>       | <dl> <span data-ttu-id="e6a04-141"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6a04-141"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6a04-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6a04-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6a04-143">**Zeilen \_ Schließen**</span><span class="sxs-lookup"><span data-stu-id="e6a04-143">**LINE\_CLOSE**</span></span>](line-close.md)
</dt> <dt>

[<span data-ttu-id="e6a04-144">**Zeilen \_ Erstellung**</span><span class="sxs-lookup"><span data-stu-id="e6a04-144">**LINE\_CREATE**</span></span>](line-create.md)
</dt> <dt>

[<span data-ttu-id="e6a04-145">**Linedevcaps**</span><span class="sxs-lookup"><span data-stu-id="e6a04-145">**LINEDEVCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)
</dt> <dt>

[<span data-ttu-id="e6a04-146">**linegetdevcaps**</span><span class="sxs-lookup"><span data-stu-id="e6a04-146">**lineGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)
</dt> <dt>

[<span data-ttu-id="e6a04-147">**linegetdevconfig**</span><span class="sxs-lookup"><span data-stu-id="e6a04-147">**lineGetDevConfig**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)
</dt> <dt>

[<span data-ttu-id="e6a04-148">**linegettranslatecaps**</span><span class="sxs-lookup"><span data-stu-id="e6a04-148">**lineGetTranslateCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)
</dt> <dt>

[<span data-ttu-id="e6a04-149">**lineinitialize**</span><span class="sxs-lookup"><span data-stu-id="e6a04-149">**lineInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)
</dt> <dt>

[<span data-ttu-id="e6a04-150">**lineOpen**</span><span class="sxs-lookup"><span data-stu-id="e6a04-150">**lineOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[<span data-ttu-id="e6a04-151">**linesetstatus-Meldungen**</span><span class="sxs-lookup"><span data-stu-id="e6a04-151">**lineSetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages)
</dt> <dt>

[<span data-ttu-id="e6a04-152">**LineShutdown**</span><span class="sxs-lookup"><span data-stu-id="e6a04-152">**lineShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)
</dt> <dt>

[<span data-ttu-id="e6a04-153">**Linetranslatecaps**</span><span class="sxs-lookup"><span data-stu-id="e6a04-153">**LINETRANSLATECAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps)
</dt> <dt>

[<span data-ttu-id="e6a04-154">**lineuncompletecall**</span><span class="sxs-lookup"><span data-stu-id="e6a04-154">**lineUncompleteCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall)
</dt> </dl>

 

 




