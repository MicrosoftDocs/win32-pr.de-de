---
description: Die \_ LINEDEVSTATE-Bitflagkonst constants beschreiben verschiedene Zeilenstatusereignisse.
ms.assetid: 41e8a777-a57a-4d6c-850f-e21b58081b0d
title: LINEDEVSTATE_ Konstanten (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb11959614999ff50e421e0b77c63d1215a831040774e3123b43aa3534a3f853
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140063"
---
# <a name="linedevstate_-constants"></a>LINEDEVSTATE-Konstanten \_

Die **\_ LINEDEVSTATE-Bitflagkonst** constants beschreiben verschiedene Zeilenstatusereignisse.

<dl> <dt>

<span id="LINEDEVSTATE_BATTERY"></span><span id="linedevstate_battery"></span>**LINEDEVSTATE \_ BATTERY**
</dt> <dd> <dl> <dt>



Der Akkustand hat sich erheblich geändert (Mobilfunk).


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_CAPSCHANGE"></span><span id="linedevstate_capschange"></span>**LINEDEVSTATE \_ CAPSCHANGE**
</dt> <dd> <dl> <dt>



Gibt an, dass sich aufgrund von Konfigurationsänderungen, die vom Benutzer oder anderen Umständen vorgenommen wurden, mindestens eines der Member in der [**LINEDEVCAPS-Struktur**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) für die Adresse geändert hat. Die Anwendung sollte [**lineGetDevCaps verwenden,**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps) um die aktualisierte Struktur zu lesen. Wenn ein Dienstanbieter eine [**LINE \_ LINEDEVSTATE-Nachricht**](line-linedevstate.md) mit diesem Wert an TAPI sendet, überträgt TAPI diese an Anwendungen, die TAPI Version 1.4 oder höher ausgehandelt haben. Anwendungen, die eine frühere TAPI-Version aushandeln, empfangen **LINE \_ LINEDEVSTATE-Nachrichten,** die LINEDEVSTATE REINIT angeben, und er muss die Verbindung mit TAPI herunterfahren und erneut initialisieren, um die aktualisierten Informationen zu \_ erhalten.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_CLOSE"></span><span id="linedevstate_close"></span>**LINEDEVSTATE \_ CLOSE**
</dt> <dd> <dl> <dt>



Die Zeile wurde von einer anderen Anwendung geschlossen.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_CONFIGCHANGE"></span><span id="linedevstate_configchange"></span>**LINEDEVSTATE \_ CONFIGCHANGE**
</dt> <dd> <dl> <dt>



Gibt an, dass Konfigurationsänderungen an einem oder an mindestens einem Mediengerät vorgenommen wurden, das dem Liniengerät zugeordnet ist. Die Anwendung kann bei Wunsch [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) verwenden, um die aktualisierten Informationen zu lesen. Wenn ein Dienstanbieter eine [**LINE \_ LINEDEVSTATE-Nachricht**](line-linedevstate.md) mit diesem Wert an TAPI sendet, überträgt TAPI diese an Anwendungen, die TAPI Version 1.4 oder höher ausgehandelt haben. Anwendungen, die eine frühere API-Version aushandeln, erhalten keine Benachrichtigung.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_COMPLCANCEL"></span><span id="linedevstate_complcancel"></span>**LINEDEVSTATE \_ COMPLCANCEL**
</dt> <dd> <dl> <dt>



Gibt an, dass die durch den Abschlussbezeichner identifizierte Aufrufvervollständigung, die im *dwParam2-Parameter* der [**LINE \_ LINEDEVSTATE-Nachricht**](line-linedevstate.md) enthalten ist, extern abgebrochen wurde und nicht mehr als gültig angesehen wird (wenn dieser Wert in einem nachfolgenden Aufruf von [**lineUncompleteCall**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall)übergeben wird, würde die Funktion mit LINEERR \_ INVALCOMPLETIONID fehlschlagen). Wenn ein Dienstanbieter eine [**LINE \_ LINEDEVSTATE-Nachricht**](line-linedevstate.md) mit diesem Wert an TAPI sendet, überträgt TAPI diese an Anwendungen, die TAPI Version 1.4 oder höher ausgehandelt haben. Anwendungen, die eine frühere API-Version aushandeln, erhalten keine Benachrichtigung.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_CONNECTED"></span><span id="linedevstate_connected"></span>**LINEDEVSTATE \_ CONNECTED**
</dt> <dd> <dl> <dt>



Die Verbindung wurde zuvor getrennt und ist jetzt mit TAPI verbunden.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_DEVSPECIFIC"></span><span id="linedevstate_devspecific"></span>**LINEDEVSTATE \_ DEVSPECIFIC**
</dt> <dd> <dl> <dt>



Die gerätespezifischen Informationen der Zeile wurden geändert.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_DISCONNECTED"></span><span id="linedevstate_disconnected"></span>**LINEDEVSTATE \_ DISCONNECTED**
</dt> <dd> <dl> <dt>



Diese Zeile war zuvor verbunden und jetzt von TAPI getrennt.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_INSERVICE"></span><span id="linedevstate_inservice"></span>**LINEDEVSTATE \_ INSERVICE**
</dt> <dd> <dl> <dt>



Die Linie ist mit TAPI verbunden. Dies geschieht, wenn TAPI zum ersten Mal aktiviert wird oder wenn die Leitungsleitung physisch angeschlossen und am Switch in Dienst ist, während TAPI aktiv ist.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_LOCK"></span><span id="linedevstate_lock"></span>**\_LINEDEVSTATE-SPERRE**
</dt> <dd> <dl> <dt>



Der gesperrte Status des Liniengeräts hat sich geändert. (Weitere Informationen finden Sie unter LINEDEVSTATUSFLAGS. \_ LOCKED in [**LINEDEVSTATUSFLAGS-Konstanten \_**](linedevstatusflags--constants.md).)


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_MAINTENANCE"></span><span id="linedevstate_maintenance"></span>**LINEDEVSTATE \_ MAINTENANCE**
</dt> <dd> <dl> <dt>



Die Wartung wird auf der Linie am Schalter ausgeführt. TAPI kann nicht für den Betrieb auf dem Liniengerät verwendet werden.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_MSGWAITOFF"></span><span id="linedevstate_msgwaitoff"></span>**LINEDEVSTATE \_ MSGWAITOFF**
</dt> <dd> <dl> <dt>



Der Warteindikator für Nachrichten ist deaktiviert.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_MSGWAITON"></span><span id="linedevstate_msgwaiton"></span>**LINEDEVSTATE \_ MSGWAITON**
</dt> <dd> <dl> <dt>



Der Warteindikator für Nachrichten ist aktiviert.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_NUMCALLS"></span><span id="linedevstate_numcalls"></span>**LINEDEVSTATE \_ NUMCALLS**
</dt> <dd> <dl> <dt>



Die Anzahl der Aufrufe auf dem Liniengerät hat sich geändert.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_NUMCOMPLETIONS"></span><span id="linedevstate_numcompletions"></span>**LINEDEVSTATE \_ NUMCOMPLETIONS**
</dt> <dd> <dl> <dt>



Die Anzahl der ausstehenden Anruferledigungen auf dem Zeilengerät hat sich geändert.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_OPEN"></span><span id="linedevstate_open"></span>**LINEDEVSTATE \_ OPEN**
</dt> <dd> <dl> <dt>



Die Zeile wurde von einer anderen Anwendung geöffnet.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_OTHER"></span><span id="linedevstate_other"></span>**LINEDEVSTATE \_ OTHER**
</dt> <dd> <dl> <dt>



Andere Gerätestatuselemente als die unten aufgeführten wurden geändert. Die Anwendung sollte den aktuellen Gerätestatus überprüfen, um zu ermitteln, welche Elemente sich geändert haben.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_OUTOFSERVICE"></span><span id="linedevstate_outofservice"></span>**LINEDEVSTATE \_ OUTOFSERVICE**
</dt> <dd> <dl> <dt>



Die Linie ist am Switch außer Dienst oder physisch getrennt. TAPI kann nicht für den Betrieb auf dem Liniengerät verwendet werden.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_REINIT"></span><span id="linedevstate_reinit"></span>**LINEDEVSTATE \_ REINIT**
</dt> <dd> <dl> <dt>



Elemente wurden in der Konfiguration von Liniengeräten geändert. Um auf diese Änderungen zu reagieren (wie bei der Darstellung neuer Liniengeräte), sollte die Anwendung ihre Verwendung von TAPI erneut initialisieren.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_REMOVED"></span><span id="linedevstate_removed"></span>**LINEDEVSTATE \_ ENTFERNT**
</dt> <dd> <dl> <dt>



Gibt an, dass das Gerät vom Dienstanbieter aus dem System entfernt wird (wahrscheinlich durch Benutzeraktion, über eine Systemsteuerung oder ein ähnliches Hilfsprogramm). Auf [**eine LINE \_ LINEDEVSTATE-Nachricht**](line-linedevstate.md) mit diesem Wert folgt normalerweise sofort eine [**LINE \_ CLOSE-Meldung**](line-close.md) auf dem Gerät. Nachfolgende Versuche, auf das Gerät zu zugreifen, bevor TAPI erneut initialisiert wird, führen dazu, dass LINEERR \_ NODEVICE an die Anwendung zurückgegeben wird. Wenn ein Dienstanbieter eine [**LINE \_ LINEDEVSTATE-Nachricht**](line-linedevstate.md) mit diesem Wert an TAPI sendet, überträgt TAPI diese an Anwendungen, die TAPI Version 1.4 oder höher ausgehandelt haben. Anwendungen, die eine frühere API-Version aushandeln, erhalten keine Benachrichtigung.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_RINGING"></span><span id="linedevstate_ringing"></span>**LINEDEVSTATE \_ RINGING**
</dt> <dd> <dl> <dt>



Der Schalter weist die Zeile an, den Benutzer zu warnen.

**TAPI:** Dienstanbieter benachrichtigen Anwendungen bei jedem Ringzyklus, indem sie [**wiederholt \_ LINEDEVSTATE-Nachrichten**](line-linedevstate.md) senden, die diese Konstante enthalten. In der -USA senden Dienstanbieter beispielsweise alle sechs Sekunden eine Nachricht mit dieser Konstante.

**TSPI:** Auf einem GERÄTEgerät kann der Dienstanbieter die Nachricht immer dann senden, wenn die Zentrale Ringspannung sendet. Auf digitalen Geräten wie ISDN muss der Dienstanbieter möglicherweise die Wiederholung der Nachricht synthetisieren, wenn der Switch nur eine Ringanforderung generiert. Bei jeder Wiederholung der Nachricht sollte angezeigt werden, dass die Anzahl der Ringe zunimmt, damit die Toll Save-Funktionen ordnungsgemäß funktionieren.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_ROAMMODE"></span><span id="linedevstate_roammode"></span>**LINEDEVSTATE \_ ROAMMODE**
</dt> <dd> <dl> <dt>



Der Roamingmodus des Liniengeräts hat sich geändert.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_SIGNAL"></span><span id="linedevstate_signal"></span>**LINEDEVSTATE \_ SIGNAL**
</dt> <dd> <dl> <dt>



Die Signalstufe hat sich erheblich geändert (Mobilfunk).


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_TERMINALS"></span><span id="linedevstate_terminals"></span>**LINEDEVSTATE-TERMINALS \_**
</dt> <dd> <dl> <dt>



Die Terminaleinstellungen wurden geändert. Dies kann beispielsweise der Fall sein, wenn mehrere Liniengeräte Terminals gemeinsam nutzen (z. B. zwei Zeilen, die sich ein Telefonterminal teilen).


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_TRANSLATECHANGE"></span><span id="linedevstate_translatechange"></span>**LINEDEVSTATE \_ TRANSLATECHANGE**
</dt> <dd> <dl> <dt>



Gibt an, dass sich aufgrund von Konfigurationsänderungen, die vom Benutzer oder anderen Umständen vorgenommen wurden, mindestens eines der Member in der [**LINETRANSLATECAPS-Struktur**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) geändert hat. Die Anwendung sollte [**lineGetTranslateCaps verwenden,**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps) um die aktualisierte Struktur zu lesen. Wenn ein Dienstanbieter eine [**LINE \_ LINEDEVSTATE-Nachricht**](line-linedevstate.md) mit diesem Wert an TAPI sendet, überträgt TAPI diese an Anwendungen, die TAPI Version 1.4 oder höher ausgehandelt haben. Anwendungen, die eine frühere TAPI-Version aushandeln, empfangen **LINE \_ LINEDEVSTATE-Nachrichten,** die LINEDEVSTATE REINIT angeben, und er muss die Verbindung mit TAPI herunterfahren und erneut initialisieren, um die aktualisierten Informationen zu \_ erhalten.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**LINE \_ CLOSE**](line-close.md)
</dt> <dt>

[**LINE \_ LINEDEVSTATE**](line-linedevstate.md)
</dt> <dt>

[**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)
</dt> <dt>

[**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)
</dt> <dt>

[**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)
</dt> <dt>

[**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)
</dt> <dt>

[**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps)
</dt> <dt>

[**lineUncompleteCall**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall)
</dt> </dl>

 

 




