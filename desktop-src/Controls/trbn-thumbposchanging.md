---
title: TRBN_THUMBPOSCHANGING Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt, dass sich die Position des Fingerabdrucks auf einer Trackleiste ändert. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 0876e026-bc07-409d-b174-b97ed704fc11
keywords:
- TRBN_THUMBPOSCHANGING Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- TRBN_THUMBPOSCHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48f05f67eb20c78f764957e73d2293d32e88f25a73d44d6b58f9a1c310b8d9d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751040"
---
# <a name="trbn_thumbposchanging-notification-code"></a>TRBN \_ THUMBPOSCHANGING-Benachrichtigungscode

Benachrichtigt, dass sich die Position des Fingerabdrucks auf einer Trackleiste ändert. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
TRBN_THUMBPOSCHANGING

    lpNMTrbThumbPosChanging = (NMTRBTHUMBPOSCHANGING*) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMTRBTHUMBPOSCHANGING-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-nmtrbthumbposchanging) Der Aufrufer ist dafür verantwortlich, diese Struktur zu zuordnen und ihre Member, einschließlich der Member der enthaltenen [**NMHDR-Struktur,**](/windows/desktop/api/richedit/ns-richedit-nmhdr) zu setzen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Geben **Sie TRUE** zurück, um zu verhindern, dass sich der Daumen an die angegebene Position bewegt.

## <a name="remarks"></a>Hinweise

Senden Sie diese Benachrichtigung an Clients, die nicht auf [**WM \_ HSCROLL-**](wm-hscroll.md) oder [**WM \_ VSCROLL-Nachrichten**](wm-vscroll.md) lauschen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





