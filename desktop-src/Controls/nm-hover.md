---
title: NM_HOVER Benachrichtigungscode (Commctrl.h)
description: Wird von einem -Steuerelement gesendet, wenn der Mauszeiger auf ein Element zusteuert. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 0eef3e88-c1f0-4f9c-9ccf-580d8e464157
keywords:
- NM_HOVER Benachrichtigungscode Windows-Steuerelemente
topic_type:
- apiref
api_name:
- NM_HOVER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1f5d1332c54328fba1b09ecf4efd48011edbe9a81139f05ad375fb6c8b070de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088700"
---
# <a name="nm_hover-notification-code"></a>NM \_ HOVER-Benachrichtigungscode

Wird von einem -Steuerelement gesendet, wenn der Mauszeiger auf ein Element zusteuert. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
NM_HOVER

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMHDR-Struktur,**](/windows/desktop/api/richedit/ns-richedit-nmhdr) die zusätzliche Informationen zu dieser Benachrichtigung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn nicht anders angegeben, geben Sie 0 (null) zurück, damit das Steuerelement den Mauszeiger normal verarbeiten kann, oder ungleich 0 (null), um zu verhindern, dass der Mauszeiger verarbeitet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





