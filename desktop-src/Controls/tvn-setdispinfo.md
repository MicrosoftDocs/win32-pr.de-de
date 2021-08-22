---
title: TVN_SETDISPINFO Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster eines Strukturansichtssteuerelements, dass es die Informationen aktualisieren muss, die es über ein Element verwaltet. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 40fa61bc-c043-4001-ada9-b627d68bd737
keywords:
- TVN_SETDISPINFO Benachrichtigungscode Windows-Steuerelemente
topic_type:
- apiref
api_name:
- TVN_SETDISPINFO
- TVN_SETDISPINFOA
- TVN_SETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e88a9b5fed4260fa88f5f40431113456950d99985ad2f2e0e97c2e951dce96bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957769"
---
# <a name="tvn_setdispinfo-notification-code"></a>TVN \_ SETDISPINFO-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster eines Strukturansichtssteuerelements, dass es die Informationen aktualisieren muss, die es über ein Element verwaltet. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
TVN_SETDISPINFO 

    lptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMTVDISPINFO-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) die das zu aktualisierende Element beschreibt. Der **hItem-Member** der [**TVITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-tvitema) gibt das zu aktualisierende Element an, und der **Maskenmember** gibt an, welche Attribute des Elements aktualisiert werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="remarks"></a>Hinweise

Wenn der **pszText-Member** der [**TVITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-tvitema) des Elements der LPSTR \_ TEXTCALLBACK-Wert ist, sendet das Steuerelement diese Benachrichtigung, um den Text des Elements festzulegen. In diesem Fall wird für den **Maskenmember** von *lParam* das TVIF \_ TEXT-Flag festgelegt.

Wenn der **iImage-** oder **iSelectedImage-Member** der [**TVITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-tvitema) des Elements der I \_ IMAGECALLBACK-Wert ist, sendet das Steuerelement diese Benachrichtigung, um den Index des anzuzeigende Symbolbilds abzurufen. In diesem Fall wird für den **Maskenmember** von *lParam* das FLAG TVIF \_ IMAGE oder TVIF \_ SELECTEDIMAGE festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TVN \_ SETDISPINFOW** (Unicode) und **TVN \_ SETDISPINFOA** (ANSI)<br/>           |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)
</dt> <dt>

[**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa)
</dt> <dt>

[TVN \_ GETDISPINFO](tvn-getdispinfo.md)
</dt> </dl>

 

 





