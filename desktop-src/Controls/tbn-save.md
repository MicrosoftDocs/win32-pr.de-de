---
title: TBN_SAVE Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass gerade eine Symbolleiste gespeichert wird. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 31622f5e-2e33-4a42-8c49-cc3028a6fa62
keywords:
- TBN_SAVE Benachrichtigungscode Windows-Steuerelemente
topic_type:
- apiref
api_name:
- TBN_SAVE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f9d4fb40d0e5beafcd720b4de52a8cf09d17c3e4c6f7b4dcfa8da78e00e97ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876590"
---
# <a name="tbn_save-notification-code"></a>TBN \_ SAVE-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass gerade eine Symbolleiste gespeichert wird. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
TBN_SAVE 

    lpnmtb = (LPNMTBSAVE) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMTBSAVE-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Die Anwendung erhält diesen Benachrichtigungscode einmal zu Beginn des Speichervorgangs und einmal für jede Schaltfläche. Mit diesem Benachrichtigungscode haben Sie die Möglichkeit, ihre eigenen Informationen zu den von der Shell gespeicherten Informationen hinzuzufügen. Wenn Sie keine Informationen hinzufügen möchten, ignorieren Sie den Benachrichtigungscode. Eine ausführlichere Erläuterung zum Umgang mit TBN SAVE finden Sie unter [Symbolleistenanpassung.](toolbar-controls-overview.md) \_

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[TBN \_ RESTORE](tbn-restore.md)
</dt> </dl>

 

 





