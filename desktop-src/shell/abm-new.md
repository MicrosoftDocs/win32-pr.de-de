---
description: Registriert eine neue App-Leiste und gibt den Nachrichtenbezeichner an, den das System zum Senden von Benachrichtigungsmeldungen verwenden soll. Eine App-Leiste sollte diese Nachricht senden, bevor andere AppBar-Nachrichten gesendet werden.
ms.assetid: 1da9db13-6fdc-44b3-9985-de32d572675a
title: ABM_NEW (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 400439e6808d40eb74c18fa4219109a0abca1973cdac4dcb9de5154384fd0071
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118460967"
---
# <a name="abm_new-message"></a>ABM \_ NEW-Nachricht

Registriert eine neue App-Leiste und gibt den Nachrichtenbezeichner an, den das System zum Senden von Benachrichtigungsmeldungen verwenden soll. Eine App-Leiste sollte diese Nachricht senden, bevor andere AppBar-Nachrichten gesendet werden.


```C++
fRegistered = (BOOL) SHAppBarMessage(ABM_NEW, pabd); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pabd* 
</dt> <dd>

Ein Zeiger auf eine [**APPBARDATA-Struktur,**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) die das Fensterhand handle und den Meldungsbezeichner der neuen App-Leiste enthält. Sie müssen beim Senden **dieser Nachricht die Member cbSize,** **hWnd** und **uCallbackMessage** angeben. alle anderen Member werden ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, oder **FALSE,** wenn ein Fehler auftritt oder die App-Leiste bereits registriert ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

 




