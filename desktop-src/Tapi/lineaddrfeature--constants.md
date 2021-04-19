---
description: Die lineaddrfeature- \_ Konstanten Listen die Vorgänge auf, die für eine Adresse aufgerufen werden können.
ms.assetid: dedeee7b-578b-4b19-8b99-5cd23779d661
title: LINEADDRFEATURE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 825902c2943806d1d495e14a0f0a5042f2949796
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366702"
---
# <a name="lineaddrfeature_-constants"></a><span data-ttu-id="dbe58-103">Lineaddrfeature- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="dbe58-103">LINEADDRFEATURE\_ Constants</span></span>

<span data-ttu-id="dbe58-104">Die **lineaddrfeature \_** -Konstanten Listen die Vorgänge auf, die für eine Adresse aufgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="dbe58-104">The **LINEADDRFEATURE\_** constants list the operations that can be invoked on an address.</span></span>

<dl> <dt>

<span data-ttu-id="dbe58-105"><span id="LINEADDRFEATURE_FORWARD"></span><span id="lineaddrfeature_forward"></span>**lineaddrfeature \_ Vorwärts**</span><span class="sxs-lookup"><span data-stu-id="dbe58-105"><span id="LINEADDRFEATURE_FORWARD"></span><span id="lineaddrfeature_forward"></span>**LINEADDRFEATURE\_FORWARD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dbe58-106">Die Adresse kann weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="dbe58-106">The address can be forwarded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dbe58-107"><span id="LINEADDRFEATURE_MAKECALL"></span><span id="lineaddrfeature_makecall"></span>**lineaddrfeature \_ MakeCall**</span><span class="sxs-lookup"><span data-stu-id="dbe58-107"><span id="LINEADDRFEATURE_MAKECALL"></span><span id="lineaddrfeature_makecall"></span>**LINEADDRFEATURE\_MAKECALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dbe58-108">Ein ausgehender Anruf kann für die Adresse platziert werden.</span><span class="sxs-lookup"><span data-stu-id="dbe58-108">An outgoing call can be placed on the address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dbe58-109"><span id="LINEADDRFEATURE_PICKUP"></span><span id="lineaddrfeature_pickup"></span>**Abholung von lineaddrfeature \_**</span><span class="sxs-lookup"><span data-stu-id="dbe58-109"><span id="LINEADDRFEATURE_PICKUP"></span><span id="lineaddrfeature_pickup"></span>**LINEADDRFEATURE\_PICKUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dbe58-110">Ein-Rückruf kann an der Adresse abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="dbe58-110">A call can be picked up at the address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dbe58-111"><span id="LINEADDRFEATURE_PICKUPDIRECT"></span><span id="lineaddrfeature_pickupdirect"></span>**lineaddrfeature \_ pickupdirect**</span><span class="sxs-lookup"><span data-stu-id="dbe58-111"><span id="LINEADDRFEATURE_PICKUPDIRECT"></span><span id="lineaddrfeature_pickupdirect"></span>**LINEADDRFEATURE\_PICKUPDIRECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dbe58-112">Die [**linepickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) -Funktion kann verwendet werden, um einen-Rückruf für eine bestimmte Adresse auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="dbe58-112">The [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) function can be used to pick up a call on a specific address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dbe58-113"><span id="LINEADDRFEATURE_PICKUPGROUP"></span><span id="lineaddrfeature_pickupgroup"></span>**"lineaddrfeature" \_ pickupgroup**</span><span class="sxs-lookup"><span data-stu-id="dbe58-113"><span id="LINEADDRFEATURE_PICKUPGROUP"></span><span id="lineaddrfeature_pickupgroup"></span>**LINEADDRFEATURE\_PICKUPGROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dbe58-114">Die [**linepickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) -Funktion kann verwendet werden, um einen-Rückruf in der Gruppe zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="dbe58-114">The [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) function can be used to pick up a call in the group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dbe58-115"><span id="LINEADDRFEATURE_PICKUPHELD"></span><span id="lineaddrfeature_pickupheld"></span>**lineaddrfeature \_ pickat**</span><span class="sxs-lookup"><span data-stu-id="dbe58-115"><span id="LINEADDRFEATURE_PICKUPHELD"></span><span id="lineaddrfeature_pickupheld"></span>**LINEADDRFEATURE\_PICKUPHELD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dbe58-116">Die [**linepickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) -Funktion (mit einer **null** -Zieladresse) kann verwendet werden, um einen für die Adresse gespeicherten-Befehl zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="dbe58-116">The [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) function (with a **null** destination address) can be used to pick up a call that is held on the address.</span></span> <span data-ttu-id="dbe58-117">Dies wird normalerweise nur in einer überbrückten exklusiven Anordnung verwendet.</span><span class="sxs-lookup"><span data-stu-id="dbe58-117">This is normally used only in a bridged-exclusive arrangement.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dbe58-118"><span id="LINEADDRFEATURE_PICKUPWAITING"></span><span id="lineaddrfeature_pickupwaiting"></span>**lineaddrfeature \_ pickupwaiting**</span><span class="sxs-lookup"><span data-stu-id="dbe58-118"><span id="LINEADDRFEATURE_PICKUPWAITING"></span><span id="lineaddrfeature_pickupwaiting"></span>**LINEADDRFEATURE\_PICKUPWAITING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dbe58-119">Die [**linepickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) -Funktion (mit einer **null** -Zieladresse) kann verwendet werden, um einen wartenden callcallaufzurufen.</span><span class="sxs-lookup"><span data-stu-id="dbe58-119">The [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) function (with a **null** destination address) can be used to pick up a call waiting call.</span></span> <span data-ttu-id="dbe58-120">Beachten Sie, dass dies nicht notwendigerweise darauf hinweist, dass ein warte Vorgang tatsächlich vorhanden ist, da es für ein Telefoniegerät oftmals nicht möglich ist, einen solchen Rückruf automatisch zu erkennen. Es zeigt jedoch an, dass die Hook-Flash-Funktion aufgerufen wird, um zu einem solchen Aufruf zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="dbe58-120">Note that this does not necessarily indicate that a waiting call is actually present, because it is often impossible for a telephony device to automatically detect such a call; it does, however, indicate that the hook-flash function will be invoked to attempt to switch to such a call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dbe58-121"><span id="LINEADDRFEATURE_SETMEDIACONTROL"></span><span id="lineaddrfeature_setmediacontrol"></span>**lineaddrfeature \_ setmediacontrol**</span><span class="sxs-lookup"><span data-stu-id="dbe58-121"><span id="LINEADDRFEATURE_SETMEDIACONTROL"></span><span id="lineaddrfeature_setmediacontrol"></span>**LINEADDRFEATURE\_SETMEDIACONTROL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dbe58-122">Für diese Adresse kann ein mediensteuer Element festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="dbe58-122">Media control can be set on this address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dbe58-123"><span id="LINEADDRFEATURE_SETTERMINAL"></span><span id="lineaddrfeature_setterminal"></span>**lineaddrfeature \_ setterminal**</span><span class="sxs-lookup"><span data-stu-id="dbe58-123"><span id="LINEADDRFEATURE_SETTERMINAL"></span><span id="lineaddrfeature_setterminal"></span>**LINEADDRFEATURE\_SETTERMINAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dbe58-124">Die Terminal Modi für diese Adresse können festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="dbe58-124">The terminal modes for this address can be set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dbe58-125"><span id="LINEADDRFEATURE_SETUPCONF"></span><span id="lineaddrfeature_setupconf"></span>**lineaddrfeature \_ setupconf**</span><span class="sxs-lookup"><span data-stu-id="dbe58-125"><span id="LINEADDRFEATURE_SETUPCONF"></span><span id="lineaddrfeature_setupconf"></span>**LINEADDRFEATURE\_SETUPCONF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dbe58-126">An dieser Adresse kann ein Konferenzgespräch mit einem anfänglichen **null** -aufrufsbefehl eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="dbe58-126">A conference call with a **NULL** initial call can be set up at this address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dbe58-127"><span id="LINEADDRFEATURE_UNCOMPLETECALL"></span><span id="lineaddrfeature_uncompletecall"></span>**uncompletecallcenter für lineaddrfeature \_**</span><span class="sxs-lookup"><span data-stu-id="dbe58-127"><span id="LINEADDRFEATURE_UNCOMPLETECALL"></span><span id="lineaddrfeature_uncompletecall"></span>**LINEADDRFEATURE\_UNCOMPLETECALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dbe58-128">Anforderungen zum Abrufen von Anforderungen können an dieser Adresse abgebrochen werden.</span><span class="sxs-lookup"><span data-stu-id="dbe58-128">Call completion requests can be canceled at this address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dbe58-129"><span id="LINEADDRFEATURE_UNPARK"></span><span id="lineaddrfeature_unpark"></span>**lineaddrfeature \_ unpark**</span><span class="sxs-lookup"><span data-stu-id="dbe58-129"><span id="LINEADDRFEATURE_UNPARK"></span><span id="lineaddrfeature_unpark"></span>**LINEADDRFEATURE\_UNPARK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dbe58-130">Aufrufe können mithilfe dieser Adresse entparkt werden.</span><span class="sxs-lookup"><span data-stu-id="dbe58-130">Calls can be unparked using this address.</span></span>

> [!Note]  
> <span data-ttu-id="dbe58-131">Wenn keines der neuen geänderten "Pickup"-Bits im **dwaddressfeatures** -Member in [**lineaddressstatus**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) festgelegt ist, aber das Pickup-Bit "lineaddrfeature" \_ festgelegt ist, kann jeder der Pickup-Modi funktionieren. der Dienstanbieter hat einfach nicht angegeben, welche Werte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dbe58-131">If none of the new modified "PICKUP" bits is set in the **dwAddressFeatures** member in [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) but the LINEADDRFEATURE\_PICKUP bit is set, then any of the pickup modes may work; the service provider has simply not specified which ones.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="dbe58-132"><span id="LINEADDRFEATURE_FORWARDDND"></span><span id="lineaddrfeature_forwarddnd"></span>**\_weiterforwarddnd für lineaddrfeature**</span><span class="sxs-lookup"><span data-stu-id="dbe58-132"><span id="LINEADDRFEATURE_FORWARDDND"></span><span id="lineaddrfeature_forwarddnd"></span>**LINEADDRFEATURE\_FORWARDDND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dbe58-133">Die [**lineforward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) -Funktion (mit einer leeren Zieladresse) kann verwendet werden, um die Funktion "nicht stören" für die Adresse zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="dbe58-133">The [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) function (with an empty destination address) can be used to turn on the Do Not Disturb feature on the address.</span></span> <span data-ttu-id="dbe58-134">Lineaddrfeature \_ Forward wird ebenfalls festgelegt.</span><span class="sxs-lookup"><span data-stu-id="dbe58-134">LINEADDRFEATURE\_FORWARD will also be set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dbe58-135"><span id="LINEADDRFEATURE_FORWARDFWD"></span><span id="lineaddrfeature_forwardfwd"></span>**lineaddrfeature \_ forwardfwd**</span><span class="sxs-lookup"><span data-stu-id="dbe58-135"><span id="LINEADDRFEATURE_FORWARDFWD"></span><span id="lineaddrfeature_forwardfwd"></span>**LINEADDRFEATURE\_FORWARDFWD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dbe58-136">Die [**lineforward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) -Funktion kann verwendet werden, um Aufrufe an die Adresse an andere Zahlen weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="dbe58-136">The [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) function can be used to forward calls on the address to other numbers.</span></span> <span data-ttu-id="dbe58-137">Lineaddrfeature \_ Forward wird ebenfalls festgelegt.</span><span class="sxs-lookup"><span data-stu-id="dbe58-137">LINEADDRFEATURE\_FORWARD will also be set.</span></span>

> [!Note]  
> <span data-ttu-id="dbe58-138">Wenn keines der neuen geänderten "Forward"-Bits im **dwaddressfeatures** -Member in [**lineaddressstatus**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) festgelegt ist, aber das lineaddrfeature- \_ Forward-Bit festgelegt ist, kann jeder der vorwärts Modi funktionieren. der Dienstanbieter hat einfach nicht angegeben, welche Werte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dbe58-138">If neither of the new modified "FORWARD" bits is set in the **dwAddressFeatures** member in [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) but the LINEADDRFEATURE\_FORWARD bit is set, then any of the forward modes may work; the service provider has simply not specified which ones.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dbe58-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dbe58-139">Remarks</span></span>

<span data-ttu-id="dbe58-140">Keine Erweiterbarkeit.</span><span class="sxs-lookup"><span data-stu-id="dbe58-140">No extensibility.</span></span> <span data-ttu-id="dbe58-141">Alle 32 Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="dbe58-141">All 32 bits are reserved.</span></span>

<span data-ttu-id="dbe58-142">Diese Konstante wird sowohl in [**lineaddresscaps**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) (von [**linegetaddresscaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)zurückgegeben) als auch in [**lineaddressstatus**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) (zurückgegeben von [**linegetaddressstatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)) verwendet.</span><span class="sxs-lookup"><span data-stu-id="dbe58-142">This constant is used both in [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) (returned by [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)) and in [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) (returned by [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)).</span></span> <span data-ttu-id="dbe58-143">**Lineaddresscaps** meldet die Verfügbarkeit der Adress Features durch den Dienstanbieter (hauptsächlich den Switch) für eine bestimmte Adresse.</span><span class="sxs-lookup"><span data-stu-id="dbe58-143">**LINEADDRESSCAPS** reports the availability of the address features by the service provider (mainly the switch) for a given address.</span></span> <span data-ttu-id="dbe58-144">Eine Anwendung würde diese Entscheidung treffen, wenn Sie initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="dbe58-144">An application would make this determination when it initializes.</span></span> <span data-ttu-id="dbe58-145">Die [**lineaddressstatus**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) -Struktur meldet für eine angegebene Adresse, welche Adress Features tatsächlich aufgerufen werden können, während sich die Adresse im aktuellen Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="dbe58-145">The [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) structure reports, for a given address, which address features can actually be invoked while the address is in the current state.</span></span> <span data-ttu-id="dbe58-146">Diese Bestimmung wird von einer Anwendung nach Änderungen des Adress Zustands dynamisch durchgeführt, was in der Regel durch Aufrufe im Zusammenhang mit der Adresse verursacht wird.</span><span class="sxs-lookup"><span data-stu-id="dbe58-146">An application would make this determination dynamically after address-state changes, typically caused by call-related activities on the address.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbe58-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dbe58-147">Requirements</span></span>



| <span data-ttu-id="dbe58-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dbe58-148">Requirement</span></span> | <span data-ttu-id="dbe58-149">Wert</span><span class="sxs-lookup"><span data-stu-id="dbe58-149">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="dbe58-150">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="dbe58-150">TAPI version</span></span><br/> | <span data-ttu-id="dbe58-151">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="dbe58-151">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="dbe58-152">Header</span><span class="sxs-lookup"><span data-stu-id="dbe58-152">Header</span></span><br/>       | <dl> <span data-ttu-id="dbe58-153"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbe58-153"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbe58-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dbe58-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbe58-155">**Lineaddresscaps**</span><span class="sxs-lookup"><span data-stu-id="dbe58-155">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="dbe58-156">**Lineaddressstatus**</span><span class="sxs-lookup"><span data-stu-id="dbe58-156">**LINEADDRESSSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[<span data-ttu-id="dbe58-157">**lineforward**</span><span class="sxs-lookup"><span data-stu-id="dbe58-157">**lineForward**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineforward)
</dt> <dt>

[<span data-ttu-id="dbe58-158">**linegetaddresscaps**</span><span class="sxs-lookup"><span data-stu-id="dbe58-158">**lineGetAddressCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> <dt>

[<span data-ttu-id="dbe58-159">**linegetaddressstatus**</span><span class="sxs-lookup"><span data-stu-id="dbe58-159">**lineGetAddressStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)
</dt> <dt>

[<span data-ttu-id="dbe58-160">**linepickup**</span><span class="sxs-lookup"><span data-stu-id="dbe58-160">**linePickup**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linepickup)
</dt> </dl>

 

 




