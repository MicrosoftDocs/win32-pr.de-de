---
description: Die \_ Bit-Flag-Konstanten von lineforwardmode beschreiben die Bedingungen, unter denen Aufrufe an eine Adresse weitergeleitet werden können.
ms.assetid: 8cc053bd-1056-42be-b48a-d2312c456893
title: LINEFORWARDMODE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33702be12afaef5d1194ca5c0d288bd967a93e2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370853"
---
# <a name="lineforwardmode_-constants"></a><span data-ttu-id="652ac-103">Lineforwardmode- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="652ac-103">LINEFORWARDMODE\_ Constants</span></span>

<span data-ttu-id="652ac-104">Die Bit-Flag-Konstanten von **lineforwardmode \_** beschreiben die Bedingungen, unter denen Aufrufe an eine Adresse weitergeleitet werden können.</span><span class="sxs-lookup"><span data-stu-id="652ac-104">The **LINEFORWARDMODE\_** bit-flag constants describe the conditions under which calls to an address can be forwarded.</span></span>

<dl> <dt>

<span data-ttu-id="652ac-105"><span id="LINEFORWARDMODE_BUSY"></span><span id="lineforwardmode_busy"></span>**lineforwardmode \_ ausgelastet**</span><span class="sxs-lookup"><span data-stu-id="652ac-105"><span id="LINEFORWARDMODE_BUSY"></span><span id="lineforwardmode_busy"></span>**LINEFORWARDMODE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="652ac-106">Alle Aufrufe an "ausgelastet" weiterleiten, unabhängig von deren Ursprung.</span><span class="sxs-lookup"><span data-stu-id="652ac-106">Forward all calls on busy, irrespective of their origin.</span></span> <span data-ttu-id="652ac-107">Verwenden Sie diesen Wert, wenn die Weiterleitung für interne und externe Aufrufe von ausgelastet ist und keine Antwort separat gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="652ac-107">Use this value when forwarding for internal and external calls on busy and on no answer cannot be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="652ac-108"><span id="LINEFORWARDMODE_BUSYEXTERNAL"></span><span id="lineforwardmode_busyexternal"></span>**lineforwardmode \_ busyextern**</span><span class="sxs-lookup"><span data-stu-id="652ac-108"><span id="LINEFORWARDMODE_BUSYEXTERNAL"></span><span id="lineforwardmode_busyexternal"></span>**LINEFORWARDMODE\_BUSYEXTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="652ac-109">Alle externen Aufrufe an ausgelasteter weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="652ac-109">Forward all external calls on busy.</span></span> <span data-ttu-id="652ac-110">Verwenden Sie diesen Wert, wenn die Weiterleitung für interne und externe Aufrufe von ausgelastet ist und keine Antwort separat gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="652ac-110">Use this value when forwarding for internal and external calls on busy and on no answer can be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="652ac-111"><span id="LINEFORWARDMODE_BUSYINTERNAL"></span><span id="lineforwardmode_busyinternal"></span>**lineforwardmode \_ busyinternal**</span><span class="sxs-lookup"><span data-stu-id="652ac-111"><span id="LINEFORWARDMODE_BUSYINTERNAL"></span><span id="lineforwardmode_busyinternal"></span>**LINEFORWARDMODE\_BUSYINTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="652ac-112">Alle internen Aufrufe von ausgelastet weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="652ac-112">Forward all internal calls on busy.</span></span> <span data-ttu-id="652ac-113">Verwenden Sie diesen Wert, wenn die Weiterleitung für interne und externe Aufrufe von ausgelastet ist und keine Antwort separat gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="652ac-113">Use this value when forwarding for internal and external calls on busy and on no answer can be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="652ac-114"><span id="LINEFORWARDMODE_BUSYNA"></span><span id="lineforwardmode_busyna"></span>**lineforwardmode- \_ busyna**</span><span class="sxs-lookup"><span data-stu-id="652ac-114"><span id="LINEFORWARDMODE_BUSYNA"></span><span id="lineforwardmode_busyna"></span>**LINEFORWARDMODE\_BUSYNA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="652ac-115">Alle Aufrufe an "ausgelastet"/"keine Antwort" weiterleiten, unabhängig von deren Ursprung.</span><span class="sxs-lookup"><span data-stu-id="652ac-115">Forward all calls on busy/no answer, irrespective of their origin.</span></span> <span data-ttu-id="652ac-116">Verwenden Sie diesen Wert, wenn die Weiterleitung für interne und externe Aufrufe von ausgelastet ist und keine Antwort separat gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="652ac-116">Use this value when forwarding for internal and external calls on busy and on no answer cannot be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="652ac-117"><span id="LINEFORWARDMODE_BUSYNAEXTERNAL"></span><span id="lineforwardmode_busynaexternal"></span>**lineforwardmode \_ busynaextern**</span><span class="sxs-lookup"><span data-stu-id="652ac-117"><span id="LINEFORWARDMODE_BUSYNAEXTERNAL"></span><span id="lineforwardmode_busynaexternal"></span>**LINEFORWARDMODE\_BUSYNAEXTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="652ac-118">Leiten Sie alle externen Aufrufe für ausgelastet/keine Antwort weiter.</span><span class="sxs-lookup"><span data-stu-id="652ac-118">Forward all external calls on busy/no answer.</span></span> <span data-ttu-id="652ac-119">Verwenden Sie diesen Wert, wenn die Aufruf Weiterleitung bei "ausgelastet" und "keine Antwort" bei internen Aufrufen nicht separat gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="652ac-119">Use this value when call forwarding on busy and on no answer cannot be controlled separately for internal calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="652ac-120"><span id="LINEFORWARDMODE_BUSYNAINTERNAL"></span><span id="lineforwardmode_busynainternal"></span>**lineforwardmode \_ busynainternal**</span><span class="sxs-lookup"><span data-stu-id="652ac-120"><span id="LINEFORWARDMODE_BUSYNAINTERNAL"></span><span id="lineforwardmode_busynainternal"></span>**LINEFORWARDMODE\_BUSYNAINTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="652ac-121">Alle internen Aufrufe an "ausgelastet"/"keine Antwort" weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="652ac-121">Forward all internal calls on busy/no answer.</span></span> <span data-ttu-id="652ac-122">Verwenden Sie diesen Wert, wenn die Aufruf Weiterleitung bei "ausgelastet" und "keine Antwort" bei internen Aufrufen nicht separat gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="652ac-122">Use this value when call forwarding on busy and on no answer cannot be controlled separately for internal calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="652ac-123"><span id="LINEFORWARDMODE_BUSYNASPECIFIC"></span><span id="lineforwardmode_busynaspecific"></span>**lineforwardmode- \_ busynaspecific**</span><span class="sxs-lookup"><span data-stu-id="652ac-123"><span id="LINEFORWARDMODE_BUSYNASPECIFIC"></span><span id="lineforwardmode_busynaspecific"></span>**LINEFORWARDMODE\_BUSYNASPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="652ac-124">Forward on ausgelastet/keine Antwort alle Aufrufe, die von einer bestimmten Adresse stammen (selektive Aufruf Weiterleitung).</span><span class="sxs-lookup"><span data-stu-id="652ac-124">Forward on busy/no answer all calls that originated at a specified address (selective call forwarding).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="652ac-125"><span id="LINEFORWARDMODE_BUSYSPECIFIC"></span><span id="lineforwardmode_busyspecific"></span>**lineforwardmode- \_ busyspecific**</span><span class="sxs-lookup"><span data-stu-id="652ac-125"><span id="LINEFORWARDMODE_BUSYSPECIFIC"></span><span id="lineforwardmode_busyspecific"></span>**LINEFORWARDMODE\_BUSYSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="652ac-126">Forward an ausgelasteten aufrufen, die bei einer bestimmten Adresse (selektive Aufruf Weiterleitung) entstanden sind.</span><span class="sxs-lookup"><span data-stu-id="652ac-126">Forward on busy all calls that originated at a specified address (selective call forwarding).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="652ac-127"><span id="LINEFORWARDMODE_NOANSW"></span><span id="lineforwardmode_noansw"></span>**lineforwardmode \_ noansw**</span><span class="sxs-lookup"><span data-stu-id="652ac-127"><span id="LINEFORWARDMODE_NOANSW"></span><span id="lineforwardmode_noansw"></span>**LINEFORWARDMODE\_NOANSW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="652ac-128">Alle Aufrufe ohne Antwort weiterleiten, unabhängig von deren Ursprung.</span><span class="sxs-lookup"><span data-stu-id="652ac-128">Forward all calls on no answer, irrespective of their origin.</span></span> <span data-ttu-id="652ac-129">Verwenden Sie diesen Wert, wenn die Aufruf Weiterleitung für interne und externe Aufrufe ohne Antwort nicht separat gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="652ac-129">Use this value when call forwarding for internal and external calls on no answer cannot be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="652ac-130"><span id="LINEFORWARDMODE_NOANSWEXTERNAL"></span><span id="lineforwardmode_noanswexternal"></span>**lineforwardmode \_ noanswexternal**</span><span class="sxs-lookup"><span data-stu-id="652ac-130"><span id="LINEFORWARDMODE_NOANSWEXTERNAL"></span><span id="lineforwardmode_noanswexternal"></span>**LINEFORWARDMODE\_NOANSWEXTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="652ac-131">Alle externen Aufrufe ohne Antwort weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="652ac-131">Forward all external calls on no answer.</span></span> <span data-ttu-id="652ac-132">Verwenden Sie diesen Wert, wenn die Weiterleitung für interne und externe Aufrufe ohne Antwort separat gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="652ac-132">Use this value when forwarding for internal and external calls on no answer can be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="652ac-133"><span id="LINEFORWARDMODE_NOANSWINTERNAL"></span><span id="lineforwardmode_noanswinternal"></span>**lineforwardmode \_ noanswinternal**</span><span class="sxs-lookup"><span data-stu-id="652ac-133"><span id="LINEFORWARDMODE_NOANSWINTERNAL"></span><span id="lineforwardmode_noanswinternal"></span>**LINEFORWARDMODE\_NOANSWINTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="652ac-134">Alle internen Aufrufe ohne Antwort weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="652ac-134">Forward all internal calls on no answer.</span></span> <span data-ttu-id="652ac-135">Verwenden Sie diesen Wert, wenn die Weiterleitung für interne und externe Aufrufe ohne Antwort separat gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="652ac-135">Use this value when forwarding for internal and external calls on no answer can be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="652ac-136"><span id="LINEFORWARDMODE_NOANSWSPECIFIC"></span><span id="lineforwardmode_noanswspecific"></span>**lineforwardmode \_ noanswspecific**</span><span class="sxs-lookup"><span data-stu-id="652ac-136"><span id="LINEFORWARDMODE_NOANSWSPECIFIC"></span><span id="lineforwardmode_noanswspecific"></span>**LINEFORWARDMODE\_NOANSWSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="652ac-137">Forward auf keine Antwort alle Aufrufe, die von einer angegebenen Adresse stammen (selektive Aufruf Weiterleitung).</span><span class="sxs-lookup"><span data-stu-id="652ac-137">Forward on no answer all calls that originated at a specified address (selective call forwarding).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="652ac-138"><span id="LINEFORWARDMODE_UNAVAIL"></span><span id="lineforwardmode_unavail"></span>**"lineforwardmode" ist \_ nicht erreichbar.**</span><span class="sxs-lookup"><span data-stu-id="652ac-138"><span id="LINEFORWARDMODE_UNAVAIL"></span><span id="lineforwardmode_unavail"></span>**LINEFORWARDMODE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="652ac-139">Aufrufe werden weitergeleitet, aber die Bedingungen, unter denen die Weiterleitung erfolgt, sind nicht bekannt, und der Dienstanbieter wird nie bekannt sein.</span><span class="sxs-lookup"><span data-stu-id="652ac-139">Calls are forwarded, but the conditions under which forwarding will occur are not known, and will never be known by the service provider.</span></span> <span data-ttu-id="652ac-140">(TAPI-Versionen 1,4 und höher)</span><span class="sxs-lookup"><span data-stu-id="652ac-140">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="652ac-141"><span id="LINEFORWARDMODE_UNCOND"></span><span id="lineforwardmode_uncond"></span>**lineforwardmode \_ untd**</span><span class="sxs-lookup"><span data-stu-id="652ac-141"><span id="LINEFORWARDMODE_UNCOND"></span><span id="lineforwardmode_uncond"></span>**LINEFORWARDMODE\_UNCOND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="652ac-142">Alle Aufrufe unabhängig von ihrem Ursprung bedingungslos weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="652ac-142">Forward all calls unconditionally, irrespective of their origin.</span></span> <span data-ttu-id="652ac-143">Verwenden Sie diesen Wert, wenn die bedingungslose Weiterleitung für interne und externe Aufrufe nicht separat gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="652ac-143">Use this value when unconditional forwarding for internal and external calls cannot be controlled separately.</span></span> <span data-ttu-id="652ac-144">Bei der bedingungslosen Weiterleitung wird die Weiterleitung von ausgelasteten und/oder keine Antwort Bedingungen</span><span class="sxs-lookup"><span data-stu-id="652ac-144">Unconditional forwarding overrides forwarding on busy and/or no answer conditions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="652ac-145"><span id="LINEFORWARDMODE_UNCONDEXTERNAL"></span><span id="lineforwardmode_uncondexternal"></span>**lineforwardmode \_ unkonform**</span><span class="sxs-lookup"><span data-stu-id="652ac-145"><span id="LINEFORWARDMODE_UNCONDEXTERNAL"></span><span id="lineforwardmode_uncondexternal"></span>**LINEFORWARDMODE\_UNCONDEXTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="652ac-146">Leiten Sie alle externen Aufrufe bedingungslos weiter.</span><span class="sxs-lookup"><span data-stu-id="652ac-146">Forward all external calls unconditionally.</span></span> <span data-ttu-id="652ac-147">Verwenden Sie diesen Wert, wenn die Bedingungs bedingte Weiterleitung für interne und externe Aufrufe separat gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="652ac-147">Use this value when unconditional forwarding for internal and external calls can be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="652ac-148"><span id="LINEFORWARDMODE_UNCONDINTERNAL"></span><span id="lineforwardmode_uncondinternal"></span>**lineforwardmode \_ unintern**</span><span class="sxs-lookup"><span data-stu-id="652ac-148"><span id="LINEFORWARDMODE_UNCONDINTERNAL"></span><span id="lineforwardmode_uncondinternal"></span>**LINEFORWARDMODE\_UNCONDINTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="652ac-149">Alle internen Aufrufe bedingungslos weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="652ac-149">Forward all internal calls unconditionally.</span></span> <span data-ttu-id="652ac-150">Verwenden Sie diesen Wert, wenn die Bedingungs bedingte Weiterleitung für interne und externe Aufrufe separat gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="652ac-150">Use this value when unconditional forwarding for internal and external calls can be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="652ac-151"><span id="LINEFORWARDMODE_UNCONDSPECIFIC"></span><span id="lineforwardmode_uncondspecific"></span>**lineforwardmode \_ nicht-spezifisch**</span><span class="sxs-lookup"><span data-stu-id="652ac-151"><span id="LINEFORWARDMODE_UNCONDSPECIFIC"></span><span id="lineforwardmode_uncondspecific"></span>**LINEFORWARDMODE\_UNCONDSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="652ac-152">Alle Aufrufe, die von einer angegebenen Adresse stammen (selektive Aufruf Weiterleitung), bedingungslos weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="652ac-152">Unconditionally forward all calls that originated at a specified address (selective call forwarding).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="652ac-153"><span id="LINEFORWARDMODE_UNKNOWN"></span><span id="lineforwardmode_unknown"></span>**"lineforwardmode" \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="652ac-153"><span id="LINEFORWARDMODE_UNKNOWN"></span><span id="lineforwardmode_unknown"></span>**LINEFORWARDMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="652ac-154">Aufrufe werden weitergeleitet, aber die Bedingungen, unter denen die Weiterleitung erfolgt, sind zurzeit nicht bekannt.</span><span class="sxs-lookup"><span data-stu-id="652ac-154">Calls are forwarded, but the conditions under which forwarding will occur are not known at this time.</span></span> <span data-ttu-id="652ac-155">Es ist möglich, dass die Bedingungen zu einem späteren Zeitpunkt bekannt werden.</span><span class="sxs-lookup"><span data-stu-id="652ac-155">It is possible that the conditions may become known at a future time.</span></span> <span data-ttu-id="652ac-156">(TAPI-Versionen 1,4 und höher)</span><span class="sxs-lookup"><span data-stu-id="652ac-156">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="652ac-157">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="652ac-157">Remarks</span></span>

<span data-ttu-id="652ac-158">Keine Erweiterbarkeit.</span><span class="sxs-lookup"><span data-stu-id="652ac-158">No extensibility.</span></span> <span data-ttu-id="652ac-159">Alle 32 Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="652ac-159">All 32 bits are reserved.</span></span>

<span data-ttu-id="652ac-160">Die von lineforwardmode definierten Bitflags \_ sind nicht orthogonal.</span><span class="sxs-lookup"><span data-stu-id="652ac-160">The bit flags defined by LINEFORWARDMODE\_ are not orthogonal.</span></span> <span data-ttu-id="652ac-161">Bei der bedingungslosen Weiterleitung werden alle spezifischen Bedingungen, z. b. ausgelastet oder keine Antwort</span><span class="sxs-lookup"><span data-stu-id="652ac-161">Unconditional forwarding ignores any specific condition such as busy or no answer.</span></span> <span data-ttu-id="652ac-162">Wenn die bedingungslose Weiterleitung nicht wirksam ist, kann die Weiterleitung an ausgelastet und ohne Antwort separat oder nicht separat gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="652ac-162">If unconditional forwarding is not in effect, then forwarding on busy and on no answer can be controlled separately or not separately.</span></span> <span data-ttu-id="652ac-163">Bei separater Steuerung \_ können die noansw-Flags "lineforwardmode ausgelastet" und "lineforwardmode" \_ separat verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="652ac-163">If controlled separately, the LINEFORWARDMODE\_BUSY and LINEFORWARDMODE\_NOANSW flags can be used separately.</span></span> <span data-ttu-id="652ac-164">Wenn diese nicht separat gesteuert wird, muss das Flag lineforwardmode \_ busyna verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="652ac-164">If not controlled separately, the flag LINEFORWARDMODE\_BUSYNA must be used.</span></span> <span data-ttu-id="652ac-165">Wenn die Weiterleitung interner und externer Aufrufe separat gesteuert werden kann, können auch die externen lineforwardmode \_ -und lineforwardmode- \_ Flags separat verwendet werden. andernfalls wird die Kombination verwendet.</span><span class="sxs-lookup"><span data-stu-id="652ac-165">Similarly, if forwarding of internal and external calls can be controlled separately, then LINEFORWARDMODE\_INTERNAL and LINEFORWARDMODE\_EXTERNAL flags can be used separately; otherwise the combination is used.</span></span>

<span data-ttu-id="652ac-166">Adress Funktionen geben an, welche Weiterleitungs Modi für jede Adresse verfügbar sind, die einer Zeile zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="652ac-166">Address capabilities indicate which forwarding modes are available for each address assigned to a line.</span></span> <span data-ttu-id="652ac-167">Eine Anwendung kann [**lineforward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) verwenden, um Weiterleitungs Bedingungen auf dem Switch festzulegen.</span><span class="sxs-lookup"><span data-stu-id="652ac-167">An application can use [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) to set forwarding conditions at the switch.</span></span>

<span data-ttu-id="652ac-168">Aus Gründen der Abwärtskompatibilität liegt es in der Verantwortung des Dienstanbieters, die ausgehandelte API-Version in der Zeile zu untersuchen und diese lineforwardmode-Werte nicht zu verwenden, \_ Wenn Sie von der ausgehandelten Version nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="652ac-168">For backward compatibility, it is the responsibility of the service provider to examine the negotiated API version on the line, and to not use these LINEFORWARDMODE\_ values if the negotiated version does not support them.</span></span>

## <a name="requirements"></a><span data-ttu-id="652ac-169">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="652ac-169">Requirements</span></span>



| <span data-ttu-id="652ac-170">Anforderung</span><span class="sxs-lookup"><span data-stu-id="652ac-170">Requirement</span></span> | <span data-ttu-id="652ac-171">Wert</span><span class="sxs-lookup"><span data-stu-id="652ac-171">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="652ac-172">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="652ac-172">TAPI version</span></span><br/> | <span data-ttu-id="652ac-173">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="652ac-173">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="652ac-174">Header</span><span class="sxs-lookup"><span data-stu-id="652ac-174">Header</span></span><br/>       | <dl> <span data-ttu-id="652ac-175"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="652ac-175"><dt>Tapi.h</dt></span></span> </dl> |



 

 




