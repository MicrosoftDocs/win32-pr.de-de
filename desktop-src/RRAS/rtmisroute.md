---
title: Rtmisroute-Funktion (RTM. h)
description: Die rtmisroute-Funktion bestimmt, ob eine oder mehrere Routen zu einem angegebenen Zielnetzwerk vorhanden sind. Wenn dies der Fall ist, gibt die Funktion Informationen für die beste Route zu diesem Netzwerk zurück.
ms.assetid: f9939790-d0a6-487e-9674-a01d436dc962
keywords:
- Rtmisroute-Funktion (RAS)
topic_type:
- apiref
api_name:
- RtmIsRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64621732f2f7a35223421e5f0fc86a309d332c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478222"
---
# <a name="rtmisroute-function"></a>Rtmisroute-Funktion

\[Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar. Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.\]

Die **rtmisroute** -Funktion bestimmt, ob eine oder mehrere Routen zu einem angegebenen Zielnetzwerk vorhanden sind. Wenn dies der Fall ist, gibt die Funktion Informationen für die beste Route zu diesem Netzwerk zurück.

## <a name="syntax"></a>Syntax


```C++
BOOL RtmIsRoute(
  _In_  DWORD ProtocolFamily,
  _In_  PVOID Network,
  _Out_ PVOID BestRoute
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ProtocolFamily* \[ in\]
</dt> <dd>

Gibt den Typ der Datenstruktur an, auf die vom *Netzwerk* Parameter verwiesen wird, z. b. [**IP- \_ Netzwerk**](ip-network.md), [**IPX- \_ Netzwerk**](ipx-network.md).

</dd> <dt>

*Netzwerk* \[ in\]
</dt> <dd>

Ein Zeiger auf eine-Struktur, die die Protokoll Familien spezifischen Netzwerk Nummern Daten angibt. Diese Daten identifizieren das Netzwerk, für das der Aufrufer Routeninformationen sucht.

</dd> <dt>

*Bestroute* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Protokoll familienspezifische Struktur, die die aktuellen besten Routeninformationen empfängt, sofern vorhanden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist einer der folgenden Codes.



| Wert                                                                                                       | BESCHREIBUNG                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Fall**</dt> </dl>                         | Es ist mindestens eine Route zum angegebenen Netzwerk vorhanden. Die beste Route wird in der Struktur zurückgegeben, auf die der *bestroute* -Parameter verweist.<br/>      |
| <dl> <dt>**Alarm**</dt> </dl>                        | Es ist keine Route zum angegebenen Netzwerk vorhanden, oder der Vorgang ist fehlgeschlagen. Rufen Sie [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf, um weitere Informationen zu erhalten:<br/> |
| <dl> <dt>**kein \_ Fehler**</dt> </dl>                    | Der Vorgang war erfolgreich, aber es ist keine Route zum angegebenen Netzwerk vorhanden.<br/>                                                                      |
| <dl> <dt>**Fehler bei \_ ungültigem \_ Parameter**</dt> </dl>    | Der Wert des *ProtocolFamily* -Parameters entspricht keiner installierten Protokollfamilie.<br/>                                             |
| <dl> <dt>**Fehler \_ keine \_ System \_ Ressourcen**</dt> </dl> | Es sind nicht genügend Ressourcen vorhanden, um den Vorgang auszuführen.<br/>                                                                                  |



 

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

[**IP- \_ Netzwerk**](ip-network.md)
</dt> <dt>

[**IPX- \_ Netzwerk**](ipx-network.md)
</dt> <dt>

[RTMv1-Protokoll Familien Bezeichner](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> </dl>

 

