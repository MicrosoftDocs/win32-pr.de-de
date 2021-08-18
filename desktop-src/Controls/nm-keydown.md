---
title: NM_KEYDOWN Benachrichtigungscode (Commctrl.h)
description: 'NM_KEYDOWN Benachrichtigungscode: Wird von einem Steuerelement gesendet, wenn das Steuerelement über den Tastaturfokus verfügt und der Benutzer eine Taste drückt. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.'
ms.assetid: e3b38096-797d-4948-9595-a252cf33dcdd
keywords:
- NM_KEYDOWN Benachrichtigungscode Windows-Steuerelemente
topic_type:
- apiref
api_name:
- NM_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c68dd0eaa82d8a8687aaadaa195e4fba121e7db84031eefe1404ad387748580
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958099"
---
# <a name="nm_keydown-notification-code"></a>NM \_ KEYDOWN-Benachrichtigungscode

Wird von einem -Steuerelement gesendet, wenn das Steuerelement über den Tastaturfokus verfügt und der Benutzer eine Taste drückt. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
NM_KEYDOWN

    lpnmk = (LPNMKEY) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMKEY-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmkey) die zusätzliche Informationen zum Schlüssel enthält, der den Benachrichtigungscode verursacht hat.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert ungleich 0 (null) zurück, um zu verhindern, dass das Steuerelement den Schlüssel verarbeitet, andernfalls 0 (null).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





