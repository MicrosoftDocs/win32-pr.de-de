---
title: Rtmkreateenumerationhandle-Funktion (RTM. h)
description: Die rtmkreateenumerationhandle-Funktion gibt ein Handle zurück, das mit rtmenumerategetnextroute verwendet werden kann, um alle Routen oder eine Teilmenge der Routen zu durchsuchen, die dem Routing Tabellen-Manager bekannt sind.
ms.assetid: 73e3ac7d-498a-4d89-a6b5-17aaf4b17ec2
keywords:
- Rtmkreateenumerationhandle-Funktion (RAS)
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
ms.openlocfilehash: 14086639db299038139e0e7d02eb12bb892042bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103115"
---
# <a name="rtmcreateenumerationhandle-function"></a>Rtmkreateenumerationhandle-Funktion

\[Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar. Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.\]

Die **rtmkreateenumerationhandle** -Funktion gibt ein Handle zurück, das mit [**rtmenumerategetnextroute**](rtmenumerategetnextroute.md) verwendet werden kann, um alle Routen oder eine Teilmenge der Routen zu durchsuchen, die dem Routing Tabellen-Manager bekannt sind.

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

*ProtocolFamily* \[ in\]
</dt> <dd>

Gibt die Protokollfamilie der aufzuzählenden Routen an.

</dd> <dt>

*Enumerationflags* \[ in\]
</dt> <dd>

Gibt an, welche Routen aufgelistet werden sollen. Mit diesem Parameter wird der von der enumerationsapi zurückgegebene Satz von Routen auf eine Teilmenge beschränkt, die durch die folgenden Flags definiert ist, sowie auf die Werte in den entsprechenden Membern der Struktur, auf die durch den *Kriterium* -Parameter verwiesen wird. Dieser Parameter kann einen der folgenden Werte annehmen.



| Enumerationflags                                                                                                                                                                              | Bedeutung                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_ONLY_THIS_NETWORK"></span><span id="rtm_only_this_network"></span><dl> <dt>**\_nur \_ dieses \_ Netzwerk RTM**</dt> </dl>       | Listet nur die Routen auf, die die gleiche Netzwerk Nummer wie das RR- \_ netzwerkmember der Struktur aufweisen, auf die von Criteria verwiesen wird.<br/>                        |
| <span id="RTM_ONLY_THIS_INTERFACE"></span><span id="rtm_only_this_interface"></span><dl> <dt>**\_nur \_ diese \_ Schnittstelle für RTM**</dt> </dl> | Listet nur die Routen auf, die durch die Schnittstelle abgerufen wurden, die durch das RR- \_ interfakeid-Feld der Struktur abgerufen wurde, auf die von Criteria verwiesen wird.<br/>    |
| <span id="RTM_ONLY_THIS_PROTOCOL"></span><span id="rtm_only_this_protocol"></span><dl> <dt>**\_nur \_ dieses \_ Protokoll für RTM**</dt> </dl>    | Enumerieren Sie nur die Routen, die durch das Routing Protokoll hinzugefügt wurden, das durch das \_ Feld RR routingprotocol der Struktur, auf die durch Kriterienwerte verwiesen wird, angegeben wurden.<br/> |
| <span id="RTM_ONLY_BEST_ROUTES"></span><span id="rtm_only_best_routes"></span><dl> <dt>**RTM hat \_ nur die \_ besten \_ Routen**</dt> </dl>          | Listet nur die optimalen Routen zu den einzelnen Netzwerken in der Gruppe auf.<br/>                                                                                           |



 

</dd> <dt>

*Kriterien* \[ in\]
</dt> <dd>

Zeiger auf eine Protokoll familienspezifische Routen Struktur ([**RTM \_ -IP- \_ Route**](rtm-ip-route.md) oder [**RTM \_ IPX- \_ Route**](rtm-ipx-route.md)). Die Element Werte in dieser Struktur entsprechen den Flags, die durch den *enumerationflags* -Parameter angegeben werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein **handle** , das bei nachfolgenden enumerationsaufrufen verwendet werden soll.

Wenn die Funktion fehlschlägt oder keine Routen mit den angegebenen Kriterien vorhanden sind, ist der Rückgabewert **null**. Rufen Sie [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf, um weitere Informationen zu erhalten.



| Wert                                                                                                       | BESCHREIBUNG                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Fehler \_ ohne \_ Routen**</dt> </dl>            | Es sind keine Routen vorhanden, die die angegebenen Kriterien aufweisen.<br/>                                                             |
| <dl> <dt>**Fehler bei \_ ungültigem \_ Parameter**</dt> </dl>    | Mindestens ein Eingabeparameter ist ungültig (z. b. unbekannte Protokollfamilie, ungültige Enumerationsflags).<br/> |
| <dl> <dt>**Fehler \_ keine \_ System \_ Ressourcen**</dt> </dl> | Es sind nicht genügend Ressourcen vorhanden, um den Vorgang auszuführen.<br/>                                                      |
| <dl> <dt>**Fehler \_ nicht \_ genügend Arbeits \_ Speicher**</dt> </dl>   | Es ist nicht genügend Arbeitsspeicher vorhanden, um das Handle zuzuordnen.<br/>                                                              |



 

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

[**RTM \_ -IP- \_ Route**](rtm-ip-route.md)
</dt> <dt>

[**RTM- \_ IPX- \_ Route**](rtm-ipx-route.md)
</dt> <dt>

[**Rtmcloseenumerationhandle**](rtmcloseenumerationhandle.md)
</dt> <dt>

[**Rtmenumschlag-ategetnextroute**](rtmenumerategetnextroute.md)
</dt> </dl>

 

