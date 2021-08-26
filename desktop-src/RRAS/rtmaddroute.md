---
title: RtmAddRoute-Funktion (Rtm.h)
description: Die RtmAddRoute-Funktion fügt einen Routeneintrag hinzu oder aktualisiert einen vorhandenen Routeneintrag.
ms.assetid: 09a9b57d-f10b-40b7-a3c1-2e0613f29431
keywords:
- RtmAddRoute-Funktion RAS
topic_type:
- apiref
api_name:
- RtmAddRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d36b96e94ba2803664e3ff4c4fce6f4f95317c33ce5ab9ccd755c95c8d23fa21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035930"
---
# <a name="rtmaddroute-function"></a>RtmAddRoute-Funktion

\[Diese API wurde durch die [RoutingTabellen-Manager-API Version 2](about-routing-table-manager-version-2.md) ersetzt und ist über Windows Server 2003 hinaus nicht mehr verfügbar. Anwendungen sollten die Routingtabellen-Manager-API Version 2 verwenden.\]

Die **RtmAddRoute-Funktion** fügt einen Routeneintrag hinzu oder aktualisiert einen vorhandenen Routeneintrag.

## <a name="syntax"></a>Syntax


```C++
DWORD RtmAddRoute(
  _In_  HANDLE ClientHandle,
  _In_  PVOID  Route,
  _In_  DWORD  TimeToLive,
  _Out_ DWORD  Flags,
  _Out_ PVOID  CurBestRoute,
  _Out_ PVOID  PrevBestRoute
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ClientHandle* \[ In\]
</dt> <dd>

Handle, das den Client und damit das Routingprotokoll identifiziert, der die Route hinzugefügt oder aktualisiert hat. Rufen Sie dieses Handle ab, indem [**Sie RtmRegisterClient aufrufen.**](rtmregisterclient.md)

</dd> <dt>

*Route* \[ In\]
</dt> <dd>

Zeiger auf eine protokollfamilienspezifische Struktur, die die neue oder aktualisierte Route angibt. Die folgenden Felder werden vom Routingtabellen-Manager verwendet, um die Routingtabelle zu aktualisieren:



| Wert                                                                                                                                                                                                                                 | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RR_Network"></span><span id="rr_network"></span><span id="RR_NETWORK"></span><dl> <dt>**\_RR-Netzwerk**</dt> </dl>                                                     | Gibt die Zielnetzwerknummer an.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="RR_InterfaceID"></span><span id="rr_interfaceid"></span><span id="RR_INTERFACEID"></span><dl> <dt>**\_RR-Schnittstellen-ID**</dt> </dl>                                     | Gibt den Index der Schnittstelle an, über die die Route empfangen wurde.<br/>                                                                                                                                                                                                                                                                                                                     |
| <span id="RR_NextHopAddress"></span><span id="rr_nexthopaddress"></span><span id="RR_NEXTHOPADDRESS"></span><dl> <dt>**RR \_ NextHopAddress**</dt> </dl>                         | Gibt die Adresse des Routers des nächsten Hops an.<br/>                                                                                                                                                                                                                                                                                                                                                  |
| <span id="RR_FamilySpecificData"></span><span id="rr_familyspecificdata"></span><span id="RR_FAMILYSPECIFICDATA"></span><dl> <dt>**RR \_ FamilySpecificData**</dt> </dl>         | Gibt Daten an, die für die Protokollfamilie spezifisch sind. Obwohl die Daten für den Routingtabellen-Manager transparent sind, werden sie beim Vergleichen von Routen berücksichtigt, um festzustellen, ob sich Routeninformationen geändert haben. Die Daten werden auch zum Festlegen von Metrikwerten verwendet, die unabhängig vom Routingprotokoll sind. Folglich werden diese Daten verwendet, um die beste Route für das Zielnetzwerk zu ermitteln.<br/> |
| <span id="RR_ProtocolSpecificData"></span><span id="rr_protocolspecificdata"></span><span id="RR_PROTOCOLSPECIFICDATA"></span><dl> <dt>**RR \_ ProtocolSpecificData**</dt> </dl> | Gibt Daten an, die spezifisch für das Routingprotokoll sind, das die Route bereitgestellt hat.<br/>                                                                                                                                                                                                                                                                                                              |
| <span id="RR_TimeStamp"></span><span id="rr_timestamp"></span><span id="RR_TIMESTAMP"></span><dl> <dt>**\_RR-Zeitstempel**</dt> </dl>                                             | Gibt die aktuelle Systemzeit an. Dieses Feld wird vom Routingtabellen-Manager festgelegt.<br/>                                                                                                                                                                                                                                                                                                             |



 

</dd> <dt>

*TimeToLive* \[ In\]
</dt> <dd>

Gibt an, wie viele Sekunden die angegebene Route in der Routingtabelle beibehalten werden soll. Wenn dieser Parameter auf INFINITE festgelegt ist, wird die Route beibehalten, bis sie explizit gelöscht wird. Der aktuelle Grenzwert für *TimeToLive* beträgt 2147483 Sekunde (24+ Tage).

</dd> <dt>

*Flags* \[ out\]
</dt> <dd>

Zeiger auf eine **DWORD-Variable.** Der Wert dieser Variablen wird vom Routingtabellen-Manager festgelegt. Der Wert gibt den Typ der Änderung an und gibt an, welche Informationen in den bereitgestellten Puffern zurückgegeben wurden. Dieser Parameter ist einer der folgenden.



| Flags                                                                                                                                                                      | Bedeutung                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_NO_CHANGE"></span><span id="rtm_no_change"></span><dl> <dt>**RTM \_ KEINE \_ ÄNDERUNG**</dt> </dl>             | Das Additions- oder Update hat entweder keinen der signifikanten Routenparameter geändert, oder der betroffene Routeneintrag ist nicht die beste Route unter den Einträgen für das Zielnetzwerk.<br/>                                                                                                          |
| <span id="RTM_ROUTE_ADDED"></span><span id="rtm_route_added"></span><dl> <dt>**\_RTM-ROUTE \_ HINZUGEFÜGT**</dt> </dl>       | Die Route wurde für das Zielnetzwerk hinzugefügt. Der *CurBestRoute-Parameter* verweist auf die Informationen für die hinzugefügte Route.<br/>                                                                                                                                                                    |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <dt>**\_RTM-ROUTE \_ GEÄNDERT**</dt> </dl> | Mindestens einer der signifikanten Parameter wurde für die beste Route zum Zielnetzwerk geändert. Die wichtigsten Parameter sind: <br/> Protokollbezeichner<br/> Schnittstellenindex<br/> Adresse des nächsten Hops<br/> Protokollfamilienspezifische Daten (einschließlich Routenmetriken)<br/> |



 

Der *PrevBestRoute-Parameter* verweist auf die Routeninformationen wie vor der Änderung. Der *CurBestRoute-Parameter* verweist auf die aktuellen Routeninformationen (d. h. nach der Änderung).

</dd> <dt>

*CurBestRoute* \[ out\]
</dt> <dd>

Zeiger auf eine -Struktur, die die aktuellen Informationen zur besten Route empfängt, sofern dies der Fall ist. Der Typ der Struktur ist spezifisch für die Protokollfamilie, z. B. IP oder IPX.

Dieser Parameter ist optional. Wenn der Aufrufer NULL **für diesen** Parameter angibt, werden die aktuellen Informationen zur besten Route nicht zurückgegeben.

</dd> <dt>

*PrevBestRoute* \[ out\]
</dt> <dd>

Zeiger auf eine -Struktur, die die vorherigen Informationen zur besten Route empfängt, sofern diese enthalten sind. Der Typ der Struktur ist spezifisch für die Protokollfamilie, z. B. IP oder IPX.

Dieser Parameter ist optional. Wenn der Aufrufer NULL **für** diesen Parameter angibt, werden die vorherigen Informationen zur besten Route nicht zurückgegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist einer der folgenden Codes.



| Wert                                                                                                       | BESCHREIBUNG                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**NO \_ ERROR**</dt> </dl>                    | Die Route wurde erfolgreich hinzugefügt oder aktualisiert.<br/>                 |
| <dl> <dt>**FEHLER \_ UNGÜLTIGES \_ HANDLE**</dt> </dl>       | Der Clienthandpunktparameter ist kein gültiges Handle.<br/>           |
| <dl> <dt>**FEHLER \_ UNGÜLTIGER \_ PARAMETER**</dt> </dl>    | Die Routenstruktur enthält einen ungültigen Parameter.<br/>           |
| <dl> <dt>**FEHLER: \_ \_ KEINE \_ SYSTEMRESSOURCEN**</dt> </dl> | Es sind nicht genügend Ressourcen zum Durchführen des Vorgangs verfügbar.<br/> |
| <dl> <dt>**FEHLER: \_ NICHT \_ GENÜGEND \_ ARBEITSSPEICHER**</dt> </dl>   | Es ist nicht genügend Arbeitsspeicher zum Zuordnen des Routeneintrags verfügbar.<br/>    |



 

## <a name="remarks"></a>Hinweise

Die Funktion generiert eine Routenänderungsmeldung, wenn sich die beste Route zu einem Zielnetzwerk als Ergebnis dieses Vorgangs geändert hat. Die Meldung zur Routenänderung wird jedoch nicht an den Client gesendet, der diesen Aufruf vorsandt. Stattdessen werden relevante Informationen von dieser Funktion über die Parameter *Flags,* *CurBestRoute* und *PrevBestRoute* direkt an diesen Client zurückgegeben.

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

[**RtmDeleteRoute**](rtmdeleteroute.md)
</dt> <dt>

[**RtmDequeueRouteChangeMessage**](rtmdequeueroutechangemessage.md)
</dt> </dl>

 

 





