---
title: Rtmde queueroutechangemess-Funktion (RTM. h)
description: Die rtmdequeueroutechangemess-Funktion gibt die nächste Weiterleitungs Änderungs Meldung in der Warteschlange zurück, die dem angegebenen Client zugeordnet ist.
ms.assetid: 44f2116a-3c8d-4ac6-896e-b12930b218a5
keywords:
- Rtmde queueroutechangemess-Funktion (RAS)
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
ms.openlocfilehash: 448df230742b03f82294de102bf14b50fefa035c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104390"
---
# <a name="rtmdequeueroutechangemessage-function"></a>Rtmde queueroutechangemess-Funktion

\[Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar. Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.\]

Die **rtmdequeueroutechangemess** -Funktion gibt die nächste Weiterleitungs Änderungs Meldung in der Warteschlange zurück, die dem angegebenen Client zugeordnet ist.

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

*Clienthandle* \[ in\]
</dt> <dd>

Handle, das den Client identifiziert, für den der Vorgang ausgeführt wird. Rufen Sie dieses Handle durch Aufrufen von [**rtmregisterclient**](rtmregisterclient.md)ab.

</dd> <dt>

*Flags* \[ vorgenommen\]
</dt> <dd>

Zeiger auf eine **DWORD** -Variable. Der Wert dieser Variablen wird vom Routing Tabellen-Manager festgelegt. Der-Wert gibt den Typ der Änderungs Meldung an und gibt an, welche Informationen in den bereitgestellten Puffern zurückgegeben wurden. Bei diesem Parameter handelt es sich um einen der folgenden Parameter.



| Flags                                                                                                                                                                      | Bedeutung                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_ROUTE_ADDED"></span><span id="rtm_route_added"></span><dl> <dt>**RTM- \_ Route \_ hinzugefügt**</dt> </dl>       | Die erste Route wurde für ein bestimmtes Zielnetzwerk hinzugefügt. Der Parameter " *currbestroute* " verweist auf die Informationen für die hinzugefügte Route.<br/>                                                                                                                                                            |
| <span id="RTM_ROUTE_DELETED"></span><span id="rtm_route_deleted"></span><dl> <dt>**RTM- \_ Route \_ gelöscht**</dt> </dl> | Die einzige Route, die für ein bestimmtes Zielnetzwerk verfügbar ist, wurde gelöscht. Der *prevbestroute* -Parameter verweist auf die Informationen für die gelöschte Route.<br/>                                                                                                                                              |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <dt>**RTM- \_ Route \_ geändert**</dt> </dl> | Mindestens einer der wichtigen Parameter wurde für eine optimale Route zu einem bestimmten Zielnetzwerk geändert. Die wichtigsten Parameter sind: <br/> Protokoll Bezeichner<br/> Schnittstellen Index<br/> Adresse des nächsten Hops<br/> Protokoll familienspezifische Daten (einschließlich Routingmetriken)<br/> |



 

Der *prevbestroute* -Parameter verweist auf die Routeninformationen wie vor der Änderung. Der Parameter " *currbestroute* " zeigt auf die aktuellen Routeninformationen (d. h. nach Änderung).

</dd> <dt>

*Cursor Route* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine-Struktur, die die aktuellen Informationen zur optimalen Route (sofern vorhanden) empfängt. Der Typ der Struktur ist spezifisch für die Protokollfamilie, z. b. IP oder IPX.

Dieser Parameter ist optional. Wenn der Aufrufer **null** für diesen Parameter angibt, werden die aktuellen Informationen zur optimalen Route nicht zurückgegeben.

</dd> <dt>

*Prevbestroute* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine-Struktur, die die vorherigen Informationen über die beste Route empfängt, sofern vorhanden. Der Typ der Struktur ist spezifisch für die Protokollfamilie, z. b. IP oder IPX.

Dieser Parameter ist optional. Wenn der Aufrufer **null** für diesen Parameter angibt, werden die vorherigen Informationen mit der besten Route nicht zurückgegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist einer der folgenden Codes.



| Wert                                                                                                       | BESCHREIBUNG                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**kein \_ Fehler**</dt> </dl>                    | Diese Meldung war die letzte Meldung in der Warteschlange des Clients. Das Ereignis Objekt wird zurückgesetzt.<br/>                                                                                                                                               |
| <dl> <dt>**Fehler bei \_ ungültigem \_ handle**</dt> </dl>       | Der *Clienthandle* -Parameter ist kein gültiges Handle, oder der Client hat bei der Registrierung kein Ereignis Objekt für die Benachrichtigung von Änderungs Meldungen bereitgestellt (siehe [**rtmregisterclient**](rtmregisterclient.md)).<br/>                           |
| <dl> <dt>**\_Weitere Fehler \_ Meldungen**</dt> </dl>        | Die Warteschlange des Clients enthält zusätzliche Nachrichten. Der Client sollte **rtmdequeueroutechangemessage** so bald wie möglich erneut abrufen, damit der Routing Tabellen-Manager die Ressourcen freigeben kann, die den ausstehenden Nachrichten zugeordnet sind.<br/> |
| <dl> <dt>**Fehler \_ \_ Meldungen**</dt> </dl>          | Die Warteschlange des Clients enthält keine Nachrichten. der-Befehl wurde nicht angefordert. Das Ereignis wird zurückgesetzt.<br/>                                                                                                                                            |
| <dl> <dt>**Fehler \_ keine \_ System \_ Ressourcen**</dt> </dl> | Es sind nicht genügend Ressourcen vorhanden, um den Vorgang auszuführen.<br/>                                                                                                                                                                      |



 

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

[**Rtmregisterclient**](rtmregisterclient.md)
</dt> </dl>

 

 





