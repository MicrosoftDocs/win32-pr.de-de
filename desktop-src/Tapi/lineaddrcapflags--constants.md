---
description: Die LINEADDRCAPFLAGS-Bitflags-Konstanten werden im \_ dwAddrCapFlags-Member der LINEADDRESSCAPS-Datenstruktur verwendet, um verschiedene Boolesche Adressfunktionen zu beschreiben.
ms.assetid: 530af273-82ba-4310-8aac-266d657e1bfe
title: LINEADDRCAPFLAGS_ Konstanten (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36ee1612c0d57b98a5f3caf82bcd26988fd5d9455c34e5caea5832153af06a50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003118"
---
# <a name="lineaddrcapflags_-constants"></a>LINEADDRCAPFLAGS-Konstanten \_

Die **LINEADDRCAPFLAGS-Bitflags-Konstanten** werden im \_ **dwAddrCapFlags-Member** der [**LINEADDRESSCAPS-Datenstruktur**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) verwendet, um verschiedene Boolesche Adressfunktionen zu beschreiben.

<dl> <dt>

<span id="LINEADDRCAPFLAGS_ACCEPTTOALERT"></span><span id="lineaddrcapflags_accepttoalert"></span>**LINEADDRCAPFLAGS \_ ACCEPTTOALERT**
</dt> <dd> <dl> <dt>



**TRUE,** wenn ein Angebotsaufruf mit [**lineAccept**](/windows/desktop/api/Tapi/nf-tapi-lineaccept) akzeptiert werden muss, um die Benutzer an beiden Enden des Anrufs zu warnen. andernfalls **FALSE**. Dies wird in der Regel nur mit ISDN verwendet.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_ACDGROUP"></span><span id="lineaddrcapflags_acdgroup"></span>**LINEADDRCAPFLAGS \_ ACDGROUP**
</dt> <dd> <dl> <dt>



Die Adresse unterstützt [ACD-Gruppen](about-call-center-controls.md#acd-group-object) in Verbindung mit Callcentervorgängen. Weitere [Informationen zu ACD-Gruppen](./about-call-center-controls.md) finden Sie unter Informationen zu Callcenter-Steuerelementen.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_AUTORECONNECT"></span><span id="lineaddrcapflags_autoreconnect"></span>**LINEADDRCAPFLAGS \_ AUTORECONNECT**
</dt> <dd> <dl> <dt>



Gibt an, ob das Löschen eines Beratungsanrufs automatisch erneut eine Verbindung mit dem Anruf bei der Beratung herstellen soll. **TRUE,** wenn die erneute Verbindung automatisch erfolgt; andernfalls **FALSE**.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_BLOCKIDDEFAULT"></span><span id="lineaddrcapflags_blockiddefault"></span>**LINEADDRCAPFLAGS \_ BLOCKIDDEFAULT**
</dt> <dd> <dl> <dt>



Gibt an, ob das Netzwerk beim Aufrufen dieser Adresse standardmäßig Aufrufer-ID-Informationen sendet oder blockiert. True **gibt an,** dass Bezeichnerinformationen standardmäßig blockiert werden. false **gibt** an, dass Bezeichnerinformationen standardmäßig übertragen werden.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_BLOCKIDOVERRIDE"></span><span id="lineaddrcapflags_blockidoverride"></span>**LINEADDRCAPFLAGS \_ BLOCKIDOVERRIDE**
</dt> <dd> <dl> <dt>



Gibt an, ob die Standardeinstellung zum Senden oder Blockieren von Aufrufer-ID-Informationen pro Aufruf überschrieben werden kann. True **gibt an,** dass eine Außerkraftsetzung möglich ist. bei **FALSE** ist eine Überschreibung nicht möglich.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_COMPLETIONID"></span><span id="lineaddrcapflags_completionid"></span>**LINEADDRCAPFLAGS \_ COMPLETIONID**
</dt> <dd> <dl> <dt>



Gibt an, ob die von [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall) zurückgegebenen Vervollständigungsbezeichner nützlich und eindeutig sind. **TRUE,** wenn nützlich; andernfalls **FALSE**.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_CONFDROP"></span><span id="lineaddrcapflags_confdrop"></span>**LINEADDRCAPFLAGS \_ CONFDROP**
</dt> <dd> <dl> <dt>



**TRUE,** [**wenn lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) in einem übergeordneten Konferenzaufruf auch den Nebeneffekt hat, dass die anderen Am Telefonkonferenz beteiligten Parteien getrennt werden. **FALSE,** wenn das Löschen eines Telefonkonferenzs weiterhin den anderen Parteien ermöglicht, untereinander zu sprechen.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_CONFERENCEHELD"></span><span id="lineaddrcapflags_conferenceheld"></span>**LINEADDRCAPFLAGS \_ CONFERENCE**
</dt> <dd> <dl> <dt>



Gibt an, ob für einen hart gehaltenen Aufruf eine Konferenz durchgeführt werden kann. Häufig können nur Aufrufe zur Beratung als Telefonkonferenz hinzugefügt werden.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_CONFERENCEMAKE"></span><span id="lineaddrcapflags_conferencemake"></span>**LINEADDRCAPFLAGS \_ CONFERENCEMAKE**
</dt> <dd> <dl> <dt>



Gibt an, ob ein völlig neuer Anruf zur Verwendung als Beratungsanruf (zum Hinzufügen) auf der Konferenz eingerichtet werden kann.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_DESTOFFHOOK"></span><span id="lineaddrcapflags_destoffhook"></span>**LINEADDRCAPFLAGS \_ DEOKHOOK**
</dt> <dd> <dl> <dt>



Gibt an, ob das Telefon der aufgerufenen Partei beim Tätigen von Anrufen automatisch einen Offhook erzwingen kann.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_DIALED"></span><span id="lineaddrcapflags_dialed"></span>**LINEADDRCAPFLAGS \_ DIALED**
</dt> <dd> <dl> <dt>



Gibt an, ob bei dieser Adresse eine Zieladresse für einen Anruf gewählt werden kann. **TRUE,** wenn eine Zieladresse gewählt werden muss; **FALSE,** wenn die Zieladresse fest ist (wie bei einem "hot phone").


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDBUSYNAADDR"></span><span id="lineaddrcapflags_fwdbusynaaddr"></span>**LINEADDRCAPFLAGS \_ FWDBUSYNAADDR**
</dt> <dd> <dl> <dt>



Gibt an, ob die Anrufweiterleitung für ausgelastet und für keine Antwort unterschiedliche Weiterleitungsadressen verwenden kann. Dieses Flag ist nur sinnvoll, wenn die Weiterleitung für ausgelastet und für keine Antwort separat gesteuert werden kann. Dieses Flag ist **TRUE,** wenn für die Weiterleitung für ausgelastet und für keine Antwort unterschiedliche Zieladressen verwendet werden können. Andernfalls ist dies **FALSE.**


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDCONSULT"></span><span id="lineaddrcapflags_fwdconsult"></span>**LINEADDRCAPFLAGS \_ FWDCONSULT**
</dt> <dd> <dl> <dt>



Gibt an, ob die Anrufweiterleitung die Einrichtung eines Beratungsanrufs umfasst.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDINTEXTADDR"></span><span id="lineaddrcapflags_fwdintextaddr"></span>**LINEADDRCAPFLAGS \_ FWDINTEXTADDR**
</dt> <dd> <dl> <dt>



Gibt an, ob interne und externe Aufrufe an verschiedene Weiterleitungsadressen weitergeleitet werden können. Dieses Flag ist nur sinnvoll, wenn die Weiterleitung interner und externer Aufrufe separat gesteuert werden kann. Dieses Flag ist **TRUE,** wenn interne und externe Aufrufe an verschiedene Zieladressen weitergeleitet werden können. Andernfalls ist dies **FALSE.**


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDNUMRINGS"></span><span id="lineaddrcapflags_fwdnumrings"></span>**LINEADDRCAPFLAGS \_ FWDNUMRINGS**
</dt> <dd> <dl> <dt>



Gibt an, ob die Anzahl der Ringe für eine Antwort ohne Antwort angegeben werden kann, wenn Aufrufe ohne Antwort weiterleitet werden. True **gibt** an, dass der gültige Bereich in den **Membern dwMinFwdNumRings** und **dwMaxFwdNumRings** der [**LINEADDRESSCAPS-Struktur**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) angegeben wird.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDSTATUSVALID"></span><span id="lineaddrcapflags_fwdstatusvalid"></span>**LINEADDRCAPFLAGS \_ FWDSTATUSVALID**
</dt> <dd> <dl> <dt>



Gibt an, ob der Weiterleitungsstatus in der [**LINEADDRESSSTATUS-Struktur**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) für diese Adresse gültig ist oder bei fehlender genauer Bestätigung durch den Switch oder das Netzwerk eine "beste Schätzung" ist.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_HOLDMAKESNEW"></span><span id="lineaddrcapflags_holdmakesnew"></span>**LINEADDRCAPFLAGS \_ HOLDMAKESNEW**
</dt> <dd> <dl> <dt>



Wenn ein Aufruf für diese Adresse zurückhalten wird (mithilfe von [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) oder einer externen Aktion), wird automatisch ein neuer Aufruf erstellt (höchstwahrscheinlich in LINECALLSTATE \_ DIALTONE).


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_NOEXTERNALCALLS"></span><span id="lineaddrcapflags_noexternalcalls"></span>**LINEADDRCAPFLAGS \_ NOEXTERNALCALLS**
</dt> <dd> <dl> <dt>



Die Adresse ist einer internen Zeile in einer PBX-Datei zugeordnet, die so eingeschränkt ist, dass sie nicht verwendet werden kann, um Aufrufe an eine Adresse außerhalb des Switches zu tätigen (z. B. eine Intercom). Die Anwendung kann diesen Hinweis verwenden, um den Benutzer bei der Auswahl der richtigen Aufrufe zu unterstützen, die für einen Aufruf verwendet werden soll. Wenn dieses Bit deaktiviert ist, bedeutet dies nicht unbedingt, dass die Adresse für externe Aufrufe verwendet werden kann, da der Dienstanbieter den Zeilentyp möglicherweise nicht kennt.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_NOINTERNALCALLS"></span><span id="lineaddrcapflags_nointernalcalls"></span>**LINEADDRCAPFLAGS \_ NOINTERNALCALLS**
</dt> <dd> <dl> <dt>



Die Adresse ist einer direkten CO-Leitung (Trunk) zugeordnet und kann nicht verwendet werden, um interne Aufrufe für eine PBX-Datei zu tätigen. Die Anwendung kann diesen Hinweis verwenden, um den Benutzer bei der Auswahl der richtigen Aufrufe zu unterstützen, die für einen Aufruf verwendet werden soll. Wenn dieses Bit deaktiviert ist, bedeutet dies nicht unbedingt, dass die Adresse für interne Aufrufe verwendet werden kann, da der Dienstanbieter den Zeilentyp möglicherweise nicht kennt.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_NOPSTNADDRESSTRANSLATION"></span><span id="lineaddrcapflags_nopstnaddresstranslation"></span>**LINEADDRCAPFLAGS \_ NOPSTNADDRESSTRANSLATION**
</dt> <dd> <dl> <dt>



Diese Adresse unterstützt nicht die Übersetzung von öffentlichen Telefonnetzwerkadressen. Dieses Flag wird nur für Anwendungen verfügbar gemacht, die eine TAPI-Version von 3.0 oder höher aushandeln.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_ORIGOFFHOOK"></span><span id="lineaddrcapflags_origoffhook"></span>**LINEADDRCAPFLAGS \_ ORIGOFFHOOK**
</dt> <dd> <dl> <dt>



Gibt an, ob das Telefon der ursprünglichen Partei beim Tätigen von Anrufen automatisch von einem Offhook abgeschaltet werden kann.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_PARTIALDIAL"></span><span id="lineaddrcapflags_partialdial"></span>**LINEADDRCAPFLAGS \_ PARTIALDIAL**
</dt> <dd> <dl> <dt>



Gibt an, ob teilwählbar ist.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_PICKUPCALLWAIT"></span><span id="lineaddrcapflags_pickupcallwait"></span>**LINEADDRCAPFLAGS \_ PICKUPCALLWAIT**
</dt> <dd> <dl> <dt>



**TRUE,** [**wenn linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) verwendet werden kann, um einen vom Benutzer erkannten Aufruf als Anrufwarteaufruf zu erfassen. andernfalls **FALSE**.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_PICKUPGROUPID"></span><span id="lineaddrcapflags_pickupgroupid"></span>**LINEADDRCAPFLAGS \_ PICKUPGROUPID**
</dt> <dd> <dl> <dt>



Gibt an, ob ein Gruppenbezeichner für die Abholung durch den Anruf erforderlich ist.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_PREDICTIVEDIALER"></span><span id="lineaddrcapflags_predictivedialer"></span>**LINEADDRCAPFLAGS \_ PREDICTIVEDIALER**
</dt> <dd> <dl> <dt>



Diese Adresse verfügt über erweiterte Funktionen zur Überwachung des Anruffortschritts, die auf ausgehende Aufrufe angewendet werden können, um Anrufzustände wie *Ringback,* Ausgelastet,  *SpecialInfo* und verbunden oder den Medientyp des Geräts zu bestimmen, das den Anruf beantwortet. Es kann auch die Möglichkeit haben, ausgehende Aufrufe automatisch an eine andere Adresse zu übertragen, wenn ein Aufruf einen vordefinierten Satz von Zuzuständen erreicht.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_QUEUE"></span><span id="lineaddrcapflags_queue"></span>**LINEADDRCAPFLAGS-WARTESCHLANGE \_**
</dt> <dd> <dl> <dt>



Diese Adresse ist nicht mit einer bestimmten Station oder einem physischen Gerät verknüpft, sondern ist ein Halteort, an dem Aufrufe auf die weitere Verarbeitung warten. Die in der Warteschlange platzierten Aufrufe können eine bestimmte Behandlung erhalten. Sie können auch automatisch übertragen werden, wenn eine bestimmte Ressource verfügbar wird (z. B. wenn die Warteschlange eine ACD-Warteschlange ist und Aufrufe auf einen verfügbaren Agent warten).


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_ROUTEPOINT"></span><span id="lineaddrcapflags_routepoint"></span>**LINEADDRCAPFLAGS-ROUTENPUNKT \_**
</dt> <dd> <dl> <dt>



Diese Adresse ist nicht einer bestimmten Station oder einem physischen Gerät zugeordnet, sondern ist ein Ort, an dem Aufrufe auf die Weiterleitung durch die Anwendung warten (die Anwendung untersucht die aufgerufene Adresse und kann den Aufruf an eine andere Adresse umleiten). Der Aufruf kann auch automatisch übertragen werden, wenn ein Routing-Timeout abläuft (der Switch geht in der Regel von einem Standardrouting aus).


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_SECURE"></span><span id="lineaddrcapflags_secure"></span>**LINEADDRCAPFLAGS \_ SECURE**
</dt> <dd> <dl> <dt>



Gibt an, ob Aufrufe dieser Adresse zum Zeitpunkt der Aufrufeinrichtung sicher gemacht werden können.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_SETCALLINGID"></span><span id="lineaddrcapflags_setcallingid"></span>**LINEADDRCAPFLAGS \_ SETCALLINGID**
</dt> <dd> <dl> <dt>



Die Anwendung kann beim Aufrufen von [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) und anderen Funktionen, die eine **LINECALLPARAMS-Struktur** akzeptieren, das **CallingPartyID-Member** in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) festlegen. Wenn der Inhalt des Bezeichners akzeptabel ist und ein Pfad verfügbar ist, über gibt der Dienstanbieter den Bezeichner an die aufgerufene Partei weiter, um die Identität der aufrufenden Partei anzugeben.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_SETUPCONFNULL"></span><span id="lineaddrcapflags_setupconfnull"></span>**LINEADDRCAPFLAGS \_ SETUPCONFNULL**
</dt> <dd> <dl> <dt>



Gibt an, ob die Einrichtung eines Konferenzaufrufs mit einem ersten Aufruf (**FALSE**) oder ohne anfänglichen Aufruf ( TRUE )**beginnt.**


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_TRANSFERHELD"></span><span id="lineaddrcapflags_transferheld"></span>**LINEADDRCAPFLAGS \_ TRANSFER WIES**
</dt> <dd> <dl> <dt>



Gibt an, ob ein harter Aufruf übertragen werden kann. Häufig können nur Aufrufe der Beratung über die Beratung übertragen werden.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_TRANSFERMAKE"></span><span id="lineaddrcapflags_transfermake"></span>**LINEADDRCAPFLAGS \_ TRANSFERMAKE**
</dt> <dd> <dl> <dt>



Gibt an, ob ein völlig neuer Anruf zur Verwendung als Beratungsanruf bei der Übertragung eingerichtet werden kann.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**lineAccept**](/windows/desktop/api/Tapi/nf-tapi-lineaccept)
</dt> <dt>

[**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)
</dt> <dt>

[**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)
</dt> <dt>

[**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop)
</dt> <dt>

[**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold)
</dt> <dt>

[**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup)
</dt> </dl>

 

