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
# <a name="phonestate_-constants"></a>Phonestate- \_ Konstanten

Die Bit-Flag-Konstanten von **phonestate \_** beschreiben verschiedene Status Elemente für ein Telefongerät.

<dl> <dt>

<span id="PHONESTATE_CAPSCHANGE"></span><span id="phonestate_capschange"></span>**"phonestate \_ capschange"**
</dt> <dd> <dl> <dt>



Gibt an, dass ein oder mehrere Member in der [**phonecaps**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) -Struktur aufgrund von Konfigurationsänderungen, die vom Benutzer oder anderen Bedingungen vorgenommen wurden, geändert wurden. Die Anwendung sollte [**phonegetdevcaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) verwenden, um die aktualisierte Struktur zu lesen. Wenn ein Dienstanbieter eine [**Telefon \_ Zustands**](phone-state.md) Meldung mit diesem Wert an TAPI sendet, übergibt TAPI ihn an Anwendungen, die die TAPI-Version 1,4 oder höher ausgehandelt haben. Anwendungen, die eine vorherige API-Version aushandeln, erhalten Telefon \_ Zustands Meldungen, die das phonestate \_ REIT-Gerät zum Abrufen der aktualisierten Informationen benötigen.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_CONNECTED"></span><span id="phonestate_connected"></span>**phonestate \_ verbunden**
</dt> <dd> <dl> <dt>



Die Verbindung zwischen dem Telefongerät und TAPI wurde soeben hergestellt. Dies ist der Fall, wenn TAPI zum ersten Mal aufgerufen wird oder wenn die Verbindung des Telefons mit dem PC mit TAPI Active angeschlossen ist.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_DEVSPECIFIC"></span><span id="phonestate_devspecific"></span>**phonestate \_ DevSpecific**
</dt> <dd> <dl> <dt>



Die gerätespezifischen Informationen des Telefons wurden geändert.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_DISCONNECTED"></span><span id="phonestate_disconnected"></span>**phonestate \_ getrennt**
</dt> <dd> <dl> <dt>



Die Verbindung zwischen dem Telefongerät und TAPI war einfach beschädigt. Dies ist der Fall, wenn die Verbindung, die das Telefon mit dem PC verbindet, getrennt ist, während TAPI aktiv ist.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_DISPLAY"></span><span id="phonestate_display"></span>**phonestate- \_ Anzeige**
</dt> <dd> <dl> <dt>



Die Anzeige des Telefons hat sich geändert.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HANDSETGAIN"></span><span id="phonestate_handsetgain"></span>**phonestate \_ handsetgewinn**
</dt> <dd> <dl> <dt>



Die Mikrofon Gewinn Einstellung des Mobiltelefons hat sich geändert.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HANDSETHOOKSWITCH"></span><span id="phonestate_handsethookswitch"></span>**phonestate \_ handlthookswitch**
</dt> <dd> <dl> <dt>



Der Status des "geokswitch" des Mobiltelefons wurde geändert.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HANDSETVOLUME"></span><span id="phonestate_handsetvolume"></span>**phonestate \_ handsetvolume**
</dt> <dd> <dl> <dt>



Die Lautstärke Einstellung des Handlers wurde geändert.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HEADSETHOOKSWITCH"></span><span id="phonestate_headsethookswitch"></span>**phonestate \_ headsinthookswitch**
</dt> <dd> <dl> <dt>



Der Status des "huokswitch" wurde geändert.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HEADSETGAIN"></span><span id="phonestate_headsetgain"></span>**phonestate \_ headsetgewinn**
</dt> <dd> <dl> <dt>



Die Mikrofon Gewinn Einstellung des Headsets hat sich geändert.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HEADSETVOLUME"></span><span id="phonestate_headsetvolume"></span>**phonestate \_ headsetvolume**
</dt> <dd> <dl> <dt>



Die Lautstärke der Lautstärke für das Headset hat sich geändert.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_LAMP"></span><span id="phonestate_lamp"></span>**phonestate- \_ Lamp**
</dt> <dd> <dl> <dt>



Eine Glühbirne des Telefons hat sich geändert.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_MONITORS"></span><span id="phonestate_monitors"></span>**phonestate- \_ Monitore**
</dt> <dd> <dl> <dt>



Die Anzahl der Monitore für das Telefongerät.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_OTHER"></span><span id="phonestate_other"></span>**Sonstige phonestate \_**
</dt> <dd> <dl> <dt>



Andere Telefonstatus Elemente als die unten aufgeführten haben sich geändert. Die Anwendung sollte den aktuellen Telefonstatus überprüfen, um zu bestimmen, welche Elemente geändert wurden.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_OWNER"></span><span id="phonestate_owner"></span>**phonestate- \_ Besitzer**
</dt> <dd> <dl> <dt>



Die Anzahl von Besitzern für das Telefongerät.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_REINIT"></span><span id="phonestate_reinit"></span>**phonestate \_ Reit**
</dt> <dd> <dl> <dt>



Elemente wurden in der Konfiguration von Telefongeräten geändert. Um diese Änderungen zu erkennen (wie bei der Darstellung neuer Telefongeräte), sollte die Anwendung die Verwendung von TAPI erneut initialisieren.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_REMOVED"></span><span id="phonestate_removed"></span>**phonestate \_ entfernt**
</dt> <dd> <dl> <dt>



Gibt an, dass das Gerät vom Dienstanbieter aus dem System entfernt wird (wahrscheinlich über eine Benutzeraktion, über eine Systemsteuerung oder ein ähnliches Hilfsprogramm). Auf eine [**Telefon \_ Zustands**](phone-state.md) Meldung mit diesem Wert folgt normalerweise direkt eine Meldung zum [**\_ Schließen des Telefons**](phone-close.md) auf dem Gerät. Nachfolgende Zugriffsversuche auf das Gerät vor der erneuten Initialisierung von TAPI führen dazu, dass "phoneerr \_ nodevice" an die Anwendung zurückgegeben wird. Wenn ein Dienstanbieter eine Telefon \_ Zustands Meldung mit diesem Wert an TAPI sendet, übergibt TAPI ihn an Anwendungen, die die TAPI-Version 1,4 oder höher ausgehandelt haben. Anwendungen, die eine frühere API-Version aushandeln, erhalten keine Benachrichtigung.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_RESUME"></span><span id="phonestate_resume"></span>**phonestate \_ Resume**
</dt> <dd> <dl> <dt>



Die Anwendungs Verwendung des Telefon Geräts wird fortgesetzt, nachdem es seit einiger Zeit angehalten wurde.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_RINGMODE"></span><span id="phonestate_ringmode"></span>**phonestate- \_ ringmodus**
</dt> <dd> <dl> <dt>



Der Klingel Modus des Telefons hat sich geändert.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_RINGVOLUME"></span><span id="phonestate_ringvolume"></span>**phonestate- \_ ringvolume**
</dt> <dd> <dl> <dt>



Das ringvolume des Telefons hat sich geändert.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_SPEAKERHOOKSWITCH"></span><span id="phonestate_speakerhookswitch"></span>**phonestate \_ speakerhookswitch**
</dt> <dd> <dl> <dt>



Der Status des Status von Speakerphone hat sich geändert.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_SPEAKERGAIN"></span><span id="phonestate_speakergain"></span>**phonestate \_ speakergewinn**
</dt> <dd> <dl> <dt>



Der Einstellungs Zustand des Mikrofon Anrufs des Speakers hat sich geändert.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_SPEAKERVOLUME"></span><span id="phonestate_speakervolume"></span>**phonestate \_ speakervolume**
</dt> <dd> <dl> <dt>



Die Lautstärke Einstellung des Lautstärke Telefons hat sich geändert.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_SUSPEND"></span><span id="phonestate_suspend"></span>**phonestate \_ Suspend**
</dt> <dd> <dl> <dt>



Die Verwendung des Telefons der Anwendung wird vorübergehend angehalten.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Telefon \_ Schließen**](phone-close.md)
</dt> <dt>

[**Telefon \_ Status**](phone-state.md)
</dt> <dt>

[**Phonecaps**](/windows/desktop/api/Tapi/ns-tapi-phonecaps)
</dt> <dt>

[**phonegetdevcaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> </dl>

 

 




