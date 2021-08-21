---
title: TBN_QUERYDELETE Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster der Symbolleiste, ob eine Schaltfläche von einer Symbolleiste gelöscht werden kann, während der Benutzer die Symbolleiste andefiniert. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: fa6a8fe4-a9a3-4c59-9237-d28bd34d664c
keywords:
- TBN_QUERYDELETE Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- TBN_QUERYDELETE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a01d1322ce8461c5cdb53fc76cfc220bbb5d292dedbe589d8b6ada5a48756d55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077884"
---
# <a name="tbn_querydelete-notification-code"></a>TBN \_ QUERYDELETE-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster der Symbolleiste, ob eine Schaltfläche von einer Symbolleiste gelöscht werden kann, während der Benutzer die Symbolleiste andefiniert. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
TBN_QUERYDELETE 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMTOOLBAR-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) Das **iItem** -Member enthält den nullbasierten Index der zu löschenden Schaltfläche.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** damit die Schaltfläche gelöscht werden kann, oder **FALSE,** um zu verhindern, dass die Schaltfläche gelöscht wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





