---
description: Die \_ Bit-Flag-Konstanten von phonestate beschreiben verschiedene Status Elemente für ein Telefongerät.
ms.assetid: 5db53dd4-606a-40b9-9159-b67a0ea1e400
title: PHONESTATE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6346251f6947aebb2a5941389843e2abcec77c4a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370611"
---
# <a name="phonestate_-constants"></a><span data-ttu-id="fb640-103">Phonestate- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="fb640-103">PHONESTATE\_ Constants</span></span>

<span data-ttu-id="fb640-104">Die Bit-Flag-Konstanten von **phonestate \_** beschreiben verschiedene Status Elemente für ein Telefongerät.</span><span class="sxs-lookup"><span data-stu-id="fb640-104">The **PHONESTATE\_** bit-flag constants describe various status items for a phone device.</span></span>

<dl> <dt>

<span data-ttu-id="fb640-105"><span id="PHONESTATE_CAPSCHANGE"></span><span id="phonestate_capschange"></span>**"phonestate \_ capschange"**</span><span class="sxs-lookup"><span data-stu-id="fb640-105"><span id="PHONESTATE_CAPSCHANGE"></span><span id="phonestate_capschange"></span>**PHONESTATE\_CAPSCHANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb640-106">Gibt an, dass ein oder mehrere Member in der [**phonecaps**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) -Struktur aufgrund von Konfigurationsänderungen, die vom Benutzer oder anderen Bedingungen vorgenommen wurden, geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="fb640-106">Indicates that, due to configuration changes made by the user or other circumstances, one or more of the members in the [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) structure have changed.</span></span> <span data-ttu-id="fb640-107">Die Anwendung sollte [**phonegetdevcaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) verwenden, um die aktualisierte Struktur zu lesen.</span><span class="sxs-lookup"><span data-stu-id="fb640-107">The application should use [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) to read the updated structure.</span></span> <span data-ttu-id="fb640-108">Wenn ein Dienstanbieter eine [**Telefon \_ Zustands**](phone-state.md) Meldung mit diesem Wert an TAPI sendet, übergibt TAPI ihn an Anwendungen, die die TAPI-Version 1,4 oder höher ausgehandelt haben. Anwendungen, die eine vorherige API-Version aushandeln, erhalten Telefon \_ Zustands Meldungen, die das phonestate \_ REIT-Gerät zum Abrufen der aktualisierten Informationen benötigen.</span><span class="sxs-lookup"><span data-stu-id="fb640-108">If a service provider sends a [**PHONE\_STATE**](phone-state.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous API version will receive PHONE\_STATE messages specifying PHONESTATE\_REINIT, requiring them to shut down and reinitialize their connection to TAPI to obtain the updated information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb640-109"><span id="PHONESTATE_CONNECTED"></span><span id="phonestate_connected"></span>**phonestate \_ verbunden**</span><span class="sxs-lookup"><span data-stu-id="fb640-109"><span id="PHONESTATE_CONNECTED"></span><span id="phonestate_connected"></span>**PHONESTATE\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb640-110">Die Verbindung zwischen dem Telefongerät und TAPI wurde soeben hergestellt.</span><span class="sxs-lookup"><span data-stu-id="fb640-110">The connection between the phone device and TAPI was just made.</span></span> <span data-ttu-id="fb640-111">Dies ist der Fall, wenn TAPI zum ersten Mal aufgerufen wird oder wenn die Verbindung des Telefons mit dem PC mit TAPI Active angeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="fb640-111">This happens when TAPI is first invoked or when the wire connecting the phone to the PC is plugged in with TAPI active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb640-112"><span id="PHONESTATE_DEVSPECIFIC"></span><span id="phonestate_devspecific"></span>**phonestate \_ DevSpecific**</span><span class="sxs-lookup"><span data-stu-id="fb640-112"><span id="PHONESTATE_DEVSPECIFIC"></span><span id="phonestate_devspecific"></span>**PHONESTATE\_DEVSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb640-113">Die gerätespezifischen Informationen des Telefons wurden geändert.</span><span class="sxs-lookup"><span data-stu-id="fb640-113">The phone's device-specific information has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb640-114"><span id="PHONESTATE_DISCONNECTED"></span><span id="phonestate_disconnected"></span>**phonestate \_ getrennt**</span><span class="sxs-lookup"><span data-stu-id="fb640-114"><span id="PHONESTATE_DISCONNECTED"></span><span id="phonestate_disconnected"></span>**PHONESTATE\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb640-115">Die Verbindung zwischen dem Telefongerät und TAPI war einfach beschädigt.</span><span class="sxs-lookup"><span data-stu-id="fb640-115">The connection between the phone device and TAPI was just broken.</span></span> <span data-ttu-id="fb640-116">Dies ist der Fall, wenn die Verbindung, die das Telefon mit dem PC verbindet, getrennt ist, während TAPI aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="fb640-116">This happens when the wire connecting the phone set to the PC is unplugged while TAPI is active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb640-117"><span id="PHONESTATE_DISPLAY"></span><span id="phonestate_display"></span>**phonestate- \_ Anzeige**</span><span class="sxs-lookup"><span data-stu-id="fb640-117"><span id="PHONESTATE_DISPLAY"></span><span id="phonestate_display"></span>**PHONESTATE\_DISPLAY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb640-118">Die Anzeige des Telefons hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="fb640-118">The display of the phone has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb640-119"><span id="PHONESTATE_HANDSETGAIN"></span><span id="phonestate_handsetgain"></span>**phonestate \_ handsetgewinn**</span><span class="sxs-lookup"><span data-stu-id="fb640-119"><span id="PHONESTATE_HANDSETGAIN"></span><span id="phonestate_handsetgain"></span>**PHONESTATE\_HANDSETGAIN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb640-120">Die Mikrofon Gewinn Einstellung des Mobiltelefons hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="fb640-120">The handset's microphone gain setting has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb640-121"><span id="PHONESTATE_HANDSETHOOKSWITCH"></span><span id="phonestate_handsethookswitch"></span>**phonestate \_ handlthookswitch**</span><span class="sxs-lookup"><span data-stu-id="fb640-121"><span id="PHONESTATE_HANDSETHOOKSWITCH"></span><span id="phonestate_handsethookswitch"></span>**PHONESTATE\_HANDSETHOOKSWITCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb640-122">Der Status des "geokswitch" des Mobiltelefons wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="fb640-122">The handset hookswitch state has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb640-123"><span id="PHONESTATE_HANDSETVOLUME"></span><span id="phonestate_handsetvolume"></span>**phonestate \_ handsetvolume**</span><span class="sxs-lookup"><span data-stu-id="fb640-123"><span id="PHONESTATE_HANDSETVOLUME"></span><span id="phonestate_handsetvolume"></span>**PHONESTATE\_HANDSETVOLUME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb640-124">Die Lautstärke Einstellung des Handlers wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="fb640-124">The handset's speaker volume setting has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb640-125"><span id="PHONESTATE_HEADSETHOOKSWITCH"></span><span id="phonestate_headsethookswitch"></span>**phonestate \_ headsinthookswitch**</span><span class="sxs-lookup"><span data-stu-id="fb640-125"><span id="PHONESTATE_HEADSETHOOKSWITCH"></span><span id="phonestate_headsethookswitch"></span>**PHONESTATE\_HEADSETHOOKSWITCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb640-126">Der Status des "huokswitch" wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="fb640-126">The headset's hookswitch state has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb640-127"><span id="PHONESTATE_HEADSETGAIN"></span><span id="phonestate_headsetgain"></span>**phonestate \_ headsetgewinn**</span><span class="sxs-lookup"><span data-stu-id="fb640-127"><span id="PHONESTATE_HEADSETGAIN"></span><span id="phonestate_headsetgain"></span>**PHONESTATE\_HEADSETGAIN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb640-128">Die Mikrofon Gewinn Einstellung des Headsets hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="fb640-128">The headset's microphone gain setting has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb640-129"><span id="PHONESTATE_HEADSETVOLUME"></span><span id="phonestate_headsetvolume"></span>**phonestate \_ headsetvolume**</span><span class="sxs-lookup"><span data-stu-id="fb640-129"><span id="PHONESTATE_HEADSETVOLUME"></span><span id="phonestate_headsetvolume"></span>**PHONESTATE\_HEADSETVOLUME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb640-130">Die Lautstärke der Lautstärke für das Headset hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="fb640-130">The headset's speaker volume setting has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb640-131"><span id="PHONESTATE_LAMP"></span><span id="phonestate_lamp"></span>**phonestate- \_ Lamp**</span><span class="sxs-lookup"><span data-stu-id="fb640-131"><span id="PHONESTATE_LAMP"></span><span id="phonestate_lamp"></span>**PHONESTATE\_LAMP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb640-132">Eine Glühbirne des Telefons hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="fb640-132">A lamp of the phone has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb640-133"><span id="PHONESTATE_MONITORS"></span><span id="phonestate_monitors"></span>**phonestate- \_ Monitore**</span><span class="sxs-lookup"><span data-stu-id="fb640-133"><span id="PHONESTATE_MONITORS"></span><span id="phonestate_monitors"></span>**PHONESTATE\_MONITORS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb640-134">Die Anzahl der Monitore für das Telefongerät.</span><span class="sxs-lookup"><span data-stu-id="fb640-134">The number of monitors for the phone device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb640-135"><span id="PHONESTATE_OTHER"></span><span id="phonestate_other"></span>**Sonstige phonestate \_**</span><span class="sxs-lookup"><span data-stu-id="fb640-135"><span id="PHONESTATE_OTHER"></span><span id="phonestate_other"></span>**PHONESTATE\_OTHER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb640-136">Andere Telefonstatus Elemente als die unten aufgeführten haben sich geändert.</span><span class="sxs-lookup"><span data-stu-id="fb640-136">Phone-status items other than those listed below have changed.</span></span> <span data-ttu-id="fb640-137">Die Anwendung sollte den aktuellen Telefonstatus überprüfen, um zu bestimmen, welche Elemente geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="fb640-137">The application should check the current phone status to determine which items have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb640-138"><span id="PHONESTATE_OWNER"></span><span id="phonestate_owner"></span>**phonestate- \_ Besitzer**</span><span class="sxs-lookup"><span data-stu-id="fb640-138"><span id="PHONESTATE_OWNER"></span><span id="phonestate_owner"></span>**PHONESTATE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb640-139">Die Anzahl von Besitzern für das Telefongerät.</span><span class="sxs-lookup"><span data-stu-id="fb640-139">The number of owners for the phone device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb640-140"><span id="PHONESTATE_REINIT"></span><span id="phonestate_reinit"></span>**phonestate \_ Reit**</span><span class="sxs-lookup"><span data-stu-id="fb640-140"><span id="PHONESTATE_REINIT"></span><span id="phonestate_reinit"></span>**PHONESTATE\_REINIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb640-141">Elemente wurden in der Konfiguration von Telefongeräten geändert.</span><span class="sxs-lookup"><span data-stu-id="fb640-141">Items have changed in the configuration of phone devices.</span></span> <span data-ttu-id="fb640-142">Um diese Änderungen zu erkennen (wie bei der Darstellung neuer Telefongeräte), sollte die Anwendung die Verwendung von TAPI erneut initialisieren.</span><span class="sxs-lookup"><span data-stu-id="fb640-142">To become aware of these changes (as for the appearance of new phone devices), the application should reinitialize its use of TAPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb640-143"><span id="PHONESTATE_REMOVED"></span><span id="phonestate_removed"></span>**phonestate \_ entfernt**</span><span class="sxs-lookup"><span data-stu-id="fb640-143"><span id="PHONESTATE_REMOVED"></span><span id="phonestate_removed"></span>**PHONESTATE\_REMOVED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb640-144">Gibt an, dass das Gerät vom Dienstanbieter aus dem System entfernt wird (wahrscheinlich über eine Benutzeraktion, über eine Systemsteuerung oder ein ähnliches Hilfsprogramm).</span><span class="sxs-lookup"><span data-stu-id="fb640-144">Indicates that the device is being removed from the system by the service provider (most likely through user action, through a control panel or similar utility).</span></span> <span data-ttu-id="fb640-145">Auf eine [**Telefon \_ Zustands**](phone-state.md) Meldung mit diesem Wert folgt normalerweise direkt eine Meldung zum [**\_ Schließen des Telefons**](phone-close.md) auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="fb640-145">A [**PHONE\_STATE**](phone-state.md) message with this value will normally be immediately followed by a [**PHONE\_CLOSE**](phone-close.md) message on the device.</span></span> <span data-ttu-id="fb640-146">Nachfolgende Zugriffsversuche auf das Gerät vor der erneuten Initialisierung von TAPI führen dazu, dass "phoneerr \_ nodevice" an die Anwendung zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fb640-146">Subsequent attempts to access the device prior to TAPI being reinitialized will result in PHONEERR\_NODEVICE being returned to the application.</span></span> <span data-ttu-id="fb640-147">Wenn ein Dienstanbieter eine Telefon \_ Zustands Meldung mit diesem Wert an TAPI sendet, übergibt TAPI ihn an Anwendungen, die die TAPI-Version 1,4 oder höher ausgehandelt haben. Anwendungen, die eine frühere API-Version aushandeln, erhalten keine Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="fb640-147">If a service provider sends a PHONE\_STATE message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous API version will not receive any notification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb640-148"><span id="PHONESTATE_RESUME"></span><span id="phonestate_resume"></span>**phonestate \_ Resume**</span><span class="sxs-lookup"><span data-stu-id="fb640-148"><span id="PHONESTATE_RESUME"></span><span id="phonestate_resume"></span>**PHONESTATE\_RESUME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb640-149">Die Anwendungs Verwendung des Telefon Geräts wird fortgesetzt, nachdem es seit einiger Zeit angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="fb640-149">The application's use of the phone device is resumed after having been suspended for some time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb640-150"><span id="PHONESTATE_RINGMODE"></span><span id="phonestate_ringmode"></span>**phonestate- \_ ringmodus**</span><span class="sxs-lookup"><span data-stu-id="fb640-150"><span id="PHONESTATE_RINGMODE"></span><span id="phonestate_ringmode"></span>**PHONESTATE\_RINGMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb640-151">Der Klingel Modus des Telefons hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="fb640-151">The ring mode of the phone has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb640-152"><span id="PHONESTATE_RINGVOLUME"></span><span id="phonestate_ringvolume"></span>**phonestate- \_ ringvolume**</span><span class="sxs-lookup"><span data-stu-id="fb640-152"><span id="PHONESTATE_RINGVOLUME"></span><span id="phonestate_ringvolume"></span>**PHONESTATE\_RINGVOLUME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb640-153">Das ringvolume des Telefons hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="fb640-153">The ring volume of the phone has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb640-154"><span id="PHONESTATE_SPEAKERHOOKSWITCH"></span><span id="phonestate_speakerhookswitch"></span>**phonestate \_ speakerhookswitch**</span><span class="sxs-lookup"><span data-stu-id="fb640-154"><span id="PHONESTATE_SPEAKERHOOKSWITCH"></span><span id="phonestate_speakerhookswitch"></span>**PHONESTATE\_SPEAKERHOOKSWITCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb640-155">Der Status des Status von Speakerphone hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="fb640-155">The speakerphone's hookswitch state has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb640-156"><span id="PHONESTATE_SPEAKERGAIN"></span><span id="phonestate_speakergain"></span>**phonestate \_ speakergewinn**</span><span class="sxs-lookup"><span data-stu-id="fb640-156"><span id="PHONESTATE_SPEAKERGAIN"></span><span id="phonestate_speakergain"></span>**PHONESTATE\_SPEAKERGAIN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb640-157">Der Einstellungs Zustand des Mikrofon Anrufs des Speakers hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="fb640-157">The speakerphone's microphone gain setting state has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb640-158"><span id="PHONESTATE_SPEAKERVOLUME"></span><span id="phonestate_speakervolume"></span>**phonestate \_ speakervolume**</span><span class="sxs-lookup"><span data-stu-id="fb640-158"><span id="PHONESTATE_SPEAKERVOLUME"></span><span id="phonestate_speakervolume"></span>**PHONESTATE\_SPEAKERVOLUME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb640-159">Die Lautstärke Einstellung des Lautstärke Telefons hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="fb640-159">The speakerphone's speaker volume setting has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb640-160"><span id="PHONESTATE_SUSPEND"></span><span id="phonestate_suspend"></span>**phonestate \_ Suspend**</span><span class="sxs-lookup"><span data-stu-id="fb640-160"><span id="PHONESTATE_SUSPEND"></span><span id="phonestate_suspend"></span>**PHONESTATE\_SUSPEND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb640-161">Die Verwendung des Telefons der Anwendung wird vorübergehend angehalten.</span><span class="sxs-lookup"><span data-stu-id="fb640-161">The application's use of the phone is temporarily suspended.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fb640-162">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fb640-162">Remarks</span></span>

<span data-ttu-id="fb640-163">Keine Erweiterbarkeit.</span><span class="sxs-lookup"><span data-stu-id="fb640-163">No extensibility.</span></span> <span data-ttu-id="fb640-164">Alle 32 Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="fb640-164">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb640-165">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fb640-165">Requirements</span></span>



| <span data-ttu-id="fb640-166">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fb640-166">Requirement</span></span> | <span data-ttu-id="fb640-167">Wert</span><span class="sxs-lookup"><span data-stu-id="fb640-167">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="fb640-168">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="fb640-168">TAPI version</span></span><br/> | <span data-ttu-id="fb640-169">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="fb640-169">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="fb640-170">Header</span><span class="sxs-lookup"><span data-stu-id="fb640-170">Header</span></span><br/>       | <dl> <span data-ttu-id="fb640-171"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb640-171"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb640-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb640-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb640-173">**Telefon \_ Schließen**</span><span class="sxs-lookup"><span data-stu-id="fb640-173">**PHONE\_CLOSE**</span></span>](phone-close.md)
</dt> <dt>

[<span data-ttu-id="fb640-174">**Telefon \_ Status**</span><span class="sxs-lookup"><span data-stu-id="fb640-174">**PHONE\_STATE**</span></span>](phone-state.md)
</dt> <dt>

[<span data-ttu-id="fb640-175">**Phonecaps**</span><span class="sxs-lookup"><span data-stu-id="fb640-175">**PHONECAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-phonecaps)
</dt> <dt>

[<span data-ttu-id="fb640-176">**phonegetdevcaps**</span><span class="sxs-lookup"><span data-stu-id="fb640-176">**phoneGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> </dl>

 

 




