---
title: TBN_RESET Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster der Symbolleiste, dass der Benutzer den Inhalt des Dialogfelds Symbolleiste anpassen zurückgesetzt hat. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 55efba85-b453-48b9-83df-76820249e7a8
keywords:
- TBN_RESET Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- TBN_RESET
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7852ee64dcf741dd291965e86d3d73f6113c1c8270bfa948d8d547fa99b9c01
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876620"
---
# <a name="tbn_reset-notification-code"></a>TBN \_ RESET-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster der Symbolleiste, dass der Benutzer den Inhalt des Dialogfelds Symbolleiste anpassen zurückgesetzt hat. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
TBN_RESET 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMHDR-Struktur,**](/windows/desktop/api/richedit/ns-richedit-nmhdr) die Informationen zum Benachrichtigungscode enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Geben Sie TBNRF \_ ENDCUSTOMIZE zurück, um das Dialogfeld Symbolleiste anpassen zu schließen. Alle anderen Rückgabewerte werden ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





