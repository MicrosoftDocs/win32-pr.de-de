---
title: Rtmderegisterclient-Funktion (RTM. h)
description: Die Funktion rtmderegisterclient hebt die Registrierung des Clients auf und gibt die dem Client zugeordneten Ressourcen frei.
ms.assetid: 5d04f276-86a7-4e63-8266-e93f0d6e5241
keywords:
- Rtmderegisterclient-Funktion (RAS)
topic_type:
- apiref
api_name:
- RtmDeregisterClient
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ab1f56d3d65e13c083d8952f500cfba4638ab83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391901"
---
# <a name="rtmderegisterclient-function"></a>Rtmderegisterclient-Funktion

\[Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar. Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.\]

Die Funktion **rtmderegisterclient** hebt die Registrierung des Clients auf und gibt die dem Client zugeordneten Ressourcen frei.

## <a name="syntax"></a>Syntax


```C++
DWORD RtmDeregisterClient(
  _In_ HANDLE ClientHandle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Clienthandle* \[ in\]
</dt> <dd>

Handle, das den Client identifiziert, dessen Registrierung aufgehoben werden soll. Rufen Sie dieses Handle durch Aufrufen von [**rtmregisterclient**](rtmregisterclient.md)ab.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert kein \_ Fehler.

Wenn die Funktion fehlschlägt, ist der Rückgabewert einer der folgenden Fehlercodes.



| Wert                                                                                                       | BESCHREIBUNG                                                    |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**Fehler bei \_ ungültigem \_ handle**</dt> </dl>       | Der *Clienthandle* -Parameter ist kein gültiges Handle.<br/> |
| <dl> <dt>**Fehler \_ keine \_ System \_ Ressourcen**</dt> </dl> | Nicht genügend Ressourcen, um den Vorgang auszuführen.<br/>  |



 

## <a name="remarks"></a>Bemerkungen

Diese Funktion entfernt alle Routen, die vom Client hinzugefügt wurden.

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

[**Rtmregisterclient**](rtmregisterclient.md)
</dt> </dl>

 

 





