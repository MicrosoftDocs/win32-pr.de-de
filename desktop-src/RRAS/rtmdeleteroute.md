---
title: Rtmdeleteroute-Funktion (RTM. h)
description: Die rtmdeleteroute-Funktion löscht einen Routen Eintrag.
ms.assetid: a98026e9-40f5-42e9-943c-dfc561feef6d
keywords:
- Rtmdeleteroute-Funktion (RAS)
topic_type:
- apiref
api_name:
- RtmDeleteRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 310364bdb6e6ba7daf285316fcaaf16884e53929
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956694"
---
# <a name="rtmdeleteroute-function"></a>Rtmdeleteroute-Funktion

\[Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar. Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.\]

Die **rtmdeleteroute** -Funktion löscht einen Routen Eintrag.

## <a name="syntax"></a>Syntax


```C++
DWORD RtmDeleteRoute(
  _In_  HANDLE ClientHandle,
  _In_  PVOID  Route,
  _Out_ DWORD  Flags,
  _Out_ PVOID  CurBestRoute
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Clienthandle* \[ in\]
</dt> <dd>

Handle, das den Client und somit das Routing Protokoll der hinzugefügten oder aktualisierten Route identifiziert. Rufen Sie dieses Handle durch Aufrufen von [**rtmregisterclient**](rtmregisterclient.md)ab.

</dd> <dt>

*Route* \[ in\]
</dt> <dd>

Zeiger auf eine Protokoll familienspezifische Struktur, die die neue oder aktualisierte Route angibt. Die folgenden Felder werden vom Routing Tabellen-Manager verwendet, um die Routing Tabelle zu aktualisieren:



| Wert                                                                                                                                                                                                         | Bedeutung                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="RR_Network"></span><span id="rr_network"></span><span id="RR_NETWORK"></span><dl> <dt>**RR- \_ Netzwerk**</dt> </dl>                             | Gibt die Zielnetzwerk Nummer an. <br/>                                 |
| <span id="RR_InterfaceID"></span><span id="rr_interfaceid"></span><span id="RR_INTERFACEID"></span><dl> <dt>**RR- \_ interfakeid**</dt> </dl>             | Gibt den Index der Schnittstelle an, über die die Route empfangen wurde.<br/> |
| <span id="RR_NextHopAddress"></span><span id="rr_nexthopaddress"></span><span id="RR_NEXTHOPADDRESS"></span><dl> <dt>**RR \_ NextHopAddress**</dt> </dl> | Gibt die Netzwerkadresse des Routers für den nächsten Hop an.<br/>                      |



 

</dd> <dt>

*Flags* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Satz von Flags, die den Typ der Änderungs Meldung angeben, und die Informationen, die in den bereitgestellten Puffern abgelegt wurden. Dieser Parameter ist einer der folgenden Werte.



| Flags                                                                                                                                                                      | Bedeutung                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_NO_CHANGE"></span><span id="rtm_no_change"></span><dl> <dt>**RTM \_ keine \_ Änderung**</dt> </dl>             | Das Löschen der Route hat keine Auswirkung auf die beste Route zu einem Zielnetzwerk. Anders ausgedrückt: ein anderer Eintrag stellt eine Route zum gleichen Zielnetzwerk dar und verfügt über eine niedrigere Metrik.<br/> |
| <span id="RTM_ROUTE_DELETED"></span><span id="rtm_route_deleted"></span><dl> <dt>**RTM- \_ Route \_ gelöscht**</dt> </dl> | Die gelöschte Route war die einzige Route, die für ein bestimmtes Zielnetzwerk verfügbar ist.<br/>                                                                                                  |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <dt>**RTM- \_ Route \_ geändert**</dt> </dl> | Nachdem diese Route gelöscht wurde, wurde eine andere Route zu einem bestimmten Zielnetzwerk. " *Currbestroute* " zeigt auf die Informationen für die neue beste Route.<br/>               |



 

</dd> <dt>

*Cursor Route* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine-Struktur, die die aktuellen Informationen über die beste Route empfängt, sofern vorhanden. Der Typ der Struktur ist spezifisch für die Protokollfamilie, z. b. IP oder IPX.

Dieser Parameter ist optional. Wenn der Aufrufer **null** für diesen Parameter angibt, werden die aktuellen Informationen zur optimalen Route nicht zurückgegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert **kein \_ Fehler**.

Wenn die Funktion fehlschlägt, ist der Rückgabewert einer der folgenden Fehlercodes.



| Wert                                                                                                       | BESCHREIBUNG                                                                                            |
|-------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Fehler bei \_ ungültigem \_ handle**</dt> </dl>       | Der Clienthandle-Parameter ist kein gültiges Handle.<br/>                                          |
| <dl> <dt>**Fehler bei \_ ungültigem \_ Parameter**</dt> </dl>    | Die Routen Struktur, auf die durch den *Routen* Parameter verwiesen wird, enthält einen Elementwert.<br/>            |
| <dl> <dt>**Fehler " \_ keine \_ solche \_ Route"**</dt> </dl>       | Es sind keine Einträge in der Routing Tabelle vorhanden, die den Parametern der angegebenen Route entsprechen.<br/> |
| <dl> <dt>**Fehler \_ keine \_ System \_ Ressourcen**</dt> </dl> | Es sind nicht genügend Ressourcen vorhanden, um den Vorgang auszuführen. <br/>                                 |



 

## <a name="remarks"></a>Bemerkungen

Die Funktion generiert eine Weiterleitungs Änderungs Meldung, wenn sich die beste Route zu einem Zielnetzwerk aufgrund des Löschvorgangs geändert hat. Die Weiterleitungs Änderungs Meldung wird jedoch nicht an den Client gesendet, von dem dieser aufgerufen wird. Stattdessen werden relevante Informationen von dieser Funktion direkt an den Client zurückgegeben.

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

[**Rtmaddroute**](rtmaddroute.md)
</dt> <dt>

[**Rtmde queueroutechangemess**](rtmdequeueroutechangemessage.md)
</dt> </dl>

 

 





