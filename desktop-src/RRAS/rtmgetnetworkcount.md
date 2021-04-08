---
title: Rtmgetnetworkcount-Funktion (RTM. h)
description: Die rtmgetnetworkcount-Funktion Ruft die Anzahl von Netzwerken ab, an die der Routing Tabellen-Manager Routen hat.
ms.assetid: d0c04b8d-a6c4-44bf-a3f2-de822d635131
keywords:
- Rtmgetnetworkcount-Funktion (RAS)
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
ms.openlocfilehash: eab4babd1e9d98071b2fbe6ab30c9b92d4a23f0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741409"
---
# <a name="rtmgetnetworkcount-function"></a>Rtmgetnetworkcount-Funktion

\[Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar. Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.\]

Die **rtmgetnetworkcount** -Funktion Ruft die Anzahl von Netzwerken ab, an die der Routing Tabellen-Manager Routen hat.

## <a name="syntax"></a>Syntax


```C++
ULONG RtmGetNetworkCount(
  _In_ DWORD ProtocolFamily
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ProtocolFamily* \[ in\]
</dt> <dd>

Gibt an, für welchen Typ von Netzwerk Routeninformationen abgerufen werden sollen, z. b. IP oder IPX.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, entspricht der Rückgabewert der Netzwerk Anzahl, der Anzahl von Netzwerken, die den Routing Protokollen der angegebenen Protokollfamilie bekannt sind.

Wenn der Rückgabewert 0 (null) ist, sind entweder keine Routen verfügbar, oder der Vorgang ist fehlgeschlagen. Rufen Sie [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf, um weitere Informationen zu erhalten.



| Wert                                                                                                    | BESCHREIBUNG                                                                                                  |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**kein \_ Fehler**</dt> </dl>                 | Der Vorgang war erfolgreich, aber es sind keine Routen verfügbar.<br/>                                             |
| <dl> <dt>**Fehler bei \_ ungültigem \_ Parameter**</dt> </dl> | Der Wert des *ProtocolFamily* -Parameters entspricht keiner installierten Protokollfamilie.<br/> |



 

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

[RTMv1-Protokoll Familien Bezeichner](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> </dl>

 

