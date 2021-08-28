---
title: NM_RCLICK -Benachrichtigungscode (Statusleiste) (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster eines Statusleisten-Steuerelements, dass der Benutzer auf die rechte Maustaste innerhalb des Steuerelements geklickt hat. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 9a441d32-f4e4-42ae-877f-17079b0188f4
keywords:
- NM_RCLICK -Benachrichtigungscode (Statusleiste) Windows-Steuerelemente
topic_type:
- apiref
api_name:
- NM_RCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8a42be8d41552173ef458d2f2c4e6232aa033aebfccd878142ac21b7f69f01b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799050"
---
# <a name="nm_rclick-status-bar-notification-code"></a>NM \_ RCLICK-Benachrichtigungscode (Statusleiste)

Benachrichtigt das übergeordnete Fenster eines Statusleisten-Steuerelements, dass der Benutzer auf die rechte Maustaste innerhalb des Steuerelements geklickt hat. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
NM_RCLICK

    lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMMOUSE-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) die zusätzliche Informationen zu dieser Benachrichtigung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, um anzugeben, dass der Mausklick verarbeitet wurde, und unterdrückt die Standardverarbeitung durch das System. Gibt **FALSE** zurück, um die Standardverarbeitung des Klicks zuzulassen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





