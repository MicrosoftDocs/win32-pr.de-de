---
description: Die "linedisconnectmode" \_ -Bitflag-Konstanten beschreiben verschiedene Gründe für eine Remote-Trennungs Anforderung. Der Verbindungs Modus ist als Telefonstatus für die Anwendung verfügbar, nachdem der Status des Aufrufes in "getrennt" übergeht.
ms.assetid: 1b26f13c-b0bf-4d2c-8514-f0c376e36bcd
title: LINEDISCONNECTMODE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c70ba70175685e2c264343f9345227ee64c206f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371713"
---
# <a name="linedisconnectmode_-constants"></a><span data-ttu-id="af76d-104">Linedisconnectmode- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="af76d-104">LINEDISCONNECTMODE\_ Constants</span></span>

<span data-ttu-id="af76d-105">Die " **linedisconnectmode \_** "-Bitflag-Konstanten beschreiben verschiedene Gründe für eine Remote-Trennungs Anforderung.</span><span class="sxs-lookup"><span data-stu-id="af76d-105">The **LINEDISCONNECTMODE\_** bit-flag constants describe different reasons for a remote disconnect request.</span></span> <span data-ttu-id="af76d-106">Der Verbindungs Modus ist als Telefonstatus für die Anwendung verfügbar, nachdem der Status des Aufrufes in "getrennt" übergeht.</span><span class="sxs-lookup"><span data-stu-id="af76d-106">A disconnect mode is available as call status to the application after the call state transitions to disconnected.</span></span>

<dl> <dt>

<span data-ttu-id="af76d-107"><span id="LINEDISCONNECTMODE_BADADDRESS"></span><span id="linedisconnectmode_badaddress"></span>**linedisconnectmode- \_ badaddress**</span><span class="sxs-lookup"><span data-stu-id="af76d-107"><span id="LINEDISCONNECTMODE_BADADDRESS"></span><span id="linedisconnectmode_badaddress"></span>**LINEDISCONNECTMODE\_BADADDRESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="af76d-108">Die Zieladresse ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="af76d-108">The destination address is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af76d-109"><span id="LINEDISCONNECTMODE_BLOCKED"></span><span id="linedisconnectmode_blocked"></span>**"linedisconnectmode" wurde \_ blockiert.**</span><span class="sxs-lookup"><span data-stu-id="af76d-109"><span id="LINEDISCONNECTMODE_BLOCKED"></span><span id="linedisconnectmode_blocked"></span>**LINEDISCONNECTMODE\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="af76d-110">Der Aufruf konnte nicht verbunden werden, weil Aufrufe von der Ursprungsadresse an der Zieladresse nicht akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="af76d-110">The call could not be connected because calls from the origination address are not being accepted at the destination address.</span></span> <span data-ttu-id="af76d-111">Dies unterscheidet sich von linedisconnectmode \_ ablehnen darin, dass die Blockierung im Netzwerk (eine passive Ablehnung) implementiert wird, während eine Ablehnung in den Ziel Geräten implementiert wird (eine aktive Ablehnung).</span><span class="sxs-lookup"><span data-stu-id="af76d-111">This differs from LINEDISCONNECTMODE\_REJECT in that blocking is implemented in the network (a passive reject) while a rejection is implemented in the destination equipment (an active reject).</span></span> <span data-ttu-id="af76d-112">Die Blockierung kann auf einen bestimmten Ausschluss der Ursprungsadresse oder darauf zurückzuführen sein, dass das Ziel nur Aufrufe von einem ausgewählten Satz von Ursprungs Adressen akzeptiert (geschlossene Benutzergruppe).</span><span class="sxs-lookup"><span data-stu-id="af76d-112">The blocking can be due to a specific exclusion of the origination address, or because the destination accepts calls from only a selected set of origination address (closed user group).</span></span> <span data-ttu-id="af76d-113">(TAPI-Versionen 2,0 und höher)</span><span class="sxs-lookup"><span data-stu-id="af76d-113">(TAPI versions 2.0 and later)</span></span>

<span data-ttu-id="af76d-114">Die Blockierung von linedisconnectmode \_ ist als Blockierungs Antwort geeignet.</span><span class="sxs-lookup"><span data-stu-id="af76d-114">LINEDISCONNECTMODE\_BLOCKED is appropriate as a blocklisted response.</span></span> <span data-ttu-id="af76d-115">Ein Modem hat z. b. eine Antwort empfangen, die mehr als sechs Sekunden gedauert hat, ohne das Rollback zu erkennen, eine bestimmte Anzahl von Wiederholungen nicht zu verbinden, feststellt, dass die Telefonnummer ungültig ist, um aufzurufen, und gibt eine blockgelistete Antwort aus.</span><span class="sxs-lookup"><span data-stu-id="af76d-115">For example, a modem has received an answer, gone more than six seconds without detecting Ringback, failed to connect a defined number of times, determines that the phone number is not valid to call, and issues a 'blocklisted' response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af76d-116"><span id="LINEDISCONNECTMODE_BUSY"></span><span id="linedisconnectmode_busy"></span>**linedisconnectmode \_ ausgelastet**</span><span class="sxs-lookup"><span data-stu-id="af76d-116"><span id="LINEDISCONNECTMODE_BUSY"></span><span id="linedisconnectmode_busy"></span>**LINEDISCONNECTMODE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="af76d-117">Die Station des Remote Benutzers ist ausgelastet.</span><span class="sxs-lookup"><span data-stu-id="af76d-117">The remote user's station is busy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af76d-118"><span id="LINEDISCONNECTMODE_CANCELLED"></span><span id="linedisconnectmode_cancelled"></span>**linedisconnectmode \_ abgebrochen**</span><span class="sxs-lookup"><span data-stu-id="af76d-118"><span id="LINEDISCONNECTMODE_CANCELLED"></span><span id="linedisconnectmode_cancelled"></span>**LINEDISCONNECTMODE\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="af76d-119">Der-Rückruf wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="af76d-119">The call was cancelled.</span></span> <span data-ttu-id="af76d-120">(TAPI-Versionen 2,0 und höher)</span><span class="sxs-lookup"><span data-stu-id="af76d-120">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af76d-121"><span id="LINEDISCONNECTMODE_CONGESTION"></span><span id="linedisconnectmode_congestion"></span>**linedisconnectmode- \_ Überlastung**</span><span class="sxs-lookup"><span data-stu-id="af76d-121"><span id="LINEDISCONNECTMODE_CONGESTION"></span><span id="linedisconnectmode_congestion"></span>**LINEDISCONNECTMODE\_CONGESTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="af76d-122">Das Netzwerk ist überlastet.</span><span class="sxs-lookup"><span data-stu-id="af76d-122">The network is congested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af76d-123"><span id="LINEDISCONNECTMODE_DONOTDISTURB"></span><span id="linedisconnectmode_donotdisturb"></span>**linedisconnectmode- \_ donotstören**</span><span class="sxs-lookup"><span data-stu-id="af76d-123"><span id="LINEDISCONNECTMODE_DONOTDISTURB"></span><span id="linedisconnectmode_donotdisturb"></span>**LINEDISCONNECTMODE\_DONOTDISTURB**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="af76d-124">Der Aufruf konnte nicht verbunden werden, da das Ziel die Funktion "nicht stören" aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="af76d-124">The call could not be connected because the destination has invoked the Do Not Disturb feature.</span></span> <span data-ttu-id="af76d-125">(TAPI-Versionen 2,0 und höher)</span><span class="sxs-lookup"><span data-stu-id="af76d-125">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af76d-126"><span id="LINEDISCONNECTMODE_FORWARDED"></span><span id="linedisconnectmode_forwarded"></span>**linedisconnectmode \_ Weitergeleitet**</span><span class="sxs-lookup"><span data-stu-id="af76d-126"><span id="LINEDISCONNECTMODE_FORWARDED"></span><span id="linedisconnectmode_forwarded"></span>**LINEDISCONNECTMODE\_FORWARDED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="af76d-127">Der-Befehl wurde vom Schalter weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="af76d-127">The call was forwarded by the switch.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af76d-128"><span id="LINEDISCONNECTMODE_INCOMPATIBLE"></span><span id="linedisconnectmode_incompatible"></span>**linedisconnectmode nicht \_ kompatibel**</span><span class="sxs-lookup"><span data-stu-id="af76d-128"><span id="LINEDISCONNECTMODE_INCOMPATIBLE"></span><span id="linedisconnectmode_incompatible"></span>**LINEDISCONNECTMODE\_INCOMPATIBLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="af76d-129">Die Stations Ausrüstung des Remote Benutzers ist nicht mit dem angeforderten Anforderungstyp kompatibel.</span><span class="sxs-lookup"><span data-stu-id="af76d-129">The remote user's station equipment is incompatible with the type of call requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af76d-130"><span id="LINEDISCONNECTMODE_NOANSWER"></span><span id="linedisconnectmode_noanswer"></span>**linedisconnectmode \_ noanswer**</span><span class="sxs-lookup"><span data-stu-id="af76d-130"><span id="LINEDISCONNECTMODE_NOANSWER"></span><span id="linedisconnectmode_noanswer"></span>**LINEDISCONNECTMODE\_NOANSWER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="af76d-131">Die Station des Remote Benutzers antwortet nicht.</span><span class="sxs-lookup"><span data-stu-id="af76d-131">The remote user's station does not answer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af76d-132"><span id="LINEDISCONNECTMODE_NODIALTONE"></span><span id="linedisconnectmode_nodialtone"></span>**linedisconnectmode \_ nodialtone**</span><span class="sxs-lookup"><span data-stu-id="af76d-132"><span id="LINEDISCONNECTMODE_NODIALTONE"></span><span id="linedisconnectmode_nodialtone"></span>**LINEDISCONNECTMODE\_NODIALTONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="af76d-133">Ein DFÜ-Ton wurde innerhalb eines vom Dienstanbieter definierten Timeouts nicht erkannt, zu einem Zeitpunkt während der Abwahl, wenn ein Wert erwartet wurde (z. b. bei einem "W" in der DFÜ-Zeichenfolge).</span><span class="sxs-lookup"><span data-stu-id="af76d-133">A dial tone was not detected within a service-provider defined timeout, at a point during dialing when one was expected (such as at a "W" in the dialable string).</span></span> <span data-ttu-id="af76d-134">Dies kann auch ohne ein vom Dienstanbieter definiertes Timeout Intervall oder ohne Angabe eines Werts im **dwwaitfordialtone** -Member der [**linedialparameams**](/windows/desktop/api/Tapi/ns-tapi-linedialparams) -Struktur vorkommen.</span><span class="sxs-lookup"><span data-stu-id="af76d-134">This can also occur without a service-provider-defined timeout period or without a value specified in the **dwWaitForDialTone** member of the [**LINEDIALPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linedialparams) structure.</span></span> <span data-ttu-id="af76d-135">(TAPI-Versionen 1,4 und höher)</span><span class="sxs-lookup"><span data-stu-id="af76d-135">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af76d-136"><span id="LINEDISCONNECTMODE_NORMAL"></span><span id="linedisconnectmode_normal"></span>**linedisconnectmode \_ Normal**</span><span class="sxs-lookup"><span data-stu-id="af76d-136"><span id="LINEDISCONNECTMODE_NORMAL"></span><span id="linedisconnectmode_normal"></span>**LINEDISCONNECTMODE\_NORMAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="af76d-137">Dabei handelt es sich um eine normale Disconnect-Anforderung durch den Remote Teilnehmer.</span><span class="sxs-lookup"><span data-stu-id="af76d-137">This is a normal disconnect request by the remote party.</span></span> <span data-ttu-id="af76d-138">Der-Befehl wurde normal beendet.</span><span class="sxs-lookup"><span data-stu-id="af76d-138">The call was terminated normally.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af76d-139"><span id="LINEDISCONNECTMODE_NUMBERCHANGED"></span><span id="linedisconnectmode_numberchanged"></span>**linedisconnectmode- \_ nummerierungsänderung**</span><span class="sxs-lookup"><span data-stu-id="af76d-139"><span id="LINEDISCONNECTMODE_NUMBERCHANGED"></span><span id="linedisconnectmode_numberchanged"></span>**LINEDISCONNECTMODE\_NUMBERCHANGED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="af76d-140">Der-Rückruf konnte nicht verbunden werden, da die Ziel Nummer geändert wurde, aber es wurde keine automatische Umleitung zur neuen Nummer bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="af76d-140">The call could not be connected because the destination number has been changed, but automatic redirection to the new number is not provided.</span></span> <span data-ttu-id="af76d-141">(TAPI-Versionen 2,0 und höher)</span><span class="sxs-lookup"><span data-stu-id="af76d-141">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af76d-142"><span id="LINEDISCONNECTMODE_OUTOFORDER"></span><span id="linedisconnectmode_outoforder"></span>**linedisconnectmode- \_ OutOfOrder**</span><span class="sxs-lookup"><span data-stu-id="af76d-142"><span id="LINEDISCONNECTMODE_OUTOFORDER"></span><span id="linedisconnectmode_outoforder"></span>**LINEDISCONNECTMODE\_OUTOFORDER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="af76d-143">Der-Rückruf konnte nicht verbunden oder getrennt werden, da das Zielgerät nicht in der richtigen Reihenfolge ist (Hardwarefehler).</span><span class="sxs-lookup"><span data-stu-id="af76d-143">The call could not be connected or was disconnected because the destination device is out of order (hardware failure).</span></span> <span data-ttu-id="af76d-144">(TAPI-Versionen 2,0 und höher)</span><span class="sxs-lookup"><span data-stu-id="af76d-144">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af76d-145"><span id="LINEDISCONNECTMODE_PICKUP"></span><span id="linedisconnectmode_pickup"></span>**linedisconnectmode \_ Pickup**</span><span class="sxs-lookup"><span data-stu-id="af76d-145"><span id="LINEDISCONNECTMODE_PICKUP"></span><span id="linedisconnectmode_pickup"></span>**LINEDISCONNECTMODE\_PICKUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="af76d-146">Der-Befehl wurde von anderen Orten aus abgerufen.</span><span class="sxs-lookup"><span data-stu-id="af76d-146">The call was picked up from elsewhere.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af76d-147"><span id="LINEDISCONNECTMODE_QOSUNAVAIL"></span><span id="linedisconnectmode_qosunavail"></span>**linedisconnectmode- \_ qosun**</span><span class="sxs-lookup"><span data-stu-id="af76d-147"><span id="LINEDISCONNECTMODE_QOSUNAVAIL"></span><span id="linedisconnectmode_qosunavail"></span>**LINEDISCONNECTMODE\_QOSUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="af76d-148">Der-Rückruf konnte nicht verbunden oder getrennt werden, da die minimale Quality of Service nicht abgerufen oder wieder hergestellt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="af76d-148">The call could not be connected or was disconnected because the minimum quality of service could not be obtained or sustained.</span></span> <span data-ttu-id="af76d-149">Dies unterscheidet sich von linedisconnectmode \_ , da das Fehlen von Ressourcen möglicherweise eine temporäre Bedingung am Ziel ist.</span><span class="sxs-lookup"><span data-stu-id="af76d-149">This differs from LINEDISCONNECTMODE\_INCOMPATIBLE in that the lack of resources may be a temporary condition at the destination.</span></span> <span data-ttu-id="af76d-150">(TAPI-Versionen 2,0 und höher)</span><span class="sxs-lookup"><span data-stu-id="af76d-150">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af76d-151"><span id="LINEDISCONNECTMODE_REJECT"></span><span id="linedisconnectmode_reject"></span>**linedisconnectmode \_ ablehnen**</span><span class="sxs-lookup"><span data-stu-id="af76d-151"><span id="LINEDISCONNECTMODE_REJECT"></span><span id="linedisconnectmode_reject"></span>**LINEDISCONNECTMODE\_REJECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="af76d-152">Der Remote Benutzer hat den-Befehl abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="af76d-152">The remote user has rejected the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af76d-153"><span id="LINEDISCONNECTMODE_TEMPFAILURE"></span><span id="linedisconnectmode_tempfailure"></span>**linedisconnectmode- \_ tempfailure**</span><span class="sxs-lookup"><span data-stu-id="af76d-153"><span id="LINEDISCONNECTMODE_TEMPFAILURE"></span><span id="linedisconnectmode_tempfailure"></span>**LINEDISCONNECTMODE\_TEMPFAILURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="af76d-154">Der-Rückruf konnte nicht verbunden werden oder wurde aufgrund eines temporären Fehlers im Netzwerk getrennt. der Versuch kann später wiederholt werden, und es wird erwartet, dass er letztendlich fertiggestellt wird.</span><span class="sxs-lookup"><span data-stu-id="af76d-154">The call could not be connected or was disconnected because of a temporary failure in the network; the call can be reattempted later and is expected to eventually complete.</span></span> <span data-ttu-id="af76d-155">(TAPI-Versionen 2,0 und höher)</span><span class="sxs-lookup"><span data-stu-id="af76d-155">(TAPI versions 2.0 and later)</span></span>

<span data-ttu-id="af76d-156">"Linedisconnectmode \_ tempfailure" ist als verzögerte Antwort geeignet.</span><span class="sxs-lookup"><span data-stu-id="af76d-156">LINEDISCONNECTMODE\_TEMPFAILURE is appropriate as a delayed response.</span></span> <span data-ttu-id="af76d-157">Ein Modem, das beispielsweise ein ausgelasteter Signal oder eine Entsprechung zu oft in einem bestimmten Zeitraum erhält, endet, dass die Zahl erst wieder aufgerufen werden soll, wenn eine definierte Zeit verstrichen ist, und eine verzögerte Antwort ausgibt.</span><span class="sxs-lookup"><span data-stu-id="af76d-157">For example, a modem getting a busy signal or equivalent too many times in a particular time period concludes that the number should not be called again until a defined time has elapsed and issues a 'delayed' response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af76d-158"><span id="LINEDISCONNECTMODE_UNAVAIL"></span><span id="linedisconnectmode_unavail"></span>**Deaktivieren von linedisconnectmode \_**</span><span class="sxs-lookup"><span data-stu-id="af76d-158"><span id="LINEDISCONNECTMODE_UNAVAIL"></span><span id="linedisconnectmode_unavail"></span>**LINEDISCONNECTMODE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="af76d-159">Der Grund für die Trennung ist nicht verfügbar und wird später noch nicht bekannt werden.</span><span class="sxs-lookup"><span data-stu-id="af76d-159">The reason for the disconnect is unavailable and will not become known later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af76d-160"><span id="LINEDISCONNECTMODE_UNKNOWN"></span><span id="linedisconnectmode_unknown"></span>**"linedisconnectmode" ist \_ unbekannt.**</span><span class="sxs-lookup"><span data-stu-id="af76d-160"><span id="LINEDISCONNECTMODE_UNKNOWN"></span><span id="linedisconnectmode_unknown"></span>**LINEDISCONNECTMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="af76d-161">Der Grund für die Trennungs Anforderung ist unbekannt, kann aber später bekannt werden.</span><span class="sxs-lookup"><span data-stu-id="af76d-161">The reason for the disconnect request is unknown but may become known later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="af76d-162"><span id="LINEDISCONNECTMODE_UNREACHABLE"></span><span id="linedisconnectmode_unreachable"></span>**linedisconnectmode \_ nicht erreichbar**</span><span class="sxs-lookup"><span data-stu-id="af76d-162"><span id="LINEDISCONNECTMODE_UNREACHABLE"></span><span id="linedisconnectmode_unreachable"></span>**LINEDISCONNECTMODE\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="af76d-163">Der Remote Benutzer konnte nicht erreicht werden.</span><span class="sxs-lookup"><span data-stu-id="af76d-163">The remote user could not be reached.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="af76d-164">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="af76d-164">Remarks</span></span>

<span data-ttu-id="af76d-165">Die höherwertigen 16 Bits können für gerätespezifische Erweiterungen zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="af76d-165">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="af76d-166">Die nieder wertigen 16 Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="af76d-166">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="af76d-167">Eine Remote Trennungs Anforderung für einen bestimmten Aufruf führt dazu, dass der Aufruf Status in den getrennten Zustand übergeht und eine [**Zeile \_ CallState**](line-callstate.md) -Meldung an die Anwendung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="af76d-167">A remote disconnect request for a given call results in the call state transitioning to the disconnected state and a [**LINE\_CALLSTATE**](line-callstate.md) message is sent to the application.</span></span> <span data-ttu-id="af76d-168">Die linedisconnectmode- \_ Informationen enthalten Informationen über die Anforderung zum Trennen der Verbindung.</span><span class="sxs-lookup"><span data-stu-id="af76d-168">The LINEDISCONNECTMODE\_ information provides details about the remote disconnect request.</span></span> <span data-ttu-id="af76d-169">Er ist in der [**linecallstatus**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) -Struktur des Aufrufes verfügbar, wenn sich der-Befehl im getrennten Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="af76d-169">It is available in the call's [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) structure when the call is in the disconnected state.</span></span> <span data-ttu-id="af76d-170">Während sich ein-Befehl in diesem Zustand befindet, kann die Anwendung die Informationen und den Status des Aufrufes weiterhin Abfragen.</span><span class="sxs-lookup"><span data-stu-id="af76d-170">While a call is in this state, the application is still allowed to query the call's information and status.</span></span> <span data-ttu-id="af76d-171">Beispielsweise sind Benutzer Benutzerinformationen, die als Teil der Remote Trennung empfangen werden, verfügbar.</span><span class="sxs-lookup"><span data-stu-id="af76d-171">For example, user-user information that is received as part of the remote disconnect is available then.</span></span> <span data-ttu-id="af76d-172">Die Anwendung kann einen getrennten-Rückruf löschen, indem der-Befehl gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="af76d-172">The application can clear a disconnected call by dropping the call.</span></span>

<span data-ttu-id="af76d-173">Aus Gründen der Abwärtskompatibilität liegt es in der Verantwortung des Dienstanbieters, die ausgehandelte API-Version in der Zeile zu untersuchen und diesen linedisconnectmode-Wert nicht zu verwenden, \_ Wenn er von der ausgehandelten Version nicht unterstützt wird (Stattdessen kann "linedisconnectmode \_ Normal" oder "unknown" \_ verwendet werden).</span><span class="sxs-lookup"><span data-stu-id="af76d-173">For backward compatibility, it is the responsibility of the service provider to examine the negotiated API version on the line, and to not use this LINEDISCONNECTMODE\_ value if it is not supported on the negotiated version (LINEDISCONNECTMODE\_NORMAL or \_UNKNOWN could be used instead).</span></span>

## <a name="requirements"></a><span data-ttu-id="af76d-174">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="af76d-174">Requirements</span></span>



| <span data-ttu-id="af76d-175">Anforderung</span><span class="sxs-lookup"><span data-stu-id="af76d-175">Requirement</span></span> | <span data-ttu-id="af76d-176">Wert</span><span class="sxs-lookup"><span data-stu-id="af76d-176">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="af76d-177">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="af76d-177">TAPI version</span></span><br/> | <span data-ttu-id="af76d-178">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="af76d-178">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="af76d-179">Header</span><span class="sxs-lookup"><span data-stu-id="af76d-179">Header</span></span><br/>       | <dl> <span data-ttu-id="af76d-180"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="af76d-180"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af76d-181">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af76d-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af76d-182">**\_liniencallstate**</span><span class="sxs-lookup"><span data-stu-id="af76d-182">**LINE\_CALLSTATE**</span></span>](line-callstate.md)
</dt> <dt>

[<span data-ttu-id="af76d-183">**Linecallstatus**</span><span class="sxs-lookup"><span data-stu-id="af76d-183">**LINECALLSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)
</dt> <dt>

[<span data-ttu-id="af76d-184">**Linedialpara**</span><span class="sxs-lookup"><span data-stu-id="af76d-184">**LINEDIALPARAMS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedialparams)
</dt> </dl>

 

 




