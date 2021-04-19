---
description: Die \_ Bit-Flag-Konstanten von lineaddrcapflags werden im dwaddrcapflags-Member der lineaddresscaps-Datenstruktur verwendet, um verschiedene boolesche Adress Funktionen zu beschreiben.
ms.assetid: 530af273-82ba-4310-8aac-266d657e1bfe
title: LINEADDRCAPFLAGS_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27ce6c8bebb5683d5ecb7d576ff7d376ad0d62cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369474"
---
# <a name="lineaddrcapflags_-constants"></a>Lineaddrcapflags- \_ Konstanten

Die Bit-Flag-Konstanten von **lineaddrcapflags** \_ werden im **dwaddrcapflags** -Member der [**lineaddresscaps**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) -Datenstruktur verwendet, um verschiedene boolesche Adress Funktionen zu beschreiben.

<dl> <dt>

<span id="LINEADDRCAPFLAGS_ACCEPTTOALERT"></span><span id="lineaddrcapflags_accepttoalert"></span>**lineaddrcapflags " \_ akzepttoalert"**
</dt> <dd> <dl> <dt>



**True** , wenn ein Angebots Befehl mithilfe von [**lineaccept**](/windows/desktop/api/Tapi/nf-tapi-lineaccept) akzeptiert werden muss, um zu beginnen, die Benutzer an beiden Enden des Aufrufens zu warnen. andernfalls **false**. Dies wird in der Regel nur mit ISDN verwendet.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_ACDGROUP"></span><span id="lineaddrcapflags_acdgroup"></span>**lineaddrcapflags- \_ acdgroup**
</dt> <dd> <dl> <dt>



Die Adresse unterstützt [ACD-Gruppen](about-call-center-controls.md#acd-group-object) in Verbindung mit callcentervorgängen. Weitere Informationen zu ACD-Gruppen finden Sie unter Informationen [zu Callcenter](./about-call-center-controls.md) -Steuerelementen.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_AUTORECONNECT"></span><span id="lineaddrcapflags_autoreconnect"></span>**lineaddrcapflags \_ autoReconnect**
</dt> <dd> <dl> <dt>



Gibt an, ob durch das Löschen eines Beratungs Aufrufes bei der Beratungs Aufbewahrung automatisch erneut eine Verbindung mit dem Rückruf **True** , wenn die erneute Verbindungs Herstellung automatisch erfolgt. andernfalls **false**.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_BLOCKIDDEFAULT"></span><span id="lineaddrcapflags_blockiddefault"></span>**lineaddrcapflags \_ blockiddefault**
</dt> <dd> <dl> <dt>



Gibt an, ob das Netzwerk bei einem Aufruf für diese Adresse standardmäßig Aufrufer-ID-Informationen sendet oder blockiert. **True** gibt an, dass die Bezeichnerinformationen standardmäßig blockiert werden. bei " **false**" werden standardmäßig die Bezeichnerinformationen übertragen.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_BLOCKIDOVERRIDE"></span><span id="lineaddrcapflags_blockidoverride"></span>**lineaddrcapflags \_ blockidoverride**
</dt> <dd> <dl> <dt>



Gibt an, ob die Standardeinstellung für das Senden oder Blockieren von Aufrufer-ID-Informationen pro Aufruf überschrieben werden kann. **True** gibt an, dass außer Kraft Setzung möglich ist. **false** gibt an, dass außer Kraft Setzung nicht möglich ist.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_COMPLETIONID"></span><span id="lineaddrcapflags_completionid"></span>**completionid für lineaddrcapflags \_**
</dt> <dd> <dl> <dt>



Gibt an, ob die von [**linecompletecallzurück**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall) gegebenen Vervollständigungs-IDs nützlich und eindeutig sind. **True** , wenn nützlich; andernfalls **false**.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_CONFDROP"></span><span id="lineaddrcapflags_confdrop"></span>**"lineaddrcapflags" ( \_ confdrop)**
</dt> <dd> <dl> <dt>



" **True** ", wenn " [**linedrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) " bei einem übergeordneten Konferenzgespräch auch den Nebeneffekt hat, dass die anderen Parteien, die am Konferenzgespräch beteiligt sind, gelöscht werden sollen. " **False** ", wenn durch das Löschen eines Konferenz Aufrufes den anderen Parteien weiterhin untereinander gesprochen werden kann.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_CONFERENCEHELD"></span><span id="lineaddrcapflags_conferenceheld"></span>**lineaddrcapflags- \_ conferenceheld**
</dt> <dd> <dl> <dt>



Gibt an, ob ein hart gehaltene-Befehl an die übertragen werden kann. Häufig können nur Aufrufe der Beratungs Aufbewahrung als Konferenz Aufruf hinzugefügt werden.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_CONFERENCEMAKE"></span><span id="lineaddrcapflags_conferencemake"></span>**lineaddrcapflags- \_ conferencemake**
</dt> <dd> <dl> <dt>



Gibt an, ob ein vollständig neuer-Rückruf für die Verwendung als Rückruf (zum Hinzufügen) auf der Konferenz erstellt werden kann.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_DESTOFFHOOK"></span><span id="lineaddrcapflags_destoffhook"></span>**lineaddrcapflags \_ destoffhook**
</dt> <dd> <dl> <dt>



Gibt an, ob das Telefon der angerufenen Partei beim Ausführen von Aufrufen automatisch erzwungen werden kann.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_DIALED"></span><span id="lineaddrcapflags_dialed"></span>**lineaddrcapflags \_ gewählt**
</dt> <dd> <dl> <dt>



Gibt an, ob eine Zieladresse für diese Adresse für einen-Rückruf gewählt werden kann. **True** , wenn eine Zieladresse gewählt werden muss. **False** , wenn die Zieladresse (wie bei einem "heißen Telefon") korrigiert ist.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDBUSYNAADDR"></span><span id="lineaddrcapflags_fwdbusynaaddr"></span>**lineaddrcapflags ( \_ f)**
</dt> <dd> <dl> <dt>



Gibt an, ob die Anrufweiterleitung für ausgelastet und für keine Antwort unterschiedliche Weiterleitungs Adressen verwenden kann. Dieses Flag ist nur dann von Bedeutung, wenn die Weiterleitung für ausgelastet und keine Antwort separat gesteuert werden kann. Dieses Flag ist **true** , wenn die Weiterleitung für ausgelastet und keine Antwort unterschiedliche Zieladressen verwenden kann. Andernfalls ist Sie **false**.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDCONSULT"></span><span id="lineaddrcapflags_fwdconsult"></span>**lineaddrcapflags ( \_ f)**
</dt> <dd> <dl> <dt>



Gibt an, ob die aufrufweiterleitung die Einrichtung eines Beratungs Aufrufens einschließt.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDINTEXTADDR"></span><span id="lineaddrcapflags_fwdintextaddr"></span>**lineaddrcapflags, \_ f.**
</dt> <dd> <dl> <dt>



Gibt an, ob interne und externe Aufrufe an verschiedene Weiterleitungs Adressen weitergeleitet werden können. Dieses Flag ist nur sinnvoll, wenn die Weiterleitung interner und externer Aufrufe separat gesteuert werden kann. Dieses Flag ist **true** , wenn interne und externe Aufrufe an verschiedene Zieladressen weitergeleitet werden können. Andernfalls ist Sie **false**.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDNUMRINGS"></span><span id="lineaddrcapflags_fwdnumrings"></span>**lineaddrcapflags-" \_ f"**
</dt> <dd> <dl> <dt>



Gibt an, ob die Anzahl der Ringe für eine Antwort ohne Antwort angegeben werden kann, wenn Aufrufe ohne Antwort weitergeleitet werden. Wenn der Wert **true** ist, wird der gültige Bereich in den Elementen **dwminfwdnumrings** und **dwmaxfwdnumrings** der [**lineaddresscaps**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) -Struktur bereitgestellt.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDSTATUSVALID"></span><span id="lineaddrcapflags_fwdstatusvalid"></span>**lineaddrcapflags \_ fwdstatus valid**
</dt> <dd> <dl> <dt>



Gibt an, ob der Weiterleitungs Status in der [**lineaddressstatus**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) -Struktur für diese Adresse gültig ist oder höchstens eine "beste Schätzung" ist, weil keine genaue Bestätigung durch den Switch oder das Netzwerk vorliegt.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_HOLDMAKESNEW"></span><span id="lineaddrcapflags_holdmakesnew"></span>**lineaddrcapflags \_ holdmakesnew**
</dt> <dd> <dl> <dt>



Wenn ein Anruf für diese Adresse angehalten wird (mit [**linehold**](/windows/desktop/api/Tapi/nf-tapi-linehold) oder externer Aktion), wird automatisch ein neuer Anruf erstellt (höchstwahrscheinlich in linecallstate \_ Dialtone).


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_NOEXTERNALCALLS"></span><span id="lineaddrcapflags_noexternalcalls"></span>**lineaddrcapflags \_ noexternalcalls**
</dt> <dd> <dl> <dt>



Die Adresse ist einer internen Zeile in einer PBX zugeordnet, die so eingeschränkt ist, dass Sie nicht zum Platzieren von Anrufen an eine Adresse außerhalb des Schalters verwendet werden kann (z. b. eine Gegenseite). Die Anwendung kann diese Angabe verwenden, um dem Benutzer zu helfen, die richtige aufrufdarstellung auszuwählen, die zum Ausführen eines Aufrufens verwendet werden soll. Wenn dieses Bit deaktiviert ist, gibt es nicht notwendigerweise an, dass die Adresse zum Ausführen externer Aufrufe verwendet werden kann, da der Dienstanbieter möglicherweise nicht der Typ der Zeile ist.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_NOINTERNALCALLS"></span><span id="lineaddrcapflags_nointernalcalls"></span>**lineaddrcapflags \_ nointernalcalls**
</dt> <dd> <dl> <dt>



Die Adresse ist einer direkten Co-Linie (trunk) zugeordnet und kann nicht verwendet werden, um interne Aufrufe an eine PBX durchführen. Die Anwendung kann diese Angabe verwenden, um dem Benutzer zu helfen, die richtige aufrufdarstellung auszuwählen, die zum Ausführen eines Aufrufens verwendet werden soll. Wenn dieses Bit deaktiviert ist, gibt es nicht notwendigerweise an, dass die Adresse verwendet werden kann, um interne Aufrufe durchzuführen, da der Dienstanbieter möglicherweise nicht dem Zeittyp entspricht.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_NOPSTNADDRESSTRANSLATION"></span><span id="lineaddrcapflags_nopstnaddresstranslation"></span>**lineaddrcapflags \_ nopstnadresssstranslations**
</dt> <dd> <dl> <dt>



Diese Adresse unterstützt keine Übersetzung der öffentlichen, übersetzte Telefon Netzwerkadresse. Dieses Flag ist nur für Anwendungen verfügbar, die eine TAPI-Version von 3,0 oder höher aushandeln.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_ORIGOFFHOOK"></span><span id="lineaddrcapflags_origoffhook"></span>**lineaddrcapflags \_ origoffhook**
</dt> <dd> <dl> <dt>



Gibt an, ob das Telefon der Ursprungs Partei beim Ausführen von Aufrufen automatisch als OFFHOOK verwendet werden kann.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_PARTIALDIAL"></span><span id="lineaddrcapflags_partialdial"></span>**lineaddrcapflags- \_ partialdial**
</dt> <dd> <dl> <dt>



Gibt an, ob partielle Wählbarkeit verfügbar ist.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_PICKUPCALLWAIT"></span><span id="lineaddrcapflags_pickupcallwait"></span>**lineaddrcapflags \_ pickupcallwait**
</dt> <dd> <dl> <dt>



" **True** ", wenn " [**linepickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) " verwendet werden kann, um einen vom Benutzer erkannten Befehl als Aufrufe aufzurufen. andernfalls **false**.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_PICKUPGROUPID"></span><span id="lineaddrcapflags_pickupgroupid"></span>**lineaddrcapflags \_ pickupgroupid**
</dt> <dd> <dl> <dt>



Gibt an, ob eine Gruppen-ID für die aufrufabholung erforderlich ist.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_PREDICTIVEDIALER"></span><span id="lineaddrcapflags_predictivedialer"></span>**lineaddrcapflags \_ predictivedialer**
</dt> <dd> <dl> <dt>



Diese Adresse verfügt über erweiterte Überwachungsfunktionen zum Aufrufen des Status, die auf ausgehende Aufrufe angewendet werden können, um Aufruf Zustände, wie z. b. " *geben*", " *ausgelastet*", " *specialinfo*" und " *verbunden*", oder den Medientyp des Geräts zu bestimmen Sie kann auch die Möglichkeit haben, ausgehende Aufrufe automatisch an eine andere Adresse zu übertragen, wenn ein Aufruf einen vordefinierten Satz von Zuständen erreicht.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_QUEUE"></span><span id="lineaddrcapflags_queue"></span>**lineaddrcapflags- \_ Warteschlange**
</dt> <dd> <dl> <dt>



Diese Adresse ist nicht mit einer bestimmten Station oder einem physischen Gerät verknüpft, sondern ist eine Position, an der Anrufe auf eine weitere Verarbeitung warten. Die in der Warteschlange platzierten Aufrufe können eine bestimmte Behandlung erhalten. Sie können auch automatisch übertragen werden, wenn eine bestimmte Ressource verfügbar wird (z. b. wenn es sich bei der Warteschlange um eine ACD-Warteschlange handelt und Aufrufe auf einen verfügbaren Agent warten).


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_ROUTEPOINT"></span><span id="lineaddrcapflags_routepoint"></span>**lineaddrcapflags- \_ Routepoint**
</dt> <dd> <dl> <dt>



Diese Adresse ist nicht mit einer bestimmten Station oder einem physischen Gerät verknüpft, sondern ist eine Anlaufstelle, an der Anrufe auf das Routing durch die Anwendung warten (die Anwendung überprüft die aufgerufene Adresse und kann den Aufruf an eine andere Adresse umleiten). Der-Befehl kann auch automatisch übertragen werden, wenn ein Routing Timeout abläuft (der Switch nimmt normalerweise ein Standard Routing an).


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_SECURE"></span><span id="lineaddrcapflags_secure"></span>**lineaddrcapflags \_ sicher**
</dt> <dd> <dl> <dt>



Gibt an, ob Aufrufe für diese Adresse zum Zeitpunkt des Aufrufs der Einrichtung sicher gemacht werden können.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_SETCALLINGID"></span><span id="lineaddrcapflags_setcallingid"></span>**lineaddrcapflags \_ setcallingid**
</dt> <dd> <dl> <dt>



Die Anwendung kann festlegen, dass das **callingpartyid** -Element beim Aufrufen von [**linemakecall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) und anderen Funktionen, die eine **linecallparameterstruktur** akzeptieren, in [**linecallpara**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) Metern festgelegt wird. Wenn der Inhalt des Bezeichners akzeptabel und ein Pfad verfügbar ist, übergibt der Dienstanbieter den Bezeichner an die aufgerufene Partei, um die Identität der aufrufenden Partei anzugeben.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_SETUPCONFNULL"></span><span id="lineaddrcapflags_setupconfnull"></span>**lineaddrcapflags \_ setupconfnull**
</dt> <dd> <dl> <dt>



Gibt an, ob das Einrichten eines Konferenz Aufrufes mit einem ersten-Befehl (**false**) oder ohne ersten-Rückruf (**true**) beginnt.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_TRANSFERHELD"></span><span id="lineaddrcapflags_transferheld"></span>**lineaddrcapflags \_ transferlake**
</dt> <dd> <dl> <dt>



Gibt an, ob ein hart gehaltene-Rückruf übertragen werden kann. Häufig können nur Aufrufe der Beratungs Aufbewahrung übertragen werden.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_TRANSFERMAKE"></span><span id="lineaddrcapflags_transfermake"></span>**lineaddrcapflags \_ transfermake**
</dt> <dd> <dl> <dt>



Gibt an, ob ein vollständig neuer-aufrufbedarf zur Verwendung als bei der Übertragung verwendetes Gespräch eingerichtet werden kann


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

[**lineaccept**](/windows/desktop/api/Tapi/nf-tapi-lineaccept)
</dt> <dt>

[**Lineaddresscaps**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**Lineaddressstatus**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[**Linecallparametriams**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)
</dt> <dt>

[**linecompletecall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)
</dt> <dt>

[**linedrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop)
</dt> <dt>

[**linehold**](/windows/desktop/api/Tapi/nf-tapi-linehold)
</dt> <dt>

[**linemakecall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[**linepickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup)
</dt> </dl>

 

