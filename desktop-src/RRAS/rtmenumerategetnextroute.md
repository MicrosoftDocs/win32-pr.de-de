---
title: RtmEnumerateGetNextRoute-Funktion (Rtm.h)
description: Die RtmEnumerateGetNextRoute-Funktion gibt den Eintrag der nächsten Route in der Enumeration zurück, der durch einen Aufruf von RtmCreateEnumerationHandle gestartet wurde.
ms.assetid: fff6fb58-8a37-49f0-abc5-354b5bc340f8
keywords:
- RtmEnumerateGetNextRoute-Funktion RAS
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
ms.openlocfilehash: 6105340003c6240b49acec4699fa7b229d11963116367ab0fa0c069211b6fd1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035870"
---
# <a name="rtmenumerategetnextroute-function"></a>RtmEnumerateGetNextRoute-Funktion

\[Diese API wurde durch die [RoutingTabellen-Manager-API Version 2](about-routing-table-manager-version-2.md) ersetzt und ist über Windows Server 2003 hinaus nicht mehr verfügbar. Anwendungen sollten die Routingtabellen-Manager-API Version 2 verwenden.\]

Die **RtmEnumerateGetNextRoute-Funktion** gibt den Next-Route-Eintrag in der -Enumeration zurück, der durch einen Aufruf von [**RtmCreateEnumerationHandle gestartet wurde.**](rtmcreateenumerationhandle.md)

## <a name="syntax"></a>Syntax


```C++
DWORD RtmEnumerateGetNextRoute(
  _In_  HANDLE EnumerationHandle,
  _Out_ PVOID  Route
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*EnumerationHandle* \[ In\]
</dt> <dd>

Handle, das die Enumeration identifiziert und ihren Bereich angibt. Rufen Sie dieses Handle ab, [**indem Sie RtmCreateEnumerationHandle aufrufen.**](rtmcreateenumerationhandle.md)

</dd> <dt>

*Route* \[ out\]
</dt> <dd>

Zeiger auf eine protokollfamilienspezifische Routenstruktur ( [**RTM \_ IP \_ ROUTE**](rtm-ip-route.md) oder [**RTM \_ IPX \_ ROUTE**](rtm-ipx-route.md)). Diese Struktur erhält die nächste Route in der -Enumeration.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert NO \_ ERROR.

Wenn die Funktion fehlschlägt, ist der Rückgabewert einer der folgenden Fehlercodes.



| Wert                                                                                                       | BESCHREIBUNG                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**FEHLER \_ UNGÜLTIGES \_ HANDLE**</dt> </dl>       | Der *EnumerationHandle-Parameter* ist ungültig.<br/>              |
| <dl> <dt>**FEHLER: \_ \_ KEINE ROUTEN \_ MEHR**</dt> </dl>      | Die -Enumeration enthält keine Routen mehr.<br/>                 |
| <dl> <dt>**FEHLER: \_ \_ KEINE \_ SYSTEMRESSOURCEN**</dt> </dl> | Es sind nicht genügend Ressourcen zum Durchführen des Vorgangs verfügbar.<br/> |



 

## <a name="remarks"></a>Hinweise

Obwohl Routen nicht in einer bestimmten Reihenfolge zurückgegeben werden, wird jede Route in der -Enumeration nur einmal zurückgegeben.

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

[**\_RTM-IP-ROUTE \_**](rtm-ip-route.md)
</dt> <dt>

[**\_RTM-IPX-ROUTE \_**](rtm-ipx-route.md)
</dt> <dt>

[**RtmCloseEnumerationHandle**](rtmcloseenumerationhandle.md)
</dt> <dt>

[**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md)
</dt> </dl>

 

 





