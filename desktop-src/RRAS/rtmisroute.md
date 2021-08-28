---
title: RtmIsRoute-Funktion (Rtm.h)
description: Die RtmIsRoute-Funktion bestimmt, ob eine oder mehrere Routen zu einem angegebenen Zielnetzwerk vorhanden sind. Wenn dies der Fall ist, gibt die Funktion Informationen für die beste Route zu diesem Netzwerk zurück.
ms.assetid: f9939790-d0a6-487e-9674-a01d436dc962
keywords:
- RtmIsRoute-Funktion RAS
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
ms.openlocfilehash: 312b43a7cf66e17cc6016fe3ad35bd21cd1e7ae19ecd7864a10de4d977a92ac9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073810"
---
# <a name="rtmisroute-function"></a>RtmIsRoute-Funktion

\[Diese API wurde durch die [RoutingTabellen-Manager-API Version 2](about-routing-table-manager-version-2.md) ersetzt und ist über Windows Server 2003 hinaus nicht mehr verfügbar. Anwendungen sollten die Routingtabellen-Manager-API Version 2 verwenden.\]

Die **RtmIsRoute-Funktion** bestimmt, ob eine oder mehrere Routen zu einem angegebenen Zielnetzwerk vorhanden sind. Wenn dies der Fall ist, gibt die Funktion Informationen für die beste Route zu diesem Netzwerk zurück.

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

*ProtocolFamily* \[ In\]
</dt> <dd>

Gibt den Typ der Datenstruktur an, auf die der *Network-Parameter* verweist, z. B. [**IP \_ NETWORK**](ip-network.md), [**IPX \_ NETWORK**](ipx-network.md).

</dd> <dt>

*Netzwerk* \[ In\]
</dt> <dd>

Zeiger auf eine -Struktur, die protokollfamilienspezifische Netzwerknummerdaten angibt. Diese Daten identifizieren das Netzwerk, für das der Aufrufer Routeninformationen sucht.

</dd> <dt>

*BestRoute* \[ out\]
</dt> <dd>

Zeiger auf eine protokollfamilienspezifische Struktur, die die aktuellen besten Routeninformationen empfängt, sofern dies der Fall ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist einer der folgenden Codes.



| Wert                                                                                                       | BESCHREIBUNG                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**STIMMT**</dt> </dl>                         | Es ist mindestens eine Route zum angegebenen Netzwerk vorhanden. Die beste Route wird in der Struktur zurückgegeben, auf die der *BestRoute-Parameter* zeigt.<br/>      |
| <dl> <dt>**FALSE**</dt> </dl>                        | Es gibt keine Route zum angegebenen Netzwerk, oder der Vorgang ist fehlgeschlagen. Rufen [**Sie GetLastError auf,**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) um weitere Informationen zu erhalten:<br/> |
| <dl> <dt>**NO \_ ERROR**</dt> </dl>                    | Der Vorgang war erfolgreich, aber es gibt keine Route zum angegebenen Netzwerk.<br/>                                                                      |
| <dl> <dt>**FEHLER \_ UNGÜLTIGER \_ PARAMETER**</dt> </dl>    | Der Wert des *ProtocolFamily-Parameters* entspricht nicht einer installierten Protokollfamilie.<br/>                                             |
| <dl> <dt>**FEHLER: \_ \_ KEINE \_ SYSTEMRESSOURCEN**</dt> </dl> | Es sind nicht genügend Ressourcen zum Durchführen des Vorgangs verfügbar.<br/>                                                                                  |



 

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

[**\_IP-NETZWERK**](ip-network.md)
</dt> <dt>

[**\_IPX-NETZWERK**](ipx-network.md)
</dt> <dt>

[Bezeichner der RTMv1-Protokollfamilie](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> </dl>

 

