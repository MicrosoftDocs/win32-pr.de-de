---
title: RtmDeleteRoute-Funktion (Rtm.h)
description: Die RtmDeleteRoute-Funktion löscht einen Routeneintrag.
ms.assetid: a98026e9-40f5-42e9-943c-dfc561feef6d
keywords:
- RtmDeleteRoute-Funktion RAS
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
ms.openlocfilehash: 0efe2e34345cc335b8214b781da4dce608dddcc4c2f77e80d8c86f76007c2855
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073850"
---
# <a name="rtmdeleteroute-function"></a>RtmDeleteRoute-Funktion

\[Diese API wurde durch die [RoutingTabellen-Manager-API Version 2](about-routing-table-manager-version-2.md) ersetzt und ist über Windows Server 2003 hinaus nicht mehr verfügbar. Anwendungen sollten die Routingtabellen-Manager-API Version 2 verwenden.\]

Die **RtmDeleteRoute-Funktion** löscht einen Routeneintrag.

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

*ClientHandle* \[ In\]
</dt> <dd>

Handle, das den Client und damit das Routingprotokoll der hinzugefügten oder aktualisierten Route identifiziert. Rufen Sie dieses Handle ab, indem [**Sie RtmRegisterClient aufrufen.**](rtmregisterclient.md)

</dd> <dt>

*Route* \[ In\]
</dt> <dd>

Zeiger auf eine protokollfamilienspezifische Struktur, die die neue oder aktualisierte Route angibt. Die folgenden Felder werden vom Routingtabellen-Manager verwendet, um die Routingtabelle zu aktualisieren:



| Wert                                                                                                                                                                                                         | Bedeutung                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="RR_Network"></span><span id="rr_network"></span><span id="RR_NETWORK"></span><dl> <dt>**\_RR-Netzwerk**</dt> </dl>                             | Gibt die Zielnetzwerknummer an. <br/>                                 |
| <span id="RR_InterfaceID"></span><span id="rr_interfaceid"></span><span id="RR_INTERFACEID"></span><dl> <dt>**\_RR-Schnittstellen-ID**</dt> </dl>             | Gibt den Index der Schnittstelle an, über die die Route empfangen wurde.<br/> |
| <span id="RR_NextHopAddress"></span><span id="rr_nexthopaddress"></span><span id="RR_NEXTHOPADDRESS"></span><dl> <dt>**RR \_ NextHopAddress**</dt> </dl> | Gibt die Netzwerkadresse des Routers des nächsten Hops an.<br/>                      |



 

</dd> <dt>

*Flags* \[ out\]
</dt> <dd>

Zeiger auf eine Gruppe von Flags, die den Typ der Änderungsmeldung angeben und angeben, welche Informationen in den bereitgestellten Puffern platziert wurden. Dieser Parameter ist einer der folgenden Werte.



| Flags                                                                                                                                                                      | Bedeutung                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_NO_CHANGE"></span><span id="rtm_no_change"></span><dl> <dt>**RTM \_ KEINE \_ ÄNDERUNG**</dt> </dl>             | Das Löschen der Route hat keine Auswirkungen auf die beste Route zu einem Zielnetzwerk. Anders ausgedrückt: Ein anderer Eintrag stellt eine Route zum gleichen Zielnetzwerk dar und verfügt über eine niedrigere Metrik.<br/> |
| <span id="RTM_ROUTE_DELETED"></span><span id="rtm_route_deleted"></span><dl> <dt>**\_RTM-ROUTE \_ GELÖSCHT**</dt> </dl> | Die gelöschte Route war die einzige verfügbare Route für ein bestimmtes Zielnetzwerk.<br/>                                                                                                  |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <dt>**\_RTM-ROUTE \_ GEÄNDERT**</dt> </dl> | Nachdem diese Route gelöscht wurde, wurde eine andere Route zur besten Route zu einem bestimmten Zielnetzwerk. *CurBestRoute* verweist auf die Informationen für die neue beste Route.<br/>               |



 

</dd> <dt>

*CurBestRoute* \[ out\]
</dt> <dd>

Zeiger auf eine -Struktur, die die aktuellen Informationen zur besten Route empfängt, sofern dies der Fall ist. Der Typ der Struktur ist spezifisch für die Protokollfamilie, z. B. IP oder IPX.

Dieser Parameter ist optional. Wenn der Aufrufer NULL **für diesen** Parameter angibt, werden die aktuellen Informationen zur besten Route nicht zurückgegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert **NO \_ ERROR**.

Wenn die Funktion fehlschlägt, ist der Rückgabewert einer der folgenden Fehlercodes.



| Wert                                                                                                       | Beschreibung                                                                                            |
|-------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**FEHLER \_ UNGÜLTIGES \_ HANDLE**</dt> </dl>       | Der Clienthandpunktparameter ist kein gültiges Handle.<br/>                                          |
| <dl> <dt>**FEHLER \_ UNGÜLTIGER \_ PARAMETER**</dt> </dl>    | Die Routenstruktur, auf die der *Route-Parameter* zeigt, enthält einen Memberwert.<br/>            |
| <dl> <dt>**FEHLER: \_ \_ KEINE SOLCHE \_ ROUTE**</dt> </dl>       | In der Routingtabelle sind keine Einträge enthalten, die mit den Parametern der angegebenen Route übereinstimmen.<br/> |
| <dl> <dt>**FEHLER: \_ \_ KEINE \_ SYSTEMRESSOURCEN**</dt> </dl> | Es sind nicht genügend Ressourcen zum Ausführen des Vorgangs verfügbar. <br/>                                 |



 

## <a name="remarks"></a>Hinweise

Die Funktion generiert eine Meldung zur Routenänderung, wenn sich die beste Route zu einem Zielnetzwerk als Ergebnis des Löschvorgang geändert hat. Die Meldung zur Routenänderung wird jedoch nicht an den Client gesendet, der diesen Aufruf vorsandt. Stattdessen werden relevante Informationen von dieser Funktion direkt an diesen Client zurückgegeben.

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

[Routing Table Manager Version 1 Reference](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Routingtabellen-Manager- Version 1-Funktionen](routing-table-manager-version-1-functions.md)
</dt> <dt>

[**RtmAddRoute**](rtmaddroute.md)
</dt> <dt>

[**RtmDequeueRouteChangeMessage**](rtmdequeueroutechangemessage.md)
</dt> </dl>

 

 





