---
title: RtmDeregisterClient-Funktion (Rtm.h)
description: Die RtmDeregisterClient-Funktion deregistriert den Client und gibt dem Client zugeordnete Ressourcen frei.
ms.assetid: 5d04f276-86a7-4e63-8266-e93f0d6e5241
keywords:
- RtmDeregisterClient-Funktion RAS
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
ms.openlocfilehash: a7df18a4fffa2bdc038aaeb980b76523448e33cca5b7f2e2d558720a5cc9a2c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073860"
---
# <a name="rtmderegisterclient-function"></a>RtmDeregisterClient-Funktion

\[Diese API wurde durch die [RoutingTabellen-Manager-API Version 2](about-routing-table-manager-version-2.md) ersetzt und ist über Windows Server 2003 hinaus nicht mehr verfügbar. Anwendungen sollten die Routingtabellen-Manager-API Version 2 verwenden.\]

Die **RtmDeregisterClient-Funktion** deregistriert den Client und gibt dem Client zugeordnete Ressourcen frei.

## <a name="syntax"></a>Syntax


```C++
DWORD RtmDeregisterClient(
  _In_ HANDLE ClientHandle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ClientHandle* \[ In\]
</dt> <dd>

Handle, das den zu registrierenden Client identifiziert. Rufen Sie dieses Handle ab, indem [**Sie RtmRegisterClient aufrufen.**](rtmregisterclient.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert NO \_ ERROR.

Wenn die Funktion fehlschlägt, ist der Rückgabewert einer der folgenden Fehlercodes.



| Wert                                                                                                       | BESCHREIBUNG                                                    |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**FEHLER \_ UNGÜLTIGES \_ HANDLE**</dt> </dl>       | Der *ClientHandle-Parameter* ist kein gültiges Handle.<br/> |
| <dl> <dt>**FEHLER: \_ \_ KEINE \_ SYSTEMRESSOURCEN**</dt> </dl> | Unzureichende Ressourcen zum Durchführen des Vorgangs.<br/>  |



 

## <a name="remarks"></a>Hinweise

Diese Funktion entfernt alle Routen, die vom Client hinzugefügt wurden.

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

[Routing Table Manager Version 1 Reference](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Routingtabellen-Manager- Version 1-Funktionen](routing-table-manager-version-1-functions.md)
</dt> <dt>

[**RtmRegisterClient**](rtmregisterclient.md)
</dt> </dl>

 

 





