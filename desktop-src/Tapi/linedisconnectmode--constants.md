---
description: Die \_ LINEDISCONNECTMODE-Bitflagkonst constants beschreiben verschiedene Gründe für eine Remoteverbindungsanforderung. Ein Trennungsmodus ist als Aufrufstatus für die Anwendung verfügbar, nachdem der Aufrufzustand in Getrennt übergeschaltet wurde.
ms.assetid: 1b26f13c-b0bf-4d2c-8514-f0c376e36bcd
title: LINEDISCONNECTMODE_ Konstanten (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41ad56f993d746e5d09e33e4dcfb74d29766dd359fa47302053e0af13513a7da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060668"
---
# <a name="linedisconnectmode_-constants"></a>\_LINEDISCONNECTMODE-Konstanten

Die **\_ LINEDISCONNECTMODE-Bitflagkonst** constants beschreiben verschiedene Gründe für eine Remoteverbindungsanforderung. Ein Trennungsmodus ist als Aufrufstatus für die Anwendung verfügbar, nachdem der Aufrufzustand in Getrennt übergeschaltet wurde.

<dl> <dt>

<span id="LINEDISCONNECTMODE_BADADDRESS"></span><span id="linedisconnectmode_badaddress"></span>**LINEDISCONNECTMODE \_ BADADDRESS**
</dt> <dd> <dl> <dt>



Die Zieladresse ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_BLOCKED"></span><span id="linedisconnectmode_blocked"></span>**LINEDISCONNECTMODE \_ BLOCKIERT**
</dt> <dd> <dl> <dt>



Der Aufruf konnte nicht verbunden werden, da Aufrufe von der Ursprungsadresse nicht an der Zieladresse akzeptiert werden. Dies unterscheidet sich von LINEDISCONNECTMODE REJECT dadurch, dass die Blockierung im Netzwerk implementiert wird (eine passive Ablehnung), während eine Ablehnung in der Zielgeräte implementiert wird (eine aktive \_ Ablehnung). Die Blockierung kann auf einen bestimmten Ausschluss der Ursprungsadresse oder darauf führen, dass das Ziel Nur Aufrufe von einem ausgewählten Satz von Ursprungsadressen (geschlossene Benutzergruppe) akzeptiert. (TAPI-Versionen 2.0 und höher)

LINEDISCONNECTMODE \_ BLOCKED ist als Antwort in der Blockliste geeignet. Beispielsweise hat ein Modem eine Antwort erhalten, mehr als sechs Sekunden ohne Erkennung von Ringback versäumt, konnte eine definierte Anzahl von Verbindungen nicht herstellen, ermittelt, dass die Telefonnummer für den Anruf ungültig ist, und gibt eine Antwort aus, die in der Blockliste aufgeführt ist.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_BUSY"></span><span id="linedisconnectmode_busy"></span>**LINEDISCONNECTMODE \_ AUSGELASTET**
</dt> <dd> <dl> <dt>



Die Station des Remotebenutzers ist ausgelastet.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_CANCELLED"></span><span id="linedisconnectmode_cancelled"></span>**LINEDISCONNECTMODE \_ CANCELLED**
</dt> <dd> <dl> <dt>



Der Aufruf wurde abgebrochen. (TAPI-Versionen 2.0 und höher)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_CONGESTION"></span><span id="linedisconnectmode_congestion"></span>**\_LINEDISCONNECTMODE-ÜBERLASTUNG**
</dt> <dd> <dl> <dt>



Das Netzwerk ist überlastet.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_DONOTDISTURB"></span><span id="linedisconnectmode_donotdisturb"></span>**LINEDISCONNECTMODE \_ DONOTDISTURB**
</dt> <dd> <dl> <dt>



Der Aufruf konnte nicht verbunden werden, da das Ziel das Feature Nicht stören aufgerufen hat. (TAPI-Versionen 2.0 und höher)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_FORWARDED"></span><span id="linedisconnectmode_forwarded"></span>**LINEDISCONNECTMODE \_ WEITERGELEITET**
</dt> <dd> <dl> <dt>



Der Aufruf wurde vom Schalter weitergeleitet.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_INCOMPATIBLE"></span><span id="linedisconnectmode_incompatible"></span>**LINEDISCONNECTMODE \_ INKOMPATIBEL**
</dt> <dd> <dl> <dt>



Das Stationsgerät des Remotebenutzers ist nicht mit dem angeforderten Anruftyp kompatibel.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_NOANSWER"></span><span id="linedisconnectmode_noanswer"></span>**LINEDISCONNECTMODE \_ NOANSWER**
</dt> <dd> <dl> <dt>



Die Station des Remotebenutzers antwortet nicht.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_NODIALTONE"></span><span id="linedisconnectmode_nodialtone"></span>**LINEDISCONNECTMODE \_ NODIALTONE**
</dt> <dd> <dl> <dt>



Ein Wählton wurde innerhalb eines vom Dienstanbieter definierten Timeouts zu einem Zeitpunkt während des Wählens nicht erkannt, als ein Solcher erwartet wurde (z. B. bei einem "W" in der Wählzeichenfolge). Dies kann auch ohne einen vom Dienstanbieter definierten Timeoutzeitraum oder ohne einen Wert auftreten, der im **dwWaitForDialTone-Member** der [**LINEDIALPARAMS-Struktur angegeben**](/windows/desktop/api/Tapi/ns-tapi-linedialparams) ist. (TAPI-Versionen 1.4 und höher)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_NORMAL"></span><span id="linedisconnectmode_normal"></span>**LINEDISCONNECTMODE \_ NORMAL**
</dt> <dd> <dl> <dt>



Dies ist eine normale Trennungsanforderung durch die Remote-Partei. Der Aufruf wurde normal beendet.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_NUMBERCHANGED"></span><span id="linedisconnectmode_numberchanged"></span>**LINEDISCONNECTMODE \_ NUMBERCHANGED**
</dt> <dd> <dl> <dt>



Der Aufruf konnte nicht verbunden werden, da die Zielnummer geändert wurde, aber es wird keine automatische Umleitung zur neuen Nummer bereitgestellt. (TAPI-Versionen 2.0 und höher)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_OUTOFORDER"></span><span id="linedisconnectmode_outoforder"></span>**LINEDISCONNECTMODE \_ OUTOFORDER**
</dt> <dd> <dl> <dt>



Der Aufruf konnte nicht verbunden werden oder wurde getrennt, da das Zielgerät nicht in der Reihenfolge ist (Hardwarefehler). (TAPI-Versionen 2.0 und höher)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_PICKUP"></span><span id="linedisconnectmode_pickup"></span>**LINEDISCONNECTMODE \_ PICKUP**
</dt> <dd> <dl> <dt>



Der Aufruf wurde von einem anderen Ort aus wähle.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_QOSUNAVAIL"></span><span id="linedisconnectmode_qosunavail"></span>**LINEDISCONNECTMODE \_ QOSUNAVAIL**
</dt> <dd> <dl> <dt>



Der Aufruf konnte nicht verbunden oder getrennt werden, da die Mindestqualität des Diensts nicht erreicht oder dauerhaft erhalten werden konnte. Dies unterscheidet sich von LINEDISCONNECTMODE INCOMPATIBLE, da das Fehlen von Ressourcen eine vorübergehende Bedingung \_ am Ziel sein kann. (TAPI-Versionen 2.0 und höher)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_REJECT"></span><span id="linedisconnectmode_reject"></span>**LINEDISCONNECTMODE \_ REJECT**
</dt> <dd> <dl> <dt>



Der Remotebenutzer hat den Aufruf abgelehnt.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_TEMPFAILURE"></span><span id="linedisconnectmode_tempfailure"></span>**LINEDISCONNECTMODE \_ TEMPFAILURE**
</dt> <dd> <dl> <dt>



Der Aufruf konnte aufgrund eines vorübergehenden Fehlers im Netzwerk nicht verbunden oder getrennt werden. der Aufruf kann später erneut angefügt werden, und es wird erwartet, dass er schließlich abgeschlossen wird. (TAPI-Versionen 2.0 und höher)

LINEDISCONNECTMODE \_ TEMPFAILURE ist als verzögerte Antwort geeignet. Beispiel: Ein Modem, das in einem bestimmten Zeitraum zu oft ein Ausgelastetsignal oder ein entsprechendes Signal bekommt, kommt zu dem Schluss, dass die Zahl erst erneut aufgerufen werden soll, wenn eine definierte Zeit verstrichen ist, und gibt eine "verzögerte" Antwort aus.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_UNAVAIL"></span><span id="linedisconnectmode_unavail"></span>**LINEDISCONNECTMODE \_ UNAVAIL**
</dt> <dd> <dl> <dt>



Der Grund für die Trennung der Verbindung ist nicht verfügbar und wird später nicht bekannt.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_UNKNOWN"></span><span id="linedisconnectmode_unknown"></span>**LINEDISCONNECTMODE \_ UNKNOWN**
</dt> <dd> <dl> <dt>



Der Grund für die Trennungsanforderung ist unbekannt, kann aber später bekannt werden.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_UNREACHABLE"></span><span id="linedisconnectmode_unreachable"></span>**LINEDISCONNECTMODE \_ NICHT ERREICHBAR**
</dt> <dd> <dl> <dt>



Der Remotebenutzer konnte nicht erreicht werden.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Die hochwertigen 16 Bits können für gerätespezifische Erweiterungen zugewiesen werden. Die niedrigen 16 Bits sind reserviert.

Eine Remote disconnect-Anforderung für einen bestimmten Aufruf führt dazu, dass der Aufrufzustand in den getrennten Zustand über geht und eine [**LINE \_ CALLSTATE-Nachricht**](line-callstate.md) an die Anwendung gesendet wird. Die LINEDISCONNECTMODE-Informationen \_ enthalten Details zur Remoteverbindungsanforderung. Sie ist in der [**LINECALLSTATUS-Struktur**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) des Aufrufs verfügbar, wenn sich der Aufruf im getrennten Zustand befindet. Während sich ein Aufruf in diesem Zustand befindet, kann die Anwendung weiterhin die Informationen und den Status des Aufrufs abfragen. Beispielsweise sind Benutzer-Benutzer-Informationen, die als Teil der Remotetrennung empfangen werden, dann verfügbar. Die Anwendung kann einen getrennten Aufruf löschen, indem sie den Aufruf verdringt.

Aus Gründen der Abwärtskompatibilität ist der Dienstanbieter dafür verantwortlich, die ausgehandelte API-Version in der Zeile zu untersuchen und diesen LINEDISCONNECTMODE-Wert nicht zu verwenden, wenn er für die ausgehandelte Version nicht unterstützt wird \_ (stattdessen könnten LINEDISCONNECTMODE NORMAL oder UNKNOWN verwendet \_ \_ werden).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**LINE \_ CALLSTATE**](line-callstate.md)
</dt> <dt>

[**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)
</dt> <dt>

[**LINEDIALPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linedialparams)
</dt> </dl>

 

 




