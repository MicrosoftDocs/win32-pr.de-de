---
title: RtmBlockDeleteRoutes-Funktion (Rtm.h)
description: Die RtmBlockDeleteRoutes-Funktion löscht alle Routen in der angegebenen Teilmenge der Routen in der Tabelle.
ms.assetid: d191883d-da3d-4a91-92e6-4979db96f4a4
keywords:
- RtmBlockDeleteRoutes-Funktion RAS
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
ms.openlocfilehash: f830603bba4bcdf07bd7bc8c631ac17028301a795fc14ebbce6483ef72f81361
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073880"
---
# <a name="rtmblockdeleteroutes-function"></a>RtmBlockDeleteRoutes-Funktion

\[Diese API wurde durch die [RoutingTabellen-Manager-API Version 2](about-routing-table-manager-version-2.md) ersetzt und ist über Windows Server 2003 hinaus nicht mehr verfügbar. Anwendungen sollten die Routingtabellen-Manager-API Version 2 verwenden.\]

Die **RtmBlockDeleteRoutes-Funktion** löscht alle Routen in der angegebenen Teilmenge der Routen in der Tabelle.

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

*ClientHandle* \[ In\]
</dt> <dd>

Handle, das den Client und somit das Routingprotokoll der zu löschenden Routen identifiziert.

</dd> <dt>

*EnumerationFlags* \[ In\]
</dt> <dd>

Gibt an, welche Routen aufzählt werden sollen. Dieser Parameter beschränkt den Satz gelöschter Routen auf eine Teilmenge, die durch die folgenden Flags definiert wird, und auf die Werte in den entsprechenden Membern der -Struktur, auf die der *CriteriaRoute-Parameter zeigt.* Die Flags sind mit denen identisch, die in [**RtmCreateEnumerationHandle verwendet**](rtmcreateenumerationhandle.md) werden, mit der Ausnahme, dass RTM \_ ONLY BEST ROUTES für \_ \_ **RtmBlockDeleteRoutes redundant ist.** Die Bezeichnung der besten Route wird angepasst, wenn Routen gelöscht werden, sodass die Funktion schließlich alle Routen in der Teilmenge löscht.

</dd> <dt>

*CriteriaRoute* \[ In\]
</dt> <dd>

Zeiger auf eine protokollfamilienspezifische Routenstruktur ( [**RTM \_ IP \_ ROUTE**](rtm-ip-route.md) oder [**RTM \_ IPX \_ ROUTE**](rtm-ipx-route.md)). Die Memberwerte in dieser Struktur entsprechen den Flags, die durch den *EnumerationFlags-Parameter angegeben* werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert NO \_ ERROR.

Wenn die Funktion fehlschlägt, ist der Rückgabewert einer der folgenden Fehlercodes.



| Wert                                                                                                       | BESCHREIBUNG                                                                                                |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**FEHLER: \_ KEINE \_ ROUTEN**</dt> </dl>            | Es gibt keine Routen mit den angegebenen Kriterien.<br/>                                           |
| <dl> <dt>**FEHLER \_ UNGÜLTIGES \_ HANDLE**</dt> </dl>       | Der *ClientHandle-Parameter* ist ungültig.<br/>                                                      |
| <dl> <dt>**FEHLER \_ UNGÜLTIGER \_ PARAMETER**</dt> </dl>    | Mindestens einer der Eingabeparameter ist ungültig, z. B. sind die Enumerationsflags ungültig.<br/> |
| <dl> <dt>**FEHLER: \_ \_ KEINE \_ SYSTEMRESSOURCEN**</dt> </dl> | Es sind nicht genügend Ressourcen zum Durchführen des Vorgangs verfügbar.<br/>                                    |
| <dl> <dt>**FEHLER: \_ NICHT \_ GENÜGEND \_ ARBEITSSPEICHER**</dt> </dl>   | Es ist nicht genügend Arbeitsspeicher verfügbar, um den Vorgang durchführen zu können.<br/>                                        |



 

## <a name="remarks"></a>Hinweise

Die Funktion generiert entsprechende Benachrichtigungsmeldungen an alle registrierten Clients, einschließlich des Aufrufers.

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

[**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md)
</dt> <dt>

[**RtmRegisterClient**](rtmregisterclient.md)
</dt> </dl>

 

 





