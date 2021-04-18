---
description: Die "linedisconnectmode" \_ -Bitflag-Konstanten beschreiben verschiedene Gründe für eine Remote-Trennungs Anforderung. Der Verbindungs Modus ist als Telefonstatus für die Anwendung verfügbar, nachdem der Status des Aufrufes in "getrennt" übergeht.
ms.assetid: 1b26f13c-b0bf-4d2c-8514-f0c376e36bcd
title: LINEDISCONNECTMODE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c70ba70175685e2c264343f9345227ee64c206f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371713"
---
# <a name="linedisconnectmode_-constants"></a>Linedisconnectmode- \_ Konstanten

Die " **linedisconnectmode \_** "-Bitflag-Konstanten beschreiben verschiedene Gründe für eine Remote-Trennungs Anforderung. Der Verbindungs Modus ist als Telefonstatus für die Anwendung verfügbar, nachdem der Status des Aufrufes in "getrennt" übergeht.

<dl> <dt>

<span id="LINEDISCONNECTMODE_BADADDRESS"></span><span id="linedisconnectmode_badaddress"></span>**linedisconnectmode- \_ badaddress**
</dt> <dd> <dl> <dt>



Die Zieladresse ist ungültig.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_BLOCKED"></span><span id="linedisconnectmode_blocked"></span>**"linedisconnectmode" wurde \_ blockiert.**
</dt> <dd> <dl> <dt>



Der Aufruf konnte nicht verbunden werden, weil Aufrufe von der Ursprungsadresse an der Zieladresse nicht akzeptiert werden. Dies unterscheidet sich von linedisconnectmode \_ ablehnen darin, dass die Blockierung im Netzwerk (eine passive Ablehnung) implementiert wird, während eine Ablehnung in den Ziel Geräten implementiert wird (eine aktive Ablehnung). Die Blockierung kann auf einen bestimmten Ausschluss der Ursprungsadresse oder darauf zurückzuführen sein, dass das Ziel nur Aufrufe von einem ausgewählten Satz von Ursprungs Adressen akzeptiert (geschlossene Benutzergruppe). (TAPI-Versionen 2,0 und höher)

Die Blockierung von linedisconnectmode \_ ist als Blockierungs Antwort geeignet. Ein Modem hat z. b. eine Antwort empfangen, die mehr als sechs Sekunden gedauert hat, ohne das Rollback zu erkennen, eine bestimmte Anzahl von Wiederholungen nicht zu verbinden, feststellt, dass die Telefonnummer ungültig ist, um aufzurufen, und gibt eine blockgelistete Antwort aus.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_BUSY"></span><span id="linedisconnectmode_busy"></span>**linedisconnectmode \_ ausgelastet**
</dt> <dd> <dl> <dt>



Die Station des Remote Benutzers ist ausgelastet.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_CANCELLED"></span><span id="linedisconnectmode_cancelled"></span>**linedisconnectmode \_ abgebrochen**
</dt> <dd> <dl> <dt>



Der-Rückruf wurde abgebrochen. (TAPI-Versionen 2,0 und höher)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_CONGESTION"></span><span id="linedisconnectmode_congestion"></span>**linedisconnectmode- \_ Überlastung**
</dt> <dd> <dl> <dt>



Das Netzwerk ist überlastet.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_DONOTDISTURB"></span><span id="linedisconnectmode_donotdisturb"></span>**linedisconnectmode- \_ donotstören**
</dt> <dd> <dl> <dt>



Der Aufruf konnte nicht verbunden werden, da das Ziel die Funktion "nicht stören" aufgerufen hat. (TAPI-Versionen 2,0 und höher)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_FORWARDED"></span><span id="linedisconnectmode_forwarded"></span>**linedisconnectmode \_ Weitergeleitet**
</dt> <dd> <dl> <dt>



Der-Befehl wurde vom Schalter weitergeleitet.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_INCOMPATIBLE"></span><span id="linedisconnectmode_incompatible"></span>**linedisconnectmode nicht \_ kompatibel**
</dt> <dd> <dl> <dt>



Die Stations Ausrüstung des Remote Benutzers ist nicht mit dem angeforderten Anforderungstyp kompatibel.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_NOANSWER"></span><span id="linedisconnectmode_noanswer"></span>**linedisconnectmode \_ noanswer**
</dt> <dd> <dl> <dt>



Die Station des Remote Benutzers antwortet nicht.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_NODIALTONE"></span><span id="linedisconnectmode_nodialtone"></span>**linedisconnectmode \_ nodialtone**
</dt> <dd> <dl> <dt>



Ein DFÜ-Ton wurde innerhalb eines vom Dienstanbieter definierten Timeouts nicht erkannt, zu einem Zeitpunkt während der Abwahl, wenn ein Wert erwartet wurde (z. b. bei einem "W" in der DFÜ-Zeichenfolge). Dies kann auch ohne ein vom Dienstanbieter definiertes Timeout Intervall oder ohne Angabe eines Werts im **dwwaitfordialtone** -Member der [**linedialparameams**](/windows/desktop/api/Tapi/ns-tapi-linedialparams) -Struktur vorkommen. (TAPI-Versionen 1,4 und höher)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_NORMAL"></span><span id="linedisconnectmode_normal"></span>**linedisconnectmode \_ Normal**
</dt> <dd> <dl> <dt>



Dabei handelt es sich um eine normale Disconnect-Anforderung durch den Remote Teilnehmer. Der-Befehl wurde normal beendet.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_NUMBERCHANGED"></span><span id="linedisconnectmode_numberchanged"></span>**linedisconnectmode- \_ nummerierungsänderung**
</dt> <dd> <dl> <dt>



Der-Rückruf konnte nicht verbunden werden, da die Ziel Nummer geändert wurde, aber es wurde keine automatische Umleitung zur neuen Nummer bereitgestellt. (TAPI-Versionen 2,0 und höher)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_OUTOFORDER"></span><span id="linedisconnectmode_outoforder"></span>**linedisconnectmode- \_ OutOfOrder**
</dt> <dd> <dl> <dt>



Der-Rückruf konnte nicht verbunden oder getrennt werden, da das Zielgerät nicht in der richtigen Reihenfolge ist (Hardwarefehler). (TAPI-Versionen 2,0 und höher)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_PICKUP"></span><span id="linedisconnectmode_pickup"></span>**linedisconnectmode \_ Pickup**
</dt> <dd> <dl> <dt>



Der-Befehl wurde von anderen Orten aus abgerufen.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_QOSUNAVAIL"></span><span id="linedisconnectmode_qosunavail"></span>**linedisconnectmode- \_ qosun**
</dt> <dd> <dl> <dt>



Der-Rückruf konnte nicht verbunden oder getrennt werden, da die minimale Quality of Service nicht abgerufen oder wieder hergestellt werden konnte. Dies unterscheidet sich von linedisconnectmode \_ , da das Fehlen von Ressourcen möglicherweise eine temporäre Bedingung am Ziel ist. (TAPI-Versionen 2,0 und höher)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_REJECT"></span><span id="linedisconnectmode_reject"></span>**linedisconnectmode \_ ablehnen**
</dt> <dd> <dl> <dt>



Der Remote Benutzer hat den-Befehl abgelehnt.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_TEMPFAILURE"></span><span id="linedisconnectmode_tempfailure"></span>**linedisconnectmode- \_ tempfailure**
</dt> <dd> <dl> <dt>



Der-Rückruf konnte nicht verbunden werden oder wurde aufgrund eines temporären Fehlers im Netzwerk getrennt. der Versuch kann später wiederholt werden, und es wird erwartet, dass er letztendlich fertiggestellt wird. (TAPI-Versionen 2,0 und höher)

"Linedisconnectmode \_ tempfailure" ist als verzögerte Antwort geeignet. Ein Modem, das beispielsweise ein ausgelasteter Signal oder eine Entsprechung zu oft in einem bestimmten Zeitraum erhält, endet, dass die Zahl erst wieder aufgerufen werden soll, wenn eine definierte Zeit verstrichen ist, und eine verzögerte Antwort ausgibt.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_UNAVAIL"></span><span id="linedisconnectmode_unavail"></span>**Deaktivieren von linedisconnectmode \_**
</dt> <dd> <dl> <dt>



Der Grund für die Trennung ist nicht verfügbar und wird später noch nicht bekannt werden.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_UNKNOWN"></span><span id="linedisconnectmode_unknown"></span>**"linedisconnectmode" ist \_ unbekannt.**
</dt> <dd> <dl> <dt>



Der Grund für die Trennungs Anforderung ist unbekannt, kann aber später bekannt werden.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_UNREACHABLE"></span><span id="linedisconnectmode_unreachable"></span>**linedisconnectmode \_ nicht erreichbar**
</dt> <dd> <dl> <dt>



Der Remote Benutzer konnte nicht erreicht werden.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die höherwertigen 16 Bits können für gerätespezifische Erweiterungen zugewiesen werden. Die nieder wertigen 16 Bits sind reserviert.

Eine Remote Trennungs Anforderung für einen bestimmten Aufruf führt dazu, dass der Aufruf Status in den getrennten Zustand übergeht und eine [**Zeile \_ CallState**](line-callstate.md) -Meldung an die Anwendung gesendet wird. Die linedisconnectmode- \_ Informationen enthalten Informationen über die Anforderung zum Trennen der Verbindung. Er ist in der [**linecallstatus**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) -Struktur des Aufrufes verfügbar, wenn sich der-Befehl im getrennten Zustand befindet. Während sich ein-Befehl in diesem Zustand befindet, kann die Anwendung die Informationen und den Status des Aufrufes weiterhin Abfragen. Beispielsweise sind Benutzer Benutzerinformationen, die als Teil der Remote Trennung empfangen werden, verfügbar. Die Anwendung kann einen getrennten-Rückruf löschen, indem der-Befehl gelöscht wird.

Aus Gründen der Abwärtskompatibilität liegt es in der Verantwortung des Dienstanbieters, die ausgehandelte API-Version in der Zeile zu untersuchen und diesen linedisconnectmode-Wert nicht zu verwenden, \_ Wenn er von der ausgehandelten Version nicht unterstützt wird (Stattdessen kann "linedisconnectmode \_ Normal" oder "unknown" \_ verwendet werden).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_liniencallstate**](line-callstate.md)
</dt> <dt>

[**Linecallstatus**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)
</dt> <dt>

[**Linedialpara**](/windows/desktop/api/Tapi/ns-tapi-linedialparams)
</dt> </dl>

 

 




