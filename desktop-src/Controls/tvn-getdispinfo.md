---
title: TVN_GETDISPINFO Benachrichtigungscode (Commctrl.h)
description: Fordert an, dass das übergeordnete Fenster eines Strukturansichtssteuerelements Informationen enthält, die zum Anzeigen oder Sortieren eines Elements erforderlich sind. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 2dfe41d8-1164-481b-ac07-8faba43c562a
keywords:
- TVN_GETDISPINFO Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- TVN_GETDISPINFO
- TVN_GETDISPINFOA
- TVN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59728c816ee3fe7dac46c12d7e62da6c18cfdad8387f03d3861e63792d9c8f66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059910"
---
# <a name="tvn_getdispinfo-notification-code"></a>TVN \_ GETDISPINFO-Benachrichtigungscode

Fordert an, dass das übergeordnete Fenster eines Strukturansichtssteuerelements Informationen enthält, die zum Anzeigen oder Sortieren eines Elements erforderlich sind. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
TVN_GETDISPINFO 

    lptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMTVDISPINFO-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) Das **Elementelement** ist eine [**TVITEM-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-tvitema) deren Masken-, **hItem-,** **Zustands-** und **lParam-Member** den erforderlichen Informationstyp angeben. Sie müssen die Member der -Struktur mit den entsprechenden Informationen füllen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="remarks"></a>Hinweise

Dieser Benachrichtigungscode wird unter den folgenden Umständen gesendet:

-   Wenn das **pszText-Element** der [**TVITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-tvitema) des Elements der LPSTR TEXTCALLBACK-Wert ist, sendet das Steuerelement diesen Benachrichtigungscode, um den Text des Elements \_ abzurufen. In diesem Fall wird für **das Maskenmitglied** *von lParam* das FLAG TVIF \_ TEXT festgelegt.
-   Wenn das **iImage-** oder **iSelectedImage-Element** der [**TVITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-tvitema) des Elements der I IMAGECALLBACK-Wert ist, sendet das Steuerelement diesen Benachrichtigungscode, um den Index der Symbole eines Elements in der Bildliste des Steuerelements \_ abzurufen. Wenn in diesem Fall das Element ausgewählt ist, wird für das **Maskenelement** von *lParam* das FLAG TVIF \_ SELECTEDIMAGE festgelegt. Wenn das Element nicht ausgewählt ist, wird für **das Maskenelement** von *lParam* das TVIF \_ IMAGE-Flag festgelegt.
-   Wenn das **cChildren-Element** der [**TVITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-tvitema) des Elements der I CHILDRENCALLBACK-Wert ist, sendet das Steuerelement diesen Benachrichtigungscode, um einen Wert abzurufen, der angibt, ob das Element über \_ untergeordnete Elemente verfügt. In diesem Fall wird für **das Maskenmitglied** *von lParam* das FLAG TVIF \_ CHILDREN festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TVN \_ GETDISPINFOW** (Unicode) und **TVN \_ GETDISPINFOA** (ANSI)<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[TVN \_ SETDISPINFO](tvn-setdispinfo.md)
</dt> </dl>

 

 





