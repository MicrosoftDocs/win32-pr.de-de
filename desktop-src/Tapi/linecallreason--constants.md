---
description: Die linecallreason \_ -bitflagkonstanten beschreiben den Grund für einen-Befehl.
ms.assetid: 16278146-886f-433a-afe5-64f4894b1428
title: LINECALLREASON_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab6d2411c652c13add1620ca6029cabbf2b878e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358239"
---
# <a name="linecallreason_-constants"></a>Linecallreason- \_ Konstanten

Die **linecallreason \_** -bitflagkonstanten beschreiben den Grund für einen-Befehl.

<dl> <dt>

<span id="LINECALLREASON_CALLCOMPLETION"></span><span id="linecallreason_callcompletion"></span>**linecallreason \_ callcompletion**
</dt> <dd> <dl> <dt>



Der-Befehl war das Ergebnis einer Anforderung zum Abschluss des Aufrufes.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_CAMPEDON"></span><span id="linecallreason_campedon"></span>**linecallreason \_ campep**
</dt> <dd> <dl> <dt>



Der-Befehl wurde für die Adresse gecampt. Normalerweise wird Sie anfänglich im OnHold-Zustand angezeigt und kann mithilfe von [**lineswaphold**](/windows/desktop/api/Tapi/nf-tapi-lineswaphold)auf gewechselt werden. Wenn ein aktiver-Vorgang in den Leerlauf wechselt, kann der gefragte-Befehl in den Angebots Status wechseln, und das Gerät beginnt mit dem Klingeln.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_DIRECT"></span><span id="linecallreason_direct"></span>**linecallreason \_ Direct**
</dt> <dd> <dl> <dt>



Dabei handelt es sich um einen direkten oder ausgehenden-Rückruf.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_FWDBUSY"></span><span id="linecallreason_fwdbusy"></span>**linecallreason \_ f wdbusy**
</dt> <dd> <dl> <dt>



Dieser Aufruf wurde von einer anderen Erweiterung weitergeleitet, die zum Zeitpunkt des Aufrufes ausgelastet war.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_FWDNOANSWER"></span><span id="linecallreason_fwdnoanswer"></span>**linecallreason \_ f wdnoanswer**
</dt> <dd> <dl> <dt>



Der Anruf wurde von einer anderen Erweiterung weitergeleitet, die den Anruf nach einigen Ringen nicht beantwortet hat.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_FWDUNCOND"></span><span id="linecallreason_fwduncond"></span>**linecallreason \_ f wdund**
</dt> <dd> <dl> <dt>



Der-Befehl wurde von einer anderen Zahl uneingeschränkt weitergeleitet.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_INTRUDE"></span><span id="linecallreason_intrude"></span>**linecallreason \_ Intrude**
</dt> <dd> <dl> <dt>



Der Aufruf wurde in die Zeile eingedrungen, entweder durch eine Aktion zum Aufrufen des Vorgangs, die durch eine andere Station oder durch eine Operator Aktion aufgerufen wurde. Abhängig von der Switch-Implementierung kann der-Befehl entweder im verbundenen Zustand oder mit einem vorhandenen aktiven-Befehl in der Zeile angezeigt werden.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_PARKED"></span><span id="linecallreason_parked"></span>**linecallreason ist \_ geparkt.**
</dt> <dd> <dl> <dt>



Der-Befehl wurde für die Adresse geparkt. Normalerweise wird Sie anfänglich im OnHold-Zustand angezeigt.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_PICKUP"></span><span id="linecallreason_pickup"></span>**linecallreason \_ Pickup**
</dt> <dd> <dl> <dt>



Der-Befehl wurde aus einer anderen Erweiterung abgerufen.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_REDIRECT"></span><span id="linecallreason_redirect"></span>**linecallreason- \_ Umleitung**
</dt> <dd> <dl> <dt>



Der-Befehl wurde an diese Station umgeleitet.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_REMINDER"></span><span id="linecallreason_reminder"></span>**linecallreason- \_ Erinnerung**
</dt> <dd> <dl> <dt>



Der Aufruf ist eine Erinnerung (oder "Rückruf"), für die der Benutzer einen Aufruf hat oder für (potenziell) eine lange Zeit hält.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_ROUTEREQUEST"></span><span id="linecallreason_routerequest"></span>**linecallreason \_ RouteRequest**
</dt> <dd> <dl> <dt>



Der-Befehl wird für die Adresse angezeigt, da der Switch Weiterleitungs Anweisungen aus der Anwendung benötigt. Die Anwendung sollte das **calledid** -Element in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)untersuchen und die [**lineredirect**](/windows/desktop/api/Tapi/nf-tapi-lineredirect) -Funktion verwenden, um eine neue, für den Aufruf angeforderte Adresse anzugeben. Wenn der-Befehl stattdessen blockiert werden soll, ruft die Anwendung möglicherweise [**linedrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop)auf. Wenn die Anwendung innerhalb eines von einem Switch definierten Timeout Zeitraums keine Maßnahmen ergreifen kann, wird eine Standardaktion ausgeführt. Ein Dienstanbieter kann diese Konstante nur verwenden, wenn die ausgehandelte Version in der Zeile 2,0 oder höher ist. Andernfalls sollte der Dienstanbieter den linecallreason- \_ nicht Gebrauch ersetzen.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_TRANSFER"></span><span id="linecallreason_transfer"></span>**linecallreason- \_ Übertragung**
</dt> <dd> <dl> <dt>



Der-Befehl wurde von einer anderen Zahl übertragen.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_UNAVAIL"></span><span id="linecallreason_unavail"></span>**linecallreason \_ nicht erreichbar**
</dt> <dd> <dl> <dt>



Der Grund für den-Aufrufvorgang ist nicht verfügbar und wird später noch nicht bekannt werden.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_UNKNOWN"></span><span id="linecallreason_unknown"></span>**linecallreason \_ unbekannt**
</dt> <dd> <dl> <dt>



Der Grund für den-aufrufsvorgang ist derzeit unbekannt, kann aber später bekannt werden.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_UNPARK"></span><span id="linecallreason_unpark"></span>**linecallreason \_ unpark**
</dt> <dd> <dl> <dt>



Der-Rückruf wurde als geparkter-Befehl abgerufen.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

Die linecallreason- \_ Konstanten werden im **dwReason** -Member der [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) -Datenstruktur verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)
</dt> <dt>

[**linedrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop)
</dt> <dt>

[**lineredirect**](/windows/desktop/api/Tapi/nf-tapi-lineredirect)
</dt> <dt>

[**lineswaphold**](/windows/desktop/api/Tapi/nf-tapi-lineswaphold)
</dt> </dl>

 

 




