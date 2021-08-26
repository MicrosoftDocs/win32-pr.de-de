---
title: RtmGetNextRoute-Funktion (Rtm.h)
description: Die RtmGetNextRoute-Funktion gibt die nächste Route aus der angegebenen Teilmenge der Routen in der Tabelle zurück.
ms.assetid: 0f413276-2ace-4216-a1a0-1b3061bacc4a
keywords:
- RtmGetNextRoute-Funktion RAS
topic_type:
- apiref
api_name:
- RtmGetNextRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec33ff5932d40a146811056d74ca3b91f0bdbfdd772a04a2d7392390d63209e3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073820"
---
# <a name="rtmgetnextroute-function"></a>RtmGetNextRoute-Funktion

\[Diese API wurde von der Routing Table Manager Version [2-API](about-routing-table-manager-version-2.md) abgelöst und ist nicht mehr als Windows Server 2003 verfügbar. Anwendungen sollten die Routing Table Manager Version 2-API verwenden.\]

Die **RtmGetNextRoute-Funktion** gibt die nächste Route aus der angegebenen Teilmenge der Routen in der Tabelle zurück.

## <a name="syntax"></a>Syntax


```C++
DWORD RtmGetNextRoute(
  _In_    DWORD ProtocolFamily,
  _In_    DWORD EnumerationFlags,
  _Inout_ PVOID Route
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ProtocolFamily* \[ In\]
</dt> <dd>

Gibt die Protokollfamilie der abzurufenden Routen an, z. B. IP oder IPX.

</dd> <dt>

*EnumerationFlags* \[ In\]
</dt> <dd>

Gibt an, welche Routen aufzählt werden sollen. Dieser Parameter beschränkt den Satz gelöschter Routen auf eine Teilmenge, die durch die folgenden Flags und die Werte in den entsprechenden Membern der Struktur definiert wird, auf die der *CriteriaRoute-Parameter* zeigt. Die Flags sind identisch mit denen, die in [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md)verwendet werden.

</dd> <dt>

*Route* \[ in, out\]
</dt> <dd>

Bei der Eingabe verweist *Route* auf eine protokollfamilienspezifische Struktur ( [**RTM \_ IP \_ ROUTE**](rtm-ip-route.md) oder [**RTM \_ IPX \_ ROUTE**](rtm-ipx-route.md)).

Die aufrufende Funktion stellt Memberwerte für diese Struktur bereit. Diese Werte geben in Verbindung mit dem *EnumerationFlags-Parameter* den Satz an, von dem Routen zurückgegeben werden sollen.

Bei der Ausgabe verweist *Route* auf eine Struktur, die die erste Route empfängt, die den angegebenen Kriterien entspricht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert **NO \_ ERROR**.

Wenn die Funktion fehlschlägt, ist der Rückgabewert einer der folgenden Fehlercodes.



| Wert                                                                                                       | BESCHREIBUNG                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**FEHLER: \_ UNGÜLTIGER \_ PARAMETER**</dt> </dl>    | Einer der Parameter ist ungültig.<br/>                            |
| <dl> <dt>**FEHLER \_ KEINE \_ ROUTEN**</dt> </dl>            | Es gibt keine Routen, die den angegebenen Kriterien entsprechen.<br/>       |
| <dl> <dt>**FEHLER \_ KEINE \_ \_ SYSTEMRESSOURCEN**</dt> </dl> | Es sind nicht genügend Ressourcen vorhanden, um den Vorgang auszuführen.<br/> |



 

## <a name="remarks"></a>Hinweise

Die Routen werden in der folgenden Reihenfolge zurückgegeben:

1.  Netzwerknummer
2.  Routingprotokoll
3.  Schnittstellen-ID
4.  Adresse des nächsten Hops

Diese Funktion ist weniger effizient als die entsprechenden Enumerationshandlefunktionen.

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

[Referenz zu Routingtabellen-Manager, Version 1](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Funktionen des Routingtabellen-Managers, Version 1](routing-table-manager-version-1-functions.md)
</dt> <dt>

[**RtmCloseEnumerationHandle**](rtmcloseenumerationhandle.md)
</dt> <dt>

[**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md)
</dt> <dt>

[**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md)
</dt> <dt>

[**RtmGetFirstRoute**](rtmgetfirstroute.md)
</dt> </dl>

 

 





