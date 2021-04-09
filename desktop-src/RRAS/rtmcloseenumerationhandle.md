---
title: Rtmcloseenumerationhandle-Funktion (RTM. h)
description: Das rtmcloseenumerationhandle beendet eine angegebene Enumeration und gibt die zugeordneten Ressourcen frei.
ms.assetid: 8daea42f-4304-4749-9894-d37f6ba733da
keywords:
- Rtmcloseenumerationhandle-Funktion (RAS)
topic_type:
- apiref
api_name:
- RtmCloseEnumerationHandle
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5adb47d40cb1300305c7ff6f9bb6f1c3c716f0f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040753"
---
# <a name="rtmcloseenumerationhandle-function"></a>Rtmcloseenumerationhandle-Funktion

\[Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar. Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.\]

Das **rtmcloseenumerationhandle** beendet eine angegebene Enumeration und gibt die zugeordneten Ressourcen frei.

## <a name="syntax"></a>Syntax


```C++
DWORD RtmCloseEnumerationHandle(
  _In_ HANDLE EnumerationHandle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Enumerationhandle* \[ in\]
</dt> <dd>

Handle für die zu beendende Enumeration. Rufen Sie dieses Handle durch Aufrufen von [**rtmcreateenumerationhandle**](rtmcreateenumerationhandle.md)ab.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert kein \_ Fehler.

Wenn die Funktion fehlschlägt, ist der Rückgabewert einer der folgenden Fehlercodes.



| Wert                                                                                                       | BESCHREIBUNG                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**Fehler bei \_ ungültigem \_ handle**</dt> </dl>       | Der Parameter ist ungültig.<br/>                                  |
| <dl> <dt>**Fehler \_ keine \_ System \_ Ressourcen**</dt> </dl> | Es sind nicht genügend Ressourcen vorhanden, um den Vorgang auszuführen.<br/> |



 

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

[**Rtmenumschlag-ategetnextroute**](rtmenumerategetnextroute.md)
</dt> </dl>

 

 





