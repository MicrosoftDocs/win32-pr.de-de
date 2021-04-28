---
title: NM_KEYDOWN Benachrichtigungscode (Commctrl.h)
description: 'NM_KEYDOWN Benachrichtigungscode: Wird von einem Steuerelement gesendet, wenn das Steuerelement den Tastaturfokus besitzt und der Benutzer eine Taste drückt. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.'
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
ms.openlocfilehash: ce595378995e41fd8a0f481d7470c8cf791f6379
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112348"
---
# <a name="nm_keydown-notification-code"></a>NM \_ KEYDOWN-Benachrichtigungscode

Wird von einem Steuerelement gesendet, wenn das Steuerelement den Tastaturfokus besitzt und der Benutzer eine Taste drückt. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
NM_KEYDOWN

    lpnmk = (LPNMKEY) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMKEY-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmkey) die zusätzliche Informationen über den Schlüssel enthält, der den Benachrichtigungscode verursacht hat.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert ungleich 0 (null) zurück, um zu verhindern, dass das Steuerelement den Schlüssel verarbeitet, andernfalls 0 (null).

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





