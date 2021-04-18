---
title: TVN_SETDISPINFO Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuer Elements, dass die Informationen, die für ein Element verwaltet werden, aktualisiert werden müssen. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 40fa61bc-c043-4001-ada9-b627d68bd737
keywords:
- Windows-Steuerelemente für TVN_SETDISPINFO Benachrichtigungs
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
ms.openlocfilehash: 9b03e60ba7d8e6d7851c62fac030bd252cf957d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338125"
---
# <a name="tvn_setdispinfo-notification-code"></a>TVN \_ setdispinfo-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuer Elements, dass die Informationen, die für ein Element verwaltet werden, aktualisiert werden müssen. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
TVN_SETDISPINFO 

    lptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) -Struktur, die das zu Aktualisier Ende Element beschreibt. Der **Hitem** -Member der [**tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema) -Struktur gibt das Element an, das aktualisiert wird, und der **Mask** -Member gibt an, welche Attribute des Elements aktualisiert werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="remarks"></a>Bemerkungen

Wenn der **pszText** -Member der [**tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema) -Struktur des Elements der LPSTR- \_ textcallback-Wert ist, sendet das Steuerelement diese Benachrichtigung, um den Text des Elements festzulegen. In diesem Fall wird für das **Mask** -Member von *LPARAM* das tvif- \_ textflag festgelegt.

Wenn das **iImage** -oder **iSelectedImage** -Element der [**tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema) -Struktur des Elements der I \_ imagecallback-Wert ist, sendet das Steuerelement diese Benachrichtigung, um den Index des anzuzeigenden Symbol Bilds abzurufen. In diesem Fall wird für das **Masken** Element von *LPARAM* das tvif- \_ Image oder das tvif \_ SelectedImage-Flag festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TVN \_ Setdispinfow** (Unicode) und **TVN \_ setdispinfoa** (ANSI)<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema)
</dt> <dt>

[**Tvitemex**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa)
</dt> <dt>

[TVN \_ getdispinfo](tvn-getdispinfo.md)
</dt> </dl>

 

 





