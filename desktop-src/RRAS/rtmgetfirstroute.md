---
title: Rtmgetfirstroute-Funktion (RTM. h)
description: Die rtmgetfirstroute-Funktion gibt die erste Route von der angegebenen Teilmenge der Routen in der Tabelle zurück.
ms.assetid: f2071b50-4b06-432f-8dbf-45696f8a5cb1
keywords:
- Rtmgetfirstroute-Funktion (RAS)
topic_type:
- apiref
api_name:
- RtmGetFirstRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32e98a5deb0f925fbf3b27c21302060bbe4869b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104385"
---
# <a name="rtmgetfirstroute-function"></a>Rtmgetfirstroute-Funktion

\[Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar. Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.\]

Die **rtmgetfirstroute** -Funktion gibt die erste Route von der angegebenen Teilmenge der Routen in der Tabelle zurück.

## <a name="syntax"></a>Syntax


```C++
DWORD RtmGetFirstRoute(
  _In_    DWORD ProtocolFamily,
  _In_    DWORD EnumerationFlags,
  _Inout_ PVOID Route
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ProtocolFamily* \[ in\]
</dt> <dd>

Gibt die Protokollfamilie der abzurufenden Routen an, z. b. IP oder IPX.

</dd> <dt>

*Enumerationflags* \[ in\]
</dt> <dd>

Gibt an, dass den Satz gelöschter Routen auf eine Teilmenge beschränkt, die durch diese Flags definiert ist, sowie die Werte in den entsprechenden Membern der Struktur, auf die durch den *Kriterienparameter* verwiesen wird. Die Flags sind identisch mit denen, die in [**rtmkreateenumerationhandle**](rtmcreateenumerationhandle.md)verwendet werden.

</dd> <dt>

*Route* \[ in, out\]
</dt> <dd>

Bei der Eingabe verweist die *Route* auf eine Protokoll familienspezifische Struktur ( [**RTM- \_ IP- \_ Route**](rtm-ip-route.md) oder [**RTM \_ IPX- \_ Route**](rtm-ipx-route.md)).

Die Aufruf Funktion stellt Element Werte für diese-Struktur bereit. Diese Werte geben in Verbindung mit dem *enumerationflags* -Parameter den Satz an, aus dem Routen zurückgegeben werden.

Ausgabe, *Route* verweist auf die erste Route, die mit den angegebenen Kriterien übereinstimmt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert kein \_ Fehler.

Wenn die Funktion fehlschlägt, ist der Rückgabewert einer der folgenden Fehlercodes.



| Wert                                                                                                       | BESCHREIBUNG                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**Fehler bei \_ ungültigem \_ Parameter**</dt> </dl>    | Einer der Parameter ist ungültig.<br/>                            |
| <dl> <dt>**Fehler \_ ohne \_ Routen**</dt> </dl>            | Es sind keine Routen vorhanden, die den angegebenen Kriterien entsprechen.<br/>       |
| <dl> <dt>**Fehler \_ keine \_ System \_ Ressourcen**</dt> </dl> | Es sind nicht genügend Ressourcen vorhanden, um den Vorgang auszuführen.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die Routen werden in der folgenden Reihenfolge zurückgegeben:

1.  Netzwerk Nummer
2.  Routing Protokoll
3.  Schnittstellen-ID
4.  Adresse des nächsten Hops

Diese Funktion ist weniger effizient als die entsprechende [**enumerationshandle-Funktion rtmenumerategetnextroute**](rtmenumerategetnextroute.md).

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

[**Rtmcloseenumerationhandle**](rtmcloseenumerationhandle.md)
</dt> <dt>

[**Rtmkreateenumerationhandle**](rtmcreateenumerationhandle.md)
</dt> <dt>

[**Rtmenumschlag-ategetnextroute**](rtmenumerategetnextroute.md)
</dt> <dt>

[**Rtmgetnextroute**](rtmgetnextroute.md)
</dt> </dl>

 

 





