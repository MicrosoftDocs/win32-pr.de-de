---
title: TBN_QUERYINSERT Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster der Symbolleiste, ob eine Schaltfläche links von der angegebenen Schaltfläche eingefügt werden kann, während der Benutzer eine Symbolleiste andefiniert. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: d389fabb-16f6-43aa-a4b6-abb80723345b
keywords:
- TBN_QUERYINSERT Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- TBN_QUERYINSERT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44f741fd7cfa5c6f72405b10ba9678aed71f7cb2359743593f117b17c8ad1c8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166960"
---
# <a name="tbn_queryinsert-notification-code"></a>TBN \_ QUERYINSERT-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster der Symbolleiste, ob eine Schaltfläche links von der angegebenen Schaltfläche eingefügt werden kann, während der Benutzer eine Symbolleiste andefiniert. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
TBN_QUERYINSERT 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMTOOLBAR-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) Das **iItem** -Member enthält den nullbasierten Index der einzufügenden Schaltfläche.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Geben **Sie TRUE** zurück, damit eine Schaltfläche vor der angegebenen Schaltfläche eingefügt werden kann, oder **FALSE,** um zu verhindern, dass die Schaltfläche eingefügt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





