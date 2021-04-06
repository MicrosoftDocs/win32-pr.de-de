---
title: Rtmregisterclient-Funktion (RTM. h)
description: Die Funktion rtmregisterclient registriert einen Client als Handler für das angegebene Protokoll. Er richtet einen Weiterleitungs Änderungs Benachrichtigungs Mechanismus für den Client ein und legt Protokoll Optionen fest.
ms.assetid: 70426601-695d-47ed-b71a-1df3fb8ddf10
keywords:
- Rtmregisterclient-Funktion (RAS)
topic_type:
- apiref
api_name:
- RtmRegisterClient
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 564f47e68fd6cdce3d5437fe184bac1ed74d8322
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743112"
---
# <a name="rtmregisterclient-function"></a>Rtmregisterclient-Funktion

\[Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar. Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.\]

Die Funktion **rtmregisterclient** registriert einen Client als Handler für das angegebene Protokoll. Er richtet einen Weiterleitungs Änderungs Benachrichtigungs Mechanismus für den Client ein und legt Protokoll Optionen fest.

## <a name="syntax"></a>Syntax


```C++
HANDLE RtmRegisterClient(
  _In_ DWORD  ProtocolFamily,
  _In_ DWORD  RoutingProtocol,
  _In_ HANDLE ChangeEvent,
  _In_ DWORD  Flags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ProtocolFamily* \[ in\]
</dt> <dd>

Gibt die Protokollfamilie des zu registrierenden Routing Protokolls an.

</dd> <dt>

*Routingprotocol* \[ in\]
</dt> <dd>

Gibt die Routing Protokoll-ID an, die mit der übereinstimmen, die bei der Registrierung beim routermanager verwendet wird. Siehe [**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol).

</dd> <dt>

*ChangeEvent* \[ in\]
</dt> <dd>

Gibt an, dass sich die beste Route zu einem Netzwerk in der Tabelle geändert hat. Der Routing Tabellen-Manager signalisiert dieses Ereignis nach einer Änderung an der optimalen Route zu einem beliebigen Netzwerk in der Tabelle. Weitere Informationen zur Weiterleitung von Änderungs Benachrichtigungen finden Sie unter [**rtmdequeueroutechangemess**](rtmdequeueroutechangemessage.md) .

Dieser Parameter ist optional. Wenn der Aufrufer **null** für diesen Parameter angibt, benachrichtigt der Routing Tabellen-Manager den Client über Änderungen am besten Routen Status.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Gibt verschiedene Optionen für die spezielle Behandlung des Routing Protokolls an. Der folgende Wert wird derzeit unterstützt.



| Flags                                                                                                                                                                                               | Bedeutung                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_PROTOCOL_SINGLE_ROUTE"></span><span id="rtm_protocol_single_route"></span><dl> <dt>**RTM- \_ Protokoll- \_ einzelne \_ Route**</dt> </dl> | Der Routing Tabellen-Manager behält nur eine Route pro Zielnetzwerk für das Routing Protokoll bei. Mit anderen Worten: der Routing Tabellen-Manager ersetzt Routen Einträge, die dieselben Zielnetzwerk Nummern aufweisen, anstatt neue hinzuzufügen.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei erfolgreicher Rückgabe ein **handle** -Wert, der den Client in nachfolgenden Aufrufen des Routing Tabellen-Managers identifiziert.

Ein **null** -handle gibt an, dass der Routing Tabellen-Manager den Client nicht registrieren konnte. Rufen Sie [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf, um den Grund für den Fehler zu erhalten.



| Wert                                                                                                         | BESCHREIBUNG                                                                                     |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**der Fehler \_ Client ist \_ bereits \_ vorhanden.**</dt> </dl> | Ein anderer Client hat sich bereits für die Verarbeitung des angegebenen Protokolls registriert.<br/>              |
| <dl> <dt>**Fehler bei \_ ungültigem \_ Parameter**</dt> </dl>      | Die angegebene Protokollfamilie wird nicht unterstützt, oder der *Flags* -Parameter ist ungültig.<br/> |
| <dl> <dt>**Fehler \_ keine \_ System \_ Ressourcen**</dt> </dl>   | Nicht genügend Ressourcen, um den Vorgang auszuführen.<br/>                                   |
| <dl> <dt>**Fehler \_ nicht \_ genügend Arbeits \_ Speicher**</dt> </dl>     | Nicht genügend Arbeitsspeicher zum Zuordnen von Datenstrukturen für den Client.<br/>                      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                     |
| Header<br/>                   | <dl> <dt>RTM. h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>RTM. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Rtm.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Referenz für Routing Tabellen-Manager Version 1](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Funktionen der Routing-Tabellen-Manager-Version 1](routing-table-manager-version-1-functions.md)
</dt> <dt>

[**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[**Register Protocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol)
</dt> <dt>

[RTMv1-Protokoll Familien Bezeichner](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> <dt>

[**Rtmde queueroutechangemess**](rtmdequeueroutechangemessage.md)
</dt> <dt>

[**Rtmderegisterclient**](rtmderegisterclient.md)
</dt> </dl>

 

