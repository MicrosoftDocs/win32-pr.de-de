---
title: TVN_BEGINDRAG Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuerelements, dass ein Drag & Drop-Vorgang mit der linken Maustaste initiiert wird. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: e118354a-329e-424c-b137-78342cc00957
keywords:
- TVN_BEGINDRAG Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- TVN_BEGINDRAG
- TVN_BEGINDRAGA
- TVN_BEGINDRAGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95952ee42dfe8eb8dd1a46c66dcd452f41cbc9723fa175c2a0d1fc75056c31ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957919"
---
# <a name="tvn_begindrag-notification-code"></a>TVN \_ BEGINDRAG-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuerelements, dass ein Drag & Drop-Vorgang mit der linken Maustaste initiiert wird. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
TVN_BEGINDRAG 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMTREEVIEW-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) Das **itemNew-Element** ist eine [**TVITEM-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-tvitema) die gültige Informationen über das Element enthält, das in die **Elemente hItem,** **state** und **lParam gezogen** wird. Das **ptDrag-Element** gibt die aktuellen Bildschirmkoordinaten der Maus an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="remarks"></a>Hinweise

Ein Strukturansicht-Steuerelement, das über den [**TVS \_ DISABLEDRAGDROP-Stil**](tree-view-control-window-styles.md) verfügt, sendet diesen Benachrichtigungscode nicht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TVN \_ BEGINDRAGW** (Unicode) und **TVN \_ BEGINDRAGA** (ANSI)<br/>               |



 

 





