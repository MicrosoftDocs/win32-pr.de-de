---
description: Wird aufgerufen, wenn der aktuelle Benutzer die Umstellung seiner Benutzeridentität angefordert hat, aber bevor der Wechsel erfolgt.
ms.assetid: f159b829-623c-4348-9692-7317663811a7
title: IIdentityChangeNotify::QuerySwitchIdentities-Methode (Msident.h)
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
ms.openlocfilehash: 38469490db92278c82e7935e1078181010757dd22be220203361d2d4c18ef380
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593080"
---
# <a name="iidentitychangenotifyqueryswitchidentities-method"></a>IIdentityChangeNotify::QuerySwitchIdentities-Methode

\[**QuerySwitchIdentities steht** für die Verwendung in den Betriebssystemen zur Verfügung, die im Abschnitt Anforderungen angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden.\]

Wird aufgerufen, wenn der aktuelle Benutzer die Umstellung seiner Benutzeridentität angefordert hat, aber bevor der Wechsel erfolgt.

## <a name="syntax"></a>Syntax


```C++
HRESULT QuerySwitchIdentities();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Ergebnis der Switchabfrage. Wenn der Schalter fortgesetzt werden soll, geben Sie S \_ OK zurück. Geben Sie andernfalls E \_ PROCESS \_ CANCELLED SWITCH zurück, um anzugeben, dass der Benutzeridentitätswechsel \_ abgebrochen werden soll.

## <a name="remarks"></a>Hinweise

Sie können diese Methode implementieren, um benutzerdefiniertes Verhalten für Ihre Anwendung zu bieten, wenn ein Benutzer das Wechseln von Identitäten an fordert. Sie können den ausstehenden Identitätswechsel beenden, indem Sie den Wert E \_ PROCESS \_ CANCELLED SWITCH \_ zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Ende des Supports (Client)<br/>    | Windows 2000 Professional<br/>                                                   |
| Ende des Supports (Server)<br/>    | Windows 2000 Server<br/>                                                         |
| Header<br/>                   | <dl> <dt>Msident.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msident.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msoe.dll</dt> </dl>    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IIdentityChangeNotify**](iidentitychangenotify.md)
</dt> <dt>

[**IIdentityChangeNotify::SwitchIdentities**](iidentitychangenotify-switchidentities.md)
</dt> </dl>

 

 




