---
title: TVN_ITEMCHANGING Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster eines Strukturansichtssteuerelements, dass sich Elementattribute ändern werden. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: c997871c-8eca-46c0-999d-2f6d7e3e6c96
keywords:
- TVN_ITEMCHANGING Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- TVN_ITEMCHANGING
- TVN_ITEMCHANGINGA
- TVN_ITEMCHANGINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85416e22562720455da3e3c03c95b3cee25b5f0f7420a31250b244f47dab0caa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957869"
---
# <a name="tvn_itemchanging-notification-code"></a>TVN \_ ITEMCHANGING-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster eines Strukturansichtssteuerelements, dass sich Elementattribute ändern werden. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
TVN_ITEMCHANGING
        
    pnm = (NMTVITEMCHANGE *) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMTVITEMCHANGE-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) die das geänderte Element beschreibt. Das **uChanged-Member** ist auf TVIF \_ STATE festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **FALSE zurück,** um die Änderung zu akzeptieren, oder **TRUE,** um die Änderung zu verhindern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TVN \_ ITEMCHANGINGW** (Unicode) und **TVN \_ ITEMCHANGINGA** (ANSI)<br/>         |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[TVN \_ ITEMCHANGED](tvn-itemchanged.md)
</dt> </dl>

 

 





