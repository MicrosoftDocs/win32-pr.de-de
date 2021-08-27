---
title: LVN_ITEMACTIVATE Benachrichtigungscode (Commctrl.h)
description: Wird von einem Listenansichtssteuerelement gesendet, wenn der Benutzer ein Element aktiviert. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 475c8e6a-8e2e-4182-8ccc-a4bc6fc891a8
keywords:
- LVN_ITEMACTIVATE Benachrichtigungscode Windows Controls
topic_type:
- apiref
api_name:
- LVN_ITEMACTIVATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f21b02406157a13d2fcf110c15e692211b26b3f9da31741489e317e6b2c68309
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105050"
---
# <a name="lvn_itemactivate-notification-code"></a>LVN \_ ITEMACTIVATE-Benachrichtigungscode

Wird von einem Listenansichtssteuerelement gesendet, wenn der Benutzer ein Element aktiviert. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
LVN_ITEMACTIVATE

#if (_WIN32_IE >= 0x0400)
    lpnmia = (LPNMITEMACTIVATE)lParam;
#else
    lpnm = (LPNMHDR)lParam;
#endif
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

[Version 4.71.](common-control-versions.md) Zeiger auf eine [**NMITEMACTIVATE-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) die Informationen zu diesem Benachrichtigungscode enthält.

[Version 4.70](common-control-versions.md) und früher. Zeiger auf eine [**NMHDR-Struktur,**](/windows/desktop/api/richedit/ns-richedit-nmhdr) die Informationen zu diesem Benachrichtigungscode enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Anwendung, die diesen Benachrichtigungscode empfängt, muss 0 (null) zurückgeben.

## <a name="remarks"></a>Hinweise

Um die aktivierten Elemente abzurufen, sollte die empfangende Anwendung die [**LVM \_ GETSELECTEDCOUNT-Nachricht**](lvm-getselectedcount.md) verwenden, um die Anzahl der ausgewählten Elemente abzurufen und dann die [**LVM \_ GETNEXTITEM-Nachricht**](lvm-getnextitem.md) mit **LVNI \_ SELECTED** zu senden, bis alle Elemente abgerufen wurden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





