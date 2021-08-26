---
title: RtmCloseEnumerationHandle-Funktion (Rtm.h)
description: RtmCloseEnumerationHandle beendet eine angegebene Enumeration und gibt die zugeordneten Ressourcen frei.
ms.assetid: 8daea42f-4304-4749-9894-d37f6ba733da
keywords:
- RTMCloseEnumerationHandle-Funktion RAS
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
ms.openlocfilehash: 0313cc594b0629509ffcee65ea333caa9dbc373de323dc656a6028bc26e14317
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081050"
---
# <a name="rtmcloseenumerationhandle-function"></a>RtmCloseEnumerationHandle-Funktion

\[Diese API wurde von der Routing Table Manager Version [2-API](about-routing-table-manager-version-2.md) abgelöst und ist nicht mehr als Windows Server 2003 verfügbar. Anwendungen sollten die Routing Table Manager Version 2-API verwenden.\]

**RtmCloseEnumerationHandle** beendet eine angegebene Enumeration und gibt die zugeordneten Ressourcen frei.

## <a name="syntax"></a>Syntax


```C++
DWORD RtmCloseEnumerationHandle(
  _In_ HANDLE EnumerationHandle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*EnumerationHandle* \[ In\]
</dt> <dd>

Handle für die zu beendende Enumeration. Rufen Sie dieses Handle ab, indem [**Sie RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md)aufrufen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert NO \_ ERROR.

Wenn die Funktion fehlschlägt, ist der Rückgabewert einer der folgenden Fehlercodes.



| Wert                                                                                                       | BESCHREIBUNG                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**FEHLER: \_ UNGÜLTIGES \_ HANDLE**</dt> </dl>       | Der Parameter ist ungültig.<br/>                                  |
| <dl> <dt>**FEHLER \_ KEINE \_ \_ SYSTEMRESSOURCEN**</dt> </dl> | Es sind nicht genügend Ressourcen vorhanden, um den Vorgang auszuführen.<br/> |



 

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

[**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md)
</dt> <dt>

[**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md)
</dt> </dl>

 

 





