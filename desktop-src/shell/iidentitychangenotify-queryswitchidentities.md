---
description: Wird aufgerufen, wenn der aktuelle Benutzer angefordert hat, dass die Benutzeridentität gewechselt wird, jedoch bevor der Switch auftritt.
ms.assetid: f159b829-623c-4348-9692-7317663811a7
title: 'Iidentitychangenotify:: queryswitchidentities-Methode (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify.QuerySwitchIdentities
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: 42f8033c943e402d434c973f8c768ed5a951811d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864900"
---
# <a name="iidentitychangenotifyqueryswitchidentities-method"></a>Iidentitychangenotify:: queryswitchidentities-Methode

\[**Queryswitchidentities** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden.\]

Wird aufgerufen, wenn der aktuelle Benutzer angefordert hat, dass die Benutzeridentität gewechselt wird, jedoch bevor der Switch auftritt.

## <a name="syntax"></a>Syntax


```C++
HRESULT QuerySwitchIdentities();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Ergebnis der Switch-Abfrage. Wenn der Switch fortgesetzt werden soll, geben Sie S \_ OK zurück. Andernfalls wird \_ der Schalter E-Prozess abgebrochen zurückgegeben, \_ \_ um anzugeben, dass der Benutzer Identitätswechsel abgebrochen werden soll.

## <a name="remarks"></a>Bemerkungen

Sie können diese Methode implementieren, um benutzerdefiniertes Verhalten für Ihre Anwendung bereitzustellen, wenn ein Benutzer anfordert, dass Identitäten gewechselt werden. Sie können den ausstehenden Identitätswechsel abbrechen, indem Sie den Schalter Wert E \_ Prozess \_ abgebrochen zurückgeben \_ .

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Ende des Supports (Client)<br/>    | Windows 2000 Professional<br/>                                                   |
| Ende des Supports (Server)<br/>    | Windows 2000 Server<br/>                                                         |
| Header<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msoe.dll</dt> </dl>    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Iidentitychangenotify**](iidentitychangenotify.md)
</dt> <dt>

[**Iidentitychangenotify:: switchidentities**](iidentitychangenotify-switchidentities.md)
</dt> </dl>

 

 




