---
title: TVN_GETDISPINFO Benachrichtigungs Code (kommctrl. h)
description: Fordert an, dass das übergeordnete Fenster eines Strukturansicht-Steuer Elements Informationen bereitstellt, die zum Anzeigen oder Sortieren eines Elements erforderlich sind. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 2dfe41d8-1164-481b-ac07-8faba43c562a
keywords:
- Windows-Steuerelemente für TVN_GETDISPINFO Benachrichtigungs
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
ms.openlocfilehash: 2a09bcc683ba9cf2d89a796e63812381254588a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517828"
---
# <a name="tvn_getdispinfo-notification-code"></a>TVN \_ getdispinfo-Benachrichtigungs Code

Fordert an, dass das übergeordnete Fenster eines Strukturansicht-Steuer Elements Informationen bereitstellt, die zum Anzeigen oder Sortieren eines Elements erforderlich sind. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
TVN_GETDISPINFO 

    lptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) -Struktur. Das **Element Element** ist eine [**tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema) -Struktur, deren " **Mask**", " **Hitem**", " **State**" und " **LPARAM** "-Member den Typ der erforderlichen Informationen angeben. Sie müssen die Elemente der Struktur mit den entsprechenden Informationen auffüllen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="remarks"></a>Bemerkungen

Dieser Benachrichtigungs Code wird in den folgenden Situationen gesendet:

-   Wenn der **pszText** -Member der [**tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema) -Struktur des Elements der LPSTR- \_ textcallback-Wert ist, sendet das Steuerelement diesen Benachrichtigungs Code, um den Text des Elements abzurufen. In diesem Fall wird für das **Mask** -Member von *LPARAM* das tvif- \_ textflag festgelegt.
-   Wenn das **iImage** -oder **iSelectedImage** -Element der [**tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema) -Struktur des Elements der I \_ imagecallback-Wert ist, sendet das Steuerelement diesen Benachrichtigungs Code, um den Index der Symbole eines Elements in der Bildliste des Steuer Elements abzurufen. In diesem Fall wird das tvif SelectedImage-Flag für das **Masken** Element von *LPARAM* festgelegt, wenn das Element ausgewählt ist \_ . Wenn das Element nicht ausgewählt ist, wird für das **Mask** -Member von *LPARAM* das tvif- \_ bildflag festgelegt.
-   Wenn das **cChildren** -Element der [**tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema) -Struktur des Elements der I \_ Children encallback-Wert ist, sendet das Steuerelement diesen Benachrichtigungs Code, um einen Wert abzurufen, der angibt, ob das Element über untergeordnete Elemente verfügt. In diesem Fall wird für das **Mask** -Member von *LPARAM* das Flag "tvif \_ Children" festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TVN \_ Getdispinfow** (Unicode) und **TVN \_ getdispinfoa** (ANSI)<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[TVN \_ setdispinfo](tvn-setdispinfo.md)
</dt> </dl>

 

 





