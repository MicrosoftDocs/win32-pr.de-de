---
title: NM_SETCURSOR (Strukturansicht) Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuerelements, dass das Steuerelement den Cursor als Reaktion auf eine WM \_ SETCURSOR-Meldung anordnt. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 2b2f2e90-edef-484d-b67a-12983a1cde29
keywords:
- NM_SETCURSOR -Benachrichtigungscode (Strukturansicht) Windows Controls
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
ms.openlocfilehash: b7791ff62fa9ed097052ebd38dae0000d7165519133527044e9716bb7e39c655
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118410457"
---
# <a name="nm_setcursor-tree-view-notification-code"></a>NM \_ SETCURSOR-Benachrichtigungscode (Strukturansicht)

Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuerelements, dass das Steuerelement den Cursor als Reaktion auf eine [**WM \_ SETCURSOR-Meldung anordnt.**](/windows/desktop/menurc/wm-setcursor) Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
NM_SETCURSOR

    lpnmm = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMMOUSE-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) die zusätzliche Informationen zu dieser Benachrichtigung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Geben Sie 0 (null) zurück, damit das Steuerelement den Cursor oder ungleich 0 (null) festlegen kann, um zu verhindern, dass der Cursor vom Steuerelement festgelegt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

