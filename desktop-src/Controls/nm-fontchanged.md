---
title: NM_FONTCHANGED Benachrichtigungscode (Commctrl.h)
description: Wird von einem Listenansicht-Steuerelement gesendet, wenn das Steuerelement eine Schriftart geändert hat. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: ffa019b0-34be-4bb3-b9dd-c267545fec84
keywords:
- NM_FONTCHANGED Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- NM_FONTCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5369b7719a02e28562f4e71aecffdd3680aa602b6154eac9cc8685bdbe2b2b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411145"
---
# <a name="nm_fontchanged-notification-code"></a>NM \_ FONTCHANGED-Benachrichtigungscode

Wird von einem Listenansicht-Steuerelement gesendet, wenn das Steuerelement eine Schriftart geändert hat. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
NM_FONTCHANGED
        
    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMHDR-Struktur,**](/windows/desktop/api/richedit/ns-richedit-nmhdr) die zusätzliche Informationen zu dieser Benachrichtigung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird vom -Steuerelement ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





