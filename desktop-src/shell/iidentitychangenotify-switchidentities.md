---
description: Wird aufgerufen, wenn Benutzer Identitäten gewechselt werden.
ms.assetid: e88383fc-e58e-4987-be4b-8ce2ab1368db
title: 'Iidentitychangenotify:: switchidentities-Methode (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify.SwitchIdentities
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: 925b52a4470c768501dd928784d85a89d05a90c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994598"
---
# <a name="iidentitychangenotifyswitchidentities-method"></a>Iidentitychangenotify:: switchidentities-Methode

\[**Switchidentities** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden.\]

Wird aufgerufen, wenn Benutzer Identitäten gewechselt werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT SwitchIdentities();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Sie können diese Methode implementieren, um benutzerdefiniertes Verhalten für Ihre Anwendung bereitzustellen, wenn ein Benutzer die Identitäten erfolgreich gewechselt hat. Um benutzerdefiniertes Verhalten bereitzustellen, bevor ein Benutzer Identitätswechsel stattfindet, implementieren Sie die [**iidentitychangenotify:: queryswitchidentities**](iidentitychangenotify-queryswitchidentities.md) -Methode.

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

[**Iidentitychangenotify:: queryswitchidentities**](iidentitychangenotify-queryswitchidentities.md)
</dt> </dl>

 

 




