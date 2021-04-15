---
title: Rtmblockdeleteroutes-Funktion (RTM. h)
description: Die rtmblockdeleteroutes-Funktion löscht alle Routen in der angegebenen Teilmenge der Routen in der Tabelle.
ms.assetid: d191883d-da3d-4a91-92e6-4979db96f4a4
keywords:
- Rtmblockdeleteroutes-Funktion (RAS)
topic_type:
- apiref
api_name:
- RtmBlockDeleteRoutes
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a71090371fe8a84698b84b84391e5a782fdc636f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477511"
---
# <a name="rtmblockdeleteroutes-function"></a>Rtmblockdeleteroutes-Funktion

\[Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar. Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.\]

Die **rtmblockdeleteroutes** -Funktion löscht alle Routen in der angegebenen Teilmenge der Routen in der Tabelle.

## <a name="syntax"></a>Syntax


```C++
HANDLE RtmBlockDeleteRoutes(
  _In_ HANDLE ClientHandle,
  _In_ DWORD  EnumerationFlags,
  _In_ PVOID  CriteriaRoute
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Clienthandle* \[ in\]
</dt> <dd>

Handle, das den Client und somit das Routing Protokoll der zu löschenden Routen identifiziert.

</dd> <dt>

*Enumerationflags* \[ in\]
</dt> <dd>

Gibt an, welche Routen aufgelistet werden sollen. Mit diesem Parameter wird der Satz gelöschter Routen auf eine Teilmenge beschränkt, die durch die folgenden Flags definiert ist, sowie auf die Werte in den entsprechenden Membern der Struktur, auf die durch den *Kriterienparameter* verwiesen wird. Die Flags sind identisch mit denen, die in [**rtmkreateenumerationhandle**](rtmcreateenumerationhandle.md) verwendet werden, mit dem Unterschied, dass RTM \_ \_ \_ für **rtmblockdeleteroutes** nur die besten Routen redundant ist. Die beste Routen Bezeichnung wird angepasst, wenn Routen gelöscht werden, sodass die Funktion schließlich alle Routen in der Teilmenge löscht.

</dd> <dt>

*Kriterien* \[ in\]
</dt> <dd>

Zeiger auf eine Protokoll familienspezifische Routen Struktur ( [**RTM \_ -IP- \_ Route**](rtm-ip-route.md) oder [**RTM \_ IPX- \_ Route**](rtm-ipx-route.md)). Die Element Werte in dieser Struktur entsprechen den Flags, die durch den *enumerationflags* -Parameter angegeben werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert kein \_ Fehler.

Wenn die Funktion fehlschlägt, ist der Rückgabewert einer der folgenden Fehlercodes.



| Wert                                                                                                       | BESCHREIBUNG                                                                                                |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Fehler \_ ohne \_ Routen**</dt> </dl>            | Es sind keine Routen vorhanden, die die angegebenen Kriterien aufweisen.<br/>                                           |
| <dl> <dt>**Fehler bei \_ ungültigem \_ handle**</dt> </dl>       | Der *Clienthandle* -Parameter ist ungültig.<br/>                                                      |
| <dl> <dt>**Fehler bei \_ ungültigem \_ Parameter**</dt> </dl>    | Mindestens ein Eingabeparameter ist ungültig, z. b. sind die Enumerationsflags ungültig.<br/> |
| <dl> <dt>**Fehler \_ keine \_ System \_ Ressourcen**</dt> </dl> | Es sind nicht genügend Ressourcen vorhanden, um den Vorgang auszuführen.<br/>                                    |
| <dl> <dt>**Fehler \_ nicht \_ genügend Arbeits \_ Speicher**</dt> </dl>   | Es ist nicht genügend Arbeitsspeicher vorhanden, um den Vorgang auszuführen.<br/>                                        |



 

## <a name="remarks"></a>Bemerkungen

Die Funktion generiert geeignete Benachrichtigungs Meldungen für alle registrierten Clients, einschließlich des Aufrufers.

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

[**Rtmkreateenumerationhandle**](rtmcreateenumerationhandle.md)
</dt> <dt>

[**Rtmregisterclient**](rtmregisterclient.md)
</dt> </dl>

 

 





