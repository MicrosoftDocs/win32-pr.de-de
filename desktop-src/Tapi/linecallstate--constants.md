---
description: Die linecallstate \_ -bitflagkonstanten beschreiben die aufrufzustände, in denen ein-Befehl erfolgen kann.
ms.assetid: 18d881ee-cf98-4dec-a561-333c2518935d
title: LINECALLSTATE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d50301dfeca49513a919fba90cc960c7ccb572d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373798"
---
# <a name="linecallstate_-constants"></a><span data-ttu-id="93b76-103">Linecallstate- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="93b76-103">LINECALLSTATE\_ Constants</span></span>

<span data-ttu-id="93b76-104">Die **linecallstate \_** -bitflagkonstanten beschreiben die aufrufzustände, in denen ein-Befehl erfolgen kann.</span><span class="sxs-lookup"><span data-stu-id="93b76-104">The **LINECALLSTATE\_** bit-flag constants describe the call states a call can be in.</span></span>

<dl> <dt>

<span data-ttu-id="93b76-105"><span id="LINECALLSTATE_ACCEPTED"></span><span id="linecallstate_accepted"></span>**linecallstate \_ akzeptiert**</span><span class="sxs-lookup"><span data-stu-id="93b76-105"><span id="LINECALLSTATE_ACCEPTED"></span><span id="linecallstate_accepted"></span>**LINECALLSTATE\_ACCEPTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="93b76-106">Der-Rückruf befand sich im Angebots Zustand und wurde akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="93b76-106">The call was in the offering state and has been accepted.</span></span> <span data-ttu-id="93b76-107">Dies weist auf andere (Überwachungs-) Anwendungen hin, die von der aktuellen Besitzer Anwendung für die Beantwortung des Aufrufes verantwortlich sind.</span><span class="sxs-lookup"><span data-stu-id="93b76-107">This indicates to other (monitoring) applications that the current owner application has claimed responsibility for answering the call.</span></span> <span data-ttu-id="93b76-108">In ISDN wird der Status "akzeptiert" eingegeben, wenn die aufgerufenen Parteien eine Nachricht an den Switch senden, um anzugeben, dass Sie den Aufruf der aufgerufenen Person bereitstellen soll.</span><span class="sxs-lookup"><span data-stu-id="93b76-108">In ISDN, the accepted state is entered when the called-party equipment sends a message to the switch indicating that it is willing to present the call to the called person.</span></span> <span data-ttu-id="93b76-109">Dies hat den Nebeneffekt, dass die Benutzer an beiden Enden des Aufrufens (Klingeln) angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="93b76-109">This has the side effect of alerting (ringing) the users at both ends of the call.</span></span> <span data-ttu-id="93b76-110">Ein eingehender-Rückruf kann immer sofort beantwortet werden, ohne dass er zuerst separat akzeptiert wird.</span><span class="sxs-lookup"><span data-stu-id="93b76-110">An incoming call can always be immediately answered without first being separately accepted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93b76-111"><span id="LINECALLSTATE_BUSY"></span><span id="linecallstate_busy"></span>**linecallstate \_ ausgelastet**</span><span class="sxs-lookup"><span data-stu-id="93b76-111"><span id="LINECALLSTATE_BUSY"></span><span id="linecallstate_busy"></span>**LINECALLSTATE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="93b76-112">Der-Befehl empfängt einen ausgelasteten Ton.</span><span class="sxs-lookup"><span data-stu-id="93b76-112">The call is receiving a busy tone.</span></span> <span data-ttu-id="93b76-113">Ein ausgelasteter Ton gibt an, dass der-Befehl nicht abgeschlossen werden kann, entweder eine Leitung (trunk) oder die Station der Remote Partei wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="93b76-113">A busy tone indicates that the call cannot be completed either a circuit (trunk) or the remote party's station are in use.</span></span> <span data-ttu-id="93b76-114">Weitere Informationen finden Sie unter [**linebusymode- \_ Konstanten**](linebusymode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="93b76-114">See [**LINEBUSYMODE\_ Constants**](linebusymode--constants.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93b76-115"><span id="LINECALLSTATE_CONFERENCED"></span><span id="linecallstate_conferenced"></span>**linecallstate-über \_ Tragung**</span><span class="sxs-lookup"><span data-stu-id="93b76-115"><span id="LINECALLSTATE_CONFERENCED"></span><span id="linecallstate_conferenced"></span>**LINECALLSTATE\_CONFERENCED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="93b76-116">Der-Rückruf ist ein Member eines Konferenz Aufrufes und befindet sich logisch im verbundenen Zustand.</span><span class="sxs-lookup"><span data-stu-id="93b76-116">The call is a member of a conference call and is logically in the connected state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93b76-117"><span id="LINECALLSTATE_CONNECTED"></span><span id="linecallstate_connected"></span>**linecallstate \_ verbunden**</span><span class="sxs-lookup"><span data-stu-id="93b76-117"><span id="LINECALLSTATE_CONNECTED"></span><span id="linecallstate_connected"></span>**LINECALLSTATE\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="93b76-118">Der-Rückruf wurde erstellt, und die Verbindung wird hergestellt.</span><span class="sxs-lookup"><span data-stu-id="93b76-118">The call has been established and the connection is made.</span></span> <span data-ttu-id="93b76-119">Informationen können über den Aufruf zwischen der Ursprungsadresse und der Zieladresse übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="93b76-119">Information is able to flow over the call between the originating address and the destination address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93b76-120"><span id="LINECALLSTATE_DIALING"></span><span id="linecallstate_dialing"></span>**linecallstate- \_ Wähl**</span><span class="sxs-lookup"><span data-stu-id="93b76-120"><span id="LINECALLSTATE_DIALING"></span><span id="linecallstate_dialing"></span>**LINECALLSTATE\_DIALING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="93b76-121">Der Absender ist für den-Befehl wählbare Ziffern.</span><span class="sxs-lookup"><span data-stu-id="93b76-121">The originator is dialing digits on the call.</span></span> <span data-ttu-id="93b76-122">Die einwählbare Ziffern werden vom-Schalter gesammelt.</span><span class="sxs-lookup"><span data-stu-id="93b76-122">The dialed digits are collected by the switch.</span></span> <span data-ttu-id="93b76-123">Beachten Sie, dass weder [**linegeneratedigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) noch [**TSPI \_ linegeneratedigits**](/windows/win32/api/tspi/nf-tspi-tspi_linegeneratedigits) die Linie in den Einwähl Status setzen.</span><span class="sxs-lookup"><span data-stu-id="93b76-123">Note that neither [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) nor [**TSPI\_lineGenerateDigits**](/windows/win32/api/tspi/nf-tspi-tspi_linegeneratedigits) will place the line into the dialing state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93b76-124"><span id="LINECALLSTATE_DIALTONE"></span><span id="linecallstate_dialtone"></span>**linecallstate \_ Dialtone**</span><span class="sxs-lookup"><span data-stu-id="93b76-124"><span id="LINECALLSTATE_DIALTONE"></span><span id="linecallstate_dialtone"></span>**LINECALLSTATE\_DIALTONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="93b76-125">Der-Befehl empfängt einen Wählton vom Switch, was bedeutet, dass der Switch bereit ist, eine einwählbare Zahl zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="93b76-125">The call is receiving a dial tone from the switch, which means that the switch is ready to receive a dialed number.</span></span> <span data-ttu-id="93b76-126">Weitere Informationen finden Sie unter [**linedialtonemode- \_ Konstanten**](linedialtonemode--constants.md) für Bezeichner von speziellen Wähltönen, wie z. b. einen ruckeln-Ton der normalen Sprachnachrichten.</span><span class="sxs-lookup"><span data-stu-id="93b76-126">See [**LINEDIALTONEMODE\_ Constants**](linedialtonemode--constants.md) for identifiers of special dial tones, such as a stutter tone of normal voice mail.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93b76-127"><span id="LINECALLSTATE_DISCONNECTED"></span><span id="linecallstate_disconnected"></span>**linecallstate \_ getrennt**</span><span class="sxs-lookup"><span data-stu-id="93b76-127"><span id="LINECALLSTATE_DISCONNECTED"></span><span id="linecallstate_disconnected"></span>**LINECALLSTATE\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="93b76-128">Der Remote Beteiligte hat die Verbindung mit dem-Befehl getrennt.</span><span class="sxs-lookup"><span data-stu-id="93b76-128">The remote party has disconnected from the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93b76-129"><span id="LINECALLSTATE_IDLE"></span><span id="linecallstate_idle"></span>**linecallstate im \_ Leerlauf**</span><span class="sxs-lookup"><span data-stu-id="93b76-129"><span id="LINECALLSTATE_IDLE"></span><span id="linecallstate_idle"></span>**LINECALLSTATE\_IDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="93b76-130">Der-Befehl ist vorhanden, aber es wurde keine Verbindung hergestellt.</span><span class="sxs-lookup"><span data-stu-id="93b76-130">The call exists but has not been connected.</span></span> <span data-ttu-id="93b76-131">Im-Befehl ist keine Aktivität vorhanden, was bedeutet, dass zurzeit kein-Rückruf aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="93b76-131">No activity exists on the call, which means that no call is currently active.</span></span> <span data-ttu-id="93b76-132">Ein-Rückruf kann nie aus dem Leerlaufzustand übergehen.</span><span class="sxs-lookup"><span data-stu-id="93b76-132">A call can never transition out of the idle state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93b76-133"><span id="LINECALLSTATE_OFFERING"></span><span id="linecallstate_offering"></span>**linecallstate- \_ Angebot**</span><span class="sxs-lookup"><span data-stu-id="93b76-133"><span id="LINECALLSTATE_OFFERING"></span><span id="linecallstate_offering"></span>**LINECALLSTATE\_OFFERING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="93b76-134">Der-Befehl wird der Station angeboten und signalisiert den Eingang eines neuen Aufrufes.</span><span class="sxs-lookup"><span data-stu-id="93b76-134">The call is being offered to the station, signaling the arrival of a new call.</span></span> <span data-ttu-id="93b76-135">Der Angebots Status ist nicht identisch mit der Ursache für das Klingeln eines Telefons oder Computers.</span><span class="sxs-lookup"><span data-stu-id="93b76-135">The offering state is not the same as causing a phone or computer to ring.</span></span> <span data-ttu-id="93b76-136">In einigen Umgebungen wird der Benutzer aufgrund eines Aufrufes Ansichts Zustands nicht so lange Klingeln, bis der Schalter die Zeile an den Ring anweist.</span><span class="sxs-lookup"><span data-stu-id="93b76-136">In some environments, a call in the offering state does not ring the user until the switch instructs the line to ring.</span></span> <span data-ttu-id="93b76-137">Ein Beispiel für die Verwendung ist, wenn ein eingehender-Befehl in mehreren Stations Sätzen, aber nur in den primären Adress Ringen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="93b76-137">An example use might be where an incoming call appears on several station sets but only the primary address rings.</span></span> <span data-ttu-id="93b76-138">Die Anweisung zum Klingeln wirkt sich nicht auf Aufrufe aus.</span><span class="sxs-lookup"><span data-stu-id="93b76-138">The instruction to ring does not affect any call states.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93b76-139"><span id="LINECALLSTATE_ONHOLD"></span><span id="linecallstate_onhold"></span>**linecallstate \_ OnHold**</span><span class="sxs-lookup"><span data-stu-id="93b76-139"><span id="LINECALLSTATE_ONHOLD"></span><span id="linecallstate_onhold"></span>**LINECALLSTATE\_ONHOLD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="93b76-140">Der-Befehl wird vom-Schalter angehalten.</span><span class="sxs-lookup"><span data-stu-id="93b76-140">The call is on hold by the switch.</span></span> <span data-ttu-id="93b76-141">Dadurch wird die physische Zeile freigegeben, wodurch ein weiterer aufrufsbefehl verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="93b76-141">This frees the physical line, which allows another call to use the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93b76-142"><span id="LINECALLSTATE_ONHOLDPENDCONF"></span><span id="linecallstate_onholdpendconf"></span>**linecallstate \_ onholdpdconf**</span><span class="sxs-lookup"><span data-stu-id="93b76-142"><span id="LINECALLSTATE_ONHOLDPENDCONF"></span><span id="linecallstate_onholdpendconf"></span>**LINECALLSTATE\_ONHOLDPENDCONF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="93b76-143">Der-Befehl wird zurzeit angehalten, während er einer Konferenz hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="93b76-143">The call is currently on hold while it is being added to a conference.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93b76-144"><span id="LINECALLSTATE_ONHOLDPENDTRANSFER"></span><span id="linecallstate_onholdpendtransfer"></span>**linecallstate \_ onholdpdtransfer**</span><span class="sxs-lookup"><span data-stu-id="93b76-144"><span id="LINECALLSTATE_ONHOLDPENDTRANSFER"></span><span id="linecallstate_onholdpendtransfer"></span>**LINECALLSTATE\_ONHOLDPENDTRANSFER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="93b76-145">Der-Aufrufer wartet aktuell auf die Übertragung an eine andere Zahl.</span><span class="sxs-lookup"><span data-stu-id="93b76-145">The call is currently on hold awaiting transfer to another number.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93b76-146"><span id="LINECALLSTATE_PROCEEDING"></span><span id="linecallstate_proceeding"></span>**linecallstate wird \_ fortgesetzt**</span><span class="sxs-lookup"><span data-stu-id="93b76-146"><span id="LINECALLSTATE_PROCEEDING"></span><span id="linecallstate_proceeding"></span>**LINECALLSTATE\_PROCEEDING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="93b76-147">Die Wahl ist abgeschlossen, und der Anruf wird durch den Switch oder das Telefon Netzwerk fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="93b76-147">Dialing has completed and the call is proceeding through the switch or telephone network.</span></span> <span data-ttu-id="93b76-148">Dies tritt auf, nachdem die Unterscheidung vollständig ist und bevor der Anruf die gewählte Partei erreicht, wie von "Ringback", "ausgelastet" oder "Antwort" angegeben.</span><span class="sxs-lookup"><span data-stu-id="93b76-148">This occurs after dialing is complete and before the call reaches the dialed party, as indicated by ringback, busy, or answer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93b76-149"><span id="LINECALLSTATE_RINGBACK"></span><span id="linecallstate_ringback"></span>**linecallstate- \_ Ringback**</span><span class="sxs-lookup"><span data-stu-id="93b76-149"><span id="LINECALLSTATE_RINGBACK"></span><span id="linecallstate_ringback"></span>**LINECALLSTATE\_RINGBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="93b76-150">Die aufzurufende Station ist erreicht, und der Schalter des Ziels erzeugt einen Klingel Ton an den Absender zurück.</span><span class="sxs-lookup"><span data-stu-id="93b76-150">The station to be called has been reached, and the destination's switch is generating a ring tone back to the originator.</span></span> <span data-ttu-id="93b76-151">Ein *Rollback* bedeutet, dass die Zieladresse mit dem-Befehl benachrichtigt wird.</span><span class="sxs-lookup"><span data-stu-id="93b76-151">A *ringback* means that the destination address is being alerted to the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93b76-152"><span id="LINECALLSTATE_SPECIALINFO"></span><span id="linecallstate_specialinfo"></span>**linecallstate \_ specialinfo**</span><span class="sxs-lookup"><span data-stu-id="93b76-152"><span id="LINECALLSTATE_SPECIALINFO"></span><span id="linecallstate_specialinfo"></span>**LINECALLSTATE\_SPECIALINFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="93b76-153">Der-Befehl empfängt ein spezielles Informations Signal, das einer Vorabversion vorangestellt ist, die angibt, warum ein-Vorgang nicht abgeschlossen werden kann.</span><span class="sxs-lookup"><span data-stu-id="93b76-153">The call is receiving a special information signal, which precedes a prerecorded announcement indicating why a call cannot be completed.</span></span> <span data-ttu-id="93b76-154">Siehe [**linespecialinfo- \_ Konstanten**](linespecialinfo--constants.md).</span><span class="sxs-lookup"><span data-stu-id="93b76-154">See [**LINESPECIALINFO\_ Constants**](linespecialinfo--constants.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93b76-155"><span id="LINECALLSTATE_UNKNOWN"></span><span id="linecallstate_unknown"></span>**linecallstate \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="93b76-155"><span id="LINECALLSTATE_UNKNOWN"></span><span id="linecallstate_unknown"></span>**LINECALLSTATE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="93b76-156">Der-Befehl ist vorhanden, aber sein Status ist zurzeit unbekannt.</span><span class="sxs-lookup"><span data-stu-id="93b76-156">The call exists, but its state is currently unknown.</span></span> <span data-ttu-id="93b76-157">Dies kann das Ergebnis einer schlechten Rückruf Status Erkennung durch den Dienstanbieter sein.</span><span class="sxs-lookup"><span data-stu-id="93b76-157">This may be the result of poor call progress detection by the service provider.</span></span> <span data-ttu-id="93b76-158">Eine Aufruf Zustands Meldung, bei der der Aufruf Status auf Unknown festgelegt ist, kann auch generiert werden, um die TAPI-dll über einen neuen Aufruf zu informieren, wenn der tatsächliche Aufruf Zustand des Aufrufes nicht genau bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="93b76-158">A call state message with the call state set to unknown may also be generated to inform the TAPI DLL about a new call at a time when the actual call state of the call is not exactly known.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="93b76-159">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="93b76-159">Remarks</span></span>

<span data-ttu-id="93b76-160">Die höherwertigen 8 Bits können einen gerätespezifischen unter Zustand eines beliebigen vordefinierten Zustands definieren, vorausgesetzt, dass eine der oben definierten linecallstate \_ Bits ebenfalls festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="93b76-160">The high-order 8 bits can define a device-specific substate of any of the predefined states, provided that one of the LINECALLSTATE\_ bits defined above is also set.</span></span> <span data-ttu-id="93b76-161">Die 24 Bits mit niedriger Ordnung sind für vordefinierte Zustände reserviert.</span><span class="sxs-lookup"><span data-stu-id="93b76-161">The low-order 24 bits are reserved for predefined states.</span></span>

<span data-ttu-id="93b76-162">Die **linecallstate- \_ Konstanten** werden als Parameter von der [**Zeile \_ CallState**](line-callstate.md) -Nachricht verwendet, die an die Anwendung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="93b76-162">The **LINECALLSTATE\_constants** are used as parameters by the [**LINE\_CALLSTATE**](line-callstate.md) message sent to the application.</span></span> <span data-ttu-id="93b76-163">Die Nachricht enthält den neuen Aufrufstatus, in den der-Befehl umgestellt hat.</span><span class="sxs-lookup"><span data-stu-id="93b76-163">The message carries the new call state that the call transitioned to.</span></span> <span data-ttu-id="93b76-164">Diese Konstanten werden auch als Member in der [**linecallstatus**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) -Struktur verwendet, die von der [**linegetcallstatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus) -Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="93b76-164">These constants are also used as members in the [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) structure returned by the [**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="93b76-165">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="93b76-165">Requirements</span></span>



| <span data-ttu-id="93b76-166">Anforderung</span><span class="sxs-lookup"><span data-stu-id="93b76-166">Requirement</span></span> | <span data-ttu-id="93b76-167">Wert</span><span class="sxs-lookup"><span data-stu-id="93b76-167">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="93b76-168">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="93b76-168">TAPI version</span></span><br/> | <span data-ttu-id="93b76-169">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="93b76-169">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="93b76-170">Header</span><span class="sxs-lookup"><span data-stu-id="93b76-170">Header</span></span><br/>       | <dl> <span data-ttu-id="93b76-171"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="93b76-171"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93b76-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93b76-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93b76-173">**\_liniencallstate**</span><span class="sxs-lookup"><span data-stu-id="93b76-173">**LINE\_CALLSTATE**</span></span>](line-callstate.md)
</dt> <dt>

[<span data-ttu-id="93b76-174">**Linecallstatus**</span><span class="sxs-lookup"><span data-stu-id="93b76-174">**LINECALLSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)
</dt> <dt>

[<span data-ttu-id="93b76-175">**linegeneratedigits**</span><span class="sxs-lookup"><span data-stu-id="93b76-175">**lineGenerateDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits)
</dt> <dt>

[<span data-ttu-id="93b76-176">**linegetcallstatus**</span><span class="sxs-lookup"><span data-stu-id="93b76-176">**lineGetCallStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)
</dt> </dl>

 

