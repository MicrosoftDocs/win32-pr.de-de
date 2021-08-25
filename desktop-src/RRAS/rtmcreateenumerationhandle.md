---
title: RtmCreateEnumerationHandle-Funktion (Rtm.h)
description: Die RtmCreateEnumerationHandle-Funktion gibt ein Handle zurück, das mit RtmEnumerateGetNextRoute verwendet werden soll, um alle Routen oder eine Teilmenge von Routen zu überprüfen, die dem Routingtabellen-Manager bekannt sind.
ms.assetid: 73e3ac7d-498a-4d89-a6b5-17aaf4b17ec2
keywords:
- RtmCreateEnumerationHandle-Funktion RAS
topic_type:
- apiref
api_name:
- RtmCreateEnumerationHandle
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 635bc169b1f68e2ef29e85e9e7ef800868453dd7221d08eda7953eda277ae423
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035910"
---
# <a name="rtmcreateenumerationhandle-function"></a>RtmCreateEnumerationHandle-Funktion

\[Diese API wurde durch die [RoutingTabellen-Manager-API Version 2](about-routing-table-manager-version-2.md) ersetzt und ist über Windows Server 2003 hinaus nicht mehr verfügbar. Anwendungen sollten die Routingtabellen-Manager-API Version 2 verwenden.\]

Die **RtmCreateEnumerationHandle-Funktion** gibt ein Handle zurück, das mit [**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md) verwendet werden soll, um alle Routen oder eine Teilmenge von Routen zu überprüfen, die dem Routingtabellen-Manager bekannt sind.

## <a name="syntax"></a>Syntax


```C++
HANDLE RtmCreateEnumerationHandle(
  _In_ DWORD ProtocolFamily,
  _In_ DWORD EnumerationFlags,
  _In_ PVOID CriteriaRoute
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ProtocolFamily* \[ In\]
</dt> <dd>

Gibt die Protokollfamilie der zu aufzählenden Routen an.

</dd> <dt>

*EnumerationFlags* \[ In\]
</dt> <dd>

Gibt an, welche Routen aufzählt werden sollen. Dieser Parameter beschränkt den Satz von Routen, die von der Enumerations-API zurückgegeben werden, auf eine Teilmenge, die durch die folgenden Flags definiert wird, und auf die Werte in den entsprechenden Membern der -Struktur, auf die der *CriteriaRoute-Parameter* zeigt. Dieser Parameter kann einen der folgenden Werte annehmen.



| EnumerationFlags                                                                                                                                                                              | Bedeutung                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_ONLY_THIS_NETWORK"></span><span id="rtm_only_this_network"></span><dl> <dt>**NUR \_ DIESES \_ NETZWERK RTM \_**</dt> </dl>       | Enumerieren Sie nur die Routen, die dieselbe Netzwerknummer wie das RR-Netzwerkmitglied der Struktur haben, auf die \_ von CriteriaRoute verwiesen wird.<br/>                        |
| <span id="RTM_ONLY_THIS_INTERFACE"></span><span id="rtm_only_this_interface"></span><dl> <dt>**NUR RTM \_ \_ DIESE \_ SCHNITTSTELLE**</dt> </dl> | Enumerieren Sie nur die Routen, die über die schnittstelle ermittelt wurden, die durch das Feld RR InterfaceID der Struktur angegeben wird, auf die \_ von CriteriaRoute verwiesen wird.<br/>    |
| <span id="RTM_ONLY_THIS_PROTOCOL"></span><span id="rtm_only_this_protocol"></span><dl> <dt>**NUR \_ RTM \_ DIESES \_ PROTOKOLL**</dt> </dl>    | Enumerieren Sie nur die Routen, die durch das Routingprotokoll hinzugefügt wurden, das durch das RR RoutingProtocol-Feld der Struktur angegeben wird, auf die \_ von CriteriaRoute verwiesen wird.<br/> |
| <span id="RTM_ONLY_BEST_ROUTES"></span><span id="rtm_only_best_routes"></span><dl> <dt>**NUR RTM \_ \_ – BESTE \_ ROUTEN**</dt> </dl>          | Enumerieren Sie nur die besten Routen zu jedem der Netzwerke in der Gruppe.<br/>                                                                                           |



 

</dd> <dt>

*CriteriaRoute* \[ In\]
</dt> <dd>

Zeiger auf eine protokollfamilienspezifische Routenstruktur ([**RTM \_ IP \_ ROUTE**](rtm-ip-route.md) oder [**RTM \_ IPX \_ ROUTE**](rtm-ipx-route.md)). Die Memberwerte in dieser Struktur entsprechen den Flags, die durch den *EnumerationFlags-Parameter angegeben* werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein **HANDLE,** das bei nachfolgenden Enumerationsaufrufen verwendet werden soll.

Wenn die Funktion fehlschlägt oder keine Routen mit den angegebenen Kriterien vorhanden sind, ist der Rückgabewert **NULL.** Rufen [**Sie GetLastError auf,**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) um weitere Informationen zu erhalten.



| Wert                                                                                                       | BESCHREIBUNG                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**FEHLER: \_ KEINE \_ ROUTEN**</dt> </dl>            | Es gibt keine Routen mit den angegebenen Kriterien.<br/>                                                             |
| <dl> <dt>**FEHLER \_ UNGÜLTIGER \_ PARAMETER**</dt> </dl>    | Mindestens einer der Eingabeparameter ist ungültig (z. B. unbekannte Protokollfamilie, ungültige Enumerationsflags).<br/> |
| <dl> <dt>**FEHLER: \_ \_ KEINE \_ SYSTEMRESSOURCEN**</dt> </dl> | Es sind nicht genügend Ressourcen zum Durchführen des Vorgangs verfügbar.<br/>                                                      |
| <dl> <dt>**FEHLER: \_ NICHT \_ GENÜGEND \_ ARBEITSSPEICHER**</dt> </dl>   | Es ist nicht genügend Arbeitsspeicher zum Zuordnen des Handles verfügbar.<br/>                                                              |



 

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

[**\_RTM-IP-ROUTE \_**](rtm-ip-route.md)
</dt> <dt>

[**\_RTM-IPX-ROUTE \_**](rtm-ipx-route.md)
</dt> <dt>

[**RtmCloseEnumerationHandle**](rtmcloseenumerationhandle.md)
</dt> <dt>

[**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md)
</dt> </dl>

 

