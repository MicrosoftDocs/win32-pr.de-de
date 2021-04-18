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
# <a name="linedevstate_-constants"></a>Linedevstate- \_ Konstanten

Die Bits-Flag-Konstanten von **linedevstate \_** beschreiben verschiedene Zeilen Statusereignisse.

<dl> <dt>

<span id="LINEDEVSTATE_BATTERY"></span><span id="linedevstate_battery"></span>**linedevstate- \_ Akku**
</dt> <dd> <dl> <dt>



Der Akku Pegel hat sich erheblich geändert (Mobilfunk).


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_CAPSCHANGE"></span><span id="linedevstate_capschange"></span>**linedevstate \_ capschange**
</dt> <dd> <dl> <dt>



Gibt an, dass ein oder mehrere Member in der [**linedevcaps**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) -Struktur für die Adresse aufgrund von Konfigurationsänderungen, die vom Benutzer oder anderen Bedingungen vorgenommen wurden, geändert wurden. Die Anwendung sollte [**linegetdevcaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps) zum Lesen der aktualisierten Struktur verwenden. Wenn ein Dienstanbieter eine [**Zeile \_ linedevstate**](line-linedevstate.md) -Nachricht mit diesem Wert an TAPI sendet, übergibt TAPI ihn an Anwendungen, die die TAPI-Version 1,4 oder höher ausgehandelt haben. Anwendungen, die eine vorherige TAPI-Version aushandeln, erhalten linedevstate- **Zeilen \_** Meldungen mit linedevstate \_ Reit, sodass diese die aktualisierten Informationen Herunterfahren und erneut initialisieren müssen.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_CLOSE"></span><span id="linedevstate_close"></span>**linedevstate \_ Schließen**
</dt> <dd> <dl> <dt>



Die Zeile wurde von einer anderen Anwendung geschlossen.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_CONFIGCHANGE"></span><span id="linedevstate_configchange"></span>**linedevstate \_ configchange**
</dt> <dd> <dl> <dt>



Gibt an, dass Konfigurationsänderungen an einem oder mehreren Mediengeräten vorgenommen wurden, die mit dem liniengerät verknüpft sind. Die Anwendung kann, wenn Sie sich wünscht, [**linegetdevconfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) verwenden, um die aktualisierten Informationen zu lesen. Wenn ein Dienstanbieter eine [**Zeile \_ linedevstate**](line-linedevstate.md) -Nachricht mit diesem Wert an TAPI sendet, übergibt TAPI ihn an Anwendungen, die TAPI-Version 1,4 oder höher ausgehandelt haben. Anwendungen, die eine frühere API-Version aushandeln, erhalten keine Benachrichtigung.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_COMPLCANCEL"></span><span id="linedevstate_complcancel"></span>**linedevstate \_ complcancel**
</dt> <dd> <dl> <dt>



Gibt an, dass der von der Vervollständigungs-ID, der im *dwParam2* -Parameter der [**line \_ linedevstate**](line-linedevstate.md) -Nachricht enthaltene Abschluss Bezeichner identifiziert wurde, extern abgebrochen wurde und nicht mehr als gültig angesehen wird (wenn der Wert in einem nachfolgenden Ausdruck von [**lineuncompletecallübergeben**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall)werden soll, schlägt die Funktion mit lineerr \_ invalcompletionid fehl). Wenn ein Dienstanbieter eine [**Zeile \_ linedevstate**](line-linedevstate.md) -Nachricht mit diesem Wert an TAPI sendet, übergibt TAPI ihn an Anwendungen, die TAPI-Version 1,4 oder höher ausgehandelt haben. Anwendungen, die eine frühere API-Version aushandeln, erhalten keine Benachrichtigung.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_CONNECTED"></span><span id="linedevstate_connected"></span>**linedevstate \_ verbunden**
</dt> <dd> <dl> <dt>



Die Zeile wurde zuvor getrennt und ist jetzt mit TAPI verbunden.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_DEVSPECIFIC"></span><span id="linedevstate_devspecific"></span>**linedevstate \_ DevSpecific**
</dt> <dd> <dl> <dt>



Die gerätespezifischen Informationen der Zeile wurden geändert.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_DISCONNECTED"></span><span id="linedevstate_disconnected"></span>**linedevstate \_ getrennt**
</dt> <dd> <dl> <dt>



Diese Zeile war bereits verbunden und ist nun von TAPI getrennt.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_INSERVICE"></span><span id="linedevstate_inservice"></span>**linedevstate- \_ INService**
</dt> <dd> <dl> <dt>



Die Linie ist mit TAPI verbunden. Dies ist der Fall, wenn TAPI zum ersten Mal aktiviert wird, oder wenn die Linienverbindung physisch an den Switch angeschlossen ist und sich im Dienst befindet, während TAPI aktiv ist.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_LOCK"></span><span id="linedevstate_lock"></span>**linedevstate- \_ Sperre**
</dt> <dd> <dl> <dt>



Der gesperrte Status des Linien Geräts hat sich geändert. (Weitere Informationen finden Sie unter linedevstatus Flags \_ In [**linedevstatus-Flags- \_ Konstanten**](linedevstatusflags--constants.md)gesperrt.)


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_MAINTENANCE"></span><span id="linedevstate_maintenance"></span>**linedevstate- \_ Wartung**
</dt> <dd> <dl> <dt>



Die Wartung erfolgt in der Zeile am Switch. TAPI kann nicht verwendet werden, um auf dem liniengerät zu arbeiten.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_MSGWAITOFF"></span><span id="linedevstate_msgwaitoff"></span>**linedevstate \_ msgwaideff**
</dt> <dd> <dl> <dt>



Der Meldungs Warnungs Indikator ist deaktiviert.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_MSGWAITON"></span><span id="linedevstate_msgwaiton"></span>**linedevstate \_ msgwaiton**
</dt> <dd> <dl> <dt>



Der Indikator für die Nachrichten Warteschlange ist aktiviert.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_NUMCALLS"></span><span id="linedevstate_numcalls"></span>**linedevstate- \_ numrufe**
</dt> <dd> <dl> <dt>



Die Anzahl der Aufrufe auf dem liniengerät hat sich geändert.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_NUMCOMPLETIONS"></span><span id="linedevstate_numcompletions"></span>**linedevstate- \_ numcompletions**
</dt> <dd> <dl> <dt>



Die Anzahl der ausstehenden Aufrufe zum Abschluss des Geräts hat sich geändert.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_OPEN"></span><span id="linedevstate_open"></span>**linedevstate \_ geöffnet**
</dt> <dd> <dl> <dt>



Die Zeile wurde von einer anderen Anwendung geöffnet.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_OTHER"></span><span id="linedevstate_other"></span>**anderer linedevstate \_**
</dt> <dd> <dl> <dt>



Andere Gerätestatus Elemente als die unten aufgeführten wurden geändert. Die Anwendung sollte den aktuellen Gerätestatus überprüfen, um zu bestimmen, welche Elemente geändert wurden.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_OUTOFSERVICE"></span><span id="linedevstate_outofservice"></span>**"linedevstate" ( \_ outo fservice)**
</dt> <dd> <dl> <dt>



Die Zeile ist nicht mehr auf dem Switch oder physisch getrennt. TAPI kann nicht verwendet werden, um auf dem liniengerät zu arbeiten.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_REINIT"></span><span id="linedevstate_reinit"></span>**linedevstate \_ Reit**
</dt> <dd> <dl> <dt>



Elemente wurden in der Konfiguration von Linien Geräten geändert. Um diese Änderungen zu beachten (wie bei der Darstellung von neuen Zeilen Geräten), sollte die Anwendung die Verwendung von TAPI erneut initialisieren.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_REMOVED"></span><span id="linedevstate_removed"></span>**linedevstate \_ entfernt**
</dt> <dd> <dl> <dt>



Gibt an, dass das Gerät vom Dienstanbieter aus dem System entfernt wird (wahrscheinlich über eine Benutzeraktion, über eine Systemsteuerung oder ein ähnliches Hilfsprogramm). An [**eine \_ linienlinedevstate**](line-linedevstate.md) -Nachricht mit diesem Wert folgt normalerweise direkt eine Meldung zum [**\_ Schließen**](line-close.md) des Geräts auf dem Gerät. Nachfolgende Zugriffsversuche auf das Gerät vor der erneuten Initialisierung von TAPI führen dazu, dass lineerr \_ nodevice an die Anwendung zurückgegeben wird. Wenn ein Dienstanbieter eine [**Zeile \_ linedevstate**](line-linedevstate.md) -Nachricht mit diesem Wert an TAPI sendet, übergibt TAPI ihn an Anwendungen, die TAPI-Version 1,4 oder höher ausgehandelt haben. Anwendungen, die eine frühere API-Version aushandeln, erhalten keine Benachrichtigung.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_RINGING"></span><span id="linedevstate_ringing"></span>**linedevstate- \_ Klingeln**
</dt> <dd> <dl> <dt>



Der-Schalter weist die Zeile an, den Benutzer zu benachrichtigen.

**TAPI:** Dienstanbieter Benachrichtigen Anwendungen in jedem Ring, indem Sie wiederholt [**Zeilen- \_ linedevstate**](line-linedevstate.md) -Nachrichten senden, die diese Konstante enthalten. Im USA senden Dienstanbieter beispielsweise alle sechs Sekunden eine Nachricht mit dieser Konstante.

**TSPI:** Auf einem Pots-Gerät kann der Dienstanbieter die Nachricht senden, wenn die zentral Niederlassung eine Ring Spannung sendet. Auf digitalen Geräten wie z. b. ISDN muss der Dienstanbieter die Wiederholung der Nachricht möglicherweise synthetisieren, wenn der Switch nur eine Ring Anforderung generiert. Jede Wiederholung der Nachricht sollte die Ring Anzahl erhöhen, sodass die Maut Speicherfunktionen ordnungsgemäß funktionieren.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_ROAMMODE"></span><span id="linedevstate_roammode"></span>**linedevstate ( \_ roammode)**
</dt> <dd> <dl> <dt>



Der Modus "Roaming" des Linien Geräts hat sich geändert.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_SIGNAL"></span><span id="linedevstate_signal"></span>**linedevstate- \_ Signal**
</dt> <dd> <dl> <dt>



Die Signalebene hat sich erheblich geändert (Mobilfunk).


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_TERMINALS"></span><span id="linedevstate_terminals"></span>**linedevstate- \_ Terminals**
</dt> <dd> <dl> <dt>



Die Terminal Einstellungen wurden geändert. Dies kann z. b. der Fall sein, wenn in mehreren Zeilen Geräten Terminals gemeinsam genutzt werden (z. b. zwei Zeilen, die ein Telefon Terminal gemeinsam verwenden).


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_TRANSLATECHANGE"></span><span id="linedevstate_translatechange"></span>**linedevstate \_ translatechange**
</dt> <dd> <dl> <dt>



Gibt an, dass ein oder mehrere Member in der [**linetranslatecaps**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) -Struktur aufgrund von Konfigurationsänderungen, die vom Benutzer oder anderen Bedingungen vorgenommen wurden, geändert wurden. Die Anwendung sollte [**linegettranslatecaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps) zum Lesen der aktualisierten Struktur verwenden. Wenn ein Dienstanbieter eine [**Zeile \_ linedevstate**](line-linedevstate.md) -Nachricht mit diesem Wert an TAPI sendet, übergibt TAPI ihn an Anwendungen, die die TAPI-Version 1,4 oder höher ausgehandelt haben. Anwendungen, die eine vorherige TAPI-Version aushandeln, erhalten linedevstate- **Zeilen \_** Meldungen mit linedevstate \_ Reit, sodass diese die aktualisierten Informationen Herunterfahren und erneut initialisieren müssen.


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

[**Zeilen \_ Schließen**](line-close.md)
</dt> <dt>

[**\_linienlinedevstate**](line-linedevstate.md)
</dt> <dt>

[**Linedevcaps**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)
</dt> <dt>

[**linegetdevcaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)
</dt> <dt>

[**linegetdevconfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)
</dt> <dt>

[**linegettranslatecaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)
</dt> <dt>

[**Linetranslatecaps**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps)
</dt> <dt>

[**lineuncompletecall**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall)
</dt> </dl>

 

 




