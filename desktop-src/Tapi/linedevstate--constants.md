---
description: Die \_ Bits-Flag-Konstanten von linedevstate beschreiben verschiedene Zeilen Statusereignisse.
ms.assetid: 41e8a777-a57a-4d6c-850f-e21b58081b0d
title: LINEDEVSTATE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49717c1adb0f62a48a041f5920c0b82c7b817277
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354835"
---
# <a name="linedevstate_-constants"></a><span data-ttu-id="18b4b-103">Linedevstate- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="18b4b-103">LINEDEVSTATE\_ Constants</span></span>

<span data-ttu-id="18b4b-104">Die Bits-Flag-Konstanten von **linedevstate \_** beschreiben verschiedene Zeilen Statusereignisse.</span><span class="sxs-lookup"><span data-stu-id="18b4b-104">The **LINEDEVSTATE\_** bit-flag constants describe various line status events.</span></span>

<dl> <dt>

<span data-ttu-id="18b4b-105"><span id="LINEDEVSTATE_BATTERY"></span><span id="linedevstate_battery"></span>**linedevstate- \_ Akku**</span><span class="sxs-lookup"><span data-stu-id="18b4b-105"><span id="LINEDEVSTATE_BATTERY"></span><span id="linedevstate_battery"></span>**LINEDEVSTATE\_BATTERY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18b4b-106">Der Akku Pegel hat sich erheblich geändert (Mobilfunk).</span><span class="sxs-lookup"><span data-stu-id="18b4b-106">The battery level has changed significantly (cellular).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18b4b-107"><span id="LINEDEVSTATE_CAPSCHANGE"></span><span id="linedevstate_capschange"></span>**linedevstate \_ capschange**</span><span class="sxs-lookup"><span data-stu-id="18b4b-107"><span id="LINEDEVSTATE_CAPSCHANGE"></span><span id="linedevstate_capschange"></span>**LINEDEVSTATE\_CAPSCHANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18b4b-108">Gibt an, dass ein oder mehrere Member in der [**linedevcaps**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) -Struktur für die Adresse aufgrund von Konfigurationsänderungen, die vom Benutzer oder anderen Bedingungen vorgenommen wurden, geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="18b4b-108">Indicates that, due to configuration changes made by the user or other circumstances, one or more of the members in the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure for the address have changed.</span></span> <span data-ttu-id="18b4b-109">Die Anwendung sollte [**linegetdevcaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps) zum Lesen der aktualisierten Struktur verwenden.</span><span class="sxs-lookup"><span data-stu-id="18b4b-109">The application should use [**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps) to read the updated structure.</span></span> <span data-ttu-id="18b4b-110">Wenn ein Dienstanbieter eine [**Zeile \_ linedevstate**](line-linedevstate.md) -Nachricht mit diesem Wert an TAPI sendet, übergibt TAPI ihn an Anwendungen, die die TAPI-Version 1,4 oder höher ausgehandelt haben. Anwendungen, die eine vorherige TAPI-Version aushandeln, erhalten linedevstate- **Zeilen \_** Meldungen mit linedevstate \_ Reit, sodass diese die aktualisierten Informationen Herunterfahren und erneut initialisieren müssen.</span><span class="sxs-lookup"><span data-stu-id="18b4b-110">If a service provider sends a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous TAPI version will receive **LINE\_LINEDEVSTATE** messages specifying LINEDEVSTATE\_REINIT, requiring them to shut down and reinitialize their connection to TAPI to obtain the updated information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18b4b-111"><span id="LINEDEVSTATE_CLOSE"></span><span id="linedevstate_close"></span>**linedevstate \_ Schließen**</span><span class="sxs-lookup"><span data-stu-id="18b4b-111"><span id="LINEDEVSTATE_CLOSE"></span><span id="linedevstate_close"></span>**LINEDEVSTATE\_CLOSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18b4b-112">Die Zeile wurde von einer anderen Anwendung geschlossen.</span><span class="sxs-lookup"><span data-stu-id="18b4b-112">The line has been closed by another application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18b4b-113"><span id="LINEDEVSTATE_CONFIGCHANGE"></span><span id="linedevstate_configchange"></span>**linedevstate \_ configchange**</span><span class="sxs-lookup"><span data-stu-id="18b4b-113"><span id="LINEDEVSTATE_CONFIGCHANGE"></span><span id="linedevstate_configchange"></span>**LINEDEVSTATE\_CONFIGCHANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18b4b-114">Gibt an, dass Konfigurationsänderungen an einem oder mehreren Mediengeräten vorgenommen wurden, die mit dem liniengerät verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="18b4b-114">Indicates that configuration changes have been made to one or more of the media devices associated with the line device.</span></span> <span data-ttu-id="18b4b-115">Die Anwendung kann, wenn Sie sich wünscht, [**linegetdevconfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) verwenden, um die aktualisierten Informationen zu lesen.</span><span class="sxs-lookup"><span data-stu-id="18b4b-115">The application, if it desires, can use [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) to read the updated information.</span></span> <span data-ttu-id="18b4b-116">Wenn ein Dienstanbieter eine [**Zeile \_ linedevstate**](line-linedevstate.md) -Nachricht mit diesem Wert an TAPI sendet, übergibt TAPI ihn an Anwendungen, die TAPI-Version 1,4 oder höher ausgehandelt haben. Anwendungen, die eine frühere API-Version aushandeln, erhalten keine Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="18b4b-116">If a service provider sends a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous API version will not receive any notification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18b4b-117"><span id="LINEDEVSTATE_COMPLCANCEL"></span><span id="linedevstate_complcancel"></span>**linedevstate \_ complcancel**</span><span class="sxs-lookup"><span data-stu-id="18b4b-117"><span id="LINEDEVSTATE_COMPLCANCEL"></span><span id="linedevstate_complcancel"></span>**LINEDEVSTATE\_COMPLCANCEL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18b4b-118">Gibt an, dass der von der Vervollständigungs-ID, der im *dwParam2* -Parameter der [**line \_ linedevstate**](line-linedevstate.md) -Nachricht enthaltene Abschluss Bezeichner identifiziert wurde, extern abgebrochen wurde und nicht mehr als gültig angesehen wird (wenn der Wert in einem nachfolgenden Ausdruck von [**lineuncompletecallübergeben**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall)werden soll, schlägt die Funktion mit lineerr \_ invalcompletionid fehl).</span><span class="sxs-lookup"><span data-stu-id="18b4b-118">Indicates that the call completion identified by the completion identifier contained in the *dwParam2* parameter of the [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message has been externally canceled and is no longer considered valid (if that value were to be passed in a subsequent call to [**lineUncompleteCall**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall), the function would fail with LINEERR\_INVALCOMPLETIONID).</span></span> <span data-ttu-id="18b4b-119">Wenn ein Dienstanbieter eine [**Zeile \_ linedevstate**](line-linedevstate.md) -Nachricht mit diesem Wert an TAPI sendet, übergibt TAPI ihn an Anwendungen, die TAPI-Version 1,4 oder höher ausgehandelt haben. Anwendungen, die eine frühere API-Version aushandeln, erhalten keine Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="18b4b-119">If a service provider sends a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous API version will not receive any notification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18b4b-120"><span id="LINEDEVSTATE_CONNECTED"></span><span id="linedevstate_connected"></span>**linedevstate \_ verbunden**</span><span class="sxs-lookup"><span data-stu-id="18b4b-120"><span id="LINEDEVSTATE_CONNECTED"></span><span id="linedevstate_connected"></span>**LINEDEVSTATE\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18b4b-121">Die Zeile wurde zuvor getrennt und ist jetzt mit TAPI verbunden.</span><span class="sxs-lookup"><span data-stu-id="18b4b-121">The line was previously disconnected and is now connected to TAPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18b4b-122"><span id="LINEDEVSTATE_DEVSPECIFIC"></span><span id="linedevstate_devspecific"></span>**linedevstate \_ DevSpecific**</span><span class="sxs-lookup"><span data-stu-id="18b4b-122"><span id="LINEDEVSTATE_DEVSPECIFIC"></span><span id="linedevstate_devspecific"></span>**LINEDEVSTATE\_DEVSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18b4b-123">Die gerätespezifischen Informationen der Zeile wurden geändert.</span><span class="sxs-lookup"><span data-stu-id="18b4b-123">The line's device-specific information has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18b4b-124"><span id="LINEDEVSTATE_DISCONNECTED"></span><span id="linedevstate_disconnected"></span>**linedevstate \_ getrennt**</span><span class="sxs-lookup"><span data-stu-id="18b4b-124"><span id="LINEDEVSTATE_DISCONNECTED"></span><span id="linedevstate_disconnected"></span>**LINEDEVSTATE\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18b4b-125">Diese Zeile war bereits verbunden und ist nun von TAPI getrennt.</span><span class="sxs-lookup"><span data-stu-id="18b4b-125">This line was previously connected and is now disconnected from TAPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18b4b-126"><span id="LINEDEVSTATE_INSERVICE"></span><span id="linedevstate_inservice"></span>**linedevstate- \_ INService**</span><span class="sxs-lookup"><span data-stu-id="18b4b-126"><span id="LINEDEVSTATE_INSERVICE"></span><span id="linedevstate_inservice"></span>**LINEDEVSTATE\_INSERVICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18b4b-127">Die Linie ist mit TAPI verbunden.</span><span class="sxs-lookup"><span data-stu-id="18b4b-127">The line is connected to TAPI.</span></span> <span data-ttu-id="18b4b-128">Dies ist der Fall, wenn TAPI zum ersten Mal aktiviert wird, oder wenn die Linienverbindung physisch an den Switch angeschlossen ist und sich im Dienst befindet, während TAPI aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="18b4b-128">This happens when TAPI is first activated or when the line wire is physically plugged in and in-service at the switch while TAPI is active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18b4b-129"><span id="LINEDEVSTATE_LOCK"></span><span id="linedevstate_lock"></span>**linedevstate- \_ Sperre**</span><span class="sxs-lookup"><span data-stu-id="18b4b-129"><span id="LINEDEVSTATE_LOCK"></span><span id="linedevstate_lock"></span>**LINEDEVSTATE\_LOCK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18b4b-130">Der gesperrte Status des Linien Geräts hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="18b4b-130">The locked status of the line device has changed.</span></span> <span data-ttu-id="18b4b-131">(Weitere Informationen finden Sie unter linedevstatus Flags \_ In [**linedevstatus-Flags- \_ Konstanten**](linedevstatusflags--constants.md)gesperrt.)</span><span class="sxs-lookup"><span data-stu-id="18b4b-131">(For more information, see LINEDEVSTATUSFLAGS\_LOCKED in [**LINEDEVSTATUSFLAGS\_ Constants**](linedevstatusflags--constants.md).)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18b4b-132"><span id="LINEDEVSTATE_MAINTENANCE"></span><span id="linedevstate_maintenance"></span>**linedevstate- \_ Wartung**</span><span class="sxs-lookup"><span data-stu-id="18b4b-132"><span id="LINEDEVSTATE_MAINTENANCE"></span><span id="linedevstate_maintenance"></span>**LINEDEVSTATE\_MAINTENANCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18b4b-133">Die Wartung erfolgt in der Zeile am Switch.</span><span class="sxs-lookup"><span data-stu-id="18b4b-133">Maintenance is being performed on the line at the switch.</span></span> <span data-ttu-id="18b4b-134">TAPI kann nicht verwendet werden, um auf dem liniengerät zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="18b4b-134">TAPI cannot be used to operate on the line device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18b4b-135"><span id="LINEDEVSTATE_MSGWAITOFF"></span><span id="linedevstate_msgwaitoff"></span>**linedevstate \_ msgwaideff**</span><span class="sxs-lookup"><span data-stu-id="18b4b-135"><span id="LINEDEVSTATE_MSGWAITOFF"></span><span id="linedevstate_msgwaitoff"></span>**LINEDEVSTATE\_MSGWAITOFF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18b4b-136">Der Meldungs Warnungs Indikator ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="18b4b-136">The message waiting indicator is turned off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18b4b-137"><span id="LINEDEVSTATE_MSGWAITON"></span><span id="linedevstate_msgwaiton"></span>**linedevstate \_ msgwaiton**</span><span class="sxs-lookup"><span data-stu-id="18b4b-137"><span id="LINEDEVSTATE_MSGWAITON"></span><span id="linedevstate_msgwaiton"></span>**LINEDEVSTATE\_MSGWAITON**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18b4b-138">Der Indikator für die Nachrichten Warteschlange ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="18b4b-138">The message waiting indicator is turned on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18b4b-139"><span id="LINEDEVSTATE_NUMCALLS"></span><span id="linedevstate_numcalls"></span>**linedevstate- \_ numrufe**</span><span class="sxs-lookup"><span data-stu-id="18b4b-139"><span id="LINEDEVSTATE_NUMCALLS"></span><span id="linedevstate_numcalls"></span>**LINEDEVSTATE\_NUMCALLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18b4b-140">Die Anzahl der Aufrufe auf dem liniengerät hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="18b4b-140">The number of calls on the line device has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18b4b-141"><span id="LINEDEVSTATE_NUMCOMPLETIONS"></span><span id="linedevstate_numcompletions"></span>**linedevstate- \_ numcompletions**</span><span class="sxs-lookup"><span data-stu-id="18b4b-141"><span id="LINEDEVSTATE_NUMCOMPLETIONS"></span><span id="linedevstate_numcompletions"></span>**LINEDEVSTATE\_NUMCOMPLETIONS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18b4b-142">Die Anzahl der ausstehenden Aufrufe zum Abschluss des Geräts hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="18b4b-142">The number of outstanding call completions on the line device has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18b4b-143"><span id="LINEDEVSTATE_OPEN"></span><span id="linedevstate_open"></span>**linedevstate \_ geöffnet**</span><span class="sxs-lookup"><span data-stu-id="18b4b-143"><span id="LINEDEVSTATE_OPEN"></span><span id="linedevstate_open"></span>**LINEDEVSTATE\_OPEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18b4b-144">Die Zeile wurde von einer anderen Anwendung geöffnet.</span><span class="sxs-lookup"><span data-stu-id="18b4b-144">The line has been opened by another application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18b4b-145"><span id="LINEDEVSTATE_OTHER"></span><span id="linedevstate_other"></span>**anderer linedevstate \_**</span><span class="sxs-lookup"><span data-stu-id="18b4b-145"><span id="LINEDEVSTATE_OTHER"></span><span id="linedevstate_other"></span>**LINEDEVSTATE\_OTHER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18b4b-146">Andere Gerätestatus Elemente als die unten aufgeführten wurden geändert.</span><span class="sxs-lookup"><span data-stu-id="18b4b-146">Device-status items other than those listed below have changed.</span></span> <span data-ttu-id="18b4b-147">Die Anwendung sollte den aktuellen Gerätestatus überprüfen, um zu bestimmen, welche Elemente geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="18b4b-147">The application should check the current device status to determine which items have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18b4b-148"><span id="LINEDEVSTATE_OUTOFSERVICE"></span><span id="linedevstate_outofservice"></span>**"linedevstate" ( \_ outo fservice)**</span><span class="sxs-lookup"><span data-stu-id="18b4b-148"><span id="LINEDEVSTATE_OUTOFSERVICE"></span><span id="linedevstate_outofservice"></span>**LINEDEVSTATE\_OUTOFSERVICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18b4b-149">Die Zeile ist nicht mehr auf dem Switch oder physisch getrennt.</span><span class="sxs-lookup"><span data-stu-id="18b4b-149">The line is out of service at the switch or physically disconnected.</span></span> <span data-ttu-id="18b4b-150">TAPI kann nicht verwendet werden, um auf dem liniengerät zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="18b4b-150">TAPI cannot be used to operate on the line device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18b4b-151"><span id="LINEDEVSTATE_REINIT"></span><span id="linedevstate_reinit"></span>**linedevstate \_ Reit**</span><span class="sxs-lookup"><span data-stu-id="18b4b-151"><span id="LINEDEVSTATE_REINIT"></span><span id="linedevstate_reinit"></span>**LINEDEVSTATE\_REINIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18b4b-152">Elemente wurden in der Konfiguration von Linien Geräten geändert.</span><span class="sxs-lookup"><span data-stu-id="18b4b-152">Items have changed in the configuration of line devices.</span></span> <span data-ttu-id="18b4b-153">Um diese Änderungen zu beachten (wie bei der Darstellung von neuen Zeilen Geräten), sollte die Anwendung die Verwendung von TAPI erneut initialisieren.</span><span class="sxs-lookup"><span data-stu-id="18b4b-153">To become aware of these changes (as for the appearance of new line devices) the application should reinitialize its use of TAPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18b4b-154"><span id="LINEDEVSTATE_REMOVED"></span><span id="linedevstate_removed"></span>**linedevstate \_ entfernt**</span><span class="sxs-lookup"><span data-stu-id="18b4b-154"><span id="LINEDEVSTATE_REMOVED"></span><span id="linedevstate_removed"></span>**LINEDEVSTATE\_REMOVED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18b4b-155">Gibt an, dass das Gerät vom Dienstanbieter aus dem System entfernt wird (wahrscheinlich über eine Benutzeraktion, über eine Systemsteuerung oder ein ähnliches Hilfsprogramm).</span><span class="sxs-lookup"><span data-stu-id="18b4b-155">Indicates that the device is being removed from the system by the service provider (most likely through user action, through a control panel or similar utility).</span></span> <span data-ttu-id="18b4b-156">An [**eine \_ linienlinedevstate**](line-linedevstate.md) -Nachricht mit diesem Wert folgt normalerweise direkt eine Meldung zum [**\_ Schließen**](line-close.md) des Geräts auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="18b4b-156">A [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message with this value will normally be immediately followed by a [**LINE\_CLOSE**](line-close.md) message on the device.</span></span> <span data-ttu-id="18b4b-157">Nachfolgende Zugriffsversuche auf das Gerät vor der erneuten Initialisierung von TAPI führen dazu, dass lineerr \_ nodevice an die Anwendung zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="18b4b-157">Subsequent attempts to access the device prior to TAPI being reinitialized will result in LINEERR\_NODEVICE being returned to the application.</span></span> <span data-ttu-id="18b4b-158">Wenn ein Dienstanbieter eine [**Zeile \_ linedevstate**](line-linedevstate.md) -Nachricht mit diesem Wert an TAPI sendet, übergibt TAPI ihn an Anwendungen, die TAPI-Version 1,4 oder höher ausgehandelt haben. Anwendungen, die eine frühere API-Version aushandeln, erhalten keine Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="18b4b-158">If a service provider sends a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous API version will not receive any notification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18b4b-159"><span id="LINEDEVSTATE_RINGING"></span><span id="linedevstate_ringing"></span>**linedevstate- \_ Klingeln**</span><span class="sxs-lookup"><span data-stu-id="18b4b-159"><span id="LINEDEVSTATE_RINGING"></span><span id="linedevstate_ringing"></span>**LINEDEVSTATE\_RINGING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18b4b-160">Der-Schalter weist die Zeile an, den Benutzer zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="18b4b-160">The switch tells the line to alert the user.</span></span>

<span data-ttu-id="18b4b-161">**TAPI:** Dienstanbieter Benachrichtigen Anwendungen in jedem Ring, indem Sie wiederholt [**Zeilen- \_ linedevstate**](line-linedevstate.md) -Nachrichten senden, die diese Konstante enthalten.</span><span class="sxs-lookup"><span data-stu-id="18b4b-161">**TAPI:** Service providers notify applications on each ring cycle by repeatedly sending [**LINE\_LINEDEVSTATE**](line-linedevstate.md) messages containing this constant.</span></span> <span data-ttu-id="18b4b-162">Im USA senden Dienstanbieter beispielsweise alle sechs Sekunden eine Nachricht mit dieser Konstante.</span><span class="sxs-lookup"><span data-stu-id="18b4b-162">For example, in the United States, service providers send a message with this constant every six seconds.</span></span>

<span data-ttu-id="18b4b-163">**TSPI:** Auf einem Pots-Gerät kann der Dienstanbieter die Nachricht senden, wenn die zentral Niederlassung eine Ring Spannung sendet.</span><span class="sxs-lookup"><span data-stu-id="18b4b-163">**TSPI:** On a POTS device, the service provider can send the message whenever the central office sends ring voltage.</span></span> <span data-ttu-id="18b4b-164">Auf digitalen Geräten wie z. b. ISDN muss der Dienstanbieter die Wiederholung der Nachricht möglicherweise synthetisieren, wenn der Switch nur eine Ring Anforderung generiert.</span><span class="sxs-lookup"><span data-stu-id="18b4b-164">On digital devices such as ISDN, the service provider may need to synthesize the repetition of the message if the switch generates only one ring request.</span></span> <span data-ttu-id="18b4b-165">Jede Wiederholung der Nachricht sollte die Ring Anzahl erhöhen, sodass die Maut Speicherfunktionen ordnungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="18b4b-165">Each repetition of the message should show the ring count increasing, so that toll save functions work properly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18b4b-166"><span id="LINEDEVSTATE_ROAMMODE"></span><span id="linedevstate_roammode"></span>**linedevstate ( \_ roammode)**</span><span class="sxs-lookup"><span data-stu-id="18b4b-166"><span id="LINEDEVSTATE_ROAMMODE"></span><span id="linedevstate_roammode"></span>**LINEDEVSTATE\_ROAMMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18b4b-167">Der Modus "Roaming" des Linien Geräts hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="18b4b-167">The roam mode of the line device has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18b4b-168"><span id="LINEDEVSTATE_SIGNAL"></span><span id="linedevstate_signal"></span>**linedevstate- \_ Signal**</span><span class="sxs-lookup"><span data-stu-id="18b4b-168"><span id="LINEDEVSTATE_SIGNAL"></span><span id="linedevstate_signal"></span>**LINEDEVSTATE\_SIGNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18b4b-169">Die Signalebene hat sich erheblich geändert (Mobilfunk).</span><span class="sxs-lookup"><span data-stu-id="18b4b-169">The signal level has changed significantly (cellular).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18b4b-170"><span id="LINEDEVSTATE_TERMINALS"></span><span id="linedevstate_terminals"></span>**linedevstate- \_ Terminals**</span><span class="sxs-lookup"><span data-stu-id="18b4b-170"><span id="LINEDEVSTATE_TERMINALS"></span><span id="linedevstate_terminals"></span>**LINEDEVSTATE\_TERMINALS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18b4b-171">Die Terminal Einstellungen wurden geändert.</span><span class="sxs-lookup"><span data-stu-id="18b4b-171">The terminal settings have changed.</span></span> <span data-ttu-id="18b4b-172">Dies kann z. b. der Fall sein, wenn in mehreren Zeilen Geräten Terminals gemeinsam genutzt werden (z. b. zwei Zeilen, die ein Telefon Terminal gemeinsam verwenden).</span><span class="sxs-lookup"><span data-stu-id="18b4b-172">This can happen, for example, if multiple line devices share terminals among them (for example, two lines sharing a phone terminal).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18b4b-173"><span id="LINEDEVSTATE_TRANSLATECHANGE"></span><span id="linedevstate_translatechange"></span>**linedevstate \_ translatechange**</span><span class="sxs-lookup"><span data-stu-id="18b4b-173"><span id="LINEDEVSTATE_TRANSLATECHANGE"></span><span id="linedevstate_translatechange"></span>**LINEDEVSTATE\_TRANSLATECHANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18b4b-174">Gibt an, dass ein oder mehrere Member in der [**linetranslatecaps**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) -Struktur aufgrund von Konfigurationsänderungen, die vom Benutzer oder anderen Bedingungen vorgenommen wurden, geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="18b4b-174">Indicates that, due to configuration changes made by the user or other circumstances, one or more of the members in the [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) structure have changed.</span></span> <span data-ttu-id="18b4b-175">Die Anwendung sollte [**linegettranslatecaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps) zum Lesen der aktualisierten Struktur verwenden.</span><span class="sxs-lookup"><span data-stu-id="18b4b-175">The application should use [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps) to read the updated structure.</span></span> <span data-ttu-id="18b4b-176">Wenn ein Dienstanbieter eine [**Zeile \_ linedevstate**](line-linedevstate.md) -Nachricht mit diesem Wert an TAPI sendet, übergibt TAPI ihn an Anwendungen, die die TAPI-Version 1,4 oder höher ausgehandelt haben. Anwendungen, die eine vorherige TAPI-Version aushandeln, erhalten linedevstate- **Zeilen \_** Meldungen mit linedevstate \_ Reit, sodass diese die aktualisierten Informationen Herunterfahren und erneut initialisieren müssen.</span><span class="sxs-lookup"><span data-stu-id="18b4b-176">If a service provider sends a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous TAPI version will receive **LINE\_LINEDEVSTATE** messages specifying LINEDEVSTATE\_REINIT, requiring them to shut down and reinitialize their connection to TAPI to obtain the updated information.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="18b4b-177">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="18b4b-177">Remarks</span></span>

<span data-ttu-id="18b4b-178">Keine Erweiterbarkeit.</span><span class="sxs-lookup"><span data-stu-id="18b4b-178">No extensibility.</span></span> <span data-ttu-id="18b4b-179">Alle 32 Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="18b4b-179">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="18b4b-180">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="18b4b-180">Requirements</span></span>



| <span data-ttu-id="18b4b-181">Anforderung</span><span class="sxs-lookup"><span data-stu-id="18b4b-181">Requirement</span></span> | <span data-ttu-id="18b4b-182">Wert</span><span class="sxs-lookup"><span data-stu-id="18b4b-182">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="18b4b-183">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="18b4b-183">TAPI version</span></span><br/> | <span data-ttu-id="18b4b-184">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="18b4b-184">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="18b4b-185">Header</span><span class="sxs-lookup"><span data-stu-id="18b4b-185">Header</span></span><br/>       | <dl> <span data-ttu-id="18b4b-186"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="18b4b-186"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18b4b-187">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18b4b-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18b4b-188">**Zeilen \_ Schließen**</span><span class="sxs-lookup"><span data-stu-id="18b4b-188">**LINE\_CLOSE**</span></span>](line-close.md)
</dt> <dt>

[<span data-ttu-id="18b4b-189">**\_linienlinedevstate**</span><span class="sxs-lookup"><span data-stu-id="18b4b-189">**LINE\_LINEDEVSTATE**</span></span>](line-linedevstate.md)
</dt> <dt>

[<span data-ttu-id="18b4b-190">**Linedevcaps**</span><span class="sxs-lookup"><span data-stu-id="18b4b-190">**LINEDEVCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)
</dt> <dt>

[<span data-ttu-id="18b4b-191">**linegetdevcaps**</span><span class="sxs-lookup"><span data-stu-id="18b4b-191">**lineGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)
</dt> <dt>

[<span data-ttu-id="18b4b-192">**linegetdevconfig**</span><span class="sxs-lookup"><span data-stu-id="18b4b-192">**lineGetDevConfig**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)
</dt> <dt>

[<span data-ttu-id="18b4b-193">**linegettranslatecaps**</span><span class="sxs-lookup"><span data-stu-id="18b4b-193">**lineGetTranslateCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)
</dt> <dt>

[<span data-ttu-id="18b4b-194">**Linetranslatecaps**</span><span class="sxs-lookup"><span data-stu-id="18b4b-194">**LINETRANSLATECAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps)
</dt> <dt>

[<span data-ttu-id="18b4b-195">**lineuncompletecall**</span><span class="sxs-lookup"><span data-stu-id="18b4b-195">**lineUncompleteCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall)
</dt> </dl>

 

 




