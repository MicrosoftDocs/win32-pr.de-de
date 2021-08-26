---
title: RtmRegisterClient-Funktion (Rtm.h)
description: Die RtmRegisterClient-Funktion registriert einen Client als Handler des angegebenen Protokolls. Es richtet einen Benachrichtigungsmechanismus für Routenänderung für den Client ein und legt Protokolloptionen fest.
ms.assetid: 70426601-695d-47ed-b71a-1df3fb8ddf10
keywords:
- RtmRegisterClient-Funktion RAS
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
ms.openlocfilehash: db58fc9457195c2149fd8d34a8a65a6d5085135275e1c878633f64cb742b02cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081040"
---
# <a name="rtmregisterclient-function"></a>RtmRegisterClient-Funktion

\[Diese API wurde durch die [RoutingTabellen-Manager-API Version 2](about-routing-table-manager-version-2.md) ersetzt und ist über Windows Server 2003 hinaus nicht mehr verfügbar. Anwendungen sollten die Routingtabellen-Manager-API Version 2 verwenden.\]

Die **RtmRegisterClient-Funktion** registriert einen Client als Handler des angegebenen Protokolls. Es richtet einen Benachrichtigungsmechanismus für Routenänderung für den Client ein und legt Protokolloptionen fest.

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

*ProtocolFamily* \[ In\]
</dt> <dd>

Gibt die Protokollfamilie des zu registrierenden Routingprotokolls an.

</dd> <dt>

*RoutingProtocol* \[ In\]
</dt> <dd>

Gibt den Routingprotokollbezeichner an, der bei der Registrierung beim Router-Manager verwendet wird. Weitere Informationen [**finden Sie unter RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol).

</dd> <dt>

*ChangeEvent* \[ In\]
</dt> <dd>

Gibt an, dass sich eine optimale Route zu einem Netzwerk in der Tabelle geändert hat. Der Routingtabellen-Manager signalisiert dieses Ereignis nach einer Änderung an die beste Route zu einem beliebigen Netzwerk in der Tabelle. Weitere Informationen zu Routenänderungsbenachrichtigungen finden Sie unter [**RtmDequeueRouteChangeMessage.**](rtmdequeueroutechangemessage.md)

Dieser Parameter ist optional. Wenn der Aufrufer NULL **für** diesen Parameter angibt, benachrichtigt der Routingtabellen-Manager den Client nicht über Änderungen am besten Routenstatus.

</dd> <dt>

*Flags* \[ In\]
</dt> <dd>

Gibt verschiedene Optionen für die spezielle Behandlung des Routingprotokolls an. Der folgende Wert wird derzeit unterstützt.



| Flags                                                                                                                                                                                               | Bedeutung                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_PROTOCOL_SINGLE_ROUTE"></span><span id="rtm_protocol_single_route"></span><dl> <dt>**\_RTM-PROTOKOLL \_ – EINZELNE \_ ROUTE**</dt> </dl> | Der Routingtabellen-Manager behält nur eine Route pro Zielnetzwerk für das Routingprotokoll bei. Anders ausgedrückt: Der Routingtabellen-Manager ersetzt Routeneinträge, die die gleichen Zielnetzwerknummern haben, anstatt neue Einträge hinzufügen zu müssen.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei erfolgreicher Rückgabe ein **HANDLE-Wert,** der den Client in nachfolgenden Aufrufen des Routingtabellen-Managers identifiziert.

Ein **NULL-Handle** gibt an, dass der Routingtabellen-Manager den Client nicht registrieren konnte. Rufen [**Sie GetLastError auf,**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) um die Ursache für den Fehler zu erhalten.



| Wert                                                                                                         | BESCHREIBUNG                                                                                     |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**FEHLERCLIENT \_ \_ IST BEREITS \_ VORHANDEN**</dt> </dl> | Ein anderer Client wurde bereits registriert, um das angegebene Protokoll zu verarbeiten.<br/>              |
| <dl> <dt>**FEHLER \_ UNGÜLTIGER \_ PARAMETER**</dt> </dl>      | Die angegebene Protokollfamilie wird nicht unterstützt, oder der *Flags-Parameter* ist ungültig.<br/> |
| <dl> <dt>**FEHLER: \_ \_ KEINE \_ SYSTEMRESSOURCEN**</dt> </dl>   | Unzureichende Ressourcen zum Durchführen des Vorgangs.<br/>                                   |
| <dl> <dt>**FEHLER: \_ NICHT \_ GENÜGEND \_ ARBEITSSPEICHER**</dt> </dl>     | Nicht genügend Arbeitsspeicher zum Zuordnen von Datenstrukturen für den Client.<br/>                      |



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                     |
| Header<br/>                   | <dl> <dt>Rtm.h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Rtm.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Rtm.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Routing Table Manager Version 1 Reference](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Routingtabellen-Manager- Version 1-Funktionen](routing-table-manager-version-1-functions.md)
</dt> <dt>

[**Getlasterror**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol)
</dt> <dt>

[Bezeichner der RTMv1-Protokollfamilie](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> <dt>

[**RtmDequeueRouteChangeMessage**](rtmdequeueroutechangemessage.md)
</dt> <dt>

[**RtmDeregisterClient**](rtmderegisterclient.md)
</dt> </dl>

 

