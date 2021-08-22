---
title: NM_CHAR Benachrichtigungscode (Commctrl.h)
description: Der NM \_ CHAR-Benachrichtigungscode wird von einem -Steuerelement gesendet, wenn ein Zeichenschlüssel verarbeitet wird. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: b750f2a6-8642-4d76-96bb-bf58b00cd5c4
keywords:
- NM_CHAR Benachrichtigungscode Windows Controls
topic_type:
- apiref
api_name:
- NM_CHAR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73c35871410244bfb69f67c7e0b2c960d0dd50d432ad9cdcfd8765c7df449bf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018948"
---
# <a name="nm_char-notification-code"></a>NM \_ CHAR-Benachrichtigungscode

Der NM \_ CHAR-Benachrichtigungscode wird von einem -Steuerelement gesendet, wenn ein Zeichenschlüssel verarbeitet wird. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
NM_CHAR

    lpnmc = (LPNMCHAR) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMCHAR-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmchar) die zusätzliche Informationen über das Zeichen enthält, das den Benachrichtigungscode verursacht hat.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird von den meisten Steuerelementen ignoriert. Weitere Informationen finden Sie in der Dokumentation zu den einzelnen Steuerelementen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[NM \_ CHAR (Symbolleiste)](nm-char-toolbar.md)
</dt> </dl>

 

 





