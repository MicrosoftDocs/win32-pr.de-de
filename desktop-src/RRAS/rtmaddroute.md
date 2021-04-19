---
title: Rtmaddroute-Funktion (RTM. h)
description: Die rtmaddroute-Funktion fügt einen Routen Eintrag hinzu oder aktualisiert einen vorhandenen Routen Eintrag.
ms.assetid: 09a9b57d-f10b-40b7-a3c1-2e0613f29431
keywords:
- Rtmaddroute-Funktion (RAS)
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
ms.openlocfilehash: a0c3ee68c9b026fc37457819777e69d2be7984e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339342"
---
# <a name="rtmaddroute-function"></a>Rtmaddroute-Funktion

\[Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar. Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.\]

Die **rtmaddroute** -Funktion fügt einen Routen Eintrag hinzu oder aktualisiert einen vorhandenen Routen Eintrag.

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

*Clienthandle* \[ in\]
</dt> <dd>

Handle, das den Client identifiziert, und damit das Routing Protokoll, das die Route hinzugefügt oder aktualisiert hat. Rufen Sie dieses Handle durch Aufrufen von [**rtmregisterclient**](rtmregisterclient.md)ab.

</dd> <dt>

*Route* \[ in\]
</dt> <dd>

Zeiger auf eine Protokoll familienspezifische Struktur, die die neue oder aktualisierte Route angibt. Die folgenden Felder werden vom Routing Tabellen-Manager verwendet, um die Routing Tabelle zu aktualisieren:



| Wert                                                                                                                                                                                                                                 | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RR_Network"></span><span id="rr_network"></span><span id="RR_NETWORK"></span><dl> <dt>**RR- \_ Netzwerk**</dt> </dl>                                                     | Gibt die Zielnetzwerk Nummer an.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="RR_InterfaceID"></span><span id="rr_interfaceid"></span><span id="RR_INTERFACEID"></span><dl> <dt>**RR- \_ interfakeid**</dt> </dl>                                     | Gibt den Index der Schnittstelle an, über die die Route empfangen wurde.<br/>                                                                                                                                                                                                                                                                                                                     |
| <span id="RR_NextHopAddress"></span><span id="rr_nexthopaddress"></span><span id="RR_NEXTHOPADDRESS"></span><dl> <dt>**RR \_ NextHopAddress**</dt> </dl>                         | Gibt die Adresse des Routers für den nächsten Hop an.<br/>                                                                                                                                                                                                                                                                                                                                                  |
| <span id="RR_FamilySpecificData"></span><span id="rr_familyspecificdata"></span><span id="RR_FAMILYSPECIFICDATA"></span><dl> <dt>**RR \_ familyspecificdata**</dt> </dl>         | Gibt Daten an, die für die Protokollfamilie spezifisch sind. Obwohl die Daten für den Routing Tabellen-Manager transparent sind, werden Sie beim Vergleichen von Routen zum ermitteln, ob sich die Routeninformationen geändert haben, berücksichtigt. Die Daten werden auch verwendet, um Metrikwerte festzulegen, die unabhängig vom Routing Protokoll sind. Folglich werden diese Daten verwendet, um die beste Route für das Zielnetzwerk zu ermitteln.<br/> |
| <span id="RR_ProtocolSpecificData"></span><span id="rr_protocolspecificdata"></span><span id="RR_PROTOCOLSPECIFICDATA"></span><dl> <dt>**RR \_ protocolspecificdata**</dt> </dl> | Gibt Daten an, die für das Routing Protokoll spezifisch sind, das die Route bereitgestellt hat.<br/>                                                                                                                                                                                                                                                                                                              |
| <span id="RR_TimeStamp"></span><span id="rr_timestamp"></span><span id="RR_TIMESTAMP"></span><dl> <dt>**RR- \_ Zeitstempel**</dt> </dl>                                             | Gibt die aktuelle Systemzeit an. Dieses Feld wird vom Routing Tabellen-Manager festgelegt.<br/>                                                                                                                                                                                                                                                                                                             |



 

</dd> <dt>

*Timeto-Live* \[ in\]
</dt> <dd>

Gibt die Anzahl der Sekunden an, die die angegebene Route in der Routing Tabelle aufbewahrt werden soll. Wenn dieser Parameter auf unendlich festgelegt ist, wird die Route so lange beibehalten, bis Sie explizit gelöscht wird. Das aktuelle Limit für *Timeto Live* beträgt 2147483 Sek. (24 + Tage).

</dd> <dt>

*Flags* \[ vorgenommen\]
</dt> <dd>

Zeiger auf eine **DWORD** -Variable. Der Wert dieser Variablen wird vom Routing Tabellen-Manager festgelegt. Der Wert gibt den Typ der Änderung an und welche Informationen in den bereitgestellten Puffern zurückgegeben wurden. Bei diesem Parameter handelt es sich um einen der folgenden Parameter.



| Flags                                                                                                                                                                      | Bedeutung                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_NO_CHANGE"></span><span id="rtm_no_change"></span><dl> <dt>**RTM \_ keine \_ Änderung**</dt> </dl>             | Das Hinzufügen oder aktualisieren hat entweder keinen der wichtigen Routen Parameter geändert, oder der betroffene Routen Eintrag ist nicht die beste Route zwischen den Einträgen für das Zielnetzwerk.<br/>                                                                                                          |
| <span id="RTM_ROUTE_ADDED"></span><span id="rtm_route_added"></span><dl> <dt>**RTM- \_ Route \_ hinzugefügt**</dt> </dl>       | Die Route wurde für das Zielnetzwerk hinzugefügt. Der Parameter " *currbestroute* " verweist auf die Informationen für die hinzugefügte Route.<br/>                                                                                                                                                                    |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <dt>**RTM- \_ Route \_ geändert**</dt> </dl> | Mindestens einer der wichtigen Parameter wurde geändert, um die beste Route zum Zielnetzwerk zu erzielen. Die wichtigsten Parameter sind: <br/> Protokoll Bezeichner<br/> Schnittstellen Index<br/> Adresse des nächsten Hops<br/> Protokoll familienspezifische Daten (einschließlich Routingmetriken)<br/> |



 

Der *prevbestroute* -Parameter verweist auf die Routeninformationen wie vor der Änderung. Der Parameter " *currbestroute* " zeigt auf die aktuellen Routeninformationen (d. h. nach Änderung).

</dd> <dt>

*Cursor Route* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine-Struktur, die die aktuellen Informationen über die beste Route empfängt, sofern vorhanden. Der Typ der Struktur ist spezifisch für die Protokollfamilie, z. b. IP oder IPX.

Dieser Parameter ist optional. Wenn der Aufrufer **null** für diesen Parameter angibt, werden die aktuellen Informationen zur optimalen Route nicht zurückgegeben.

</dd> <dt>

*Prevbestroute* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine-Struktur, die die vorherigen Informationen über die beste Route empfängt, sofern vorhanden. Der Typ der Struktur ist spezifisch für die Protokollfamilie, z. b. IP oder IPX.

Dieser Parameter ist optional. Wenn der Aufrufer für diesen Parameter **null** angibt, werden die vorherigen Informationen zur optimalen Route nicht zurückgegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist einer der folgenden Codes.



| Wert                                                                                                       | BESCHREIBUNG                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**kein \_ Fehler**</dt> </dl>                    | Die Route wurde erfolgreich hinzugefügt oder aktualisiert.<br/>                 |
| <dl> <dt>**Fehler bei \_ ungültigem \_ handle**</dt> </dl>       | Der Clienthandle-Parameter ist kein gültiges Handle.<br/>           |
| <dl> <dt>**Fehler bei \_ ungültigem \_ Parameter**</dt> </dl>    | Die Routen Struktur enthält einen ungültigen Parameter.<br/>           |
| <dl> <dt>**Fehler \_ keine \_ System \_ Ressourcen**</dt> </dl> | Es sind nicht genügend Ressourcen vorhanden, um den Vorgang auszuführen.<br/> |
| <dl> <dt>**Fehler \_ nicht \_ genügend Arbeits \_ Speicher**</dt> </dl>   | Es ist nicht genügend Arbeitsspeicher zum Zuordnen des Routen Eintrags vorhanden.<br/>    |



 

## <a name="remarks"></a>Bemerkungen

Die-Funktion generiert eine Weiterleitungs Änderungs Meldung, wenn sich die beste Route zu einem Zielnetzwerk aufgrund dieses Vorgangs geändert hat. Die Weiterleitungs Änderungs Meldung wird jedoch nicht an den Client gesendet, von dem dieser aufgerufen wird. Stattdessen werden relevante Informationen von dieser Funktion direkt über die *Flags*, die Parameter " *currbestroute*" und " *prevbestroute* " an den Client zurückgegeben.

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

[**Rtmdeleteroute**](rtmdeleteroute.md)
</dt> <dt>

[**Rtmde queueroutechangemess**](rtmdequeueroutechangemessage.md)
</dt> </dl>

 

 





