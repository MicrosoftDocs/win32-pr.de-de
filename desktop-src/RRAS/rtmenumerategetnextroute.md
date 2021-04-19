---
title: Rtmenenerategetnextroute-Funktion (RTM. h)
description: Die rtmenumerategetnextroute-Funktion gibt den Eintrag für die nächste Route in der Enumeration zurück, die durch einen Aufruf von rtmkreateenumerationhandle gestartet wird.
ms.assetid: fff6fb58-8a37-49f0-abc5-354b5bc340f8
keywords:
- Rtmenumschlag-Funktion (RAS)
topic_type:
- apiref
api_name:
- RtmEnumerateGetNextRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e74cc5aa15c1014056075e876efca296556066d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339989"
---
# <a name="rtmenumerategetnextroute-function"></a>Rtmenenerategetnextroute-Funktion

\[Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar. Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.\]

Die **rtmenumerategetnextroute** -Funktion gibt den Eintrag für die nächste Route in der Enumeration zurück, die durch einen Aufruf von [**rtmkreateenumerationhandle**](rtmcreateenumerationhandle.md)gestartet wird.

## <a name="syntax"></a>Syntax


```C++
DWORD RtmEnumerateGetNextRoute(
  _In_  HANDLE EnumerationHandle,
  _Out_ PVOID  Route
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Enumerationhandle* \[ in\]
</dt> <dd>

Handle, das die Enumeration identifiziert und den Gültigkeitsbereich angibt. Rufen Sie dieses Handle durch Aufrufen von [**rtmcreateenumerationhandle**](rtmcreateenumerationhandle.md)ab.

</dd> <dt>

*Route* \[ vorgenommen\]
</dt> <dd>

Zeiger auf eine Protokoll familienspezifische Routen Struktur ( [**RTM \_ -IP- \_ Route**](rtm-ip-route.md) oder [**RTM \_ IPX- \_ Route**](rtm-ipx-route.md)). Diese Struktur empfängt die nächste Route in der-Enumeration.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert kein \_ Fehler.

Wenn die Funktion fehlschlägt, ist der Rückgabewert einer der folgenden Fehlercodes.



| Wert                                                                                                       | BESCHREIBUNG                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**Fehler bei \_ ungültigem \_ handle**</dt> </dl>       | Der *enumerationhandle* -Parameter ist ungültig.<br/>              |
| <dl> <dt>**Fehler \_ keine \_ weiteren \_ Routen**</dt> </dl>      | In der-Enumeration sind keine weiteren Routen vorhanden.<br/>                 |
| <dl> <dt>**Fehler \_ keine \_ System \_ Ressourcen**</dt> </dl> | Es sind nicht genügend Ressourcen vorhanden, um den Vorgang auszuführen.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Obwohl Routen nicht in einer bestimmten Reihenfolge zurückgegeben werden, wird jede Route in der Enumeration nur einmal zurückgegeben.

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

[**RTM \_ -IP- \_ Route**](rtm-ip-route.md)
</dt> <dt>

[**RTM- \_ IPX- \_ Route**](rtm-ipx-route.md)
</dt> <dt>

[**Rtmcloseenumerationhandle**](rtmcloseenumerationhandle.md)
</dt> <dt>

[**Rtmkreateenumerationhandle**](rtmcreateenumerationhandle.md)
</dt> </dl>

 

 





