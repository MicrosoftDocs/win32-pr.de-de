---
title: NM_HOVER -Benachrichtigungscode (Listenansicht) (Commctrl.h)
description: Wird von einem Listenansichtssteuerelement gesendet, wenn der Mauszeiger auf ein Element zeigt. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 0d4a2eee-9c98-43d1-bc05-226d91c0480a
keywords:
- NM_HOVER -Benachrichtigungscode (Listenansicht) Windows-Steuerelemente
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
ms.openlocfilehash: fb380e96e579e5e740678a4fa91270c510e7ca01c3596a68cdac02eedd3f1da8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411134"
---
# <a name="nm_hover-list-view-notification-code"></a>\_NM-HOVER-Benachrichtigungscode (Listenansicht)

Wird von einem Listenansichtssteuerelement gesendet, wenn der Mauszeiger auf ein Element zeigt. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
NM_HOVER

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMHDR-Struktur,**](/windows/desktop/api/richedit/ns-richedit-nmhdr) die zusätzliche Informationen zu dieser Benachrichtigung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, damit die Listenansicht den Mauszeiger normal verarbeiten kann, oder ungleich 0 (null), um zu verhindern, dass der Mauszeiger verarbeitet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





