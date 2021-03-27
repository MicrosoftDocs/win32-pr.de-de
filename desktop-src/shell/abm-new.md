---
description: Registriert eine neue appbar und gibt die Nachrichten-ID an, die vom System zum Senden von Benachrichtigungs Meldungen verwendet werden soll. Diese Nachricht sollte von einer appbar gesendet werden, bevor andere appbar-Meldungen gesendet werden.
ms.assetid: 1da9db13-6fdc-44b3-9985-de32d572675a
title: ABM_NEW Meldung (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fad11e6712d0afd0c1a5e9de07fd3d690800db13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750312"
---
# <a name="abm_new-message"></a>\_Neue Nachricht ABM

Registriert eine neue appbar und gibt die Nachrichten-ID an, die vom System zum Senden von Benachrichtigungs Meldungen verwendet werden soll. Diese Nachricht sollte von einer appbar gesendet werden, bevor andere appbar-Meldungen gesendet werden.


```C++
fRegistered = (BOOL) SHAppBarMessage(ABM_NEW, pabd); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pabd* 
</dt> <dd>

Ein Zeiger auf eine [**appbardata**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) -Struktur, die das Fenster Handle und den Meldungs Bezeichner der neuen App-Leiste enthält. Sie müssen die Member **CBSIZE**, **HWND** und **ucallbackmessage** angeben, wenn diese Nachricht gesendet wird. alle anderen Member werden ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, oder **false** , wenn ein Fehler auftritt oder die appbar bereits registriert ist.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

 




