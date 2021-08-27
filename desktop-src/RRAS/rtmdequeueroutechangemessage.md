---
title: RtmDequeueRouteChangeMessage-Funktion (Rtm.h)
description: Die RtmDequeueRouteChangeMessage-Funktion gibt die nächste Routenänderungsnachricht in der Warteschlange zurück, die dem angegebenen Client zugeordnet ist.
ms.assetid: 44f2116a-3c8d-4ac6-896e-b12930b218a5
keywords:
- RtmDequeueRouteChangeMessage-Funktion RAS
topic_type:
- apiref
api_name:
- RtmDequeueRouteChangeMessage
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ad69b711568fd8233a60e829da8fb6fd6ce5f74d3556afa82c721a835b98e60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035880"
---
# <a name="rtmdequeueroutechangemessage-function"></a>RtmDequeueRouteChangeMessage-Funktion

\[Diese API wurde von der Routing Table Manager Version [2-API](about-routing-table-manager-version-2.md) abgelöst und ist nicht mehr als Windows Server 2003 verfügbar. Anwendungen sollten die Routing Table Manager Version 2-API verwenden.\]

Die **RtmDequeueRouteChangeMessage-Funktion** gibt die nächste Routenänderungsnachricht in der Warteschlange zurück, die dem angegebenen Client zugeordnet ist.

## <a name="syntax"></a>Syntax


```C++
DWORD RtmDequeueRouteChangeMessage(
  _In_  HANDLE ClientHandle,
  _Out_ DWORD  Flags,
  _Out_ PVOID  CurBestRoute,
  _Out_ PVOID  PrevBestRoute
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ClientHandle* \[ In\]
</dt> <dd>

Handle, das den Client identifiziert, für den der Vorgang ausgeführt wird. Rufen Sie dieses Handle ab, indem [**Sie RtmRegisterClient**](rtmregisterclient.md)aufrufen.

</dd> <dt>

*Flags* \[ out\]
</dt> <dd>

Zeiger auf eine **DWORD-Variable.** Der Wert dieser Variablen wird vom Routingtabellen-Manager festgelegt. Der Wert gibt den Typ der Änderungsnachricht und die Informationen an, die in den bereitgestellten Puffern zurückgegeben wurden. Dieser Parameter ist einer der folgenden.



| Flags                                                                                                                                                                      | Bedeutung                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_ROUTE_ADDED"></span><span id="rtm_route_added"></span><dl> <dt>**\_RTM-ROUTE \_ HINZUGEFÜGT**</dt> </dl>       | Die erste Route wurde für ein bestimmtes Zielnetzwerk hinzugefügt. Der *CurBestRoute-Parameter* verweist auf die Informationen für die hinzugefügte Route.<br/>                                                                                                                                                            |
| <span id="RTM_ROUTE_DELETED"></span><span id="rtm_route_deleted"></span><dl> <dt>**RTM \_ ROUTE DELETED (RTM-ROUTE \_ GELÖSCHT)**</dt> </dl> | Die einzige für ein bestimmtes Zielnetzwerk verfügbare Route wurde gelöscht. Der *PrevBestRoute-Parameter* verweist auf die Informationen für die gelöschte Route.<br/>                                                                                                                                              |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <dt>**\_RTM-ROUTE \_ GEÄNDERT**</dt> </dl> | Mindestens einer der signifikanten Parameter wurde für eine optimale Route zu einem bestimmten Zielnetzwerk geändert. Die wichtigsten Parameter sind: <br/> Protokollbezeichner<br/> Schnittstellenindex<br/> Adresse des nächsten Hops<br/> Protokollfamilienspezifische Daten (einschließlich Routenmetriken)<br/> |



 

Der *PrevBestRoute-Parameter* verweist auf die Routeninformationen wie vor der Änderung. Der *CurBestRoute-Parameter* verweist auf aktuelle Routeninformationen (d. h. nach der Änderung).

</dd> <dt>

*CurBestRoute* \[ out\]
</dt> <dd>

Zeiger auf eine -Struktur, die die aktuellen Informationen zur besten Route empfängt (sofern vorhanden). Der Typ der Struktur ist spezifisch für die Protokollfamilie, z. B. IP oder IPX.

Dieser Parameter ist optional. Wenn der Aufrufer **NULL** für diesen Parameter angibt, werden die aktuellen Informationen zur besten Route nicht zurückgegeben.

</dd> <dt>

*PrevBestRoute* \[ out\]
</dt> <dd>

Zeiger auf eine -Struktur, die ggf. die vorherigen Informationen zur besten Route empfängt. Der Typ der Struktur ist spezifisch für die Protokollfamilie, z. B. IP oder IPX.

Dieser Parameter ist optional. Wenn der Aufrufer **NULL** für diesen Parameter angibt, werden die vorherigen Informationen zur besten Route nicht zurückgegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist einer der folgenden Codes.



| Wert                                                                                                       | BESCHREIBUNG                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**KEIN \_ FEHLER**</dt> </dl>                    | Diese Nachricht war die letzte Nachricht in der Warteschlange des Clients. Das Ereignisobjekt wird zurückgesetzt.<br/>                                                                                                                                               |
| <dl> <dt>**FEHLER: \_ UNGÜLTIGES \_ HANDLE**</dt> </dl>       | Der *ClientHandle-Parameter* ist kein gültiges Handle, oder bei der Registrierung hat der Client kein Ereignisobjekt für die Änderungsmeldungsbenachrichtigung (siehe [**RtmRegisterClient)**](rtmregisterclient.md)zur Verfügung stellen.<br/>                           |
| <dl> <dt>**\_WEITERE \_ FEHLERMELDUNGEN**</dt> </dl>        | Die Warteschlange des Clients enthält zusätzliche Nachrichten. Der Client sollte **RtmDequeueRouteChangeMessage** so bald wie möglich erneut aufrufen, damit der Routingtabellen-Manager die Ressourcen freigeben kann, die den ausstehenden Nachrichten zugeordnet sind.<br/> |
| <dl> <dt>**\_FEHLER: KEINE \_ MELDUNGEN**</dt> </dl>          | Die Warteschlange des Clients enthält keine Nachrichten. der Aufruf nicht angefordert wurde. Das Ereignis wird zurückgesetzt.<br/>                                                                                                                                            |
| <dl> <dt>**FEHLER \_ KEINE \_ \_ SYSTEMRESSOURCEN**</dt> </dl> | Es sind nicht genügend Ressourcen vorhanden, um den Vorgang auszuführen.<br/>                                                                                                                                                                      |



 

## <a name="requirements"></a>Anforderungen



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

[Referenz zu Routingtabellen-Manager, Version 1](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Funktionen des Routingtabellen-Managers, Version 1](routing-table-manager-version-1-functions.md)
</dt> <dt>

[**RtmRegisterClient**](rtmregisterclient.md)
</dt> </dl>

 

 





