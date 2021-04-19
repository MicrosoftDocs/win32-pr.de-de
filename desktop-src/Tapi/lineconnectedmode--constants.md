---
description: Die \_ Bit-Flag-Konstanten von lineconnectedmode beschreiben verschiedene Unterzustände eines verbundenen Aufrufes.
ms.assetid: d75a5989-3f4e-4e5d-90b1-4e450def017e
title: LINECONNECTEDMODE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5191d3a575ef353c54c91c0e53b3228621b703cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359400"
---
# <a name="lineconnectedmode_-constants"></a><span data-ttu-id="c2209-103">Lineconnectedmode- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="c2209-103">LINECONNECTEDMODE\_ Constants</span></span>

<span data-ttu-id="c2209-104">Die Bit-Flag-Konstanten von **lineconnectedmode \_** beschreiben verschiedene Unterzustände eines verbundenen Aufrufes.</span><span class="sxs-lookup"><span data-stu-id="c2209-104">The **LINECONNECTEDMODE\_** bit-flag constants describe different substates of a connected call.</span></span> <span data-ttu-id="c2209-105">Ein Modus ist als Anrufstatus für die Anwendung verfügbar, nachdem der Aufruf Status in verbunden übergegangen ist, und innerhalb der Zeile "CallState", die angibt, dass \_ der Aufruf von "linecallstate" \_ verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="c2209-105">A mode is available as call status to the application after the call state transitions to connected, and within the LINE\_CALLSTATE message indicating the call is in LINECALLSTATE\_CONNECTED.</span></span> <span data-ttu-id="c2209-106">Diese Werte werden verwendet, wenn der Aufruf einer freigegebenen Adresse (überbrückt) mit anderen Stationen erfolgt (Weitere Informationen finden Sie unter [**lineaddresssharing- \_ Konstanten**](lineaddresssharing--constants.md)), primär für elektronische Schlüsselsysteme.</span><span class="sxs-lookup"><span data-stu-id="c2209-106">These values are used when the call is on an address that is shared (bridged) with other stations (for more information, see [**LINEADDRESSSHARING\_ Constants**](lineaddresssharing--constants.md)), primarily electronic key systems.</span></span> <span data-ttu-id="c2209-107">Die **lineconnectedmode- \_ Konstanten** haben die folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="c2209-107">The **LINECONNECTEDMODE\_constants** have the following values:</span></span>

<dl> <dt>

<span data-ttu-id="c2209-108"><span id="LINECONNECTEDMODE_ACTIVE"></span><span id="lineconnectedmode_active"></span>**lineconnectedmode \_ aktiv**</span><span class="sxs-lookup"><span data-stu-id="c2209-108"><span id="LINECONNECTEDMODE_ACTIVE"></span><span id="lineconnectedmode_active"></span>**LINECONNECTEDMODE\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c2209-109">Gibt an, dass der-Befehl an der aktuellen Station verbunden ist (die aktuelle Station ist ein Teilnehmer des Aufrufes).</span><span class="sxs-lookup"><span data-stu-id="c2209-109">Indicates that the call is connected at the current station (the current station is a participant in the call).</span></span> <span data-ttu-id="c2209-110">Wenn der Zustands Modus des Aufrufes den Wert 0 (null) aufweist, sollte die Anwendung davon ausgehen, dass der Wert "aktiv" ist (Dies wäre die Situation bei einer nicht überbrückten Adresse).</span><span class="sxs-lookup"><span data-stu-id="c2209-110">If the call state mode is 0 (zero), the application should assume that the value is "active" (which would be the situation on a non-bridged address).</span></span> <span data-ttu-id="c2209-111">Der Modus kann während eines Aufrufes zwischen "aktiv" und "inaktiv" wechseln, wenn der Benutzer mit der manuellen Aktion verknüpft und den Vorgang verlässt.</span><span class="sxs-lookup"><span data-stu-id="c2209-111">The mode can switch between ACTIVE and INACTIVE during a call if the user joins and leaves the call through manual action.</span></span> <span data-ttu-id="c2209-112">In solch einer überbrückten Situation kann es vorkommen, dass ein [**linedrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) -oder [**linehold**](/windows/desktop/api/Tapi/nf-tapi-linehold) -Vorgang den-Vorgang nicht tatsächlich löscht oder auf dem Stand hält, da der Status anderer Stationen des Aufrufes möglicherweise regelt (z. b. Wenn Sie versuchen, einen-Befehl anzuhalten, wenn andere Stationen teilnehmen); Stattdessen kann der-Befehl in den inaktiven Modus geändert werden, wenn er an anderen Stationen verbunden bleibt.</span><span class="sxs-lookup"><span data-stu-id="c2209-112">In such a bridged situation, a [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) or [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) operation may possibly not actually drop the call or place it on hold, because the status of other stations on the call may govern (for example, attempting to "hold" a call when other stations are participating is not possible); instead, the call may be changed to the INACTIVE mode if it remains CONNECTED at other stations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c2209-113"><span id="LINECONNECTEDMODE_ACTIVEHELD"></span><span id="lineconnectedmode_activeheld"></span>**lineconnectedmode \_ activeheld**</span><span class="sxs-lookup"><span data-stu-id="c2209-113"><span id="LINECONNECTEDMODE_ACTIVEHELD"></span><span id="lineconnectedmode_activeheld"></span>**LINECONNECTEDMODE\_ACTIVEHELD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c2209-114">Gibt an, dass die Station ein aktiver Teilnehmer des Aufrufes ist, aber dass die Remote Partei den Anruf angehalten hat (die andere Partei hält den Anruf als "OnHold" an).</span><span class="sxs-lookup"><span data-stu-id="c2209-114">Indicates that the station is an active participant in the call, but that the remote party has placed the call on hold (the other party considers the call to be in the onhold state).</span></span> <span data-ttu-id="c2209-115">Diese Informationen sind normalerweise nur verfügbar, wenn beide Endpunkte des Aufrufes innerhalb derselben Wechsel Domäne liegen.</span><span class="sxs-lookup"><span data-stu-id="c2209-115">Normally, such information is available only when both endpoints of the call fall within the same switching domain.</span></span> <span data-ttu-id="c2209-116">Dieses Flag ist nur für Anwendungen verfügbar, die eine TAPI-Version von 2,0 oder höher aushandeln.</span><span class="sxs-lookup"><span data-stu-id="c2209-116">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span> <span data-ttu-id="c2209-117">(TAPI-Versionen 2,0 und höher)</span><span class="sxs-lookup"><span data-stu-id="c2209-117">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c2209-118"><span id="LINECONNECTEDMODE_CONFIRMED"></span><span id="lineconnectedmode_confirmed"></span>**"lineconnectedmode" wurde \_ bestätigt.**</span><span class="sxs-lookup"><span data-stu-id="c2209-118"><span id="LINECONNECTEDMODE_CONFIRMED"></span><span id="lineconnectedmode_confirmed"></span>**LINECONNECTEDMODE\_CONFIRMED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c2209-119">Gibt an, dass der Dienstanbieter eine Benachrichtigung erhalten hat, dass der Anruf in den Status "verbunden" eingetreten ist (z. b. durch Antwort Aufsicht oder ähnliche Mechanismen).</span><span class="sxs-lookup"><span data-stu-id="c2209-119">Indicates that the service provider received affirmative notification that the call has entered the connected state (for example, through answer supervision or similar mechanisms).</span></span> <span data-ttu-id="c2209-120">Dieses Flag ist nur für Anwendungen verfügbar, die eine TAPI-Version von 2,0 oder höher aushandeln.</span><span class="sxs-lookup"><span data-stu-id="c2209-120">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span> <span data-ttu-id="c2209-121">(TAPI-Versionen 2,0 und höher)</span><span class="sxs-lookup"><span data-stu-id="c2209-121">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c2209-122"><span id="LINECONNECTEDMODE_INACTIVE"></span><span id="lineconnectedmode_inactive"></span>**lineconnectedmode \_ inaktiv**</span><span class="sxs-lookup"><span data-stu-id="c2209-122"><span id="LINECONNECTEDMODE_INACTIVE"></span><span id="lineconnectedmode_inactive"></span>**LINECONNECTEDMODE\_INACTIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c2209-123">Gibt an, dass der-Befehl an einer oder mehreren anderen Stationen aktiv ist, die aktuelle Station ist jedoch kein Teilnehmer des Aufrufes.</span><span class="sxs-lookup"><span data-stu-id="c2209-123">Indicates that the call is active at one or more other stations, but the current station is not a participant in the call.</span></span> <span data-ttu-id="c2209-124">Wenn der aufrufstatusmodus 0 (null) ist, sollte die Anwendung davon ausgehen, dass der Wert "aktiv" ist (Dies wäre die Situation bei einer nicht überbrücken Adresse).</span><span class="sxs-lookup"><span data-stu-id="c2209-124">If the call state mode is ZERO, the application should assume that the value is "active" (which would be the situation on a non-bridged address).</span></span> <span data-ttu-id="c2209-125">Ein Anruf im inaktiven Zustand kann mithilfe von [**lineanswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer)verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="c2209-125">A call in the INACTIVE state can be joined using [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer).</span></span> <span data-ttu-id="c2209-126">Viele Vorgänge, die in Aufrufen im verbundenen Zustand gültig sind, können im inaktiven Modus nicht ausgeführt werden, wie z. b. die Überwachung von Tönen und Ziffern, da die Station nicht an dem Anruf teilnimmt. die Überwachung wird in der Regel angehalten (obwohl Sie nicht abgebrochen wird), während der-Befehl im inaktiven Modus</span><span class="sxs-lookup"><span data-stu-id="c2209-126">Many operations that are valid in calls in the CONNECTED state can be impossible in the INACTIVE mode, such as monitoring for tones and digits, because the station is not actually participating in the call; monitoring is usually suspended (although not canceled) while the call is in the INACTIVE mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c2209-127"><span id="LINECONNECTEDMODE_INACTIVEHELD"></span><span id="lineconnectedmode_inactiveheld"></span>**lineconnectedmode \_ inactiveheld**</span><span class="sxs-lookup"><span data-stu-id="c2209-127"><span id="LINECONNECTEDMODE_INACTIVEHELD"></span><span id="lineconnectedmode_inactiveheld"></span>**LINECONNECTEDMODE\_INACTIVEHELD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c2209-128">Gibt an, dass es sich bei der Station nicht um einen aktiven Teilnehmer des Aufrufes handelt und dass die Remote Partei den Anruf angehalten hat.</span><span class="sxs-lookup"><span data-stu-id="c2209-128">Indicates that the station is not an active participant in the call, and that the remote party has placed the call on hold.</span></span> <span data-ttu-id="c2209-129">Dieses Flag ist nur für Anwendungen verfügbar, die eine TAPI-Version von 2,0 oder höher aushandeln.</span><span class="sxs-lookup"><span data-stu-id="c2209-129">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span> <span data-ttu-id="c2209-130">(TAPI-Versionen 2,0 und höher)</span><span class="sxs-lookup"><span data-stu-id="c2209-130">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c2209-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c2209-131">Remarks</span></span>

<span data-ttu-id="c2209-132">Nicht erweiterbar.</span><span class="sxs-lookup"><span data-stu-id="c2209-132">Not extensible.</span></span> <span data-ttu-id="c2209-133">Alle 32 Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="c2209-133">All 32 bits are reserved.</span></span>

<span data-ttu-id="c2209-134">Aus Gründen der Abwärtskompatibilität liegt es in der Verantwortung des Dienstanbieters, die ausgehandelte API-Version in der Zeile zu untersuchen und diese lineconnectedmode-Werte nicht zu verwenden, die \_ von der ausgehandelten Version nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="c2209-134">For backward compatibility, it is the responsibility of the service provider to examine the negotiated API version on the line, and to not use those LINECONNECTEDMODE\_ values that are not supported on the negotiated version.</span></span> <span data-ttu-id="c2209-135">Anwendungen, die nicht von lineconnectedmode erkannt werden, \_ nehmen wahrscheinlich an, dass sich ein in linecallstate \_ verbundener Befehl in lineconnectedmode \_ aktiv befindet.</span><span class="sxs-lookup"><span data-stu-id="c2209-135">Applications that are not cognizant of LINECONNECTEDMODE\_ will most likely assume that a call that is in LINECALLSTATE\_CONNECTED is in LINECONNECTEDMODE\_ACTIVE.</span></span>

<span data-ttu-id="c2209-136">Die inaktiven Werte für "lineconnectedmode" \_ und "lineconnectedmode" \_ werden verwendet, wenn sich der Aufruf auf einer Adresse befindet, die für andere Stationen freigegeben ist (überbrückt, siehe [**lineaddresssharing- \_ Konstanten**](lineaddresssharing--constants.md)), primär in elektronischen Schlüssel Systemen.</span><span class="sxs-lookup"><span data-stu-id="c2209-136">The LINECONNECTEDMODE\_ACTIVE and LINECONNECTEDMODE\_INACTIVE values are used when the call is on an address that is shared with other stations (bridged; see [**LINEADDRESSSHARING\_ Constants**](lineaddresssharing--constants.md)), primarily electronic key systems.</span></span> <span data-ttu-id="c2209-137">Wenn der verbundene CallState-Modus "aktiv" ist, bedeutet dies, dass der-Befehl an der aktuellen Station verbunden ist (die aktuelle Station ist ein Teilnehmer des Aufrufes).</span><span class="sxs-lookup"><span data-stu-id="c2209-137">If the connected call state mode is "active," it means that the call is connected at the current station (the current station is a participant in the call).</span></span> <span data-ttu-id="c2209-138">Wenn der aufrufsstatusmodus "inaktiv" ist, ist der-Befehl an einer oder mehreren anderen Stationen aktiv, aber die aktuelle Station ist kein Teilnehmer des Aufrufes.</span><span class="sxs-lookup"><span data-stu-id="c2209-138">If the call state mode is "inactive," the call is active at one or more other stations, but the current station is not a participant in the call.</span></span> <span data-ttu-id="c2209-139">Wenn der aufrufstatusmodus 0 (null) ist, sollte die Anwendung davon ausgehen, dass der Wert "aktiv" ist (Dies wäre die Situation bei einer nicht überbrücken Adresse).</span><span class="sxs-lookup"><span data-stu-id="c2209-139">If the call state mode is ZERO, the application should assume that the value is "active" (which would be the situation on a non-bridged address).</span></span> <span data-ttu-id="c2209-140">Der Modus kann während eines Aufrufes zwischen "aktiv" und "inaktiv" wechseln, wenn der Benutzer mit der manuellen Aktion verknüpft und den Vorgang verlässt.</span><span class="sxs-lookup"><span data-stu-id="c2209-140">The mode can switch between ACTIVE and INACTIVE during a call if the user joins and leaves the call through manual action.</span></span>

<span data-ttu-id="c2209-141">In solch einer überbrückten Situation kann es vorkommen, dass ein [**linedrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) -oder [**linehold**](/windows/desktop/api/Tapi/nf-tapi-linehold) -Vorgang den Rückruf nicht tatsächlich löscht oder auf dem Stand hält, da der Status anderer Stationen des Aufrufes möglicherweise regelt (z. b. Wenn Sie versuchen, einen Telefon anzuhalten, wenn andere Stationen teilnehmen); Stattdessen kann der-Befehl einfach in den inaktiven Modus geändert werden, wenn er an anderen Stationen verbunden bleibt.</span><span class="sxs-lookup"><span data-stu-id="c2209-141">In such a bridged situation, a [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) or [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) operation may possibly not actually drop the call or place it on hold, because the status of other stations on the call may govern (for example, attempting to "hold" a call when other stations are participating will not be possible); instead, the call can simply be changed to the INACTIVE mode if it remains connected at other stations.</span></span> <span data-ttu-id="c2209-142">Ein-Anruf im inaktiven Zustand kann mithilfe von [**lineanswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer)verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="c2209-142">A call in the INACTIVE state can be joined using the [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer).</span></span>

<span data-ttu-id="c2209-143">Viele Vorgänge, die in Aufrufen im verbundenen Zustand gültig sind, können im inaktiven Modus nicht ausgeführt werden, wie z. b. die Überwachung von Tönen und Ziffern, da die Station nicht an dem Anruf teilnimmt. die Überwachung wird in der Regel angehalten (obwohl Sie nicht abgebrochen wird), während der-Befehl im inaktiven Modus</span><span class="sxs-lookup"><span data-stu-id="c2209-143">Many operations that are valid in calls in the connected state can be impossible in the INACTIVE mode, such as monitoring for tones and digits, because the station is not actually participating in the call; monitoring is usually suspended (although not canceled) while the call is in the INACTIVE mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2209-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2209-144">Requirements</span></span>



| <span data-ttu-id="c2209-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2209-145">Requirement</span></span> | <span data-ttu-id="c2209-146">Wert</span><span class="sxs-lookup"><span data-stu-id="c2209-146">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="c2209-147">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="c2209-147">TAPI version</span></span><br/> | <span data-ttu-id="c2209-148">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="c2209-148">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="c2209-149">Header</span><span class="sxs-lookup"><span data-stu-id="c2209-149">Header</span></span><br/>       | <dl> <span data-ttu-id="c2209-150"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2209-150"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2209-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2209-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2209-152">**lineanswer**</span><span class="sxs-lookup"><span data-stu-id="c2209-152">**lineAnswer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineanswer)
</dt> <dt>

[<span data-ttu-id="c2209-153">**linedrop**</span><span class="sxs-lookup"><span data-stu-id="c2209-153">**lineDrop**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedrop)
</dt> <dt>

[<span data-ttu-id="c2209-154">**linehold**</span><span class="sxs-lookup"><span data-stu-id="c2209-154">**lineHold**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linehold)
</dt> </dl>

 

 




