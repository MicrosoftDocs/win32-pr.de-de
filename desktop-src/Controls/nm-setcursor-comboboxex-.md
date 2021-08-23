---
title: NM_SETCURSOR -Benachrichtigungscode (ComboBoxEx) (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster eines ComboBoxEx-Steuerelements, dass das -Steuerelement den Cursor als Reaktion auf eine WM \_ SETCURSOR-Meldung anordnt. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: a1c617fa-8eb2-444f-88d1-9913de7a42d1
keywords:
- NM_SETCURSOR -Benachrichtigungscode (ComboBoxEx) Windows Controls
topic_type:
- apiref
api_name:
- NM_SETCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa0f7c7ffc8459ae1da279b6e53329f894662dd6ae6f30888fd9bdbdf631fa8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119798990"
---
# <a name="nm_setcursor-comboboxex-notification-code"></a>NM \_ SETCURSOR -Benachrichtigungscode (ComboBoxEx)

Benachrichtigt das übergeordnete Fenster eines ComboBoxEx-Steuerelements, dass das -Steuerelement den Cursor als Reaktion auf eine [**WM \_ SETCURSOR-Meldung anordnt.**](/windows/desktop/menurc/wm-setcursor) Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
NM_SETCURSOR

    lpnmm = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMMOUSE-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) die zusätzliche Informationen zu dieser Benachrichtigung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Geben Sie 0 (null) zurück, damit das Steuerelement den Cursor oder ungleich 0 (null) festlegen kann, um zu verhindern, dass der Cursor vom Steuerelement festgelegt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

