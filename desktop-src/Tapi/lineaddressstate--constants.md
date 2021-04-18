---
description: Die lineaddressstate \_ -Bitflag-Konstanten beschreiben verschiedene Adress Status Elemente.
ms.assetid: f06140d0-f41a-4228-93c5-21d609af5473
title: LINEADDRESSSTATE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 483ac665c41989c65b43419442601dfb70667dc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352131"
---
# <a name="lineaddressstate_-constants"></a><span data-ttu-id="56a65-103">Lineaddressstate- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="56a65-103">LINEADDRESSSTATE\_ Constants</span></span>

<span data-ttu-id="56a65-104">Die **lineaddressstate \_** -Bitflag-Konstanten beschreiben verschiedene Adress Status Elemente.</span><span class="sxs-lookup"><span data-stu-id="56a65-104">The **LINEADDRESSSTATE\_** bit-flag constants describe various address status items.</span></span>

<dl> <dt>

<span data-ttu-id="56a65-105"><span id="LINEADDRESSSTATE_CAPSCHANGE"></span><span id="lineaddressstate_capschange"></span>**lineaddressstate \_ capschange**</span><span class="sxs-lookup"><span data-stu-id="56a65-105"><span id="LINEADDRESSSTATE_CAPSCHANGE"></span><span id="lineaddressstate_capschange"></span>**LINEADDRESSSTATE\_CAPSCHANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="56a65-106">Gibt an, dass ein oder mehrere der Elemente in der [**lineaddresscaps**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) -Struktur für die Adresse aufgrund von Konfigurationsänderungen, die vom Benutzer oder anderen Bedingungen vorgenommen wurden, geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="56a65-106">Indicates that, due to configuration changes made by the user or other circumstances, one or more of the members in the [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) structure for the address have changed.</span></span> <span data-ttu-id="56a65-107">Die Anwendung sollte [**linegetaddresscaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps) zum Lesen der aktualisierten Struktur verwenden.</span><span class="sxs-lookup"><span data-stu-id="56a65-107">The application should use [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps) to read the updated structure.</span></span> <span data-ttu-id="56a65-108">Wenn ein Dienstanbieter eine [**Zeile \_ addressstate**](line-addressstate.md) -Nachricht mit diesem Wert an TAPI sendet, übergibt TAPI ihn an Anwendungen, die die TAPI-Version 1,4 oder höher ausgehandelt haben. Anwendungen, die eine vorherige API-Version aushandeln, erhalten [**Zeilen- \_ linedevstate**](line-linedevstate.md) -Nachrichten, die linedevstate \_ REIT enthalten, sodass diese die aktualisierten Informationen Herunterfahren und erneut initialisieren müssen.</span><span class="sxs-lookup"><span data-stu-id="56a65-108">If a service provider sends a [**LINE\_ADDRESSSTATE**](line-addressstate.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous API version will receive [**LINE\_LINEDEVSTATE**](line-linedevstate.md) messages specifying LINEDEVSTATE\_REINIT, requiring them to shut down and reinitialize their connection to TAPI to obtain the updated information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56a65-109"><span id="LINEADDRESSSTATE_DEVSPECIFIC"></span><span id="lineaddressstate_devspecific"></span>**lineaddressstate \_ DevSpecific**</span><span class="sxs-lookup"><span data-stu-id="56a65-109"><span id="LINEADDRESSSTATE_DEVSPECIFIC"></span><span id="lineaddressstate_devspecific"></span>**LINEADDRESSSTATE\_DEVSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="56a65-110">Das gerätespezifische Element des Adress Status hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="56a65-110">The device-specific item of the address status has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56a65-111"><span id="LINEADDRESSSTATE_FORWARD"></span><span id="lineaddressstate_forward"></span>**lineaddressstate \_ Vorwärts**</span><span class="sxs-lookup"><span data-stu-id="56a65-111"><span id="LINEADDRESSSTATE_FORWARD"></span><span id="lineaddressstate_forward"></span>**LINEADDRESSSTATE\_FORWARD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="56a65-112">Der Weiterleitungs Status der Adresse hat sich geändert, einschließlich der Anzahl der Ringe zum Ermitteln der Bedingung "keine Antwort".</span><span class="sxs-lookup"><span data-stu-id="56a65-112">The forwarding status of the address has changed, including possibly the number of rings for determining a no-answer condition.</span></span> <span data-ttu-id="56a65-113">Die Anwendung sollte den Adress Status überprüfen, um Details zum aktuellen Weiterleitungs Status der Adresse zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="56a65-113">The application should check the address status to determine details about the address's current forwarding status.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56a65-114"><span id="LINEADDRESSSTATE_INUSEMANY"></span><span id="lineaddressstate_inusemany"></span>**lineaddressstate \_ inusemany**</span><span class="sxs-lookup"><span data-stu-id="56a65-114"><span id="LINEADDRESSSTATE_INUSEMANY"></span><span id="lineaddressstate_inusemany"></span>**LINEADDRESSSTATE\_INUSEMANY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="56a65-115">Die überwachte oder überbrückte Adresse wurde von einer Station in der Verwendung durch mehr als eine Station geändert.</span><span class="sxs-lookup"><span data-stu-id="56a65-115">The monitored or bridged address has changed from being in use by one station to being in use by more than one station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56a65-116"><span id="LINEADDRESSSTATE_INUSEONE"></span><span id="lineaddressstate_inuseone"></span>**lineaddressstate \_ inuseone**</span><span class="sxs-lookup"><span data-stu-id="56a65-116"><span id="LINEADDRESSSTATE_INUSEONE"></span><span id="lineaddressstate_inuseone"></span>**LINEADDRESSSTATE\_INUSEONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="56a65-117">Die Adresse hat sich im Leerlauf geändert oder von vielen überbrückten Stationen verwendet, um von nur einer Station verwendet zu werden.</span><span class="sxs-lookup"><span data-stu-id="56a65-117">The address has changed from idle or in use by many bridged stations to being in use by just one station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56a65-118"><span id="LINEADDRESSSTATE_INUSEZERO"></span><span id="lineaddressstate_inusezero"></span>**lineaddressstate \_ inusezero**</span><span class="sxs-lookup"><span data-stu-id="56a65-118"><span id="LINEADDRESSSTATE_INUSEZERO"></span><span id="lineaddressstate_inusezero"></span>**LINEADDRESSSTATE\_INUSEZERO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="56a65-119">Die Adresse wurde in den Leerlauf geändert (Sie wird von keiner Station verwendet).</span><span class="sxs-lookup"><span data-stu-id="56a65-119">The address has changed to idle (it is not in use by any stations).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56a65-120"><span id="LINEADDRESSSTATE_NUMCALLS"></span><span id="lineaddressstate_numcalls"></span>**lineaddressstate- \_ numrufe**</span><span class="sxs-lookup"><span data-stu-id="56a65-120"><span id="LINEADDRESSSTATE_NUMCALLS"></span><span id="lineaddressstate_numcalls"></span>**LINEADDRESSSTATE\_NUMCALLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="56a65-121">Die Anzahl der Aufrufe für die Adresse hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="56a65-121">The number of calls on the address has changed.</span></span> <span data-ttu-id="56a65-122">Dies ist das Ergebnis von Ereignissen, z. b. einem neuen eingehenden-Befehl, einem ausgehenden-Rückruf für die Adresse oder einem-Rückruf, der seinen Haltezeit ändert.</span><span class="sxs-lookup"><span data-stu-id="56a65-122">This is the result of events such as a new incoming call, an outgoing call on the address, or a call changing its hold status.</span></span> <span data-ttu-id="56a65-123">Dieses Flag deckt die Änderungen in allen Membern **dwnumactivecalls**, **dwnumonholdcalls** und **dwnumonholdcudingcalls** in der [**lineaddressstatus**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) -Struktur ab.</span><span class="sxs-lookup"><span data-stu-id="56a65-123">This flag covers changes in any of the members **dwNumActiveCalls**, **dwNumOnHoldCalls** and **dwNumOnHoldPendingCalls** in the [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) structure.</span></span> <span data-ttu-id="56a65-124">Die Anwendung sollte alle drei Member überprüfen, wenn Sie eine [**Zeile \_ addressstate**](line-addressstate.md) (numcalls) empfängt.</span><span class="sxs-lookup"><span data-stu-id="56a65-124">The application should check all three of these members when it receives a [**LINE\_ADDRESSSTATE**](line-addressstate.md) (numCalls) message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56a65-125"><span id="LINEADDRESSSTATE_OTHER"></span><span id="lineaddressstate_other"></span>**lineaddressstate \_ other**</span><span class="sxs-lookup"><span data-stu-id="56a65-125"><span id="LINEADDRESSSTATE_OTHER"></span><span id="lineaddressstate_other"></span>**LINEADDRESSSTATE\_OTHER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="56a65-126">Address-Status Elemente, die nicht den unten aufgeführten unterliegen, wurden geändert.</span><span class="sxs-lookup"><span data-stu-id="56a65-126">Address-status items other than those listed below have changed.</span></span> <span data-ttu-id="56a65-127">Die Anwendung sollte den aktuellen Adress Status überprüfen, um zu bestimmen, welche Elemente geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="56a65-127">The application should check the current address status to determine which items have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56a65-128"><span id="LINEADDRESSSTATE_TERMINALS"></span><span id="lineaddressstate_terminals"></span>**lineaddressstate- \_ Terminals**</span><span class="sxs-lookup"><span data-stu-id="56a65-128"><span id="LINEADDRESSSTATE_TERMINALS"></span><span id="lineaddressstate_terminals"></span>**LINEADDRESSSTATE\_TERMINALS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="56a65-129">Die Terminal Einstellungen für die Adresse wurden geändert.</span><span class="sxs-lookup"><span data-stu-id="56a65-129">The terminal settings for the address have changed.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="56a65-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="56a65-130">Remarks</span></span>

<span data-ttu-id="56a65-131">Keine Erweiterbarkeit.</span><span class="sxs-lookup"><span data-stu-id="56a65-131">No extensibility.</span></span> <span data-ttu-id="56a65-132">Alle 32 Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="56a65-132">All 32 bits are reserved.</span></span>

<span data-ttu-id="56a65-133">Eine Anwendung wird über Änderungen an diesen Status Elementen in der [**Zeile \_ addressstate**](line-addressstate.md) -Nachricht benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="56a65-133">An application is notified about changes to these status items in the [**LINE\_ADDRESSSTATE**](line-addressstate.md) message.</span></span> <span data-ttu-id="56a65-134">Die Gerätefunktionen der Adresse geben an, welche Adressen Zustandsänderungen für diese Adresse möglicherweise gemeldet werden können.</span><span class="sxs-lookup"><span data-stu-id="56a65-134">The address's device capabilities indicate which address state changes can possibly be reported for this address.</span></span>

## <a name="requirements"></a><span data-ttu-id="56a65-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56a65-135">Requirements</span></span>



| <span data-ttu-id="56a65-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="56a65-136">Requirement</span></span> | <span data-ttu-id="56a65-137">Wert</span><span class="sxs-lookup"><span data-stu-id="56a65-137">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="56a65-138">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="56a65-138">TAPI version</span></span><br/> | <span data-ttu-id="56a65-139">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="56a65-139">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="56a65-140">Header</span><span class="sxs-lookup"><span data-stu-id="56a65-140">Header</span></span><br/>       | <dl> <span data-ttu-id="56a65-141"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="56a65-141"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56a65-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56a65-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56a65-143">**Zeile \_ addressstate**</span><span class="sxs-lookup"><span data-stu-id="56a65-143">**LINE\_ADDRESSSTATE**</span></span>](line-addressstate.md)
</dt> <dt>

[<span data-ttu-id="56a65-144">**\_linienlinedevstate**</span><span class="sxs-lookup"><span data-stu-id="56a65-144">**LINE\_LINEDEVSTATE**</span></span>](line-linedevstate.md)
</dt> <dt>

[<span data-ttu-id="56a65-145">**Lineaddresscaps**</span><span class="sxs-lookup"><span data-stu-id="56a65-145">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="56a65-146">**Lineaddressstatus**</span><span class="sxs-lookup"><span data-stu-id="56a65-146">**LINEADDRESSSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[<span data-ttu-id="56a65-147">**linegetaddresscaps**</span><span class="sxs-lookup"><span data-stu-id="56a65-147">**lineGetAddressCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> </dl>

 

 




