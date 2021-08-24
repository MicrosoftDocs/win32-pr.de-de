---
title: RtmGetNetworkCount-Funktion (Rtm.h)
description: Die RtmGetNetworkCount-Funktion ruft die Anzahl der Netzwerke ab, zu denen der Routingtabellen-Manager Routen hat.
ms.assetid: d0c04b8d-a6c4-44bf-a3f2-de822d635131
keywords:
- RtmGetNetworkCount-Funktion RAS
topic_type:
- apiref
api_name:
- RtmGetNetworkCount
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c721605988f15661030ddbeaadf4140fb716a089c87cc46fc2a8316bc2de9e42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035670"
---
# <a name="rtmgetnetworkcount-function"></a>RtmGetNetworkCount-Funktion

\[Diese API wurde durch die [RoutingTabellen-Manager-API Version 2](about-routing-table-manager-version-2.md) ersetzt und ist über Windows Server 2003 hinaus nicht mehr verfügbar. Anwendungen sollten die Routingtabellen-Manager-API Version 2 verwenden.\]

Die **RtmGetNetworkCount-Funktion** ruft die Anzahl der Netzwerke ab, zu denen der Routingtabellen-Manager Routen hat.

## <a name="syntax"></a>Syntax


```C++
ULONG RtmGetNetworkCount(
  _In_ DWORD ProtocolFamily
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ProtocolFamily* \[ In\]
</dt> <dd>

Gibt an, für welche Art von Netzwerk Routeninformationen wie IP oder IPX erhalten werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert die Netzwerkanzahl, die Anzahl der Netzwerke, die den Routingprotokollen der angegebenen Protokollfamilie bekannt sind.

Wenn der Rückgabewert 0 (null) ist, sind entweder keine Routen verfügbar, oder der Vorgang ist fehlgeschlagen. Rufen [**Sie GetLastError auf,**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) um weitere Informationen zu erhalten.



| Wert                                                                                                    | BESCHREIBUNG                                                                                                  |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NO \_ ERROR**</dt> </dl>                 | Der Vorgang war erfolgreich, aber es sind keine Routen verfügbar.<br/>                                             |
| <dl> <dt>**FEHLER \_ UNGÜLTIGER \_ PARAMETER**</dt> </dl> | Der Wert des *ProtocolFamily-Parameters* entspricht nicht einer installierten Protokollfamilie.<br/> |



 

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

[**Getlasterror**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[Bezeichner der RTMv1-Protokollfamilie](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> </dl>

 

